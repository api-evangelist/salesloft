---
name: Read Salesloft revenue data through the official MCP server
description: Connect an agent to Salesloft's first-party remote MCP server, understand the fifteen read-only tools it exposes, and know when to fall back to REST.
api: mcp/salesloft-mcp.yml
operations:
  - current_user
  - current_team
  - search_accounts
  - account_by_id
  - search_people
  - person_by_id
  - search_users
  - user_by_id
  - search_opportunities
  - opportunity_by_id
  - search_conversations
  - conversation_by_id
  - conversation_recording_by_id
generated: '2026-08-13'
method: generated
source: https://mcp.salesloft.com/
---

# Read Salesloft revenue data through the official MCP server

Endpoint: `https://mcp.salesloft.com/mcp` (JSON-RPC over HTTP). Manifest: `GET https://mcp.salesloft.com/` returns the full tool list **anonymously**, with a JSON Schema `inputSchema` *and* `outputSchema` per tool.

## Connect

1. The endpoint is an OAuth 2.1 protected resource. An unauthenticated call returns `401` with
   `WWW-Authenticate: Bearer resource_metadata="https://mcp.salesloft.com/.well-known/oauth-protected-resource"`.
2. Discover the authorization server at `https://mcp.salesloft.com/.well-known/oauth-authorization-server`:
   authorize `https://accounts.salesloft.com/oauth/authorize`, token `https://accounts.salesloft.com/oauth/token`, **dynamic client registration** at `https://accounts.salesloft.com/oauth/client/register`, PKCE `S256`.
3. Scopes offered: `accounts:read`, `conversations:read`, `opportunities:read`, `people:read`, `team:read`.
4. A Salesloft Admin must have enabled **Settings > Artificial Intelligence > Salesloft MCP**, and the account must be on a Salesloft Agentic entitlement. Claude lists the connector natively; a ChatGPT custom connector shipped 2026-08-11.

## The surface, honestly

- **All fifteen tools are read-only** (`readOnlyHint: true`, `destructiveHint: false`). There is no write path.
- Thirteen tools map 1:1 onto a documented v2 REST operation — see `mcp/salesloft-tool-crosswalk.yml`.
- Two tools (`report_missing_functionality`, `submit_feedback`) are product telemetry, not data access. Do not call them proactively.
- **Raw transcripts are not available.** The transcript-retrieval tool was removed in the August 2026 release; use `conversation_by_id`, which returns the AI summary, extracted fields and key moments.

## When to fall back to REST

Anything you cannot do here: writing, cadences and steps, tasks, emails and templates, calls and dialer data, bulk jobs, imports, webhooks, redaction, and all taxonomy resources. That is 163 of the 176 REST operations. Use the Platform API with an OAuth token — see `salesloft-authenticate-and-call.md`.

## Rules

- Pull the manifest from `https://mcp.salesloft.com/` and use each tool's published `inputSchema`; do not guess parameters.
- The tools accept the same filters as the REST list endpoints, including the deep-paging cost model. Prefer a tight filter over a large `page` value.
