# Oura Ring GraphQL Schema

Conceptual GraphQL schema derived from the Oura REST API v2
(https://cloud.ouraring.com/v2/docs). The Oura Ring is a titanium smart ring
that tracks continuous biometrics — PPG, body temperature, SpO2, motion — and
surfaces them through the Oura Cloud as scored daily summaries for sleep,
activity, readiness, stress, and resilience.

## Source API

- **Base URL:** https://cloud.ouraring.com/v2
- **Auth:** OAuth 2.0 (8 scopes) and Personal Access Tokens
- **Rate limit:** 5,000 requests per 5 minutes per access token
- **Sandbox:** /v2/sandbox/usercollection/* (deterministic sample data)

## Schema file

`oura-ring-schema.graphql`

## Type groups

### Personal Info
`PersonalInfo`, `PersonalInfoDetails`, `Age`, `Weight`, `Height`,
`BiologicalSex`

Authenticated user profile from `/v2/usercollection/personal_info`.
Requires the `personal` scope.

### Ring Hardware
`Ring`, `RingDetails`, `RingColor`, `RingDesign`, `RingSize`,
`RingBatteryLevel`

Ring configuration (color, design, firmware, hardware type, set ID) and
per-sample battery level from `/v2/usercollection/ring_configuration` and
`/v2/usercollection/ring_battery_level`.

### Sleep
`Sleep`, `SleepDetails`, `SleepScore`, `SleepContributors`, `SleepStage`,
`SleepBreath`, `SleepHrv`, `SleepHR`, `SleepTemperature`, `SleepLatency`,
`SleepEfficiency`, `SleepMidpoint`, `SleepRem`, `SleepDeep`, `SleepLight`,
`SleepAwake`, `DailySleep`, `SleepTime`, `RestModePeriod`, `RestModeEpisode`

Detailed sleep period documents from `/v2/usercollection/sleep` including HRV,
respiratory rate, sleep stages (REM/deep/light/awake), movement, efficiency,
and midpoint. `DailySleep` surfaces the scored day-level summary.
`SleepTime` provides the recommended bedtime window. `RestModePeriod` captures
user-defined recovery blocks.

### Activity
`Activity`, `ActivityDetails`, `ActivityScore`, `ActivityContributors`,
`Steps`, `Calories`, `Met`, `MetDetails`, `DailyActivity`, `ActivityClass`

Per-day activity documents from `/v2/usercollection/daily_activity` including
MET time series, step counts, calorie breakdown, and inactivity intervals.

### Workouts & Sessions
`Workout`, `WorkoutDetails`, `WorkoutType`, `WorkoutIntensity`,
`Session`, `SessionDetails`

Auto-detected and manually logged workouts from `/v2/usercollection/workout`.
Guided sessions (meditation, breathwork, reset) from
`/v2/usercollection/session`.

### Heart Rate & HRV
`HeartRate`, `HeartRateDetails`, `HrvSample`, `HrvDetails`,
`InterbeatInterval`

Continuous BPM samples from `/v2/usercollection/heartrate` and underlying
interbeat-interval (RR) time series from
`/v2/usercollection/interbeat_interval`.

### Readiness
`Readiness`, `ReadinessDetails`, `ReadinessScore`, `ReadinessContributors`

Daily readiness score combining HRV balance, sleep balance, recovery index,
resting heart rate, and body temperature deviation from
`/v2/usercollection/daily_readiness`.

### Temperature
`Temperature`, `TemperatureDetails`, `SkinTemperature`

Skin temperature deviation and trend from
`/v2/usercollection/daily_temperature`.

### Stress & Resilience
`DailyStress`, `StressSample`, `DailyResilience`, `ResilienceContributors`

Minute-level stress classification (high/recovered/relaxed/restored) from
`/v2/usercollection/daily_stress` and long-term resilience level from
`/v2/usercollection/daily_resilience`.

### SpO2, Cardiovascular & VO2 Max
`DailySpo2`, `Spo2Percentage`, `CardiovascularAge`, `Vo2Max`

Nighttime SpO2 average and breathing-disturbance index from
`/v2/usercollection/daily_spo2`. Cardiovascular age estimation from
`/v2/usercollection/cardiovascular_age`. VO2 Max from
`/v2/usercollection/vo2_max`.

### Tags
`Tag`, `TagDetails`, `EnhancedTag`

User-authored day annotations from `/v2/usercollection/tag` (legacy) and
typed structured annotations from `/v2/usercollection/enhanced_tag` carrying
categories such as ailment, lifestyle, and nutrition.

### Auth
`APIKey`, `Token`

Personal Access Token metadata and OAuth token representation.

### Webhooks
`Webhook`, `WebhookEvent`

Subscription management via `/v2/webhook/subscription`. Each subscription
targets a `dataType` (sleep, activity, readiness, etc.) and `eventType`
(create, update, delete) and posts HMAC-signed events to a callback URL.

### Pagination & Inputs
`PageInfo`, `DateRangeInput`, `DateTimeRangeInput`, `WebhookCreateInput`,
`WebhookUpdateInput`

All list queries accept `DateRangeInput` (date-bounded) or
`DateTimeRangeInput` (datetime-bounded for time-series resources) with cursor
support via `nextToken`.

## Named types count

67 named types (excluding scalar aliases and enum values).

## Queries

| Query | REST equivalent |
|---|---|
| `personalInfo` | GET /v2/usercollection/personal_info |
| `ringConfigurations` | GET /v2/usercollection/ring_configuration |
| `ringBatteryLevels` | GET /v2/usercollection/ring_battery_level |
| `sleep` / `sleepById` | GET /v2/usercollection/sleep |
| `dailySleep` / `dailySleepById` | GET /v2/usercollection/daily_sleep |
| `sleepTime` | GET /v2/usercollection/sleep_time |
| `dailyActivity` / `dailyActivityById` | GET /v2/usercollection/daily_activity |
| `workouts` / `workoutById` | GET /v2/usercollection/workout |
| `sessions` / `sessionById` | GET /v2/usercollection/session |
| `heartRate` | GET /v2/usercollection/heartrate |
| `interbeatInterval` | GET /v2/usercollection/interbeat_interval |
| `dailyReadiness` / `dailyReadinessById` | GET /v2/usercollection/daily_readiness |
| `dailyStress` / `dailyStressById` | GET /v2/usercollection/daily_stress |
| `dailyResilience` / `dailyResilienceById` | GET /v2/usercollection/daily_resilience |
| `dailySpo2` / `dailySpo2ById` | GET /v2/usercollection/daily_spo2 |
| `cardiovascularAge` | GET /v2/usercollection/cardiovascular_age |
| `vo2Max` | GET /v2/usercollection/vo2_max |
| `dailyTemperature` / `dailyTemperatureById` | GET /v2/usercollection/daily_temperature |
| `tags` / `tagById` | GET /v2/usercollection/tag |
| `enhancedTags` / `enhancedTagById` | GET /v2/usercollection/enhanced_tag |
| `restModePeriods` / `restModePeriodById` | GET /v2/usercollection/rest_mode_period |
| `webhooks` / `webhookById` | GET /v2/webhook/subscription |
| `apiKeys` | GET /v2/personal-access-tokens |

## Mutations

| Mutation | REST equivalent |
|---|---|
| `createTag` | POST /v2/usercollection/tag |
| `deleteTag` | DELETE /v2/usercollection/tag/{id} |
| `createEnhancedTag` | POST /v2/usercollection/enhanced_tag |
| `updateEnhancedTag` | PUT /v2/usercollection/enhanced_tag/{id} |
| `deleteEnhancedTag` | DELETE /v2/usercollection/enhanced_tag/{id} |
| `createWebhook` | POST /v2/webhook/subscription |
| `updateWebhook` | PUT /v2/webhook/subscription/{id} |
| `renewWebhook` | PUT /v2/webhook/subscription/{id}/renew |
| `deleteWebhook` | DELETE /v2/webhook/subscription/{id} |
