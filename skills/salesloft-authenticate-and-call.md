---
name: Authenticate against the Salesloft Platform API
description: Obtain a Salesloft access token (OAuth authorization code, OAuth client credentials, or an API key) and make a first verified call, then keep the token alive.
api: openapi/salesloft-me-api-openapi.yml
operations:
  - GET /me
  - GET /team
  - POST /oauth/token
generated: '2026-08-13'
method: generated
source: https://developers.salesloft.com/docs/platform/api-basics/
---

# Authenticate against the Salesloft Platform API

Base URL: `https://api.salesloft.com/v2`. Auth host: `https://accounts.salesloft.com`.

## 1. Pick the right credential

| Situation | Credential | Why |
|---|---|---|
| Partner / public app, end user authorizes | OAuth **authorization_code** | Required. Partner apps submitted with API keys are rejected. |
| Private, server-to-server, no end user | OAuth **client_credentials** | Admin-enabled, assumes that admin's permissions, cannot be allowlisted. |
| A customer automating their own account | **API key** (`ak` + 64 hex) | Acts on behalf of the issuing user. |

Every credential is sent the same way: `Authorization: Bearer <token>`.

## 2. Get a token

Authorization code:

```
POST https://accounts.salesloft.com/oauth/token
Content-Type: application/json
{"client_id":"...","client_secret":"...","code":"...","grant_type":"authorization_code","redirect_uri":"..."}
```

Client credentials (scopes are **space**-delimited):

```
POST https://accounts.salesloft.com/oauth/token
Content-Type: application/json
{"client_id":"...","client_secret":"...","grant_type":"client_credentials","scope":"accounts:read people:read"}
```

Both return `expires_in: 7200`. Authorization code additionally returns a `refresh_token`.

## 3. Verify with the cheapest call in the API

- `GET /me` — the authenticated user (id, guid, name, email).
- `GET /team` — the team, including `plan` (`group` | `professional` | `enterprise`) and `plan_features`.

Both cost 1 rate-limit point.

## 4. Keep it alive

- Access tokens expire after **7200 seconds**.
- Authorization code: `POST /oauth/token` with `grant_type=refresh_token`. **Refresh tokens rotate** — the response contains a new `refresh_token` and all previous ones are revoked. Store the new one before you use the access token, or you will lock yourself out.
- Client credentials: there is no refresh token. Just request a new token.

## Failure modes

- `401 {"error":"No Bearer Token attached to request, please see documentation at developers.salesloft.com"}` — missing/expired token, or you sent the refresh token instead of the access token.
- `invalid_grant` — parameters were sent as headers instead of body, `Content-Type` was not `application/json`, or the code was already used.
- `403` — the token is valid but lacks the scope the endpoint requires. Check `scopes/salesloft-scopes.yml`.

## Rules

- Never put an API key in client-side code; it is equivalent to a login.
- Request the minimum scope set. Privileged scopes (`email_contents:read`, `data_control:*`, `crm_id_*:write`, `external_emails:write`) are reviewed and should be requested only when required.
