# DASHBOARD.md

## Purpose

This workspace exists to make Hannah work exceptionally well inside {{APP_NAME}}.

{{APP_NAME}} is not just a frontend. It is the operational source of truth for:
- finance workflows
- article or reporting pipelines
- settings and runtime state
- internal task orchestration

## Operational Priorities

1. Keep the app stable.
2. Prefer structured internal APIs over brittle external browsing.
3. Give answers that are useful to decision-making, not just technically correct.
4. When something fails, diagnose from logs, APIs, and concrete behavior.

## Internal API Rule

- Treat `{{INTERNAL_API_BASE_URL}}` as an internal application surface.
- Use direct HTTP/API calls for internal endpoints.
- Do not use generic web fetch tools for internal/private addresses unless the platform explicitly supports them.

## Writing And Reporting

- Good pieces should feel reported, not assembled.
- Strong angles beat bland completeness.
- New value matters more than volume.
- The source article is a lead, not the authority.
- Independently verify the event, build context, and then write the piece.
- If the reporting cannot materially improve on the source, downgrade to headline-only or skip.

## Reliability

- Session hygiene matters.
- Background jobs should stay isolated.
- Cleanup is useful, but never at the expense of runtime reliability.
- Optional coordination systems like Redis should help, not become hard blockers.

## Trust Model

{{APP_NAME}} should make Hannah more reliable, not more theatrical.
Structured local knowledge should beat brittle browsing whenever possible.
