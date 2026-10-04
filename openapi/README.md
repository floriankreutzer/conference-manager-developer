# Published OpenAPI Artifacts

This directory contains public, release-bound copies of approved Conference Manager OpenAPI contracts.

## Source of truth

The canonical source contract and implementation live in the private trusted backend repository `floriankreutzer/conference-manager-api`.

Published specifications here must:

1. come from an approved backend commit/release;
2. record their source commit/release and contract version;
3. pass publication validation and drift checks;
4. never be manually changed to create a contract the backend does not implement.

The planned Caterer API artifact will be published under `catering/v1/openapi.yaml` after the corresponding backend contract and public release are approved. No placeholder API specification is committed here.
