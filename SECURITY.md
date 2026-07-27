# Security Policy

## Overview

DERAS-RFID takes the security of our software products and services seriously. We are committed to responsible vulnerability disclosure and timely remediation to protect our clients across all industries.

---

## Reporting a Vulnerability

**Please do NOT report security vulnerabilities through public GitHub Issues.**

If you discover a security vulnerability in any DERAS-RFID software, please report it privately via:

- **Email**: security@deras-rfid.com
- **Subject Line**: `[SECURITY] <Brief Description>`
- **PGP Encryption**: Available upon request for sensitive disclosures

### What to Include in Your Report

To help us triage and respond efficiently, please provide:

1. Affected component / module name
2. Description of the vulnerability
3. Steps to reproduce (Proof of Concept if available)
4. Potential impact assessment
5. Your contact information (for follow-up)

---

## Response Timeline (SLA)

| Stage                          | Target Time         |
| ------------------------------ | ------------------- |
| Acknowledgement of report      | ≤ 48 hours          |
| Initial triage & severity rating | ≤ 5 business days |
| Patch development (Critical)   | ≤ 7 days            |
| Patch development (High)       | ≤ 14 days           |
| Patch development (Medium/Low) | ≤ 30 days           |
| Public disclosure (CVE)        | After patch release |

---

## Severity Classification

We use the **CVSS v3.1** scoring system to rate vulnerabilities:

| Severity  | CVSS Score  | Description                                           |
| --------- | ----------- | ----------------------------------------------------- |
| Critical  | 9.0 – 10.0  | Immediate action required; full system compromise     |
| High      | 7.0 – 8.9   | Significant risk; exploitation likely                 |
| Medium    | 4.0 – 6.9   | Limited scope; exploitation requires conditions       |
| Low       | 0.1 – 3.9   | Minimal impact; informational                         |

---

## CVE Disclosure Policy

DERAS-RFID will:

- **Request CVE IDs** from [MITRE](https://cve.mitre.org/) or the relevant CNA (CVE Numbering Authority) for confirmed, significant vulnerabilities in our software.
- Publish a **Security Advisory** on this GitHub repository upon patch release.
- Update the **SBOM (Software Bill of Materials)** when vulnerable dependencies are replaced.
- Notify affected enterprise and banking clients **directly via secure channel** before public disclosure.

We adhere to **coordinated vulnerability disclosure (CVD)** principles and request that reporters allow us the above SLA before any public disclosure.

---

## Dependency Vulnerability Monitoring

DERAS Middleware dependencies are actively monitored against:

- **NVD (National Vulnerability Database)** — [nvd.nist.gov](https://nvd.nist.gov)
- **GitHub Dependabot Alerts**
- **OWASP Dependency-Check**
- **Snyk / Trivy** (on integration pipeline)

A full list of dependencies is maintained in our [Software Bill of Materials (SBOM)](./profile/SBOM.md).

---

## Responsible Disclosure Credits

We appreciate and acknowledge the security research community. Researchers who responsibly disclose vulnerabilities will be:

- Credited in our Security Advisory (with permission)
- Recognized in our public **Hall of Thanks** (upon request)

---

## Compliance References

Our security practices are aligned with:

- **ISO/IEC 27001** — Information Security Management
- **OWASP Top 10** — Web Application Security Risks
- **NIST SP 800-53** — Security and Privacy Controls
- **PCI DSS** (informational alignment for clients in financial services)

---

*This policy is reviewed and updated at minimum every 6 months or following any significant security event.*

*Last reviewed: July 2026*