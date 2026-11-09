# Contributing to TinkeringDao Repositories

## Legal & Clean-Room Interoperability Standards

Before submitting an issue or Pull Request to any [`TinkeringDao`](https://github.com/TinkeringDao) repository, review [`LEGAL.md`](./LEGAL.md) and [`CODE_OF_CONDUCT.md`](./CODE_OF_CONDUCT.md):

1. **Zero Proprietary OEM Assets:** Never submit proprietary firmware binaries (`.bin`, `.dfu`), commercial mobile application packages (`.ipa`, `.apk`), decompiled vendor source code, cryptographic keys, or verbatim OEM firmware hex dumps.
2. **Clean-Room Interoperability Only:** All protocol descriptions and implementations must derive exclusively from clean-room black-box hardware observation (`Directive 2009/24/EC (Articles 1(2), 5(3), 6, 8)`, `Article 3(1)(b) of Directive (EU) 2016/943`, `17 U.S.C. §§ 102(b), 107, 1201(f)`, `18 U.S.C. § 1839(6)(B)`) or documented open-source upstream trees.
3. **Hardware Privacy:** Redact personal Bluetooth/Wi-Fi/LoRa MAC addresses, device serial numbers, and geographic coordinates from all logs and packet traces before submission.

## Workflow Standards

1. **Branch-Per-Change:** Never commit directly to `main`. Create a focused topic branch (`feat/<scope>`, `fix/<scope>`, `refactor/<scope>`, `docs/<scope>`).
2. **Atomic Commits:** Each commit must represent a single logical change that compiles cleanly and passes tests independently. Use imperative commit subjects (`fix(rfcomm): validate packet length before buffer copy`).
3. **CI Green Before Merge:** All configured GitHub Actions checks, linters, compilers (`-Wall -Wextra -Werror` where applicable), and test suites must pass before merge. Stale review approvals are dismissed automatically on push.
4. **Thread Resolution:** All review threads must be resolved prior to merging (`@TinkeringDao`).

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
