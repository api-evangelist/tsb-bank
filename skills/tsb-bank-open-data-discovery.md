---
name: Discover TSB Open Data
description: Query TSB's public, unauthenticated OBIE Open Data API for branch, ATM, and product reference data.
api: openapi/obie-open-data-openapi.json
operations:
  - GET /branches
  - GET /atms
  - GET /personal-current-accounts
  - GET /business-current-accounts
  - GET /unsecured-sme-loans
  - GET /commercial-credit-cards
---

# Discover TSB Open Data

TSB's Open Data API is public and requires **no authentication** — it serves OBIE
Open Data reference data. Base host: `https://apis.tsb.co.uk`.

## Steps

1. **List physical locations.** `GET /branches` returns TSB branch locations and
   services; `GET /atms` returns ATM locations. Both are OBIE Open Data
   collections paged via the `Links`/`Meta` envelope.
2. **List products.** Call the product collections as needed:
   `GET /personal-current-accounts`, `GET /business-current-accounts`,
   `GET /unsecured-sme-loans`, `GET /commercial-credit-cards`.
3. **Handle throttling and errors.** All operations may return `400` (request not
   understood), `408` (timeout), `429` (too many requests — back off), `500`, or
   `503`. See `errors/tsb-bank-problem-types.yml`.

## Rules
- No credentials, tokens, or consent are needed for Open Data — do not attempt OAuth.
- Respect `429` by backing off; these are unauthenticated shared endpoints.
