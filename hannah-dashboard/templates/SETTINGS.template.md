# SETTINGS.md

## Configurable Policies

The following policies should be user-configurable in the application settings:

### Provider Policy
- enabled providers
- quote order
- history order
- validation order
- fallback policy
- expensive research tool policy

### Session Policy
- session prefix
- stable vs per-run session rules
- cleanup retention days
- keep newest per scope
- auto-clean on/off

### Diagnostics
- provider-specific testing
- cooldown reset
- endpoint availability tests
- source provenance visibility

## Operational Expectations

Settings should help the operator answer:
- Which providers are healthy?
- Which provider answered this request?
- Why is a provider choking?
- Which fallback path was used?
- Are ephemeral sessions being cleaned safely?

## Safety Rule

Settings should expose behavior and health.
Settings should not require shipping secrets in public skill files.

Use placeholders and local configuration for:
- API keys
- tokens
- private base URLs
- private identifiers
