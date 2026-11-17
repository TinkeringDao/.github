# TinkeringDao/.github

[![License: MIT](https://img.shields.io/badge/License-MIT-blue.svg)](LICENSE)

Default community health documents, issue/PR templates, and SHA-pinned reusable GitHub Actions workflows shared across [`TinkeringDao`](https://github.com/TinkeringDao) repositories.

## Contents

| Path | Purpose |
| :--- | :--- |
| [`LEGAL.md`](LEGAL.md) | Account-wide statutory interoperability, trademark nominative fair use, non-commercial FOSS, and RF compliance notice |
| [`LICENSE`](LICENSE) | MIT License (`Copyright (c) 2026 TinkeringDao`) |
| [`CODE_OF_CONDUCT.md`](CODE_OF_CONDUCT.md) | Contributor Covenant 2.1 Code of Conduct |
| [`SECURITY.md`](SECURITY.md) | Default vulnerability reporting policy via GitHub Private Vulnerability Reporting |
| [`CONTRIBUTING.md`](CONTRIBUTING.md) | Contribution guidelines, signed commit requirements, and PR checks |
| [`.github/PULL_REQUEST_TEMPLATE.md`](.github/PULL_REQUEST_TEMPLATE.md) | Default pull request checklist |
| [`.github/ISSUE_TEMPLATE/`](.github/ISSUE_TEMPLATE) | YAML bug report and feature request forms |
| [`.github/workflows/reusable-ci-python.yml`](.github/workflows/reusable-ci-python.yml) | Reusable `workflow_call` Python lint and unit-test workflow |
| [`.github/workflows/reusable-ci-node.yml`](.github/workflows/reusable-ci-node.yml) | Reusable `workflow_call` Node.js lint, typecheck, and test workflow |
| [`.github/workflows/reusable-security.yml`](.github/workflows/reusable-security.yml) | Reusable `workflow_call` Gitleaks, key-hygiene, signature, governance, and `zizmor` workflow |

## Reusable Workflow Examples

### Python CI

```yaml
jobs:
  ci:
    uses: TinkeringDao/.github/.github/workflows/reusable-ci-python.yml@main
    with:
      python-version: "3.12"
```

### Node.js CI

```yaml
jobs:
  ci:
    uses: TinkeringDao/.github/.github/workflows/reusable-ci-node.yml@main
    with:
      node-version: "22"
```

### Security Gate

```yaml
jobs:
  security:
    uses: TinkeringDao/.github/.github/workflows/reusable-security.yml@main
```

## License & Legal

Released under the [MIT License](LICENSE). See [`LEGAL.md`](LEGAL.md) for account-wide legal, trademark, interoperability, and German statutory notices.
