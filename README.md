# TinkeringDao/.github

[![License: MIT](https://img.shields.io/badge/License-MIT-blue.svg)](LICENSE)

> [!IMPORTANT]
> **Account-Wide Legal, Interoperability, EU CRA/PLD Non-Commercial & RF Regulatory Notice**
> All repositories published under [`TinkeringDao`](https://github.com/TinkeringDao) are independent, non-commercial free and open-source projects governed by [`LEGAL.md`](LEGAL.md):
> 1. **Indication of Intended Purpose & Nominative Fair Use:** `Article 14(1)(c) of Regulation (EU) 2017/1001 (EUTMR)`, CJEU *C-228/03 Gillette*, `15 U.S.C. §§ 1115(b)(4), 1125` — no vendor affiliation or endorsement.
> 2. **Statutory Interoperability & Clean-Room Safe Harbor:** `Directive 2009/24/EC (Articles 1(2), 5(3), 6, 8)`, CJEU *C-406/10 SAS Institute*, `Article 3(1)(b) of Directive (EU) 2016/943`, `17 U.S.C. §§ 102(b), 107, 1201(f)`, `18 U.S.C. § 1839(6)(B) (Defend Trade Secrets Act)`.
> 3. **Non-Circumvention of TPMs:** `Directive 2009/24/EC`, `17 U.S.C. §§ 1201(a), 1201(f)` — zero cryptographic keys or secure-boot bypasses.
> 4. **Zero Proprietary Code or OEM Binaries:** 100% original or licensed open-source code (`SPDX-License-Identifier: MIT`); zero OEM firmware binaries or verbatim hex slices (`<REDACTED_OEM_BYTES>`).
> 5. **Authorized Local Owner Execution Only:** `18 U.S.C. § 1030 (CFAA)`.
> 6. **EU CRA & PLD Non-Commercial FOSS Exemption:** `Regulation (EU) 2024/2847` (Recitals 15 & 18, `Art. 2(5)`) and `Directive (EU) 2024/2853` (`Art. 2(2)`).
> 7. **Radio Frequency (RF) Compliance:** `Directive 2014/53/EU (RED)`, `ETSI EN 300 220` / `ETSI EN 300 328`, `ERC/REC 70-03`, `Decision (EU) 2017/1483`, `FCC 47 C.F.R. Part 15 / Part 97`.
> 8. **AS IS Warranty Disclaimer:** Provided `"AS IS"` without warranty of any kind.

Account-wide community health standards, legal & regulatory compliance policies, and SHA-pinned reusable CI and security workflows for [`TinkeringDao`](https://github.com/TinkeringDao) repositories.

## Contents

| Path | Purpose |
| :--- | :--- |
| [`LEGAL.md`](./LEGAL.md) | Account-wide 8-pillar legal, interoperability (`Directive 2009/24/EC`, `Article 3(1)(b) of Directive (EU) 2016/943`, `Article 14(1)(c) of Regulation (EU) 2017/1001 (EUTMR)`, `15 U.S.C. §§ 1115(b)(4), 1125`, `17 U.S.C. §§ 102(b), 107, 1201(a), 1201(f)`, `18 U.S.C. §§ 1839(6)(B), 1030`), EU CRA (`2024/2847`), EU PLD (`2024/2853`), and RF (`Directive 2014/53/EU (RED)` / `ETSI EN 300 220` / `ETSI EN 300 328` / `FCC 47 C.F.R. Part 15 / Part 97`) policy |
| [`LICENSE`](./LICENSE) | MIT License (`Copyright (c) 2026 TinkeringDao`) |
| [`CODE_OF_CONDUCT.md`](./CODE_OF_CONDUCT.md) | Contributor Covenant 2.1 Code of Conduct (`@TinkeringDao`) |
| [`SECURITY.md`](./SECURITY.md) | Default vulnerability disclosure policy (`main` branch support, GitHub Security Advisories, safe-harbor research boundaries) |
| [`CONTRIBUTING.md`](./CONTRIBUTING.md) | Contribution standards (clean-room compliance, signed atomic commits, green CI and security checks, squash-merge workflow) |
| [`.github/PULL_REQUEST_TEMPLATE.md`](./.github/PULL_REQUEST_TEMPLATE.md) | Pull request template (Summary and Verification checklist) |
| [`.github/ISSUE_TEMPLATE/bug_report.yml`](./.github/ISSUE_TEMPLATE/bug_report.yml) | YAML bug report form (`needs-triage` auto-labeling) |
| [`.github/ISSUE_TEMPLATE/feature_request.yml`](./.github/ISSUE_TEMPLATE/feature_request.yml) | YAML feature request form (`needs-triage` auto-labeling) |
| [`.github/workflows/reusable-ci-python.yml`](./.github/workflows/reusable-ci-python.yml) | Hardened `workflow_call` Python lint/test pipeline (SHA-pinned actions, read-only token) |
| [`.github/workflows/reusable-ci-node.yml`](./.github/workflows/reusable-ci-node.yml) | Hardened `workflow_call` Node.js lint/typecheck/test pipeline (SHA-pinned actions, read-only token) |
| [`.github/workflows/reusable-security.yml`](./.github/workflows/reusable-security.yml) | Hardened `workflow_call` secret-scanning, signature-verification, governance, and workflow security pipeline |

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

### Security Gate

```yaml
jobs:
  security:
    uses: TinkeringDao/.github/.github/workflows/reusable-security.yml@main
    secrets:
      OPSEC_BLOCKLIST_REGEX: ${{ secrets.OPSEC_BLOCKLIST_REGEX }}
```
