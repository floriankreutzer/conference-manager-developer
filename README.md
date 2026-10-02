# Conference Manager Developer

## SaaS 3.9 publication governance

SaaS 3.9 formalizes this repository as the intentionally public Developer Portal while the trusted backend and canonical API-contract source remain private. Public artifacts must be approved, source-traceable and fail-closed against accidental private-content publication. See `docs/PUBLICATION-GOVERNANCE.md`.

Public documentation for integrating with released Conference Manager partner APIs.

> **Status:** No production Caterer API is published yet.

## Public scope

This repository intentionally contains only information an external integrator needs to implement and operate an approved integration:

- released API specifications;
- authentication and onboarding instructions;
- request/response and lifecycle guidance required to use the API correctly;
- synthetic examples;
- version, compatibility, deprecation, and public changelog information;
- integration-specific security requirements.

It intentionally excludes internal architecture, provider research, product roadmaps, internal release gates, customer/Tenant information, operational topology, internal controls, and implementation details that are not required by an external integrator.

## Contract authority

The trusted backend owns the canonical source API contract. This repository publishes approved release artifacts. Published OpenAPI files are not independently edited API authority.

No placeholder OpenAPI specification is published before an API contract is approved.

## Public access

Documentation is readable without login. API access requires separately provisioned credentials and authorization. No credentials, customer data, production payloads, or internal-only information belong in this repository.

## Planned structure

```text
docs/
  getting-started/
  authentication/
  catering/v1/
  security/
  versioning/
openapi/
  catering/v1/
examples/
CHANGELOG.md
```
