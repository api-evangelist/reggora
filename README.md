# Reggora

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

Reggora is a modern appraisal management platform that connects mortgage lenders and appraisal vendors on a single system, automating the appraisal lifecycle from order placement and product selection through payment, document submission, revision review, and delivery back into the loan origination system (LOS). Reggora exposes a documented Lender API and Vendor API so lenders can manage 100% of their appraisal orders directly from their own LOS or proprietary tech stack. All key platform functionality is available via secure REST endpoints (JWT bearer token plus a per-integration API key), with sandbox and production environments and webhook callbacks for loan and order events. Endpoint paths in this catalog are modeled from Reggora's documented resource areas; the full reference is partner-facing at api.reggora.io/docs.

**Areas:** Appraisal Management · Mortgage · Lending · Real Estate · Valuation · Loan Origination · LOS Integration · Fintech

## Reggora on APIs.io

Everything profiled for Reggora is published on APIs.io rather than in this repository. Start at the provider page — **[apis.io/providers/reggora/](https://apis.io/providers/reggora/)** — or go straight to one of the APIs or properties below.

### APIs (8)

- [Reggora Loans API](https://apis.io/apis/reggora/reggora-loans-api/) — Create and manage the loan records that appraisal orders are placed against - sync loan data from the LOS, retrieve loan detail, update loan fields, and…
- [Reggora Orders (Appraisals) API](https://apis.io/apis/reggora/reggora-orders-api/) — Place appraisal orders against a loan, list and retrieve orders, track order status through the appraisal lifecycle, and manage order-level actions.…
- [Reggora Products API](https://apis.io/apis/reggora/reggora-products-api/) — List the appraisal products (report types and associated fees) a lender has configured so an integration can present valid product options when placing an…
- [Reggora Submissions & Revisions API](https://apis.io/apis/reggora/reggora-submissions-revisions-api/) — Retrieve appraisal report submissions on an order, request and track revisions, and drive the document review workflow between lender and vendor. Endpoints…
- [Reggora Documents (eVault) API](https://apis.io/apis/reggora/reggora-documents-evault-api/) — Access the eVault to list, upload, and download appraisal documents and supporting files associated with an order. Endpoints modeled from Reggora's…
- [Reggora Vendors & Branches API](https://apis.io/apis/reggora/reggora-vendors-branches-api/) — Manage the appraisal vendors (appraisers and AMCs) a lender works with and the lender's branch structure used to route and assign orders. Endpoints modeled…
- [Reggora Users & Authentication API](https://apis.io/apis/reggora/reggora-users-auth-api/) — Authenticate integrations with a JWT bearer token plus a per-integration API key, and manage the lender users that act within the platform. Endpoints…
- [Reggora Webhook Events API](https://apis.io/apis/reggora/reggora-webhooks-api/) — Subscribe to server-to-server webhook callbacks that notify an integration when an order is created or updated and when a loan is deleted. Delivery is HTTP…

### Published properties

Each property below is a page on APIs.io carrying the machine-readable artifact and what it says.

#### Security (2)

Authentication, trust centre, and vulnerability disclosure.

- [Reggora Domain Security](https://apis.io/security/reggora/reggora-domain-security/)
- [Reggora Trust Center](https://apis.io/security/reggora/reggora-trust-center/)

#### Plans and pricing (1)

Published plans, tiers and prices.

- [Reggora Plans Pricing](https://apis.io/plans/reggora/reggora-plans-pricing/)

#### Rate limits (1)

Published request limits.

- [Reggora Rate Limits](https://apis.io/rate-limits/reggora/reggora-rate-limits/)

#### FinOps (1)

What the API costs to run, by operation.

- [Reggora Finops](https://apis.io/finops/reggora/reggora-finops/)

## Where to find this API

Links to the company's own pages. This repository publishes no copy of their specifications — the canonical document is theirs and lives at the URLs below.

- [Website](https://www.reggora.com)
- [Documentation](https://api.reggora.io/docs/)
- [Blog](https://www.reggora.com/blog)

## API Evangelist rating

**Kin Score 13.5** — emerging · rubric 0.24.0 · scored 2026-10-17

| Facet | Score |
|---|---|
| Discoverability | 71.4 |
| Contract quality | 0.0 |
| Contract governance | 0.0 |
| Operational transparency | 7.9 |
| Developer ergonomics | 16.7 |
| Access clarity | 13.2 |

**Agent readiness 0.6** — human-only

| Agent-readiness dimension | Result |
|---|---|
| Spec Presence | — |
| Agentic Access | — |
| Reversibility Documented | — |
| MCP Server | — |
| Auth Clarity | — |
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

**Regulatory alignment 10.8** — Horizontal (data, software, accessibility, platform)

The rubric is published at [github.com/api-evangelist/kin-score](https://github.com/api-evangelist/kin-score). The per-check breakdown behind these numbers — which checks were earned, partial or missed — along with score history and how this provider compares to its peers, is available at [apis.io/providers/reggora/](https://apis.io/providers/reggora/).

## How this profile is made

API Evangelist profiles a company's public API surface the way a developer would find it: the website, developer portal and documentation, the specifications it publishes, its public repositories, and its pricing, status and changelog pages. From that it derives the properties above — contracts split per API, workflows, schemas, collections, governance rules, plans and rate limits — and scores them against the published [Kin Score rubric](https://github.com/api-evangelist/kin-score).

The artifacts are published on [APIs.io](https://apis.io), not in this repository. This repository is the public record for Reggora: the place to say something is wrong, missing or out of date, and to ask for a re-score or a removal.

## Open an issue

- **Something about this listing** — a wrong description, a missing API, a stale artifact or a question about the rating: [open an issue on this repository](https://github.com/api-evangelist/reggora/issues/new).
- **A new API, or one that is not in the catalog yet** — [submit it on APIs.io](https://apis.io/add/).
- **Anything else** — [the APIs.io inbox](https://github.com/api-search/inbox/issues/new) or [info@apievangelist.com](mailto:info@apievangelist.com).
