# Beds24 (beds24)

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
