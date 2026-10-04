# Conference Manager Developer

## Publication governance

This repository is the intentionally public Developer Portal. Approved artifacts must be source-traceable and validated before publication. See [publication governance](docs/PUBLICATION-GOVERNANCE.md).

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
