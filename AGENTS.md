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

## Public-by-necessity rule

Before adding any information, apply this test: **does an external integrator need this information to implement, authenticate, validate, troubleshoot, migrate, or safely operate the documented public API?** If not, do not publish it here.

Do not publish internal architecture diagrams, provider/vendor discovery, roadmap or milestone details, internal issue numbers, internal release gates, internal role/governance discussions, infrastructure topology, database/storage design, internal monitoring/operations procedures, internal security-control implementation, vulnerability details, or repository-to-repository implementation notes unless a narrowly scoped part is strictly required for correct public API use.

Describe externally observable behavior and obligations, not internal implementation. Security documentation must tell integrators what they must do without exposing defensive internals that are unnecessary for integration.

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

## Cost-constrained execution

Work must remain within the owner's configured zero-additional-spend limits. Do not upgrade plans, increase paid quotas, change spending limits, or start billable runners or deployments without an explicit new owner decision. Prefer local validation, bundle related documentation changes, and avoid unnecessary workflow reruns and Hosted Demo traffic. Configured cost controls do not provide additional included capacity.

Required reviews, security checks, regression/progression tests and release gates remain mandatory. A local result does not substitute for a required GitHub status check. If a required gate is blocked by quota, record it as pending or unavailable and retain the open release/merge gate. Do not weaken protections, skip checks, or claim completion to work around cost limits. User-reported spending controls must be distinguished from independently verified provider settings.

## Documentation status integrity

Reconcile current documentation with the exact merged implementation and named deployment evidence. Distinguish current main, unmerged pull requests, deployed immutable counterparts, dated test evidence and planned behavior. Keep historical failures and accepted scope limits explicitly historical. A closed milestone does not prove every later change passed its own gates.
