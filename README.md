# Conference Manager Developer

Public developer documentation for Conference Manager partner integrations.

> **Status:** Foundation prepared for SaaS 4. No production Caterer API is published yet. Do not build against planned or placeholder contracts.

## Documentation model

- **`conference-manager-api`** owns the trusted backend implementation and canonical source OpenAPI contract.
- **This repository** publishes approved, release-bound OpenAPI artifacts and public developer guides, examples, changelogs, and onboarding documentation.
- **Confluence** records internal architecture, governance, provider capability decisions, and acceptance evidence.

Published OpenAPI artifacts here are generated or release-published from the approved backend contract. They are not independently edited API authority.

## Planned SaaS 4 Caterer API

The public Caterer API will use a provider-neutral contract. Caterers and integration partners will retrieve authorized released orders and approved change/cancellation requests and submit supported catalogue, availability, confirmation/status, substitution, and exception-quote information.

Key decisions already established:

- the canonical Conference Manager business catalogue remains authoritative for Employee presentation;
- provider catalogues are imported/synchronized and linked to canonical catalogue entries;
- provider cost and Conference Manager price are distinct values;
- multiple caterers, including multiple providers in the same category, are supported;
- each provider has a separate order/version/status lifecycle;
- transport/API success is not business confirmation;
- partial confirmation is supported;
- substitutions require Conference Manager review and a new order version;
- changes and cancellations require Conference Manager review;
- extra provider costs require renewed Conference Manager approval;
- the previously confirmed provider state remains effective until replacement/change/cancellation is confirmed;
- hybrid integrations are allowed per capability;
- the generic partner API is pull-first, with optional signed notification webhooks;
- provider outages may be reconciled later; conflicts require Conference Manager action.

## Planned public structure

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
  curl/
  javascript/
  python/
CHANGELOG.md
```

The `openapi/catering/v1/openapi.yaml` path will be populated only from an approved backend contract. It is intentionally absent until that contract exists.

## Public access and credentials

Documentation is intended to be readable without login. API access will require separately provisioned credentials scoped to authorized Tenant/provider connections. No credentials, customer data, or production secrets belong here.

## Versioning and publication

A published API release must identify its API contract version, source backend commit/release, publication date, compatibility or migration notes, applicable authentication/scopes, tested examples, and known limitations. Breaking changes require an explicit version and migration/deprecation policy.

## Current roadmap

SaaS 4 architecture and the canonical Caterer API contract remain subject to the existing Conference Manager roadmap and release gates. This repository can prepare documentation infrastructure now, but it does not make blocked backend implementation production-ready.
