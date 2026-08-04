# Oura (oura-ring)

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
> **On a security or compliance team?** Email
> [info@apievangelist.com](mailto:info@apievangelist.com) with *security* in the subject line and
> you will get a person, not a form. We will tell you exactly which public URLs this profile was
> built from so your team can see the same surface we did, and we will take the listing down on
> request while you work through it.
>
> Full detail: **[Where this data comes from](https://apievangelist.com/about/where-our-data-comes-from)**
<!-- API-EVANGELIST-PROVENANCE:END -->

Oura is a health-technology company that makes the Oura Ring — a titanium smart ring packed with PPG, body-temperature, SpO2, and motion sensors — and the Oura App and Oura Cloud platform that turn raw biometrics into daily Sleep, Activity, Readiness, Stress, and Resilience scores. The Oura Developer Cloud exposes a v2 REST API and webhook subscriptions over OAuth 2.0 and Personal Access Tokens, letting third-party applications read 50+ health metrics, raw heart-rate and interbeat-interval time series, sleep stages, workouts, sessions, user-authored tags, and ring telemetry. A parallel /v2/sandbox/usercollection/* surface provides deterministic sample data for integration testing.

**APIs.json:** [https://raw.githubusercontent.com/api-evangelist/oura-ring/refs/heads/main/apis.yml](https://raw.githubusercontent.com/api-evangelist/oura-ring/refs/heads/main/apis.yml)

## Scope

- **Position:** Consuming
- **Access:** 3rd-Party

## Tags

- Activity
- Biometrics
- Cardiovascular
- Fitness
- Health
- HRV
- Quantified Self
- Readiness
- Resilience
- Ring
- Sleep
- SpO2
- Stress
- Wearables
- Wellness
- Women's Health

## Timestamps

- **Created:** 2026-05-25T00:00:00.000Z
- **Modified:** 2026-05-25

## APIs

### Oura Personal Info API

Retrieve the authenticated user's Oura profile including age, weight, height, biological sex, and email via /v2/usercollection/personal_info. Returned with the personal scope and represents the static profile metadata associated with the Oura account.

- **Human URL:** [https://cloud.ouraring.com/v2/docs](https://cloud.ouraring.com/v2/docs)

#### Tags

- Health
- Personal Info
- User
- Wearables

#### Properties

- [Documentation](https://cloud.ouraring.com/v2/docs)
- [OpenAPI](openapi/oura-api-openapi.yml) — [OpenAPI Specification](https://spec.openapis.org/oas/latest.html)
- [Postman Collection](collections/oura-api.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/oura-api.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)

### Oura Daily Summaries API

Per-day scored summaries derived from Oura Ring sensor data — daily_activity, daily_sleep, daily_readiness, daily_resilience, daily_stress, daily_spo2, daily_cardiovascular_age, and vO2_max. Each document collection supports list with start_date/end_date and individual document retrieval by document_id.

- **Human URL:** [https://cloud.ouraring.com/v2/docs](https://cloud.ouraring.com/v2/docs)

#### Tags

- Activity
- Cardiovascular Age
- Daily
- Health
- Readiness
- Resilience
- Sleep
- SpO2
- Stress
- VO2 Max
- Wearables

#### Properties

- [Documentation](https://cloud.ouraring.com/v2/docs)
- [OpenAPI](openapi/oura-api-openapi.yml) — [OpenAPI Specification](https://spec.openapis.org/oas/latest.html)
- [Postman Collection](collections/oura-api.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/oura-api.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)

### Oura Sleep API

Detailed sleep period documents from the ring including HRV, respiratory rate, sleep stages, and movement plus recommended sleep_time windows and user-defined rest_mode_period blocks. Endpoints under /v2/usercollection/sleep, /v2/usercollection/sleep_time, and /v2/usercollection/rest_mode_period.

- **Human URL:** [https://cloud.ouraring.com/v2/docs](https://cloud.ouraring.com/v2/docs)

#### Tags

- Health
- Rest Mode
- Sleep
- Sleep Time
- Wearables

#### Properties

- [Documentation](https://cloud.ouraring.com/v2/docs)
- [OpenAPI](openapi/oura-api-openapi.yml) — [OpenAPI Specification](https://spec.openapis.org/oas/latest.html)
- [Postman Collection](collections/oura-api.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/oura-api.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)

### Oura Activity API

Workout, session (meditation/breathwork/reset), and movement data captured by the Oura Ring. /v2/usercollection/workout returns auto-detected and manually logged workouts; /v2/usercollection/session returns guided sessions with intensity and labels.

- **Human URL:** [https://cloud.ouraring.com/v2/docs](https://cloud.ouraring.com/v2/docs)

#### Tags

- Activity
- Fitness
- Health
- Sessions
- Wearables
- Workouts

#### Properties

- [Documentation](https://cloud.ouraring.com/v2/docs)
- [OpenAPI](openapi/oura-api-openapi.yml) — [OpenAPI Specification](https://spec.openapis.org/oas/latest.html)
- [Postman Collection](collections/oura-api.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/oura-api.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)

### Oura Heart Rate API

Continuous heart-rate samples and interbeat interval (RR) data captured by the Oura Ring. /v2/usercollection/heartrate returns datetime-bounded BPM samples; /v2/usercollection/interbeat_interval returns the underlying IBI time series used for HRV calculation.

- **Human URL:** [https://cloud.ouraring.com/v2/docs](https://cloud.ouraring.com/v2/docs)

#### Tags

- Health
- Heart Rate
- HRV
- Interbeat Interval
- Time Series
- Wearables

#### Properties

- [Documentation](https://cloud.ouraring.com/v2/docs)
- [OpenAPI](openapi/oura-api-openapi.yml) — [OpenAPI Specification](https://spec.openapis.org/oas/latest.html)
- [Postman Collection](collections/oura-api.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/oura-api.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)

### Oura Tags API

User-authored annotations attached to specific days or events — legacy /v2/usercollection/tag and structured /v2/usercollection/enhanced_tag. Tags carry custom text, comments, and (for enhanced tags) typed categories like ailment, lifestyle, or nutrition.

- **Human URL:** [https://cloud.ouraring.com/v2/docs](https://cloud.ouraring.com/v2/docs)

#### Tags

- Annotations
- Enhanced Tags
- Health
- Tags
- Wearables

#### Properties

- [Documentation](https://cloud.ouraring.com/v2/docs)
- [OpenAPI](openapi/oura-api-openapi.yml) — [OpenAPI Specification](https://spec.openapis.org/oas/latest.html)
- [Postman Collection](collections/oura-api.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/oura-api.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)

### Oura Ring Configuration API

Metadata about the Oura Ring hardware itself — color, design, firmware version, hardware type, set id, and ring battery level samples — via /v2/usercollection/ring_configuration and /v2/usercollection/ring_battery_level.

- **Human URL:** [https://cloud.ouraring.com/v2/docs](https://cloud.ouraring.com/v2/docs)

#### Tags

- Battery
- Hardware
- Ring
- Telemetry
- Wearables

#### Properties

- [Documentation](https://cloud.ouraring.com/v2/docs)
- [OpenAPI](openapi/oura-api-openapi.yml) — [OpenAPI Specification](https://spec.openapis.org/oas/latest.html)
- [Postman Collection](collections/oura-api.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/oura-api.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)

### Oura Webhooks API

Create, list, renew, update, and delete event subscriptions over /v2/webhook/subscription. Each subscription targets a data_type (sleep, activity, readiness, tag, workout, session, daily_*, heartrate, etc.) and an event_type (create, update, delete) and posts events to a developer-controlled callback URL with HMAC verification.

- **Human URL:** [https://cloud.ouraring.com/v2/docs](https://cloud.ouraring.com/v2/docs)

#### Tags

- Events
- Notifications
- Subscriptions
- Webhooks

#### Properties

- [Documentation](https://cloud.ouraring.com/v2/docs)
- [OpenAPI](openapi/oura-api-openapi.yml) — [OpenAPI Specification](https://spec.openapis.org/oas/latest.html)
- [Postman Collection](collections/oura-api.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/oura-api.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)

### Oura Sandbox API

Mirror of the production usercollection endpoints under /v2/sandbox/usercollection/* that returns deterministic sample data without requiring a connected ring or real user consent. Used for integration testing, demos, and CI.

- **Human URL:** [https://cloud.ouraring.com/v2/docs](https://cloud.ouraring.com/v2/docs)

#### Tags

- Sandbox
- Sample Data
- Testing
- Wearables

#### Properties

- [Documentation](https://cloud.ouraring.com/v2/docs)
- [OpenAPI](openapi/oura-api-openapi.yml) — [OpenAPI Specification](https://spec.openapis.org/oas/latest.html)
- [Postman Collection](collections/oura-api.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/oura-api.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)

## Common Properties

- [Portal](https://ouraring.com)
- [Documentation](https://cloud.ouraring.com/v2/docs)
- [Portal](https://cloud.ouraring.com)
- [Getting Started](https://cloud.ouraring.com/docs)
- [Sign Up](https://cloud.ouraring.com/oauth/applications)
- [Authentication](https://cloud.ouraring.com/personal-access-tokens)
- [Authentication](https://cloud.ouraring.com/v2/docs#tag/oauth2)
- [Webhooks](https://cloud.ouraring.com/v2/docs#operation/Webhook_Subscription_Route)
- [Blog](https://ouraring.com/blog)
- [Privacy Policy](https://ouraring.com/legal/privacy-policy)
- [Terms of Service](https://ouraring.com/terms-and-conditions)
- [Support](https://ouraring.com/support)
- [Status Page](https://status.ouraring.com)
- [Research](https://ouraring.com/research)
- [Enterprise](https://ouraring.com/teams)
- [Enterprise](https://ouraring.com/lp/oura-health)
- [Product](https://ouraring.com/product/rings/oura-ring-4)
- [Product](https://ouraring.com/product/rings/oura-ring-4-ceramic)
- [Product](https://ouraring.com/oura-experience/app)
- [LinkedIn](https://www.linkedin.com/company/oura/)
- [Twitter](https://twitter.com/ouraring)
- [Instagram](https://www.instagram.com/ouraring/)
- [YouTube](https://www.youtube.com/@ouraring)
- [Facebook](https://www.facebook.com/ouraring/)
- [Plans](plans/oura-ring-plans-pricing.yml)
- [Rate Limits](rate-limits/oura-ring-rate-limits.yml)
- [Fin Ops](finops/oura-ring-finops.yml)
- [Features](undefined)

## Maintainers

**FN:** Kin Lane
**Email:** info@apievangelist.com
**URL:** https://apievangelist.com
