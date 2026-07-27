---
name: Read ISO New England capacity market results and system forecasts
description: Retrieve Forward Capacity Market auction and reconfiguration results, the morning report, and the seven-day capacity and wind forecasts from the ISO New England Web Services API v1.1.
api: openapi/iso-new-england-web-services-openapi.yml
generated: '2026-07-27'
method: generated
operations:
  - getFcmaraCurrent
  - getFcmaraCpByCp
  - getFcmaraCpByCpAraByAra
  - getFcmmraCurrent
  - getFcmmraCpByCpMonthByMonth
  - getMorningreportCurrent
  - getSevendayforecastCurrent
  - getSevendaywindpowerforecastCurrent
  - getForecastcapacityCurrent
---

# Read ISO New England capacity market results and system forecasts

Use this for capacity-market analysis and for forward-looking system adequacy questions ("is next
week tight?", "what cleared in ARA2 for the 2027-28 commitment period?").

## Before you call

- Base path `https://webservices.iso-ne.com/api/v1.1`, HTTP Basic over TLS, `.json` extension.
- **Commitment period (`cp`)** is formatted `nnnn-nn`, e.g. `2010-11` for the FCA1 commitment period.
- **ARA** values are `ARA1`, `ARA2`, `ARA3` - the first, second and third annual reconfiguration
  auctions. Monthly reconfiguration auctions use the `fcmmra` resource with a `month` (`YYYYMM`).

## Capacity market

1. `getFcmaraCurrent` (`GET /fcmara/current.json`) - the current annual reconfiguration auction
   results.
2. `getFcmaraCpByCp` (`GET /fcmara/cp/{cp}.json`) - all ARA results for one commitment period.
3. `getFcmaraCpByCpAraByAra` (`GET /fcmara/cp/{cp}/ara/{ara}.json`) - one specific auction, e.g.
   `/fcmara/cp/2027-28/ara/ARA2.json`.
4. `getFcmmraCurrent` and `getFcmmraCpByCpMonthByMonth`
   (`GET /fcmmra/cp/{cp}/month/{month}.json`) - monthly reconfiguration auction results.
5. Bilateral periods are separate resources (`/fcmabp`, `/fcmmbp`) with their own `arabp` parameter.

## Forecasts and adequacy

1. `getMorningreportCurrent` (`GET /morningreport/current.json`) - the daily operations picture:
   total available capacity, planned outage reductions, uncommitted available demand response,
   replacement reserve. Use it to answer "how tight is today".
2. `getSevendayforecastCurrent` (`GET /sevendayforecast/current.json`) - the seven-day capacity
   forecast, one `MarketDay` block per day with delist, outage and margin figures.
3. `getSevendaywindpowerforecastCurrent` (`GET /sevendaywindpowerforecast/current.json`) - the wind
   power forecast over the same horizon.
4. `getForecastcapacityCurrent` - forecast capacity analysis report values.

Every one of these has `/day/{day}` and `/info` siblings; use `/info` for freshness and `/day/{day}`
to reconstruct what was forecast on a past day (important when judging forecast accuracy - always
compare the forecast *as published on that day*, not today's revision).

## Honesty rules for the agent

- Capacity auction results are settled market outcomes with real money attached. Quote the
  commitment period and the auction (`ARA1`/`ARA2`/`ARA3`) with every number - a clearing price
  without its period and auction is meaningless.
- The morning report and seven-day forecast are ISO New England's operational outlook, not a
  guarantee; label them as forecasts with their `CreationDate`.
- If a commitment period returns nothing, say the feed published nothing for it. Do not interpolate.
- 401 = credentials, 404 = no data at that address; there is no error catalogue beyond HTTP status.
