# CompTIA Security+ SY0-701 – Technical Study Guide

This edition keeps the same 19 thematic groups and the official CompTIA acronym appendix as its coverage baseline. It replaces generic acronym paraphrases with exam-oriented technical explanations, comparisons, attack/defense mechanisms, scenario cues, and technical references.

## How to use this guide

**Edition update:** the official acronym tables now use a technical-role description instead of the original PDF-page column. Selected acronyms have been regrouped under the part where their function is taught. The CompTIA expansion is retained as printed; explanatory notes distinguish similar terms and flag legacy technologies.

1. Read the technical model and understand the mechanism.
2. Study the distinctions and exam traps; Security+ questions often describe a scenario rather than ask for a definition.
3. Review supplementary acronyms separately. They are **not** part of the official CompTIA appendix unless explicitly stated.
4. Use the linked RFCs, NIST publications, standards bodies, and OWASP guidance for deeper study.

## Important source discipline

- **Official appendix acronym** means the abbreviation appears in the supplied CompTIA acronym appendix.
- **Supplementary concept** means it is added for learning and is not in that appendix; it may nevertheless help explain an exam objective.
- **Legacy / optional depth** identifies older or additional technology included for context, not as a claim that CompTIA requires memorizing it.

- Official expansions are preserved from the supplied CompTIA SY0-701 Exam Objectives, Version 5.0, pages 17–20.
- Official entries are not silently corrected, even where wording differs from standard industry phrasing.
- Supplementary concepts are clearly labeled and added only to explain related technology or current practice.
- Exam emphasis is guided by the SY0-701 objectives; this is a study aid, not a substitute for the official objectives or hands-on practice.

## Contents

The PDF edition includes an automatically generated table of contents with page numbers. The 19 thematic parts remain in the original order.

## Source document

CompTIA Security+ SY0-701 Certification Exam: Exam Objectives, Version 5.0, especially the official acronym list on PDF pages 17–20 and hardware/software list on page 21.

---

# PARTIE I — Security foundations and core principles

> **Scope:** Core security principles and organizational foundations: confidentiality, integrity, availability, authentication, authorization, accounting, non-repudiation, security-control categories and functions, Zero Trust fundamentals, physical security principles, deception technologies, change management, and security accountability. Focus on the purpose of security controls and how foundational principles guide enterprise security decisions.

## 1. Security model: what are we protecting?

Security controls should be selected against a defined security objective. The CIA triad is not a product or a control family; it is a way to classify the impact of an event.

- **Confidentiality** prevents unauthorized disclosure. Typical controls: encryption, access control, data classification, tokenization, and least privilege.
- **Integrity** prevents or detects unauthorized or accidental alteration. Typical controls: cryptographic hashes for change detection, HMAC for keyed integrity/authentication, digital signatures for integrity plus signer authentication, and FIM for monitoring critical files.
- **Availability** keeps systems and data usable when required. Typical controls: redundancy, failover, capacity planning, backups, disaster recovery, DDoS protection, and resilient architecture.

**Do not confuse the mechanisms.** Encryption primarily protects confidentiality; it does not automatically prove that data was not modified. A plain hash detects a changed value only when the expected hash is trusted. An HMAC adds a shared secret, while a digital signature uses asymmetric cryptography. A backup supports recovery but does not by itself provide high availability.

A single incident can affect more than one CIA property. Ransomware may affect availability by making data unusable and integrity if it alters or destroys data. Exfiltration is primarily a confidentiality breach. A DDoS is primarily an availability attack.

## 2. AAA: separate identity, permission, and evidence

AAA divides access management into three decisions/events:

1. **Authentication** establishes or verifies an identity (password, certificate, token, biometric, or a combination).
2. **Authorization** evaluates what the authenticated identity is allowed to do (role, group, policy, resource ACL, attributes, device posture, or context).
3. **Accounting** records what happened (login time, session duration, commands, bytes transferred, or administrative actions).

Authentication success is not authorization. A valid employee account should not automatically receive administrator rights. Accounting is evidence for auditing and investigation; it is not itself a preventive access decision.

Centralized AAA commonly uses RADIUS or TACACS+ for network-device and network-access scenarios. LDAP is a directory access protocol; it may supply identity/group data to an authentication system, but it is not interchangeable with RADIUS or TACACS+.

## 3. Organizational accountability

CIO, CTO, CSO/CISO, and ISSO are responsibility labels, not technical protocols. In scenario questions, map the described decision to the role: enterprise IT strategy (CIO), technology direction/architecture (CTO), security leadership and risk oversight (CSO/CISO), or security implementation/assessment for a particular information system (ISSO). Actual reporting lines vary by organization.

A corrective action process should identify the finding, determine root cause, assign an owner and deadline, implement a correction, and verify effectiveness. Merely fixing the immediate symptom is weaker than removing the process failure that caused it.

## 4. Standards and frameworks: ISO and NIST

**ISO/IEC 27001** specifies requirements for an Information Security Management System (ISMS): organizational context, leadership, risk assessment/treatment, documented processes, evaluation, and continual improvement. **ISO/IEC 27002** provides guidance on information-security controls; it is not the certifiable ISMS requirements standard.

**NIST** publishes standards and guidance. NIST CSF 2.0 is an outcome-oriented cybersecurity risk framework with Govern, Identify, Protect, Detect, Respond, and Recover. NIST SP 800-53 is a catalog of security and privacy controls; SP 800-61 Rev. 3 is current NIST incident-response guidance aligned with CSF 2.0. Do not treat a framework, control catalog, and certification standard as the same thing.

## 5. Economic reasoning

ROI compares a financial benefit with an investment cost. It is useful for communicating value, but security benefits are often estimates (avoided loss, reduced downtime, lower response cost, or compliance exposure). Do not confuse ROI with ALE: ROI evaluates an investment; ALE estimates annualized loss from a risk scenario.

## Exam cues

- “Unauthorized disclosure/read” → confidentiality.
- “Unauthorized modification/tampering” → integrity.
- “Service unavailable, outage, resource exhaustion” → availability.
- “Who are you / what can you do / what did you do?” → authentication / authorization / accounting.
- “Correct the root cause and prevent recurrence” → corrective action, not only remediation of the individual finding.
- “ISMS requirements / certification” → ISO/IEC 27001; “risk framework functions” → NIST CSF; “control catalog” → NIST SP 800-53.

## Supplementary concepts — not in the official acronym appendix
These items are added for technical understanding and are not entries in CompTIA’s acronym appendix. Some may still support exam-objective topics; absence from the appendix does **not** mean “out of scope.” Treat items explicitly described as legacy or optional as additional depth.

- **CISO** — Chief Information Security Officer; commonly the executive accountable for information-security strategy. The exact relationship to CSO varies by organization.
- **ISMS** — Information Security Management System; the management system addressed by ISO/IEC 27001.
- **CSF** — Cybersecurity Framework; in this context, NIST CSF 2.0.
- **ALE** — Annualized Loss Expectancy; estimated annual loss, commonly SLE × ARO.

## Technical references

