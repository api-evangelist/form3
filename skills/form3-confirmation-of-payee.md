---
name: Run a Confirmation of Payee check with Form3
description: Perform a UK Confirmation of Payee / Verification of Payee name check against a beneficiary before paying, using the Form3 Public API.
api: openapi/form3-payments.yml
operations:
- CreateNameVerification
- GetNameVerification
- GetNameVerificationAdmission
---

# Confirmation of Payee (CoP) with Form3

Verify that a beneficiary's name matches the account before sending a payment.

## Preconditions
- OAuth2 client-credentials token + HTTP Message Signatures signing.
- json:api envelope, media type `application/vnd.api+json`.

## Steps
1. **Create the name verification** — `CreateNameVerification` (`POST /organisation/nameverifications`). Supply a client-generated UUID `id` and `attributes` for the account to check (sort code / account number, account name, account type).
2. **Track processing** — `GetNameVerificationAdmission` (`GET /organisation/nameverifications/{name_verification_id}/admissions/{id}`) to follow the scheme admission.
3. **Read the result** — `GetNameVerification` (`GET /organisation/nameverifications/{id}`). The response carries the match result (match / close match with the actual name / no match) and reason.
4. **Decide.** Use the match outcome to allow, warn, or block the downstream payment (`skills/form3-send-a-payment.md`).

## Notes
- Client-supplied `id` makes the check idempotent; a duplicate returns 409 with the stored result.
- A "close match" returns the name held at the beneficiary bank so the payer can confirm intent.
