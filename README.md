# Reggora (reggora)

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
