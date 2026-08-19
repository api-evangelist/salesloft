---
name: Subscribe to Salesloft webhooks and verify the signature
description: Register a webhook subscription through the API, then validate every delivery using the x-salesloft-signature HMAC before trusting it.
api: openapi/salesloft-webhook-subscriptions-api-openapi.yml
operations:
  - POST /webhook_subscriptions
  - GET /webhook_subscriptions
  - GET /webhook_subscriptions/{id}
  - PUT /webhook_subscriptions/{id}
  - DELETE /webhook_subscriptions/{id}
generated: '2026-08-13'
method: generated
source: https://developers.salesloft.com/docs/platform/webhooks/
---

# Subscribe to Salesloft webhooks and verify the signature

The event catalogue is described in `asyncapi.yml` in this repo and spans accounts, cadences, cadence memberships, calls, call data records, conversations, emails, meetings, notes, people, steps, tasks, users, successes and bulk jobs.

## Steps

1. **Stand up an HTTPS endpoint** that responds fast and does its work asynchronously.
2. **Create the subscription.** `POST /webhook_subscriptions` with the callback URL, the callback token, and the event type you want.
3. **List / confirm.** `GET /webhook_subscriptions`, `GET /webhook_subscriptions/{id}`.
4. **Verify every delivery before acting on it:**
   - `x-salesloft-event` names the event type.
   - `x-salesloft-signature` is the **HMAC-SHA1 hex digest of the raw response body**, keyed with that subscription's **callback token**.
   - Compute the digest over the raw bytes, compare in constant time, and reject on mismatch. Never parse the body first.
5. **Rotate or disable** with `PUT /webhook_subscriptions/{id}`, remove with `DELETE /webhook_subscriptions/{id}`.

## Rules

- HMAC-**SHA1** is what Salesloft signs with. It is weaker than you would choose today; treat the callback token as a secret and keep the endpoint URL unguessable.
- Deliveries are per subscription, so one token compromise is scoped to one subscription — use a distinct token per subscription.
- Webhooks are the correct alternative to polling for most event-driven work; see `salesloft-poll-changes-with-a-cursor.md` only when you need reconciliation.

## Scopes

Whatever scope the underlying resource requires, plus the ability to manage subscriptions on the app.
