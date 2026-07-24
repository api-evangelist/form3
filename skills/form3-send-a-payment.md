---
name: Send a payment with Form3
description: Create and submit an account-to-account payment (Faster Payments, Bacs, CHAPS, SEPA) and track it to completion using the Form3 Public API.
api: openapi/form3-payments.yml
operations:
- CreatePayment
- CreatePaymentSubmission
- GetPaymentSubmission
- GetPayment
---

# Send a payment with Form3

Use this flow to originate an outbound account-to-account payment and follow it through the scheme.

## Preconditions
- OAuth2 client-credentials token from `https://api.form3.tech/v1/oauth2/token`.
- Every request is signed with HTTP Message Signatures (see `authentication/form3-authentication.yml`); some environments also require mutual TLS.
- Media type `application/vnd.api+json`; resources are wrapped in a json:api `{ "data": { ... } }` envelope.

## Steps
1. **Generate a client id.** Create a UUID for the payment `id`. This is your idempotency key: re-sending the same create returns HTTP 409 with the already-stored resource, so retries never double-book.
2. **Create the payment** — `CreatePayment` (`POST /transaction/payments`). Supply `data.type: "payments"`, your `id`, `organisation_id`, and `attributes` (amount, currency, payment_scheme, beneficiary/debtor parties, processing_date).
3. **Submit it to the scheme** — `CreatePaymentSubmission` (`POST /transaction/payments/{id}/submissions`).
4. **Poll the submission** — `GetPaymentSubmission` (`GET /transaction/payments/{id}/submissions/{submissionId}`) until status is terminal (e.g. submitted/accepted/released).
5. **Read final state** — `GetPayment` (`GET /transaction/payments/{id}`) for the current version and status.
6. **Subscribe instead of polling (recommended).** Register an event-notification subscription so the platform pushes status transitions to you — see `skills/form3-event-notifications.md`.

## Error & retry rules
- 400 = validation error (`{ error_code, error_message }`); fix and resubmit.
- 401 = token expired or bad signature; re-authenticate / re-sign.
- 403 = the user/role lacks the ACE permission.
- 409 on create = duplicate id; treat as success and read `actual_resource`.
- 500/502 = transient; retry the SAME id (idempotent).
