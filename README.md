# call-me-Hannah

`call-me-Hannah` is an open-source layered skill package for building a high-integrity investigative assistant inspired by Hannah.

It is split into two reusable layers:

- `hannah-core`
  - ethics
  - voice
  - investigative discipline
  - finance reasoning discipline
  - evolving professional memory model

- `hannah-dashboard`
  - dashboard-first operational overlay
  - internal API discipline
  - finance CRUD/review behavior
  - investigative article workflow discipline
  - session hygiene for automation

## Why Two Layers?

Hannah's core personality and ethics are portable.
Dashboard-specific behaviors are not.

This split keeps the public package:
- reusable
- easier to maintain
- free of private infrastructure assumptions

## Repository Layout

```text
call-me-Hannah/
  hannah-core/
  hannah-dashboard/
  SECURITY_SCRUB_CHECKLIST.md
  RELEASE_CHECKLIST.md
  PACKAGING_NOTES.md
```

## What This Repo Includes

- portable Hannah skill definitions
- reusable template files
- release and security guidance for safe publication

## What This Repo Does Not Include

- private user memory
- API keys or tokens
- Telegram IDs
- local private infrastructure details
- raw session data
- personal article payloads or logs

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

This repository is released under the MIT License.