- [NIST Cybersecurity Framework 2.0](https://doi.org/10.6028/NIST.CSWP.29)
- [ISO/IEC 27001 overview](https://www.iso.org/standard/27001)
- [NIST SP 800-61 Rev. 3 — Incident Response](https://csrc.nist.gov/pubs/sp/800/61/r3/final)
- [NIST SP 800-53 — Security and Privacy Controls](https://csrc.nist.gov/pubs/sp/800/53/r5/upd1/final)

## Official acronym coverage

The following entries are preserved from the CompTIA SY0-701 acronym appendix. The third column explains the technical role and highlights useful distinctions. An acronym can have different meanings in different domains; read the expansion and the surrounding context together.


| Acronym | Official expansion (CompTIA) | Description / technical role |
|---|---|---|
| `AAA` | Authentication, Authorization, and Accounting | Framework separating identity verification, permission decisions and activity logging. |
| `AI` | Artificial Intelligence | Systems performing tasks associated with human intelligence; in security, also used for analytics and automation. |
| `CAR` | Corrective Action Report | Document recording a corrective action, its owner, cause, deadline and verification. |
| `CIA` | Confidentiality, Integrity, Availability | Confidentiality prevents disclosure; integrity protects against unauthorized change; availability keeps services usable. |
| `CIO` | Chief Information Officer | Executive responsible for enterprise information technology strategy and operations. |
| `CSO` | Chief Security Officer | Senior security executive; exact remit may overlap with or differ from the CISO. |
| `CTO` | Chief Technology Officer | Executive responsible for technology direction, engineering and architecture. |
| `ISO` | International Standards Organization | International standards organization; do not confuse the organization with an individual ISO standard. |
| `ISSO` | Information Systems Security Officer | Officer coordinating security requirements and controls for a particular information system. |
| `NIST` | National Institute of Standards & Technology | US standards body publishing cybersecurity frameworks, standards and technical guidance. |
| `ROI` | Return on Investment | Investment-value measure; compare financial benefit with cost, unlike ALE which estimates annualized risk loss. |

---

**Study rule:** learn the technical distinction in the explanation above, then use the official acronym list as a recognition checklist. Do not memorize an acronym expansion as a substitute for understanding the mechanism.


---


# PARTIE II — Access control models and permissions

> **Scope:** Authorization and permission-management mechanisms: subjects, objects, access rights, discretionary, mandatory, role-based and attribute-based access control, rule-based access, access control lists, file permissions, group policies, privileged access, least privilege, and access reviews. Focus on how access decisions are defined, assigned, enforced, and periodically reassessed.

## 1. Access-control decision model

An access-control system evaluates a **subject** (user, process, service account) attempting an **operation** on an **object** (file, database row, API, device, or network service). A policy decides whether the operation is allowed. The useful exam question is: *who controls the policy, what attribute drives the decision, and where is the permission enforced?*

### DAC — Discretionary Access Control

The resource owner can grant or revoke access, commonly through file permissions or ACL entries. It is flexible and familiar, but permissions can spread through user-controlled sharing. A file owner may accidentally expose sensitive data. Unix ownership and discretionary file permissions are common examples.

### MAC — Mandatory Access Control

A central policy enforces access using security labels/classifications and user clearances. A user generally cannot override the policy simply because they own the file. Think classified environments and strict information-flow rules. In classic confidentiality models, a subject's clearance and an object's classification determine whether access is permitted.

### RBAC — Role-based Access Control

Permissions are assigned to job roles; users receive permissions through role membership. It scales better than assigning every permission individually and supports separation of duties. Its weakness is role explosion or stale role membership if roles are poorly designed.

CompTIA lists **RBAC twice**: Role-based Access Control and Rule-based Access Control. Do not collapse them. Role-based decisions depend on a user's assigned role; rule-based decisions depend on explicit conditions/policies (for example, allow SSH only from a management subnet during approved hours). Product terminology sometimes uses “rule-based” inconsistently, so read the scenario.

### ABAC — Attribute-Based Access Control (supplementary)

ABAC evaluates attributes of the subject, object, action, and environment: department, data sensitivity, device compliance, location, time, or requested operation. It is more context-aware than basic RBAC but policy design and troubleshooting are more complex.

## 2. ACL and FACL: how permissions are represented

An **Access Control List** is attached to a resource or enforcement point and specifies which identities/groups can perform which operations. A **File System ACL (FACL)** is the filesystem-specific form. Typical permissions include read, write, execute, delete, modify, and ownership/control.

Do not assume that “user is in the right group” means access is granted. Effective access may be the result of allow and deny entries, group nesting, inheritance, ownership, share permissions combined with filesystem permissions, and platform-specific precedence. In Windows, share permissions and NTFS permissions both apply over a network share; the more restrictive effective result normally governs.

An ACL is not the same as a capability list: an ACL answers “who can access this object?”; a capability model associates a subject with unforgeable authority to access specified objects/operations.

## 3. IAM, GPO, and NAC operate at different layers

- **IAM** governs digital identities and their lifecycle: provisioning, role/group assignment, authentication integration, access changes, deprovisioning, and periodic review.
- **GPO** (Group Policy Object) applies centrally managed configuration settings to users/computers in Active Directory environments. It can enforce security baselines, password policies, firewall settings, audit policy, and software restrictions. GPO is configuration management, not an authorization model by itself.
- **NAC** evaluates whether a device/user may connect to a network and may assign a VLAN, quarantine network, or restricted access based on identity, device posture, and policy. NAC commonly integrates with 802.1X, RADIUS, directory services, and endpoint posture checks.

## 4. PAM and privileged access

**Privileged Access Management (PAM)** controls powerful accounts and sessions: administrator/root accounts, service accounts, database admins, and emergency accounts. Common capabilities include credential vaulting, password/key rotation, just-in-time elevation, approval workflows, session recording, command auditing, and removal of standing privileges.

PAM is not the same as **Pluggable Authentication Modules (PAM)**, also listed by CompTIA. The latter is an operating-system authentication framework that lets services use configurable authentication modules (for example, password, smart-card, or MFA modules). Context decides which PAM is meant.

## Exam traps

- Owner discretion → DAC; centrally enforced labels/clearance → MAC; job function → role-based RBAC; contextual attributes → ABAC.
- A GPO configures systems/users; it is not itself an ACL or an identity provider.
- NAC controls network admission/posture; IAM manages identity lifecycle and access governance.
- PAM (Privileged Access Management) secures elevated accounts; PAM (Pluggable Authentication Modules) is an authentication framework.
- Authentication proves identity; ACL/RBAC/ABAC authorization determines permitted actions.

## Supplementary concepts — not in the official acronym appendix
These items are added for technical understanding and are not entries in CompTIA’s acronym appendix. Some may still support exam-objective topics; absence from the appendix does **not** mean “out of scope.” Treat items explicitly described as legacy or optional as additional depth.

- **ABAC** — Attribute-Based Access Control.
- **JIT access** — Just-in-time, time-limited privilege elevation.
- **JEA** — Just Enough Administration; restricts administrators to only the commands/tasks needed.
- **SoD** — Separation of Duties; divides sensitive tasks so one person cannot complete an entire high-risk process alone.
- **PIM** — Privileged Identity Management; often used for time-bound activation of privileged roles.

## Technical references

- [NIST SP 800-162 — Guide to Attribute Based Access Control](https://csrc.nist.gov/pubs/sp/800/162/upd2/final)
- [NIST SP 800-53 — Access Control family](https://csrc.nist.gov/pubs/sp/800/53/r5/upd1/final)
- [Microsoft — Access Control Lists](https://learn.microsoft.com/en-us/windows/win32/secauthz/access-control-lists)
- [Microsoft — Group Policy overview](https://learn.microsoft.com/en-us/windows-server/identity/ad-ds/manage/group-policy/group-policy-overview)

## Official acronym coverage

The following entries are preserved from the CompTIA SY0-701 acronym appendix. The third column explains the technical role and highlights useful distinctions. An acronym can have different meanings in different domains; read the expansion and the surrounding context together.


| Acronym | Official expansion (CompTIA) | Description / technical role |
|---|---|---|
| `ACL` | Access Control List | List of subjects and permitted operations on a resource; commonly discretionary or filesystem-enforced. |
| `DAC` | Discretionary Access Control | Owner or designated authority controls access grants; permissions may be propagated to others. |
| `FACL` | File System Access Control List | Filesystem-specific ACL describing users/groups and their allowed file operations. |
| `FIM` | File Integrity Management | Monitoring critical files/configurations for unauthorized changes; complements access control and logging. |
| `GPO` | Group Policy Object | Windows Active Directory policy object applying centrally managed settings to users/computers. |
| `IAM` | Identity and Access Management | Lifecycle and governance of digital identities, authentication and authorization. |
| `IdP` | Identity Provider | System that authenticates users and supplies identity assertions/tokens to relying services. |
| `MAC` | Mandatory Access Control | Mandatory Access Control: policy/labels centrally enforce access; distinct from Message Authentication Code and Media Access Control. |
| `NAC` | Network Access Control | Controls whether a device may connect to a network, often using identity and posture checks. |
| `PAM` | Privileged Access Management | Controls privileged accounts, credentials, elevated sessions and approvals; distinct from Linux Pluggable Authentication Modules. |
| `RBAC` | Role-based Access Control | Role-based Access Control assigns permissions through roles; distinct from rule-based evaluation of conditions. |
| `RBAC` | Rule-based Access Control | Rule-based Access Control evaluates policy rules/conditions; distinct from role-based permissions assigned through job functions. |

---

**Study rule:** learn the technical distinction in the explanation above, then use the official acronym list as a recognition checklist. Do not memorize an acronym expansion as a substitute for understanding the mechanism.


---


# PARTIE III — Authentication, identity protocols and federation

> **Scope:** Identity verification and authentication technologies: authentication factors, multifactor authentication, biometrics, authentication protocols, directory services, Kerberos, RADIUS, TACACS+, LDAP, EAP, federation, single sign-on, SAML, OAuth, and OpenID Connect. Focus on how identities are verified, credentials are exchanged, authentication is centralized, and trust is established across systems and organizations.

## 1. Authentication factors and assurance

Authentication factors belong to different categories: **something you know** (password/PIN), **something you have** (hardware token, smart card, registered device), and **something you are** (biometric characteristic). MFA requires factors from at least two different categories. Two passwords are not MFA; password + authenticator-app code is generally two categories (knowledge + possession), subject to the implementation.

Biometric systems compare a sample against an enrolled template. **FAR** (False Acceptance Rate) measures impostors incorrectly accepted; **FRR** (False Rejection Rate) measures legitimate users incorrectly rejected. Tightening a biometric threshold often reduces FAR while increasing FRR. The crossover is commonly called the **CER/EER** (Crossover/Equal Error Rate); lower is generally better when comparing systems under equivalent test conditions.

HOTP is counter-based; TOTP is time-based. Both generate one-time passwords using HMAC-based constructions. TOTP requires reasonable clock synchronization; HOTP requires counter synchronization/resynchronization. Neither acronym alone means “MFA”—they are OTP mechanisms that may be one factor in an MFA flow.

## 2. Directory services: LDAP is not authentication itself

LDAP is a protocol for querying and modifying directory information, commonly users, groups, attributes, and organizational units. A directory stores identity data; an application or authentication service uses that data to make an authentication/authorization decision. LDAP can use TLS (commonly called LDAPS in deployments) or StartTLS to protect transport. Anonymous/simple binds without transport protection expose credentials and should not be used.

**Active Directory Domain Services (AD DS)** is Microsoft's directory service; LDAP is one protocol used to interact with it. Kerberos is commonly the domain authentication protocol. Do not confuse the directory (where identity objects live), the protocol used to query it (LDAP), and the authentication protocol (Kerberos).

## 3. Kerberos: tickets, KDC, TGT

Kerberos uses symmetric cryptography and a trusted **Key Distribution Center (KDC)**, typically composed of an Authentication Server (AS) and Ticket-Granting Server (TGS). A client authenticates and receives a **Ticket-Granting Ticket (TGT)**; the TGT is then used to request service tickets for specific services. The user's password is not sent to each service for every access.

The TGT is not the service ticket. The TGT allows the client to obtain service tickets; a service ticket is presented to the target service. Kerberos depends on time synchronization, protected KDC infrastructure, strong secrets, and correct SPN/service configuration. Clock skew, weak service-account passwords, ticket theft, and misconfigured delegation are common attack surfaces.

## 4. EAP family and network authentication

EAP is an authentication framework, not one single authentication algorithm. It allows different methods to be carried through a network access exchange, commonly 802.1X. **PEAP** creates a TLS-protected outer tunnel and then performs an inner authentication method. **LEAP** is an older Cisco method with known weaknesses and should not be treated as a modern preferred choice. CHAP and MS-CHAP are challenge-response protocols; PAP sends credentials in a simple form and requires a protected channel to avoid exposure.

In enterprise Wi-Fi, a supplicant (client) communicates through an authenticator (wireless AP/switch), which relays authentication to a RADIUS server. This is the common 802.1X/EAP architecture. The AP is not necessarily validating the user's password itself.

## 5. Federation and delegated authorization

**SAML** is an XML-based federation standard commonly used for browser-based enterprise SSO. An Identity Provider (IdP) authenticates the user and issues a signed assertion for a Service Provider (SP). Validate issuer, audience, recipient, validity window, signature, and assertion binding; weak validation or replay can enable account takeover.

**OAuth 2.0** is an authorization framework: it lets a client obtain limited access to a resource using access tokens. OAuth alone is not an authentication protocol. **OpenID Connect (OIDC)** adds an identity layer on top of OAuth 2.0, including an ID Token (usually a JWT) for authentication. SAML and OIDC are common SSO/federation alternatives; OAuth is primarily delegated authorization.

SSO means one authentication event/session can provide access to multiple services. It does not mean all services share one password or that MFA is unnecessary. A compromised IdP/session can have broad impact, so protect IdP accounts, signing keys, tokens, redirect URIs, and session lifetimes.

## Technical clarification: the 802.1X / EAP / RADIUS chain

These terms operate at different layers and should not be treated as competing protocols:

1. **802.1X** controls access to a wired switch port or wireless network before normal network access is granted.
2. The **supplicant** is the client requesting access; the **authenticator** is usually the switch or access point; the **authentication server** is commonly RADIUS.
3. **EAP** is the framework that carries an authentication method. It is not one single password algorithm.
4. **EAP-TLS** authenticates with certificates (normally client and server certificates). **PEAP** first creates a TLS-protected tunnel using the server certificate, then runs an inner method such as MS-CHAPv2.
5. **RADIUS** transports the authentication/authorization exchange between the network access device and the central server. It is not itself the EAP method.

**MS-CHAPv2 vs NTLM:** both use challenge-response ideas and are associated with Microsoft authentication, but they belong to different contexts. MS-CHAPv2 is encountered in PPP/network-access scenarios and as an inner PEAP method; NTLM is a Windows network authentication suite. Neither should be mistaken for modern certificate-based mutual authentication. Prefer EAP-TLS where the environment supports managed certificates.

## Exam traps

- LDAP = directory access; Kerberos = ticket-based authentication; RADIUS/TACACS+ = AAA; SAML/OIDC = federation/SSO; OAuth = delegated authorization.
- TGT ≠ service ticket.
- HOTP uses a counter; TOTP uses time.
- MFA requires different factor categories, not merely two credentials.
- EAP is a framework; PEAP is an EAP method/tunneled method.
- SAML assertion / OIDC ID Token convey authentication claims; OAuth access token authorizes API/resource access.

## Supplementary concepts — not in the official acronym appendix
These items are added for technical understanding and are not entries in CompTIA’s acronym appendix. Some may still support exam-objective topics; absence from the appendix does **not** mean “out of scope.” Treat items explicitly described as legacy or optional as additional depth.

- **OIDC** — OpenID Connect.
- **JWT** — JSON Web Token; compact claims representation, commonly signed (JWS) or encrypted (JWE). A JWT is not automatically encrypted.
- **PKCE** — Proof Key for Code Exchange; protects OAuth authorization-code flows, especially public clients.
- **FIDO2/WebAuthn** — phishing-resistant public-key authentication using origin-bound credentials.
- **SP / IdP** — Service Provider / Identity Provider in federation.

## Technical references

- [RFC 4120 — Kerberos V5](https://www.rfc-editor.org/rfc/rfc4120)
- [RFC 4511 — LDAP](https://www.rfc-editor.org/rfc/rfc4511)
- [RFC 9700 — OAuth 2.0 Security Best Current Practice](https://www.rfc-editor.org/rfc/rfc9700)
- [OpenID Connect specifications](https://openid.net/developers/specs/)
- [OASIS SAML 2.0](https://www.oasis-open.org/standard/saml/)

## Official acronym coverage

The following entries are preserved from the CompTIA SY0-701 acronym appendix. The third column explains the technical role and highlights useful distinctions. An acronym can have different meanings in different domains; read the expansion and the surrounding context together.


| Acronym | Official expansion (CompTIA) | Description / technical role |
|---|---|---|
| `CHAP` | Challenge Handshake Authentication Protocol | Challenge-response authentication; compare PAP, which transmits the password directly at protocol level. |
| `EAP` | Extensible Authentication Protocol | Authentication framework carrying methods; PEAP and EAP-TLS are methods within the EAP family. |
| `FRR` | False Rejection Rate | Biometric false-rejection rate: legitimate users incorrectly denied; compare with FAR, false acceptance rate. |
| `HOTP` | HMAC-based One-time Password | Counter-based one-time password; TOTP is time-based. |
| `KDC` | Key Distribution Center | Kerberos trusted service that issues tickets and helps establish session keys. |
| `LDAP` | Lightweight Directory Access Protocol | Protocol for querying/updating directory services; not itself a VPN or a RADIUS replacement. |
| `LEAP` | Lightweight Extensible Authentication Protocol | Legacy Cisco EAP method with known weaknesses; not to be confused with modern EAP-TLS. |
| `MFA` | Multifactor Authentication | Uses at least two different factor categories: knowledge, possession or inherence. |
| `MSCHAP` | Microsoft Challenge Handshake Authentication Protocol | Microsoft challenge-response method often used inside PEAP; distinct from NTLM, which is a Windows network authentication suite. |
| `NTLM` | New Technology LAN Manager | Legacy Windows challenge-response authentication; distinct from MS-CHAP used in PPP/network access and PEAP inner authentication. |
| `OAUTH` | Open Authorization | Delegated authorization framework allowing scoped access tokens; OpenID Connect adds an authentication/identity layer. |
| `PAM` | Pluggable Authentication Modules | Linux/Unix authentication framework through which applications load configurable modules; distinct from Privileged Access Management. |
| `PAP` | Password Authentication Protocol | Sends password credentials without its own encryption; protect it inside a secure tunnel. |
| `PEAP` | Protected Extensible Authentication Protocol | EAP method: TLS tunnel using server certificate, then inner authentication; unlike EAP-TLS, client certificate is not always required. |
| `PED` | Personal Electronic Device | Personal electronic device; a broad device category, not an authentication protocol. |
| `PIV` | Personal Identity Verification | US federal smart-card identity credential standard; supports strong certificate-based authentication. |
| `RADIUS` | Remote Authentication Dial-in User Service | Central AAA service commonly used with 802.1X/EAP; not itself an EAP authentication method. |
| `SAML` | Security Assertions Markup Language | XML-based federation standard exchanging signed authentication/authorization assertions between identity and service providers. |
| `SSO` | Single Sign-on | One authentication event grants access to multiple trusted services; federation often uses SAML or OIDC. |
| `TACACS+` | Terminal Access Controller Access Control System | AAA protocol commonly used for network-device administration; TCP and separates AAA functions. |
| `TGT` | Ticket Granting Ticket | Kerberos ticket used to request service tickets without re-entering the password. |
| `TOTP` | Time-based One-time Password | Time-based one-time password; HOTP advances using a counter. |

---

**Study rule:** learn the technical distinction in the explanation above, then use the official acronym list as a recognition checklist. Do not memorize an acronym expansion as a substitute for understanding the mechanism.


---


# PARTIE IV — Symmetric encryption, hashes and cryptographic modes

> **Scope:** Symmetric cryptography and cryptographic integrity mechanisms: block and stream ciphers, AES, DES, 3DES, cipher modes, initialization vectors, nonces, hashing algorithms, HMAC, salting, password hashing, key stretching, and key derivation. Focus on cryptographic properties, key and nonce requirements, algorithm selection, and common implementation weaknesses.

## 1. Symmetric cryptography

A symmetric cipher uses the same secret key (or a trivially related key pair) to encrypt and decrypt. It is efficient for bulk data, but both parties need a secure way to obtain and protect the key. AES is the modern standard in this list; AES-256 refers to AES with a 256-bit key, not a different cipher family. DES, 3DES (supplementary), and RC4 are legacy algorithms and should not be selected for new secure designs.

Block ciphers process fixed-size blocks. A **mode of operation** defines how the cipher handles multiple blocks and whether it provides integrity:

- **ECB** encrypts each block independently. Equal plaintext blocks produce equal ciphertext blocks under the same key, revealing patterns. Avoid for general data encryption.
- **CBC** chains each plaintext block with the previous ciphertext block and uses an IV for the first block. It requires correct padding and is malleable without separate authentication; padding-oracle risks arise from distinguishable errors.
- **CFB** turns a block cipher into a self-synchronizing stream-like mode.
- **CTR/CTM** uses a counter to generate a keystream; it supports parallelism but nonce/counter reuse with the same key is catastrophic.
- **GCM** is an AEAD mode: it provides confidentiality and integrity/authenticity through an authentication tag. Nonce uniqueness is critical.

**AEAD** (Authenticated Encryption with Associated Data) is the modern design goal: encrypt the payload and authenticate it, while optionally authenticating unencrypted metadata (associated data). GCM and CCM are examples. Never treat encryption without authentication as sufficient protection against active tampering.

## 2. IVs, nonces, and key reuse

An Initialization Vector or nonce is a value used to ensure encryption does not repeat the same internal state for repeated messages. It is often not secret, but its uniqueness or unpredictability requirement depends on the mode. For AES-GCM and CTR, nonce reuse with the same key can expose plaintext relationships and undermine authentication. For CBC, IV requirements differ. “Random IV” is not a universal substitute for understanding the mode's exact requirements.

## 3. Hashing vs integrity/authentication

A cryptographic hash maps arbitrary-length input to a fixed-length digest. SHA-256/SHA-384/SHA-512 are common SHA-2 members. MD5 and SHA-1 are unsuitable where collision resistance is required. Hashing is one-way in normal use; it is not encryption and has no decryption key.

- **Hash**: detects changes only if the expected digest is trusted.
- **HMAC**: combines a hash function with a shared secret; verifies message integrity and that the sender knows the secret.
- **Digital signature**: uses a private key to sign and a public key to verify; supports integrity and origin authentication, and can support non-repudiation subject to key control and legal context.
- **CRC**: detects accidental transmission/storage errors; it is not cryptographically secure and does not stop a malicious attacker.

## 4. Password storage and key derivation

Passwords should not be stored as plaintext or as fast general-purpose hashes alone. **PBKDF2** applies a password-based derivation process with salt and configurable iteration count to slow guessing. Modern alternatives include Argon2id, scrypt, and bcrypt. A unique random salt prevents precomputed rainbow-table reuse and makes identical passwords produce different stored hashes. A pepper is an additional secret kept separately from the password database.

## Technical clarification: hash, HMAC, CRC, salt and password KDFs

- A **cryptographic hash** maps input to a fixed-size digest. It has no secret key; anyone can calculate it. It can detect modification only when the expected digest is obtained from a trusted source.
- **HMAC** combines a cryptographic hash with a shared secret. It authenticates message integrity to parties that know the key; it does not encrypt the message and does not provide non-repudiation.
- **CRC** is designed to detect accidental transmission/storage errors, not malicious tampering. An attacker can alter data and recompute the CRC.
- A **salt** is a unique random value stored alongside a password verifier. It prevents identical passwords from producing identical hashes and frustrates precomputed rainbow tables; it is not a secret.
- **PBKDF2** applies a password-based key derivation process with a salt and configurable iteration count. Its purpose is to make each password guess more expensive, not to make a weak password strong.

**Authenticated encryption:** ECB, CBC, CFB and ordinary CTR provide confidentiality modes but do not by themselves authenticate ciphertext. GCM is an authenticated-encryption mode (AEAD). CCMP uses AES-CCM and adds integrity/authentication and replay protection for Wi-Fi data. Never reuse a nonce/IV where the chosen mode requires uniqueness (especially CTR/GCM).

**Exam comparison:** hash = unkeyed digest; HMAC = keyed integrity/authentication; CRC = non-cryptographic error detection; encryption = confidentiality; digital signature = asymmetric integrity plus signer authentication.

## Exam traps

- AES is a cipher; GCM/CBC/CTR are modes.
- ECB leaks patterns; CBC needs correct IV/padding and separate integrity; GCM is authenticated encryption.
- Hashing ≠ encryption; CRC ≠ secure hash; HMAC ≠ digital signature.
- Salts are not secrets and should be unique; peppers are secret and stored separately.
- Reusing a GCM nonce with the same key is a critical failure.

## Supplementary concepts — not in the official acronym appendix
These items are added for technical understanding and are not entries in CompTIA’s acronym appendix. Some may still support exam-objective topics; absence from the appendix does **not** mean “out of scope.” Treat items explicitly described as legacy or optional as additional depth.

- **AEAD** — Authenticated Encryption with Associated Data.
- **CCM** — Counter with CBC-MAC, another AEAD mode used in wireless/security protocols.
- **Argon2id / scrypt / bcrypt** — password hashing/KDF alternatives designed to resist guessing, with different resource-hardness properties.
- **KDF** — Key Derivation Function; derives cryptographic keys from input key material.
- **Salt / pepper** — per-password public random value / separately protected secret value.

## Technical references

- [NIST FIPS 197 — AES](https://csrc.nist.gov/pubs/fips/197/final)
- [NIST SP 800-38D — GCM](https://csrc.nist.gov/pubs/sp/800/38/d/final)
- [NIST SP 800-132 — Password-Based Key Derivation](https://csrc.nist.gov/pubs/sp/800/132/final)
- [RFC 2104 — HMAC](https://www.rfc-editor.org/rfc/rfc2104)
- [OWASP Password Storage Cheat Sheet](https://cheatsheetseries.owasp.org/cheatsheets/Password_Storage_Cheat_Sheet.html)

## Official acronym coverage

The following entries are preserved from the CompTIA SY0-701 acronym appendix. The third column explains the technical role and highlights useful distinctions. An acronym can have different meanings in different domains; read the expansion and the surrounding context together.


| Acronym | Official expansion (CompTIA) | Description / technical role |
|---|---|---|
| `AES` | Advanced Encryption Standard | Modern symmetric block cipher with 128-bit blocks and 128/192/256-bit keys. |
| `AES-256` | Advanced Encryption Standards 256-bit | AES using a 256-bit key; the AES block size remains 128 bits. |
| `CBC` | Cipher Block Chaining | Chains blocks using prior ciphertext and an IV; confidentiality mode only, no built-in authentication. |
| `CCMP` | Counter Mode/CBC-MAC Protocol | Wi-Fi protection using AES-CCM for confidentiality, integrity and replay protection; stronger than legacy TKIP. |
| `CFB` | Cipher Feedback | Block-cipher mode operating in a stream-like feedback manner; does not itself authenticate data. |
| `CRC` | Cyclical Redundancy Check | Detects accidental errors, not malicious modification; compare HMAC or digital signatures for security integrity. |
| `CTM` | Counter Mode | CompTIA's appendix says Counter Mode; standard technical shorthand is CTR. A nonce/counter must not be reused with the same key. |
| `DES` | Digital Encryption Standard | Obsolete symmetric block cipher with an inadequate 56-bit effective key. |
| `ECB` | Electronic Code Book | Encrypts blocks independently and leaks repeated patterns; avoid for structured data. |
| `GCM` | Galois Counter Mode | Authenticated-encryption mode providing confidentiality and integrity/authentication when nonce use is correct. |
| `HMAC` | Hashed Message Authentication Code | Hash plus shared secret for integrity/authentication; unlike a plain hash it is keyed, and unlike encryption it hides no data. |
| `IDEA` | International Data Encryption Algorithm | Historical 64-bit-block symmetric cipher with 128-bit key, notably associated with older PGP use. |
| `IV` | Initialization Vector | Initialization value used by a cryptographic mode; uniqueness/unpredictability requirements depend on the mode. |
| `MAC` | Message Authentication Code | Message Authentication Code: keyed tag for integrity/authentication; distinct from access-control and network-interface meanings. |
| `MD5` | Message Digest 5 | Legacy 128-bit hash with broken collision resistance; not suitable for security-sensitive integrity. |
| `PBKDF2` | Password-based Key Derivation Function 2 | Password KDF using salt and iterations to increase guessing cost; compare ordinary fast hashes such as SHA/MD5. |
| `RC4` | Rivest Cipher version 4 | Legacy stream cipher with statistical weaknesses; deprecated and unsafe for modern protection. |
| `RIPEMD` | RACE Integrity Primitives Evaluation Message Digest | Family of cryptographic hash functions; RIPEMD-160 is historical and less commonly deployed than SHA-2/3. |
| `SHA` | Secure Hashing Algorithm | Cryptographic hash family; use SHA-2/SHA-3 rather than SHA-1 for collision-resistant security. |
| `TKIP` | Temporal Key Integrity Protocol | Legacy WPA transitional protocol; deprecated and weaker than AES-CCMP. |
| `XOR` | Exclusive Or | Bitwise exclusive-OR; fundamental operation in ciphers and checksums, not encryption by itself. |

---

**Study rule:** learn the technical distinction in the explanation above, then use the official acronym list as a recognition checklist. Do not memorize an acronym expansion as a substitute for understanding the mechanism.


---


# PARTIE V — Asymmetric cryptography, certificates and PKI

> **Scope:** Public-key cryptography and digital trust infrastructure: asymmetric key pairs, RSA, ECC, digital signatures, key exchange, public key infrastructure, certificate authorities, certificate chains, certificate validation, revocation mechanisms, key escrow, hardware security modules, trusted platform modules, and certificate lifecycle management. Focus on identity binding, authenticity, integrity, confidentiality, and trust establishment.

## 1. Public-key cryptography: two different jobs

Asymmetric cryptography uses a mathematically related public/private key pair. The public key may be distributed; the private key must remain controlled by its owner.

- **Encryption for confidentiality**: encrypt with the recipient's public key; only the corresponding private key can decrypt. In practice, protocols use hybrid encryption: public-key cryptography establishes or protects a symmetric session key, and symmetric encryption protects bulk data.
- **Digital signature**: sign with the sender's private key; verify with the sender's public key. This supports integrity and authentication of the signing key. Non-repudiation depends on private-key control, identity proofing, process, and legal context; it is not guaranteed by mathematics alone.

RSA supports encryption (with appropriate padding schemes) and signatures. DSA/ECDSA are signature algorithms, not general-purpose encryption algorithms. ECC provides security based on elliptic-curve discrete-log problems and can achieve comparable security with smaller keys than classic RSA. ECDH/ECDHE establish shared secrets; ECDSA signs. Ephemeral Diffie-Hellman (DHE/ECDHE) creates temporary key material and supports forward secrecy when correctly used.

## 2. Key exchange and Perfect Forward Secrecy

Diffie-Hellman allows two parties to derive a shared secret over an observed channel; it does not authenticate the parties by itself. An active attacker can perform a man-in-the-middle attack unless the exchange is authenticated (for example, by certificates/signatures or a pre-shared key).

**Ephemeral** means fresh temporary key material is generated for a session. With ephemeral DHE/ECDHE, compromise of the server's long-term private key later should not reveal previously captured session traffic, assuming ephemeral secrets were erased and the protocol was implemented correctly. This property is Perfect Forward Secrecy (PFS).

## 3. PKI and certificate lifecycle

A Public Key Infrastructure binds identities to public keys through certificates and trusted issuers:

1. A subject generates a key pair and creates a **CSR** containing its public key and requested identity/attributes.
2. A **Registration Authority (RA)** may validate identity and approve the request.
3. A **Certificate Authority (CA)** signs and issues the certificate.
4. Relying parties validate the chain to a trusted root, check names/usage/validity, and check revocation status where required.
5. The certificate is renewed, revoked, or expires; private keys are protected and rotated.

A certificate does not contain the subject's private key. It binds identity information to a public key and is signed by an issuer. Trust depends on the relying party's trust store, correct chain building, hostname/SAN validation, key usage, validity period, and revocation policy.

**CRL** is a periodically published list of revoked certificates. **OCSP** checks certificate status through a responder. CRLs can be larger and less current; OCSP can provide fresher status but introduces responder availability/privacy considerations. OCSP stapling lets the server provide a signed status response during the TLS handshake.

**SAN (Subject Alternative Name)** contains identities a certificate is valid for, such as DNS names and IP addresses. Modern TLS hostname validation relies on SAN; do not assume the Common Name alone is sufficient.

## 4. Key protection and packaging

An **HSM** is tamper-resistant hardware for generating, storing, and using cryptographic keys, often designed so private keys cannot be exported in plaintext. A **KEK** encrypts/protects other keys (key wrapping); it is distinct from a data-encryption key. PKCS standards define cryptographic message, key, and certificate formats. PKCS #12/P12 commonly packages a private key with its certificate chain in a password-protected file; protect it as sensitive key material. PEM is a Base64-encoded textual container format, not an encryption algorithm.

## Technical clarification: certificate validation in practice

A certificate is a signed binding between an identity (for example, a DNS name) and a public key. It does **not** contain the subject's private key.

A client validating a TLS certificate should check at least:

1. **Chain of trust:** the leaf certificate chains through valid intermediate CA certificates to a trusted root CA in the trust store.
2. **Identity:** the requested hostname must match a name in the certificate's **SAN** extension. Do not rely only on the legacy Common Name.
3. **Validity and purpose:** current time is within the validity period, and key usage / extended key usage permit the intended operation.
4. **Signature and algorithms:** certificate signatures and public-key parameters meet policy.
5. **Revocation status:** check revocation using **OCSP** or a **CRL**, subject to the client's policy and availability.

A **CSR** is a request sent to a CA; it normally contains the applicant's public key and requested identity attributes, and is signed using the corresponding private key. The private key stays with the applicant. A **P12/PFX** file can bundle a private key and certificates; **PEM** is a textual encoding/container convention and is not encryption by itself.

## Exam traps

- Public-key encryption for recipient confidentiality vs private-key signing for sender authenticity/integrity.
- ECDSA/DSA sign; ECDHE/DHE establishes a shared secret (it does not authenticate without an additional mechanism).
- CA vs RA: the RA verifies identity; the CA issues the certificate; CSR requests a certificate.
- CRL vs OCSP: a list of revoked certificates versus an online status query.
- PKCS vs P12: PKCS is the standards family; PKCS #12 is one member of that family.
- P12 vs PEM: a cryptographic package/container versus a text-based encoding.
- Certificate contains public key, not private key; SAN identifies valid hostnames.
- PGP vs GPG: PGP is the cryptographic system/product family; GPG is an open-source implementation.

## Supplementary concepts — not in the official acronym appendix
These items are added for technical understanding and are not entries in CompTIA’s acronym appendix. Some may still support exam-objective topics; absence from the appendix does **not** mean “out of scope.” Treat items explicitly described as legacy or optional as additional depth.

- **JWS/JWE/JWK** — JSON Web Signature / Encryption / Key; formats used in token ecosystems.
- **OCSP stapling** — server supplies a signed certificate-status response.
- **Root CA / intermediate CA** — trust anchor and subordinate issuing CA in a certificate chain.
- **Key escrow** — controlled recovery arrangement for keys; creates governance and insider-risk concerns.

## Technical references

- [NIST SP 800-57 — Key Management](https://csrc.nist.gov/pubs/sp/800/57/pt1/r5/final)
- [RFC 5280 — X.509 PKI Certificate and CRL Profile](https://www.rfc-editor.org/rfc/rfc5280)
- [RFC 6960 — OCSP](https://www.rfc-editor.org/rfc/rfc6960)
- [RFC 8446 — TLS 1.3](https://www.rfc-editor.org/rfc/rfc8446)
- [NIST FIPS 186-5 — Digital Signature Standard](https://csrc.nist.gov/pubs/fips/186-5/final)

## Official acronym coverage

The following entries are preserved from the CompTIA SY0-701 acronym appendix. The third column explains the technical role and highlights useful distinctions. An acronym can have different meanings in different domains; read the expansion and the surrounding context together.


| Acronym | Official expansion (CompTIA) | Description / technical role |
|---|---|---|
| `CA` | Certificate Authority | Certificate Authority signs certificates and establishes trust chains; RA typically verifies applicant identity. |
| `CRL` | Certificate Revocation List | Published revocation list; OCSP queries status for an individual certificate. |
| `CSR` | Certificate Signing Request | Certificate request containing a public key and identity details; the corresponding private key stays with requester. |
| `DHE` | Diffie-Hellman Ephemeral | Ephemeral Diffie–Hellman key exchange; can provide forward secrecy when ephemeral secrets are discarded. |
| `DSA` | Digital Signature Algorithm | Digital signature algorithm; signature only, not encryption or key exchange. |
| `ECC` | Elliptic Curve Cryptography | Cryptography using elliptic-curve groups; enables compact keys for key exchange and signatures. |
| `ECDHE` | Elliptic Curve Diffie-Hellman Ephemeral | Elliptic-curve ephemeral Diffie–Hellman; key exchange with forward secrecy, not a signature algorithm. |
| `ECDSA` | Elliptic Curve Digital Signature Algorithm | Elliptic-curve digital signatures; does not encrypt data or establish a shared session key. |
| `GPG` | Gnu Privacy Guard | GNU Privacy Guard, an OpenPGP implementation for encryption, signatures and key management. |
| `HSM` | Hardware Security Module | Tamper-resistant hardware for cryptographic key generation, storage and operations. |
| `KEK` | Key Encryption Key | Key Encryption Key used to wrap/protect another key, such as a data-encryption key. |
| `OCSP` | Online Certificate Status Protocol | Online status query for a certificate; CRL is a published list of revoked certificates. |
| `P12` | PKCS #12 | PKCS #12 container often bundling private key and certificates; protect it with a strong password. |
| `PEM` | Privacy Enhanced Mail | Base64 text encoding/container with boundary labels; PEM encoding does not automatically encrypt private keys. |
| `PFS` | Perfect Forward Secrecy | Protects past sessions from later long-term-key compromise when ephemeral key exchange is used. |
| `PGP` | Pretty Good Privacy | Pretty Good Privacy; hybrid encryption and digital-signature approach for files/email. |
| `PKCS` | Public Key Cryptography Standards | Family of Public-Key Cryptography Standards defining formats and cryptographic procedures. |
| `PKI` | Public Key Infrastructure | Trust infrastructure of CAs, certificates, policies and revocation; binds identities to public keys. |
| `PSK` | Pre-shared Key | Pre-shared secret configured at both ends; simple but harder to rotate/manage at scale. |
| `RA` | Registration Authority | Registration Authority verifies certificate applicant identity on behalf of a CA; it does not normally sign the certificate. |
| `RSA` | Rivest, Shamir, & Adleman | Public-key algorithm used for encryption/key transport and signatures; security depends on key size and correct padding. |
| `SAN` | Subject Alternative Name | Subject Alternative Name: certificate extension listing DNS names/IP identities; distinct from Storage Area Network (SAN) in infrastructure. |
| `SCEP` | Simple Certificate Enrollment Protocol | Protocol automating certificate enrollment between devices and a CA; it does not itself act as a CA. |

---

**Study rule:** learn the technical distinction in the explanation above, then use the official acronym list as a recognition checklist. Do not memorize an acronym expansion as a substitute for understanding the mechanism.


---


# PARTIE VI — Network architecture, addressing and infrastructure

> **Scope:** Network architecture and infrastructure fundamentals: network topologies, addressing, subnetting, routing, switching, network segmentation, security zones, VLANs, DMZs, network isolation, network appliances, and infrastructure placement. Focus on how network design determines traffic flow, connectivity, exposure, segmentation boundaries, and the overall attack surface.

## 1. Network architecture and segmentation

A network is built from endpoints, switches, routers, firewalls, wireless access points, and services. A **switch** forwards frames within a Layer 2 network using MAC addresses; a **router** forwards IP packets between Layer 3 networks using routing tables. A VLAN creates a logical Layer 2 broadcast domain; inter-VLAN communication requires Layer 3 routing and should be filtered by policy.

Segmentation reduces lateral movement and limits blast radius. A common design separates user workstations, servers, management interfaces, guest Wi-Fi, payment systems, and OT/ICS. A VLAN alone is not a security boundary if routing between VLANs is unrestricted. Use firewall/ACL policy at Layer 3/4 and identity-aware controls where appropriate.

**DMZ** is a network segment for services exposed to less-trusted networks (e.g., public web/reverse proxy). It should not be a flat extension of the internal LAN. A compromise of a DMZ host should not automatically grant access to internal systems.

## 2. Addressing and network services

IPv4 uses 32-bit addresses; IPv6 uses 128-bit addresses. CIDR notation expresses a prefix length (e.g., /24), and subnetting divides address space into networks. VLSM allows subnets of different sizes. The default gateway is the router next hop used to reach off-subnet destinations.

DHCP dynamically leases IP configuration (address, mask/prefix, gateway, DNS). DNS resolves names to records/addresses. ARP resolves an IPv4 address to a link-layer MAC address on the local network; IPv6 uses Neighbor Discovery (NDP), not ARP. ARP has no native authentication, so spoofing/poisoning can redirect local traffic.

NAT rewrites addresses; PAT also multiplexes many internal hosts through one public address using transport-layer ports. DNAT changes the destination (common for publishing an internal service); SNAT changes the source (common for outbound connections). NAT is not a firewall by itself and should not be treated as a security control.

## 3. Routing and switching protocols

BGP exchanges routing information between autonomous systems and is central to Internet routing; route hijacking/leaks can redirect traffic. OSPF is an interior gateway link-state routing protocol used within an autonomous system. BPDU is a Spanning Tree Protocol control message used to prevent Layer 2 loops. Rogue/forged BPDUs can manipulate topology; BPDU Guard and Root Guard are switch protections in appropriate designs.

MPLS forwards traffic using labels and is used in provider WANs; it is not encryption. GRE encapsulates packets to create tunnels but provides no encryption/authentication by itself. RTBH (Remotely Triggered Black Hole) can discard traffic to a target route during DDoS mitigation, but may also discard legitimate traffic to that destination.

## 4. Network performance and physical infrastructure

MTU is the maximum Layer 3 packet size supported by a link without fragmentation at that layer; mismatches can cause path-MTU problems. CSU/DSU and IDF/MDF refer to carrier/telecom and building distribution infrastructure. UTP is unshielded twisted-pair cabling; SFP/GBIC are transceiver form factors (hardware list context). A UPS supplies temporary power during outages; redundant power and network paths reduce single points of failure.

## Exam traps

- Switch = MAC/frame/L2; router = IP/packet/L3.
- VLAN segmentation does not enforce inter-VLAN policy by itself.
- ARP is IPv4 local-link resolution; NDP serves corresponding IPv6 functions.
- NAT/PAT translate; they do not provide encryption or full firewall inspection.
- GRE/MPLS do not inherently encrypt payloads; use IPsec/TLS where confidentiality is required.
- BGP is inter-domain; OSPF is typically intra-domain.

## Supplementary concepts — not in the official acronym appendix
These items are added for technical understanding and are not entries in CompTIA’s acronym appendix. Some may still support exam-objective topics; absence from the appendix does **not** mean “out of scope.” Treat items explicitly described as legacy or optional as additional depth.

- **NDP** — IPv6 Neighbor Discovery Protocol.
- **CIDR** — Classless Inter-Domain Routing.
- **SDN** — Software-Defined Networking; separates control plane from forwarding/data plane.
- **VXLAN** — Layer 2 overlay over Layer 3 underlay, often used in data centers.
- **SASE** — Secure Access Service Edge; converges network and security services delivered from cloud edges.

## Technical references

- [RFC 1918 — Private IPv4 Address Allocation](https://www.rfc-editor.org/rfc/rfc1918)
- [RFC 8200 — IPv6](https://www.rfc-editor.org/rfc/rfc8200)
- [RFC 4861 — IPv6 Neighbor Discovery](https://www.rfc-editor.org/rfc/rfc4861)
- [RFC 4271 — BGP-4](https://www.rfc-editor.org/rfc/rfc4271)
- [RFC 2328 — OSPFv2](https://www.rfc-editor.org/rfc/rfc2328)

## Official acronym coverage

The following entries are preserved from the CompTIA SY0-701 acronym appendix. The third column explains the technical role and highlights useful distinctions. An acronym can have different meanings in different domains; read the expansion and the surrounding context together.


| Acronym | Official expansion (CompTIA) | Description / technical role |
|---|---|---|
| `AP` | Access Point | Wireless access point bridging wireless clients to a wired network. |
| `ARP` | Address Resolution Protocol | Maps IPv4 addresses to local MAC addresses; spoofing can enable traffic interception. |
| `BGP` | Border Gateway Protocol | Inter-domain routing between autonomous systems; route leaks/hijacks can redirect traffic. |
| `BPDU` | Bridge Protocol Data Unit | Spanning Tree Protocol control frame used by switches to prevent Layer-2 loops. |
| `CSU` | Channel Service Unit | Telecommunications interface device connecting customer equipment to a digital carrier circuit. |
| `DSL` | Digital Subscriber Line | Broadband technology transmitting data over copper telephone lines. |
| `ESN` | Electronic Serial Number | Electronic device identifier historically used by cellular systems; not a secret authentication factor. |
| `GPS` | Global Positioning System | Satellite-based positioning and timing system; can be jammed or spoofed. |
| `IDF` | Intermediate Distribution Frame | Intermediate network-distribution room connecting local wiring to the main distribution frame. |
| `IEEE` | Institute of Electrical and Electronics Engineers | Standards organization responsible for many networking standards, including Ethernet and Wi-Fi families. |
| `IP` | Internet Protocol | Network-layer protocol providing logical addressing and packet routing. |
| `LAN` | Local Area Network | Network covering a limited local area such as an office or building. |
| `MAC` | Media Access Control | Media Access Control: Layer-2 addressing/access method; MAC address identifies a network interface, not an access policy. |
| `MAN` | Metropolitan Area Network | Network spanning a metropolitan/city area, larger than a LAN and typically smaller than a WAN. |
| `MDF` | Main Distribution Frame | Main building distribution point for telecommunications/network cabling. |
| `MFD` | Multifunction Device | Multifunction device combining functions such as printing, scanning and copying; often needs hardening. |
| `MFP` | Multifunction Printer | Multifunction printer/device; secure print, storage and admin interfaces. |
| `MPLS` | Multi-protocol Label Switching | Provider networking technique forwarding packets using labels rather than only longest-prefix IP lookup. |
| `MTU` | Maximum Transmission Unit | Maximum transmission unit; mismatches can cause fragmentation or connectivity problems. |
| `NAT` | Network Address Translation | Translates IP addresses; not a substitute for firewall policy or authentication. |
| `OSPF` | Open Shortest Path First | Interior link-state routing protocol used within an autonomous system. |
| `P2P` | Peer to Peer | Peer-to-peer model where endpoints communicate/share resources directly rather than only through a central server. |
| `PAC` | Proxy Auto Configuration | Proxy Auto-Configuration file/script telling clients which proxy to use for a URL. |
| `PAT` | Port Address Translation | NAT variant multiplexing many private hosts through one public IP using port numbers. |
| `PBX` | Private Branch Exchange | Private telephone switching system connecting internal extensions and external telephone networks. |
| `PDU` | Power Distribution Unit | Power Distribution Unit supplying electrical power to rack equipment; distinct from protocol data unit in networking. |
| `POTS` | Plain Old Telephone Service | Traditional analog telephone service over copper lines. |
| `RTBH` | Remotely Triggered Black Hole | Routing technique discarding traffic destined for a targeted address to mitigate DDoS, with availability trade-offs. |
| `UAV` | Unmanned Aerial Vehicle | Unmanned aerial vehicle; can create physical, wireless or privacy risks. |
| `UTP` | Unshielded Twisted Pair | Unshielded twisted-pair copper cabling used in Ethernet networks. |
| `VLAN` | Virtual Local Area Network | Logical Layer-2 segmentation; inter-VLAN traffic still needs appropriate controls. |
| `VLSM` | Variable Length Subnet Masking | Variable-length subnet masks allocate different subnet sizes efficiently. |
| `WAP` | Wireless Access Point | Wireless Access Point in this appendix; do not confuse it with historical Wireless Application Protocol. |

---

**Study rule:** learn the technical distinction in the explanation above, then use the official acronym list as a recognition checklist. Do not memorize an acronym expansion as a substitute for understanding the mechanism.


---


# PARTIE VII — Network services, application protocols and messaging

> **Scope:** Network service and application-layer communication protocols: DNS, DHCP, HTTP, HTTPS, SMTP, IMAP, POP3, FTP, SFTP, SSH, SNMP, NTP, LDAP, SIP, and related messaging and service-discovery technologies. Focus on protocol purpose, communication behavior, common ports and transports, security weaknesses, and the consequences of insecure service configuration.

## 1. Application protocols and their security properties

Protocols define message formats, state transitions, and expected behavior. A familiar port number is a clue, not proof that traffic is safe or that the service is correctly configured.

- **HTTP** carries web requests/responses; HTTPS is HTTP protected by TLS. TLS protects the transport channel, but it does not make a vulnerable application secure.
- **DNS** resolves names and supports records such as A/AAAA, MX, TXT, CNAME, and NS. DNS spoofing/cache poisoning can redirect clients; DNSSEC authenticates DNS data origin/integrity but does not encrypt queries.
- **DHCP** provides dynamic network configuration. Rogue DHCP can supply a malicious gateway or DNS server; DHCP snooping on switches can restrict trusted DHCP server ports.
- **NTP** synchronizes clocks. Accurate time is essential for logs, Kerberos, certificates, and incident timelines. NTP spoofing/manipulation can disrupt authentication and forensic correlation.

## 2. Email security: SPF, DKIM, DMARC

Email authentication uses complementary controls:

- **SPF** publishes which sending hosts are authorized to send mail for a domain. It evaluates the envelope/HELO identity, not necessarily the visible From header.
- **DKIM** adds a cryptographic signature to selected message headers/body content. The receiving system retrieves the public key from DNS and verifies the signature.
- **DMARC** aligns the visible From domain with SPF and/or DKIM results and publishes a policy (none, quarantine, reject) plus reporting instructions.

SPF alone does not cryptographically sign the message; DKIM alone does not prove that the visible From address is aligned; DMARC ties authentication results to domain alignment and policy. Forwarding can break SPF; DKIM may survive if signed content is not modified. DMARC can pass when either aligned SPF or aligned DKIM passes, depending on policy configuration.

## 3. File transfer, mail access, and messaging

FTP sends credentials/data without encryption. FTPS adds TLS to FTP; SFTP is file transfer over SSH and is a different protocol from FTP. SCP also uses SSH for file copy. Do not assume SFTP is “FTP with SSL.”

SMTP sends/relays email; IMAP synchronizes/accesses messages on a server; POP typically downloads messages. SMTPS or SMTP submission with STARTTLS protects the connection when correctly configured. IMAP/POP also require TLS (commonly IMAPS/POP3S or STARTTLS).

SNMP monitors/manages network devices. SNMPv1/v2c use community strings and lack modern cryptographic protection; SNMPv3 adds authentication, integrity, and privacy (encryption) options. SOAP is an XML-based web-service messaging protocol; REST is an architectural style, not an acronym in the official list.

## 4. Remote management and voice/media protocols

SSH provides encrypted remote shell and tunneling; Telnet (supplementary) is plaintext and should not be used for sensitive administration. RDP provides remote desktop access and should be restricted, patched, protected with MFA/NLA/VPN or zero-trust access, and monitored. SIP commonly establishes/controls VoIP sessions; RTP carries real-time media; SRTP protects RTP media. RTCP provides quality/control feedback and is not the same as RTP payload transport.

## Exam traps

- SFTP ≠ FTPS. SFTP runs over SSH; FTPS is FTP protected by TLS.
- SPF authorizes senders; DKIM signs; DMARC enforces alignment/policy and reporting.
- DNSSEC authenticates DNS data; DoH/DoT encrypt DNS transport. These solve different problems.
- SNMPv3 is the secure choice; v1/v2c community strings are not equivalent protection.
- TLS protects data in transit, not application logic or stored data.

## Supplementary concepts — not in the official acronym appendix
These items are added for technical understanding and are not entries in CompTIA’s acronym appendix. Some may still support exam-objective topics; absence from the appendix does **not** mean “out of scope.” Treat items explicitly described as legacy or optional as additional depth.

- **DNSSEC** — DNS Security Extensions.
- **DoH / DoT** — DNS over HTTPS / DNS over TLS.
- **MTA-STS / DANE** — mechanisms that strengthen TLS use for SMTP delivery.
- **STARTTLS** — upgrades an existing plaintext-capable protocol connection to TLS; downgrade/misconfiguration risks must be considered.
- **SIP / RTP / SRTP** — session signaling / media transport / secure media transport.

## Technical references

- [RFC 8446 — TLS 1.3](https://www.rfc-editor.org/rfc/rfc8446)
- [RFC 6376 — DKIM](https://www.rfc-editor.org/rfc/rfc6376)
- [RFC 7208 — SPF](https://www.rfc-editor.org/rfc/rfc7208)
- [RFC 7489 — DMARC](https://www.rfc-editor.org/rfc/rfc7489)
- [RFC 3414 — SNMPv3 User-based Security Model](https://www.rfc-editor.org/rfc/rfc3414)

## Official acronym coverage

The following entries are preserved from the CompTIA SY0-701 acronym appendix. The third column explains the technical role and highlights useful distinctions. An acronym can have different meanings in different domains; read the expansion and the surrounding context together.


| Acronym | Official expansion (CompTIA) | Description / technical role |
|---|---|---|
| `DHCP` | Dynamic Host Configuration Protocol | Leases IP configuration automatically; rogue DHCP can supply malicious gateway/DNS settings. |
| `DKIM` | DomainKeys Identified Mail | Cryptographic email-domain signature; SPF checks sender infrastructure and DMARC applies alignment policy. |
| `DMARC` | Domain Message Authentication Reporting and Conformance | Email authentication policy/reporting aligning SPF/DKIM with visible From domain. |
| `DNAT` | Destination Network Address Translation | Changes destination IP/port, commonly to publish an internal service through a firewall/router. |
| `DNS` | Domain Name System | Resolves names to records; poisoning or malicious records can redirect traffic. |
| `FTP` | File Transfer Protocol | Traditional file-transfer protocol without built-in encryption; credentials/data can be exposed. |
| `FTPS` | Secured File Transfer Protocol | FTP protected with TLS; distinct from SFTP, which runs over SSH. |
| `HTTP` | Hypertext Transfer Protocol | Web request/response protocol; HTTPS adds TLS protection. |
| `HTTPS` | Hypertext Transfer Protocol Secure | HTTP over TLS; protects transport but does not guarantee site legitimacy. |
| `ICMP` | Internet Control Message Protocol | Network control/diagnostic messages, including reachability and error reporting. |
| `IM` | Instant Messaging | Instant messaging; content and metadata require appropriate transport and endpoint protection. |
| `IMAP` | Internet Message Access Protocol | Email access protocol synchronizing messages/folders on a server. |
| `IRC` | Internet Relay Chat | Text-based real-time chat protocol; can be abused for command-and-control. |
| `ISP` | Internet Service Provider | Organization providing Internet connectivity and related services. |
| `MMS` | Multimedia Message Service | Mobile multimedia messaging service. |
| `NTP` | Network Time Protocol | Synchronizes system clocks; accurate time is essential for logs, certificates and Kerberos. |
| `OTA` | Over the Air | Over-the-air delivery of updates/configuration; secure signing and validation are critical. |
| `PCAP` | Packet Capture | Packet-capture file/data used for network troubleshooting and forensic analysis. |
| `POP` | Post Office Protocol | Email retrieval protocol, traditionally downloads messages to a client. |
| `RTP` | Real-time Transport Protocol | Real-time media transport; SRTP adds encryption/authentication. |
| `SMTP` | Simple Mail Transfer Protocol | Protocol for sending/relaying email between clients and mail servers. |
| `SMTPS` | Simple Mail Transfer Protocol Secure | SMTP protected with TLS; STARTTLS upgrades a connection, while implicit TLS starts protected. |
| `SNMP` | Simple Network Management Protocol | Network monitoring/management protocol; prefer SNMPv3 with authentication and encryption. |
| `SOAP` | Simple Object Access Protocol | XML-based web-service messaging protocol, often using HTTP and WS-* standards. |
| `SPF` | Sender Policy Framework | DNS policy listing authorized mail senders; DKIM signs messages and DMARC aligns/enforces results. |
| `TSIG` | Transaction Signature | Shared-secret message authentication for DNS transactions/updates. |
| `URI` | Uniform Resource Identifier | Uniform Resource Identifier; broader category that includes URLs. |
| `URL` | Universal Resource Locator | Uniform Resource Locator identifying where/how to access a resource; commonly treated as a URI subtype. |
| `VoIP` | Voice over IP | Voice communication transported over IP networks. |
| `VTC` | Video Teleconferencing | Video teleconferencing system; secure signaling, media and endpoints. |

---

**Study rule:** learn the technical distinction in the explanation above, then use the official acronym list as a recognition checklist. Do not memorize an acronym expansion as a substitute for understanding the mechanism.


---


# PARTIE VIII — Secure communications, remote access and wireless

> **Scope:** Secure network communication and wireless access technologies: TLS, IPsec, VPN architectures, tunneling, remote-access solutions, secure wireless configurations, WPA2/WPA3, enterprise wireless authentication, 802.1X, wireless monitoring, Bluetooth, NFC, and RFID security considerations. Focus on protecting data in transit, authenticating network access, and reducing exposure across wired, wireless, and remote connections.

## 1. Secure transport: TLS, IPsec, and legacy protocols

TLS protects application traffic between endpoints and is used by HTTPS, secure email, APIs, and many other services. TLS 1.3 uses an authenticated key exchange and modern AEAD cipher suites; SSL is obsolete, and older TLS versions/cipher suites should be evaluated against current policy. A valid certificate does not prove that a website is trustworthy in every sense; it proves a cryptographic binding between a name and a key under a trust chain, subject to validation.

IPsec protects IP-layer traffic. **AH** provides integrity, origin authentication, and anti-replay but not confidentiality. **ESP** can provide confidentiality and, when configured with authenticated encryption or integrity mechanisms, integrity/authentication. IKE negotiates security associations and keys. IPsec tunnel mode commonly protects traffic between gateways; transport mode protects the IP payload between hosts. NAT traversal may encapsulate IPsec ESP in UDP.

L2TP creates a tunnel but does not encrypt by itself; it is commonly paired with IPsec. PPTP is obsolete and insecure. GRE also encapsulates but does not encrypt. A VPN label alone does not tell you which cryptographic protections are present—identify the protocol stack.

## 2. Remote access architecture

A remote-access server (RAS) or VPN concentrator terminates remote sessions. Use strong authentication (MFA/certificates), device posture checks, least-privilege routes, logging, patching, and restricted management access. Split tunneling sends only selected traffic through the VPN; full tunneling sends all client traffic through the organization. Split tunneling can reduce bandwidth but may allow simultaneous access to untrusted networks and increase exposure.

Zero Trust Network Access (ZTNA, supplementary) grants application-specific access based on identity, device, context, and policy rather than implicitly trusting an entire network because a VPN tunnel exists. VPNs remain useful, but network connectivity should not equal unrestricted trust.

## 3. Wireless security generations

- **WEP** is broken; static/shared-key RC4-based design and weak IV handling make it insecure.
- **WPA** was an interim improvement; TKIP is legacy and deprecated.
- **WPA2** commonly uses AES-CCMP; enterprise mode uses 802.1X/EAP with RADIUS, while personal mode uses a PSK.
- **WPA3-Personal** uses SAE (Simultaneous Authentication of Equals) instead of the traditional WPA2-PSK handshake, improving resistance to offline dictionary attacks. WPA3-Enterprise strengthens enterprise security requirements.

CCMP combines counter-mode encryption with CBC-MAC authentication. TKIP was designed as a transitional fix for older hardware and should not be treated as modern strong encryption. WPS (Wi-Fi Protected Setup) can weaken network security if exposed or poorly implemented; disable it when not needed.

## 4. Wireless monitoring and access points

A WAP/AP bridges wireless clients to a wired network. A rogue AP is unauthorized; an evil twin imitates a legitimate SSID to trick clients. WIDS detects wireless threats; WIPS can actively contain/block them. Wireless containment must be used carefully because it can disrupt legitimate devices and may be legally constrained.

NFC and RFID enable short-range identification/communication; security depends on protocol, distance, authentication, cryptography, and application design—not merely the physical range. Bluetooth is also a wireless attack surface (pairing abuse, insecure profiles, device discovery).

## Technical clarification: TLS, IPsec and their component protocols

**TLS** protects application transport sessions (for example, HTTPS). **IPsec** protects IP traffic at the network layer and is commonly used for site-to-site or remote-access VPNs. A VPN is a deployment/use case, not one single cryptographic protocol.

Within IPsec:
- **IKE/IKEv2** authenticates peers, negotiates algorithms and establishes Security Associations (SAs) and keys.
- **AH** provides integrity, data-origin authentication and anti-replay, but no confidentiality; it is often impractical where NAT is involved.
- **ESP** can provide confidentiality and can also provide integrity/authentication and anti-replay. It is the commonly deployed IPsec protection protocol.

**TLS vs SSL:** SSL is obsolete and insecure; modern deployments use TLS. **WTLS** is a legacy WAP-era wireless protocol, not a modern alternative to TLS. **SAE** belongs to WPA3-Personal Wi-Fi authentication, not IPsec or RADIUS.

## Exam traps

- AH ≠ ESP: AH does not encrypt; ESP can.
- L2TP/GRE are tunneling/encapsulation mechanisms, not encryption by themselves.
- WEP/TKIP are legacy; WPA2-CCMP and WPA3-SAE are stronger modern choices.
- SAE is associated with WPA3-Personal; it is not the same as a RADIUS server.
- WIDS detects; WIPS can prevent/contain.
- VPN access is not automatically zero trust or least privilege.

## Supplementary concepts — not in the official acronym appendix
These items are added for technical understanding and are not entries in CompTIA’s acronym appendix. Some may still support exam-objective topics; absence from the appendix does **not** mean “out of scope.” Treat items explicitly described as legacy or optional as additional depth.

- **ZTNA** — Zero Trust Network Access.
- **802.1X** — port-based network access control framework commonly used with EAP/RADIUS.
- **SAE** — password-authenticated key exchange used by WPA3-Personal.
- **EAP-TLS** — certificate-based EAP method providing mutual authentication when correctly configured.
- **MFA** — add a second factor to remote access; prefer phishing-resistant methods where feasible.

## Technical references

- [RFC 8446 — TLS 1.3](https://www.rfc-editor.org/rfc/rfc8446)
- [RFC 4301 — IPsec Architecture](https://www.rfc-editor.org/rfc/rfc4301)
- [RFC 7296 — IKEv2](https://www.rfc-editor.org/rfc/rfc7296)
- [IEEE 802.11 working group](https://www.ieee802.org/11/)
- [Wi-Fi Alliance — WPA3](https://www.wi-fi.org/discover-wi-fi/security)

## Official acronym coverage

The following entries are preserved from the CompTIA SY0-701 acronym appendix. The third column explains the technical role and highlights useful distinctions. An acronym can have different meanings in different domains; read the expansion and the surrounding context together.


| Acronym | Official expansion (CompTIA) | Description / technical role |
|---|---|---|
| `AH` | Authentication Header | IPsec integrity/authentication and anti-replay without confidentiality; compare ESP, which can encrypt payloads. |
| `ESP` | Encapsulated Security Payload | IPsec payload protection supporting confidentiality and integrity/authentication; compare AH, which does not encrypt. |
| `GRE` | Generic Routing Encapsulation | Encapsulation/tunneling only; no built-in confidentiality or authentication. |
| `IKE` | Internet Key Exchange | Negotiates IPsec peers, algorithms, keys and Security Associations; AH/ESP protect the resulting traffic. |
| `IPSec` | Internet Protocol Security | Network-layer IP protection suite; IKE negotiates, AH authenticates, and ESP can encrypt. |
| `L2TP` | Layer 2 Tunneling Protocol | Tunneling protocol without native encryption; commonly combined with IPsec. |
| `PPP` | Point-to-Point Protocol | Point-to-point link protocol supporting framing and optional authentication. |
| `PPTP` | Point-to-Point Tunneling Protocol | Legacy VPN tunneling protocol with weak security; avoid for modern deployments. |
| `RAS` | Remote Access Server | Remote Access Server providing remote connectivity, often VPN/dial-in. |
| `RDP` | Remote Desktop Protocol | Microsoft remote desktop protocol; restrict exposure and enforce MFA/NLA. |
| `S/MIME` | Secure/Multipurpose Internet Mail Extensions | Email security standard using certificates for signing and encryption. |
| `SAE` | Simultaneous Authentication of Equals | WPA3-Personal password-authenticated key exchange; not a RADIUS server or an IPsec protocol. |
| `SFTP` | Secured File Transfer Protocol | File transfer over SSH; distinct from FTPS (FTP over TLS) and plaintext FTP. |
| `SHTTP` | Secure Hypertext Transfer Protocol | Historical Secure HTTP protocol; not the same as HTTPS and rarely used. |
| `SMS` | Short Message Service | Short text messaging service; vulnerable to interception/SIM-swap and weak as MFA. |
| `SRTP` | Secure Real-Time Protocol | Secure RTP adding confidentiality, message authentication and replay protection to media streams. |
| `SSH` | Secure Shell | Secure remote shell and tunneling protocol; supports key-based authentication. |
| `SSL` | Secure Sockets Layer | Obsolete predecessor to TLS; do not enable SSL versions in modern systems. |
| `TCP/IP` | Transmission Control Protocol/Internet Protocol | Internet protocol suite; TCP provides reliable ordered transport, IP routes packets. |
| `TLS` | Transport Layer Security | Modern transport-security protocol; SSL is its obsolete predecessor. HTTPS is HTTP protected by TLS. |
| `UDP` | User Datagram Protocol | Connectionless transport with low overhead; reliability must be provided by application if needed. |
| `VPN` | Virtual Private Network | Encrypted/authenticated tunnel over untrusted networks; VPN connectivity does not imply zero-trust authorization. |
| `WEP` | Wired Equivalent Privacy | Broken legacy Wi-Fi security; avoid due to RC4/IV weaknesses. |
| `WPA` | Wi-Fi Protected Access | Wi-Fi security family; WPA2-CCMP and WPA3-SAE supersede original WPA/TKIP. |
| `WPS` | Wi-Fi Protected Setup | Wi-Fi enrollment convenience feature; PIN weaknesses can expose wireless networks. |
| `WTLS` | Wireless TLS | Legacy WAP-era wireless TLS variant; obsolete and distinct from modern TLS. |

---

**Study rule:** learn the technical distinction in the explanation above, then use the official acronym list as a recognition checklist. Do not memorize an acronym expansion as a substitute for understanding the mechanism.


---


# PARTIE IX — Threat actors, threat intelligence and reconnaissance

> **Scope:** Adversary profiling and intelligence-driven security: threat-actor categories, motivations, resources, capabilities, reconnaissance, OSINT, attack attribution limitations, indicators of compromise, tactics, techniques and procedures, threat-intelligence sources, and structured intelligence-sharing frameworks. Focus on understanding adversary behavior and translating intelligence into defensive priorities.

## 1. Threat actors: capability, motivation, and resources

Classify threat actors by **who they are, what motivates them, what access they have, and what resources they can sustain**. Common categories include nation-state/APT groups, cybercriminals, hacktivists, insiders, competitors, and unskilled attackers. These labels describe likely capability/motivation, not a guaranteed behavior.

An **APT** is characterized by sustained, adaptive, targeted activity and persistence. “Advanced” does not necessarily mean novel zero-days in every operation; an APT may use stolen credentials, living-off-the-land tools, and legitimate remote-management utilities. The important clue is long-term targeted access and operational patience.

Insiders may be malicious, negligent, or compromised. An employee account used by an external attacker can create insider-like access without the employee being malicious. Controls include least privilege, separation of duties, behavioral monitoring, access reviews, and rapid offboarding.

## 2. Threat intelligence and the intelligence cycle

Threat intelligence turns raw observations into decision-support. A useful cycle is direction/requirements → collection → processing → analysis → dissemination → feedback. Intelligence should be relevant to the organization's assets, sector, exposure, and threat model.

**IoCs** are observable artifacts or behaviors associated with compromise: malicious IP/domain, file hash, registry key, process tree, unusual authentication, or command-and-control pattern. IoCs are often time-sensitive and can be changed by attackers. A single IP/hash is not a complete attribution or proof of compromise; correlate with context and behavior.

**TTPs** describe adversary tactics, techniques, and procedures—the behavior and methods used across operations. TTPs are generally more durable than individual IoCs. MITRE ATT&CK organizes adversary behaviors into tactics, techniques, sub-techniques, and procedures; it is a knowledge base, not a scanner or a threat actor attribution oracle.

OSINT collects information from publicly available sources. It can support attack-surface discovery, exposure analysis, and investigations. Public availability does not automatically mean information is accurate, current, or lawful to use in every context.

## 3. Sharing formats and automation

STIX represents cyber threat intelligence in a structured, machine-readable format. TAXII is a protocol for exchanging that information. AIS is an automated indicator-sharing initiative/program context. PCAP is packet-capture data, not a threat-intelligence standard. Distinguish a content model (STIX), transport/exchange protocol (TAXII), and raw evidence (PCAP/logs).

## Exam traps

- APT = targeted, persistent campaign; not simply “any advanced malware.”
- IoC = observable indicator; TTP = behavior/method. TTPs usually outlast individual IoCs.
- OSINT = publicly available information collection; not necessarily social-media-only.
- STIX structures threat information; TAXII transports/exchanges it.
- Attribution is a confidence-based analytic judgment, not a conclusion from one IP address.

## Supplementary concepts — not in the official acronym appendix
These items are added for technical understanding and are not entries in CompTIA’s acronym appendix. Some may still support exam-objective topics; absence from the appendix does **not** mean “out of scope.” Treat items explicitly described as legacy or optional as additional depth.

- **TLP** — Traffic Light Protocol; labels sharing/dissemination restrictions for information.
- **ATT&CK Navigator** — tool to visualize/map techniques and coverage; not the ATT&CK knowledge base itself.
- **YARA** — rule language for identifying patterns in files/malware samples.
- **Sigma** — generic rule format for describing SIEM/log detections.
- **IOC enrichment** — adding reputation, passive DNS, WHOIS, sandbox, and telemetry context to an indicator.

## Technical references

- [MITRE ATT&CK](https://attack.mitre.org/)
- [OASIS STIX](https://oasis-open.github.io/cti-documentation/)
- [OASIS TAXII](https://oasis-open.github.io/cti-documentation/)
- [FIRST Traffic Light Protocol](https://www.first.org/tlp/)
- [CISA Automated Indicator Sharing](https://www.cisa.gov/topics/cyber-threats-and-advisories/information-sharing)

## Official acronym coverage

The following entries are preserved from the CompTIA SY0-701 acronym appendix. The third column explains the technical role and highlights useful distinctions. An acronym can have different meanings in different domains; read the expansion and the surrounding context together.


| Acronym | Official expansion (CompTIA) | Description / technical role |
|---|---|---|
| `AIS` | Automated Indicator Sharing | Automated sharing of threat indicators between organizations/platforms. |
| `APT` | Advanced Persistent Threat | Well-resourced, persistent adversary conducting sustained targeted operations. |
| `ATT&CK` | Adversarial Tactics, Techniques, and Common Knowledge | Knowledge base mapping adversary tactics and techniques to observed behavior and defensive coverage. |
| `CERT` | Computer Emergency Response Team | Computer emergency response team; coordinates vulnerability/incident handling. |
| `CIRT` | Computer Incident Response Team | Incident-response team; IR is the activity/capability and IRP is the documented plan. |
| `IoC` | Indicators of Compromise | Observable artifact suggesting compromise, such as a hash, domain or IP; context and freshness matter. |
| `OSINT` | Open-source Intelligence | Intelligence gathered from publicly available sources; validate reliability and provenance. |
| `TTP` | Tactics, Techniques, and Procedures | Adversary tactics, techniques and procedures describing behavior beyond single indicators. |

---

**Study rule:** learn the technical distinction in the explanation above, then use the official acronym list as a recognition checklist. Do not memorize an acronym expansion as a substitute for understanding the mechanism.


---


# PARTIE X — Vulnerabilities, malware and exploit mitigation

> **Scope:** Vulnerability analysis and system-level risk reduction: software, operating-system, hardware, firmware, cloud, mobile, virtualization, and supply-chain weaknesses; vulnerability scanning; CVE and CVSS; malware classifications; exploitability; patch management; secure configuration; hardening; and mitigation techniques. Focus on identifying weaknesses, assessing their severity, prioritizing remediation, and verifying that corrective controls are effective.

## 1. Vulnerability management lifecycle

A vulnerability is a weakness that could be exploited; a threat is a potential cause of harm; risk combines likelihood and impact in a given context. A vulnerability scanner identifies potential weaknesses, but results require validation and prioritization. A patch fixes known software defects; configuration hardening reduces attack surface; compensating controls reduce risk when immediate remediation is not possible.

**CVE** identifies a publicly disclosed vulnerability record; it is not a severity score. **CVSS** assigns a standardized severity score based on metrics such as attack vector, complexity, privileges required, user interaction, and impact. A high CVSS score does not automatically mean highest organizational priority: exposure, exploit availability, asset criticality, compensating controls, and threat activity matter.

**OVAL** is a language for expressing and evaluating system configuration/vulnerability state. **SCAP** is a suite/framework of specifications for automating security configuration, vulnerability, and compliance assessment. A scanner may consume OVAL/SCAP content; the acronyms are not interchangeable with CVE/CVSS.

## 2. Malware and execution behavior

- **Virus** attaches to a host file/program and typically requires execution of that host.
- **Worm** self-propagates across systems/networks without needing a host file in the same way.
- **Trojan** disguises malicious functionality as legitimate software; it does not inherently self-replicate.
- **RAT** gives remote control/access to a compromised system; the acronym can also mean Remote Access Trojan.
- **Ransomware** encrypts or otherwise denies access to data/systems and demands payment; modern campaigns may also exfiltrate data (double extortion).
- **Rootkit** hides malicious presence and may operate at kernel/boot/firmware levels.
- **PUP** is potentially unwanted software; not every PUP is malware, but it may introduce privacy, performance, or security risk.

**AV** traditionally uses signatures, heuristics, and behavior monitoring. EDR adds endpoint telemetry, detection, investigation, and response capabilities. No single tool guarantees prevention; defense-in-depth and timely patching remain necessary.

## 3. Exploit mitigation and memory protections

**ASLR** randomizes memory locations so attackers cannot reliably predict addresses. **DEP/NX** marks memory regions non-executable, making it harder to execute injected code from data pages. Stack canaries, control-flow integrity, sandboxing, and least privilege add layers. These controls raise exploit difficulty but do not eliminate memory-corruption vulnerabilities.

A buffer overflow occurs when data exceeds a buffer's bounds and corrupts adjacent memory. Integer overflow/wraparound can cause incorrect size calculations and under-allocation. Use bounds checking, safe libraries, compiler protections, memory-safe languages, and fuzz testing.

## 4. Prioritization and remediation

Prioritize exposed, exploitable, business-critical assets first. Consider internet reachability, exploit-in-the-wild evidence, asset function, data sensitivity, privilege required, and lateral-movement potential. Validate scanner findings; false positives and missing credentials can distort results. Track remediation SLAs and verify the fix with rescanning or testing.

## Technical clarification: CVE, CVSS, CWE, OVAL and SCAP

These labels answer different questions:

- **CVE**: which publicly disclosed vulnerability is being referenced? It is an identifier/record, not a severity score.
- **CVSS**: how severe is the vulnerability according to a standardized technical scoring model? It does not by itself establish business risk or exploitation probability.
- **CWE**: what class of software/hardware weakness is involved (for example, buffer errors or improper input validation)? A CWE weakness can contribute to many CVEs.
- **OVAL**: how can a machine-readable check describe/evaluate whether a system has a particular configuration or vulnerability state?
- **SCAP**: what standards suite can automate security configuration, vulnerability assessment and compliance reporting?

**Prioritization rule:** combine severity with asset criticality, exposure, exploit availability/known exploitation, business impact and compensating controls. A lower CVSS finding on an internet-facing critical system may deserve attention before a higher-scoring issue on an isolated test machine.

## Exam traps

- CVE = identifier; CVSS = severity scoring system.
- Vulnerability scan ≠ penetration test: scanning identifies likely weaknesses; a penetration test attempts controlled exploitation to demonstrate impact.
- Virus vs worm vs Trojan vs RAT are behavior distinctions, not interchangeable labels.
- ASLR randomizes locations; DEP/NX prevents execution from non-executable pages.
- Patching closes known flaws; hardening reduces exposure; compensating control reduces risk when patching is delayed.

## Supplementary concepts — not in the official acronym appendix
These items are added for technical understanding and are not entries in CompTIA’s acronym appendix. Some may still support exam-objective topics; absence from the appendix does **not** mean “out of scope.” Treat items explicitly described as legacy or optional as additional depth.

- **KEV** — Known Exploited Vulnerabilities catalog (CISA); useful prioritization signal.
- **EPSS** — Exploit Prediction Scoring System; estimates probability of exploitation in the wild.
- **SAST/DAST/SCA** — static code analysis / dynamic application testing / software composition analysis.
- **Fuzzing** — automated generation/mutation of inputs to discover crashes and unexpected behavior.
- **CWE** — Common Weakness Enumeration; weakness classes, distinct from CVE vulnerability instances.

## Technical references

- [CVE Program](https://www.cve.org/)
- [FIRST CVSS v4.0](https://www.first.org/cvss/)
- [CISA Known Exploited Vulnerabilities Catalog](https://www.cisa.gov/known-exploited-vulnerabilities-catalog)
- [CISA Secure by Design](https://www.cisa.gov/securebydesign)
- [MITRE CWE](https://cwe.mitre.org/)

## Official acronym coverage

The following entries are preserved from the CompTIA SY0-701 acronym appendix. The third column explains the technical role and highlights useful distinctions. An acronym can have different meanings in different domains; read the expansion and the surrounding context together.


| Acronym | Official expansion (CompTIA) | Description / technical role |
|---|---|---|
| `ASLR` | Address Space Layout Randomization | Randomizes memory addresses to make exploitation less predictable; DEP/NX blocks execution from data pages. |
| `AV` | Antivirus | Antivirus/anti-malware controls using signatures, heuristics and behavior detection. |
| `CVE` | Common Vulnerability Enumeration | Identifier for a disclosed vulnerability; compare CVSS (severity score) and CWE (weakness category). |
| `CVSS` | Common Vulnerability Scoring System | Standardized vulnerability severity score; compare CVE (identifier) and EPSS (estimated exploitation probability, supplementary). |
| `DEP` | Data Execution Prevention | Marks data memory non-executable; ASLR randomizes addresses, so the protections are complementary. |
| `DLL` | Dynamic Link Library | Windows shared library loaded by processes; DLL search-order hijacking is a security risk. |
| `OVAL` | Open Vulnerability Assessment Language | Machine-readable language for checking configuration/vulnerability state; SCAP is the broader automation standards suite. |
| `PUP` | Potentially Unwanted Program | Potentially unwanted program; may be unwanted/risky without meeting malware definition. |
| `RAT` | Remote Access Trojan | Remote Access Trojan gives an attacker remote control; the same acronym can also mean legitimate Remote Administration Tool. |
| `SEH` | Structured Exception Handler | Windows exception-handling mechanism; older exploitation techniques target SEH structures. |
| `TOC` | Time-of-check | Time-of-check: moment a program checks a condition/resource state. |
| `TOU` | Time-of-use | Time-of-use: later moment resource is used; TOCTOU race exists if state changes between check and use. |

---

**Study rule:** learn the technical distinction in the explanation above, then use the official acronym list as a recognition checklist. Do not memorize an acronym expansion as a substitute for understanding the mechanism.


---


# PARTIE XI — Attack techniques and application-layer attacks

> **Scope:** Attack methods, exploitation techniques, and malicious-activity indicators: denial-of-service, DDoS, DNS attacks, credential attacks, replay attacks, privilege escalation, injection, SQL injection, cross-site scripting, directory traversal, buffer overflow exploitation, race conditions, and suspicious system or network behavior. Focus on understanding attack execution, identifying observable indicators, and connecting each technique to its potential security impact.

## 1. Denial of Service and resource exhaustion

A DoS attempts to make a service unavailable; a DDoS uses many distributed sources, often compromised devices in a botnet. Volumetric attacks exhaust bandwidth; protocol attacks exhaust connection/state tables; application-layer attacks exhaust CPU, memory, threads, or expensive application functions. Mitigations include upstream scrubbing, rate limiting, CDN/Anycast distribution, connection limits, caching, WAF rules, and resilient capacity.

A remotely triggered black hole (RTBH) can discard traffic to a targeted route during an attack. It protects the wider network but may intentionally make the targeted destination unreachable. Sinkholing is different: malicious traffic is redirected to a controlled destination for analysis/containment.

## 2. Injection and browser attacks

**SQL injection (SQLi)** occurs when untrusted input changes the structure/meaning of a database query. The primary defense is parameterized queries/prepared statements, with least-privilege database accounts and safe ORM usage. Input validation is useful but should not replace parameterization.

**Cross-site scripting (XSS)** injects attacker-controlled script/content into a page viewed by another user. Stored XSS persists server-side; reflected XSS is returned in a response; DOM-based XSS arises from unsafe client-side DOM handling. Context-aware output encoding, safe templating, sanitization where HTML is intentionally accepted, and Content Security Policy (CSP) reduce risk. HttpOnly cookies limit JavaScript access to cookies but do not fix XSS.

**CSRF/XSRF** tricks a victim's authenticated browser into submitting an unwanted request to a site where the victim is already logged in. Defenses include anti-CSRF tokens, SameSite cookies, origin/referrer validation, and re-authentication for sensitive actions. CSRF exploits ambient authority (browser-sent credentials); it is not the same as stealing a password.

## 3. Related web weaknesses

- **SSRF** (supplementary) makes a server send requests to unintended destinations, potentially internal metadata endpoints.
- **Directory traversal** manipulates file paths to access files outside the intended directory.
- **Command injection** causes untrusted input to be interpreted by an OS shell or command processor.
- **Deserialization attacks** exploit unsafe reconstruction of untrusted serialized objects.
- **Clickjacking** frames a trusted site to trick users into clicking hidden/overlaid controls.

## 4. Time-of-check/time-of-use

TOC/TOU issues occur when a condition is checked and then changes before the resource is used. Example: an application checks a file's permissions/path, but an attacker swaps a symlink or file between the check and the open operation. Mitigate with atomic operations, file-descriptor-based checks, safe APIs, locking, and avoiding trust in mutable pathnames.

## Exam traps

- SQLi changes a database query; XSS executes attacker-controlled script in a victim's browser; CSRF abuses a victim's authenticated browser to perform an unwanted action.
- XSS is generally client-side execution; SQLi targets database query construction.
- CSRF does not require stealing the session token if the browser automatically sends credentials.
- DDoS is distributed; a DoS need not be.
- Parameterized queries are the primary SQLi defense; output encoding is central to XSS prevention.

## Supplementary concepts — not in the official acronym appendix
These items are added for technical understanding and are not entries in CompTIA’s acronym appendix. Some may still support exam-objective topics; absence from the appendix does **not** mean “out of scope.” Treat items explicitly described as legacy or optional as additional depth.

- **CSP** — Content Security Policy; browser-enforced restrictions on allowed content/script sources.
- **SameSite** — cookie attribute controlling cross-site cookie sending behavior.
- **SSRF** — Server-Side Request Forgery.
- **SRI** — Subresource Integrity; browser verifies fetched resource hashes.
- **WAF** — Web Application Firewall; filters HTTP(S) traffic but is not a substitute for secure coding.

## Technical references

- [OWASP SQL Injection Prevention](https://cheatsheetseries.owasp.org/cheatsheets/SQL_Injection_Prevention_Cheat_Sheet.html)
- [OWASP XSS Prevention](https://cheatsheetseries.owasp.org/cheatsheets/Cross_Site_Scripting_Prevention_Cheat_Sheet.html)
- [OWASP CSRF Prevention](https://cheatsheetseries.owasp.org/cheatsheets/Cross-Site_Request_Forgery_Prevention_Cheat_Sheet.html)
- [OWASP Injection Prevention](https://cheatsheetseries.owasp.org/cheatsheets/Injection_Prevention_Cheat_Sheet.html)

## Official acronym coverage

The following entries are preserved from the CompTIA SY0-701 acronym appendix. The third column explains the technical role and highlights useful distinctions. An acronym can have different meanings in different domains; read the expansion and the surrounding context together.


| Acronym | Official expansion (CompTIA) | Description / technical role |
|---|---|---|
| `CSRF` | Cross-site Request Forgery | Tricks a logged-in browser into sending an unwanted request; anti-CSRF tokens and SameSite help defend. |
| `DDoS` | Distributed Denial of Service | Distributed resource-exhaustion/service disruption; filtering and attribution are harder than single-source DoS. |
| `DoS` | Denial of Service | Disrupts availability from one or limited sources; DDoS distributes the attack across many sources. |
| `ML` | Machine Learning | Machine learning; security uses include anomaly detection, classification and automated analysis. |
| `SPIM` | Spam over Internet Messaging | Unsolicited spam sent through instant-messaging systems. |
| `SQLi` | SQL Injection | SQL injection changes query structure through untrusted input; parameterized queries are primary defense. |
| `XSRF` | Cross-site Request Forgery | Tricks a logged-in browser into sending an unwanted request; anti-CSRF tokens and SameSite help defend. |
| `XSS` | Cross-site Scripting | Injects script/content into pages viewed by users; stored, reflected and DOM-based variants. |

---

**Study rule:** learn the technical distinction in the explanation above, then use the official acronym list as a recognition checklist. Do not memorize an acronym expansion as a substitute for understanding the mechanism.


---


# PARTIE XII — Security monitoring, detection and defensive platforms

> **Scope:** Security monitoring and enterprise detection capabilities: IDS, IPS, SIEM, SOAR, EDR, XDR, NDR, DLP, CASB, SOC operations, security telemetry, log collection, event correlation, alert prioritization, automated response, and managed security services. Focus on how security technologies collect evidence, identify suspicious activity, generate alerts, and support defensive operations.

## 1. Detection architecture: IDS, IPS, HIDS, NIDS

An **IDS** detects suspicious activity and generates alerts. An **IPS** is positioned to block or prevent traffic/actions, often inline. A **NIDS/NIPS** monitors or enforces at network level; a **HIDS/HIPS** operates on an individual host and can observe local logs, files, processes, and system events. Inline prevention can stop attacks but introduces availability risk if misconfigured or overloaded; passive detection is less disruptive but cannot block by itself.

Detection methods include signature-based detection (known patterns), anomaly-based detection (deviation from baseline), and behavior/heuristic analysis. Signature detection is precise for known patterns but misses novel variants; anomaly detection can find unknown behavior but often produces false positives.

## 2. SIEM vs SOAR vs SOC

A **SIEM** centralizes logs/events, normalizes and correlates them, applies detection rules, and supports investigation/reporting. It is only as useful as its log sources, parsing, time synchronization, retention, detection engineering, and analyst process. A SIEM is not automatically an incident-response team.

**SOAR** orchestrates workflows and automates repeatable response tasks: enrich an alert, open a ticket, disable an account, isolate an endpoint, or notify stakeholders. Playbooks need safeguards, approval gates, error handling, and rollback procedures. SOAR commonly integrates with SIEM, EDR, threat-intelligence feeds, ticketing, and identity platforms.

A **SOC** is the people/process/technology function responsible for monitoring, triage, detection, and coordination. A SIEM is a platform; a SOC is an operational team/function.

## 3. Endpoint detection and response

**EDR** collects endpoint telemetry (process creation, command lines, network connections, file changes, registry events, authentication) and supports investigation and response such as process termination or host isolation. **XDR** correlates telemetry across multiple domains (endpoint, identity, email, cloud, network). **MDR** is a managed service in which an external provider supplies monitoring/response expertise. EDR/XDR describe technology scope; MDR describes a service model.

HIDS/FIM may detect file/configuration changes; EDR generally offers broader behavioral telemetry and response. Antivirus focuses more traditionally on malware prevention/detection, though modern products overlap.

## 4. DLP, CASB, SWG and monitoring services

**DLP** detects/prevents sensitive-data leakage using content inspection, labels, fingerprints, context, and policy. Enforcement may occur at endpoint, network, email, or cloud. False positives and encrypted traffic inspection are operational challenges.

**CASB** provides visibility/control between users and cloud services (discovery, data protection, threat protection, compliance). **SWG** filters web traffic and enforces acceptable-use/malware controls. They overlap but are not identical: CASB is cloud-service-centric; SWG is web-access-centric. MaaS is a service delivery model for monitoring; distinguish it from the actual detection platform.

## Technical clarification: detection and response platforms

- **IDS vs IPS:** IDS observes and alerts; IPS can block inline. A false positive in an IPS can interrupt legitimate traffic.
- **HIDS/NIDS:** the first observes an individual host; the second observes network traffic at a sensor/monitoring point. **HIPS/NIPS** add prevention/blocking capability at the corresponding level.
- **SIEM vs SOAR vs SOC:** SIEM collects, normalizes and correlates events; SOAR coordinates/automates response playbooks; SOC is the people/process/technology function operating detection and response.
- **EDR vs XDR vs MDR:** EDR focuses on endpoint telemetry and response; XDR correlates several security domains; MDR is a managed service delivered by an external provider. The first two describe technology capabilities, the last describes service delivery.
- **DLP vs CASB vs SWG:** DLP focuses on sensitive-data movement; CASB governs use of cloud services; SWG filters web access. Products can overlap, but the primary control objective differs.

## Exam traps

- IDS detects/alerts; IPS can block inline.
- NIDS/NIPS = network; HIDS/HIPS = host.
- SIEM collects/correlates; SOAR orchestrates/automates; SOC is the operational function.
- EDR endpoint-focused; XDR cross-domain correlation; MDR managed service.
- DLP protects data; CASB governs cloud-service usage; SWG secures web access.

## Supplementary concepts — not in the official acronym appendix
These items are added for technical understanding and are not entries in CompTIA’s acronym appendix. Some may still support exam-objective topics; absence from the appendix does **not** mean “out of scope.” Treat items explicitly described as legacy or optional as additional depth.

- **UEBA** — User and Entity Behavior Analytics; detects anomalous behavior relative to baselines.
- **NDR** — Network Detection and Response; network-traffic analytics and response.
- **MITRE ATT&CK mapping** — maps detections/telemetry to adversary techniques to identify coverage gaps.
- **Sigma** — portable detection-rule format for log events.
- **MSSP** — Managed Security Service Provider; external security operations provider (related to but not identical to MDR).

## Technical references

- [NIST SP 800-94 — Intrusion Detection and Prevention Systems](https://csrc.nist.gov/pubs/sp/800/94/final)
- [MITRE ATT&CK](https://attack.mitre.org/)
- [CISA Logging Made Easy](https://www.cisa.gov/resources-tools/services/logging-made-easy)
- [NIST SP 800-92 — Log Management](https://csrc.nist.gov/pubs/sp/800/92/final)

## Official acronym coverage

The following entries are preserved from the CompTIA SY0-701 acronym appendix. The third column explains the technical role and highlights useful distinctions. An acronym can have different meanings in different domains; read the expansion and the surrounding context together.


| Acronym | Official expansion (CompTIA) | Description / technical role |
|---|---|---|
| `DLP` | Data Loss Prevention | Detects/prevents sensitive data leakage using content, context and policy controls. |
| `EDR` | Endpoint Detection and Response | Endpoint telemetry, detection, investigation and response; XDR spans domains, while MDR is a managed service. |
| `HIDS` | Host-based Intrusion Detection System | Host-based detection on an individual system; compare NIDS, which monitors network traffic. |
| `HIPS` | Host-based Intrusion Prevention System | Host-based intrusion prevention blocks or prevents suspicious host activity. |
| `IDS` | Intrusion Detection System | Detects and alerts; compare IPS, which can actively block, often inline. |
| `IPS` | Intrusion Prevention System | Can prevent/block suspicious traffic; compare IDS, which primarily detects and alerts. |
| `MaaS` | Monitoring as a Service | Monitoring delivered as a service by a provider. |
| `MSP` | Managed Service Provider | Managed service provider operating IT services; not necessarily security-specialized. |
| `MSSP` | Managed Security Service Provider | Managed security service provider delivering outsourced security monitoring/operations. |
| `NIDS` | Network-based Intrusion Detection System | Network-based detection at traffic observation points; compare HIDS, which monitors a host. |
| `NIPS` | Network-based Intrusion Prevention System | Inline network IPS can drop/block malicious traffic; may add latency or false-positive risk. |
| `SCAP` | Security Content Automation Protocol | Standards suite for automated configuration/vulnerability assessment; can use OVAL content, but is not a vulnerability identifier. |
| `SIEM` | Security Information and Event Management | Collects, normalizes and correlates logs/events; SOAR automates response workflows and SOC is the team/function. |
| `SOAR` | Security Orchestration, Automation, Response | Automates/orchestrates security workflows and playbooks; SIEM correlates events, while SOC is the operational function. |
| `SOC` | Security Operations Center | Security Operations Center: operational team/function monitoring and responding to security events; distinct from SoC (System on Chip). |
| `WIDS` | Wireless Intrusion Detection System | Monitors wireless spectrum/network for rogue APs and suspicious wireless activity. |
| `WIPS` | Wireless Intrusion Prevention System | Wireless prevention capability that can contain/block unauthorized wireless activity. |
| `XDR` | Extended Detection and Response | Correlates detections across multiple domains; EDR is endpoint-focused and MDR describes an outsourced service. |

---

**Study rule:** learn the technical distinction in the explanation above, then use the official acronym list as a recognition checklist. Do not memorize an acronym expansion as a substitute for understanding the mechanism.


---


# PARTIE XIII — Incident response, investigation and threat data exchange

> **Scope:** Incident response and digital investigation: incident identification, preparation, triage, containment, eradication, recovery, lessons learned, evidence acquisition, chain of custody, forensic analysis, event documentation, response-team coordination, and structured threat-information exchange. Focus on preserving evidence integrity while making timely operational decisions throughout the incident lifecycle.

## 1. Incident response lifecycle

Incident response is a coordinated capability, not simply “remove malware.” A useful operational sequence is preparation → detection/analysis → containment → eradication → recovery → post-incident improvement. Current NIST SP 800-61 Rev. 3 integrates incident response into CSF 2.0 risk management; older course diagrams may show the Rev. 2 lifecycle, so recognize the exam's terminology while understanding the current guidance.

- **Preparation**: roles, playbooks, contact lists, tooling, backups, evidence procedures, tabletop exercises.
- **Detection/analysis**: validate alert, scope affected assets/accounts, determine severity and likely vector.
- **Containment**: limit spread (isolate host, disable account, block indicator, segment network). Preserve evidence where possible.
- **Eradication**: remove persistence, malware, unauthorized accounts, and root cause.
- **Recovery**: restore clean systems, monitor for recurrence, validate business services.
- **Lessons learned**: root cause, control gaps, timeline, metrics, and corrective actions.

Containment choices involve trade-offs. Pulling the plug may stop activity but destroy volatile evidence; network isolation may preserve forensic state. Follow the incident plan and legal/evidence requirements.

## 2. Evidence and investigation

Maintain chain of custody: identify evidence, record who collected/handled it, when, where, how it was stored, and every transfer. Preserve integrity using hashes and write blockers where appropriate. Capture volatile data (memory, active network connections, processes) before shutdown when justified by the plan. Document time zones and clock offsets.

A PCAP records network packets and can support protocol-level analysis. Logs show system/application events. Memory forensics may reveal injected code, credentials, and live processes that disappear after power-off. Evidence collection must be proportionate and authorized.

## 3. CERT, CIRT, IR and IRP

CERT/CIRT are organizational or community response-team labels; exact naming varies. IR is the activity/capability; an IRP is the documented plan defining triggers, roles, escalation, communications, evidence handling, and recovery coordination. A team name is not a response process.

## 4. Threat information exchange

STIX structures cyber threat information; TAXII provides a standardized way to exchange it. IoCs can support blocklists/detection, but should be enriched and time-bounded. Automated sharing without confidence, expiration, provenance, and context can create false positives or operational outages.

## Technical clarification: incident process versus plan versus team

Keep three levels separate: **IR** is the response capability/activity; **IRP** is the documented plan defining roles, triggers, escalation, communications and procedures; **CERT/CIRT** names a response team. A plan does not perform the response, and a team name does not define a complete process.

For threat sharing, **STIX** structures threat information (objects, indicators, relationships and context); **TAXII** provides a protocol/API for exchanging that information. An IoC is an individual observable; STIX can represent it with context, and TAXII can transport it. Sharing an indicator without provenance, confidence, expiration or context can create false positives.

## Exam traps

- Containment limits damage; eradication removes the cause/artifact; recovery restores trusted operations.
- A plan (IRP) defines procedures; a team (CIRT/CERT) executes/co-ordinates them.
- Chain of custody documents evidence control; a hash helps verify evidence integrity but does not prove how it was collected.
- Preserve volatile evidence before shutdown when incident procedures and safety allow.
- STIX = structured content; TAXII = exchange protocol.

## Supplementary concepts — not in the official acronym appendix
These items are added for technical understanding and are not entries in CompTIA’s acronym appendix. Some may still support exam-objective topics; absence from the appendix does **not** mean “out of scope.” Treat items explicitly described as legacy or optional as additional depth.

- **DFIR** — Digital Forensics and Incident Response.
- **SOAR playbook** — repeatable automated workflow with decision points and approval gates.
- **TLP** — sharing classification for threat information.
- **MTTD / MTTR** — mean time to detect / respond or recover; organizations define the exact “R” metric carefully.
- **IOC expiration** — indicators should be reviewed because infrastructure and hashes can become stale.

## Technical references

- [NIST SP 800-61 Rev. 3 (2025)](https://csrc.nist.gov/pubs/sp/800/61/r3/final)
- [NIST SP 800-86 — Integrating Forensic Techniques](https://csrc.nist.gov/pubs/sp/800/86/final)
- [OASIS Cyber Threat Intelligence / STIX / TAXII](https://oasis-open.github.io/cti-documentation/)

## Official acronym coverage

The following entries are preserved from the CompTIA SY0-701 acronym appendix. The third column explains the technical role and highlights useful distinctions. An acronym can have different meanings in different domains; read the expansion and the surrounding context together.


| Acronym | Official expansion (CompTIA) | Description / technical role |
|---|---|---|
| `IR` | Incident Response | Incident-response capability/activity; IRP is the plan and CERT/CIRT names a response team. |
| `IRP` | Incident Response Plan | Documented response plan; IR is the activity and CERT/CIRT is the team. |
| `STIX` | Structured Threat Information eXchange | Structured representation of threat intelligence; TAXII is the transport/exchange protocol commonly used to share it. |
| `TAXII` | Trusted Automated eXchange of Indicator Information | Protocol/API for exchanging threat intelligence; STIX defines structured content that TAXII can transport. |

---

**Study rule:** learn the technical distinction in the explanation above, then use the official acronym list as a recognition checklist. Do not memorize an acronym expansion as a substitute for understanding the mechanism.


---


# PARTIE XIV — Cloud services, cloud security and service models

> **Scope:** Cloud computing architecture and security responsibilities: IaaS, PaaS, SaaS, public, private, hybrid and multi-cloud deployments, shared responsibility, cloud-native services, serverless computing, containers, cloud identity, storage security, network controls, cloud monitoring, and infrastructure as code. Focus on responsibility boundaries, cloud-specific attack surfaces, configuration risks, and the security implications of different deployment models.

## 1. Cloud service models and responsibility

Cloud security questions often test the **shared responsibility model**: the provider secures the underlying cloud infrastructure, while the customer remains responsible for some combination of identity, data, configuration, workloads, and network controls. The exact boundary depends on service model and contract.

- **IaaS**: customer manages guest OS, applications, identities, data, and much of network configuration; provider manages physical facilities, hardware, and virtualization layer.
- **PaaS**: provider manages OS/runtime/platform components; customer manages application code, identities, data, and configuration.
- **SaaS**: provider manages most application infrastructure; customer still manages users, access, data governance, endpoint security, and tenant configuration.

“Cloud provider is responsible for security” is an exam trap. Misconfigured storage, excessive IAM permissions, exposed keys, insecure APIs, and public snapshots are commonly customer-side failures.

## 2. Cloud architecture and controls

A **VPC** is a logically isolated virtual network in a public cloud. Subnets, route tables, security groups, network ACLs, gateways, and private endpoints define connectivity. A private subnet is not automatically safe if outbound routes, identities, or workload permissions are excessive.

**CASB** adds visibility and policy enforcement for cloud-service usage. **CSP** is the cloud service provider; **MSP/MSSP** are managed service/security providers. MaaS is monitoring delivered as a service. Distinguish provider type from the technical control being deployed.

**IaC** defines infrastructure in version-controlled templates/code. It improves repeatability but can replicate insecure configurations at scale. Use code review, secret scanning, policy-as-code, signed artifacts, state protection, and drift detection. Never hardcode cloud credentials in templates or repositories.

## 3. Cloud identity and workload security

Use federated identity, MFA, short-lived credentials, workload identities, least privilege, and conditional access. Prefer role-based temporary credentials over long-lived access keys. Protect metadata services against SSRF and restrict instance roles to the minimum required permissions.

Cloud logging should cover control-plane/API activity, identity events, network flow, workload telemetry, storage access, and configuration changes. Centralize logs in a protected account/project with retention and alerting; attackers who compromise a workload should not be able to erase the only audit trail.

## 4. Availability and resilience

Cloud regions and availability zones support resilience, but multi-zone or multi-region design must be explicitly configured. Backups should be isolated/immutable where appropriate and regularly restore-tested. Autoscaling helps with variable demand but can amplify cost or be abused by denial-of-wallet attacks.

## Exam traps

- IaaS gives the customer more OS/network responsibility than PaaS/SaaS.
- Provider security of the cloud does not equal customer security in the cloud.
- VPC isolation is logical; IAM, routing, security groups, and storage policies still matter.
- IaC improves consistency but can propagate misconfiguration.
- Long-lived access keys are riskier than short-lived, scoped credentials.

## Supplementary concepts — not in the official acronym appendix
These items are added for technical understanding and are not entries in CompTIA’s acronym appendix. Some may still support exam-objective topics; absence from the appendix does **not** mean “out of scope.” Treat items explicitly described as legacy or optional as additional depth.

- **CSPM** — Cloud Security Posture Management; identifies cloud misconfigurations and policy violations.
- **CWPP** — Cloud Workload Protection Platform; protects workloads/compute.
- **CIEM** — Cloud Infrastructure Entitlement Management; analyzes excessive cloud permissions.
- **KMS** — Key Management Service.
- **STS** — Security Token Service; issues temporary credentials/tokens.
- **S3-style object storage** — object store permissions and public-access controls are frequent misconfiguration targets.

## Technical references

- [NIST SP 800-210 — General Access Control Guidance for Cloud Systems](https://csrc.nist.gov/pubs/sp/800/210/final)
- [AWS Shared Responsibility Model](https://aws.amazon.com/compliance/shared-responsibility-model/)
- [Microsoft Shared Responsibility in the Cloud](https://learn.microsoft.com/en-us/azure/security/fundamentals/shared-responsibility)
- [CSA Cloud Controls Matrix](https://cloudsecurityalliance.org/research/cloud-controls-matrix)

## Official acronym coverage

The following entries are preserved from the CompTIA SY0-701 acronym appendix. The third column explains the technical role and highlights useful distinctions. An acronym can have different meanings in different domains; read the expansion and the surrounding context together.


| Acronym | Official expansion (CompTIA) | Description / technical role |
|---|---|---|
| `CASB` | Cloud Access Security Broker | Visibility and policy between users and cloud services; SWG focuses more broadly on web access. |
| `CSP` | Cloud Service Provider | Cloud provider supplying cloud infrastructure/platform/software services. |
| `IaaS` | Infrastructure as a Service | Provider manages physical/virtual infrastructure; customer manages OS, applications, identities and data. |
| `IaC` | Infrastructure as Code | Infrastructure defined in versioned code/templates; repeatability can also replicate insecure settings. |
| `PaaS` | Platform as a Service | Provider manages platform/runtime; customer manages application code, identities and data. |
| `SaaS` | Software as a Service | Provider operates the application; customer still manages identities, data and tenant configuration. |
| `SASE` | Secure Access Service Edge | Cloud-delivered architecture converging networking and security services for users/locations. |
| `SD-WAN` | Software-defined Wide Area Network | Software-controlled WAN overlay selecting paths based on policy/performance. |
| `SWG` | Secure Web Gateway | Secure web gateway filters web access and inspects traffic for policy/malware threats. |
| `VPC` | Virtual Private Cloud | Logically isolated virtual network within a cloud provider. |
| `WAF` | Web Application Firewall | HTTP(S) application-layer firewall; complements secure coding rather than replacing it. |

---

**Study rule:** learn the technical distinction in the explanation above, then use the official acronym list as a recognition checklist. Do not memorize an acronym expansion as a substitute for understanding the mechanism.


---


# PARTIE XV — Systems architecture, virtualization and industrial technology

> **Scope:** Enterprise computing and specialized system architectures: virtualization, hypervisors, virtual machines, containers, embedded systems, firmware, real-time operating systems, ICS, SCADA, industrial networks, hardware security components, high availability, and platform resilience. Focus on isolation boundaries, resource sharing, legacy constraints, operational availability, and the security consequences of running critical or specialized workloads.

## 1. Enterprise architecture and resilience

High availability (HA) aims to keep a service operating through component failure, often with clustering, redundancy, load balancing, and failover. Fault tolerance attempts to continue operation despite a fault, sometimes without interruption. Redundancy is duplication; it only improves resilience if components do not share the same failure domain (power, rack, network path, region, identity provider, or software defect).

RAID improves disk availability/performance depending on level; it is not a backup. RAID 1 mirrors; RAID 5/6 use parity; RAID 10 combines mirroring and striping. A controller failure, ransomware, deletion, or site disaster can still destroy data. Keep independent, tested backups.

## 2. Virtualization and containers

A **VM** virtualizes a full guest operating system on a hypervisor. Type 1 hypervisors run on hardware; Type 2 run on a host OS. **VDI** delivers virtual desktops; VDE is a broader virtual desktop environment concept. Isolation depends on hypervisor hardening, patching, management-plane protection, and segmentation.

Containers share the host kernel and isolate processes/namespaces; they are lighter than VMs but do not provide the same kernel boundary. Secure images, scan dependencies, run as non-root, drop capabilities, use read-only filesystems, and protect orchestration APIs/secrets. A container is not automatically a sandbox.

## 3. Industrial and embedded systems

**OT** includes systems that monitor/control physical processes. **ICS** is a broad category of industrial control systems; **SCADA** supervises geographically distributed processes and telemetry. PLCs, RTUs, HMIs, sensors, and actuators are common components. Availability and safety can outweigh conventional IT patch cadence; changes require testing and operational coordination.

IT and OT differ in priorities and constraints: OT often requires deterministic timing, long equipment lifecycles, legacy protocols, and physical safety. Segment OT from enterprise IT, control remote vendor access, inventory assets, monitor passive network traffic, and plan patches around safety/availability windows.

**RTOS** supports deterministic or bounded response timing; it is not necessarily a safety-certified OS. IoT/embedded devices may have limited memory, weak update support, default credentials, exposed services, and long deployment lifetimes.

## 4. Firmware and hardware trust

BIOS/UEFI initializes hardware and begins the boot process. Secure Boot verifies signatures of boot components against trusted keys, helping prevent unauthorized bootloaders. TPM provides hardware-backed storage/operations for keys and platform measurements; measured boot records boot measurements so a remote/local verifier can assess platform state. A TPM does not automatically encrypt the entire disk; BitLocker or another full-disk encryption system can use TPM-protected key material.

FPGA and SoC are hardware architecture terms. Firmware updates must be authenticated and protected against rollback where supported. A compromised firmware/boot chain can persist below the OS and evade ordinary endpoint tools.

## Exam traps

- RAID ≠ backup; HA ≠ disaster recovery; redundancy must avoid shared failure domains.
- VM includes a guest OS; container shares host kernel.
- OT/ICS/SCADA environments have safety and uptime constraints; do not apply disruptive IT assumptions blindly.
- UEFI Secure Boot verifies boot components; TPM supports hardware-rooted trust/measurements/key protection.
- TPM alone does not mean full-disk encryption is enabled.

## Supplementary concepts — not in the official acronym appendix
These items are added for technical understanding and are not entries in CompTIA’s acronym appendix. Some may still support exam-objective topics; absence from the appendix does **not** mean “out of scope.” Treat items explicitly described as legacy or optional as additional depth.

- **PLC / RTU / HMI** — Programmable Logic Controller / Remote Terminal Unit / Human-Machine Interface.
- **SBOM** — Software Bill of Materials; inventory of software components/dependencies.
- **Measured Boot / Remote Attestation** — records and evaluates platform measurements.
- **Microsegmentation** — fine-grained workload-to-workload access control.
- **Confidential computing** — protects data in use using hardware-backed trusted execution environments.

## Technical references

- [NIST SP 800-82 Rev. 3 — OT Security](https://csrc.nist.gov/pubs/sp/800/82/r3/final)
- [NIST SP 800-193 — Platform Firmware Resiliency](https://csrc.nist.gov/pubs/sp/800/193/final)
- [Trusted Computing Group — TPM](https://trustedcomputinggroup.org/resource/tpm-library-specification/)
- [NIST SP 800-125 — Server Virtualization Security](https://csrc.nist.gov/pubs/sp/800/125/final)

## Official acronym coverage

The following entries are preserved from the CompTIA SY0-701 acronym appendix. The third column explains the technical role and highlights useful distinctions. An acronym can have different meanings in different domains; read the expansion and the surrounding context together.


| Acronym | Official expansion (CompTIA) | Description / technical role |
|---|---|---|
| `BIOS` | Basic Input/Output System | Legacy firmware startup interface; UEFI is the modern successor with Secure Boot support. |
| `CMS` | Content Management System | Content management system; exposed plugins/themes/admin interfaces require patching and hardening. |
| `EFS` | Encrypted File System | Windows file-level encryption; distinct from full-disk encryption. |
| `ERP` | Enterprise Resource Planning | Enterprise resource planning platform integrating business processes and sensitive records. |
| `FPGA` | Field Programmable Gate Array | Reconfigurable hardware logic; firmware/bitstream integrity and supply chain matter. |
| `GPU` | Graphics Processing Unit | Parallel processor used for graphics and compute; also relevant to AI workloads. |
| `HA` | High Availability | High availability design reducing service interruption through redundancy/failover. |
| `HDD` | Hard Disk Drive | Magnetic storage; deleted files may remain recoverable until securely sanitized. |
| `ICS` | Industrial Control Systems | Industrial control systems; SCADA supervises distributed processes and PLCs execute local control. |
| `IoT` | Internet of Things | Connected physical devices/sensors; often constrained and difficult to patch. |
| `MBR` | Master Boot Record | Legacy disk boot record/partition table; bootkits may target it. |
| `MDM` | Mobile Device Management | Manages device enrollment, configuration, compliance and remote wipe; UEM covers broader endpoint fleets. |
| `NGFW` | Next-generation Firewall | Next-generation firewall combining stateful filtering with application/user/threat inspection. |
| `NTFS` | New Technology File System | Windows filesystem supporting permissions, auditing, encryption features and journaling. |
| `OS` | Operating System | Operating system managing hardware, processes, memory, files and security boundaries. |
| `OT` | Operational Technology | Operational technology controlling physical processes; safety/availability priorities differ from IT. |
| `RAID` | Redundant Array of Inexpensive Disks | Combines disks for availability/performance; never replaces an independent backup. |
| `RTOS` | Real-time Operating System | Designed for predictable timing/deadlines; deterministic behavior does not automatically mean secure or safety-certified. |
| `SAN` | Storage Area Network | Subject Alternative Name: certificate extension listing DNS names/IP identities; distinct from Storage Area Network (SAN) in infrastructure. |
| `SCADA` | Supervisory Control and Data Acquisition | Supervisory monitoring/control for distributed industrial processes; part of the broader ICS environment. |
| `SDK` | Software Development Kit | Software development kit containing APIs, libraries, tools and documentation. |
| `SDN` | Software-defined Networking | Separates network control logic from packet forwarding to enable programmable management. |
| `SE Linux` | Security-enhanced Linux | Linux security module implementing mandatory access control policies. |
| `SoC` | System on Chip | System on Chip integrates processor and other hardware components; case-sensitive distinction from SOC (Security Operations Center). |
| `SSD` | Solid State Drive | Flash storage; secure erase and encryption depend on controller and key-management implementation. |
| `TPM` | Trusted Platform Module | Hardware security component for key protection and platform measurements; supports measured/secure boot. |
| `UEFI` | Unified Extensible Firmware Interface | Modern firmware interface; Secure Boot verifies boot components, subject to key/policy configuration. |
| `UEM` | Unified Endpoint Management | Unified management across mobile and other endpoint types; broader scope than MDM. |
| `UTM` | Unified Threat Management | Unified threat management appliance combining multiple security functions. |
| `VDE` | Virtual Desktop Environment | Virtual desktop environment delivered to users remotely or locally. |
| `VDI` | Virtual Desktop Infrastructure | Centralized virtual desktop infrastructure hosting desktop instances in data center/cloud. |
| `VM` | Virtual Machine | Virtual machine emulating computer hardware and running an isolated guest OS. |

---

**Study rule:** learn the technical distinction in the explanation above, then use the official acronym list as a recognition checklist. Do not memorize an acronym expansion as a substitute for understanding the mechanism.


---


# PARTIE XVI — Endpoint, mobile, wireless and physical security

> **Scope:** Protection of endpoints, mobile devices, and physical assets: workstation and server hardening, mobile device management, BYOD, COPE, CYOD, wireless device deployment, removable media, Bluetooth and NFC exposure, hardware interfaces, physical access controls, surveillance, and device-loss protection. Focus on securing devices throughout deployment, use, maintenance, and retirement.

## 1. Endpoint and mobile device management

Endpoints include workstations, laptops, smartphones, tablets, servers, and IoT devices. Their risk comes from local data, user interaction, unpatched software, removable media, credentials, and network access. Baseline controls include secure configuration, patching, endpoint protection, disk encryption, least privilege, application control, and centralized telemetry.

**MDM** manages mobile-device enrollment, configuration, compliance, remote lock/wipe, certificates, and policy. **UEM** extends management across multiple endpoint types (mobile, desktop, and sometimes IoT). **BYOD** allows personally owned devices; **COPE** is corporate-owned but personally enabled; **CYOD** lets users choose from approved corporate devices. The ownership model changes privacy, control, support, and data-separation expectations.

Containerization/work profiles separate corporate data from personal data. Remote wipe should distinguish corporate container from full device wipe where possible. Device compliance can be used as a condition for network/application access.

## 2. Hardware and physical security

Physical controls protect facilities and assets: locks, badges, mantraps, CCTV, guards, barriers, secure racks, environmental controls, and visitor logs. CCTV supports detection/investigation but does not prevent entry by itself. PTZ cameras can pan/tilt/zoom; coverage planning must account for blind spots, retention, access control, and privacy requirements.

HVAC maintains environmental conditions; UPS provides short-term backup power and surge protection; redundant power and generators support longer outages. A UPS does not replace tested backups or disaster recovery.

## 3. SIM, NFC, RFID and device identifiers

SIM/eSIM identity is used by cellular networks to authenticate a subscriber. SIM swapping is a social-engineering/account-recovery attack in which an attacker transfers a victim's phone number to a SIM they control, potentially intercepting SMS-based OTPs. SMS is therefore weaker than phishing-resistant MFA.

RFID identifies/communicates with tags using radio frequency; NFC is a short-range subset/technology often used for contactless payments and pairing. Short range is not a complete security boundary: relay attacks, cloning, weak access controls, and insecure backend workflows remain possible.

## 4. Removable media and endpoint hardening

USB devices can carry malware, exfiltrate data, or impersonate keyboards/network adapters. Apply device control, allowlisting, encryption, scanning, and user training. USB OTG allows mobile devices to act as USB hosts/peripherals. Disable unused interfaces and restrict boot from removable media where appropriate.

## Exam traps

- BYOD = employee-owned; COPE = company-owned with personal use; CYOD = choice among approved devices.
- MDM manages mobile devices; UEM covers broader endpoint estate.
- CCTV is detective, not a complete preventive control.
- UPS bridges power interruption; generator supports longer operation; neither replaces backup/DR.
- SMS OTP is vulnerable to SIM swap and phishing; prefer app-based or hardware-backed phishing-resistant authentication.

## Supplementary concepts — not in the official acronym appendix
These items are added for technical understanding and are not entries in CompTIA’s acronym appendix. Some may still support exam-objective topics; absence from the appendix does **not** mean “out of scope.” Treat items explicitly described as legacy or optional as additional depth.

- **MAM** — Mobile Application Management; controls apps/data without necessarily managing the entire device.
- **MCM** — Mobile Content Management.
- **FIDO2/WebAuthn** — phishing-resistant authentication.
- **USB device control** — endpoint policy for allowed classes/serials of removable hardware.
- **Geofencing** — policy based on device location; location can be spoofed and should not be the sole control.

## Technical references

- [NIST SP 800-124 Rev. 2 — Mobile Device Security](https://csrc.nist.gov/pubs/sp/800/124/r2/final)
- [NIST SP 800-46 — Telework and Remote Access](https://csrc.nist.gov/pubs/sp/800/46/r2/final)
- [CISA Mobile Communications Best Practices](https://www.cisa.gov/resources-tools/resources/mobile-communications-best-practices)

## Official acronym coverage

The following entries are preserved from the CompTIA SY0-701 acronym appendix. The third column explains the technical role and highlights useful distinctions. An acronym can have different meanings in different domains; read the expansion and the surrounding context together.


| Acronym | Official expansion (CompTIA) | Description / technical role |
|---|---|---|
| `BYOD` | Bring Your Own Device | Personal device used for work; requires clear ownership, privacy and data-separation policies. |
| `CAPTCHA` | Completely Automated Public Turing Test to Tell Computers and Humans Apart | Challenge intended to distinguish human interaction from automated abuse; not a strong identity factor. |
| `CCTV` | Closed-circuit Television | Closed-circuit video surveillance for physical monitoring and investigation. |
| `COPE` | Corporate Owned, Personally Enabled | Organization-owned device with permitted personal use; unlike BYOD, enterprise owns hardware. |
| `CYOD` | Choose Your Own Device | User chooses from approved corporate devices; differs from unrestricted BYOD. |
| `HVAC` | Heating, Ventilation Air Conditioning | Building heating/ventilation/air-conditioning systems; networked controls can affect physical safety. |
| `NFC` | Near Field Communication | Very short-range 13.56 MHz communication; related to RFID but typically designed for close-proximity interaction. |
| `PTZ` | Pan-tilt-zoom | Camera capable of pan, tilt and zoom movement. |
| `RFID` | Radio Frequency Identifier | Radio-frequency identification family using tags/readers; NFC is a short-range related technology, not a synonym. |
| `SIM` | Subscriber Identity Module | Cellular subscriber identity/credential module; SIM-swap attacks target the account/number association. |
| `UPS` | Uninterruptable Power Supply | Uninterruptible power supply providing temporary power and surge protection; supports graceful shutdown. |
| `USB` | Universal Serial Bus | Peripheral/removable-storage interface; control device classes and data transfer to reduce exfiltration risk. |
| `USB OTG` | USB On the Go | Lets a mobile device act as USB host or peripheral; increases the range of attachable devices. |

---

**Study rule:** learn the technical distinction in the explanation above, then use the official acronym list as a recognition checklist. Do not memorize an acronym expansion as a substitute for understanding the mechanism.


---


# PARTIE XVII — Data protection, privacy and information handling

> **Scope:** Data security throughout its lifecycle: data classification, sensitivity levels, PII, PHI, regulated information, intellectual property, data sovereignty, data residency, data at rest, data in transit, data in use, encryption, hashing, masking, tokenization, DLP, retention, secure deletion, and media sanitization. Focus on selecting protection mechanisms according to data sensitivity, location, state, access requirements, and regulatory obligations.

## 1. Data classification and lifecycle

Data protection begins with knowing what data exists, who owns it, where it is stored, how sensitive it is, and how long it must be retained. Classification labels (public, internal, confidential, restricted, or organization-specific tiers) drive handling requirements such as encryption, access approval, logging, retention, and disposal.

Data states:
- **At rest**: stored on disk, backup, database, or removable media. Use full-disk/file/database encryption and key management.
- **In transit**: moving over a network. Use TLS, IPsec, SSH, or other authenticated secure transport.
- **In use**: being processed in memory. Traditional encryption at rest/in transit does not protect plaintext while an authorized process uses it; memory isolation, least privilege, trusted execution, and data minimization matter.

## 2. PII and PHI

**PII** is information that identifies or can be linked to an individual, directly or indirectly. **PHI** is health information linked to an individual in the context defined by applicable law (for example, HIPAA in the United States). A dataset can be sensitive even if it does not contain a name; combinations of attributes can re-identify a person.

GDPR is the EU General Data Protection Regulation. It establishes principles and rights around personal-data processing, including lawfulness, purpose limitation, data minimization, accuracy, storage limitation, integrity/confidentiality, and accountability. It is not merely an encryption standard. Organizations need a lawful basis, transparency, data-subject rights handling, retention controls, processor arrangements, and breach procedures.

## 3. Data-loss prevention and sanitization

DLP identifies and controls sensitive data movement using content inspection, labels, patterns, fingerprints, endpoint/network/cloud controls, and policy. DLP can block, quarantine, encrypt, or alert. It can generate false positives and may not inspect end-to-end encrypted channels without an authorized inspection point.

Data sanitization must match media and sensitivity. Clear, purge, and destroy are different assurance levels in NIST guidance. Deleting a file or formatting a drive is not necessarily secure sanitization; SSD wear-leveling and remapped blocks complicate overwrite assumptions. Cryptographic erase may be appropriate when encryption/key management was correctly implemented.

## 4. Privacy-enhancing transformations

- **Masking** hides selected fields for display/use (e.g., show only last four digits).
- **Tokenization** replaces sensitive values with tokens; a protected mapping system can reverse them.
- **Pseudonymization** replaces direct identifiers but may allow re-linking using additional information.
- **Anonymization** aims to make re-identification no longer reasonably possible; robust anonymization is difficult with rich datasets.
- **Encryption** is reversible with the key; it does not anonymize data.

## Exam traps

- PII vs PHI: PHI is health-related personal information under relevant legal definitions.
- Data at rest / in transit / in use require different control considerations.
- Tokenization replaces values; encryption transforms data mathematically; masking limits what is displayed.
- Deletion ≠ sanitization; SSDs require media-aware methods.
- GDPR governs personal-data processing and rights, not only technical security.

## Supplementary concepts — not in the official acronym appendix
These items are added for technical understanding and are not entries in CompTIA’s acronym appendix. Some may still support exam-objective topics; absence from the appendix does **not** mean “out of scope.” Treat items explicitly described as legacy or optional as additional depth.

- **DPIA** — Data Protection Impact Assessment.
- **DPO** — Data Protection Officer (official acronym in CompTIA list).
- **DSAR** — Data Subject Access Request.
- **Data minimization** — collect/process only what is necessary for a stated purpose.
- **Cryptographic erase** — sanitization by securely destroying encryption keys so ciphertext becomes inaccessible.

## Technical references

- [GDPR — Regulation (EU) 2016/679](https://eur-lex.europa.eu/eli/reg/2016/679/oj)
- [NIST SP 800-88 Rev. 2 — Media Sanitization](https://csrc.nist.gov/pubs/sp/800/88/r2/final)
- [NIST Privacy Framework](https://www.nist.gov/privacy-framework)
- [NIST SP 800-122 — Protecting PII](https://csrc.nist.gov/pubs/sp/800/122/final)

## Official acronym coverage

The following entries are preserved from the CompTIA SY0-701 acronym appendix. The third column explains the technical role and highlights useful distinctions. An acronym can have different meanings in different domains; read the expansion and the surrounding context together.


| Acronym | Official expansion (CompTIA) | Description / technical role |
|---|---|---|
| `DPO` | Data Privacy Officer | Data Protection Officer overseeing data-protection compliance/advice where legally required. |
| `FDE` | Full Disk Encryption | Full-disk encryption protects stored data when device is off/locked; not plaintext while in use. |
| `GDPR` | General Data Protection Regulation | EU data-protection regulation governing processing of personal data and individual rights. |
| `NDA` | Non-disclosure Agreement | Contractual confidentiality obligation; does not replace technical access controls. |
| `PHI` | Personal Health Information | Identifiable health information in a regulated context; a subset/special category relative to PII. |
| `PII` | Personally Identifiable Information | Information that identifies or can be linked to a person; broader than PHI. |
| `RA` | Recovery Agent | Recovery Agent is authorized to recover protected data/keys under policy; distinct from a PKI Registration Authority. |
| `SED` | Self-encrypting Drives | Drive performs internal encryption; security depends on key handling, authentication and correct sanitization. |
| `SQL` | Structured Query Language | Structured Query Language for relational database operations; injection risk arises from unsafe query construction. |
| `XML` | Extensible Markup Language | Markup format used for structured data; unsafe parser features can enable XXE. |

---

**Study rule:** learn the technical distinction in the explanation above, then use the official acronym list as a recognition checklist. Do not memorize an acronym expansion as a substitute for understanding the mechanism.


---


# PARTIE XVIII — Risk, governance, compliance and business continuity

> **Scope:** Security governance and organizational risk management: policies, standards, procedures, risk identification and assessment, qualitative and quantitative analysis, risk treatment, business impact analysis, compliance, audits, third-party risk, vendor management, business continuity, disaster recovery, recovery objectives, and security-program oversight. Focus on how organizations manage risk, demonstrate compliance, assign accountability, and maintain critical operations.

## 1. Risk assessment and quantitative analysis

Risk is the potential for an event to affect objectives. A practical assessment considers threat, vulnerability, likelihood, impact, existing controls, and uncertainty. Risk is not identical to vulnerability severity: the same vulnerability can have different business risk depending on asset value, exposure, exploitability, and compensating controls.

Quantitative risk terms:

- **SLE** = Asset Value × Exposure Factor (EF): estimated loss from one occurrence.
- **ARO** = estimated frequency of occurrence per year.
- **ALE** = SLE × ARO: estimated annualized loss.

Example: asset value €100,000; EF 30%; SLE €30,000. If ARO is 0.2/year, ALE = €6,000/year. This is an estimate, not a guaranteed forecast. Qualitative scales (low/medium/high) are useful when reliable financial data is unavailable.

Risk treatment options commonly include mitigate/reduce, transfer/share, avoid, and accept. Transfer (e.g., insurance) does not eliminate all residual risk or accountability. Acceptance should be documented by an authorized risk owner and revisited when conditions change.

## 2. Business impact and continuity

**BIA** identifies critical business processes, dependencies, impacts of disruption, and recovery priorities. It informs RTO and RPO:

- **RTO**: target maximum time to restore a service/process after disruption.
- **RPO**: maximum tolerable data-loss window measured backward from disruption; it drives backup/replication frequency.

If RPO is 4 hours, the organization is prepared to lose up to roughly 4 hours of data. If RTO is 8 hours, the service should be restored within the target 8-hour window. RTO is not the same as MTTR, and RPO is not backup retention duration.

BCP maintains critical business operations during disruption; DRP focuses on restoring IT systems/infrastructure. COOP focuses on continuing essential government/organizational functions in a continuity context. CP is contingency planning. Plans need owners, dependencies, alternate sites, communications, tests, and realistic recovery resources.

## 3. Reliability metrics

- **MTBF**: average operating time between failures for a repairable system.
- **MTTF**: expected operating time to failure for a non-repairable item (or lifetime metric in the relevant context).
- **MTTR**: mean time to repair/recover/restore; the exact “R” meaning varies by organization, so read the definition used.

These are operational reliability metrics, not substitutes for RTO/RPO. A system can have a good MTBF but still violate RTO if recovery is slow.

## 4. Governance, contracts, and compliance

Policies state management intent and mandatory direction; standards define mandatory requirements; procedures give step-by-step instructions; guidelines are recommended practices; baselines define minimum configurations. Audit evaluates evidence against criteria. Compliance is adherence to applicable laws, regulations, contracts, and policies; it does not guarantee security.

NDA protects confidential information; MOU records mutual understanding; MOA formalizes agreed responsibilities/commitments; MSA sets overarching commercial/legal terms; SOW defines specific work, deliverables, schedule, and acceptance criteria; SLA defines measurable service levels and remedies. BPA is an agreement between business partners. PCI DSS applies to environments handling payment-card data; GDPR governs personal-data processing in the EU.

## Exam traps

- SLE = loss per event; ALE = annualized loss; ARO = annual frequency estimate.
- RTO = time to restore; RPO = acceptable data-loss interval.
- BIA identifies criticality and recovery requirements; BCP sustains business; DRP restores IT.
- Insurance transfers some financial impact, not all risk/accountability.
- Policy / standard / procedure / guideline / baseline are different document types.
- SLA is measurable service performance; SOW describes work/deliverables; MSA is overarching agreement.

## Supplementary concepts — not in the official acronym appendix
These items are added for technical understanding and are not entries in CompTIA’s acronym appendix. Some may still support exam-objective topics; absence from the appendix does **not** mean “out of scope.” Treat items explicitly described as legacy or optional as additional depth.

- **KRI** — Key Risk Indicator; signals increasing risk exposure.
- **KPI** — Key Performance Indicator; measures performance against objectives.
- **Residual risk** — risk remaining after controls.
- **Inherent risk** — risk before controls.
- **Risk appetite/tolerance** — amount/type of risk leadership is willing to pursue/accept and permitted variation.
- **BIA outputs** — criticality, dependencies, maximum tolerable downtime, RTO/RPO targets.

## Technical references

- [NIST SP 800-30 Rev. 1 — Risk Assessments](https://csrc.nist.gov/pubs/sp/800/30/r1/final)
- [NIST SP 800-34 Rev. 1 — Contingency Planning](https://csrc.nist.gov/pubs/sp/800/34/r1/final)
- [PCI Security Standards Council](https://www.pcisecuritystandards.org/)
- [GDPR official text](https://eur-lex.europa.eu/eli/reg/2016/679/oj)

## Official acronym coverage

The following entries are preserved from the CompTIA SY0-701 acronym appendix. The third column explains the technical role and highlights useful distinctions. An acronym can have different meanings in different domains; read the expansion and the surrounding context together.


| Acronym | Official expansion (CompTIA) | Description / technical role |
|---|---|---|
| `ALE` | Annualized Loss Expectancy | Annualized expected loss; calculated as SLE × ARO. |
| `ARO` | Annualized Rate of Occurrence | Estimated annual frequency of a loss event; used to calculate ALE. |
| `AUP` | Acceptable Use Policy | Acceptable use policy defining permitted/prohibited use of organizational systems. |
| `BCP` | Business Continuity Planning | Business continuity planning keeps critical business functions operating during disruption. |
| `BIA` | Business Impact Analysis | Business impact analysis identifies critical processes, dependencies and disruption impacts. |
| `BPA` | Business Partners Agreement | Business partners agreement defining relationship/obligations between partner organizations. |
| `COOP` | Continuity of Operation Planning | Continuity of operations planning for sustaining essential functions during disruption. |
| `CP` | Contingency Planning | Contingency planning preparing alternative procedures/resources for disruptive events. |
| `DRP` | Disaster Recovery Plan | Disaster recovery plan restoring IT systems/data after major disruption; supports BCP. |
| `MOA` | Memorandum of Agreement | Memorandum of agreement documenting agreed responsibilities/terms between parties. |
| `MOU` | Memorandum of Understanding | Memorandum of understanding expressing shared intent/understanding; legal enforceability varies. |
| `MSA` | Master Service Agreement | Master service agreement setting general contractual terms for future work orders/SOWs. |
| `MTBF` | Mean Time Between Failures | Mean operating time between failures for repairable systems. |
| `MTTF` | Mean Time to Failure | Expected time to failure for a non-repairable item. |
| `MTTR` | Mean Time to Recover | Mean time to repair/recover/restore; check which R meaning the question uses. |
| `PCI DSS` | Payment Card Industry Data Security Standard | Payment-card industry security requirements for entities handling cardholder data. |
| `RPO` | Recovery Point Objective | Maximum tolerable data-loss interval; determines backup/replication frequency. |
| `RTO` | Recovery Time Objective | Target time to restore a service after disruption. |
| `SLA` | Service-level Agreement | Service-level agreement defining measurable service commitments and remedies. |
| `SLE` | Single Loss Expectancy | Estimated loss from one event; ALE = SLE × ARO. |
| `SOW` | Statement of Work | Statement of work specifying deliverables, scope, milestones and acceptance criteria. |
| `WO` | Work Order | Work order authorizing/describing a specific task or service. |

---

**Study rule:** learn the technical distinction in the explanation above, then use the official acronym list as a recognition checklist. Do not memorize an acronym expansion as a substitute for understanding the mechanism.


---


# PARTIE XIX — Software development, application components and cross-domain terms

> **Scope:** Secure software engineering and application security: software development lifecycle, secure coding, source-code analysis, dynamic testing, application testing, input validation, APIs, application components, dependencies, software supply-chain security, code signing, deployment integrity, and secure development practices. Focus on preventing, detecting, and correcting software weaknesses throughout development, integration, deployment, and maintenance.

## 1. Secure SDLC and security testing

The Software Development Life Cycle (SDLC) includes requirements, design, implementation, testing, deployment, and maintenance. Security should be integrated into every phase (“shift left”), not added only during final testing. Threat modeling during design identifies assets, trust boundaries, entry points, abuse cases, and mitigations. Secure coding standards and code review reduce implementation flaws; security testing validates controls.

**SAST** analyzes source/bytecode without executing the application; it can find insecure patterns early but may produce false positives and miss runtime/configuration issues. **DAST** tests a running application from the outside; it finds runtime behavior but may not identify the exact source line. **IAST** instruments the running app to observe data flow. **SCA** identifies third-party dependencies, known vulnerabilities, licenses, and component provenance. Penetration testing attempts controlled exploitation; it is not a replacement for continuous testing.

UAT checks whether the system meets user/business acceptance needs. Passing UAT does not prove security. Regression testing checks that changes have not broken existing functionality or security controls.

## 2. APIs and application components

An **API** is a defined contract through which software components communicate. Secure APIs require strong authentication, authorization at object/function level, input validation, rate limiting, schema enforcement, secure transport, logging, and version/lifecycle management. API keys identify a client but are not necessarily strong user authentication; secrets can leak from mobile apps, source code, logs, and repositories.

HTML structures web content; JavaScript executes client-side logic; XML is a markup/data format; SQL is a query language for relational databases. Security depends on context: HTML output encoding, safe DOM APIs, XML parser hardening (disable dangerous external entities where appropriate), parameterized SQL, and server-side authorization.

DLLs are shared libraries loaded by applications. DLL search-order hijacking can cause a program to load a malicious library from an attacker-controlled location. Structured Exception Handling (SEH) is a Windows exception-handling mechanism and can be relevant to exploit techniques. Bash and VBA are scripting/automation environments that can be abused for execution, but also used legitimately for administration.

## 3. Development approaches and supply-chain controls

RAD emphasizes rapid prototyping/iteration; speed does not remove the need for security requirements, review, and testing. SDLM refers to a methodology for the SDLC. SDKs provide tools/libraries for building against a platform; third-party SDKs and packages expand the software supply-chain attack surface. Maintain dependency inventories, pin versions, verify signatures/hashes, scan for known vulnerabilities, and protect build pipelines.

Build systems and CI/CD credentials are high-value targets. Apply least privilege, isolated runners, protected branches, code review, artifact signing, secrets management, provenance/attestation, and separation between build and deployment permissions.

## Technical clarification: application-security testing methods

- **SAST** analyzes source code or bytecode without running the application. It is useful early in development but may produce false positives and cannot fully observe runtime behavior.
- **DAST** tests a running application from the outside, often by sending requests and observing responses. It can reveal runtime issues but may miss code paths it does not reach.
- **IAST** instruments or observes an application while tests execute, combining runtime context with test activity.
- **SCA** inventories third-party libraries/components and checks known vulnerabilities and license concerns. It is not the same as analyzing the developer's own source code.
- **Fuzzing** generates or mutates inputs to expose crashes, hangs and unexpected behavior. It is a testing technique, not a synonym for SAST or DAST.

Use complementary methods: no single scanner proves that an application is secure. Findings should be validated, prioritized, fixed and regression-tested.

## Exam traps

- SAST = static/no execution; DAST = running application; SCA = third-party component/dependency analysis.
- UAT = user/business acceptance, not a security certification.
- API key ≠ robust user identity; enforce authorization on every object/action.
- XML is a data format; XML parser configuration can create XXE risk.
- SQLi prevention uses parameterized queries; XSS prevention uses context-aware output encoding/safe DOM handling.
- SDLC security is continuous, not a final-stage scan only.

## Supplementary concepts — not in the official acronym appendix
These items are added for technical understanding and are not entries in CompTIA’s acronym appendix. Some may still support exam-objective topics; absence from the appendix does **not** mean “out of scope.” Treat items explicitly described as legacy or optional as additional depth.

- **Threat modeling** — systematic identification of assets, trust boundaries, threats, and mitigations (e.g., STRIDE).
- **SBOM** — Software Bill of Materials.
- **SAST / DAST / IAST / SCA** — complementary application-security testing approaches.
- **CI/CD** — Continuous Integration / Continuous Delivery or Deployment.
- **ASVS** — OWASP Application Security Verification Standard.
- **XXE** — XML External Entity; exploit of unsafe XML parser features.

## Technical references

- [OWASP Software Assurance Maturity Model (SAMM)](https://owaspsamm.org/)
- [OWASP Application Security Verification Standard](https://owasp.org/www-project-application-security-verification-standard/)
- [OWASP Cheat Sheet Series](https://cheatsheetseries.owasp.org/cheatsheets/Index.html)
- [NIST SP 800-218 — Secure Software Development Framework (SSDF)](https://csrc.nist.gov/pubs/sp/800/218/final)
- [CISA Secure Software Development Attestation](https://www.cisa.gov/secure-software-attestation-form)

## Official acronym coverage

The following entries are preserved from the CompTIA SY0-701 acronym appendix. The third column explains the technical role and highlights useful distinctions. An acronym can have different meanings in different domains; read the expansion and the surrounding context together.


| Acronym | Official expansion (CompTIA) | Description / technical role |
|---|---|---|
| `API` | Application Programming Interface | Defined software interface; authorization, input validation and rate limiting are key API security controls. |
| `BASH` | Bourne Again Shell | Unix shell and scripting language used for command execution and automation. |
| `DBA` | Database Administrator | Database administrator responsible for database availability, access, maintenance and security. |
| `HTML` | Hypertext Markup Language | Markup language structuring web content; browser interprets it rather than executing it as a general-purpose program. |
| `OID` | Object Identifier | Object identifier: globally structured identifier used in standards, certificates and directory schemas. |
| `RACE` | Research and Development in Advanced Communications Technologies in Europe | Research program acronym appearing in the official appendix; historical expansion, not a core security control. |
| `RAD` | Rapid Application Development | Rapid application development emphasizing iterative prototyping and short feedback cycles. |
| `SDLC` | Software Development Lifecycle | Lifecycle from planning/design through build, test, deployment and maintenance; secure SDLC embeds security throughout. |
| `SDLM` | Software Development Lifecycle Methodology | Software development lifecycle methodology; structured approach governing SDLC activities. |
| `UAT` | User Acceptance Testing | User acceptance testing checks business requirements; it is not a substitute for security testing. |
| `VBA` | Visual Basic | Visual Basic for Applications; automation/scripting language embedded in Office applications. |

---

**Study rule:** learn the technical distinction in the explanation above, then use the official acronym list as a recognition checklist. Do not memorize an acronym expansion as a substitute for understanding the mechanism.
