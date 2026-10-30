# ISO New England

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
> **Not from the company, and here with a question?** You are welcome here — we would rather be the
> front line and point you the right way than have a good report go nowhere. What this repository
> can answer is narrow, though, so it is worth knowing who you are actually looking for:
>
> - **A question about how the API works, an account, billing, or a bug in the service** — that is
>   the company's own support, not us. We profile this API; we do not operate it and cannot see
>   your account.
> - **A bug in an open-source project we only catalog** — file it on that project's own repository.
>   This has happened with a real and correct bug report that reached us instead of the people who
>   could fix it, which helped nobody.
> - **Anything about this listing itself** — the description, the tags, the rating, a missing or
>   wrong artifact — is ours. Open an issue here.
> - **Not sure, or something general about API Evangelist or APIs.io** — open an issue on the
>   [APIs.io Inbox](https://github.com/api-search/inbox) and we will route it.
>
> **This repository contains no software, and we will never ask you to download anything.** There is
> no build, release, installer, or binary here — only text and machine-readable API descriptions, so
> there is nothing here that can be "corrupt" or need "repairing". Any issue, comment, or email
> claiming otherwise and offering a download link is not from us and is hostile. Do not follow the
> link; it is a lure. Report it to GitHub and, if you like, tell us at
> [info@apievangelist.com](mailto:info@apievangelist.com) so we can take it down.
>
> **On a security or compliance team?** Email
> [info@apievangelist.com](mailto:info@apievangelist.com) with *security* in the subject line and
> you will get a person, not a form. We will tell you exactly which public URLs this profile was
> built from so your team can see the same surface we did, and we will take the listing down on
> request while you work through it.
>
> Full detail: **[Where this data comes from](https://apievangelist.com/about/where-our-data-comes-from)**
<!-- API-EVANGELIST-PROVENANCE:END -->

ISO New England Inc. is the independent, nonprofit regional transmission organization authorized by the Federal Energy Regulatory Commission to operate the high-voltage power system, administer the wholesale electricity markets, and plan the power system for Connecticut, Rhode Island, Massachusetts, Vermont, New Hampshire, and most of Maine. Home market is the United States. It sits at the wholesale layer of the value chain, between generators, transmission owners, interconnections with New York and Canada, and the load-serving entities that resell power to retail customers - and it states on its own site that handling retail electricity is something it does not do. Its API posture is the sector's classic split, read from the wholesale end. Market and system data is genuinely open, so open that the ISO Express portal serves full nodal day-ahead LMP files as anonymous CSV and the public dashboards are backed by an anonymous JSON feed. Consumer data does not exist here at all, and cannot, because ISO New England holds no retail customer relationships and no Green Button, ESPI, or consumer data-portability mandate reaches it. The one documented programmatic contract, the Web Services API v1.1, is a real, richly documented RESTful surface of 477 path templates across 90 market and operations resources, but it answers 401 to anonymous callers - a developer must first create a free, self-serve ISO Express account, which the ISO says automatically grants access to the data feeds, and then authenticate with HTTP Basic over SSL.

**Areas:** Energy · United States · Electricity · Energy Markets · Grid · Open Data · Wholesale Markets · Demand Response · Renewables · New England

## ISO New England on APIs.io

Everything profiled for ISO New England is published on APIs.io rather than in this repository. Start at the provider page — **[apis.io/providers/iso-new-england/](https://apis.io/providers/iso-new-england/)** — or go straight to one of the APIs or properties below.

### APIs (91)

- [ISO New England Actualinterchange API](https://apis.io/apis/iso-new-england/iso-new-england-actualinterchange-api/) — 4 path template(s) under /actualinterchange in the published ISO New England Web Services API v1.1 documentation.
- [ISO New England Ams API](https://apis.io/apis/iso-new-england/iso-new-england-ams-api/) — 4 path template(s) under /ams in the published ISO New England Web Services API v1.1 documentation.
- [ISO New England Capacityscarcitycondition API](https://apis.io/apis/iso-new-england/iso-new-england-capacityscarcitycondition-api/) — 6 path template(s) under /capacityscarcitycondition in the published ISO New England Web Services API v1.1 documentation.
- [ISO New England Combinedhourlydemand API](https://apis.io/apis/iso-new-england/iso-new-england-combinedhourlydemand-api/) — 3 path template(s) under /combinedhourlydemand in the published ISO New England Web Services API v1.1 documentation.
- [ISO New England Daasreservedata API](https://apis.io/apis/iso-new-england/iso-new-england-daasreservedata-api/) — 3 path template(s) under /daasreservedata in the published ISO New England Web Services API v1.1 documentation.
- [ISO New England Daasstrikeprices API](https://apis.io/apis/iso-new-england/iso-new-england-daasstrikeprices-api/) — 3 path template(s) under /daasstrikeprices in the published ISO New England Web Services API v1.1 documentation.
- [ISO New England Dailyofferthreshprice API](https://apis.io/apis/iso-new-england/iso-new-england-dailyofferthreshprice-api/) — 5 path template(s) under /dailyofferthreshprice in the published ISO New England Web Services API v1.1 documentation.
- [ISO New England Dayaheadconstraints API](https://apis.io/apis/iso-new-england/iso-new-england-dayaheadconstraints-api/) — 4 path template(s) under /dayaheadconstraints in the published ISO New England Web Services API v1.1 documentation.
- [ISO New England Dayaheadhourlydemand API](https://apis.io/apis/iso-new-england/iso-new-england-dayaheadhourlydemand-api/) — 6 path template(s) under /dayaheadhourlydemand in the published ISO New England Web Services API v1.1 documentation.
- [ISO New England Dayaheadhourlyoperatingreserve API](https://apis.io/apis/iso-new-england/iso-new-england-dayaheadhourlyoperatingreserve-api/) — 6 path template(s) under /dayaheadhourlyoperatingreserve in the published ISO New England Web Services API v1.1 documentation.
- [ISO New England Dayaheadlmpavgcongestion API](https://apis.io/apis/iso-new-england/iso-new-england-dayaheadlmpavgcongestion-api/) — 5 path template(s) under /dayaheadlmpavgcongestion in the published ISO New England Web Services API v1.1 documentation.
- [ISO New England Dayaheadprdclearing API](https://apis.io/apis/iso-new-england/iso-new-england-dayaheadprdclearing-api/) — 5 path template(s) under /dayaheadprdclearing in the published ISO New England Web Services API v1.1 documentation.
- [ISO New England Dayaheadvirtualproxy API](https://apis.io/apis/iso-new-england/iso-new-england-dayaheadvirtualproxy-api/) — 6 path template(s) under /dayaheadvirtualproxy in the published ISO New England Web Services API v1.1 documentation.
- [ISO New England Drdispatch API](https://apis.io/apis/iso-new-england/iso-new-england-drdispatch-api/) — 6 path template(s) under /drdispatch in the published ISO New England Web Services API v1.1 documentation.
- [ISO New England Drtp API](https://apis.io/apis/iso-new-england/iso-new-england-drtp-api/) — 5 path template(s) under /drtp in the published ISO New England Web Services API v1.1 documentation.
- [ISO New England Fcmabp API](https://apis.io/apis/iso-new-england/iso-new-england-fcmabp-api/) — 4 path template(s) under /fcmabp in the published ISO New England Web Services API v1.1 documentation.
- [ISO New England Fcmara API](https://apis.io/apis/iso-new-england/iso-new-england-fcmara-api/) — 4 path template(s) under /fcmara in the published ISO New England Web Services API v1.1 documentation.
- [ISO New England Fcmmbp API](https://apis.io/apis/iso-new-england/iso-new-england-fcmmbp-api/) — 4 path template(s) under /fcmmbp in the published ISO New England Web Services API v1.1 documentation.
- [ISO New England Fcmmra API](https://apis.io/apis/iso-new-england/iso-new-england-fcmmra-api/) — 4 path template(s) under /fcmmra in the published ISO New England Web Services API v1.1 documentation.
- [ISO New England Fifteenminuteconstraints API](https://apis.io/apis/iso-new-england/iso-new-england-fifteenminuteconstraints-api/) — 5 path template(s) under /fifteenminuteconstraints in the published ISO New England Web Services API v1.1 documentation.
- [ISO New England Fifteenminuteinterchange API](https://apis.io/apis/iso-new-england/iso-new-england-fifteenminuteinterchange-api/) — 6 path template(s) under /fifteenminuteinterchange in the published ISO New England Web Services API v1.1 documentation.
- [ISO New England Fifteenminutelmp API](https://apis.io/apis/iso-new-england/iso-new-england-fifteenminutelmp-api/) — 5 path template(s) under /fifteenminutelmp in the published ISO New England Web Services API v1.1 documentation.
- [ISO New England Fiveminuteconstraints API](https://apis.io/apis/iso-new-england/iso-new-england-fiveminuteconstraints-api/) — 4 path template(s) under /fiveminuteconstraints in the published ISO New England Web Services API v1.1 documentation.
- [ISO New England Fiveminuteestimatedzonalload API](https://apis.io/apis/iso-new-england/iso-new-england-fiveminuteestimatedzonalload-api/) — 5 path template(s) under /fiveminuteestimatedzonalload in the published ISO New England Web Services API v1.1 documentation.
- [ISO New England Fiveminuteexternalflow API](https://apis.io/apis/iso-new-england/iso-new-england-fiveminuteexternalflow-api/) — 7 path template(s) under /fiveminuteexternalflow in the published ISO New England Web Services API v1.1 documentation.
- [ISO New England Fiveminutelmp API](https://apis.io/apis/iso-new-england/iso-new-england-fiveminutelmp-api/) — 14 path template(s) under /fiveminutelmp in the published ISO New England Web Services API v1.1 documentation.
- [ISO New England Fiveminutercp API](https://apis.io/apis/iso-new-england/iso-new-england-fiveminutercp-api/) — 7 path template(s) under /fiveminutercp in the published ISO New England Web Services API v1.1 documentation.
- [ISO New England Fiveminutereserveprice API](https://apis.io/apis/iso-new-england/iso-new-england-fiveminutereserveprice-api/) — 13 path template(s) under /fiveminutereserveprice in the published ISO New England Web Services API v1.1 documentation.
- [ISO New England Fiveminutesystemload API](https://apis.io/apis/iso-new-england/iso-new-england-fiveminutesystemload-api/) — 4 path template(s) under /fiveminutesystemload in the published ISO New England Web Services API v1.1 documentation.
- [ISO New England Fiveminutezonalloadforecast API](https://apis.io/apis/iso-new-england/iso-new-england-fiveminutezonalloadforecast-api/) — 3 path template(s) under /fiveminutezonalloadforecast in the published ISO New England Web Services API v1.1 documentation.
- [ISO New England Forecastcapacity API](https://apis.io/apis/iso-new-england/iso-new-england-forecastcapacity-api/) — 6 path template(s) under /forecastcapacity in the published ISO New England Web Services API v1.1 documentation.
- [ISO New England Frmdtp API](https://apis.io/apis/iso-new-england/iso-new-england-frmdtp-api/) — 5 path template(s) under /frmdtp in the published ISO New England Web Services API v1.1 documentation.
- [ISO New England Ftrauctionclearingprices API](https://apis.io/apis/iso-new-england/iso-new-england-ftrauctionclearingprices-api/) — 4 path template(s) under /ftrauctionclearingprices in the published ISO New England Web Services API v1.1 documentation.
- [ISO New England Ftrauctionresults API](https://apis.io/apis/iso-new-england/iso-new-england-ftrauctionresults-api/) — 4 path template(s) under /ftrauctionresults in the published ISO New England Web Services API v1.1 documentation.
- [ISO New England Genfuelmix API](https://apis.io/apis/iso-new-england/iso-new-england-genfuelmix-api/) — 6 path template(s) under /genfuelmix in the published ISO New England Web Services API v1.1 documentation.
- [ISO New England Hbannualftrauction API](https://apis.io/apis/iso-new-england/iso-new-england-hbannualftrauction-api/) — 4 path template(s) under /hbannualftrauction in the published ISO New England Web Services API v1.1 documentation.
- [ISO New England Hbdaasardoffer API](https://apis.io/apis/iso-new-england/iso-new-england-hbdaasardoffer-api/) — 3 path template(s) under /hbdaasardoffer in the published ISO New England Web Services API v1.1 documentation.
- [ISO New England Hbdaasdrroffer API](https://apis.io/apis/iso-new-england/iso-new-england-hbdaasdrroffer-api/) — 3 path template(s) under /hbdaasdrroffer in the published ISO New England Web Services API v1.1 documentation.
- [ISO New England Hbdaasenergyoffer API](https://apis.io/apis/iso-new-england/iso-new-england-hbdaasenergyoffer-api/) — 3 path template(s) under /hbdaasenergyoffer in the published ISO New England Web Services API v1.1 documentation.
- [ISO New England Hbdayaheadardbid API](https://apis.io/apis/iso-new-england/iso-new-england-hbdayaheadardbid-api/) — 4 path template(s) under /hbdayaheadardbid in the published ISO New England Web Services API v1.1 documentation.
- [ISO New England Hbdayaheaddemandbid API](https://apis.io/apis/iso-new-england/iso-new-england-hbdayaheaddemandbid-api/) — 6 path template(s) under /hbdayaheaddemandbid in the published ISO New England Web Services API v1.1 documentation.
- [ISO New England Hbdayaheaddrrbid API](https://apis.io/apis/iso-new-england/iso-new-england-hbdayaheaddrrbid-api/) — 3 path template(s) under /hbdayaheaddrrbid in the published ISO New England Web Services API v1.1 documentation.
- [ISO New England Hbdayaheadenergyoffer API](https://apis.io/apis/iso-new-england/iso-new-england-hbdayaheadenergyoffer-api/) — 4 path template(s) under /hbdayaheadenergyoffer in the published ISO New England Web Services API v1.1 documentation.
- [ISO New England Hbdayaheadloadresponseoffer API](https://apis.io/apis/iso-new-england/iso-new-england-hbdayaheadloadresponseoffer-api/) — 4 path template(s) under /hbdayaheadloadresponseoffer in the published ISO New England Web Services API v1.1 documentation.
- [ISO New England Hbfcmara API](https://apis.io/apis/iso-new-england/iso-new-england-hbfcmara-api/) — 5 path template(s) under /hbfcmara in the published ISO New England Web Services API v1.1 documentation.
- [ISO New England Hbfcmmra API](https://apis.io/apis/iso-new-england/iso-new-england-hbfcmmra-api/) — 4 path template(s) under /hbfcmmra in the published ISO New England Web Services API v1.1 documentation.
- [ISO New England Hbforwardreserveauctionoffer API](https://apis.io/apis/iso-new-england/iso-new-england-hbforwardreserveauctionoffer-api/) — 3 path template(s) under /hbforwardreserveauctionoffer in the published ISO New England Web Services API v1.1 documentation.
- [ISO New England Hbimportexport API](https://apis.io/apis/iso-new-england/iso-new-england-hbimportexport-api/) — 4 path template(s) under /hbimportexport in the published ISO New England Web Services API v1.1 documentation.
- [ISO New England Hbmonthlyftrauction API](https://apis.io/apis/iso-new-england/iso-new-england-hbmonthlyftrauction-api/) — 4 path template(s) under /hbmonthlyftrauction in the published ISO New England Web Services API v1.1 documentation.
- [ISO New England Hbrealtimeardbid API](https://apis.io/apis/iso-new-england/iso-new-england-hbrealtimeardbid-api/) — 4 path template(s) under /hbrealtimeardbid in the published ISO New England Web Services API v1.1 documentation.
- [ISO New England Hbrealtimedrrbid API](https://apis.io/apis/iso-new-england/iso-new-england-hbrealtimedrrbid-api/) — 3 path template(s) under /hbrealtimedrrbid in the published ISO New England Web Services API v1.1 documentation.
- [ISO New England Hbrealtimeenergyoffer API](https://apis.io/apis/iso-new-england/iso-new-england-hbrealtimeenergyoffer-api/) — 4 path template(s) under /hbrealtimeenergyoffer in the published ISO New England Web Services API v1.1 documentation.
- [ISO New England Hbregulationoffer API](https://apis.io/apis/iso-new-england/iso-new-england-hbregulationoffer-api/) — 4 path template(s) under /hbregulationoffer in the published ISO New England Web Services API v1.1 documentation.
- [ISO New England Hourlybainterchange API](https://apis.io/apis/iso-new-england/iso-new-england-hourlybainterchange-api/) — 4 path template(s) under /hourlybainterchange in the published ISO New England Web Services API v1.1 documentation.
- [ISO New England Hourlyfinalreserveprice API](https://apis.io/apis/iso-new-england/iso-new-england-hourlyfinalreserveprice-api/) — 7 path template(s) under /hourlyfinalreserveprice in the published ISO New England Web Services API v1.1 documentation.
- [ISO New England Hourlylmp API](https://apis.io/apis/iso-new-england/iso-new-england-hourlylmp-api/) — 24 path template(s) under /hourlylmp in the published ISO New England Web Services API v1.1 documentation.
- [ISO New England Hourlyloadforecast API](https://apis.io/apis/iso-new-england/iso-new-england-hourlyloadforecast-api/) — 5 path template(s) under /hourlyloadforecast in the published ISO New England Web Services API v1.1 documentation.
- [ISO New England Hourlyloadgeninterchange API](https://apis.io/apis/iso-new-england/iso-new-england-hourlyloadgeninterchange-api/) — 4 path template(s) under /hourlyloadgeninterchange in the published ISO New England Web Services API v1.1 documentation.
- [ISO New England Hourlyper API](https://apis.io/apis/iso-new-england/iso-new-england-hourlyper-api/) — 5 path template(s) under /hourlyper in the published ISO New England Web Services API v1.1 documentation.
- [ISO New England Hourlyprelimreserveprice API](https://apis.io/apis/iso-new-england/iso-new-england-hourlyprelimreserveprice-api/) — 7 path template(s) under /hourlyprelimreserveprice in the published ISO New England Web Services API v1.1 documentation.
- [ISO New England Hourlyrcp API](https://apis.io/apis/iso-new-england/iso-new-england-hourlyrcp-api/) — 8 path template(s) under /hourlyrcp in the published ISO New England Web Services API v1.1 documentation.
- [ISO New England Hourlysysload API](https://apis.io/apis/iso-new-england/iso-new-england-hourlysysload-api/) — 8 path template(s) under /hourlysysload in the published ISO New England Web Services API v1.1 documentation.
- [ISO New England Lmp Index API](https://apis.io/apis/iso-new-england/iso-new-england-lmpindex-api/) — 12 path template(s) under /lmpIndex in the published ISO New England Web Services API v1.1 documentation.
- [ISO New England Loadzonencpc API](https://apis.io/apis/iso-new-england/iso-new-england-loadzonencpc-api/) — 6 path template(s) under /loadzonencpc in the published ISO New England Web Services API v1.1 documentation.
- [ISO New England Locations API](https://apis.io/apis/iso-new-england/iso-new-england-locations-api/) — 3 path template(s) under /locations in the published ISO New England Web Services API v1.1 documentation.
- [ISO New England Monthlyassetncpc API](https://apis.io/apis/iso-new-england/iso-new-england-monthlyassetncpc-api/) — 4 path template(s) under /monthlyassetncpc in the published ISO New England Web Services API v1.1 documentation.
- [ISO New England Monthlylmpindex API](https://apis.io/apis/iso-new-england/iso-new-england-monthlylmpindex-api/) — 4 path template(s) under /monthlylmpindex in the published ISO New England Web Services API v1.1 documentation.
- [ISO New England Monthlyper API](https://apis.io/apis/iso-new-england/iso-new-england-monthlyper-api/) — 5 path template(s) under /monthlyper in the published ISO New England Web Services API v1.1 documentation.
- [ISO New England Morningreport API](https://apis.io/apis/iso-new-england/iso-new-england-morningreport-api/) — 6 path template(s) under /morningreport in the published ISO New England Web Services API v1.1 documentation.
- [ISO New England Ncpc API](https://apis.io/apis/iso-new-england/iso-new-england-ncpc-api/) — 5 path template(s) under /ncpc in the published ISO New England Web Services API v1.1 documentation.
- [ISO New England Networkload API](https://apis.io/apis/iso-new-england/iso-new-england-networkload-api/) — 4 path template(s) under /networkload in the published ISO New England Web Services API v1.1 documentation.
- [ISO New England Nextdayoperationalcapacityreport API](https://apis.io/apis/iso-new-england/iso-new-england-nextdayoperationalcapacityreport-api/) — 4 path template(s) under /nextdayoperationalcapacityreport in the published ISO New England Web Services API v1.1 documentation.
- [ISO New England Nodalloadstat API](https://apis.io/apis/iso-new-england/iso-new-england-nodalloadstat-api/) — 3 path template(s) under /nodalloadstat in the published ISO New England Web Services API v1.1 documentation.
- [ISO New England Nodalloadweight API](https://apis.io/apis/iso-new-england/iso-new-england-nodalloadweight-api/) — 6 path template(s) under /nodalloadweight in the published ISO New England Web Services API v1.1 documentation.
- [ISO New England Outages API](https://apis.io/apis/iso-new-england/iso-new-england-outages-api/) — 20 path template(s) under /outages in the published ISO New England Web Services API v1.1 documentation.
- [ISO New England Performancescore API](https://apis.io/apis/iso-new-england/iso-new-england-performancescore-api/) — 4 path template(s) under /performancescore in the published ISO New England Web Services API v1.1 documentation.
- [ISO New England Powersystemconditions API](https://apis.io/apis/iso-new-england/iso-new-england-powersystemconditions-api/) — 4 path template(s) under /powersystemconditions in the published ISO New England Web Services API v1.1 documentation.
- [ISO New England Pricerespevent API](https://apis.io/apis/iso-new-england/iso-new-england-pricerespevent-api/) — 5 path template(s) under /pricerespevent in the published ISO New England Web Services API v1.1 documentation.
- [ISO New England Realtimeconstraints API](https://apis.io/apis/iso-new-england/iso-new-england-realtimeconstraints-api/) — 9 path template(s) under /realtimeconstraints in the published ISO New England Web Services API v1.1 documentation.
- [ISO New England Realtimehourlydemand API](https://apis.io/apis/iso-new-england/iso-new-england-realtimehourlydemand-api/) — 6 path template(s) under /realtimehourlydemand in the published ISO New England Web Services API v1.1 documentation.
- [ISO New England Realtimehourlyoperatingreserve API](https://apis.io/apis/iso-new-england/iso-new-england-realtimehourlyoperatingreserve-api/) — 6 path template(s) under /realtimehourlyoperatingreserve in the published ISO New England Web Services API v1.1 documentation.
- [ISO New England Reliabilityregionloadforecast API](https://apis.io/apis/iso-new-england/iso-new-england-reliabilityregionloadforecast-api/) — 5 path template(s) under /reliabilityregionloadforecast in the published ISO New England Web Services API v1.1 documentation.
- [ISO New England Schedule2varstatus API](https://apis.io/apis/iso-new-england/iso-new-england-schedule2varstatus-api/) — 4 path template(s) under /schedule2varstatus in the published ISO New England Web Services API v1.1 documentation.
- [ISO New England Seasonalpeakhourdata API](https://apis.io/apis/iso-new-england/iso-new-england-seasonalpeakhourdata-api/) — 4 path template(s) under /seasonalpeakhourdata in the published ISO New England Web Services API v1.1 documentation.
- [ISO New England Sevendayforecast API](https://apis.io/apis/iso-new-england/iso-new-england-sevendayforecast-api/) — 5 path template(s) under /sevendayforecast in the published ISO New England Web Services API v1.1 documentation.
- [ISO New England Sevendaywindpowerforecast API](https://apis.io/apis/iso-new-england/iso-new-england-sevendaywindpowerforecast-api/) — 4 path template(s) under /sevendaywindpowerforecast in the published ISO New England Web Services API v1.1 documentation.
- [ISO New England Singlesrccontingencylimits API](https://apis.io/apis/iso-new-england/iso-new-england-singlesrccontingencylimits-api/) — 6 path template(s) under /singlesrccontingencylimits in the published ISO New England Web Services API v1.1 documentation.
- [ISO New England Totaltransfercapability API](https://apis.io/apis/iso-new-england/iso-new-england-totaltransfercapability-api/) — 5 path template(s) under /totaltransfercapability in the published ISO New England Web Services API v1.1 documentation.
- [ISO New England Weeklylmpindex API](https://apis.io/apis/iso-new-england/iso-new-england-weeklylmpindex-api/) — 4 path template(s) under /weeklylmpindex in the published ISO New England Web Services API v1.1 documentation.
- [ISO New England Whlsecost API](https://apis.io/apis/iso-new-england/iso-new-england-whlsecost-api/) — 8 path template(s) under /whlsecost in the published ISO New England Web Services API v1.1 documentation.
- [ISO New England Power System API](https://apis.io/apis/iso-new-england/iso-new-england-power-system-api/) — 2 path template(s) under /powersystem in the published ISO New England Web Services API v1.1 documentation.

### Published properties

Each property below is a page on APIs.io carrying the machine-readable artifact and what it says.

#### Arazzo workflows (2)

Multi-step workflows that chain operations into a business task.

- [ISO New England grid snapshot](https://apis.io/arazzos/iso-new-england/iso-new-england-grid-snapshot/)
- [ISO New England price spike diagnosis](https://apis.io/arazzos/iso-new-england/iso-new-england-price-spike-diagnosis/)

#### MCP servers (1)

Model Context Protocol servers that expose the API to agents.

- [iso-new-england-web-services](https://apis.io/servers/iso-new-england/iso-new-england-web-services/)

#### Agentic access (1)

Which operations an agent can call, which act, and which need a human in the loop.

- [Iso New England Agentic Access](https://apis.io/agentic-access/iso-new-england/iso-new-england-agentic-access/)

#### JSON Schema (1)

The data models the API reads and writes.

- [ISO New England Web Services API v1.1 data model](https://apis.io/schemas/iso-new-england/iso-new-england-web-services-schemas/)

#### Vocabulary (1)

The provider's domain terms, defined.

- [Iso New England Vocabulary](https://apis.io/vocabularies/iso-new-england/iso-new-england-vocabulary/)

#### Examples (14)

Example requests and responses.

- [Iso New England Actualinterchange_Current](https://apis.io/examples/iso-new-england/iso-new-england-actualinterchange_current/)
- [Iso New England Dayaheadconstraints_Current](https://apis.io/examples/iso-new-england/iso-new-england-dayaheadconstraints_current/)
- [Iso New England Dayaheadhourlydemand_Current](https://apis.io/examples/iso-new-england/iso-new-england-dayaheadhourlydemand_current/)
- [Iso New England Fifteenminutelmp_Final_Current](https://apis.io/examples/iso-new-england/iso-new-england-fifteenminutelmp_final_current/)
- [Iso New England Fiveminutelmp_Current](https://apis.io/examples/iso-new-england/iso-new-england-fiveminutelmp_current/)
- [Iso New England Fiveminutelmp_Info](https://apis.io/examples/iso-new-england/iso-new-england-fiveminutelmp_info/)
- [Iso New England Fiveminutesystemload_Current](https://apis.io/examples/iso-new-england/iso-new-england-fiveminutesystemload_current/)
- [Iso New England Genfuelmix_Current](https://apis.io/examples/iso-new-england/iso-new-england-genfuelmix_current/)
- [Iso New England Genfuelmix_Info](https://apis.io/examples/iso-new-england/iso-new-england-genfuelmix_info/)
- [Iso New England Hourlyloadforecast_Current](https://apis.io/examples/iso-new-england/iso-new-england-hourlyloadforecast_current/)
- [Iso New England Locations_All](https://apis.io/examples/iso-new-england/iso-new-england-locations_all/)
- [Iso New England Morningreport_Current](https://apis.io/examples/iso-new-england/iso-new-england-morningreport_current/)
- [Iso New England Realtimehourlydemand_Current](https://apis.io/examples/iso-new-england/iso-new-england-realtimehourlydemand_current/)
- [Iso New England Sevendayforecast_Current](https://apis.io/examples/iso-new-england/iso-new-england-sevendayforecast_current/)

#### Collections (1)

Postman and Open Collection request collections.

- [ISO New England Web Services API v1.1](https://apis.io/collections/iso-new-england/open-iso-new-england-web-services/)

#### Overlays (1)

OpenAPI overlays, including conversational phrasing for each operation.

- [Iso New England Web Services Overlay](https://apis.io/overlays/iso-new-england/iso-new-england-web-services-overlay/)

#### Security (2)

Authentication, trust centre, and vulnerability disclosure.

- [Iso New England Authentication](https://apis.io/security/iso-new-england/iso-new-england-authentication/)
- [Iso New England Domain Security](https://apis.io/security/iso-new-england/iso-new-england-domain-security/)

## Where to find this API

Links to the company's own pages. This repository publishes no copy of their specifications — the canonical document is theirs and lives at the URLs below.

- [Website](https://www.iso-ne.com/)
- [Documentation](https://www.iso-ne.com/participate/support/web-services-data)
- [Getting started](https://www.iso-ne.com/participate/applications-status-changes/access-software-systems#data-feeds)
- [API reference](https://webservices.iso-ne.com/docs/v1.1/)
- [Sign up](https://www.iso-ne.com/signup)
- [Support](https://askiso.iso-ne.com/s/)
- [Blog](https://isonewswire.com/)
- [Compliance](https://www.iso-ne.com/participate/rules-procedures/nerc-npcc)
- [Terms of service](https://www.iso-ne.com/legal-privacy)
- [Privacy policy](https://www.iso-ne.com/legal-privacy)
- [GitHub](https://github.com/iso-ne)

## API Evangelist rating

**Kin Score 49.3** — developing · rubric 0.25.0 · scored 2026-10-23

| Facet | Score |
|---|---|
| Discoverability | 69.6 |
| Contract quality | 56.0 |
| Contract governance | 19.7 |
| Operational transparency | 23.7 |
| Developer ergonomics | 58.9 |
| Access clarity | 42.1 |

**Agent readiness 24.2** — agent-aware

| Agent-readiness dimension | Result |
|---|---|
| Spec Presence | yes |
| Agentic Access | derived (partial credit) |
| Reversibility Documented | na |
| MCP Server | — |
| Auth Clarity | bearer (partial credit) |
| Idempotency | na |
| Error Semantics | derived (partial credit) |
| OpenAPI Examples | partial |
| Rate Limit Signal | — |
| Event Surface Described | — |
| Agent Skills | derived (partial credit) |
| Well Known Catalog | — |
| Consent Identity | — |
| Agent Card | — |
| Dry Run Mode | na |
| Delegated Identity | — |
| Protected Resource Metadata | — |
| Dynamic Client Registration | — |
| Agentic Commerce | — |
| Pagination Ratio | na |
| Operation Distinctiveness | — |

**Regulatory alignment 31.1** — Energy & Utilities

The rubric is published at [github.com/api-evangelist/kin-score](https://github.com/api-evangelist/kin-score). The per-check breakdown behind these numbers — which checks were earned, partial or missed — along with score history and how this provider compares to its peers, is available at [apis.io/providers/iso-new-england/](https://apis.io/providers/iso-new-england/).

## How this profile is made

API Evangelist profiles a company's public API surface the way a developer would find it: the website, developer portal and documentation, the specifications it publishes, its public repositories, and its pricing, status and changelog pages. From that it derives the properties above — contracts split per API, workflows, schemas, collections, governance rules, plans and rate limits — and scores them against the published [Kin Score rubric](https://github.com/api-evangelist/kin-score).

The artifacts are published on [APIs.io](https://apis.io), not in this repository. This repository is the public record for ISO New England: the place to say something is wrong, missing or out of date, and to ask for a re-score or a removal.

## Open an issue

- **Something about this listing** — a wrong description, a missing API, a stale artifact or a question about the rating: [open an issue on this repository](https://github.com/api-evangelist/iso-new-england/issues/new).
- **A new API, or one that is not in the catalog yet** — [submit it on APIs.io](https://apis.io/add/).
- **Anything else** — [the APIs.io inbox](https://github.com/api-search/inbox/issues/new) or [info@apievangelist.com](mailto:info@apievangelist.com).
