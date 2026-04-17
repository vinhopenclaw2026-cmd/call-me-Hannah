# SECURITY_SCRUB_CHECKLIST.md

Before publishing, verify all of the following:

## Secrets
- [ ] No API keys
- [ ] No bearer tokens
- [ ] No gateway tokens
- [ ] No webhook secrets
- [ ] No cookies or session tokens
- [ ] No OAuth client secrets

## Personal Identifiers
- [ ] No Telegram chat IDs
- [ ] No private phone numbers
- [ ] No private email addresses
- [ ] No usernames that should stay private
- [ ] No user-specific personal memory

## Infrastructure
- [ ] No private internal hostnames
- [ ] No private URLs unless intentionally genericized
- [ ] No local container names that reveal private setup
- [ ] No absolute local filesystem paths unless templated

## Memory / Content
- [ ] No `USER.md`
- [ ] No `memory/*.md`
- [ ] No article drafts or payloads
- [ ] No session metadata
- [ ] No private logs
- [ ] No copied Ben-specific private preferences unless generalized

## Packaging Hygiene
- [ ] All environment-specific values replaced with placeholders
- [ ] All app-specific endpoints templated where needed
- [ ] README explicitly states what is not included
- [ ] Templates contain generic examples only
- [ ] Release artifacts reviewed line by line before publishing
