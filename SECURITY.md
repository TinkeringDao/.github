# Security Policy

## Supported Versions

Security updates are applied to the latest state of the default branch (`main`) across active `TinkeringDao` software, firmware, and hardware tooling repositories.

| Branch / Version | Supported |
| :--- | :--- |
| `main` (HEAD) | Yes |
| Historical tags / feature branches | No |

## Reporting a Vulnerability

Do **not** open a public GitHub issue for suspected security vulnerabilities, RF/Bluetooth protocol exploit primitives, credential leaks, or memory corruption bugs.

1. **GitHub Security Advisories (Preferred):** Submit a report directly via the repository's **Security -> Report a vulnerability** tab (Private Vulnerability Reporting is enabled across `TinkeringDao` repositories).
2. **Direct Contact:** If advisory submission is unavailable, email [`acid9burn@gmail.com`](mailto:acid9burn@gmail.com) with the subject prefix `[SECURITY][<repo-name>]`.

### Required Report Details

- Affected repository, commit SHA, and build target / hardware revision (e.g., `ESP32-S3`, `QCC5181`, macOS architecture).
- Minimal deterministic reproduction steps, proof-of-concept payload, or packet capture trace.
- Assessment of impact, privilege boundary crossed, and blast radius.

## Disclosure Policy

Reports are triaged upon receipt. Once a fix is verified and merged to `main`, coordinated disclosure is published via a GitHub Security Advisory.
