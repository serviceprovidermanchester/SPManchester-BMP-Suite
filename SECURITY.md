# Security Policy

## Overview

**SPManchester Private Limited** takes the security of **PixelForge BMP Conversion Suite** seriously. Although this is a pure client-side, static web application with no server infrastructure, database, or authentication system, we are committed to maintaining a secure and trustworthy product for all users.

This document outlines our security policy, how to responsibly report a vulnerability, and what you can expect from us in response.

---

## Supported Versions

We actively maintain and issue security patches for the following versions:

| Version         | Supported          |
|-----------------|--------------------|
| Current release | ✅ Supported        |
| Older releases  | ❌ Not supported    |

> **Note:** We recommend all users always use the **latest version** of PixelForge BMP Conversion Suite, available at the official GitHub Pages deployment. Older versions receive no security updates.

---

## Scope & Attack Surface

PixelForge BMP Conversion Suite is a **100% client-side application**:

- ✅ Pure HTML, CSS, and JavaScript
- ✅ Runs entirely in the user's browser
- ✅ No server-side components
- ✅ No database
- ✅ No user authentication or account system
- ✅ No cookies or session tokens
- ✅ No network requests to any backend
- ✅ All file processing occurs locally in the browser via the Canvas API and FileReader API

As a result, the **attack surface is significantly limited** compared to a typical web application. However, potential security concerns may still include:

- **Malicious file parsing**: Specially crafted BMP files that could exploit browser-level vulnerabilities via Canvas API or FileReader API.
- **Cross-Site Scripting (XSS)**: Any dynamic HTML rendering that could be abused.
- **Dependency vulnerabilities**: Any third-party CDN-loaded resources (fonts, icons, etc.).
- **Content Security Policy (CSP)**: Misconfigured CSP headers on the GitHub Pages deployment.
- **Malicious redirects**: Any client-side routing that could be manipulated.

---

## Reporting a Vulnerability

If you believe you have found a security vulnerability in PixelForge BMP Conversion Suite, **please do not open a public GitHub Issue**. Public disclosure before a patch is available could put users at risk.

### How to Report

Please report vulnerabilities **privately** via email:

- 📧 **Primary:** [security@spmanchester.com](mailto:security@spmanchester.com)
- 📧 **Backup:** [info@spmanchester.com](mailto:info@spmanchester.com)

### What to Include in Your Report

Please provide as much detail as possible to help us reproduce and assess the issue:

1. **Description**: A clear and concise description of the vulnerability.
2. **Affected Component**: Which tool or section of the application is affected.
3. **Reproduction Steps**: Step-by-step instructions to reliably reproduce the issue.
4. **Proof of Concept**: Code snippets, screenshots, screen recordings, or a crafted test file (if applicable).
5. **Impact Assessment**: Your assessment of the potential impact (e.g., data exposure, code execution, UI spoofing).
6. **Environment**: Browser name and version, OS, and any relevant details.
7. **Suggested Fix** *(optional)*: If you have a proposed remediation, we welcome it.

**Please encrypt sensitive reports** using our PGP key if available. Contact us at [security@spmanchester.com](mailto:security@spmanchester.com) to request the public key.

---

## Response SLA (Service Level Agreement)

We are committed to the following response timeline from the moment your report is received:

| Milestone                          | Target Timeline         |
|------------------------------------|-------------------------|
| Initial acknowledgement            | Within **48 hours**     |
| Triage and severity assessment     | Within **5 business days** |
| Status update to reporter          | Within **7 business days** |
| Patch release — **Critical** severity | Within **14 days**   |
| Patch release — **High** severity  | Within **30 days**      |
| Patch release — **Medium / Low**   | Within **90 days**      |

> Timelines may vary for issues requiring coordination with browser vendors or third-party CDN providers. We will keep you informed of any delays.

---

## What NOT to Report Here

The following are **out of scope** for security reports. Please use [GitHub Issues](https://github.com/spmanchester/bmp/issues) for these instead:

- 🐛 **General software bugs** that do not have a security impact (e.g., incorrect colour output, UI glitches).
- 💡 **Feature requests or enhancements**.
- ⚡ **Performance issues** unrelated to security.
- 📄 **Documentation errors**.
- Issues that are **theoretical** with no demonstrated impact or reproduction steps.
- Vulnerabilities in **browsers themselves** (report these directly to the browser vendor).
- Issues requiring **physical access** to the user's device.
- **Self-XSS** (where a user must be tricked into running code in their own browser console).
- **Social engineering attacks** targeting SPManchester staff.

---

## Responsible Disclosure Policy

We follow the principles of **responsible / coordinated disclosure**:

1. **Report privately first.** Submit your findings to [security@spmanchester.com](mailto:security@spmanchester.com) before any public disclosure.
2. **Give us reasonable time.** Allow us the agreed SLA timeline to investigate and patch the issue before publishing.
3. **We will keep you informed.** We will provide regular updates on our progress throughout the process.
4. **We will credit you.** With your permission, we will publicly acknowledge your contribution in our Hall of Fame (see below) and in the patch release notes.
5. **Coordinated release.** We aim to publish a security advisory simultaneously with the patch release, unless disclosure would cause additional harm.
6. **No legal action.** We will not pursue legal action against researchers who report vulnerabilities in good faith and adhere to this policy.

We ask that you:
- **Do not** exploit the vulnerability beyond what is necessary to demonstrate it.
- **Do not** access, modify, or delete user data (note: this application processes no user data server-side).
- **Do not** perform any disruptive testing (DoS, spam, etc.) against the GitHub Pages deployment.
- **Do not** publicly disclose the vulnerability until we have issued a patch and given you the go-ahead.

---

## Hall of Fame

We are grateful to the security researchers who help keep PixelForge BMP Conversion Suite safe. With their permission, we acknowledge their contributions here.

| Researcher | Vulnerability | Date Reported |
|------------|---------------|---------------|
| *Be the first to contribute!* | — | — |

If you report a valid, in-scope vulnerability, we will add your name (or alias) and a brief description of the issue to this table once the patch has been released.

---

## Attribution

This security policy was authored by **SPManchester Private Limited** and is inspired by industry best practices including [GitHub's Security Advisories](https://docs.github.com/en/code-security/security-advisories) and the [CERT/CC Vulnerability Disclosure Policy](https://www.sei.cmu.edu/about/divisions/cert/).

---

**SPManchester Private Limited**
- 🌐 [www.spmanchester.com](https://www.spmanchester.com)
- 📧 [security@spmanchester.com](mailto:security@spmanchester.com) *(security reports)*
- 📧 [info@spmanchester.com](mailto:info@spmanchester.com) *(general enquiries)*
