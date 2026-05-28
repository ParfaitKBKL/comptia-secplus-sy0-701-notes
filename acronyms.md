# Security+ SY0-701 - Key Acronyms

Essential acronyms organized by domain for quick review.
**Recommended method:** Go back and forth acronym to definition, then definition to acronym.

---

## Domain 1 - General Security Concepts

| Acronym | Full name | Note |
|---|---|---|
| CIA | Confidentiality, Integrity, Availability | Fundamental triad |
| AAA | Authentication, Authorization, Accounting | Access framework |
| ZT | Zero Trust | "Never trust, always verify" |
| PEP | Policy Enforcement Point | ZT component |
| PKI | Public Key Infrastructure | Certificate infrastructure |
| CA | Certificate Authority | Issues and signs certificates |
| CSR | Certificate Signing Request | Request for certificate signature |
| CRL | Certificate Revocation List | List of revoked certificates |
| OCSP | Online Certificate Status Protocol | Real-time certificate status check |
| TPM | Trusted Platform Module | Secure chip on motherboard |
| HSM | Hardware Security Module | Dedicated hardware for key management (FIPS 140-2) |
| AES | Advanced Encryption Standard | Current symmetric encryption |
| RSA | Rivest, Shamir and Adleman | Asymmetric encryption |
| ECC | Elliptic Curve Cryptography | Asymmetric - smaller keys, faster |
| DH | Diffie-Hellman | Secure key exchange |
| DHE | Diffie-Hellman Ephemeral | Supports Perfect Forward Secrecy |
| ECDHE | Elliptic Curve Diffie-Hellman Ephemeral | ECC variant of DHE |
| PFS | Perfect Forward Secrecy | Unique session key per connection |
| PBKDF2 | Password-Based Key Derivation Function 2 | Key stretching - slows brute force |
| SHA | Secure Hash Algorithm | SHA-256 recommended |
| MD5 | Message Digest 5 | **Broken** - no longer use for security |

---

## Domain 2 - Threats, Vulnerabilities, Mitigations

| Acronym | Full name | Note |
|---|---|---|
| APT | Advanced Persistent Threat | Nation-state, long dwell time |
| TTP | Tactics, Techniques and Procedures | How attackers operate |
| ATT&CK | Adversarial Tactics, Techniques and Common Knowledge | MITRE framework |
| IoC | Indicators of Compromise | Observable compromise signals |
| CVE | Common Vulnerabilities and Exposures | Unique vulnerability identifier |
| CVSS | Common Vulnerability Scoring System | Severity score 0-10 |
| NVD | National Vulnerability Database | NIST CVE database |
| KEV | Known Exploited Vulnerabilities | CISA catalog - actively exploited |
| DDoS | Distributed Denial of Service | Availability attack |
| MitM | Man-in-the-Middle | Traffic interception/modification |
| SQLi | SQL Injection | Injection into SQL queries |
| XSS | Cross-Site Scripting | Malicious script in a web page |
| CSRF | Cross-Site Request Forgery | Force an unwanted request |
| SSRF | Server-Side Request Forgery | Force the server to make internal requests |
| BEC | Business Email Compromise | Executive identity spoofing for wire fraud |
| RAT | Remote Access Trojan | Trojan granting remote access |
| PUP | Potentially Unwanted Program | Unwanted program |
| RFID | Radio Frequency Identification | Access card technology |
| NFC | Near Field Communication | Short-range communication |
| ASLR | Address Space Layout Randomization | Buffer overflow mitigation |
| DEP | Data Execution Prevention | Buffer overflow mitigation |
| TOC | Time-of-Check | Component of TOC/TOU race condition |
| TOU | Time-of-Use | Component of TOC/TOU race condition |
| MSP | Managed Service Provider | Outsourced IT provider |
| MSSP | Managed Security Service Provider | Outsourced SOC, managed SIEM |

---

## Domain 3 - Security Architecture

| Acronym | Full name | Note |
|---|---|---|
| IaaS | Infrastructure as a Service | Cloud - OS managed by customer |
| PaaS | Platform as a Service | Cloud - app managed by customer |
| SaaS | Software as a Service | Cloud - only data on customer side |
| IaC | Infrastructure as Code | Terraform, Ansible |
| SDN | Software-Defined Networking | Separated control plane |
| SCADA | Supervisory Control and Data Acquisition | OT/ICS - industrial control |
| ICS | Industrial Control Systems | Industrial control systems |
| RTOS | Real-Time Operating System | Strict real-time constraints |
| OT | Operational Technology | Physical control systems |
| DMZ | Demilitarized Zone | Network buffer zone |
| VPN | Virtual Private Network | Encrypted tunnel |
| TLS | Transport Layer Security | Transport encryption (HTTPS) |
| SSL | Secure Sockets Layer | **Deprecated** - replaced by TLS |
| IPSec | Internet Protocol Security | Network-layer VPN |
| AH | Authentication Header | IPSec - integrity without encryption |
| ESP | Encapsulating Security Payload | IPSec - integrity + encryption |
| IKE | Internet Key Exchange | IPSec key exchange |
| SD-WAN | Software-Defined Wide Area Network | Software-managed WAN |
| SASE | Secure Access Service Edge | SD-WAN + cloud security |
| ZTNA | Zero Trust Network Access | SASE component |
| CASB | Cloud Access Security Broker | Cloud app visibility/control |
| WAF | Web Application Firewall | Layer 7, OWASP Top 10 |
| NGFW | Next-Generation Firewall | Deep packet inspection |
| UTM | Unified Threat Management | All-in-one FW+IPS+AV+VPN |
| UPS | Uninterruptible Power Supply | Immediate backup power |
| RTO | Recovery Time Objective | Maximum acceptable downtime |
| RPO | Recovery Point Objective | Maximum acceptable data loss |
| MTTR | Mean Time to Repair | Average repair time |
| MTBF | Mean Time Between Failures | System reliability |
| FDE | Full Disk Encryption | Full disk encryption |

