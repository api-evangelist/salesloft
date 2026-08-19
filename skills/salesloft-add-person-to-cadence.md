---
name: Add a person to a cadence
description: Create or resolve a person, choose a cadence, and enroll them by creating a cadence membership - the core Salesloft engagement flow.
api: openapi/salesloft-cadence-memberships-api-openapi.yml
operations:
  - GET /people
  - POST /people
  - GET /cadences
  - GET /cadences/{id}
  - POST /cadence_memberships
  - GET /cadence_memberships
  - DELETE /cadence_memberships/{id}
generated: '2026-08-13'
method: generated
source: https://developers.salesloft.com/docs/api/
---

# Add a person to a cadence

## Steps

1. **Resolve the person.** `GET /people` filtered by email address. If there is no match, `POST /people` with at least `email_address`, `first_name`, `last_name`, and ideally `account_id`.
2. **Pick the cadence.** `GET /cadences` to list, `GET /cadences/{id}` to confirm the one you want. Cadence steps are separate: `GET /steps`.
3. **Enroll.** `POST /cadence_memberships` with the person id, the cadence id, and the user id the membership belongs to.
4. **Confirm.** `GET /cadence_memberships` filtered to that person, or `GET /cadence_memberships/{id}`.
5. **Remove** when needed: `DELETE /cadence_memberships/{id}`.

## Rules that will bite you

- **There is no idempotency key on any of these writes.** Only `POST /v2/signals` accepts an `idempotency_key`. If a `POST /people` times out, do **not** blind-retry — re-run the `GET /people` lookup first, or you will create a duplicate person.
- Check `do_not_contact`, `bouncing` and `contact_restrictions` on the person before enrolling. `eu_resident` is published on the person record and is there for a reason.
- `422` returns an `errors` object of `field -> [messages]`, e.g. `{"errors":{"email_address":["is already taken"]}}` — that specific message means the person exists; go back to step 1.

## Scopes

`people:read`, `people:write`, `cadences:read`, `cadences:write`.
