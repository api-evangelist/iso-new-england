# ISO New England (iso-new-england)

<!-- API-EVANGELIST-PROVENANCE:BEGIN -->
> ### About this repository
>
> **This is not our API.** This repository is an independent, third-party profile of a company's
> **publicly available** API surface, maintained by [API Evangelist](https://apievangelist.com).
> API Evangelist does not operate, host, resell, or support this company's APIs, and is not
> affiliated with or endorsed by the company unless stated on the profile.
>
> **Where the information came from.** Everything here is assembled from material a member of the
> public can reach with a browser and no credentials — the company's own website, developer portal
> and documentation, the specifications it publishes for public use (OpenAPI, AsyncAPI, JSON Schema,
> `apis.json`, `llms.txt` and similar), its public repositories, and its public status, pricing and
> changelog pages. **Nothing here is obtained by breaching a system, defeating an access control, or
> using credentials of any kind.**
>
> **The rating is an independent assessment.** The Kin Score and Agent Readiness rating are
> independently calculated scores of a company's *public* API artifacts, produced by API Evangelist
> against a published rubric. They are not certifications, endorsements, security assessments, or
> audits, and they score published artifacts — not the quality, safety, or security of the software.
>
> **Corrections, re-scores, and removal are free.** No partnership, contract, or purchase is
> required, and you do not need to justify the request.
>
> - **Something wrong?** Open an issue on this repository, or email
>   [info@apievangelist.com](mailto:info@apievangelist.com).
> - **Published something new?** Ask for a re-score and we will re-run the rating.
> - **Want the listing taken down?** Say so and we will honor it. The profile is reduced to your
>   company name, a factual description, and a link to your own site, and the company is recorded as
>   **unrated** — never scored zero for having asked.
>
> **Response times.** Acknowledgement within **one business day**; removal or restriction within
> **two business days**; corrections and re-scores within **five business days**.
>
> **On a security or compliance team?** Email
> [info@apievangelist.com](mailto:info@apievangelist.com) with *security* in the subject line and
> you will get a person, not a form. We will tell you exactly which public URLs this profile was
> built from so your team can see the same surface we did, and we will take the listing down on
> request while you work through it.
>
> Full detail: **[Where this data comes from](https://apievangelist.com/about/where-our-data-comes-from)**
<!-- API-EVANGELIST-PROVENANCE:END -->

ISO New England Inc. is the independent, nonprofit regional transmission organization authorized by the Federal Energy Regulatory Commission to operate the high-voltage power system, administer the wholesale electricity markets, and plan the power system for Connecticut, Rhode Island, Massachusetts, Vermont, New Hampshire, and most of Maine. Home market is the United States. It sits at the wholesale layer of the value chain, between generators, transmission owners, interconnections with New York and Canada, and the load-serving entities that resell power to retail customers — and it states on its own site that handling retail electricity is something it does not do. Its API posture is the sector's classic split, read from the wholesale end. Market and system data is genuinely open, so open that the ISO Express portal serves full nodal day-ahead LMP files as anonymous CSV and the public dashboards are backed by an anonymous JSON feed. Consumer data does not exist here at all, and cannot, because ISO New England holds no retail customer relationships and no Green Button, ESPI, or consumer data-portability mandate reaches it. The one documented programmatic contract, the Web Services API v1.1, is a real, richly documented RESTful surface of 477 path templates across 90 market and operations resources, but it answers 401 to anonymous callers — a developer must first create a free, self-serve ISO Express account, which the ISO says automatically grants access to the data feeds, and then authenticate with HTTP Basic over SSL.

**APIs.json:** [https://raw.githubusercontent.com/api-evangelist/iso-new-england/refs/heads/main/apis.yml](https://raw.githubusercontent.com/api-evangelist/iso-new-england/refs/heads/main/apis.yml)

## Tags

- Energy
- United States
- Electricity
- Energy Markets
- Grid
- Open Data
- Wholesale Markets
- Demand Response
- Renewables
- New England

## Timestamps

- **Created:** 2026-07-27
- **Modified:** 2026-07-27

## APIs

### ISO New England Web Services API v1.1

ISO New England's RESTful interface to energy and market data, deployed November 2013 and still the current version. The public Enunciate-generated technical documentation lists 477 unique path templates across 90 root resources — five-minute and hourly locational marginal prices, day-ahead and real-time demand, generation fuel mix, system load, external interchange and flows, day-ahead and real-time constraints, operating reserve and reserve prices, regulation clearing prices, Forward Capacity Market auction and reconfiguration results, FTR auction clearing prices and results, NCPC, outages, seven-day and seven-day wind forecasts, load forecasts, power system status and conditions, demand response dispatch and price-response events, locations, and hourly-bid participant resources. Every feed is available in XML and JSON. Authentication is HTTP Basic over SSL; anonymous requests return HTTP 401.

- **Human URL:** [https://webservices.iso-ne.com/docs/v1.1/](https://webservices.iso-ne.com/docs/v1.1/)
- **Base URL:** `https://webservices.iso-ne.com/api/v1.1`

#### Tags

- Energy Markets
- Electricity
- Grid
- Pricing
- Demand
- Forecasting

#### Properties

- [API Reference](https://webservices.iso-ne.com/docs/v1.1/)
- [Documentation](https://www.iso-ne.com/participate/support/web-services-data)
- [Documentation](https://www.iso-ne.com/participate/applications-status-changes/access-software-systems)
- [Documentation](https://www.iso-ne.com/static-assets/documents/2017/06/webservices_documentation.xlsx)
- [Sign Up](https://www.iso-ne.com/signup)
- [Portal](https://www.iso-ne.com/isoexpress/)
- [XML Schema](schemas/nextt-web-services.xsd)

## Common Properties

- [Website](https://www.iso-ne.com/)
- [Portal](https://www.iso-ne.com/isoexpress/)
- [API Reference](https://webservices.iso-ne.com/docs/v1.1/)
- [Documentation](https://www.iso-ne.com/participate/support/web-services-data)
- [Sign Up](https://www.iso-ne.com/signup)
- [Documentation](https://www.iso-ne.com/markets-operations/iso-express)
- [Regulation](https://www.iso-ne.com/markets-operations/transmission-operations-services/oasis)
- [Blog](https://isonewswire.com/)
- [Blog RSS](https://isonewswire.com/feed/)
- [LinkedIn](https://www.linkedin.com/company/iso-new-england/)
- [Twitter](https://twitter.com/isonewengland)
- [YouTube](https://www.youtube.com/@isonewengland)
- [GitHub Organization](https://github.com/iso-ne)
- [Support](https://askiso.iso-ne.com/s/)

## Mandate and Access Posture

- **Mandate regime:** `other` — FERC open-access and wholesale-market transparency (FERC Order No. 889 OASIS, NAESB standards, FERC-approved ISO-NE Tariff/OATT). There is **no** consumer energy data-portability mandate in play; Green Button/ESPI is voluntary in the US and no ISO-NE surface references it.
- **Mandate status:** `live-implemented` — verified by direct anonymous probe of the open market-data surface (2.46 MB day-ahead nodal LMP CSV, HTTP 200, no account), not by reading a compliance page. The OASIS node itself resolves in DNS but could not be reached over TLS from the probe environment and is recorded as claimed-unverified.
- **Data standard:** Proprietary ISO-NE XML/JSON schema, WADL-described. NAESB WEQ OASIS standards claimed on the Order 889 surface. No Green Button/ESPI, CDR, IEC CIM, IEEE 2030.5, OpenADR, OCPP or OCPI reference found.
- **Market data open:** yes — ISO Express is explicitly public, historical reports download anonymously as CSV.
- **Consumer data API:** no — ISO New England has no retail customers; its own site lists "Handle retail electricity" under things it does not do.
- **Access gate:** `self-serve` — a free ISO Express account (name, phone, company, email, password, CAPTCHA) which ISO-NE states automatically grants access to the data feeds.
- **Auth model:** HTTP Basic authentication over SSL. No API key header, no OAuth2, no OIDC, no mTLS, no accreditation.

## Harvested Artifacts (searched — real ISO New England documents, saved verbatim)

- `schemas/iso-new-england-web-services-ns0.xsd` — the full Web Services payload model, fetched 2026-07-27 from `https://webservices.iso-ne.com/docs/v1.1/ns0.xsd` (HTTP 200, 107,647 bytes, 205 complex types, parses as valid XSD).
- `schemas/iso-new-england-web-services-ns1.xsd` — second schema namespace, from `https://webservices.iso-ne.com/docs/v1.1/ns1.xsd` (HTTP 200, 5,917 bytes).
- `schemas/nextt-web-services.xsd` — NEXTT external transaction XML Schema, from `https://www.iso-ne.com/static-assets/documents/2019/09/nextt-web-services.xsd` (HTTP 200, 12,751 bytes).
- `examples/` — 14 real response payloads observed anonymously on 2026-07-27 through the public ISO Express dashboard proxy, with the proxy envelope removed.
- `vocabulary/iso-new-england-vocabulary.yml` — the 24 published parameter vocabularies (load/dispatch/reserve/capacity zones, external nodes, interfaces, NCPC types, fuel categories, bid types, ARA, market/outage/equipment/company/status codes) plus the live 1,302-entry location registry.

## Derived and Generated Artifacts (API Evangelist, not ISO New England)

- `openapi/iso-new-england-web-services-openapi.yml` — **derived** OpenAPI 3.1: 489 GET operations, 217 schemas, 91 tags, 13 real response examples. Built by parsing all 489 machine-generated Enunciate documentation pages plus the two published XSDs. Every operation carries `x-evidence` naming the documentation page it came from. **ISO New England does not publish an OpenAPI** — its only machine-readable interface description is a WADL served from inside the authenticated base path (HTTP 401 anonymously). This document must never be presented as an ISO New England artifact.
- `json-schema/`, `data-model/`, `errors/`, `conformance/`, `authentication/`, `agentic-access/` — derived from the OpenAPI and XSDs.
- `conventions/`, `lifecycle/`, `changelog/`, `packages/`, `well-known/`, `security/` — searched or probed; absences (no rate limits, no deprecation policy, no status page, no `/.well-known` document, no first-party SDK, no security.txt, no trust centre) are recorded as data.
- `skills/`, `arazzo/`, `mcp/`, `overlays/`, `llms/` — generated; every operationId used was verified verbatim against the spec. The MCP tool list is a **candidate** — ISO New England publishes no MCP server.

See `review.yml` for every URL probed and its HTTP status, including the `specHarvest.revision` note explaining what the first pass missed.
