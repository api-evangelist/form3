# Form3 (form3)

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
