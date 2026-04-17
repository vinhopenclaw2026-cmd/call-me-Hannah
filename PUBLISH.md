# PUBLISH.md

## Purpose

This file records the exact ClawHub publish flow for `call-me-Hannah`.

The package is split into two skills:
- `hannah-core`
- `hannah-dashboard`

## Preconditions

Before publishing, confirm all of the following:

1. You are logged into ClawHub:
   ```bash
   clawhub whoami
   ```

2. The repository is clean:
   ```bash
   git status --short
   ```

3. The package has already been reviewed with:
   - `SECURITY_SCRUB_CHECKLIST.md`
   - `RELEASE_CHECKLIST.md`

4. The GitHub repository is public and available at:
   - `https://github.com/vinhopenclaw2026-cmd/call-me-Hannah`

## Important CLI Notes

### Current CLI

The active CLI is:
- `clawhub`

### Version Flag Required

This CLI requires an explicit semantic version on publish.

Use:
- `--version 0.1.0`

### Path Format

The CLI accepted absolute folder paths reliably during testing.

## Publish Commands

From the repo root:

```bash
cd /path/to/call-me-Hannah
```

### Publish `hannah-core`

```bash
clawhub publish \
  "$(pwd)/hannah-core" \
  --slug hannah-core \
  --version 0.1.0 \
  --tags latest \
  --changelog "Initial public release"
```

### Publish `hannah-dashboard`

```bash
clawhub publish \
  "$(pwd)/hannah-dashboard" \
  --slug hannah-dashboard \
  --version 0.1.0 \
  --tags latest \
  --changelog "Initial public release"
```

## Verification

After publishing, verify:

```bash
clawhub search hannah-core
clawhub search hannah-dashboard
```

Optional:

```bash
clawhub inspect hannah-core
clawhub inspect hannah-dashboard
```

## Current Blocker Observed

Publishing was attempted successfully up to the registry policy checks, but blocked by this platform requirement:

> GitHub account must be at least 14 days old to publish skills or post comments.

That means:
- package structure is acceptable
- auth is working
- slug names are available
- commands are correct
- only the account-age rule is preventing publication right now

## When The Account Is Old Enough

Re-run the exact commands above.

No additional package restructuring should be necessary unless ClawHub changes its requirements.

## Troubleshooting

### If you see `Path must be a folder`
- use the absolute folder path shown above

### If you see `--version must be valid semver`
- pass `--version 0.1.0`

### If you see `Skill not found` on `inspect`
- that usually means the slug is still available and not yet published

### If you see a GitHub API rate-limit error
- wait briefly and retry

### If you still cannot publish after 14 days
- re-run:
  ```bash
  clawhub whoami
  clawhub publish --help
  ```
- then inspect any new error message directly
