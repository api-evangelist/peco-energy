# PECO Energy (peco-energy)

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

### PECO My Account Customer Portal
Authenticated customer self-service portal hosted at secure.peco.com that lets residential and small-business customers view and pay bills, schedule payments, enroll in AutoPay and Budget Billing, report and track outages, manage alerts, and view interval and monthly energy usage. The portal is a JavaScript single-page application backed by the internal Exelon Utilities API platform (eudapi.peco.com); no public OpenAPI specification or developer credentials are published.

**Human URL:** [https://secure.peco.com/MyAccount](https://secure.peco.com/MyAccount)

#### Tags

- Account Management, Billing, Customer Portal, Outages, Payments, Usage Data

#### Properties

- [Portal](https://secure.peco.com/MyAccount)
- [Documentation](https://www.peco.com/MyAccount)
- [Usage Data](https://www.peco.com/MyAccount/MyBillUsage/Pages/EnergyUsage.aspx)

### PECO My Data / Energy Usage Export
Customer-driven My Data / Energy Usage export inside the PECO My Account portal, providing smart-meter interval, daily, and monthly usage views with download options for the authenticated account holder. This is the mechanism PECO offers customers to obtain their own usage data; PECO does not publish a documented Green Button Connect My Data third-party API, so programmatic third-party access typically goes through customer credential sharing with utility-data aggregators (UtilityAPI, Arcadia, legacy Urjanet) under Pennsylvania PUC customer-data rules.

**Human URL:** [https://secure.peco.com/MyAccount/MyService/Pages/MyDataMyUsage.aspx](https://secure.peco.com/MyAccount/MyService/Pages/MyDataMyUsage.aspx)

#### Tags

- CSV, Energy Usage, Green Button, Interval Data, Self-Service, Smart Meter

#### Properties

- [Documentation](https://secure.peco.com/MyAccount/MyService/Pages/MyDataMyUsage.aspx)
- [Usage Data](https://www.peco.com/MyAccount/MyBillUsage/Pages/EnergyUsage.aspx)

### PECO Outage Map
Public county- and ZIP-level outage map showing active electric outages across PECO's southeastern Pennsylvania service territory, with customer counts affected, estimated restoration, and crew status. The map is browser-rendered; PECO does not publish an outage feed (XML/JSON/CAP) for third-party consumption, so outage data is available only through the map UI and customer-facing alert subscriptions (SMS / email / push via the mobile app).

**Human URL:** [https://www.peco.com/SafetyCommunity/EmergencyPreparedness/PoweroutageMap](https://www.peco.com/SafetyCommunity/EmergencyPreparedness/PoweroutageMap)

#### Tags

- GIS, Outages, Public Data, Real Time, Storm Response

#### Properties

- [Outage Map](https://www.peco.com/SafetyCommunity/EmergencyPreparedness/PoweroutageMap)
- [Documentation](https://www.peco.com/SafetyCommunity/EmergencyPreparedness/Pages/OutageMap.aspx)

### PECO Mobile Apps (iOS and Android)
Native iOS (App Store id 1274171957) and Android (com.exelon.mobile.peco) mobile apps providing biometric sign-in, bill pay, outage reporting, outage map, usage and bill comparison, alerts, multi-account management, and Apple Watch support. Per the iOS listing: "Secure, easy, convenient, PECO's free mobile app allows you to easily access and manage your residential or business account on the go." The apps consume the same internal Exelon Utilities API (eudapi.peco.com) that powers the web portal and are the primary mobile entry point for PECO customers; no public SDK is offered.

**Human URL:** [https://apps.apple.com/us/app/peco/id1274171957](https://apps.apple.com/us/app/peco/id1274171957)

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
