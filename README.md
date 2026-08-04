# TSB Bank (tsb-bank)

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
> **On a security or compliance team?** Email
> [info@apievangelist.com](mailto:info@apievangelist.com) with *security* in the subject line and
> you will get a person, not a form. We will tell you exactly which public URLs this profile was
> built from so your team can see the same surface we did, and we will take the listing down on
> request while you work through it.
>
> Full detail: **[Where this data comes from](https://apievangelist.com/about/where-our-data-comes-from)**
<!-- API-EVANGELIST-PROVENANCE:END -->

TSB Bank plc is a British retail and commercial bank headquartered in Edinburgh, offering current accounts, savings, mortgages, personal loans, credit cards, and insurance to personal and business customers across the United Kingdom. Spun out of Lloyds Banking Group in 2013, TSB is a wholly owned subsidiary of the Spanish banking group Banco Sabadell. As an FCA-authorised account servicing payment service provider (ASPSP) under PSD2, TSB participates in UK Open Banking and publishes OBIE-conformant APIs through a public developer portal at apis.developer.tsb.co.uk. TSB is not one of the CMA9 banks but implements the same OBIE Open Data and Read/Write API family.

**APIs.json:** [https://raw.githubusercontent.com/api-evangelist/tsb-bank/refs/heads/main/apis.yml](https://raw.githubusercontent.com/api-evangelist/tsb-bank/refs/heads/main/apis.yml)

## Tags

- Financial Services
- Banking
- Open Banking
- PSD2
- OBIE
- United Kingdom
- Payments
- Account Information
- FAPI
- Fintech

## Timestamps

- **Created:** 2026-07-23
- **Modified:** 2026-07-23

## APIs

### TSB Open Data API

TSB's public, unauthenticated Open Data API conformant to the OBIE Open Data API Standard, exposing reference data for ATMs, branches, personal current accounts, business current accounts, unsecured SME loans, and commercial credit cards. No live TSB Open Data endpoint was confirmed at review time; the harvested OpenAPI is the shared OBIE Open Data standard, not a TSB proprietary contract.

- **Human URL:** [https://www.tsb.co.uk/help-and-support/open-banking/](https://www.tsb.co.uk/help-and-support/open-banking/)
- **Base URL:** `https://apis.tsb.co.uk`

#### Tags

- Open Data
- ATMs
- Branches
- Reference Data

#### Properties

- [OpenAPI](openapi/obie-open-data-openapi.json) — shared OBIE Open Data standard (Swagger 2.0, v1.3)
- [Documentation](https://www.tsb.co.uk/help-and-support/open-banking/)
- [API Reference](https://openbankinguk.github.io/opendata-api-docs-pub/v2.4.0/)

### TSB Account and Transaction Information API (AIS)

TSB's OBIE Read/Write Account and Transaction Information (AIS) API, providing authorised third-party providers read access to account, balance, transaction, beneficiary, standing order, direct debit, and statement data. FAPI-secured with OAuth2/OIDC, mutual-TLS, and PSD2 strong customer authentication; access requires developer-portal onboarding with OBIE/eIDAS certificates.

- **Human URL:** [https://apis.developer.tsb.co.uk/](https://apis.developer.tsb.co.uk/)
- **Base URL:** `https://apis.tsb.co.uk`

#### Tags

- Account Information
- AIS
- Open Banking

#### Properties

- [Documentation](https://apis.developer.tsb.co.uk/)
- [API Reference](https://github.com/OpenBankingUK/read-write-api-specs)

### TSB Payment Initiation API (PIS)

TSB's OBIE Read/Write Payment Initiation (PIS) API, enabling authorised third-party providers to initiate domestic and scheduled payments and standing orders on behalf of consenting customers. FAPI-secured with OAuth2/OIDC, mutual-TLS, and PSD2 strong customer authentication; access requires developer-portal onboarding with OBIE/eIDAS certificates.

- **Human URL:** [https://apis.developer.tsb.co.uk/](https://apis.developer.tsb.co.uk/)
- **Base URL:** `https://apis.tsb.co.uk`

#### Tags

- Payment Initiation
- PIS
- Payments

#### Properties

- [Documentation](https://apis.developer.tsb.co.uk/)
- [API Reference](https://github.com/OpenBankingUK/read-write-api-specs)

### TSB Confirmation of Funds API (CBPII)

TSB's OBIE Read/Write Confirmation of Funds (CBPII) API, allowing authorised card-based payment instrument issuers to confirm whether funds are available on a customer account. FAPI-secured with OAuth2/OIDC, mutual-TLS, and PSD2 strong customer authentication; access requires developer-portal onboarding with OBIE/eIDAS certificates.

- **Human URL:** [https://apis.developer.tsb.co.uk/](https://apis.developer.tsb.co.uk/)
- **Base URL:** `https://apis.tsb.co.uk`

#### Tags

- Confirmation of Funds
- CBPII
- Open Banking

#### Properties

- [Documentation](https://apis.developer.tsb.co.uk/)
- [API Reference](https://github.com/OpenBankingUK/read-write-api-specs)

## Common Properties

- [Website](https://www.tsb.co.uk/)
- [Developer Portal](https://apis.developer.tsb.co.uk/)
- [Documentation](https://www.tsb.co.uk/help-and-support/open-banking/)
- [LinkedIn](https://www.linkedin.com/company/tsb-bank)
- [Terms of Service](https://www.tsb.co.uk/legal/)
- [Privacy Policy](https://www.tsb.co.uk/privacy/)
- [Support](https://www.tsb.co.uk/help-and-support/)

## Maintainers

**FN:** Kin Lane
**Email:** kin@apievangelist.com
