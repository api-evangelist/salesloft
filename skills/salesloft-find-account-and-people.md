---
name: Find an account and the people on it
description: Resolve a company to a Salesloft account, then page through the people attached to it, using the documented filter, paging and sorting conventions.
api: openapi/salesloft-accounts-api-openapi.yml
operations:
  - GET /accounts
  - GET /accounts/{id}
  - GET /people
  - GET /people/{id}
generated: '2026-08-13'
method: generated
source: https://developers.salesloft.com/docs/platform/api-basics/filtering-paging-sorting/
---

# Find an account and the people on it

## Steps

1. **Search accounts** — `GET /accounts` with a filter. Filters are per-endpoint; common ones are `crm_id`, `owner_crm_id`, `account_tier_id`, `tag_id`, `locales`.
   Prefix matching, where the endpoint documents "Supports partial matching", uses an object param and needs **at least 3 leading characters**:
   `GET /accounts?industry[_starts_with]=Health`
2. **Read the envelope.** Results are under `data`; `metadata` echoes the filter, paging and sorting values **as actually applied**. Always trust `metadata`, not your request — an out-of-range `per_page` is silently corrected, and an unrecognised filter *name* is silently ignored.
3. **Fetch the account** — `GET /accounts/{id}` for the full 42-field record.
4. **List its people** — `GET /people` filtered to the account. Each person embeds `account: {_href, id}`; follow `_href` to hydrate, there is no `expand[]` parameter.
5. **Fetch a person** — `GET /people/{id}`.

## Paging

```
GET /accounts?per_page=100&page=1
```

`per_page` defaults to 25, max 100. Response `metadata` carries `current_page`, `next_page`, `prev_page`, `total_pages`, `total_count`.

**Do not deep-page.** Page 101-150 costs 3 points, 151-250 costs 8, 251-500 costs 10, and 501+ costs **30** — against a 600-point-per-minute team budget. Past a few pages, switch to the `updated_at` cursor pattern (see `salesloft-poll-changes-with-a-cursor.md`).

## Sorting

`sort_by` + `sort_direction` (`ASC` | `DESC`). ASC puts nulls first, DESC puts nulls last. An invalid sort returns `422`.

## Failure modes

- `422` with an `errors` object — invalid sort, or an invalid filter *value*.
- `404` with a singular `error` — not found, or outside your visibility under the team's group privacy setting.
- `403` — missing `accounts:read` / `people:read` scope.
