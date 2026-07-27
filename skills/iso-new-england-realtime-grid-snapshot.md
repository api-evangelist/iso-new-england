---
name: ISO New England real-time grid snapshot
description: Pull a complete current picture of the New England power system - system load, generation fuel mix, five-minute LMPs and the hourly load forecast - from the ISO New England Web Services API v1.1.
api: openapi/iso-new-england-web-services-openapi.yml
generated: '2026-07-27'
method: generated
operations:
  - getFiveminutesystemloadCurrent
  - getGenfuelmixCurrent
  - getFiveminutelmpCurrent
  - getFiveminutelmpCurrentLocationByLocationId
  - getHourlyloadforecastCurrent
  - getFiveminutelmpInfo
  - getLocationsAll
---

# ISO New England real-time grid snapshot

Use this when an agent needs the current state of the New England grid: how much load there is,
what is generating it, what power costs right now, and what is expected next.

## Before you call

- **Base path**: `https://webservices.iso-ne.com/api/v1.1`
- **Auth**: HTTP Basic over TLS with ISO Express credentials. Send
  `Authorization: Basic base64(user:password)`. Anonymous calls return **401** - there is no
  anonymous mode and no API key. Get credentials free at <https://www.iso-ne.com/signup>.
- **Format**: append `.json` to any path (or send `Accept: application/json`). XML is the default.
- **JSON shape**: XML attributes come back as `"@name"` and element text as `"$"`. A plural wrapper
  holds the rows, e.g. `{"FiveMinLmps": {"FiveMinLmp": [ ... ]}}`. A single result may be an object
  rather than an array - always normalise before iterating.

## Steps

1. **System load** - `getFiveminutesystemloadCurrent` (`GET /fiveminutesystemload/current.json`).
   Returns `LoadMw`, `NativeLoad`, `SystemLoadBtmPv`, `NativeLoadBtmPv`, `ArdDemand` and `BeginDate`.
   `*BtmPv` values include behind-the-meter photovoltaic estimates; say which one you are quoting.
2. **Fuel mix** - `getGenfuelmixCurrent` (`GET /genfuelmix/current.json`). One row per fuel category
   with `GenMw`, `FuelCategory`, `FuelCategoryRollup` and `MarginalFlag`. `MarginalFlag: "Y"` marks
   the fuels setting price at that instant. Categories are Batteries, Coal, Hydro, Natural Gas,
   Nuclear, Oil and Renewables (Batteries was added in May 2026).
3. **Prices** - `getFiveminutelmpCurrent` (`GET /fiveminutelmp/current.json`) for every location, or
   `getFiveminutelmpCurrentLocationByLocationId` (`GET /fiveminutelmp/current/location/{locationId}.json`)
   for one. `4000` is the Hub; `4001`-`4008` are the eight load zones. Each row splits
   `LmpTotal` into `EnergyComponent`, `CongestionComponent` and `LossComponent` - report the total
   unless asked for the decomposition.
4. **Forecast** - `getHourlyloadforecastCurrent` (`GET /hourlyloadforecast/current.json`) for the
   forward hourly load forecast with its `CreationDate`.
5. **Resolve location ids** - `getLocationsAll` (`GET /locations/all.json`) returns the full registry
   (1,302 entries as of 2026-07-27) with `LocationID`, `LocationName`, `LocationType`, `AreaType`.
   Cache it; do not hard-code ids beyond the well-known zone numbers. Some internal nodes have opted
   out of publishing by rule.

## Freshness and polling

- Every resource has an `/info` sibling - `getFiveminutelmpInfo` (`GET /fiveminutelmp/info.json`)
  returns `ServiceInfo.CreationDate` and `ServiceInfo.LatestBeginDate`. Poll `/info` first and skip
  the full pull when `LatestBeginDate` has not advanced.
- Five-minute feeds advance every five minutes; hourly feeds hourly. ISO New England documents no
  rate limit and returns no rate-limit headers - poll no faster than the feed publishes.

## Errors

- **401** - missing or bad Basic credentials. Do not retry without fixing credentials.
- **404** - the path template or the requested interval has no data.
- There is no `problem+json` envelope and no error-code registry; treat the HTTP status as the whole
  error signal. See `errors/iso-new-england-problem-types.yml`.

## Honesty rules for the agent

- All timestamps are ISO 8601 with a `-04:00`/`-05:00` New England offset - keep the offset when
  quoting a time.
- These are *wholesale* prices in $/MWh at pricing nodes, not retail electricity rates. ISO New
  England does not handle retail electricity and has no consumer usage or billing data.
- An empty response (e.g. `{"FiveMinLmps": {}}`) is a real answer - the feed has nothing for that
  interval. Say so; do not substitute an earlier interval silently.