---

## Domain 4 - Security Operations

| Acronym | Full name | Note |
|---|---|---|
| MDM | Mobile Device Management | Mobile device management |
| BYOD | Bring Your Own Device | Personal device - low control |
| COPE | Company-Owned, Personally Enabled | Company device - high control |
| CYOD | Choose Your Own Device | Approved list - medium control |
| WPA3 | Wi-Fi Protected Access 3 | Current standard, SAE |
| SAE | Simultaneous Authentication of Equals | WPA3 - resistant to dict. attacks |
| RADIUS | Remote Authentication Dial-In User Service | 802.1X authentication server |
| EAP | Extensible Authentication Protocol | Auth framework with 802.1X |
| EAP-TLS | EAP with Transport Layer Security | Certificates - most secure |
| PEAP | Protected EAP | Password in a TLS tunnel |
| IDS | Intrusion Detection System | Out-of-band - alert only |
| IPS | Intrusion Prevention System | Inline - alert + block |
| HIPS | Host-based Intrusion Prevention System | IPS at the endpoint level |
| EDR | Endpoint Detection and Response | Behavioral + forensic |
| XDR | Extended Detection and Response | EDR + network + cloud + email |
| UBA | User Behavior Analytics | Detects behavioral anomalies |
| UEBA | User and Entity Behavior Analytics | Extends UBA to non-human entities |
| SIEM | Security Information and Event Management | Aggregates + correlates logs |
| SOAR | Security Orchestration, Automation and Response | Automated alert response |
| DLP | Data Loss Prevention | Prevents data leakage |
| NAC | Network Access Control | Network access control (posture) |
| FIM | File Integrity Monitoring | Detects file changes |
| SCAP | Security Content Automation Protocol | Standardized compliance checking |
| SNMP | Simple Network Management Protocol | Network device alerts |
| GPO | Group Policy Object | Centralized Windows policies |
| SPF | Sender Policy Framework | Email - authorizes sending servers |
| DKIM | DomainKeys Identified Mail | Email - cryptographic signature |
| DMARC | Domain-based Message Authentication, Reporting and Conformance | Email - SPF/DKIM policy |
| MFA | Multifactor Authentication | 2+ authentication factors |
| TOTP | Time-based One-Time Password | OTP valid for 30 seconds |
| HOTP | HMAC-based One-Time Password | OTP valid until used |
| FIDO2 | Fast Identity Online 2 | WebAuthn standard - phishing resistant |
| SSO | Single Sign-On | Single authentication |
| LDAP | Lightweight Directory Access Protocol | Active Directory querying |
| SAML | Security Assertion Markup Language | XML-based enterprise SSO |
| OIDC | OpenID Connect | Authentication layer on OAuth |
| RBAC | Role-Based Access Control | Permissions tied to roles |
| DAC | Discretionary Access Control | Owner decides |
| MAC | Mandatory Access Control | OS enforces based on labels |
| ABAC | Attribute-Based Access Control | Decisions based on contextual attributes |
| PAM | Privileged Access Management | Privileged access management |
| SAST | Static Application Security Testing | Source code analysis |
| DAST | Dynamic Application Security Testing | Running app testing |
| CMDB | Configuration Management Database | Asset inventory |
| PCAP | Packet Capture | Network packet capture |
| MTTD | Mean Time to Detect | Average detection delay |
| IOC | Indicators of Compromise | Evidence of compromise |

---

## Domain 5 - Security Program Management

| Acronym | Full name | Note |
|---|---|---|
| AUP | Acceptable Use Policy | Rules for system use |
| SLA | Service Level Agreement | Performance standards - violations = penalties |
| MOA | Memorandum of Agreement | Formal agreement between parties |
| MOU | Memorandum of Understanding | Informal agreement - intentions |
| MSA | Master Service Agreement | Framework contract |
| SOW | Statement of Work | Specific project deliverables |
| NDA | Non-Disclosure Agreement | Confidentiality |
| BPA | Business Partners Agreement | Ongoing business relationship |
| SLE | Single Loss Expectancy | Cost of a single incident (AV x EF) |
| ALE | Annualized Loss Expectancy | Expected annual cost (SLE x ARO) |
| ARO | Annualized Rate of Occurrence | Annual frequency of an incident |
| AV | Asset Value | Value of the asset |
| EF | Exposure Factor | % of asset lost if incident occurs |
| BIA | Business Impact Analysis | Impact of disruption to critical functions |
| GDPR | General Data Protection Regulation | EU citizens data |
| CCPA | California Consumer Privacy Act | California residents data |
| PCI DSS | Payment Card Industry Data Security Standard | Payment card data |
| HIPAA | Health Insurance Portability and Accountability Act | US health data (PHI) |
| SOX | Sarbanes-Oxley Act | Financial controls for public companies |
| PHI | Protected Health Information | HIPAA-protected health data |
| PII | Personally Identifiable Information | Personally identifiable data |
| OSINT | Open-Source Intelligence | Open-source intelligence gathering |
| SDLC | Software Development Lifecycle | Development lifecycle |
| ISAC | Information Sharing and Analysis Center | Sector-based threat intel sharing |
| SOC | System and Organization Controls | Audit report (SOC 1, SOC 2) |
| CAB | Change Advisory Board | Change approval committee |
