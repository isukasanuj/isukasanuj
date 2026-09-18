<div align="center">

<img src="https://media1.tenor.com/m/2EwShyE5d0oAAAAd/capybara-smile-funny-bara.gif" alt="Smiling capybara" width="240" height="240" />

# `isuk4`

**Penetration Tester · Computer enthusiastic · Exploit developer**

<img src="https://readme-typing-svg.demolab.com?font=Fira+Code&weight=600&size=18&pause=1200&color=00E5A0&center=true&vCenter=true&width=620&lines=break_things()+-%3E+understand()+-%3E+repeat();I+like+to+take+things+apart.;" alt="Typing SVG" />

<br />

[![GitHub](https://img.shields.io/badge/GitHub-isukasanuj-00E5A0?style=for-the-badge&logo=github&logoColor=white&labelColor=0d1117)](https://github.com/isukasanuj)
[![CVEs](https://img.shields.io/badge/Published_CVEs-4-00E5A0?style=for-the-badge&logo=common-workflow-language&logoColor=white&labelColor=0d1117)](#-published-findings)

</div>

<br />

## `> whoami`

```text
Cybersecurity researcher focused on finding — and understanding — the way things break.
I work across web application logic, Active Directory attack paths, and native-code
internals, and I enjoy the full loop: root-cause analysis, writing a working PoC,
and disclosing responsibly.
```

<br />

## `> focus`

- **Web application security** — authorization and business-logic flaws
- **Active Directory** — attack-path assessment
- **Native code** — reverse engineering and exploit development

<br />

## `> published-findings`

| # | CVE | Target | Class | Impact |
| :-: | :-- | :-- | :-- | :-- |
| 01 | [CVE-2026-85769](https://github.com/isukasanuj/CVE-2026-85769) | libtpms | Heap OOB Read | DoS — emulated-TPM crash (C:N confirmed) |
| 02 | [CVE-2026-79411](https://github.com/isukasanuj/bagisto-cve/blob/main/CVE-2026-79411.md) | Bagisto 2.4.9 | Privilege Escalation | Low-priv user → Administrator |
| 03 | [CVE-2026-79410](https://github.com/isukasanuj/bagisto-cve/blob/main/CVE-2026-79410.md) | Bagisto 2.4.9 | Business Logic | Order total forced below real price |
| 04 | [CVE-2026-79409](https://github.com/isukasanuj/bagisto-cve/blob/main/CVE-2026-79409.md) | Bagisto 2.4.9 | Info Disclosure (IDOR) | Sensitive data exposed to authed user |

<details>
<summary><b>Read the details</b></summary>

<br />

### 01 — [CVE-2026-85769](https://github.com/isukasanuj/CVE-2026-85769) · libtpms · Heap Out-of-Bounds Read
A heap out-of-bounds read in **libtpms** during TPM 2.0 state deserialization. The affected component powers `swtpm` / QEMU software-TPM deployments, placing the bug in an emulated-TPM path used across virtualization stacks. Exploitation results in DoS only — no information disclosure or code execution confirmed.
`root-cause analysis` · `proof of concept` · `TPM 2.0`

### 02 — [CVE-2026-79411](https://github.com/isukasanuj/bagisto-cve/blob/main/CVE-2026-79411.md) · Webkul Bagisto 2.4.9 · Privilege Escalation
A backend user holding only `settings.users.edit` can assign themselves the Administrator role through the user-management update path and gain full admin-panel access.
`authorization` · `role escalation` · `admin panel`

### 03 — [CVE-2026-79410](https://github.com/isukasanuj/bagisto-cve/blob/main/CVE-2026-79410.md) · Webkul Bagisto 2.4.9 · Price Manipulation
Improper validation of the add-to-cart `quantity` parameter lets an authenticated user reduce an order total below the legitimate price of shippable goods.
`input validation` · `business logic` · `e-commerce`

### 04 — [CVE-2026-79409](https://github.com/isukasanuj/bagisto-cve/blob/main/CVE-2026-79409.md) · Webkul Bagisto 2.4.9 · Information Disclosure
An authorization flaw in the add-to-cart API and downloadable-product fulfilment flow can expose sensitive information to an authenticated user.
`IDOR` · `authorization` · `information disclosure`

</details>

<br />

## `> acknowledgements`

> 🏆 Credited by **GIGABYTE Product Security** for a responsibly disclosed vulnerability.

> 🏆 Credited by **Red Hat Product Security** for responsibly disclosing [CVE-2026-85769](https://access.redhat.com/security/cve/cve-2026-85769) — heap out-of-bounds read in libtpms (swtpm / QEMU vTPM path).

> 🏆 Credited by **WP Recipe Maker** (wordpress.org) in the 10.8.2 changelog for responsibly disclosing an unauthenticated notice-dismissal vulnerability.

<br />

<div align="center">

`break_things() → learn() → repeat()`

</div>
