# TinkeringDao/.github

Account-wide community health standards, reusable CI workflows, and autonomous agent configuration templates for [`TinkeringDao`](https://github.com/TinkeringDao) repositories.

## Contents

| Path | Purpose |
| :--- | :--- |
| [`SECURITY.md`](./SECURITY.md) | Default vulnerability disclosure policy (`main` branch support, GitHub Security Advisories) |
| [`CONTRIBUTING.md`](./CONTRIBUTING.md) | Contribution standards (atomic commits, branch-per-change, green CI, structured PRs) |
| [`.github/PULL_REQUEST_TEMPLATE.md`](./.github/PULL_REQUEST_TEMPLATE.md) | Structured `/pr` template (Summary, Before/After Evidence, One-Way vs Two-Way Door classification) |
| [`.github/ISSUE_TEMPLATE/bug_report.yml`](./.github/ISSUE_TEMPLATE/bug_report.yml) | YAML bug report form (`needs-triage` auto-labeling) |
| [`.github/ISSUE_TEMPLATE/feature_request.yml`](./.github/ISSUE_TEMPLATE/feature_request.yml) | YAML feature request form (`needs-triage` auto-labeling) |
| [`.github/workflows/reusable-ci-python.yml`](./.github/workflows/reusable-ci-python.yml) | Hardened `workflow_call` Python lint/test pipeline (SHA-pinned actions, read-only token) |
| [`.github/workflows/reusable-ci-node.yml`](./.github/workflows/reusable-ci-node.yml) | Hardened `workflow_call` Node.js lint/typecheck/test pipeline (SHA-pinned actions, read-only token) |
| [`docs/agents/issue-tracker.md`](./docs/agents/issue-tracker.md) | Matt Pocock `/triage`, `/to-tickets`, and `/wayfinder` GitHub issue tracker specification |
| [`docs/agents/triage-labels.md`](./docs/agents/triage-labels.md) | Canonical 5-role triage label vocabulary (`needs-triage`, `needs-info`, `ready-for-agent`, `ready-for-human`, `wontfix`) |
| [`docs/agents/domain.md`](./docs/agents/domain.md) | Domain glossary (`GLOSSARY.md`) and ADR (`docs/adr/`) consumption rules |

## Reusable Workflow Usage

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
