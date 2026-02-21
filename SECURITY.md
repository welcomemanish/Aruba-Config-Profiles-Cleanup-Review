# Security Policy

## Supported Versions

| Version | Supported |
|---|---|
| Latest (HTML single-file) | ✅ Active |

---

## About This Tool

**Aruba CPCR — Config Profiles Cleanup Review** is a fully client-side, single HTML file tool. It runs entirely in your browser — no data is transmitted to any server, no backend exists, and no network requests are made during file processing.

That said, responsible disclosure of any security concerns is always welcome.

---

## Reporting a Vulnerability

If you discover a security vulnerability in this project, please **do not open a public GitHub Issue**. Instead, report it privately by following these steps:

1. Go to the **Security** tab of this repository
2. Click **"Report a vulnerability"** to open a private advisory
3. Alternatively, contact the maintainer directly via GitHub: [github.com/welcomemanish](https://github.com/welcomemanish)

Please include the following in your report:

- A clear description of the vulnerability
- Steps to reproduce the issue
- The potential impact or attack scenario
- Any suggested mitigation or fix (optional but appreciated)

---

## What to Report

Examples of issues worth reporting:

- **XSS (Cross-Site Scripting)** — malicious content from a crafted log file being executed in the browser
- **Malicious file handling** — the file parser being exploited via a specially crafted input file
- **Data leakage** — any scenario where file contents could be inadvertently exposed
- **Dependency vulnerabilities** — issues with any external resources (e.g. Google Fonts CDN) that could be abused

---

## Response Timeline

| Stage | Target |
|---|---|
| Acknowledgement of report | Within 5 business days |
| Initial assessment | Within 10 business days |
| Fix or mitigation | As soon as reasonably possible |

---

## Scope

This policy covers the HTML file distributed in this repository. It does not cover:

- Vulnerabilities in the user's browser itself
- Issues arising from running the tool in unsupported or modified environments
- Social engineering attacks

---

Thank you for helping keep this project and its users safe.
