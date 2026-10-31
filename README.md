# Salesloft

<!-- API-EVANGELIST-PROVENANCE:BEGIN -->
> ### About this repository
>
> **This is not our API.** This repository is an independent, third-party profile of a company's
> **publicly available** API surface, maintained by [API Evangelist](https://apievangelist.com).
> API Evangelist does not operate, host, resell, or support this company's APIs, and is not
> affiliated with or endorsed by the company unless stated on the profile.
>
> **Where the information came from.** Everything here is assembled from material a member of the
> public can reach with a browser and no credentials — the company's own website, developer portal
> and documentation, the specifications it publishes for public use (OpenAPI, AsyncAPI, JSON Schema,
> `apis.json`, `llms.txt` and similar), its public repositories, and its public status, pricing and
> changelog pages. **Nothing here is obtained by breaching a system, defeating an access control, or
> using credentials of any kind.**
>
> **The rating is an independent assessment.** The Kin Score and Agent Readiness rating are
> independently calculated scores of a company's *public* API artifacts, produced by API Evangelist
> against a published rubric. They are not certifications, endorsements, security assessments, or
> audits, and they score published artifacts — not the quality, safety, or security of the software.
>
> **Corrections, re-scores, and removal are free.** No partnership, contract, or purchase is
> required, and you do not need to justify the request.
>
> - **Something wrong?** Open an issue on this repository, or email
>   [info@apievangelist.com](mailto:info@apievangelist.com).
> - **Published something new?** Ask for a re-score and we will re-run the rating.
> - **Want the listing taken down?** Say so and we will honor it. The profile is reduced to your
>   company name, a factual description, and a link to your own site, and the company is recorded as
>   **unrated** — never scored zero for having asked.
>
> **Response times.** Acknowledgement within **one business day**; removal or restriction within
> **two business days**; corrections and re-scores within **five business days**.
>
> **Not from the company, and here with a question?** You are welcome here — we would rather be the
> front line and point you the right way than have a good report go nowhere. What this repository
> can answer is narrow, though, so it is worth knowing who you are actually looking for:
>
> - **A question about how the API works, an account, billing, or a bug in the service** — that is
>   the company's own support, not us. We profile this API; we do not operate it and cannot see
>   your account.
> - **A bug in an open-source project we only catalog** — file it on that project's own repository.
>   This has happened with a real and correct bug report that reached us instead of the people who
>   could fix it, which helped nobody.
> - **Anything about this listing itself** — the description, the tags, the rating, a missing or
>   wrong artifact — is ours. Open an issue here.
> - **Not sure, or something general about API Evangelist or APIs.io** — open an issue on the
>   [APIs.io Inbox](https://github.com/api-search/inbox) and we will route it.
>
> **This repository contains no software, and we will never ask you to download anything.** There is
> no build, release, installer, or binary here — only text and machine-readable API descriptions, so
> there is nothing here that can be "corrupt" or need "repairing". Any issue, comment, or email
> claiming otherwise and offering a download link is not from us and is hostile. Do not follow the
> link; it is a lure. Report it to GitHub and, if you like, tell us at
> [info@apievangelist.com](mailto:info@apievangelist.com) so we can take it down.
>
> **On a security or compliance team?** Email
> [info@apievangelist.com](mailto:info@apievangelist.com) with *security* in the subject line and
> you will get a person, not a form. We will tell you exactly which public URLs this profile was
> built from so your team can see the same surface we did, and we will take the listing down on
> request while you work through it.
>
> Full detail: **[Where this data comes from](https://apievangelist.com/about/where-our-data-comes-from)**
<!-- API-EVANGELIST-PROVENANCE:END -->

Salesloft is a sales engagement and revenue orchestration platform, now combined with Clari, Drift and Groove, used by more than 4,000 sales teams to run cadences, dial and email prospects, capture and analyse conversations, and forecast pipeline. The Salesloft Platform API v2 at https://api.salesloft.com/v2 covers accounts, people, cadences, steps and actions, tasks, calls, emails, meetings, notes, opportunities, conversation intelligence, bulk jobs, imports, CRM mirroring, data-redaction governance and Rhythm signals, authenticated with OAuth 2.0 (authorization code and client credentials) or scoped API keys and priced against a 600-cost-per-minute per-team budget. Salesloft also publishes a documented webhook surface with HMAC-signed deliveries and a first-party remote MCP server at https://mcp.salesloft.com/mcp exposing fifteen read-only tools to AI agents.

**Areas:** Sales · Sales Engagement · Cadences · CRM · Email · Revenue Intelligence · Conversation Intelligence · Sales Automation · Webhook · MCP · Agents · Sales Dialer

## Salesloft on APIs.io

Everything profiled for Salesloft is published on APIs.io rather than in this repository. Start at the provider page — **[apis.io/providers/salesloft/](https://apis.io/providers/salesloft/)** — or go straight to one of the APIs or properties below.

### APIs (85)

- [Salesloft Platform API](https://apis.io/apis/salesloft/salesloft-platform-api/) — REST API for cadences, people, accounts, emails, calls, tasks, opportunities and analytics.
- [Salesloft MCP Server](https://apis.io/apis/salesloft/salesloft-mcp-server/) — First-party remote Model Context Protocol server exposing fifteen read-only tools over Salesloft accounts, people, users, opportunities, conversations and…
- [Salesloft Webhooks API](https://apis.io/apis/salesloft/salesloft-webhooks-api/) — Subscribe to platform events for real-time updates.
- [Salesloft Account and People Redaction API](https://apis.io/apis/salesloft/salesloft-account-and-people-redaction-api/) — [https://developer.salesloft.com/docs/api/account-and-people-redaction/](https://developer.salesloft.com/docs/api/account-and-people-redaction/)
- [Salesloft Account Redaction API](https://apis.io/apis/salesloft/salesloft-account-redaction-api/) — [https://developer.salesloft.com/docs/api/account-redaction/](https://developer.salesloft.com/docs/api/account-redaction/)
- [Salesloft Account Stages API](https://apis.io/apis/salesloft/salesloft-account-stages-api/) — [https://developer.salesloft.com/docs/api/account-stages/](https://developer.salesloft.com/docs/api/account-stages/)
- [Salesloft Account Team Member Roles API](https://apis.io/apis/salesloft/salesloft-account-team-member-roles-api/) — [https://developer.salesloft.com/docs/api/account-team-member-roles-index/](https://developer.salesloft.com/docs/api/account-team-member-roles-index/)
- [Salesloft Account Tiers API](https://apis.io/apis/salesloft/salesloft-account-tiers-api/) — [https://developer.salesloft.com/docs/api/account-tiers/](https://developer.salesloft.com/docs/api/account-tiers/)
- [Salesloft Account Upserts API](https://apis.io/apis/salesloft/salesloft-account-upserts-api/) — [https://developer.salesloft.com/docs/api/account-upserts/](https://developer.salesloft.com/docs/api/account-upserts/)
- [Salesloft Accounts API](https://apis.io/apis/salesloft/salesloft-accounts-api/) — [https://developer.salesloft.com/docs/api/accounts/](https://developer.salesloft.com/docs/api/accounts/)
- [Salesloft Actions API](https://apis.io/apis/salesloft/salesloft-actions-api/) — [https://developer.salesloft.com/docs/api/actions/](https://developer.salesloft.com/docs/api/actions/)
- [Salesloft Activities API](https://apis.io/apis/salesloft/salesloft-activities-api/) — [https://developer.salesloft.com/docs/api/activities/](https://developer.salesloft.com/docs/api/activities/)
- [Salesloft Activity Histories API](https://apis.io/apis/salesloft/salesloft-activity-histories-api/) — [https://developer.salesloft.com/docs/api/activity-histories/](https://developer.salesloft.com/docs/api/activity-histories/)
- [Salesloft Bulk Jobs API](https://apis.io/apis/salesloft/salesloft-bulk-jobs-api/) — [https://developer.salesloft.com/docs/api/bulk-jobs/](https://developer.salesloft.com/docs/api/bulk-jobs/)
- [Salesloft Bulk Jobs - Job Data API](https://apis.io/apis/salesloft/salesloft-bulk-jobs-job-data-api/) — [https://developer.salesloft.com/docs/api/bulk-jobs-job-data/](https://developer.salesloft.com/docs/api/bulk-jobs-job-data/)
- [Salesloft Bulk Jobs - Results API](https://apis.io/apis/salesloft/salesloft-bulk-jobs-results-api/) — [https://developer.salesloft.com/docs/api/bulk-jobs-results/](https://developer.salesloft.com/docs/api/bulk-jobs-results/)
- [Salesloft Bulk Reschedule Tasks API](https://apis.io/apis/salesloft/salesloft-bulk-reschedule-tasks-api/) — [https://developer.salesloft.com/docs/api/bulk-reschedule-tasks/](https://developer.salesloft.com/docs/api/bulk-reschedule-tasks/)
- [Salesloft Cadence Exports API](https://apis.io/apis/salesloft/salesloft-cadence-exports-api/) — [https://developer.salesloft.com/docs/api/cadence-exports/](https://developer.salesloft.com/docs/api/cadence-exports/)
- [Salesloft Cadence Imports API](https://apis.io/apis/salesloft/salesloft-cadence-imports-api/) — [https://developer.salesloft.com/docs/api/cadence-imports/](https://developer.salesloft.com/docs/api/cadence-imports/)
- [Salesloft Cadence Memberships API](https://apis.io/apis/salesloft/salesloft-cadence-memberships-api/) — [https://developer.salesloft.com/docs/api/cadence-memberships/](https://developer.salesloft.com/docs/api/cadence-memberships/)
- [Salesloft Cadence Stats API](https://apis.io/apis/salesloft/salesloft-cadence-stats-api/) — [https://developer.salesloft.com/docs/api/cadence-stats/](https://developer.salesloft.com/docs/api/cadence-stats/)
- [Salesloft Cadences API](https://apis.io/apis/salesloft/salesloft-cadences-api/) — [https://developer.salesloft.com/docs/api/cadences/](https://developer.salesloft.com/docs/api/cadences/)
- [Salesloft Calendar Events API](https://apis.io/apis/salesloft/salesloft-calendar-events-api/) — [https://developer.salesloft.com/docs/api/calendar-events/](https://developer.salesloft.com/docs/api/calendar-events/)
- [Salesloft Call Data Records API](https://apis.io/apis/salesloft/salesloft-call-data-records-api/) — [https://developer.salesloft.com/docs/api/call-data-records/](https://developer.salesloft.com/docs/api/call-data-records/)
- [Salesloft Call Dispositions API](https://apis.io/apis/salesloft/salesloft-call-dispositions-api/) — [https://developer.salesloft.com/docs/api/call-dispositions/](https://developer.salesloft.com/docs/api/call-dispositions/)
- [Salesloft Call Instructions API](https://apis.io/apis/salesloft/salesloft-call-instructions-api/) — [https://developer.salesloft.com/docs/api/call-instructions/](https://developer.salesloft.com/docs/api/call-instructions/)
- [Salesloft Call Sentiments API](https://apis.io/apis/salesloft/salesloft-call-sentiments-api/) — [https://developer.salesloft.com/docs/api/call-sentiments/](https://developer.salesloft.com/docs/api/call-sentiments/)
- [Salesloft Caller Ids API](https://apis.io/apis/salesloft/salesloft-caller-ids-api/) — [https://developer.salesloft.com/docs/api/caller-ids/](https://developer.salesloft.com/docs/api/caller-ids/)
- [Salesloft Calls API](https://apis.io/apis/salesloft/salesloft-calls-api/) — [https://developer.salesloft.com/docs/api/calls/](https://developer.salesloft.com/docs/api/calls/)
- [Salesloft Client Credentials Access Token API](https://apis.io/apis/salesloft/salesloft-client-credentials-access-token-api/) — OAuth 2.0 token endpoint for private Salesloft applications using the client credentials grant. POST /oauth/token on the Salesloft accounts host, not on the…
- [Salesloft Conversations API](https://apis.io/apis/salesloft/salesloft-conversations-api/) — [https://developer.salesloft.com/docs/api/conversations/](https://developer.salesloft.com/docs/api/conversations/)
- [Salesloft Conversations Calls API](https://apis.io/apis/salesloft/salesloft-conversations-calls-api/) — [https://developer.salesloft.com/docs/api/conversations-calls/](https://developer.salesloft.com/docs/api/conversations-calls/)
- [Salesloft Counts API](https://apis.io/apis/salesloft/salesloft-counts-api/) — [https://developer.salesloft.com/docs/api/counts/](https://developer.salesloft.com/docs/api/counts/)
- [Salesloft Crm Account Team Members API](https://apis.io/apis/salesloft/salesloft-crm-account-team-members-api/) — [https://developers.salesloft.com/docs/api/crm-account-team-members/](https://developers.salesloft.com/docs/api/crm-account-team-members/)
- [Salesloft Crm Activities API](https://apis.io/apis/salesloft/salesloft-crm-activities-api/) — [https://developer.salesloft.com/docs/api/crm-activities/](https://developer.salesloft.com/docs/api/crm-activities/)
- [Salesloft Crm Activity Fields API](https://apis.io/apis/salesloft/salesloft-crm-activity-fields-api/) — [https://developer.salesloft.com/docs/api/crm-activity-fields/](https://developer.salesloft.com/docs/api/crm-activity-fields/)
- [Salesloft Crm Users API](https://apis.io/apis/salesloft/salesloft-crm-users-api/) — [https://developer.salesloft.com/docs/api/crm-users/](https://developer.salesloft.com/docs/api/crm-users/)
- [Salesloft Custom Fields API](https://apis.io/apis/salesloft/salesloft-custom-fields-api/) — [https://developer.salesloft.com/docs/api/custom-fields/](https://developer.salesloft.com/docs/api/custom-fields/)
- [Salesloft Custom Roles API](https://apis.io/apis/salesloft/salesloft-custom-roles-api/) — [https://developer.salesloft.com/docs/api/custom-roles/](https://developer.salesloft.com/docs/api/custom-roles/)
- [Salesloft Email Missing Tags API](https://apis.io/apis/salesloft/salesloft-email-missing-tags-api/) — [https://developer.salesloft.com/docs/api/email-missing-tags/](https://developer.salesloft.com/docs/api/email-missing-tags/)
- [Salesloft Email Template Attachments API](https://apis.io/apis/salesloft/salesloft-email-template-attachments-api/) — [https://developer.salesloft.com/docs/api/email-template-attachments/](https://developer.salesloft.com/docs/api/email-template-attachments/)
- [Salesloft Email Templates API](https://apis.io/apis/salesloft/salesloft-email-templates-api/) — [https://developer.salesloft.com/docs/api/email-templates/](https://developer.salesloft.com/docs/api/email-templates/)
- [Salesloft Emails API](https://apis.io/apis/salesloft/salesloft-emails-api/) — [https://developer.salesloft.com/docs/api/emails/](https://developer.salesloft.com/docs/api/emails/)
- [Salesloft External Emails API](https://apis.io/apis/salesloft/salesloft-external-emails-api/) — [https://developer.salesloft.com/docs/api/external-emails/](https://developer.salesloft.com/docs/api/external-emails/)
- [Salesloft External Id Configuration API](https://apis.io/apis/salesloft/salesloft-external-id-configuration-api/) — [https://developer.salesloft.com/docs/api/external-id-configuration/](https://developer.salesloft.com/docs/api/external-id-configuration/)
- [Salesloft External Id Mapping API](https://apis.io/apis/salesloft/salesloft-external-id-mapping-api/) — [https://developer.salesloft.com/docs/api/external-id-mapping/](https://developer.salesloft.com/docs/api/external-id-mapping/)
- [Salesloft Groups API](https://apis.io/apis/salesloft/salesloft-groups-api/) — [https://developer.salesloft.com/docs/api/groups/](https://developer.salesloft.com/docs/api/groups/)
- [Salesloft Imports API](https://apis.io/apis/salesloft/salesloft-imports-api/) — [https://developer.salesloft.com/docs/api/imports/](https://developer.salesloft.com/docs/api/imports/)
- [Salesloft Live Feed Items API](https://apis.io/apis/salesloft/salesloft-live-feed-items-api/) — [https://developer.salesloft.com/docs/api/live-feed-items/](https://developer.salesloft.com/docs/api/live-feed-items/)
- [Salesloft Live Website Tracking Parameters API](https://apis.io/apis/salesloft/salesloft-live-website-tracking-parameters-api/) — [https://developer.salesloft.com/docs/api/live-website-tracking-parameters/](https://developer.salesloft.com/docs/api/live-website-tracking-parameters/)
- [Salesloft Me API](https://apis.io/apis/salesloft/salesloft-me-api/) — [https://developer.salesloft.com/docs/api/me/](https://developer.salesloft.com/docs/api/me/)
- [Salesloft Meetings API](https://apis.io/apis/salesloft/salesloft-meetings-api/) — [https://developer.salesloft.com/docs/api/meetings/](https://developer.salesloft.com/docs/api/meetings/)
- [Salesloft Mime Email Payloads API](https://apis.io/apis/salesloft/salesloft-mime-email-payloads-api/) — [https://developer.salesloft.com/docs/api/mime-email-payloads/](https://developer.salesloft.com/docs/api/mime-email-payloads/)
- [Salesloft Notes API](https://apis.io/apis/salesloft/salesloft-notes-api/) — [https://developer.salesloft.com/docs/api/notes/](https://developer.salesloft.com/docs/api/notes/)
- [Salesloft Ongoing Actions API](https://apis.io/apis/salesloft/salesloft-ongoing-actions-api/) — [https://developer.salesloft.com/docs/api/ongoing-actions/](https://developer.salesloft.com/docs/api/ongoing-actions/)
- [Salesloft Opportunities API](https://apis.io/apis/salesloft/salesloft-opportunities-api/) — [https://developers.salesloft.com/docs/api/opportunities/](https://developers.salesloft.com/docs/api/opportunities/)
- [Salesloft Opportunity People API](https://apis.io/apis/salesloft/salesloft-opportunity-people-api/) — [https://developers.salesloft.com/docs/api/opportunity-people/](https://developers.salesloft.com/docs/api/opportunity-people/)
- [Salesloft Opportunity Stages API](https://apis.io/apis/salesloft/salesloft-opportunity-stages-api/) — [https://developers.salesloft.com/docs/api/opportunity-stages/](https://developers.salesloft.com/docs/api/opportunity-stages/)
- [Salesloft Pending Emails API](https://apis.io/apis/salesloft/salesloft-pending-emails-api/) — [https://developer.salesloft.com/docs/api/pending-emails/](https://developer.salesloft.com/docs/api/pending-emails/)
- [Salesloft People API](https://apis.io/apis/salesloft/salesloft-people-api/) — [https://developer.salesloft.com/docs/api/people/](https://developer.salesloft.com/docs/api/people/)
- [Salesloft People Soft Deletion API](https://apis.io/apis/salesloft/salesloft-people-soft-deletion-api/) — [https://developer.salesloft.com/docs/api/people-soft-deletion/](https://developer.salesloft.com/docs/api/people-soft-deletion/)
- [Salesloft Person Stages API](https://apis.io/apis/salesloft/salesloft-person-stages-api/) — [https://developer.salesloft.com/docs/api/person-stages/](https://developer.salesloft.com/docs/api/person-stages/)
- [Salesloft Person Upserts API](https://apis.io/apis/salesloft/salesloft-person-upserts-api/) — [https://developer.salesloft.com/docs/api/person-upserts/](https://developer.salesloft.com/docs/api/person-upserts/)
- [Salesloft Phone Number Assignments API](https://apis.io/apis/salesloft/salesloft-phone-number-assignments-api/) — [https://developer.salesloft.com/docs/api/phone-number-assignments/](https://developer.salesloft.com/docs/api/phone-number-assignments/)
- [Salesloft Play Registrations API](https://apis.io/apis/salesloft/salesloft-play-registrations-api/) — [https://developer.salesloft.com/docs/api/play-registrations/](https://developer.salesloft.com/docs/api/play-registrations/)
- [Salesloft Profiles API](https://apis.io/apis/salesloft/salesloft-profiles-api/) — [https://developers.salesloft.com/docs/api/profiles/](https://developers.salesloft.com/docs/api/profiles/)
- [Salesloft Recording Settings API](https://apis.io/apis/salesloft/salesloft-recording-settings-api/) — [https://developer.salesloft.com/docs/api/recording-settings/](https://developer.salesloft.com/docs/api/recording-settings/)
- [Salesloft Requests API](https://apis.io/apis/salesloft/salesloft-requests-api/) — [https://developer.salesloft.com/docs/api/requests/](https://developer.salesloft.com/docs/api/requests/)
- [Salesloft Reschedule Links API](https://apis.io/apis/salesloft/salesloft-reschedule-links-api/) — [https://developer.salesloft.com/docs/api/reschedule-links/](https://developer.salesloft.com/docs/api/reschedule-links/)
- [Salesloft Right to Be Forgotten API](https://apis.io/apis/salesloft/salesloft-right-to-be-forgotten-api/) — [https://developer.salesloft.com/docs/api/right-to-be-forgotten/](https://developer.salesloft.com/docs/api/right-to-be-forgotten/)
- [Salesloft Saved List Views API](https://apis.io/apis/salesloft/salesloft-saved-list-views-api/) — [https://developer.salesloft.com/docs/api/saved-list-views/](https://developer.salesloft.com/docs/api/saved-list-views/)
- [Salesloft Searches API](https://apis.io/apis/salesloft/salesloft-searches-api/) — [https://developer.salesloft.com/docs/api/searches/](https://developer.salesloft.com/docs/api/searches/)
- [Salesloft Settings API](https://apis.io/apis/salesloft/salesloft-settings-api/) — [https://developer.salesloft.com/docs/api/settings/](https://developer.salesloft.com/docs/api/settings/)
- [Salesloft Signal Registrations API](https://apis.io/apis/salesloft/salesloft-signal-registrations-api/) — [https://developer.salesloft.com/docs/api/signal-registrations/](https://developer.salesloft.com/docs/api/signal-registrations/)
- [Salesloft Signals API](https://apis.io/apis/salesloft/salesloft-signals-api/) — [https://developer.salesloft.com/docs/api/signals/](https://developer.salesloft.com/docs/api/signals/)
- [Salesloft Steps API](https://apis.io/apis/salesloft/salesloft-steps-api/) — [https://developer.salesloft.com/docs/api/steps/](https://developer.salesloft.com/docs/api/steps/)
- [Salesloft Successes API](https://apis.io/apis/salesloft/salesloft-successes-api/) — [https://developer.salesloft.com/docs/api/successes/](https://developer.salesloft.com/docs/api/successes/)
- [Salesloft Tags API](https://apis.io/apis/salesloft/salesloft-tags-api/) — The Tags API from Salesloft — 1 operation(s) for tags.
- [Salesloft Tasks API](https://apis.io/apis/salesloft/salesloft-tasks-api/) — [https://developer.salesloft.com/docs/api/tasks/](https://developer.salesloft.com/docs/api/tasks/)
- [Salesloft Team API](https://apis.io/apis/salesloft/salesloft-team-api/) — [https://developer.salesloft.com/docs/api/team/](https://developer.salesloft.com/docs/api/team/)
- [Salesloft Team Template Attachments API](https://apis.io/apis/salesloft/salesloft-team-template-attachments-api/) — [https://developer.salesloft.com/docs/api/team-template-attachments/](https://developer.salesloft.com/docs/api/team-template-attachments/)
- [Salesloft Team Templates API](https://apis.io/apis/salesloft/salesloft-team-templates-api/) — [https://developer.salesloft.com/docs/api/team-templates/](https://developer.salesloft.com/docs/api/team-templates/)
- [Salesloft Transcriptions API](https://apis.io/apis/salesloft/salesloft-transcriptions-api/) — [https://developer.salesloft.com/docs/api/transcriptions/](https://developer.salesloft.com/docs/api/transcriptions/)
- [Salesloft Users API](https://apis.io/apis/salesloft/salesloft-users-api/) — [https://developer.salesloft.com/docs/api/users/](https://developer.salesloft.com/docs/api/users/)
- [Salesloft Webhook Subscriptions API](https://apis.io/apis/salesloft/salesloft-webhook-subscriptions-api/) — [https://developer.salesloft.com/docs/api/webhook-subscriptions/](https://developer.salesloft.com/docs/api/webhook-subscriptions/)

### Published properties

Each property below is a page on APIs.io carrying the machine-readable artifact and what it says.

#### MCP servers (1)

Model Context Protocol servers that expose the API to agents.

- [salesloft](https://apis.io/servers/salesloft/salesloft/)

#### Agentic access (1)

Which operations an agent can call, which act, and which need a human in the loop.

- [Salesloft Agentic Access](https://apis.io/agentic-access/salesloft/salesloft-agentic-access/)

#### JSON Schema (3)

The data models the API reads and writes.

- [Salesloft Account](https://apis.io/schemas/salesloft/salesloft-account/)
- [Salesloft Cadence](https://apis.io/schemas/salesloft/salesloft-cadence/)
- [Salesloft Person](https://apis.io/schemas/salesloft/salesloft-person/)

#### JSON Structure (2)

Data models expressed in JSON Structure.

- [Salesloft Account Structure](https://apis.io/json-structure/salesloft/salesloft-account-structure/)
- [Salesloft Person Structure](https://apis.io/json-structure/salesloft/salesloft-person-structure/)

#### JSON-LD (1)

Linked-data contexts for the provider's vocabulary.

- [Salesloft Context](https://apis.io/jsonld/salesloft/salesloft-context/)

#### Vocabulary (1)

The provider's domain terms, defined.

- [Salesloft API Vocabulary](https://apis.io/vocabularies/salesloft/salesloft-vocabulary/)

#### Examples (2)

Example requests and responses.

- [Salesloft Create Person Example](https://apis.io/examples/salesloft/salesloft-create-person-example/)
- [Salesloft List Accounts Example](https://apis.io/examples/salesloft/salesloft-list-accounts-example/)

#### Collections (83)

Postman and Open Collection request collections.

- [Salesloft](https://apis.io/collections/salesloft/open-salesloft/)
- [Salesloft Account and People Redaction API](https://apis.io/collections/salesloft/open-salesloft-account-and-people-redaction-api/)
- [Salesloft Account and People Redaction Account Redaction API](https://apis.io/collections/salesloft/open-salesloft-account-redaction-api/)
- [Salesloft Account and People Redaction Account Stages API](https://apis.io/collections/salesloft/open-salesloft-account-stages-api/)
- [Salesloft Account and People Redaction Account Team Member Roles API](https://apis.io/collections/salesloft/open-salesloft-account-team-member-roles-api/)
- [Salesloft Account and People Redaction Account Tiers API](https://apis.io/collections/salesloft/open-salesloft-account-tiers-api/)
- [Salesloft Account and People Redaction Account Upserts API](https://apis.io/collections/salesloft/open-salesloft-account-upserts-api/)
- [Salesloft Account and People Redaction Accounts API](https://apis.io/collections/salesloft/open-salesloft-accounts-api/)
- [Salesloft Account and People Redaction Actions API](https://apis.io/collections/salesloft/open-salesloft-actions-api/)
- [Salesloft Account and People Redaction Activities API](https://apis.io/collections/salesloft/open-salesloft-activities-api/)
- [Salesloft Account and People Redaction Activity Histories API](https://apis.io/collections/salesloft/open-salesloft-activity-histories-api/)
- [Salesloft Account and People Redaction Bulk Jobs API](https://apis.io/collections/salesloft/open-salesloft-bulk-jobs-api/)
- [Salesloft Account and People Redaction Bulk Jobs - Job Data API](https://apis.io/collections/salesloft/open-salesloft-bulk-jobs-job-data-api/)
- [Salesloft Account and People Redaction Bulk Jobs - Results API](https://apis.io/collections/salesloft/open-salesloft-bulk-jobs-results-api/)
- [Salesloft Account and People Redaction Bulk Reschedule Tasks API](https://apis.io/collections/salesloft/open-salesloft-bulk-reschedule-tasks-api/)
- [Salesloft Account and People Redaction Cadence Exports API](https://apis.io/collections/salesloft/open-salesloft-cadence-exports-api/)
- [Salesloft Account and People Redaction Cadence Imports API](https://apis.io/collections/salesloft/open-salesloft-cadence-imports-api/)
- [Salesloft Account and People Redaction Cadence Memberships API](https://apis.io/collections/salesloft/open-salesloft-cadence-memberships-api/)
- [Salesloft Account and People Redaction Cadence Stats API](https://apis.io/collections/salesloft/open-salesloft-cadence-stats-api/)
- [Salesloft Account and People Redaction Cadences API](https://apis.io/collections/salesloft/open-salesloft-cadences-api/)
- [Salesloft Account and People Redaction Calendar Events API](https://apis.io/collections/salesloft/open-salesloft-calendar-events-api/)
- [Salesloft Account and People Redaction Call Data Records API](https://apis.io/collections/salesloft/open-salesloft-call-data-records-api/)
- [Salesloft Account and People Redaction Call Dispositions API](https://apis.io/collections/salesloft/open-salesloft-call-dispositions-api/)
- [Salesloft Account and People Redaction Call Instructions API](https://apis.io/collections/salesloft/open-salesloft-call-instructions-api/)
- [Salesloft Account and People Redaction Call Sentiments API](https://apis.io/collections/salesloft/open-salesloft-call-sentiments-api/)
- …and 58 more published on APIs.io

#### Overlays (82)

OpenAPI overlays, including conversational phrasing for each operation.

- [Salesloft Account And People Redaction Api Overlay](https://apis.io/overlays/salesloft/salesloft-account-and-people-redaction-api-overlay/)
- [Salesloft Account Redaction Api Overlay](https://apis.io/overlays/salesloft/salesloft-account-redaction-api-overlay/)
- [Salesloft Account Stages Api Overlay](https://apis.io/overlays/salesloft/salesloft-account-stages-api-overlay/)
- [Salesloft Account Team Member Roles Api Overlay](https://apis.io/overlays/salesloft/salesloft-account-team-member-roles-api-overlay/)
- [Salesloft Account Tiers Api Overlay](https://apis.io/overlays/salesloft/salesloft-account-tiers-api-overlay/)
- [Salesloft Account Upserts Api Overlay](https://apis.io/overlays/salesloft/salesloft-account-upserts-api-overlay/)
- [Salesloft Accounts Api Overlay](https://apis.io/overlays/salesloft/salesloft-accounts-api-overlay/)
- [Salesloft Actions Api Overlay](https://apis.io/overlays/salesloft/salesloft-actions-api-overlay/)
- [Salesloft Activities Api Overlay](https://apis.io/overlays/salesloft/salesloft-activities-api-overlay/)
- [Salesloft Activity Histories Api Overlay](https://apis.io/overlays/salesloft/salesloft-activity-histories-api-overlay/)
- [Salesloft Bulk Jobs Api Overlay](https://apis.io/overlays/salesloft/salesloft-bulk-jobs-api-overlay/)
- [Salesloft Bulk Jobs Job Data Api Overlay](https://apis.io/overlays/salesloft/salesloft-bulk-jobs-job-data-api-overlay/)
- [Salesloft Bulk Jobs Results Api Overlay](https://apis.io/overlays/salesloft/salesloft-bulk-jobs-results-api-overlay/)
- [Salesloft Bulk Reschedule Tasks Api Overlay](https://apis.io/overlays/salesloft/salesloft-bulk-reschedule-tasks-api-overlay/)
- [Salesloft Cadence Exports Api Overlay](https://apis.io/overlays/salesloft/salesloft-cadence-exports-api-overlay/)
- [Salesloft Cadence Imports Api Overlay](https://apis.io/overlays/salesloft/salesloft-cadence-imports-api-overlay/)
- [Salesloft Cadence Memberships Api Overlay](https://apis.io/overlays/salesloft/salesloft-cadence-memberships-api-overlay/)
- [Salesloft Cadence Stats Api Overlay](https://apis.io/overlays/salesloft/salesloft-cadence-stats-api-overlay/)
- [Salesloft Cadences Api Overlay](https://apis.io/overlays/salesloft/salesloft-cadences-api-overlay/)
- [Salesloft Calendar Events Api Overlay](https://apis.io/overlays/salesloft/salesloft-calendar-events-api-overlay/)
- [Salesloft Call Data Records Api Overlay](https://apis.io/overlays/salesloft/salesloft-call-data-records-api-overlay/)
- [Salesloft Call Dispositions Api Overlay](https://apis.io/overlays/salesloft/salesloft-call-dispositions-api-overlay/)
- [Salesloft Call Instructions Api Overlay](https://apis.io/overlays/salesloft/salesloft-call-instructions-api-overlay/)
- [Salesloft Call Sentiments Api Overlay](https://apis.io/overlays/salesloft/salesloft-call-sentiments-api-overlay/)
- [Salesloft Caller Ids Api Overlay](https://apis.io/overlays/salesloft/salesloft-caller-ids-api-overlay/)
- …and 57 more published on APIs.io

#### Governance rules (2)

Spectral rulesets for the provider's contracts.

- [Salesloft — jsonschema rules](https://apis.io/rules/salesloft/salesloft-jsonschema-spectral-rules/)
- [Salesloft API Rules](https://apis.io/rules/salesloft/salesloft-rules/)

#### Security (4)

Authentication, trust centre, and vulnerability disclosure.

- [Salesloft Authentication](https://apis.io/security/salesloft/salesloft-authentication/)
- [Salesloft Domain Security](https://apis.io/security/salesloft/salesloft-domain-security/)
- [Salesloft Trust Center](https://apis.io/security/salesloft/salesloft-trust-center/)
- [Salesloft Vulnerability Disclosure](https://apis.io/security/salesloft/salesloft-vulnerability-disclosure/)

#### OAuth scopes (1)

The permissions the API asks for.

- [Salesloft Scopes](https://apis.io/scopes/salesloft/salesloft-scopes/)

#### Plans and pricing (1)

Published plans, tiers and prices.

- [Salesloft Plans Pricing](https://apis.io/plans/salesloft/salesloft-plans-pricing/)

#### Rate limits (1)

Published request limits.

- [Salesloft Rate Limits](https://apis.io/rate-limits/salesloft/salesloft-rate-limits/)

#### FinOps (1)

What the API costs to run, by operation.

- [Salesloft Finops](https://apis.io/finops/salesloft/salesloft-finops/)

## Where to find this API

Links to the company's own pages. This repository publishes no copy of their specifications — the canonical document is theirs and lives at the URLs below.

- [Website](https://salesloft.com/)
- [Documentation](https://developers.salesloft.com/docs/platform/)
- [Getting started](https://developers.salesloft.com/docs/platform/intro/)
- [API reference](https://developers.salesloft.com/docs/api/)
- [Pricing](https://www.salesloft.com/pricing)
- [Support](https://help.salesloft.com/)
- [Blog](https://www.salesloft.com/resources/blog)
- [Security](https://www.salesloft.com/security)
- [Compliance](https://trust.salesloft.com/)
- [Terms of service](https://www.salesloft.com/legal/msa)
- [Privacy policy](https://www.salesloft.com/legal/platform-privacy-notice)
- [GitHub](https://github.com/SalesLoft)
- [Status](https://status.salesloft.com/)

## API Evangelist rating

**Kin Score 62.5** — strong · rubric 0.25.0 · scored 2026-10-23

| Facet | Score |
|---|---|
| Discoverability | 68.3 |
| Contract quality | 56.5 |
| Contract governance | 31.8 |
| Operational transparency | 84.2 |
| Developer ergonomics | 61.3 |
| Access clarity | 46.1 |

**Agent readiness 45.4** — agent-native

| Agent-readiness dimension | Result |
|---|---|
| Spec Presence | yes |
| Agentic Access | derived (partial credit) |
| Reversibility Documented | — |
| MCP Server | documented (partial credit) |
| Auth Clarity | served (partial credit) |
| Idempotency | documented (partial credit) |
| Error Semantics | documented (partial credit) |
| OpenAPI Examples | partial |
| Rate Limit Signal | documented (partial credit) |
| Event Surface Described | unknown |
| Agent Skills | derived (partial credit) |
| Well Known Catalog | — |
| Consent Identity | — |
| Agent Card | — |
| Dry Run Mode | — |
| Delegated Identity | — |
| Protected Resource Metadata | verified |
| Dynamic Client Registration | — |
| Agentic Commerce | — |
| Pagination Ratio | na |
| Operation Distinctiveness | distinct |

**Regulatory alignment 40.2** — Horizontal (data, software, accessibility, platform)

The rubric is published at [github.com/api-evangelist/kin-score](https://github.com/api-evangelist/kin-score). The per-check breakdown behind these numbers — which checks were earned, partial or missed — along with score history and how this provider compares to its peers, is available at [apis.io/providers/salesloft/](https://apis.io/providers/salesloft/).

## How this profile is made

API Evangelist profiles a company's public API surface the way a developer would find it: the website, developer portal and documentation, the specifications it publishes, its public repositories, and its pricing, status and changelog pages. From that it derives the properties above — contracts split per API, workflows, schemas, collections, governance rules, plans and rate limits — and scores them against the published [Kin Score rubric](https://github.com/api-evangelist/kin-score).

The artifacts are published on [APIs.io](https://apis.io), not in this repository. This repository is the public record for Salesloft: the place to say something is wrong, missing or out of date, and to ask for a re-score or a removal.

## Open an issue

- **Something about this listing** — a wrong description, a missing API, a stale artifact or a question about the rating: [open an issue on this repository](https://github.com/api-evangelist/salesloft/issues/new).
- **A new API, or one that is not in the catalog yet** — [submit it on APIs.io](https://apis.io/add/).
- **Anything else** — [the APIs.io inbox](https://github.com/api-search/inbox/issues/new) or [info@apievangelist.com](mailto:info@apievangelist.com).
