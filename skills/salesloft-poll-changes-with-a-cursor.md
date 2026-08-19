---
name: Poll Salesloft for changes without burning the rate limit
description: Keep an external system in sync by polling on updated_at instead of paging deeper, and by reading the cost headers Salesloft returns on every response.
api: openapi/salesloft-people-api-openapi.yml
operations:
  - GET /people
  - GET /accounts
  - GET /activities
  - GET /activity_histories
generated: '2026-08-13'
method: generated
source: https://developers.salesloft.com/docs/platform/guides/building-an-efficient-cursor-poller/
---

# Poll Salesloft for changes without burning the rate limit

Salesloft prices requests instead of counting them. Your **team** — not your integration — has **600 cost per minute**. Other integrations on the same team draw from the same budget.

## The cost model

- Every endpoint costs **1** by default. Salesloft may change an endpoint's cost at any time and does not treat that as a deprecation.
- Deep paging is surcharged: pages **101-150 cost 3**, **151-250 cost 8**, **251-500 cost 10**, **501+ cost 30**.
- Two headers come back on every response:
  - `x-ratelimit-endpoint-cost` — what the request you just made cost.
  - `x-ratelimit-remaining-minute` — what is left this minute.

## The pattern

1. Sort ascending by `updated_at` and hold a high-water mark:
   `GET /people?sort_by=updated_at&sort_direction=ASC&per_page=100`
2. Read `data`, take the highest `updated_at` you saw, persist it.
3. On the next poll, filter to records updated after that mark rather than incrementing `page`. **Never let `page` climb past ~100.**
4. Before each burst, read `x-ratelimit-remaining-minute` from the previous response. If it is low, sleep to the top of the next minute.
5. On `429`, back off exponentially with jitter. **No `Retry-After` header is documented** — do not wait for one.

## Sorting caveat

ASC sorts nulls **first** and DESC sorts nulls **last**, so a record with a null `updated_at` will lead your ascending page. Guard the high-water mark against nulls.

## If you genuinely need more headroom

Email `integrations@salesloft.com`. The limit is adjustable customer-wide or per team.
