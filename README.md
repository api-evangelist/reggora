# Reggora (reggora)

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

Reggora is a modern appraisal management platform that connects mortgage lenders and appraisal vendors on a single, intelligent system. It automates the appraisal lifecycle - order placement, product selection, payment, scheduling, document submission, revision review, and delivery - and pushes results back into the lender's loan origination system (LOS). Reggora publishes a documented **Lender API** and **Vendor API** so lenders can manage 100% of their appraisal orders directly from their own LOS or proprietary tech stack.

**APIs.json:** [https://raw.githubusercontent.com/api-evangelist/reggora/refs/heads/main/apis.yml](https://raw.githubusercontent.com/api-evangelist/reggora/refs/heads/main/apis.yml)

## Access Model (Read This First)

Reggora's API is **real and documented, but partner/customer-facing** rather than open self-serve:

- The reference is published at [https://api.reggora.io/docs/](https://api.reggora.io/docs/) (the developer portal at `developer.reggora.io` redirects there).
- Requests authenticate with a **JWT bearer token plus a per-integration API key** header. Those credentials are provisioned to contracted lenders and vendors - there is no public self-service signup for keys.
- There are **sandbox** and **production** environments:
  - Lender (production): `https://api.reggora.io/lender/`
  - Vendor (production): `https://api.reggora.io/vendor/`
  - Sandbox: `https://sandbox.reggora.io/lender/` and `https://sandbox.reggora.io/vendor/`
- A public OpenAPI/JSON definition is **not** available (the `openapi.json` path returns 403), and the reference is rendered by a single-page app, so exact endpoint paths could not be scraped verbatim.

Because of that, the logical APIs and endpoints in this catalog entry are **modeled** (`endpointsModeled: true`) from Reggora's documented resource areas - loans, orders, products, submissions, revisions, documents/eVault, vendors, branches, users, and webhooks - rather than copied path-for-path from a public spec. Treat the base URLs and auth model as confirmed and the individual endpoint paths as representative.

## Tags

- Appraisal Management
- Mortgage
- Lending
- Real Estate
- Valuation
- Loan Origination
- LOS Integration
- Fintech

## Timestamps

- **Created:** 2026-07-04
- **Modified:** 2026-07-04

## APIs

Base URL (Lender API, production): `https://api.reggora.io/lender`

### Reggora Loans API

Create and manage the loan records that appraisal orders are placed against - sync loan data from the LOS, retrieve loan detail, update fields, and receive a webhook when a loan is deleted.

### Reggora Orders (Appraisals) API

Place appraisal orders against a loan, list and retrieve orders, and track order status through the appraisal lifecycle. Order-created and order-updated events are delivered via webhooks.

### Reggora Products API

List the appraisal products (report types and associated fees) a lender has configured, so an integration can present valid product options when placing an order.

### Reggora Submissions & Revisions API

Retrieve appraisal report submissions on an order, request and track revisions, and drive the document review workflow between lender and vendor.

### Reggora Documents (eVault) API

Access the eVault to list, upload, and download appraisal documents and supporting files associated with an order.

### Reggora Vendors & Branches API

Manage the appraisal vendors (appraisers and AMCs) a lender works with and the lender's branch structure used to route and assign orders.

### Reggora Users & Authentication API

Authenticate integrations with a JWT bearer token plus a per-integration API key, and manage the lender users that act within the platform.

### Reggora Webhook Events API

Subscribe to server-to-server webhook callbacks that fire when an order is created or updated and when a loan is deleted. Delivery is HTTP POST to a configured endpoint URL - **not** a WebSocket.

## Common Properties

- [LinkedIn](https://www.linkedin.com/company/reggora)
- [Website](https://www.reggora.com)
- [Documentation](https://api.reggora.io/docs/)
- [Plans](plans/reggora-plans-pricing.yml)
- [Rate Limits](rate-limits/reggora-rate-limits.yml)
- [Fin Ops](finops/reggora-finops.yml)
- [Blog](https://www.reggora.com/blog)

## Pricing

Reggora does not publish public per-seat or per-call API pricing. It is sold as a platform to lenders (and is free to appraisal vendors who receive orders) via a **contact-sales** model, typically framed around cost-per-loan savings - Reggora cites roughly **$258 saved per loan** from automating appraisal order management and quality control. See [plans/reggora-plans-pricing.yml](plans/reggora-plans-pricing.yml).

## Maintainers

**FN:** Kin Lane
**Email:** kin@apievangelist.com
