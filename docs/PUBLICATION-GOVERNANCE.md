# Public Developer Documentation Governance

## Purpose

This public repository is the approved external integration-documentation surface for Conference Manager. SaaS 3.9 formalizes this boundary; it does not make this repository an authority for backend implementation.

## Source of truth

`conference-manager-api` is private and owns canonical API contracts. Released public specifications in this repository are derived publication artifacts and must be traceable to an immutable backend source commit.

Do not independently edit a published OpenAPI contract in a way that creates a second source of truth.

## Allowed public content

- released external API specifications;
- authentication and onboarding guidance required by integrators;
- public request/response and lifecycle semantics;
- webhooks where released;
- versioning, compatibility, deprecation and changelog information;
- synthetic examples;
- integration-specific security requirements external consumers must follow.

## Prohibited content

- credentials, tokens, secrets or private keys;
- customer/Tenant information or production payloads;
- internal/private endpoints or schemas;
- backend implementation source;
- internal architecture or operational topology not required by integrators;
- internal runbooks, release gates and incident/security findings;
- provider research and commercial evaluation;
- product roadmap material not explicitly approved for publication.

## Publication controls

SaaS 3.9 #250 must provide a deterministic, fail-closed publication mechanism. Public artifacts must be allowlisted, validated, secret-scanned, versioned and source-traceable. Sanitization or validation failure must stop publication rather than publish a partial or broader contract.

Examples must use synthetic data only.

## SaaS 4 relationship

SaaS 4 #236 defines the generic Caterer API. SaaS 4 #237 owns complete external documentation for that API. This repository publishes those artifacts only after the owning functional/release gates approve them.

No placeholder production API is to be published merely to exercise the publication pipeline.
