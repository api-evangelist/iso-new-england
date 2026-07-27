---
name: Pull historical ISO New England locational marginal prices
description: Retrieve day-ahead and real-time locational marginal prices for a given day, hour or location from the ISO New England Web Services API v1.1, and know when to use the anonymous bulk CSV files instead.
api: openapi/iso-new-england-web-services-openapi.yml
generated: '2026-07-27'
method: generated
operations:
  - getHourlylmpDaFinalDayByDay
  - getHourlylmpDaFinalDayByDayLocationByLocationId
  - getHourlylmpDaFinalDayByDayHourBySh
  - getHourlylmpRtFinalDayByDay
  - getHourlylmpRtPrelimCurrent
  - getFiveminutelmpDayByDayLocationByLocationId
  - getHourlylmpDaFinalInfo
  - getDayaheadconstraintsDayByDay
---

# Pull historical ISO New England locational marginal prices

Use this for price analysis over a past day, hour or location - backtests, settlement checks, or
congestion studies.

## Before you call

- Base path `https://webservices.iso-ne.com/api/v1.1`, HTTP Basic over TLS with ISO Express
  credentials, `.json` extension or `Accept: application/json`. Anonymous calls return 401.
- Date parameters are strict: **day = `YYYYMMDD`**, month = `YYYYMM`, year = `YYYY`. Hour parameters
  (`sh`, start hour) follow the market hour convention of the feed.
- Location ids come from `getLocationsAll`; `4000` = Hub, `4001`-`4008` = load zones.

## Choose the right price series

| Series | Operation | Path |
|---|---|---|
| Day-ahead hourly, final | `getHourlylmpDaFinalDayByDay` | `/hourlylmp/da/final/day/{day}` |
| Day-ahead hourly, one location | `getHourlylmpDaFinalDayByDayLocationByLocationId` | `/hourlylmp/da/final/day/{day}/location/{locationId}` |
| Day-ahead hourly, one hour | `getHourlylmpDaFinalDayByDayHourBySh` | `/hourlylmp/da/final/day/{day}/hour/{sh}` |
| Real-time hourly, final | `getHourlylmpRtFinalDayByDay` | `/hourlylmp/rt/final/day/{day}` |
| Real-time hourly, preliminary (current) | `getHourlylmpRtPrelimCurrent` | `/hourlylmp/rt/prelim/current` |
| Real-time five-minute, one day and location | `getFiveminutelmpDayByDayLocationByLocationId` | `/fiveminutelmp/day/{day}/location/{locationId}` |

**Preliminary vs final matters.** `rt/prelim` is the fast, unsettled series; `rt/final` is the
settled one. Never mix them in a single time series, and always label which one you used.

## Steps

1. Check freshness/availability with the matching `/info` operation - e.g. `getHourlylmpDaFinalInfo`
   (`GET /hourlylmp/da/final/info.json`) - before pulling a day.
2. Pull the day. The five-minute feeds document a limited retention window ("only the past N days
   are supported") - if a historical day returns nothing, that is the window, not a bug.
3. To explain a price spike, pull the constraints for the same day with
   `getDayaheadconstraintsDayByDay` (`GET /dayaheadconstraints/day/{day}.json`) and correlate
   `ConstraintName` / `ContingencyName` / `MarginalValue` with the `CongestionComponent` of the LMP.
4. Decompose each row: `LmpTotal = EnergyComponent + CongestionComponent + LossComponent`.

## When NOT to use the API

For bulk history - a whole month of nodal prices, or a multi-year backfill - use ISO Express report
files instead. They download **anonymously**, no account required, as CSV:

- Report trees: `https://www.iso-ne.com/isoexpress/web/reports/pricing/-/tree/lmps-da-hourly`
- One file per operating day, e.g.
  `https://www.iso-ne.com/static-transform/csv/histRpts/da-lmp/WW_DALMP_ISO_YYYYMMDD.csv`
  (verified 2026-07-27: HTTP 200, 2.46 MB of text/csv for a single day's full nodal set).

The API is the per-resource, credentialed path; ISO Express is the bulk, anonymous path. Both carry
the same public data.

## Errors and honesty rules

- 401 = credentials; 404 = unknown path or no data at that address. No `problem+json`, no error codes.
- An empty element is a real answer for a day with no publication.
- Prices are wholesale $/MWh at pricing nodes. Do not present them as retail rates or as a bill.
