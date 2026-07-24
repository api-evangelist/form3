# Form3 (form3)

Form3 is a United Kingdom-headquartered, cloud-native payments technology company offering account-to-account payment processing as a single, unified REST API to banks and fintechs. Founded in 2016 and based in London, Form3 runs a fully managed Payments-as-a-Service platform connecting customers to domestic and cross-border schemes — UK Faster Payments, Bacs and CHAPS, SEPA Credit Transfer, SEPA Instant and SEPA Direct Debit, and US instant rails — alongside Confirmation of Payee / Verification of Payee name-checking, direct debit mandate management, scheme-addressable account identification, event notifications (webhooks), and full audit trails.

The public API is REST built on the [json:api](https://jsonapi.org/) specification, documented at [api-docs.form3.tech](https://www.api-docs.form3.tech/) with a downloadable Swagger 2.0 definition (host `api.form3.tech`, basePath `/v1`, 163 paths). Authentication is OAuth2 client-credentials plus HTTP Message Signatures request signing, with mutual TLS supported in some environments. Form3 is API-native and developer-facing, but is a regulated B2B rail rather than an open self-serve signup product — production access is contracted.

**APIs.json:** [https://raw.githubusercontent.com/api-evangelist/form3/refs/heads/main/apis.yml](https://raw.githubusercontent.com/api-evangelist/form3/refs/heads/main/apis.yml)

## Tags

- Payments
- United Kingdom
- Payment Processing
- Account-to-Account
- Real-Time Payments
- Faster Payments
- Bacs
- SEPA
- Direct Debit
- Confirmation of Payee
- Cross-Border
- Banking-as-a-Service
- Embedded Payments

## Timestamps

- **Created:** 2026-07-24
- **Modified:** 2026-07-24

## APIs

### Form3 Public API

The unified Form3 Public API — a single REST API built on the json:api specification that connects banks and fintechs to domestic and cross-border payment schemes. Swagger 2.0, 163 documented paths.

- **Human URL:** [https://www.api-docs.form3.tech/](https://www.api-docs.form3.tech/)
- **Base URL:** `https://api.form3.tech/v1`
- [OpenAPI](openapi/form3-payments.yml)
- [API Reference](https://api-docs.form3.tech/api.html)
- [Getting Started](https://www.api-docs.form3.tech/api/tutorials/getting-started/introduction)

### Form3 Payments API

Send and receive account-to-account payments across UK Faster Payments, Bacs, CHAPS, SEPA and US instant rails, and handle exceptions (rejections, returns, reversals, recalls).

- **Human URL:** [https://www.api-docs.form3.tech/api/tutorials/getting-started/send-a-payment](https://www.api-docs.form3.tech/api/tutorials/getting-started/send-a-payment)
- **Base URL:** `https://api.form3.tech/v1`
- [OpenAPI](openapi/form3-payments.yml)

### Form3 Direct Debits & Mandates API

Originate and receive Bacs and SEPA direct debits, manage mandates, and process indemnity claims.

- **Human URL:** [https://www.api-docs.form3.tech/api/tutorials/bacs/direct-debit-instructions-for-originators](https://www.api-docs.form3.tech/api/tutorials/bacs/direct-debit-instructions-for-originators)
- **Base URL:** `https://api.form3.tech/v1`
- [OpenAPI](openapi/form3-payments.yml)

### Form3 Account Identification & Verification API

Generate scheme-addressable account numbers, validate UK sort code / account number pairs, and run Confirmation of Payee / Verification of Payee name-checking.

- **Human URL:** [https://www.api-docs.form3.tech/api/tutorials/confirmation-of-payee/cop-tutorial](https://www.api-docs.form3.tech/api/tutorials/confirmation-of-payee/cop-tutorial)
- **Base URL:** `https://api.form3.tech/v1`
- [OpenAPI](openapi/form3-payments.yml)

### Form3 Files API

Submit and receive bulk payment instructions and scheme messages as files (Transaction File / Scheme File).

- **Human URL:** [https://www.api-docs.form3.tech/api/tutorials/bacs/send-transactions-in-a-file](https://www.api-docs.form3.tech/api/tutorials/bacs/send-transactions-in-a-file)
- **Base URL:** `https://api.form3.tech/v1`
- [OpenAPI](openapi/form3-payments.yml)

### Form3 Event Notifications API

Subscribe to and receive signed event notifications (webhooks) for payment and platform lifecycle events, and verify them.

- **Human URL:** [https://www.api-docs.form3.tech/api/tutorials/event-notifications/subscriptions-for-event-notifications](https://www.api-docs.form3.tech/api/tutorials/event-notifications/subscriptions-for-event-notifications)
- **Base URL:** `https://api.form3.tech/v1`
- [OpenAPI](openapi/form3-payments.yml)

### Form3 Security & Access API

Manage users, roles, access-control entries and public keys under a flexible security and approval model, and read audit trails and platform metrics.

- **Human URL:** [https://www.api-docs.form3.tech/api/tutorials/security/create-a-read-only-user](https://www.api-docs.form3.tech/api/tutorials/security/create-a-read-only-user)
- **Base URL:** `https://api.form3.tech/v1`
- [OpenAPI](openapi/form3-payments.yml)

## Common Properties

- [Website](https://www.form3.tech/)
- [Developer Portal](https://www.api-docs.form3.tech/)
- [API Reference](https://api-docs.form3.tech/api.html)
- [Getting Started](https://www.api-docs.form3.tech/api/tutorials/getting-started/introduction)
- [GitHub Organization](https://github.com/form3tech-oss)
- [Postman](https://documenter.getpostman.com/view/5561717/TWDTNzaD)
- [Status Page](https://status.form3.tech/)
- [Blog](https://www.form3.tech/news)
- [LinkedIn](https://www.linkedin.com/company/form3)
- [Terms of Service](https://www.form3.tech/legal/terms-and-conditions)
- [Privacy Policy](https://www.form3.tech/legal/data-privacy-statement)

## Maintainers

**FN:** Kin Lane
**Email:** kin@apievangelist.com
