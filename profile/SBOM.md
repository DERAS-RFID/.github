# Software Bill of Materials (SBOM)
## DERAS Middleware — MAIN_CORE

**Document Type**: SBOM (Software Bill of Materials)  
**Format Reference**: NTIA SBOM Minimum Elements  
**Component**: DERAS Middleware — MAIN_CORE  
**Generated**: July 2026  
**Standard**: CycloneDX / SPDX-compatible listing  

---

## Purpose

This document provides a complete inventory of all third-party software components included in the DERAS Middleware (MAIN_CORE) build. It is intended for:

- **Security audits** by banking and enterprise clients
- **Vulnerability assessment** teams (CVE / NVD scanning)
- **Compliance reviews** under frameworks such as ISO 27001, NIST SP 800-53, and PCI DSS
- **Supply chain risk management**

---

## Top-Level Dependencies

These are direct dependencies explicitly declared in the project.

| Package ID | Version | License | Source |
|---|---|---|---|
| 32feet.NET | v3.5.0 | MIT | [NuGet](https://www.nuget.org/packages/32feet.NET) |
| dotenv.net | v3.2.1 | MIT | [NuGet](https://www.nuget.org/packages/dotenv.net) |
| EmbedIO | v3.5.2 | MIT | [NuGet](https://www.nuget.org/packages/EmbedIO) |
| EmbedIO.BearerToken | v3.4.2 | MIT | [NuGet](https://www.nuget.org/packages/EmbedIO.BearerToken) |
| EntityFramework | v6.5.1 | Apache-2.0 | [NuGet](https://www.nuget.org/packages/EntityFramework) |
| LibVLCSharp.WinForms | v3.9.3 | LGPL-2.1 | [NuGet](https://www.nuget.org/packages/LibVLCSharp.WinForms) |
| Microsoft.Bcl.TimeProvider | v9.0.6 | MIT | [NuGet](https://www.nuget.org/packages/Microsoft.Bcl.TimeProvider) |
| Microsoft.Extensions.Logging.Abstractions | v9.0.6 | MIT | [NuGet](https://www.nuget.org/packages/Microsoft.Extensions.Logging.Abstractions) |
| NAudio | v2.2.1 | MIT | [NuGet](https://www.nuget.org/packages/NAudio) |
| Newtonsoft.Json | v13.0.3 | MIT | [NuGet](https://www.nuget.org/packages/Newtonsoft.Json) |
| protobuf-net | v3.2.52 | Apache-2.0 | [NuGet](https://www.nuget.org/packages/protobuf-net) |
| System.Data.SQLite | v1.0.119 | Public Domain | [NuGet](https://www.nuget.org/packages/System.Data.SQLite) |
| System.IdentityModel.Tokens.Jwt | v8.12.0 | MIT | [NuGet](https://www.nuget.org/packages/System.IdentityModel.Tokens.Jwt) |
| System.Memory | v4.6.3 | MIT | [NuGet](https://www.nuget.org/packages/System.Memory) |
| System.Text.Json | v9.0.6 | MIT | [NuGet](https://www.nuget.org/packages/System.Text.Json) |
| System.Threading.Tasks.Extensions | v4.6.3 | MIT | [NuGet](https://www.nuget.org/packages/System.Threading.Tasks.Extensions) |
| System.ValueTuple | v4.6.1 | MIT | [NuGet](https://www.nuget.org/packages/System.ValueTuple) |
| VideoLAN.LibVLC.Windows | v3.0.21 | LGPL-2.1 | [NuGet](https://www.nuget.org/packages/VideoLAN.LibVLC.Windows) |

---

## Transitive Dependencies

These are indirect dependencies pulled in by the top-level packages above.

| Package ID | Version | Source |
|---|---|---|
| LibVLCSharp | v3.9.3 | [NuGet](https://www.nuget.org/packages/LibVLCSharp) |
| Microsoft.Bcl.AsyncInterfaces | v9.0.6 | [NuGet](https://www.nuget.org/packages/Microsoft.Bcl.AsyncInterfaces) |
| Microsoft.Extensions.DependencyInjection.Abstractions | v9.0.6 | [NuGet](https://www.nuget.org/packages/Microsoft.Extensions.DependencyInjection.Abstractions) |
| Microsoft.IdentityModel.Abstractions | v8.12.0 | [NuGet](https://www.nuget.org/packages/Microsoft.IdentityModel.Abstractions) |
| Microsoft.IdentityModel.JsonWebTokens | v8.12.0 | [NuGet](https://www.nuget.org/packages/Microsoft.IdentityModel.JsonWebTokens) |
| Microsoft.IdentityModel.Logging | v8.12.0 | [NuGet](https://www.nuget.org/packages/Microsoft.IdentityModel.Logging) |
| Microsoft.IdentityModel.Tokens | v8.12.0 | [NuGet](https://www.nuget.org/packages/Microsoft.IdentityModel.Tokens) |
| Microsoft.NETCore.Platforms | v1.1.1 | [NuGet](https://www.nuget.org/packages/Microsoft.NETCore.Platforms) |
| Microsoft.NETCore.Targets | v1.1.3 | [NuGet](https://www.nuget.org/packages/Microsoft.NETCore.Targets) |
| Microsoft.Win32.Registry | v4.7.0 | [NuGet](https://www.nuget.org/packages/Microsoft.Win32.Registry) |
| NAudio.Asio | v2.2.1 | [NuGet](https://www.nuget.org/packages/NAudio.Asio) |
| NAudio.Core | v2.2.1 | [NuGet](https://www.nuget.org/packages/NAudio.Core) |
| NAudio.Midi | v2.2.1 | [NuGet](https://www.nuget.org/packages/NAudio.Midi) |
| NAudio.Wasapi | v2.2.1 | [NuGet](https://www.nuget.org/packages/NAudio.Wasapi) |
| NAudio.WinForms | v2.2.1 | [NuGet](https://www.nuget.org/packages/NAudio.WinForms) |
| NAudio.WinMM | v2.2.1 | [NuGet](https://www.nuget.org/packages/NAudio.WinMM) |
| protobuf-net.Core | v3.2.52 | [NuGet](https://www.nuget.org/packages/protobuf-net.Core) |
| Stub.System.Data.SQLite.Core.NetFramework | v1.0.119 | [NuGet](https://www.nuget.org/packages/Stub.System.Data.SQLite.Core.NetFramework) |
| System.Buffers | v4.6.1 | [NuGet](https://www.nuget.org/packages/System.Buffers) |
| System.Collections.Immutable | v7.0.0 | [NuGet](https://www.nuget.org/packages/System.Collections.Immutable) |
| System.Data.SQLite.Core | v1.0.119 | [NuGet](https://www.nuget.org/packages/System.Data.SQLite.Core) |
| System.Data.SQLite.EF6 | v1.0.119 | [NuGet](https://www.nuget.org/packages/System.Data.SQLite.EF6) |
| System.Data.SQLite.Linq | v1.0.119 | [NuGet](https://www.nuget.org/packages/System.Data.SQLite.Linq) |
| System.Diagnostics.DiagnosticSource | v9.0.6 | [NuGet](https://www.nuget.org/packages/System.Diagnostics.DiagnosticSource) |
| System.IO | v4.3.0 | [NuGet](https://www.nuget.org/packages/System.IO) |
| System.IO.Pipelines | v9.0.6 | [NuGet](https://www.nuget.org/packages/System.IO.Pipelines) |
| System.Net.Http | v4.3.4 | [NuGet](https://www.nuget.org/packages/System.Net.Http) |
| System.Numerics.Vectors | v4.6.1 | [NuGet](https://www.nuget.org/packages/System.Numerics.Vectors) |
| System.Private.Uri | v4.3.2 | [NuGet](https://www.nuget.org/packages/System.Private.Uri) |
| System.Runtime | v4.3.0 | [NuGet](https://www.nuget.org/packages/System.Runtime) |
| System.Runtime.CompilerServices.Unsafe | v6.1.2 | [NuGet](https://www.nuget.org/packages/System.Runtime.CompilerServices.Unsafe) |
| System.Security.AccessControl | v4.7.0 | [NuGet](https://www.nuget.org/packages/System.Security.AccessControl) |
| System.Security.Cryptography.Algorithms | v4.3.0 | [NuGet](https://www.nuget.org/packages/System.Security.Cryptography.Algorithms) |
| System.Security.Cryptography.Encoding | v4.3.0 | [NuGet](https://www.nuget.org/packages/System.Security.Cryptography.Encoding) |
| System.Security.Cryptography.Primitives | v4.3.0 | [NuGet](https://www.nuget.org/packages/System.Security.Cryptography.Primitives) |
| System.Security.Cryptography.X509Certificates | v4.3.0 | [NuGet](https://www.nuget.org/packages/System.Security.Cryptography.X509Certificates) |
| System.Security.Principal.Windows | v4.7.0 | [NuGet](https://www.nuget.org/packages/System.Security.Principal.Windows) |
| System.Text.Encodings.Web | v9.0.6 | [NuGet](https://www.nuget.org/packages/System.Text.Encodings.Web) |
| System.Text.RegularExpressions | v4.3.1 | [NuGet](https://www.nuget.org/packages/System.Text.RegularExpressions) |
| Unosquare.Swan.Lite | v3.1.0 | [NuGet](https://www.nuget.org/packages/Unosquare.Swan.Lite) |

---

## Known Vulnerability Status

All packages listed above were scanned at the time of migration (July 2026) against:
- **NVD (National Vulnerability Database)**
- **GitHub Advisory Database**

> ✅ **No known vulnerabilities (CVEs) were identified at the time of this SBOM generation.**

*This SBOM should be re-evaluated upon every release or when NIST NVD publishes new advisories affecting any listed component.*

---

## SBOM Maintenance

| Event | Action |
|---|---|
| New package added | SBOM updated before merge |
| Package version bumped | SBOM updated and CVE re-scan performed |
| New CVE published | Triage within 5 business days |
| Major release | Full SBOM re-generation and review |

---

*For questions about this SBOM, contact: security@deras-rfid.com*  
*Last updated: July 2026*
