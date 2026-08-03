# Beds24 (beds24)

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

Beds24 is a vacation rental and hotel channel manager, property management system (PMS), and online booking engine. It synchronizes availability, rates, and reservations across OTAs such as Booking.com, Airbnb, Expedia, Vrbo, and Google, and exposes a documented REST API (v2 at `api.beds24.com/v2`, plus a legacy JSON/XML v1) for reading and writing bookings, properties, room inventory, availability calendars, prices, invoices, channels, and account data. API V2 uses expiring access tokens generated from refresh tokens, scoped permissions, optional IP whitelisting, and a credit-based rate limit enforced per account over a rolling 5-minute window.

**APIs.json:** [https://raw.githubusercontent.com/api-evangelist/beds24/refs/heads/main/apis.yml](https://raw.githubusercontent.com/api-evangelist/beds24/refs/heads/main/apis.yml)

## Tags

- Vacation Rental
- Hotel
- Channel Manager
- Property Management System
- Booking Engine
- Hospitality
- Reservations

## Timestamps

- **Created:** 2026-07-03
- **Modified:** 2026-07-03

## Authentication

API V2 is token based. An invite code (created in SETTINGS > ACCOUNT > ACCESS) is exchanged for a long-life refresh token via `GET /authentication/setup`; the refresh token generates short-lived access tokens via `GET /authentication/token`. The access token is sent in the `token` request header. A read-only long-life token is also available. Each API category except `/authentication` requires a matching scope.

## Rate Limits

Usage is governed by an account-level credit limit over a rolling 5-minute window (default 100 credits). Each request deducts credits based on its cost, reported via the `x-five-min-limit-remaining`, `x-five-min-limit-resets-in`, and `x-request-cost` response headers. Tokens under the same account share one pool; separate accounts and sub-accounts have their own.

## APIs

### Beds24 Authentication API

Exchange an invite code for a long-life refresh token, generate short-lived access tokens from that refresh token, inspect token scopes and diagnostics, and revoke tokens. Access tokens are sent in the `token` request header and each API category requires a matching scope.

- **Human URL:** [https://wiki.beds24.com/index.php/Category:API_V2](https://wiki.beds24.com/index.php/Category:API_V2)
- **Base URL:** `https://api.beds24.com/v2`

#### Tags

- Authentication
- Tokens
- OAuth

#### Properties

- [Documentation](https://beds24.com/developer-api.html)
- [API Reference](https://wiki.beds24.com/index.php/Category:API_V2)
- [OpenAPI](openapi/beds24-openapi.yml) — [OpenAPI Specification](https://spec.openapis.org/oas/latest.html)
- [Postman Collection](collections/beds24.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/beds24.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)

### Beds24 Bookings API

Search, read, create, and modify reservations across all connected channels - filter bookings by property, room, arrival/departure, status, and modification time, and write new or updated bookings, guest details, statuses, and booking-level notes and info items.

- **Human URL:** [https://wiki.beds24.com/index.php/Category:API_V2](https://wiki.beds24.com/index.php/Category:API_V2)
- **Base URL:** `https://api.beds24.com/v2`

#### Tags

- Bookings
- Reservations
- Guests

#### Properties

- [API Reference](https://wiki.beds24.com/index.php/Category:API_V2)
- [OpenAPI](openapi/beds24-openapi.yml) — [OpenAPI Specification](https://spec.openapis.org/oas/latest.html)
- [Postman Collection](collections/beds24.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/beds24.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)

### Beds24 Invoices & Charges API

Read and write the invoice items, charges, and payments attached to a booking - line-item description, quantity, price, type, and VAT - so external accounting and payment tooling can reconcile guest financials held in Beds24.

- **Human URL:** [https://wiki.beds24.com/index.php/Category:API_V2](https://wiki.beds24.com/index.php/Category:API_V2)
- **Base URL:** `https://api.beds24.com/v2`

#### Tags

- Invoices
- Payments
- Charges

#### Properties

- [API Reference](https://wiki.beds24.com/index.php/Category:API_V2)
- [OpenAPI](openapi/beds24-openapi.yml) — [OpenAPI Specification](https://spec.openapis.org/oas/latest.html)
- [Postman Collection](collections/beds24.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/beds24.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)

### Beds24 Booking Messages API

Retrieve and post guest and channel messages associated with a booking, enabling two-way messaging with guests and OTAs (for example Booking.com and Airbnb) from an external inbox or automation.

- **Human URL:** [https://wiki.beds24.com/index.php/Category:API_V2](https://wiki.beds24.com/index.php/Category:API_V2)
- **Base URL:** `https://api.beds24.com/v2`

#### Tags

- Messages
- Guest Communication
- Notifications

#### Properties

- [API Reference](https://wiki.beds24.com/index.php/Category:API_V2)
- [OpenAPI](openapi/beds24-openapi.yml) — [OpenAPI Specification](https://spec.openapis.org/oas/latest.html)
- [Postman Collection](collections/beds24.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/beds24.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)

### Beds24 Properties API

List and read property and room configuration - names, room types, units, descriptions, texts, settings, and bookable offers - and create or modify properties and rooms, providing the structural catalog behind availability and pricing.

- **Human URL:** [https://wiki.beds24.com/index.php/Category:API_V2](https://wiki.beds24.com/index.php/Category:API_V2)
- **Base URL:** `https://api.beds24.com/v2`

#### Tags

- Properties
- Rooms
- Configuration

#### Properties

- [API Reference](https://wiki.beds24.com/index.php/Category:API_V2)
- [OpenAPI](openapi/beds24-openapi.yml) — [OpenAPI Specification](https://spec.openapis.org/oas/latest.html)
- [Postman Collection](collections/beds24.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/beds24.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)

### Beds24 Availability & Calendar API

Read and write per-day room inventory - the calendar of number of units available, min/max stay, and open/close status - via the inventory calendar and availability endpoints. Retrieve one year at a time to cache locally, and push availability updates back to synchronize channels.

- **Human URL:** [https://wiki.beds24.com/index.php/Category:API_V2](https://wiki.beds24.com/index.php/Category:API_V2)
- **Base URL:** `https://api.beds24.com/v2`

#### Tags

- Availability
- Calendar
- Inventory

#### Properties

- [API Reference](https://wiki.beds24.com/index.php/Category:API_V2)
- [OpenAPI](openapi/beds24-openapi.yml) — [OpenAPI Specification](https://spec.openapis.org/oas/latest.html)
- [Postman Collection](collections/beds24.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/beds24.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)

### Beds24 Rates & Prices API

Manage per-day prices in the inventory calendar and the fixed price rules and bookable offers that drive channel and booking-engine pricing - list, create, update, and delete fixed prices, and set daily rates alongside availability.

- **Human URL:** [https://wiki.beds24.com/index.php/Category:API_V2](https://wiki.beds24.com/index.php/Category:API_V2)
- **Base URL:** `https://api.beds24.com/v2`

#### Tags

- Rates
- Prices
- Offers

#### Properties

- [API Reference](https://wiki.beds24.com/index.php/Category:API_V2)
- [OpenAPI](openapi/beds24-openapi.yml) — [OpenAPI Specification](https://spec.openapis.org/oas/latest.html)
- [Postman Collection](collections/beds24.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/beds24.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)

### Beds24 Channels API

Manage OTA channel connections and mappings that distribute inventory to Booking.com, Airbnb, Expedia, Vrbo, and other portals - reading channel configuration and pushing the room, rate, and availability mappings that keep external listings in sync.

- **Human URL:** [https://wiki.beds24.com/index.php/OTAs:_How_to_connect_to_Beds24_using_API_V2](https://wiki.beds24.com/index.php/OTAs:_How_to_connect_to_Beds24_using_API_V2)
- **Base URL:** `https://api.beds24.com/v2`

#### Tags

- Channels
- OTA
- Distribution

#### Properties

- [Documentation](https://wiki.beds24.com/index.php/OTAs:_How_to_connect_to_Beds24_using_API_V2)
- [OpenAPI](openapi/beds24-openapi.yml) — [OpenAPI Specification](https://spec.openapis.org/oas/latest.html)
- [Postman Collection](collections/beds24.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/beds24.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)

### Beds24 Accounts API

Read account-level information and manage sub-accounts and users - surfacing the account context, permissions, and structure that scope every other API category and its shared credit-based rate limit.

- **Human URL:** [https://wiki.beds24.com/index.php/Category:API_V2](https://wiki.beds24.com/index.php/Category:API_V2)
- **Base URL:** `https://api.beds24.com/v2`

#### Tags

- Accounts
- Users
- Management

#### Properties

- [API Reference](https://wiki.beds24.com/index.php/Category:API_V2)
- [OpenAPI](openapi/beds24-openapi.yml) — [OpenAPI Specification](https://spec.openapis.org/oas/latest.html)
- [Postman Collection](collections/beds24.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/beds24.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)

## Common Properties

- [LinkedIn](https://www.linkedin.com/company/beds24)
- [Website](https://beds24.com)
- [Documentation](https://wiki.beds24.com/index.php/Category:API_V2)
- [Plans](plans/beds24-plans-pricing.yml)
- [Rate Limits](rate-limits/beds24-rate-limits.yml)
- [Fin Ops](finops/beds24-finops.yml)

## Maintainers

**FN:** Kin Lane
**Email:** kin@apievangelist.com
