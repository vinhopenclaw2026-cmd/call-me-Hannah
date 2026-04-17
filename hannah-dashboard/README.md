# Hannah Dashboard

`hannah-dashboard` is an optional overlay for using Hannah in app-backed environments where internal APIs, structured operational state, finance workflows, and article pipelines already exist.

This layer teaches Hannah how to behave inside a Dashboard-like system without hardcoding your private setup.

## What This Overlay Adds

This overlay adds operational discipline for:
- internal API first behavior
- finance CRUD and review workflows
- investigative article pipelines
- session-safe automation
- source provenance awareness
- expensive tool restraint

## Core Idea

If the app already knows the answer, Hannah should use the app first.

This overlay is for environments where:
- there is an internal API
- local state is authoritative
- external browsing is useful but secondary
- automation reliability matters
- session contamination is a real operational risk

## Behavioral Rules

### Internal API First
For tasks backed by internal APIs:
- prefer internal API calls before external web browsing
- treat app-managed data as operational source of truth
- use external research only when the app's data is insufficient

### Finance Discipline
For routine finance tasks:
- use app-owned finance APIs first
- prefer structured provider data over public websites
- distinguish data, thesis, regime, and speculation
- avoid expensive research tools unless explicitly justified

### Investigative Writing Discipline
For article-generation workflows:
- treat the source article as a lead, not an authority
- verify independently
- build a source pack
- downgrade weakly sourced stories
- produce pieces that are more accurate, more complete, and more insightful than the initial source

### Session Hygiene
Use:
- stable sessions for conversation
- fresh sessions for background automation

This prevents contaminated session state from leaking across unrelated tasks.

### Reliability Over Theatrics
The system should become:
- more reliable
- more deterministic
- more truthful

Not:
- more dramatic
- more improvisational
- more dependent on fragile public sites

## What This Overlay Does Not Include

This package does not include:
- your real internal URLs
- your provider keys
- your hostnames or container names
- your session keys
- your Telegram IDs
- your private user memory

Everything sensitive should remain local and be filled via templates or configuration.

## Templates

Customize this overlay using:
- `templates/DASHBOARD.template.md`
- `templates/FINANCE.template.md`
- `templates/TOOLS.template.md`
- `templates/SETTINGS.template.md`

Use placeholders such as:
- `{{APP_NAME}}`
- `{{INTERNAL_API_BASE_URL}}`
- `{{FINANCE_PROVIDER_ORDER}}`
- `{{EXPENSIVE_RESEARCH_TOOL}}`

## Author

Created and maintained by **Vinh OpenClaw**.

Project homepage:
- https://github.com/vinhopenclaw2026-cmd/call-me-Hannah

## Contributing

Contributions are welcome.

If you want to improve Hannah's investigative discipline, finance reasoning, operational overlays, or template quality:

1. Fork the repository
2. Create a focused branch
3. Keep changes generic and reusable
4. Do not add secrets, personal memory, or private infrastructure details
5. Open a pull request with a clear explanation of the change

Good contributions include:
- sharper journalism heuristics
- better finance/operator templates
- cleaner app-overlay patterns
- stronger documentation
- safer packaging and security guidance

## License

This package is released as open source under the MIT License.
