# Formance (formance)

Formance builds open-source financial infrastructure for money movement. The platform pairs a programmable double-entry Ledger (with the Numscript DSL) with a unified Payments connectivity layer and Flows orchestration, plus Wallets, Reconciliation, Auth, and Webhooks. It is delivered as open-source components and as a managed multi-tenant Formance Cloud, exposing REST APIs secured with OAuth2 client-credentials Bearer tokens.

**APIs.json:** [https://raw.githubusercontent.com/api-evangelist/formance/refs/heads/main/apis.yml](https://raw.githubusercontent.com/api-evangelist/formance/refs/heads/main/apis.yml)

## Tags

- Financial Infrastructure
- Ledger
- Double-Entry Accounting
- Payments
- Orchestration
- Money Movement
- Open Source
- Fintech

## Timestamps

- **Created:** 2026-07-01
- **Modified:** 2026-07-01

## Authentication

All Formance APIs are secured with OAuth2 client-credentials. Exchange a client id and secret at `POST /api/auth/oauth/token` for a Bearer access token, then send it as `Authorization: Bearer <token>` on every request. Modules are served under per-module path prefixes (for example `/api/ledger`, `/api/payments`) on a single Formance Cloud stack host, `https://{organization}.{environment}.formance.cloud`.

## APIs

### Formance Ledger API

The programmable, open-source double-entry Ledger (v2). Create ledgers, post immutable transactions with multi-posting sources and destinations, read accounts, balances, aggregated balances and volumes, attach metadata, revert transactions, and model complex money flows with the Numscript DSL. Supports bulk requests and a full transaction/account log.

- **Human URL:** [https://docs.formance.com/ledger](https://docs.formance.com/ledger)
- **Base URL:** `https://{organization}.{environment}.formance.cloud/api/ledger`

#### Tags

- Ledger
- Double-Entry Accounting
- Transactions
- Accounts
- Balances
- Numscript

#### Properties

- [Documentation](https://docs.formance.com/ledger)
- [API Reference](https://docs.formance.com/api)
- [OpenAPI](openapi/formance-openapi.yml) — [OpenAPI Specification](https://spec.openapis.org/oas/latest.html)
- [Postman Collection](collections/formance.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/formance.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)

### Formance Payments API

Unified Payments connectivity layer. Install and configure connectors to payment processors and banks (Stripe, Wise, Mangopay, Adyen, and more), ingest payments and accounts, manage bank accounts, initiate and manage transfers / payment initiations, and group accounts into pools with aggregated balances. Available as v1 and the expanded v3 API surface.

- **Human URL:** [https://docs.formance.com/payments](https://docs.formance.com/payments)
- **Base URL:** `https://{organization}.{environment}.formance.cloud/api/payments`

#### Tags

- Payments
- Connectors
- Bank Accounts
- Transfer Initiation
- Pools

#### Properties

- [Documentation](https://docs.formance.com/payments)
- [API Reference](https://docs.formance.com/api)
- [OpenAPI](openapi/formance-openapi.yml) — [OpenAPI Specification](https://spec.openapis.org/oas/latest.html)
- [Postman Collection](collections/formance.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/formance.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)

### Formance Orchestration API

Flows orchestration engine (v2) for composing durable financial workflows across the Ledger, Payments, and Wallets. Define and run workflows, inspect workflow instances and their stage history, and wire event-driven triggers that launch workflows in response to platform events.

- **Human URL:** [https://docs.formance.com/flows](https://docs.formance.com/flows)
- **Base URL:** `https://{organization}.{environment}.formance.cloud/api/orchestration`

#### Tags

- Orchestration
- Flows
- Workflows
- Triggers
- Money Movement

#### Properties

- [Documentation](https://docs.formance.com/flows)
- [API Reference](https://docs.formance.com/api)
- [OpenAPI](openapi/formance-openapi.yml) — [OpenAPI Specification](https://spec.openapis.org/oas/latest.html)
- [Postman Collection](collections/formance.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/formance.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)

### Formance Wallets API

White-label Wallets service built on top of the Ledger. Create and list wallets and named balances, credit and debit wallets, place and confirm or void holds (authorization-then-capture), and read wallet summaries, balances, and transactions.

- **Human URL:** [https://docs.formance.com/wallets](https://docs.formance.com/wallets)
- **Base URL:** `https://{organization}.{environment}.formance.cloud/api/wallets`

#### Tags

- Wallets
- Balances
- Holds
- Credit
- Debit

#### Properties

- [Documentation](https://docs.formance.com/wallets)
- [API Reference](https://docs.formance.com/api)
- [OpenAPI](openapi/formance-openapi.yml) — [OpenAPI Specification](https://spec.openapis.org/oas/latest.html)
- [Postman Collection](collections/formance.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/formance.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)

### Formance Reconciliation API

Reconciliation toolkit for auditing assets under management. Define reconciliation policies, run reconciliations that compare Ledger balances against payments-side balances at a point in time, and list or retrieve reconciliation results.

- **Human URL:** [https://docs.formance.com/reconciliation](https://docs.formance.com/reconciliation)
- **Base URL:** `https://{organization}.{environment}.formance.cloud/api/reconciliation`

#### Tags

- Reconciliation
- Policies
- Audit
- Assets Under Management

#### Properties

- [Documentation](https://docs.formance.com/reconciliation)
- [API Reference](https://docs.formance.com/api)
- [OpenAPI](openapi/formance-openapi.yml) — [OpenAPI Specification](https://spec.openapis.org/oas/latest.html)
- [Postman Collection](collections/formance.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/formance.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)

### Formance Auth API

OAuth2 / OIDC authorization server for the platform. Issue client-credentials access tokens, manage OAuth clients and their secrets, list users, and read the OpenID Connect well-known configuration used to secure every other Formance API.

- **Human URL:** [https://docs.formance.com/security](https://docs.formance.com/security)
- **Base URL:** `https://{organization}.{environment}.formance.cloud/api/auth`

#### Tags

- Auth
- OAuth2
- Clients
- Identity
- OIDC

#### Properties

- [Documentation](https://docs.formance.com/security)
- [API Reference](https://docs.formance.com/api)
- [OpenAPI](openapi/formance-openapi.yml) — [OpenAPI Specification](https://spec.openapis.org/oas/latest.html)
- [Postman Collection](collections/formance.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/formance.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)

### Formance Webhooks API

Manage webhook subscriptions that deliver platform events (ledger, payments, wallets, and orchestration) to your endpoints. Insert and list configs, activate or deactivate them, rotate signing secrets, and send test events.

- **Human URL:** [https://docs.formance.com/webhooks](https://docs.formance.com/webhooks)
- **Base URL:** `https://{organization}.{environment}.formance.cloud/api/webhooks`

#### Tags

- Webhooks
- Events
- Subscriptions

#### Properties

- [Documentation](https://docs.formance.com/webhooks)
- [API Reference](https://docs.formance.com/api)
- [OpenAPI](openapi/formance-openapi.yml) — [OpenAPI Specification](https://spec.openapis.org/oas/latest.html)
- [Postman Collection](collections/formance.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/formance.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)

### Formance Search API

Full-platform Search service that indexes ledger transactions and accounts, payments, and other resources so they can be queried across modules from a single endpoint, with a target/terms query model.

- **Human URL:** [https://docs.formance.com/search](https://docs.formance.com/search)
- **Base URL:** `https://{organization}.{environment}.formance.cloud/api/search`

#### Tags

- Search
- Indexing
- Query

#### Properties

- [Documentation](https://docs.formance.com/search)
- [API Reference](https://docs.formance.com/api)
- [OpenAPI](openapi/formance-openapi.yml) — [OpenAPI Specification](https://spec.openapis.org/oas/latest.html)
- [Postman Collection](collections/formance.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/formance.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)

## Common Properties

- [GitHub Organization](https://github.com/formancehq)
- [LinkedIn](https://www.linkedin.com/company/formance)
- [Website](https://www.formance.com)
- [Documentation](https://docs.formance.com)
- [Plans](plans/formance-plans-pricing.yml)
- [Rate Limits](rate-limits/formance-rate-limits.yml)
- [Fin Ops](finops/formance-finops.yml)

## Maintainers

**FN:** Kin Lane
**Email:** kin@apievangelist.com
