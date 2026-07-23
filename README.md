# TSB Bank (tsb-bank)

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
