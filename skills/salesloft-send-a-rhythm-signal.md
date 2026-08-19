---
name: Send a Rhythm signal (the one idempotent write in the API)
description: Push an external buying signal into Salesloft Rhythm with the required urgency, occurred_at and idempotency_key, so a retry cannot double-fire a play.
api: openapi/salesloft-signals-api-openapi.yml
operations:
  - POST /signals
  - GET /signal_registrations
  - DELETE /signal_registrations/{id}
  - POST /play_registrations
generated: '2026-08-13'
method: generated
source: https://developers.salesloft.com/docs/platform/rhythm-resources/sending-signals/
---

# Send a Rhythm signal

`POST https://api.salesloft.com/v2/signals` is the **only** Salesloft write that accepts an idempotency key. Use it.

## Required fields

| Field | Required | Notes |
|---|---|---|
| `name` | yes | Front-end version of the signal type. |
| `type` | yes | Signal type. |
| `data` | yes | Context metadata shown to the end user; must follow the registered structure. |
| `urgency` | yes | |
| `occurred_at` | yes | When the real-world event happened, not when you posted it. |
| `idempotency_key` | yes | **UUID4.** |
| `attribution` | | e.g. `["person"]` |
| `integration_id` | | your integration |
| `broadcast_notification` | | |

## Steps

1. **Register the signal type first** — `GET /signal_registrations` to see what exists; register the type and its `data` schema before sending instances.
2. **Generate a UUID4 idempotency key that is derived from the source event**, not from the attempt. If your upstream event has a stable id, hash it into the UUID. A per-retry random key defeats the whole mechanism.
3. **POST the signal.**
4. **Retry safely.** Because the key is stable per event, a network-timeout retry with the same body cannot create a second signal — the only place in this API where that is true.
5. **Plays**: `POST /play_registrations` to register the play a signal should drive.

## Rules

- `occurred_at` drives Rhythm prioritisation. Sending "now" for a three-day-old event mis-ranks the rep's day.
- Do **not** carry this pattern to other endpoints. `POST /people`, `POST /accounts`, `POST /notes`, `POST /tasks` and `POST /activities/calls` have **no** idempotency contract; a retry there duplicates.

## Scopes

`signals:write`, `signal_registrations:read`, `signal_registrations:delete`, `workflow:*` for play registration.
