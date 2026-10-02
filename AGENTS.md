# Repository-Wide Agent Instructions

These instructions are mandatory for every human contributor and AI coding agent working in `conference-manager-developer`.

## Purpose and authority

This public repository owns the externally readable Conference Manager developer documentation and published API artifacts. It is documentation and publication infrastructure only. It does not own runtime business rules, authorization, Tenant authority, provider credentials, or the canonical executable API contract.

For the Catering API and future public partner APIs:

- the trusted implementation and canonical source OpenAPI contract are owned by `floriankreutzer/conference-manager-api`;
- this repository publishes release-bound copies of approved OpenAPI artifacts plus public guides, examples, changelogs, and onboarding documentation;
- published OpenAPI files must not be edited manually to diverge from the approved backend contract;
- Confluence remains the internal architecture/governance/evidence record; this repository is the public developer surface.

## Mandatory workflow

Before modifying this repository:

1. Read this `AGENTS.md` completely.
2. Treat current `main` as the baseline.
3. Read the current version of every existing file before editing it.
4. Keep changes small, reviewable, and free of secrets or customer data.
5. Use a branch and pull request after repository initialization; do not bypass required checks or reviews.
6. Validate links, examples, schemas, generated/published OpenAPI provenance, and any site build before considering a change complete.
7. Add regression/progression checks appropriate to the change.

## Public-content security

Everything committed here must be safe for unrestricted public access.

Never commit:

- API keys, bearer tokens, passwords, private keys, cookies, CSRF/session material, connection strings, or secret references that reveal protected locations;
- real Tenant, customer, guest, attendee, employee, provider-order, booking, or confidential business data;
- internal-only hostnames, diagnostics, stack traces, provider credentials, security bypasses, reset/reseed authority, or operational details that materially weaken security.

Use synthetic examples only. Redact identifiers where necessary. Public examples must not imply that example credentials or endpoints are live.

## API documentation rules

- Public documentation must describe only released or explicitly marked preview contracts.
- The published OpenAPI artifact must identify its source backend release/commit and contract version.
- Endpoint, schema, error, authentication, idempotency, pagination, webhook, rate-limit, and lifecycle documentation must not contradict the published OpenAPI contract.
- Unsupported provider capabilities must never be presented as available.
- Transport success must not be described as business confirmation when the domain contract distinguishes them.
- Breaking changes require an explicit version/migration/deprecation decision and changelog entry.
- Examples must be executable against an approved synthetic/sandbox environment when such an environment exists.
- Authentication documentation may explain mechanisms and scopes but must never contain real credentials.

## Architecture boundary

This repository may contain:

- public developer guides;
- generated/static developer portal assets;
- published OpenAPI artifacts;
- synthetic examples and SDK usage examples;
- public changelog/versioning/security-contact guidance;
- documentation validation tooling and CI.

It must not contain:

- authoritative SaaS business logic;
- duplicated runtime authorization or validation logic;
- production secrets/configuration;
- customer application runtime code;
- a second manually maintained canonical API schema.

## Quality and security

Public documentation changes must consider:

- accidental secret/PII disclosure;
- unsafe copy/paste examples;
- misleading authentication or authorization guidance;
- broken links and stale version references;
- OpenAPI drift/provenance;
- dependency/supply-chain risk for documentation tooling;
- XSS/injection risks in generated documentation/site content;
- unsafe external scripts or third-party analytics.

Dependencies should be minimal, pinned, and justified. Secret scanning and dependency review should be enabled when tooling is introduced.

## Definition of Done

A change is complete only when its content is accurate for the named release, contains no sensitive data, preserves the source-of-truth boundary, passes applicable validation, and is merged through the repository's normal review process.
