# Oura (oura-ring)

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
