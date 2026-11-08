# Contributing to TinkeringDao Repositories

## Workflow Standards

1. **Branch-Per-Change:** Never commit directly to `main`. Create a focused topic branch (`feat/<scope>`, `fix/<scope>`, `refactor/<scope>`, `docs/<scope>`).
2. **Atomic Commits:** Each commit must represent a single logical change that compiles cleanly and passes tests independently. Use imperative commit subjects (`fix(rfcomm): validate packet length before buffer copy`).
3. **CI Green Before Merge:** All configured GitHub Actions checks, linters, compilers (`-Wall -Wextra -Werror` where applicable), and test suites must pass before merge. Stale review approvals are dismissed automatically on push.
4. **Thread Resolution:** All review threads must be resolved prior to merging.

## Pull Request Structure

Every Pull Request must follow [`.github/PULL_REQUEST_TEMPLATE.md`](./.github/PULL_REQUEST_TEMPLATE.md):

- **Summary:** Concise architecture diff sketch, call tree, or Mermaid sequence diagram illustrating the structural change.
- **Evidence:** Deterministic **Before** and **After** verification output (test runner transcripts, binary CLI output, packet traces, or UI screenshots).
- **Merge Danger:** Explicit classification as a **One-Way Door** (irreversible NVRAM write, schema migration, breaking wire protocol change) or **Two-Way Door** (easily revertible code change), accompanied by a blast-radius summary.

## Issue Triage Lifecycle

New issues enter with the `needs-triage` label and progress through five canonical states defined in [`docs/agents/triage-labels.md`](./docs/agents/triage-labels.md):

- `needs-triage`: Awaiting maintainer evaluation.
- `needs-info`: Blocked on reproduction details or hardware logs from the reporter.
- `ready-for-agent`: Fully specified and scoped for autonomous agent execution.
- `ready-for-human`: Requires human architectural judgment or physical hardware-in-the-loop verification.
- `wontfix`: Out of scope or declined.
