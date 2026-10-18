# Conference Manager Developer

Public documentation for approved Conference Manager partner integrations.

**Current status:** No production Caterer API contract is published in this repository. Do not infer API availability from the documentation structure.

## Contents

- Public integration guides in [`docs/`](docs/README.md).
- Approved API specifications in [`openapi/`](openapi/README.md), when released.
- Synthetic examples in [`examples/`](examples/README.md).
- Public version and compatibility information in [CHANGELOG.md](CHANGELOG.md).

Published specifications must identify their approved source commit and contract version. This repository distributes approved contracts; it does not independently define backend behavior.

## Read the documentation

The static documentation entry point is `index.html`. You can inspect it locally without application credentials:

```bash
git clone https://github.com/floriankreutzer/conference-manager-developer.git
cd conference-manager-developer
python3 -m http.server 8080 --bind 127.0.0.1
```

Open `http://127.0.0.1:8080`. Python 3 is required only for this optional local server. No Node.js build is currently defined.

Reading documentation does not grant API access. Released APIs require separately provisioned credentials and authorization.

## Contributing and validation

Read [CONTRIBUTING.md](CONTRIBUTING.md) and [AGENTS.md](AGENTS.md) before contributing. Use synthetic examples and describe released behavior accurately.

The repository's `Public documentation safety` workflow checks repository history for secrets, prohibited private material, API publication provenance and local Markdown links. Changes must pass the applicable checks and review before publication.

## Security

Never publish credentials, real customer payloads or sensitive findings. Report suspected vulnerabilities privately using [SECURITY.md](SECURITY.md).

## License

No project-level license file is currently included. Refer to any corresponding third-party notices.
