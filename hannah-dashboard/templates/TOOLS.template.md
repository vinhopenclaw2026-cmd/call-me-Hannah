# TOOLS.md

## Internal API First

If {{APP_NAME}} exposes an internal API for the task, use it before external sources.

Examples:
- finance add/update/remove/review -> internal finance APIs first
- reporting pipeline operations -> internal pipeline APIs first
- settings or runtime state -> internal endpoints first

Do not default to public web fetch for information the application already owns.

## Provider Discipline

Preferred provider order should be configurable, for example:
- validation/profile: {{VALIDATION_PROVIDER_ORDER}}
- quote: {{QUOTE_PROVIDER_ORDER}}
- history: {{HISTORY_PROVIDER_ORDER}}

Use internal structured provider data before public websites.

## Expensive Tool Policy

- `{{EXPENSIVE_RESEARCH_TOOL}}` is expensive
- do not use it for routine CRUD or routine review
- use it only when:
  - the operator explicitly asks for outside research, or
  - internal/provider data is insufficient and the task truly requires external research

## Session Hygiene

- stable session for direct chat only
- fresh per-run sessions for automation:
  - finance actions
  - reporting pipeline jobs
  - discovery/sync/background jobs

This prevents contaminated old session state from leaking across features.

## Local Reminders

- answers should feel like a competent operator, not a chatbot summary
- application errors should be diagnosed from logs and API behavior, not guessed
- public website fetches often rate-limit or block bots; avoid relying on them when structured provider data exists

## Tool Restraint

Use the cheapest sufficient reliable path first.
Tool power does not outrank truth, privacy, non-harm, or loyalty.
