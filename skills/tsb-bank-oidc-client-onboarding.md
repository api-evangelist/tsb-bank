---
name: Inspect TSB identity and register an OIDC client
description: Read TSB's OpenID Provider metadata and JWKS, and dynamically register an OIDC client against the OAuth Toolkit server.
api: openapi/tsb-bank-oauth-server-openapi.json
operations:
  - Get_OpenIDDiscovery
  - Get_jwk_set_
  - Post_oidc_register
  - Get_oidc_register_config
  - Create_request_token
---

# Inspect TSB identity and register an OIDC client

TSB runs a Curity OAuth Toolkit OpenID Provider at `https://apis.tsb.co.uk`.
This skill covers anonymous identity discovery plus dynamic client registration.
The FAPI-secured OBIE Read/Write services (AIS/PIS/CBPII) additionally require
mutual-TLS with OBIE/eIDAS certificates and developer-portal onboarding — see
`authentication/tsb-bank-authentication.yml`.

## Steps

1. **Read provider metadata.** `Get_OpenIDDiscovery`
   (`GET /.well-known/openid-configuration`) returns issuer
   `https://apis.tsb.co.uk:8443`, the authorize/token/userinfo/registration
   endpoints, supported scopes (`openid`, `email`, `profile`,
   `openid_client_registration`), and `token_endpoint_auth_methods` including
   `private_key_jwt`.
2. **Fetch signing keys.** `Get_jwk_set_` (`GET /openid/connect/jwks.json`)
   returns the JWKS used to verify id_tokens (RS256/HS256).
3. **Register a client.** `Post_oidc_register`
   (`POST /openid/connect/register`) performs OIDC dynamic client registration;
   it requires the `openid_client_registration` scope. Retrieve the resulting
   configuration with `Get_oidc_register_config`
   (`GET /openid/connect/register/{client_id}`).
4. **Obtain a token.** `Create_request_token` (`POST /auth/oauth/v2/token`)
   with an authorization_code, using `private_key_jwt` client authentication for
   FAPI compliance.

## Rules
- Use `authorization_code` + PKCE and `private_key_jwt`; the `implicit` flow is
  legacy and unsuitable for confidential Open Banking clients.
- OBIE Read/Write scopes (`accounts`, `payments`, `fundsconfirmations`) and
  mutual-TLS are required for account/payment APIs — see `scopes/` and
  `authentication/`.
