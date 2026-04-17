# RELEASE_CHECKLIST.md

## Scope

This checklist is for packaging and releasing `call-me-Hannah` as open-source layered skills:

- `hannah-core`
- `hannah-dashboard`

## Required Files

### hannah-core
- [ ] `SKILL.md`
- [ ] `README.md`
- [ ] `LICENSE`
- [ ] `CHANGELOG.md`
- [ ] `templates/PRINCIPLES.template.md`
- [ ] `templates/SOUL.template.md`
- [ ] `templates/BEATBOOK.template.md`

### hannah-dashboard
- [ ] `SKILL.md`
- [ ] `README.md`
- [ ] `LICENSE`
- [ ] `CHANGELOG.md`
- [ ] `templates/DASHBOARD.template.md`
- [ ] `templates/FINANCE.template.md`
- [ ] `templates/TOOLS.template.md`
- [ ] `templates/SETTINGS.template.md`

### top-level
- [ ] `SECURITY_SCRUB_CHECKLIST.md`
- [ ] `RELEASE_CHECKLIST.md`
- [ ] `PACKAGING_NOTES.md`

## Content Review

- [ ] `hannah-core` contains only portable Hannah behavior
- [ ] `hannah-dashboard` contains only generic app-overlay behavior
- [ ] No private workspace memory was copied
- [ ] No live environment-specific values remain
- [ ] Placeholders are used wherever local customization is required

## Security Review

- [ ] No API keys
- [ ] No bearer tokens
- [ ] No gateway tokens
- [ ] No webhook secrets
- [ ] No Telegram chat IDs
- [ ] No private email addresses
- [ ] No local hostnames or private URLs unless genericized
- [ ] No raw session metadata
- [ ] No article payloads or internal logs
- [ ] No copied `USER.md`
- [ ] No copied `memory/*.md`

## Quality Review

- [ ] `SKILL.md` frontmatter is valid
- [ ] Version numbers are set
- [ ] Descriptions are clear and accurate
- [ ] READMEs explain purpose and limits clearly
- [ ] Templates are generic and reusable
- [ ] Changelog starts at `0.1.0`

## Licensing

- [ ] Choose and include a license
- [ ] Confirm all copied/adapted language is yours to publish
- [ ] Confirm no third-party proprietary content was included

## Publish Prep

- [ ] Verify actual registry/CLI name in current environment (`clawhub` vs `clawdhub`)
- [ ] Verify required publish metadata format
- [ ] Decide whether publish metadata is generated at release time or stored in repo
- [ ] Test local install before publishing

## Local Test Before Release

- [ ] Install `hannah-core` into a clean test workspace
- [ ] Install `hannah-dashboard` overlay on top
- [ ] Confirm files are readable and coherent
- [ ] Confirm no private/local assumptions remain
- [ ] Confirm templates are enough for customization

## Final Release Gate

- [ ] Security scrub passed
- [ ] README review passed
- [ ] Local install test passed
- [ ] Metadata format verified
- [ ] Ready to publish `hannah-core`
- [ ] Ready to publish `hannah-dashboard`
