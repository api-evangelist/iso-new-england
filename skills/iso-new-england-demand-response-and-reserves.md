---
name: Track ISO New England demand response and operating reserves
description: Follow demand-response dispatch instructions, price-response events, real-time demand-response prices and operating-reserve pricing from the ISO New England Web Services API v1.1.
api: openapi/iso-new-england-web-services-openapi.yml
generated: '2026-07-27'
method: generated
operations:
  - getDrdispatchCurrent
  - getDrdispatchCurrentLocationByLocationId
  - getDrdispatchDayByDay
  - getDrtpCurrent
  - getDrtpDayByDay
  - getPricerespeventCurrent
  - getPricerespeventMonthByMonth
  - getFiveminutereservepriceCurrent
  - getDaasreservedataCurrent
---

# Track ISO New England demand response and operating reserves

Use this when an agent must know whether demand resources are being dispatched right now, what
demand response is being paid, and how operating reserves are pricing.

## Before you call

- Base path `https://webservices.iso-ne.com/api/v1.1`, HTTP Basic over TLS with ISO Express
  credentials, `.json` extension. Anonymous calls return 401.
- `day` = `YYYYMMDD`, `month` = `YYYYMM`. Location ids come from `getLocationsAll`; demand-response
  aggregation zones appear in that registry as `DRRAZ` / `DRR AGGREGATION ZONE` location types.

## Steps

1. **Is anything dispatched now?** - `getDrdispatchCurrent` (`GET /drdispatch/current.json`), or
   `getDrdispatchCurrentLocationByLocationId`
   (`GET /drdispatch/current/location/{locationId}.json`) for one zone. An empty element means no
   dispatch is active - report that as the answer, not as an error.
2. **What happened on a given day?** - `getDrdispatchDayByDay`
   (`GET /drdispatch/day/{day}.json`).
3. **Demand response prices** - `getDrtpCurrent` (`GET /drtp/current.json`) and `getDrtpDayByDay`
   (`GET /drtp/day/{day}.json`). A per-resource detail view exists at `/drtp/detail/day/{day}`.
4. **Price-response events** - `getPricerespeventCurrent` (`GET /pricerespevent/current.json`) for
   an active event, `getPricerespeventMonthByMonth` (`GET /pricerespevent/month/{month}.json`) for a
   month of history.
5. **Reserve pricing** - `getFiveminutereservepriceCurrent`
   (`GET /fiveminutereserveprice/current.json`) for real-time operating-reserve prices, and
   `getDaasreservedataCurrent` (`GET /daasreservedata/current.json`) for Day-Ahead Ancillary
   Services Market reserve data. Reserve zones are `7000` Rest Of System, `7001` Southwest
   Connecticut, `7002` Connecticut, `7003` NEMA/Boston.

## Interpreting the answer

- Correlate a dispatch with system tightness: pull `getMorningreportCurrent` for available capacity
  and `getFiveminutesystemloadCurrent` for load before saying *why* resources were called.
- Every one of these resources has an `/info` sibling returning `CreationDate` and
  `LatestBeginDate`; poll it rather than re-pulling the feed.

## Honesty rules for the agent

- Dispatch instructions are operational signals to market participants, not advice to consumers.
  ISO New England has no retail relationship and this API carries no household or premise data.
- An empty result is a real state of the system (nothing dispatched, no event). Never fill the gap
  with an earlier interval or an estimate.
- 401 = credentials, 404 = no data at that address. No `problem+json`, no error-code registry -
  see `errors/iso-new-england-problem-types.yml`.
