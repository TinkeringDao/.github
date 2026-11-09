# Security Policy

## Supported Versions

Security updates are applied to the latest state of the default branch (`main`) across active [`TinkeringDao`](https://github.com/TinkeringDao) software, firmware, and hardware interoperability repositories.

| Branch / Version | Supported |
| :--- | :--- |
| `main` (HEAD) | Yes |
| Historical tags / feature branches | No |

## Reporting a Vulnerability

Do **not** open a public GitHub issue for suspected security vulnerabilities, RF/Bluetooth protocol exploit primitives, credential leaks, or memory corruption bugs.

1. **GitHub Security Advisories (Preferred):** Submit a report directly via the repository's **Security -> Report a vulnerability** tab (Private Vulnerability Reporting is enabled across `TinkeringDao` repositories).
2. **Maintainer Contact:** Reports are reviewed by `@TinkeringDao` via GitHub Security Advisories.

### Required Report Details

- Affected repository, commit SHA, and build target / hardware revision (e.g., `ESP32-S3`, `QCC5181`, macOS architecture).
- Minimal deterministic reproduction steps, proof-of-concept payload, or packet capture trace (with all personal MAC addresses, serial numbers, and OEM firmware bytes redacted).
- Assessment of impact, privilege boundary crossed, and blast radius.

## Legal & Safe-Harbor Boundaries

All security testing and protocol research must comply with [`LEGAL.md`](./LEGAL.md):

- Test exclusively on hardware that you personally own or are explicitly authorized to test (**Authorized Local Owner Execution Only**, `18 U.S.C. § 1030` — CFAA).
- Never include proprietary OEM firmware binaries, cryptographic keys, or verbatim OEM hex dumps in vulnerability reports or pull requests (`Directive 2009/24/EC (Articles 1(2), 5(3), 6, 8)`, `17 U.S.C. §§ 102(b), 107, 1201(a), 1201(f)`).

## Disclosure Policy

Reports are triaged upon receipt. Once a fix is verified and merged to `main`, coordinated disclosure is published via a GitHub Security Advisory.
