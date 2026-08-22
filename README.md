# PECO Energy (peco-energy)

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

PECO Energy Company is the largest electric and natural gas utility in Pennsylvania, serving roughly 1.7 million electric and 553,000 natural gas customers across a 2,100-square-mile service territory in southeastern Pennsylvania. Headquartered in Philadelphia and a wholly owned subsidiary of Exelon Corporation, PECO operates a regulated transmission and distribution business that includes a fully deployed smart-meter network, an LNG storage facility in West Conshohocken, and a portfolio of energy-efficiency, demand response, and assistance programs marketed under the Smart Ideas brand. PECO does not publish a public developer portal or general-purpose API: its digital surface is delivered through the PECO web portal (peco.com / secure.peco.com), iOS and Android mobile apps, and an internal Exelon Utilities content / configuration API (eudapi.peco.com) that is not documented for third-party use. Customer-authorized programmatic access to interval energy usage is available through the customer-facing My Data / Energy Usage tools and, where supported via the Pennsylvania PUC EDI / data access framework, through third-party data aggregators (UtilityAPI, Arcadia, etc.) using customer credentials.

**URL:** [Visit APIs.yml URL](https://raw.githubusercontent.com/api-evangelist/peco-energy/refs/heads/main/apis.yml)

## Scope

- **Type:** Index
- **Position:** Consumer
- **Access:** 3rd-Party

## Tags

- Electric
- Energy
- Exelon
- Mobile App
- Natural Gas
- Pennsylvania
- Smart Meter
- Utility

## Timestamps

- **Created:** 2026-05-23
- **Modified:** 2026-05-23

## APIs


#### Tags

- Account Management, Billing, Customer Portal, Outages, Payments, Usage Data

#### Properties

- [Portal](https://secure.peco.com/MyAccount)
- [Documentation](https://www.peco.com/MyAccount)
- [Usage Data](https://www.peco.com/MyAccount/MyBillUsage/Pages/EnergyUsage.aspx)


#### Tags

- CSV, Energy Usage, Green Button, Interval Data, Self-Service, Smart Meter

#### Properties

- [Documentation](https://secure.peco.com/MyAccount/MyService/Pages/MyDataMyUsage.aspx)
- [Usage Data](https://www.peco.com/MyAccount/MyBillUsage/Pages/EnergyUsage.aspx)


#### Tags

- GIS, Outages, Public Data, Real Time, Storm Response

#### Properties

- [Outage Map](https://www.peco.com/SafetyCommunity/EmergencyPreparedness/PoweroutageMap)
- [Documentation](https://www.peco.com/SafetyCommunity/EmergencyPreparedness/Pages/OutageMap.aspx)


#### Tags

- Android, Apple Watch, Biometric, iOS, Mobile, Push Notifications

#### Properties

- [iOS App](https://apps.apple.com/us/app/peco/id1274171957)
- [Android App](https://play.google.com/store/apps/details?id=com.exelon.mobile.peco)

### Exelon Utilities Content API (Internal)
Shared Exelon Utilities backend (eudapi.peco.com) referenced by the PECO web portal's runtime configuration at https://www.peco.com/api/GetConfig (which exposes baseUrl, contentApiBaseUrl, euApiUrl, AITranslationAPI, and Oracle Digital Assistant / chatbot identifiers). Endpoints discovered include /content-api for portal content and /eult/translate for an AI-translation feature. The API is not documented publicly, returns 404 to anonymous probes for /swagger, /openapi.json, and similar discovery paths, and is intended only as the mobile and web frontend backend for Exelon's regulated utilities.

**Human URL:** [https://eudapi.peco.com](https://eudapi.peco.com)

#### Tags

- Content Delivery, Internal, Mobile Backend, Undocumented

#### Properties

- [BaseURL](https://eudapi.peco.com/content-api)
- [Configuration Endpoint](https://www.peco.com/api/GetConfig)
- [AI Translation Endpoint](https://eudapi.peco.com/eult/translate)

## Common Properties

- [Website](https://www.peco.com)
- [Customer Portal](https://secure.peco.com/MyAccount)
- [My Data Energy Usage](https://secure.peco.com/MyAccount/MyService/Pages/MyDataMyUsage.aspx)
- [Outage Map](https://www.peco.com/SafetyCommunity/EmergencyPreparedness/PoweroutageMap)
- [Smart Meters](https://www.peco.com/SmartIdeas/Pages/SmartMeters.aspx)
- [Smart Ideas Programs](https://www.peco.com/SmartIdeas)
- [Rates and Fees](https://www.peco.com/CustomerService/RatesandFees)
- [Assistance Programs](https://www.peco.com/CustomerService/AssistancePrograms)
- [Business Solutions](https://www.peco.com/Business/SmartBusinessSolutions)
- [iOS App](https://apps.apple.com/us/app/peco/id1274171957)
- [Android App](https://play.google.com/store/apps/details?id=com.exelon.mobile.peco)
- [Newsroom](https://www.peco.com/AboutUs/Pages/Newsroom.aspx)
- [Parent Company](https://www.exeloncorp.com)
- [Wikipedia](https://en.wikipedia.org/wiki/PECO_Energy_Company)

## Maintainers

**FN:** Kin Lane

**Email:** kin@apievangelist.com
