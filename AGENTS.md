# AGENTS.md

Context pointers for agents operating in the `TinkeringDao/.github` organization-wide governance, legal baseline, and reusable CI workflow repository.

- **Organization-wide legal & clean-room hardware interoperability baseline**: read [`LEGAL.md`](LEGAL.md) (including the `Addendum: German Statutory References (Applicable to Residents of Germany)`).
- **Coordinated vulnerability disclosure & hardware security boundaries**: read [`SECURITY.md`](SECURITY.md).
- **Contributor workflow, PR structure, and issue triage lifecycle**: read [`CONTRIBUTING.md`](CONTRIBUTING.md) and [`.github/PULL_REQUEST_TEMPLATE.md`](.github/PULL_REQUEST_TEMPLATE.md).
- **Reusable GitHub Actions CI & Autonomous PR Review workflows**: inspect [`.github/workflows/autonomous-pr-review.yml`](.github/workflows/autonomous-pr-review.yml), [`.github/workflows/reusable-autonomous-pr-review.yml`](.github/workflows/reusable-autonomous-pr-review.yml), [`.github/workflows/reusable-ci-python.yml`](.github/workflows/reusable-ci-python.yml), and [`.github/workflows/reusable-ci-node.yml`](.github/workflows/reusable-ci-node.yml).

## Fully Autonomous Development Pipeline

All autonomous agent contributions, pull request reviews, remediations, and merges in this repository are governed by the 6-stage specification in [`docs/agents/autonomous-pipeline.md`](docs/agents/autonomous-pipeline.md) and enforced on every Pull Request by [`.github/workflows/autonomous-pr-review.yml`](.github/workflows/autonomous-pr-review.yml) (and exported org-wide via [`.github/workflows/reusable-autonomous-pr-review.yml`](.github/workflows/reusable-autonomous-pr-review.yml)).

### Project Verification Commands

Run these verification checks locally before pushing any commit:

```bash
test -s LEGAL.md && grep -q "Addendum: German Statutory References" LEGAL.md
test -s AGENTS.md && test -s CLAUDE.md && test -s docs/agents/autonomous-pipeline.md
python3 -c 'import yaml, glob; [yaml.safe_load(open(f)) for f in glob.glob(".github/workflows/*.yml")]'
```

### Verification Checklist & Pre-Merge Gate Commands

| Gate | Requirement | Local Pre-Merge Command |
| :--- | :--- | :--- |
| **Gate 1: OPSEC & Zero-PII** | Zero personal identifiers, local usernames, postal codes, or coordinates in repo tree | `grep -rnI -iE "<FORBIDDEN_PII_PATTERN>" . --exclude-dir=.git --exclude="*autonomous-pr-review.yml"` (see workflow) |
| **Gate 2: Cryptographic Signatures** | Every commit signed with `ED25519` SSH key (`verified == true`) | `git log -1 --show-signature` |
| **Gate 3: Legal & Autonomous Spec** | `LEGAL.md` (with German Statutory Addendum), `LICENSE`, `SECURITY.md`, `CODE_OF_CONDUCT.md`, `CODEOWNERS`, `AGENTS.md`, `CLAUDE.md`, `docs/agents/autonomous-pipeline.md` present | `grep -q "Addendum: German Statutory References" LEGAL.md && test -s docs/agents/autonomous-pipeline.md` |
| **Gate 4: Workflow & Syntax** | All GitHub Actions reusable and standalone workflows parse cleanly | `python3 -c 'import yaml, glob; [yaml.safe_load(open(f)) for f in glob.glob(".github/workflows/*.yml")]'` |

## Agent skills

### Issue tracker

Issues and specs for this repo live in GitHub Issues. See [`docs/agents/issue-tracker.md`](docs/agents/issue-tracker.md).

### Triage labels

Uses the five default canonical triage labels (`needs-triage`, `needs-info`, `ready-for-agent`, `ready-for-human`, `wontfix`). See [`docs/agents/triage-labels.md`](docs/agents/triage-labels.md).

### Domain docs

Single-context (`GLOSSARY.md` + `docs/adr/` at the repo root). See [`docs/agents/domain.md`](docs/agents/domain.md).
