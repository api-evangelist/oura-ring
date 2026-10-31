# Oura

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

Oura is a health-technology company that makes the Oura Ring — a titanium smart ring packed with PPG, body-temperature, SpO2, and motion sensors — and the Oura App and Oura Cloud platform that turn raw biometrics into daily Sleep, Activity, Readiness, Stress, and Resilience scores. The Oura Developer Cloud exposes a v2 REST API and webhook subscriptions over OAuth 2.0 and Personal Access Tokens, letting third-party applications read 50+ health metrics, raw heart-rate and interbeat-interval time series, sleep stages, workouts, sessions, user-authored tags, and ring telemetry. A parallel /v2/sandbox/usercollection/* surface provides deterministic sample data for integration testing.

**Areas:** Activity · Biometrics · Cardiovascular · Fitness · Health · HRV · Quantified Self · Readiness · Resilience · Ring · Sleep · SpO2

## Oura on APIs.io

Everything profiled for Oura is published on APIs.io rather than in this repository. Start at the provider page — **[apis.io/providers/oura-ring/](https://apis.io/providers/oura-ring/)** — or go straight to one of the APIs or properties below.

### APIs (22)

- [Oura Daily Activity Routes API](https://apis.io/apis/oura-ring/oura-ring-daily-activity-routes-api/) — The Daily Activity Routes API from Oura — 2 operation(s) for daily activity routes.
- [Oura Daily Cardiovascular Age Routes API](https://apis.io/apis/oura-ring/oura-ring-daily-cardiovascular-age-routes-api/) — The Daily Cardiovascular Age Routes API from Oura — 2 operation(s) for daily cardiovascular age routes.
- [Oura Daily Readiness Routes API](https://apis.io/apis/oura-ring/oura-ring-daily-readiness-routes-api/) — The Daily Readiness Routes API from Oura — 2 operation(s) for daily readiness routes.
- [Oura Daily Resilience Routes API](https://apis.io/apis/oura-ring/oura-ring-daily-resilience-routes-api/) — The Daily Resilience Routes API from Oura — 2 operation(s) for daily resilience routes.
- [Oura Daily Sleep Routes API](https://apis.io/apis/oura-ring/oura-ring-daily-sleep-routes-api/) — The Daily Sleep Routes API from Oura — 2 operation(s) for daily sleep routes.
- [Oura Daily Spo2 Routes API](https://apis.io/apis/oura-ring/oura-ring-daily-spo2-routes-api/) — The Daily Spo2 Routes API from Oura — 2 operation(s) for daily spo2 routes.
- [Oura Daily Stress Routes API](https://apis.io/apis/oura-ring/oura-ring-daily-stress-routes-api/) — The Daily Stress Routes API from Oura — 2 operation(s) for daily stress routes.
- [Oura Enhanced Tag Routes API](https://apis.io/apis/oura-ring/oura-ring-enhanced-tag-routes-api/) — The Enhanced Tag Routes API from Oura — 2 operation(s) for enhanced tag routes.
- [Oura Heart Rate Routes API](https://apis.io/apis/oura-ring/oura-ring-heart-rate-routes-api/) — The Heart Rate Routes API from Oura — 1 operation(s) for heart rate routes.
- [Oura Interbeat Interval Routes API](https://apis.io/apis/oura-ring/oura-ring-interbeat-interval-routes-api/) — The Interbeat Interval Routes API from Oura — 1 operation(s) for interbeat interval routes.
- [Oura Personal Info Routes API](https://apis.io/apis/oura-ring/oura-ring-personal-info-routes-api/) — The Personal Info Routes API from Oura — 1 operation(s) for personal info routes.
- [Oura Rest Mode Period Routes API](https://apis.io/apis/oura-ring/oura-ring-rest-mode-period-routes-api/) — The Rest Mode Period Routes API from Oura — 2 operation(s) for rest mode period routes.
- [Oura Ring Battery Level Routes API](https://apis.io/apis/oura-ring/oura-ring-ring-battery-level-routes-api/) — The Ring Battery Level Routes API from Oura — 1 operation(s) for ring battery level routes.
- [Oura Ring Configuration Routes API](https://apis.io/apis/oura-ring/oura-ring-ring-configuration-routes-api/) — The Ring Configuration Routes API from Oura — 2 operation(s) for ring configuration routes.
- [Oura Sandbox Routes API](https://apis.io/apis/oura-ring/oura-ring-sandbox-routes-api/) — The Sandbox Routes API from Oura — 35 operation(s) for sandbox routes.
- [Oura Session Routes API](https://apis.io/apis/oura-ring/oura-ring-session-routes-api/) — The Session Routes API from Oura — 2 operation(s) for session routes.
- [Oura Sleep Routes API](https://apis.io/apis/oura-ring/oura-ring-sleep-routes-api/) — The Sleep Routes API from Oura — 2 operation(s) for sleep routes.
- [Oura Sleep Time Routes API](https://apis.io/apis/oura-ring/oura-ring-sleep-time-routes-api/) — The Sleep Time Routes API from Oura — 2 operation(s) for sleep time routes.
- [Oura Tag Routes API](https://apis.io/apis/oura-ring/oura-ring-tag-routes-api/) — The Tag Routes API from Oura — 2 operation(s) for tag routes.
- [Oura VO2 Max Routes API](https://apis.io/apis/oura-ring/oura-ring-vo2-max-routes-api/) — The VO2 Max Routes API from Oura — 2 operation(s) for vo2 max routes.
- [Oura Webhook Subscription Routes API](https://apis.io/apis/oura-ring/oura-ring-webhook-subscription-routes-api/) — The Webhook Subscription Routes API from Oura — 3 operation(s) for webhook subscription routes.
- [Oura Workout Routes API](https://apis.io/apis/oura-ring/oura-ring-workout-routes-api/) — The Workout Routes API from Oura — 2 operation(s) for workout routes.

### Published properties

Each property below is a page on APIs.io carrying the machine-readable artifact and what it says.

#### GraphQL (1)

GraphQL schemas.

- [Moved to /providers/oura-ring/](https://apis.io/graphqls/oura-ring/oura-ring-graphql/)

#### Agentic access (1)

Which operations an agent can call, which act, and which need a human in the loop.

- [Oura Ring Agentic Access](https://apis.io/agentic-access/oura-ring/oura-ring-agentic-access/)

#### JSON Schema (3)

The data models the API reads and writes.

- [Oura Daily Activity](https://apis.io/schemas/oura-ring/oura-daily-activity/)
- [Oura Daily Sleep](https://apis.io/schemas/oura-ring/oura-daily-sleep/)
- [Oura Webhook Subscription](https://apis.io/schemas/oura-ring/oura-webhook-subscription/)

#### JSON-LD (1)

Linked-data contexts for the provider's vocabulary.

- [Oura Ring Context](https://apis.io/jsonld/oura-ring/oura-ring-context/)

#### Vocabulary (1)

The provider's domain terms, defined.

- [Oura Ring Vocabulary](https://apis.io/vocabularies/oura-ring/oura-ring-vocabulary/)

#### Examples (3)

Example requests and responses.

- [Oura Daily Activity Example](https://apis.io/examples/oura-ring/oura-daily-activity-example/)
- [Oura Daily Sleep Example](https://apis.io/examples/oura-ring/oura-daily-sleep-example/)
- [Oura Webhook Subscription Create Example](https://apis.io/examples/oura-ring/oura-webhook-subscription-create-example/)

#### Collections (45)

Postman and Open Collection request collections.

- [Oura API](https://apis.io/collections/oura-ring/open-oura-api/)
- [Oura Daily Activity Routes API](https://apis.io/collections/oura-ring/open-oura-ring-daily-activity-routes-api/)
- [Oura Daily Activity Routes Daily Cardiovascular Age Routes API](https://apis.io/collections/oura-ring/open-oura-ring-daily-cardiovascular-age-routes-api/)
- [Oura Daily Activity Routes Daily Readiness Routes API](https://apis.io/collections/oura-ring/open-oura-ring-daily-readiness-routes-api/)
- [Oura Daily Activity Routes Daily Resilience Routes API](https://apis.io/collections/oura-ring/open-oura-ring-daily-resilience-routes-api/)
- [Oura Daily Activity Routes Daily Sleep Routes API](https://apis.io/collections/oura-ring/open-oura-ring-daily-sleep-routes-api/)
- [Oura Daily Activity Routes Daily Spo2 Routes API](https://apis.io/collections/oura-ring/open-oura-ring-daily-spo2-routes-api/)
- [Oura Daily Activity Routes Daily Stress Routes API](https://apis.io/collections/oura-ring/open-oura-ring-daily-stress-routes-api/)
- [Oura Daily Activity Routes Enhanced Tag Routes API](https://apis.io/collections/oura-ring/open-oura-ring-enhanced-tag-routes-api/)
- [Oura Daily Activity Routes Heart Rate Routes API](https://apis.io/collections/oura-ring/open-oura-ring-heart-rate-routes-api/)
- [Oura Daily Activity Routes Interbeat Interval Routes API](https://apis.io/collections/oura-ring/open-oura-ring-interbeat-interval-routes-api/)
- [Oura Daily Activity Routes Personal Info Routes API](https://apis.io/collections/oura-ring/open-oura-ring-personal-info-routes-api/)
- [Oura Daily Activity Routes Rest Mode Period Routes API](https://apis.io/collections/oura-ring/open-oura-ring-rest-mode-period-routes-api/)
- [Oura Daily Activity Routes Ring Battery Level Routes API](https://apis.io/collections/oura-ring/open-oura-ring-ring-battery-level-routes-api/)
- [Oura Daily Activity Routes Ring Configuration Routes API](https://apis.io/collections/oura-ring/open-oura-ring-ring-configuration-routes-api/)
- [Oura Daily Activity Routes Sandbox Routes API](https://apis.io/collections/oura-ring/open-oura-ring-sandbox-routes-api/)
- [Oura Daily Activity Routes Session Routes API](https://apis.io/collections/oura-ring/open-oura-ring-session-routes-api/)
- [Oura Daily Activity Routes Sleep Routes API](https://apis.io/collections/oura-ring/open-oura-ring-sleep-routes-api/)
- [Oura Daily Activity Routes Sleep Time Routes API](https://apis.io/collections/oura-ring/open-oura-ring-sleep-time-routes-api/)
- [Oura Daily Activity Routes Tag Routes API](https://apis.io/collections/oura-ring/open-oura-ring-tag-routes-api/)
- [Oura Daily Activity Routes VO2 Max Routes API](https://apis.io/collections/oura-ring/open-oura-ring-vo2-max-routes-api/)
- [Oura Daily Activity Routes Webhook Subscription Routes API](https://apis.io/collections/oura-ring/open-oura-ring-webhook-subscription-routes-api/)
- [Oura Daily Activity Routes Workout Routes API](https://apis.io/collections/oura-ring/open-oura-ring-workout-routes-api/)
- [Oura Daily Activity Routes API](https://apis.io/collections/oura-ring/postman-oura-ring-daily-activity-routes-api/)
- [Oura Daily Activity Routes Daily Cardiovascular Age Routes API](https://apis.io/collections/oura-ring/postman-oura-ring-daily-cardiovascular-age-routes-api/)
- …and 20 more published on APIs.io

#### Governance rules (2)

Spectral rulesets for the provider's contracts.

- [Oura — jsonschema rules](https://apis.io/rules/oura-ring/oura-ring-jsonschema-spectral-rules/)
- [Oura API Rules](https://apis.io/rules/oura-ring/oura-ring-rules/)

#### Security (3)

Authentication, trust centre, and vulnerability disclosure.

- [Oura Ring Domain Security](https://apis.io/security/oura-ring/oura-ring-domain-security/)
- [Oura Ring Trust Center](https://apis.io/security/oura-ring/oura-ring-trust-center/)
- [Oura Ring Vulnerability Disclosure](https://apis.io/security/oura-ring/oura-ring-vulnerability-disclosure/)

#### Plans and pricing (1)

Published plans, tiers and prices.

- [Oura Ring Plans Pricing](https://apis.io/plans/oura-ring/oura-ring-plans-pricing/)

#### Rate limits (1)

Published request limits.

- [Oura Ring Rate Limits](https://apis.io/rate-limits/oura-ring/oura-ring-rate-limits/)

#### FinOps (1)

What the API costs to run, by operation.

- [Oura Ring Finops](https://apis.io/finops/oura-ring/oura-ring-finops/)

## Where to find this API

Links to the company's own pages. This repository publishes no copy of their specifications — the canonical document is theirs and lives at the URLs below.

- [Website](https://www.ouraring.com/)
- [Documentation](https://cloud.ouraring.com/v2/docs)
- [Getting started](https://cloud.ouraring.com/docs)
- [Support](https://ouraring.com/support)
- [Blog](https://ouraring.com/blog)
- [Terms of service](https://ouraring.com/terms-and-conditions)
- [Privacy policy](https://ouraring.com/legal/privacy-policy)
- [Status](https://status.ouraring.com)

## API Evangelist rating

**Kin Score 49.0** — developing · rubric 0.25.0 · scored 2026-10-23

| Facet | Score |
|---|---|
| Discoverability | 66.1 |
| Contract quality | 49.1 |
| Contract governance | 13.6 |
| Operational transparency | 39.5 |
| Developer ergonomics | 51.2 |
| Access clarity | 57.9 |

**Agent readiness 28.1** — agent-aware

| Agent-readiness dimension | Result |
|---|---|
| Spec Presence | yes |
| Agentic Access | derived (partial credit) |
| Reversibility Documented | — |
| MCP Server | — |
| Auth Clarity | bearer (partial credit) |
| Idempotency | — |
| Error Semantics | verified |
| OpenAPI Examples | — |
| Rate Limit Signal | derived (partial credit) |
| Event Surface Described | unknown |
| Agent Skills | — |
| Well Known Catalog | — |
| Consent Identity | — |
| Agent Card | — |
| Dry Run Mode | — |
| Delegated Identity | — |
| Protected Resource Metadata | — |
| Dynamic Client Registration | — |
| Agentic Commerce | — |
| Pagination Ratio | — |
| Operation Distinctiveness | distinct |

**Regulatory alignment 27.3** — Health

The rubric is published at [github.com/api-evangelist/kin-score](https://github.com/api-evangelist/kin-score). The per-check breakdown behind these numbers — which checks were earned, partial or missed — along with score history and how this provider compares to its peers, is available at [apis.io/providers/oura-ring/](https://apis.io/providers/oura-ring/).

## How this profile is made

API Evangelist profiles a company's public API surface the way a developer would find it: the website, developer portal and documentation, the specifications it publishes, its public repositories, and its pricing, status and changelog pages. From that it derives the properties above — contracts split per API, workflows, schemas, collections, governance rules, plans and rate limits — and scores them against the published [Kin Score rubric](https://github.com/api-evangelist/kin-score).

The artifacts are published on [APIs.io](https://apis.io), not in this repository. This repository is the public record for Oura: the place to say something is wrong, missing or out of date, and to ask for a re-score or a removal.

## Open an issue

- **Something about this listing** — a wrong description, a missing API, a stale artifact or a question about the rating: [open an issue on this repository](https://github.com/api-evangelist/oura-ring/issues/new).
- **A new API, or one that is not in the catalog yet** — [submit it on APIs.io](https://apis.io/add/).
- **Anything else** — [the APIs.io inbox](https://github.com/api-search/inbox/issues/new) or [info@apievangelist.com](mailto:info@apievangelist.com).
