# Beds24

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

Beds24 is a vacation rental and hotel channel manager, property management system (PMS), and online booking engine. It synchronizes availability, rates, and reservations across OTAs such as Booking.com, Airbnb, Expedia, Vrbo, and Google, and exposes a documented REST API (v2 at api.beds24.com/v2, with a legacy JSON/XML v1) for reading and writing bookings, properties, room inventory, availability calendars, prices, invoices, channels, and account data. API V2 uses expiring access tokens generated from refresh tokens, scoped permissions, optional IP whitelisting, and a credit-based rate limit enforced per account over a rolling 5-minute window.

**Areas:** Vacation Rentals · Hotels · Channel Manager · Property Management System · Booking Engine · Hospitality · Reservations

## Beds24 on APIs.io

Everything profiled for Beds24 is published on APIs.io rather than in this repository. Start at the provider page — **[apis.io/providers/beds24/](https://apis.io/providers/beds24/)** — or go straight to one of the APIs or properties below.

### APIs (8)

- [Beds24 Accounts API](https://apis.io/apis/beds24/beds24-accounts-api/) — Account-level information, sub-accounts, and users.
- [Beds24 Authentication API](https://apis.io/apis/beds24/beds24-authentication-api/) — Refresh and access token management and diagnostics.
- [Beds24 Bookings API](https://apis.io/apis/beds24/beds24-bookings-api/) — Read, create, and modify reservations across all channels.
- [Beds24 Channels API](https://apis.io/apis/beds24/beds24-channels-api/) — OTA channel connection and mapping management.
- [Beds24 Inventory API](https://apis.io/apis/beds24/beds24-inventory-api/) — Per-day availability calendar, availability status, and fixed prices.
- [Beds24 Invoices API](https://apis.io/apis/beds24/beds24-invoices-api/) — Invoice items, charges, and payments attached to bookings.
- [Beds24 Messages API](https://apis.io/apis/beds24/beds24-messages-api/) — Guest and channel messages attached to bookings.
- [Beds24 Properties API](https://apis.io/apis/beds24/beds24-properties-api/) — Property and room configuration and bookable offers.

### Published properties

Each property below is a page on APIs.io carrying the machine-readable artifact and what it says.

#### Agentic access (1)

Which operations an agent can call, which act, and which need a human in the loop.

- [Beds24 Agentic Access](https://apis.io/agentic-access/beds24/beds24-agentic-access/)

#### Collections (9)

Postman and Open Collection request collections.

- [Beds24 API V2](https://apis.io/collections/beds24/open-beds24/)
- [Beds24 API V2 Accounts API](https://apis.io/collections/beds24/open-beds24-accounts-api/)
- [Beds24 API V2 Accounts Authentication API](https://apis.io/collections/beds24/open-beds24-authentication-api/)
- [Beds24 API V2 Accounts Bookings API](https://apis.io/collections/beds24/open-beds24-bookings-api/)
- [Beds24 API V2 Accounts Channels API](https://apis.io/collections/beds24/open-beds24-channels-api/)
- [Beds24 API V2 Accounts Inventory API](https://apis.io/collections/beds24/open-beds24-inventory-api/)
- [Beds24 API V2 Accounts Invoices API](https://apis.io/collections/beds24/open-beds24-invoices-api/)
- [Beds24 API V2 Accounts Messages API](https://apis.io/collections/beds24/open-beds24-messages-api/)
- [Beds24 API V2 Accounts Properties API](https://apis.io/collections/beds24/open-beds24-properties-api/)

#### Security (2)

Authentication, trust centre, and vulnerability disclosure.

- [Beds24 Authentication](https://apis.io/security/beds24/beds24-authentication/)
- [Beds24 Domain Security](https://apis.io/security/beds24/beds24-domain-security/)

#### Plans and pricing (1)

Published plans, tiers and prices.

- [Beds24 Plans Pricing](https://apis.io/plans/beds24/beds24-plans-pricing/)

#### Rate limits (1)

Published request limits.

- [Beds24 Rate Limits](https://apis.io/rate-limits/beds24/beds24-rate-limits/)

#### FinOps (1)

What the API costs to run, by operation.

- [Beds24 Finops](https://apis.io/finops/beds24/beds24-finops/)

## Where to find this API

Links to the company's own pages. This repository publishes no copy of their specifications — the canonical document is theirs and lives at the URLs below.

- [Website](https://beds24.com)
- [Documentation](https://wiki.beds24.com/index.php/Category:API_V2)
- [Blog](https://beds24.com/en/company/blog)

## API Evangelist rating

**Kin Score 27.2** — thin · rubric 0.24.0 · scored 2026-10-17

| Facet | Score |
|---|---|
| Discoverability | 66.1 |
| Contract quality | 51.1 |
| Contract governance | 0.0 |
| Operational transparency | 7.9 |
| Developer ergonomics | 32.1 |
| Access clarity | 7.9 |

**Agent readiness 17.9** — agent-aware

| Agent-readiness dimension | Result |
|---|---|
| Spec Presence | yes |
| Agentic Access | derived (partial credit) |
| Reversibility Documented | — |
| MCP Server | — |
| Auth Clarity | bearer (partial credit) |
| Idempotency | — |
| Error Semantics | — |
| OpenAPI Examples | — |
| Rate Limit Signal | derived (partial credit) |
| Event Surface Described | — |
| Agent Skills | — |
| Well Known Catalog | — |
| Consent Identity | — |
| Agent Card | — |
| Dry Run Mode | — |
| Delegated Identity | — |
| Protected Resource Metadata | — |
| Dynamic Client Registration | — |
| Agentic Commerce | — |

**Regulatory alignment 11.8** — Horizontal (data, software, accessibility, platform)

The rubric is published at [github.com/api-evangelist/kin-score](https://github.com/api-evangelist/kin-score). The per-check breakdown behind these numbers — which checks were earned, partial or missed — along with score history and how this provider compares to its peers, is available at [apis.io/providers/beds24/](https://apis.io/providers/beds24/).

## How this profile is made

API Evangelist profiles a company's public API surface the way a developer would find it: the website, developer portal and documentation, the specifications it publishes, its public repositories, and its pricing, status and changelog pages. From that it derives the properties above — contracts split per API, workflows, schemas, collections, governance rules, plans and rate limits — and scores them against the published [Kin Score rubric](https://github.com/api-evangelist/kin-score).

The artifacts are published on [APIs.io](https://apis.io), not in this repository. This repository is the public record for Beds24: the place to say something is wrong, missing or out of date, and to ask for a re-score or a removal.

## Open an issue

- **Something about this listing** — a wrong description, a missing API, a stale artifact or a question about the rating: [open an issue on this repository](https://github.com/api-evangelist/beds24/issues/new).
- **A new API, or one that is not in the catalog yet** — [submit it on APIs.io](https://apis.io/add/).
- **Anything else** — [the APIs.io inbox](https://github.com/api-search/inbox/issues/new) or [info@apievangelist.com](mailto:info@apievangelist.com).
