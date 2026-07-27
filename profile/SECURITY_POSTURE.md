# Security Posture & Trust Document
## DERAS Middleware — For Banking & Enterprise Clients

**Document Classification**: Public / Client-Facing  
**Prepared by**: DERAS-RFID Engineering & Security Team  
**Version**: 1.0  
**Date**: July 2026  
**Audience**: IT Security Officers, Procurement Teams, Enterprise Auditors  

---

## 1. Executive Summary

DERAS Middleware is an in-house developed software platform built by **DERAS-RFID** to serve as the integration layer between UHF RFID hardware and enterprise business systems. This document outlines the security controls, development practices, dependency management, and compliance alignment that DERAS-RFID maintains to ensure the software is safe to deploy in **banking, financial services, and regulated enterprise environments**.

---

## 2. Software Identity

| Field | Value |
|---|---|
| Product Name | DERAS Middleware |
| Component | MAIN_CORE |
| Developer | DERAS-RFID (In-House) |
| Platform | Windows / .NET Framework |
| Primary Function | UHF RFID Integration Gateway |
| Repository | [github.com/DERAS-RFID/.github](https://github.com/DERAS-RFID) |
| SBOM Available | ✅ [View SBOM](./SBOM.md) |
| Security Policy | ✅ [View Policy](../SECURITY.md) |

---

## 3. Secure Development Lifecycle (SDL)

DERAS-RFID follows a structured Secure Development Lifecycle to ensure security is addressed at every stage of software development:

### 3.1 Design Phase
- Threat modeling is performed for new features that involve data transmission, authentication, or external API exposure.
- The principle of **least privilege** is applied to all system components.
- Sensitive data (API tokens, credentials) are **never hardcoded**; environment variable injection is used via `dotenv.net`.

### 3.2 Development Phase
- Code follows **OWASP Secure Coding Practices**.
- Static code analysis is performed using integrated IDE analyzers.
- Input validation and output encoding are enforced at all API entry points.
- Bearer Token authentication (`EmbedIO.BearerToken` + `System.IdentityModel.Tokens.Jwt`) is used to protect all API endpoints.

### 3.3 Dependency Management
- All third-party packages are sourced exclusively from **NuGet.org** (Microsoft's verified package registry).
- Packages are managed using **PackageReference** (migrated from `packages.config`) to enable precise version locking.
- A full **Software Bill of Materials (SBOM)** is maintained and published: [SBOM.md](./SBOM.md).
- Dependencies are scanned against the **NVD (National Vulnerability Database)** on every release.

### 3.4 Build & Release Phase
- Builds are performed from clean environments.
- Release artifacts are version-tagged in the Git repository for full traceability.
- Release notes include security-relevant changes.

### 3.5 Vulnerability Response
- We maintain a published [Security Policy (SECURITY.md)](../SECURITY.md) with defined SLAs.
- Critical vulnerabilities are patched within **7 days**.
- CVE IDs are requested from MITRE for significant vulnerabilities.
- Affected banking clients are notified **privately before public disclosure**.

---

## 4. Authentication & Authorization Controls

| Control | Implementation |
|---|---|
| API Authentication | Bearer Token (JWT — `System.IdentityModel.Tokens.Jwt` v8.12.0) |
| Token Signing | Configurable symmetric/asymmetric key |
| Token Validation | Standard JWT claims validation (expiry, issuer, audience) |
| Transport Security | HTTPS enforced at the gateway layer (EmbedIO v3.5.2) |
| Credential Storage | Environment variables via `dotenv.net` — no hardcoded secrets |

---

## 5. Data Handling & Privacy

- **No PII (Personally Identifiable Information)** is processed by the RFID middleware layer. The middleware handles hardware tag IDs and device events only.
- Local data persistence uses **SQLite** (`System.Data.SQLite` v1.0.119) with file-level access controls enforced by the OS.
- Data serialization uses industry-standard formats: **JSON** (`System.Text.Json`, `Newtonsoft.Json`) and **Protobuf** (`protobuf-net`) — no proprietary binary formats.
- Log output is controlled via `Microsoft.Extensions.Logging.Abstractions` — sensitive fields are excluded from logs.

---

## 6. Network Security

| Aspect | Detail |
|---|---|
| API Transport | HTTP/HTTPS via EmbedIO embedded web server |
| WebSocket Support | Real-time event streaming over WSS |
| Port Binding | Configurable; default binding to localhost or defined network interface |
| Firewall Compatibility | No outbound cloud dependencies by default; fully on-premise capable |
| Network Protocol | Standard HTTP/1.1 — no custom or proprietary protocols |

---

## 7. Dependency Risk Assessment

All dependencies used in DERAS Middleware are:

- ✅ **Open-source** with publicly auditable source code
- ✅ **Published on NuGet.org** by verified publishers (Microsoft, VideoLAN, community)
- ✅ **Version-locked** via PackageReference
- ✅ **Scanned for known CVEs** at time of each release
- ✅ **Fully listed** in the published [SBOM](./SBOM.md)

**Key security-relevant packages:**

| Package | Role | Security Note |
|---|---|---|
| `System.IdentityModel.Tokens.Jwt` v8.12.0 | JWT authentication | Latest stable; active Microsoft maintenance |
| `Microsoft.IdentityModel.Tokens` v8.12.0 | Token validation | Actively maintained by Microsoft Identity team |
| `EmbedIO` v3.5.2 | Embedded HTTP/WS server | Scoped to internal network; no public exposure required |
| `System.Text.Json` v9.0.6 | JSON serialization | Latest .NET 9 series; replaces legacy Newtonsoft for new code |
| `EntityFramework` v6.5.1 | ORM / Database access | Parameterized queries enforced; SQL injection prevention |
| `protobuf-net` v3.2.52 | Binary serialization | Schema-defined; resistant to deserialization attacks |

---

## 8. Compliance Alignment

DERAS Middleware development practices are aligned with — though not certified against — the following standards. Clients requiring formal certification may request a detailed compliance mapping document.

| Framework / Standard | Alignment |
|---|---|
| **ISO/IEC 27001:2022** | Security controls in SDL, access management, incident response |
| **NIST SP 800-53 Rev. 5** | SA (System & Services Acquisition), SI (System Integrity), CM (Configuration Mgmt) |
| **OWASP Top 10 (2021)** | Input validation, authentication, logging, dependency management |
| **NTIA SBOM Minimum Elements** | SBOM published with supplier, component, version, dependency relationships |
| **PCI DSS v4.0** (informational) | Relevant controls for clients deploying in card-present environments |
| **Bank Indonesia / OJK Guidelines** | Alignment with domestic Indonesian banking IT governance (POJK MRTI) |

---

## 9. Incident Response

In the event of a security incident affecting DERAS Middleware:

1. **Detection** — Vulnerability report received or internally identified
2. **Triage** — Severity rated using CVSS v3.1 within 5 business days
3. **Containment** — Hotfix branch created; affected clients notified
4. **Remediation** — Patch developed and tested per SLA timelines
5. **Disclosure** — CVE requested from MITRE (if applicable); Security Advisory published
6. **Post-Incident Review** — Root cause documented; SDL process updated

Contact for incident reporting: **security@deras-rfid.com**

---

## 10. Client Audit Support

DERAS-RFID is prepared to support banking clients in their vendor security assessment process by providing:

- ✅ This Security Posture Document
- ✅ Published SBOM ([SBOM.md](./SBOM.md))
- ✅ Published Security Policy ([SECURITY.md](../SECURITY.md))
- ✅ CVE scan reports upon request
- ✅ Answers to vendor security questionnaires (VSQ / TPRM)
- ✅ Architecture and data-flow diagrams (available under NDA)
- ✅ Penetration test coordination (upon client request)

---

## 11. Document Revision History

| Version | Date | Author | Change |
|---|---|---|---|
| 1.0 | July 2026 | DERAS-RFID Engineering | Initial release |

---

*For security inquiries: **security@deras-rfid.com***  
*For general inquiries: Refer to [profile/README.md](./README.md)*
