---
name: Log a call and attach a note
description: Record a completed call activity against a person and attach a note, the standard write-back path for a dialer or CRM integration.
api: openapi/salesloft-calls-api-openapi.yml
operations:
  - POST /activities/calls
  - GET /activities/calls
  - GET /activities/calls/{id}
  - GET /call_dispositions
  - GET /call_sentiments
  - POST /notes
  - GET /notes
generated: '2026-08-13'
method: generated
source: https://developers.salesloft.com/docs/platform/api-basics/third-party-dialers/
---

# Log a call and attach a note

## Steps

1. **Read the team's vocabulary first.** `GET /call_dispositions` and `GET /call_sentiments` return the values this team accepts. They are team-configurable — never hardcode a disposition string.
2. **Check whether they are mandatory.** `GET /team` exposes `dispositions_required` and `sentiments_required`. If either is true, a call logged without it is incomplete for that team's reporting.
3. **Log the call.** `POST /activities/calls` with the person id, the disposition, the sentiment, and the duration.
4. **Attach a note.** `POST /notes` associated to the person (or to the call).
5. **Verify.** `GET /activities/calls/{id}`.

## Rules

- No idempotency key. A retried `POST /activities/calls` logs a second call. Record the returned id before retrying anything.
- Recording is governed at team level: `GET /team` exposes `call_recording_disabled` and `record_by_default`. Respect them.
- Times are ISO 8601; see the timezone guidance in the API Basics docs.

## Scopes

`calls:read`, `calls:write`, `activities:read`, `activities:write`, `notes:write`, `team:read`.
