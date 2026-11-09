# Account-Wide Legal, Interoperability, & Regulatory Policy (`TinkeringDao`)

This document establishes the uniform 8-pillar legal, intellectual property, regulatory, and hardware safety policy governing all open-source software, firmware, and hardware interoperability repositories published under [`TinkeringDao`](https://github.com/TinkeringDao). Individual repositories may include a repository-specific `LEGAL.md` that supplements this baseline policy.

---

## 1. Independent Non-Commercial Open-Source Projects, Indication of Intended Purpose, & Nominative Fair Use

All repositories published under `TinkeringDao` are **independent, non-commercial, community-developed free and open-source projects** created solely to enable hardware interoperability, open-source firmware customization, and diagnostic telemetry on lawfully acquired consumer hardware.

- **No Affiliation or Endorsement:** `TinkeringDao` projects are **not affiliated with, authorized by, sponsored by, or endorsed by** any referenced third-party hardware or semiconductor manufacturer (including, without limitation, Bose Corporation, Qualcomm Incorporated, Analog Devices, Inc., Espressif Systems, Semtech Corporation, LilyGo, Heltec Automation, or Apple Inc.).
- **Indication of Intended Purpose & Nominative Fair Use:**
  - Pursuant to **Article 14(1)(c) of Regulation (EU) 2017/1001 (EU Trade Mark Regulation — EUTMR)**, settled Court of Justice of the European Union jurisprudence (*Case C-228/03 — Gillette v. LA-Laboratories*; *Case C-63/97 — BMW v. Deenik*), and **US Nominative Fair Use (`15 U.S.C. §§ 1115(b)(4), 1125`**, *New Kids on the Block v. News America Publishing, Inc.*, 971 F.2d 302 (9th Cir. 1992)), third-party product names, chip designations, and trademarks are referenced strictly as a necessary indication of intended purpose, nominative fair use, and target hardware compatibility of the software.
  - Zero corporate logos, proprietary icons, vendor mobile application screenshots, or proprietary trade dress are distributed in `TinkeringDao` repositories.

---

## 2. Statutory Software/Hardware Interoperability & Trade Secret Safe Harbor

All source code, register descriptions, and wire protocol documentation across `TinkeringDao` repositories are developed independently via clean-room observation, published datasheets, or licensed open-source upstream trees on lawfully acquired hardware owned by the operator:

### 2.1 European Union (`Directive 2009/24/EC` & `Directive (EU) 2016/943`)
1. **Exclusion of Functional Protocols & Interfaces from Copyright (`Article 1(2) of Directive 2009/24/EC`):**
   - Under `Article 1(2) of Directive 2009/24/EC` and settled CJEU precedent (*SAS Institute Inc. v. World Programming Ltd*, Case `C-406/10`, paras. 39–46), ideas, principles, functional interfaces, data formats, register layouts, and wire command protocols are **excluded from copyright protection**.
2. **Right to Observe, Study, and Test (`Article 5(3) of Directive 2009/24/EC`):**
   - Permits the lawful owner or user of a device or computer program to observe, study, and test its functioning without prior authorization in order to determine the underlying ideas, principles, and packet framing during normal use.
3. **Mandatory Right of Interoperability (`Article 6 of Directive 2009/24/EC`):**
   - Permits independent analysis necessary to achieve the **interoperability** of an independently created computer program with existing hardware and software where interface specifications were not previously published.
4. **Statutory Nullity of Contrary EULA Provisions (`Article 8 of Directive 2009/24/EC`):**
   - Under mandatory European Union law (`Article 8 of Directive 2009/24/EC`), any contractual or End-User License Agreement (EULA) clauses purporting to waive or restrict rights under `Article 5(3)` or `Article 6 of Directive 2009/24/EC` are **statutorily null and void**.
5. **Lawful Hardware Reverse Engineering (`Article 3(1)(b) of Directive (EU) 2016/943`):**
   - Under **Article 3(1)(b) of Directive (EU) 2016/943**, obtaining technical information by observing, studying, disassembling, or testing a product that has been made available to the public or that is lawfully in the possession of the acquirer of the information (who is free from any legally valid duty to limit the acquisition of the trade secret) is expressly declared a **lawful acquisition**.

### 2.2 United States (`17 U.S.C. §§ 102(b), 107, 1201(f)` & `18 U.S.C. § 1839(6)(B)`)
1. **Uncopyrightable Methods of Operation & Merger (`17 U.S.C. § 102(b)`):**
   - Numeric opcodes, command IDs, register offsets, and DSP filter coefficients constitute uncopyrightable systems, methods of operation, and functional facts necessary for hardware compatibility (*Baker v. Selden*, 101 U.S. 99 (1879); *Google LLC v. Oracle America, Inc.*, 593 U.S. 1 (2021); *Lexmark Int'l, Inc. v. Static Control Components, Inc.*, 387 F.3d 522 (6th Cir. 2004)).
2. **Interoperability Exemptions (`17 U.S.C. § 1201(f)`, `17 U.S.C. § 107`, & `37 C.F.R. § 201.40`):**
   - Developed exclusively for achieving interoperability of independently created computer programs with lawfully owned consumer hardware (*Sega Enterprises Ltd. v. Accolade, Inc.*, 977 F.2d 1510 (9th Cir. 1992); *Sony Computer Entertainment, Inc. v. Connectix Corp.*, 203 F.3d 596 (9th Cir. 2000); *The Chamberlain Group, Inc. v. Skylink Technologies, Inc.*, 381 F.3d 1178 (Fed. Cir. 2004)).
3. **Defend Trade Secrets Act Reverse-Engineering Safe Harbor (`18 U.S.C. § 1839(6)(B)`):**
   - Under the Defend Trade Secrets Act (`18 U.S.C. § 1839(6)(B)`), reverse engineering, independent derivation, and clean-room observation of a lawfully acquired product on the open market are explicitly excluded from the definition of "improper means".

---

## 3. Non-Circumvention of Technological Protection Measures (`Directive 2009/24/EC` & `17 U.S.C. §§ 1201(a), 1201(f)`)

Under **Directive 2009/24/EC (Articles 1(2), 5(3), 6, 8)** and **17 U.S.C. §§ 1201(a), 1201(f)**, `TinkeringDao` software **does not circumvent, bypass, decrypt, or defeat any Technological Protection Measure (TPM)**:

- **Zero Cryptographic Key Extraction or Secure-Boot Bypass:** `TinkeringDao` repositories contain **zero proprietary cryptographic keys, OEM private keys, seeds, nonces, certificates, or hardware secure-boot exploits**, and never decrypt or patch encrypted OEM firmware partitions.
- **Standard Interfaces & Open Developer Hardware:** Interoperability tools communicate exclusively over standard, unencrypted host interfaces (such as Bluetooth SPP/RFCOMM user-preference channels or USB CDC/UART developer interfaces) on hardware owned by the user.

---

## 4. Zero Proprietary Code, Verbatim Firmware Bytes, or Binary Distribution

- **100% Original or Properly Licensed Open-Source Code (`SPDX-License-Identifier: MIT`):** All source code in `TinkeringDao` repositories is either original clean-room code (`SPDX-License-Identifier: MIT`) or properly attributed open-source code distributed in full compliance with its respective open-source license (`MIT`, `LGPL-2.1`, etc.).
- **No OEM Binaries, Hex Slices, or Assets:** `TinkeringDao` repositories do **not** host, redistribute, or link to proprietary OEM firmware images (`.bin`, `.dfu`), commercial mobile application packages (`.ipa`, `.apk`), decompiled vendor source code, or verbatim proprietary firmware hex slices (`<REDACTED_OEM_BYTES>`).

---

## 5. Authorized Local Owner Execution Only (`18 U.S.C. § 1030` — CFAA)

In accordance with the **Computer Fraud and Abuse Act (`18 U.S.C. § 1030` — CFAA)** (*Van Buren v. United States*, 593 U.S. 374 (2021)):

- **No Access-Security Circumvention:** `TinkeringDao` software is neither designed nor adapted to bypass any authentication barrier or intercept non-public transmissions.
- **Authorized Local Owner Execution Only (`18 U.S.C. § 1030`):** All utilities and firmware builds are designed solely for local execution by the physical owner on their own lawfully acquired hardware. Zero manufacturer cloud servers or unauthorized remote endpoints are accessed. Executing `TinkeringDao` software against third-party devices without the explicit authorization of the hardware owner is strictly prohibited.

---

## 6. Non-Commercial Open-Source Software Exemption (EU CRA `Regulation (EU) 2024/2847` & EU PLD `Directive (EU) 2024/2853`)

- **EU Cyber Resilience Act Exemption (`Regulation (EU) 2024/2847`, Recitals 15 & 18; `Art. 2(5)`; `Art. 3(13)-(14)`):** All repositories under `TinkeringDao` are developed, maintained, and supplied strictly as **non-commercial free and open-source software outside the course of any commercial activity**. No fee is charged, no paid support or commercial services are offered, and no personal data is collected or monetized. Accordingly, the authors and contributors are neither "manufacturers" (`Art. 3(13)`) nor "open-source software stewards" (`Art. 3(14)`), and CE-marking (`Art. 28`) and commercial manufacturer obligations under Regulation (EU) 2024/2847 do not apply.
- **EU Product Liability Directive Exemption (`Directive (EU) 2024/2853`, `Art. 2(2)` & Recitals 14, 15, 24):** Pursuant to **Article 2(2)** and **Recitals 14, 15, and 24 of Directive (EU) 2024/2853**, strict product liability under this Directive does not apply to free and open-source software developed or supplied outside the course of a commercial activity. Any third party who integrates, bundles, compiles, or redistributes `TinkeringDao` software or firmware in the course of a commercial activity does so solely under their own legal and regulatory responsibility as a manufacturer.

---

## 7. Radio Frequency (RF) & Spectrum Regulatory Compliance (`Directive 2014/53/EU (RED)`, `ETSI EN 300 220` / `ETSI EN 300 328`, `ERC/REC 70-03`, `Decision (EU) 2017/1483`, `FCC 47 C.F.R. Part 15 / Part 97`)

- **Bluetooth / 2.4 GHz Peripherals (`Directive 2014/53/EU (RED)` / `ETSI EN 300 328` / `FCC 47 C.F.R. Part 15`):** Host-side Bluetooth utilities communicate solely via standard OS Bluetooth APIs and never alter certified baseband RF calibration tables, carrier frequencies, or EIRP limits.
- **Sub-GHz LoRa Mesh Firmware (`Directive 2014/53/EU (RED)`, `ETSI EN 300 220`, `ERC/REC 70-03`, `Decision (EU) 2017/1483`, `FCC 47 C.F.R. Part 15 / Part 97`):** Source-only firmware repositories for open developer transceiver boards (e.g., `ESP32-S3` + `SX1262`) require the physical operator to configure carrier frequency, bandwidth, radiated power (`ERP` / `EIRP`), and hourly duty cycle (`<= 1%` or `<= 10%` in EU SRD sub-bands under `ETSI EN 300 220`, `ERC/REC 70-03`, and `Decision (EU) 2017/1483`, or within US `902–928 MHz` ISM / amateur rules under `FCC 47 C.F.R. Part 15 / Part 97`) strictly in accordance with the laws of the jurisdiction in which the hardware is operated.

---

## 8. AS IS Warranty Disclaimer & Hardware Risk Notice

ALL SOFTWARE, FIRMWARE SOURCE CODE, AND DOCUMENTATION PUBLISHED UNDER `TinkeringDao` ARE PROVIDED **"AS IS"**, WITHOUT WARRANTY OF ANY KIND, EXPRESS OR IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF MERCHANTABILITY, FITNESS FOR A PARTICULAR PURPOSE, AND NONINFRINGEMENT. IN NO EVENT SHALL THE AUTHORS OR COPYRIGHT HOLDERS BE LIABLE FOR ANY CLAIM, DAMAGES, OR OTHER LIABILITY, WHETHER IN AN ACTION OF CONTRACT, TORT, OR OTHERWISE, ARISING FROM, OUT OF, OR IN CONNECTION WITH THE SOFTWARE OR THE USE OR OTHER DEALINGS IN THE SOFTWARE.

- **Operator's Sole Risk:** Compiling, flashing, or executing hardware interoperability tools or embedded firmware is performed entirely at the operator's own risk. The authors and contributors assume no liability for hardware malfunction, bricked devices, battery/thermal damage, regulatory non-compliance by the operator, or warranty disputes.

---

## Addendum: German Statutory References (Applicable to Residents of Germany)

Where German national law applies alongside European Union regulations and directives, the following national statutory provisions govern all `TinkeringDao` repositories:

- **Trademark Indication of Intended Purpose (`§ 23 Abs. 1 Nr. 3 MarkenG` — *Bestimmungsangabe*):** Section 23(1) No. 3 of the German Trademark Act (*Markengesetz*, implementing `Art. 14(1)(c) EUTMR`; BGH `I ZR 6/10`) permits referencing third-party trademarks, chip designations, and product names where necessary to indicate the intended purpose and target hardware compatibility of independent software.
- **Software Interoperability & Uncopyrightable Interfaces (`§§ 69a Abs. 2 & 5, 69d Abs. 3, 69e, 69f Abs. 2, 69g Abs. 2, 95a UrhG`):** Under the German Copyright Act (*Urheberrechtsgesetz*, implementing `Directive 2009/24/EC`):
  - `§ 69a Abs. 2 Satz 2 UrhG` excludes ideas, principles, and functional interfaces underlying a computer program from copyright protection.
  - `§ 69d Abs. 3 UrhG` entitles the lawful user to observe, study, or test the functioning of a program to determine its underlying ideas and principles.
  - `§ 69e UrhG` authorizes independent analysis necessary to achieve the interoperability of an independently created computer program.
  - `§ 69g Abs. 2 UrhG` renders any contractual or EULA clauses contrary to `§ 69d Abs. 2, 3` or `§ 69e UrhG` statutorily null and void (*nichtig*).
  - `§ 69a Abs. 5 UrhG` (*lex specialis*) excludes computer programs from general technological protection measure rules (`§ 95a UrhG`), and `TinkeringDao` software circumvents zero technical protection mechanisms (`§ 69f Abs. 2 UrhG`).
- **Reverse Engineering of Lawfully Acquired Hardware (`§ 3 Abs. 1 Nr. 2 lit. a & b GeschGehG`):** Section 3(1) No. 2 of the German Trade Secrets Act (*Geschäftsgeheimnisgesetz*, implementing `Article 3(1)(b) of Directive (EU) 2016/943`) expressly authorizes obtaining technical information by observing, examining, disassembling, or testing a product that has been made publicly available (`lit. a`) or is in the lawful possession of the observer (`lit. b`).
- **German IT Criminal Law & Property Ownership (`§§ 202a–202c, 303a StGB`, `§ 903 BGB`):** Under the German Criminal Code (*Strafgesetzbuch*, as interpreted by the Federal Constitutional Court, *BVerfG, 2 BvR 2233/07*) and Section 903 of the German Civil Code (*Bürgerliches Gesetzbuch*):
  - No access security mechanism (*Zugangssicherung*) is bypassed (`§§ 202a, 202c StGB`) and no non-public transmission is intercepted (`§ 202b StGB`).
  - All utilities and firmware builds operate exclusively on the physical owner's (`§ 903 BGB`) own local device data (*eigene Daten*, `§ 303a StGB`).
- **Radio Equipment & Spectrum Regulations (`FuAG`, `BNetzA Vfg 99/2022`, `AFuG` / `AFuV`):** Under the German Radio Equipment Act (*Funkanlagengesetz* — `FuAG`, implementing `Directive 2014/53/EU (RED)`), Federal Network Agency Short-Range Device general allocations (*Allgemeinzuteilungen*, including `BNetzA Vfg 99/2022` for 868 MHz SRD bands), and the Amateur Radio Act/Ordinance (`AFuG` / `AFuV`), operators of open developer transceiver boards are solely responsible for adhering to applicable frequency, ERP/EIRP, and duty-cycle limits.
- **Gratuitous Open-Source Liability Standard (`§§ 521, 523, 524, 599, 600 BGB`):** Because all `TinkeringDao` software, firmware source code, and documentation are provided gratuitously (*unentgeltlich*) outside the course of commercial activity, statutory liability under the German Civil Code (`§§ 521, 523, 524, 599, 600 BGB`) is limited strictly to intent (*Vorsatz*) and gross negligence (*grobe Fahrlässigkeit*).
