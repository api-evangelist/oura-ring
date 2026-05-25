# Oura (oura-ring)
Oura is a health-technology company that makes the Oura Ring — a titanium smart ring packed with PPG, body-temperature, SpO2, and motion sensors — and the Oura App and Oura Cloud platform that turn raw biometrics into daily Sleep, Activity, Readiness, Stress, and Resilience scores. The Oura Developer Cloud exposes a v2 REST API and webhook subscriptions over OAuth 2.0 and Personal Access Tokens, letting third-party applications read 50+ health metrics, raw heart-rate and interbeat-interval time series, sleep stages, workouts, sessions, user-authored tags, and ring telemetry. A parallel `/v2/sandbox/usercollection/*` surface provides deterministic sample data for integration testing.

**URL:** [Visit APIs.json](https://raw.githubusercontent.com/api-evangelist/oura-ring/refs/heads/main/apis.yml)

**Run:** [Capabilities Using Naftiko](https://github.com/naftiko/fleet?utm_source=api-evangelist&utm_medium=readme&utm_campaign=company-api-evangelist&utm_content=repo)

## Tags

 - Activity, Biometrics, Cardiovascular, Fitness, Health, HRV, Quantified Self, Readiness, Resilience, Ring, Sleep, SpO2, Stress, Wearables, Wellness, Women's Health

## Timestamps

- **Created:** 2026-05-25
- **Modified:** 2026-05-25

## APIs

### Oura Personal Info API
Retrieve the authenticated user's static profile (age, weight, height, biological sex, email) via `/v2/usercollection/personal_info`.

**Human URL:** [https://cloud.ouraring.com/v2/docs](https://cloud.ouraring.com/v2/docs)

- [Documentation](https://cloud.ouraring.com/v2/docs)
- [OpenAPI](openapi/oura-api-openapi.yml)
- [Naftiko Capability — Personal Info](capabilities/personal-info.yaml)

### Oura Daily Summaries API
Per-day scored summaries: `daily_activity`, `daily_sleep`, `daily_readiness`, `daily_resilience`, `daily_stress`, `daily_spo2`, `daily_cardiovascular_age`, `vO2_max`. List by date range or fetch by `document_id`.

**Human URL:** [https://cloud.ouraring.com/v2/docs](https://cloud.ouraring.com/v2/docs)

- [OpenAPI](openapi/oura-api-openapi.yml)
- [JSON Schema — Daily Sleep](json-schema/oura-daily-sleep-schema.json)
- [JSON Schema — Daily Activity](json-schema/oura-daily-activity-schema.json)
- [Naftiko Capability — Daily Summaries](capabilities/daily-summaries.yaml)

### Oura Sleep API
Detailed sleep period documents (HRV, respiratory rate, stages, movement), recommended `sleep_time` windows, and user-defined `rest_mode_period` blocks.

**Human URL:** [https://cloud.ouraring.com/v2/docs](https://cloud.ouraring.com/v2/docs)

- [OpenAPI](openapi/oura-api-openapi.yml)
- [Naftiko Capability — Sleep](capabilities/sleep.yaml)

### Oura Activity API
Auto-detected and manual workouts (`/v2/usercollection/workout`) plus guided sessions — meditation, breathwork, reset (`/v2/usercollection/session`).

**Human URL:** [https://cloud.ouraring.com/v2/docs](https://cloud.ouraring.com/v2/docs)

- [OpenAPI](openapi/oura-api-openapi.yml)
- [Naftiko Capability — Activity](capabilities/activity.yaml)

### Oura Heart Rate API
Continuous heart-rate samples and interbeat interval (RR) time series.

**Human URL:** [https://cloud.ouraring.com/v2/docs](https://cloud.ouraring.com/v2/docs)

- [OpenAPI](openapi/oura-api-openapi.yml)
- [Naftiko Capability — Heart Rate](capabilities/heart-rate.yaml)

### Oura Tags API
Legacy free-text tags and structured enhanced tags (typed categories: ailment, lifestyle, nutrition, etc.).

**Human URL:** [https://cloud.ouraring.com/v2/docs](https://cloud.ouraring.com/v2/docs)

- [OpenAPI](openapi/oura-api-openapi.yml)
- [Naftiko Capability — Tags](capabilities/tags.yaml)

### Oura Ring Configuration API
Ring hardware metadata (color, design, firmware, hardware type) and battery level samples.

**Human URL:** [https://cloud.ouraring.com/v2/docs](https://cloud.ouraring.com/v2/docs)

- [OpenAPI](openapi/oura-api-openapi.yml)
- [Naftiko Capability — Ring Configuration](capabilities/ring-configuration.yaml)

### Oura Webhooks API
Create, list, get, update, renew, and delete webhook subscriptions. Each subscription pairs a `data_type` with an `event_type` (create / update / delete) and posts to a developer callback URL.

**Human URL:** [https://cloud.ouraring.com/v2/docs](https://cloud.ouraring.com/v2/docs)

- [OpenAPI](openapi/oura-api-openapi.yml)
- [JSON Schema — Webhook Subscription](json-schema/oura-webhook-subscription-schema.json)
- [Naftiko Capability — Webhooks](capabilities/webhooks.yaml)

### Oura Sandbox API
Mirror of the production `usercollection` surface under `/v2/sandbox/usercollection/*` that returns deterministic sample data — useful for CI, demos, and developing without a real ring.

**Human URL:** [https://cloud.ouraring.com/v2/docs](https://cloud.ouraring.com/v2/docs)

- [OpenAPI](openapi/oura-api-openapi.yml)
- [Naftiko Capability — Sandbox](capabilities/sandbox.yaml)

## Authentication

- **OAuth 2.0** — `https://cloud.ouraring.com/oauth/authorize` (authorize), `https://api.ouraring.com/oauth/token` (token), `https://api.ouraring.com/oauth/revoke` (revoke). Scopes: `email`, `personal`, `daily`, `heartrate`, `workout`, `tag`, `session`, `spo2`.
- **Personal Access Tokens** — long-lived bearer tokens generated from a user's developer dashboard for personal projects.

Both authentication mechanisms send the credential as `Authorization: Bearer <token>` and count against the same per-token rate limit.

## Rate limits

- 5,000 requests per 5-minute window per access token.
- Heavy time-series endpoints (`heartrate`, `interbeat_interval`) should be paginated via `next_token`; webhooks are preferred over polling for state changes.

See [`rate-limits/oura-ring-rate-limits.yml`](rate-limits/oura-ring-rate-limits.yml).

## Commercial offering

- **Oura Ring 4** — $349 (titanium) / $499 (Ceramic); FSA/HSA eligible.
- **Oura Membership** — $5.99/month or $69.99/year; required to unlock full insights in the Oura App.
- **Oura for Teams** — quoted enterprise program for organizations, research cohorts, and sports teams.
- **Oura Developer Cloud** — free API tier, no per-call charges.

See [`plans/oura-ring-plans-pricing.yml`](plans/oura-ring-plans-pricing.yml) and [`finops/oura-ring-finops.yml`](finops/oura-ring-finops.yml).

## Artifacts

### OpenAPI

- [Oura API v2](openapi/oura-api-openapi.yml)

### JSON Schema

- [Daily Sleep](json-schema/oura-daily-sleep-schema.json)
- [Daily Activity](json-schema/oura-daily-activity-schema.json)
- [Webhook Subscription](json-schema/oura-webhook-subscription-schema.json)

### JSON-LD

- [Oura Context](json-ld/oura-ring-context.jsonld)

### Examples

- [Daily Sleep](examples/oura-daily-sleep-example.json)
- [Daily Activity](examples/oura-daily-activity-example.json)
- [Webhook Subscription — Create](examples/oura-webhook-subscription-create-example.json)

### Capabilities (Naftiko)

- [Personal Info](capabilities/personal-info.yaml)
- [Daily Summaries](capabilities/daily-summaries.yaml)
- [Sleep](capabilities/sleep.yaml)
- [Activity](capabilities/activity.yaml)
- [Heart Rate](capabilities/heart-rate.yaml)
- [Tags](capabilities/tags.yaml)
- [Ring Configuration](capabilities/ring-configuration.yaml)
- [Webhooks](capabilities/webhooks.yaml)
- [Sandbox](capabilities/sandbox.yaml)

### Spectral rules

- [Oura Ruleset](rules/oura-ring-rules.yml)

### Vocabulary

- [Oura Vocabulary](vocabulary/oura-ring-vocabulary.yml)

### Commercial artifacts

- [Plans / Pricing](plans/oura-ring-plans-pricing.yml)
- [Rate Limits](rate-limits/oura-ring-rate-limits.yml)
- [FinOps Definition](finops/oura-ring-finops.yml)

## Maintainers

**FN:** Kin Lane

**Email:** info@apievangelist.com
