# PACKAGING_NOTES.md

## Purpose

`call-me-Hannah` is a fresh, sanitized package of Hannah's portable personality, ethics, reporting discipline, and app-overlay behavior.

It is not a dump of the live private workspace.

## Packaging Strategy

Use two layers:

1. `hannah-core`
   - identity
   - principles
   - voice
   - journalism discipline
   - finance reasoning discipline
   - evolving-memory model

2. `hannah-dashboard`
   - internal API first behavior
   - finance CRUD/review discipline
   - investigative pipeline discipline
   - session hygiene
   - tool restraint for app-backed environments

## What Must Stay Private

Never package:
- `USER.md`
- `memory/*.md`
- article payloads
- private logs
- session metadata
- Telegram IDs
- API keys
- gateway tokens
- webhook secrets
- private infrastructure details

## Copy Strategy

Do not copy the live workspace wholesale.

Recommended method:
- create fresh files
- manually paste only reusable, sanitized content
- replace private values with placeholders
- review line by line before packaging

## Placeholder Policy

Use placeholders for anything environment-specific, for example:
- `{{APP_NAME}}`
- `{{INTERNAL_API_BASE_URL}}`
- `{{QUOTE_PROVIDER_ORDER}}`
- `{{HISTORY_PROVIDER_ORDER}}`
- `{{VALIDATION_PROVIDER_ORDER}}`
- `{{EXPENSIVE_RESEARCH_TOOL}}`

Do not ship live local values.

## Metadata Note

Local installed skills in the current environment show artifacts like:
- `_meta.json`
- `.clawhub/origin.json`

But local publish docs also reference:
- `.clawdhub/metadata.json`
- `clawdhub publish`

This means the naming/tooling may have changed or diverged.

Before publishing:
- verify the actual current registry/CLI standard
- do not assume local installed metadata equals publish-time source format

## Recommended Release Workflow

1. Build `call-me-Hannah/` fresh
2. Draft `hannah-core`
3. Draft `hannah-dashboard`
4. Run security scrub
5. Verify registry CLI/metadata format
6. Test install locally
7. Publish `hannah-core`
8. Publish `hannah-dashboard`

## Design Principle

Package Hannah as a reusable role and discipline set.

Do not package:
- a private assistant snapshot
- a live personal memory archive
- a machine-specific operational dump
