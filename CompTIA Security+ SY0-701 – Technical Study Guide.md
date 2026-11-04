# CompTIA Security+ SY0-701 – Technical Study Guide

This edition keeps the same 19 thematic groups and the official CompTIA acronym appendix as its coverage baseline. It replaces generic acronym paraphrases with exam-oriented technical explanations, comparisons, attack/defense mechanisms, scenario cues, and technical references.

## How to use this guide

1. Read the technical model and understand the mechanism.
2. Study the distinctions and exam traps; Security+ questions often describe a scenario rather than ask for a definition.
3. Review supplementary acronyms separately. They are **not** part of the official CompTIA appendix unless explicitly stated.
4. Use the linked RFCs, NIST publications, standards bodies, and OWASP guidance for deeper study.

## Important source discipline

- Official expansions are preserved from the supplied CompTIA SY0-701 Exam Objectives, Version 5.0, pages 17–20.
- Official entries are not silently corrected, even where wording differs from standard industry phrasing.
- Supplementary concepts are clearly labeled and added only to explain related technology or current practice.
- Exam emphasis is guided by the SY0-701 objectives; this is a study aid, not a substitute for the official objectives or hands-on practice.

## Contents

- [PARTIE I — Security foundations and core principles](PARTIE-I.md)
- [PARTIE II — Access control models and permissions](PARTIE-II.md)
- [PARTIE III — Authentication, identity protocols and federation](PARTIE-III.md)
- [PARTIE IV — Symmetric encryption, hashes and cryptographic modes](PARTIE-IV.md)
- [PARTIE V — Asymmetric cryptography, certificates and PKI](PARTIE-V.md)
- [PARTIE VI — Network architecture, addressing and infrastructure](PARTIE-VI.md)
- [PARTIE VII — Network services, application protocols and messaging](PARTIE-VII.md)
- [PARTIE VIII — Secure communications, remote access and wireless](PARTIE-VIII.md)
- [PARTIE IX — Threat actors, threat intelligence and reconnaissance](PARTIE-IX.md)
- [PARTIE X — Vulnerabilities, malware and exploit mitigation](PARTIE-X.md)
- [PARTIE XI — Attack techniques and application-layer attacks](PARTIE-XI.md)
- [PARTIE XII — Security monitoring, detection and defensive platforms](PARTIE-XII.md)
- [PARTIE XIII — Incident response, investigation and threat data exchange](PARTIE-XIII.md)
- [PARTIE XIV — Cloud services, cloud security and service models](PARTIE-XIV.md)
- [PARTIE XV — Systems architecture, virtualization and industrial technology](PARTIE-XV.md)
- [PARTIE XVI — Endpoint, mobile, wireless and physical security](PARTIE-XVI.md)
- [PARTIE XVII — Data protection, privacy and information handling](PARTIE-XVII.md)
- [PARTIE XVIII — Risk, governance, compliance and business continuity](PARTIE-XVIII.md)
- [PARTIE XIX — Software development, application components and cross-domain terms](PARTIE-XIX.md)

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

## Supplementary concepts (not official appendix entries)

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

The following entries are from the CompTIA appendix. Duplicate abbreviations are intentionally retained where CompTIA lists more than one meaning. The expansion is preserved as printed, including wording that may differ from common technical usage.

| Acronym | Official expansion | Source PDF page |
|---|---|---:|
| `AAA` | Authentication, Authorization, and Accounting | 17 |
| `AI` | Artificial Intelligence | 17 |
| `CAR` | Corrective Action Report | 17 |
| `CIA` | Confidentiality, Integrity, Availability | 17 |
| `CIO` | Chief Information Officer | 17 |
| `CSO` | Chief Security Officer | 17 |
| `CTO` | Chief Technology Officer | 17 |
| `ISO` | International Standards Organization | 18 |
| `ISSO` | Information Systems Security Officer | 18 |
| `NIST` | National Institute of Standards & Technology | 19 |
| `ROI` | Return on Investment | 19 |

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

## Supplementary concepts

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

The following entries are from the CompTIA appendix. Duplicate abbreviations are intentionally retained where CompTIA lists more than one meaning. The expansion is preserved as printed, including wording that may differ from common technical usage.

| Acronym | Official expansion | Source PDF page |
|---|---|---:|
| `ACL` | Access Control List | 17 |
| `DAC` | Discretionary Access Control | 17 |
| `FACL` | File System Access Control List | 18 |
| `FIM` | File Integrity Management | 18 |
| `GPO` | Group Policy Object | 18 |
| `IAM` | Identity and Access Management | 18 |
| `IdP` | Identity Provider | 18 |
| `MAC` | Mandatory Access Control | 18 |
| `NAC` | Network Access Control | 19 |
| `PAM` | Privileged Access Management | 19 |
| `RBAC` | Role-based Access Control | 19 |
| `RBAC` | Rule-based Access Control | 19 |

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

## Exam traps

- LDAP = directory access; Kerberos = ticket-based authentication; RADIUS/TACACS+ = AAA; SAML/OIDC = federation/SSO; OAuth = delegated authorization.
- TGT ≠ service ticket.
- HOTP uses a counter; TOTP uses time.
- MFA requires different factor categories, not merely two credentials.
- EAP is a framework; PEAP is an EAP method/tunneled method.
- SAML assertion / OIDC ID Token convey authentication claims; OAuth access token authorizes API/resource access.

## Supplementary concepts

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

The following entries are from the CompTIA appendix. Duplicate abbreviations are intentionally retained where CompTIA lists more than one meaning. The expansion is preserved as printed, including wording that may differ from common technical usage.

| Acronym | Official expansion | Source PDF page |
|---|---|---:|
| `CHAP` | Challenge Handshake Authentication Protocol | 17 |
| `EAP` | Extensible Authentication Protocol | 18 |
| `FRR` | False Rejection Rate | 18 |
| `HOTP` | HMAC-based One-time Password | 18 |
| `KDC` | Key Distribution Center | 18 |
| `LDAP` | Lightweight Directory Access Protocol | 18 |
| `LEAP` | Lightweight Extensible Authentication Protocol | 18 |
| `MFA` | Multifactor Authentication | 18 |
| `MSCHAP` | Microsoft Challenge Handshake Authentication Protocol | 18 |
| `NTLM` | New Technology LAN Manager | 19 |
| `OAUTH` | Open Authorization | 19 |
| `PAM` | Pluggable Authentication Modules | 19 |
| `PAP` | Password Authentication Protocol | 19 |
| `PEAP` | Protected Extensible Authentication Protocol | 19 |
| `PED` | Personal Electronic Device | 19 |
| `PIV` | Personal Identity Verification | 19 |
| `RADIUS` | Remote Authentication Dial-in User Service | 19 |
| `SAML` | Security Assertions Markup Language | 19 |
| `SSO` | Single Sign-on | 20 |
| `TACACS+` | Terminal Access Controller Access Control System | 20 |
| `TGT` | Ticket Granting Ticket | 20 |
| `TOTP` | Time-based One-time Password | 20 |

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

## Exam traps

- AES is a cipher; GCM/CBC/CTR are modes.
- ECB leaks patterns; CBC needs correct IV/padding and separate integrity; GCM is authenticated encryption.
- Hashing ≠ encryption; CRC ≠ secure hash; HMAC ≠ digital signature.
- Salts are not secrets and should be unique; peppers are secret and stored separately.
- Reusing a GCM nonce with the same key is a critical failure.

## Supplementary concepts

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

The following entries are from the CompTIA appendix. Duplicate abbreviations are intentionally retained where CompTIA lists more than one meaning. The expansion is preserved as printed, including wording that may differ from common technical usage.

| Acronym | Official expansion | Source PDF page |
|---|---|---:|
| `AES` | Advanced Encryption Standard | 17 |
| `AES-256` | Advanced Encryption Standards 256-bit | 17 |
| `CBC` | Cipher Block Chaining | 17 |
| `CCMP` | Counter Mode/CBC-MAC Protocol | 17 |
| `CFB` | Cipher Feedback | 17 |
| `CRC` | Cyclical Redundancy Check | 17 |
| `CTM` | Counter Mode | 17 |
| `DES` | Digital Encryption Standard | 17 |
| `ECB` | Electronic Code Book | 18 |
| `GCM` | Galois Counter Mode | 18 |
| `IDEA` | International Data Encryption Algorithm | 18 |
| `IV` | Initialization Vector | 18 |
| `MAC` | Message Authentication Code | 18 |
| `MD5` | Message Digest 5 | 18 |
| `PBKDF2` | Password-based Key Derivation Function 2 | 19 |
| `RC4` | Rivest Cipher version 4 | 19 |
| `RIPEMD` | RACE Integrity Primitives Evaluation Message Digest | 19 |
| `SHA` | Secure Hashing Algorithm | 20 |
| `TKIP` | Temporal Key Integrity Protocol | 20 |
| `XOR` | Exclusive Or | 20 |

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

## Exam traps

- Public-key encryption for recipient confidentiality vs private-key signing for sender authenticity/integrity.
- DH/ECDH establishes a shared secret; it does not authenticate without an additional mechanism.
- ECDSA/DSA sign; ECDHE/DHE exchange keys.
- CA issues/signs; RA validates/approves; CSR requests a certificate.
- CRL is a list; OCSP is an online status query.
- Certificate contains public key, not private key; SAN identifies valid hostnames.

## Supplementary concepts

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

The following entries are from the CompTIA appendix. Duplicate abbreviations are intentionally retained where CompTIA lists more than one meaning. The expansion is preserved as printed, including wording that may differ from common technical usage.

| Acronym | Official expansion | Source PDF page |
|---|---|---:|
| `AH` | Authentication Header | 17 |
| `CA` | Certificate Authority | 17 |
| `CRL` | Certificate Revocation List | 17 |
| `CSR` | Certificate Signing Request | 17 |
| `DHE` | Diffie-Hellman Ephemeral | 17 |
| `DSA` | Digital Signature Algorithm | 18 |
| `ECC` | Elliptic Curve Cryptography | 18 |
| `ECDHE` | Elliptic Curve Diffie-Hellman Ephemeral | 18 |
| `ECDSA` | Elliptic Curve Digital Signature Algorithm | 18 |
| `ESP` | Encapsulated Security Payload | 18 |
| `GPG` | Gnu Privacy Guard | 18 |
| `HMAC` | Hashed Message Authentication Code | 18 |
| `HSM` | Hardware Security Module | 18 |
| `IKE` | Internet Key Exchange | 18 |
| `KEK` | Key Encryption Key | 18 |
| `OCSP` | Online Certificate Status Protocol | 19 |
| `P12` | PKCS #12 | 19 |
| `PEM` | Privacy Enhanced Mail | 19 |
| `PFS` | Perfect Forward Secrecy | 19 |
| `PGP` | Pretty Good Privacy | 19 |
| `PKCS` | Public Key Cryptography Standards | 19 |
| `PKI` | Public Key Infrastructure | 19 |
| `PSK` | Pre-shared Key | 19 |
| `RA` | Recovery Agent | 19 |
| `RA` | Registration Authority | 19 |
| `RSA` | Rivest, Shamir, & Adleman | 19 |
| `SAE` | Simultaneous Authentication of Equals | 19 |
| `SAN` | Subject Alternative Name | 19 |
| `SCEP` | Simple Certificate Enrollment Protocol | 19 |
| `SED` | Self-encrypting Drives | 20 |
| `SSL` | Secure Sockets Layer | 20 |
| `TLS` | Transport Layer Security | 20 |
| `TPM` | Trusted Platform Module | 20 |
| `WTLS` | Wireless TLS | 20 |

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

## Supplementary concepts

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

The following entries are from the CompTIA appendix. Duplicate abbreviations are intentionally retained where CompTIA lists more than one meaning. The expansion is preserved as printed, including wording that may differ from common technical usage.

| Acronym | Official expansion | Source PDF page |
|---|---|---:|
| `AP` | Access Point | 17 |
| `ARP` | Address Resolution Protocol | 17 |
| `BGP` | Border Gateway Protocol | 17 |
| `BPDU` | Bridge Protocol Data Unit | 17 |
| `CSU` | Channel Service Unit | 17 |
| `DSL` | Digital Subscriber Line | 18 |
| `ESN` | Electronic Serial Number | 18 |
| `GPS` | Global Positioning System | 18 |
| `IDF` | Intermediate Distribution Frame | 18 |
| `IEEE` | Institute of Electrical and Electronics Engineers | 18 |
| `IP` | Internet Protocol | 18 |
| `LAN` | Local Area Network | 18 |
| `MAC` | Media Access Control | 18 |
| `MAN` | Metropolitan Area Network | 18 |
| `MDF` | Main Distribution Frame | 18 |
| `MFD` | Multifunction Device | 18 |
| `MFP` | Multifunction Printer | 18 |
| `MPLS` | Multi-protocol Label Switching | 18 |
| `MTU` | Maximum Transmission Unit | 19 |
| `NAT` | Network Address Translation | 19 |
| `NFC` | Near Field Communication | 19 |
| `OSPF` | Open Shortest Path First | 19 |
| `P2P` | Peer to Peer | 19 |
| `PAC` | Proxy Auto Configuration | 19 |
| `PAT` | Port Address Translation | 19 |
| `PBX` | Private Branch Exchange | 19 |
| `PDU` | Power Distribution Unit | 19 |
| `POTS` | Plain Old Telephone Service | 19 |
| `RTBH` | Remotely Triggered Black Hole | 19 |
| `UAV` | Unmanned Aerial Vehicle | 20 |
| `UTP` | Unshielded Twisted Pair | 20 |
| `VLAN` | Virtual Local Area Network | 20 |
| `VLSM` | Variable Length Subnet Masking | 20 |
| `WAP` | Wireless Access Point | 20 |

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

## Supplementary concepts

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

The following entries are from the CompTIA appendix. Duplicate abbreviations are intentionally retained where CompTIA lists more than one meaning. The expansion is preserved as printed, including wording that may differ from common technical usage.

| Acronym | Official expansion | Source PDF page |
|---|---|---:|
| `DHCP` | Dynamic Host Configuration Protocol | 17 |
| `DKIM` | DomainKeys Identified Mail | 17 |
| `DMARC` | Domain Message Authentication Reporting and Conformance | 17 |
| `DNAT` | Destination Network Address Translation | 17 |
| `DNS` | Domain Name System | 17 |
| `FTP` | File Transfer Protocol | 18 |
| `FTPS` | Secured File Transfer Protocol | 18 |
| `HTTP` | Hypertext Transfer Protocol | 18 |
| `HTTPS` | Hypertext Transfer Protocol Secure | 18 |
| `ICMP` | Internet Control Message Protocol | 18 |
| `IM` | Instant Messaging | 18 |
| `IMAP` | Internet Message Access Protocol | 18 |
| `IRC` | Internet Relay Chat | 18 |
| `ISP` | Internet Service Provider | 18 |
| `MMS` | Multimedia Message Service | 18 |
| `NTP` | Network Time Protocol | 19 |
| `OTA` | Over the Air | 19 |
| `PCAP` | Packet Capture | 19 |
| `POP` | Post Office Protocol | 19 |
| `RTP` | Real-time Transport Protocol | 19 |
| `SMTP` | Simple Mail Transfer Protocol | 20 |
| `SMTPS` | Simple Mail Transfer Protocol Secure | 20 |
| `SNMP` | Simple Network Management Protocol | 20 |
| `SOAP` | Simple Object Access Protocol | 20 |
| `SPF` | Sender Policy Framework | 20 |
| `TSIG` | Transaction Signature | 20 |
| `URI` | Uniform Resource Identifier | 20 |
| `URL` | Universal Resource Locator | 20 |
| `VoIP` | Voice over IP | 20 |
| `VTC` | Video Teleconferencing | 20 |

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

## Exam traps

- AH ≠ ESP: AH does not encrypt; ESP can.
- L2TP/GRE are tunneling/encapsulation mechanisms, not encryption by themselves.
- WEP/TKIP are legacy; WPA2-CCMP and WPA3-SAE are stronger modern choices.
- SAE is associated with WPA3-Personal; it is not the same as a RADIUS server.
- WIDS detects; WIPS can prevent/contain.
- VPN access is not automatically zero trust or least privilege.

## Supplementary concepts

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

The following entries are from the CompTIA appendix. Duplicate abbreviations are intentionally retained where CompTIA lists more than one meaning. The expansion is preserved as printed, including wording that may differ from common technical usage.

| Acronym | Official expansion | Source PDF page |
|---|---|---:|
| `GRE` | Generic Routing Encapsulation | 18 |
| `IPSec` | Internet Protocol Security | 18 |
| `L2TP` | Layer 2 Tunneling Protocol | 18 |
| `PPP` | Point-to-Point Protocol | 19 |
| `PPTP` | Point-to-Point Tunneling Protocol | 19 |
| `RAS` | Remote Access Server | 19 |
| `RDP` | Remote Desktop Protocol | 19 |
| `RFID` | Radio Frequency Identifier | 19 |
| `S/MIME` | Secure/Multipurpose Internet Mail Extensions | 19 |
| `SFTP` | Secured File Transfer Protocol | 20 |
| `SHTTP` | Secure Hypertext Transfer Protocol | 20 |
| `SIM` | Subscriber Identity Module | 20 |
| `SMS` | Short Message Service | 20 |
| `SRTP` | Secure Real-Time Protocol | 20 |
| `SSH` | Secure Shell | 20 |
| `TCP/IP` | Transmission Control Protocol/Internet Protocol | 20 |
| `UDP` | User Datagram Protocol | 20 |
| `USB` | Universal Serial Bus | 20 |
| `USB OTG` | USB On the Go | 20 |
| `VPN` | Virtual Private Network | 20 |
| `WEP` | Wired Equivalent Privacy | 20 |
| `WPA` | Wi-Fi Protected Access | 20 |
| `WPS` | Wi-Fi Protected Setup | 20 |

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

## Supplementary concepts

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

The following entries are from the CompTIA appendix. Duplicate abbreviations are intentionally retained where CompTIA lists more than one meaning. The expansion is preserved as printed, including wording that may differ from common technical usage.

| Acronym | Official expansion | Source PDF page |
|---|---|---:|
| `AIS` | Automated Indicator Sharing | 17 |
| `APT` | Advanced Persistent Threat | 17 |
| `ATT&CK` | Adversarial Tactics, Techniques, and Common Knowledge | 17 |
| `CERT` | Computer Emergency Response Team | 17 |
| `CIRT` | Computer Incident Response Team | 17 |
| `IoC` | Indicators of Compromise | 18 |
| `OSINT` | Open-source Intelligence | 19 |
| `TTP` | Tactics, Techniques, and Procedures | 20 |

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

## Exam traps

- CVE = identifier; CVSS = severity scoring system.
- Vulnerability scan ≠ penetration test: scanning identifies likely weaknesses; a penetration test attempts controlled exploitation to demonstrate impact.
- Virus vs worm vs Trojan vs RAT are behavior distinctions, not interchangeable labels.
- ASLR randomizes locations; DEP/NX prevents execution from non-executable pages.
- Patching closes known flaws; hardening reduces exposure; compensating control reduces risk when patching is delayed.

## Supplementary concepts

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

The following entries are from the CompTIA appendix. Duplicate abbreviations are intentionally retained where CompTIA lists more than one meaning. The expansion is preserved as printed, including wording that may differ from common technical usage.

| Acronym | Official expansion | Source PDF page |
|---|---|---:|
| `ASLR` | Address Space Layout Randomization | 17 |
| `AV` | Antivirus | 17 |
| `CVE` | Common Vulnerability Enumeration | 17 |
| `CVSS` | Common Vulnerability Scoring System | 17 |
| `DEP` | Data Execution Prevention | 17 |
| `DLL` | Dynamic Link Library | 17 |
| `OVAL` | Open Vulnerability Assessment Language | 19 |
| `PUP` | Potentially Unwanted Program | 19 |
| `RAT` | Remote Access Trojan | 19 |
| `SEH` | Structured Exception Handler | 20 |
| `TOC` | Time-of-check | 20 |
| `TOU` | Time-of-use | 20 |

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

## Supplementary concepts

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

The following entries are from the CompTIA appendix. Duplicate abbreviations are intentionally retained where CompTIA lists more than one meaning. The expansion is preserved as printed, including wording that may differ from common technical usage.

| Acronym | Official expansion | Source PDF page |
|---|---|---:|
| `CSRF` | Cross-site Request Forgery | 17 |
| `DDoS` | Distributed Denial of Service | 17 |
| `DoS` | Denial of Service | 17 |
| `ML` | Machine Learning | 18 |
| `SPIM` | Spam over Internet Messaging | 20 |
| `SQLi` | SQL Injection | 20 |
| `XSRF` | Cross-site Request Forgery | 20 |
| `XSS` | Cross-site Scripting | 20 |

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

## Exam traps

- IDS detects/alerts; IPS can block inline.
- NIDS/NIPS = network; HIDS/HIPS = host.
- SIEM collects/correlates; SOAR orchestrates/automates; SOC is the operational function.
- EDR endpoint-focused; XDR cross-domain correlation; MDR managed service.
- DLP protects data; CASB governs cloud-service usage; SWG secures web access.

## Supplementary concepts

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

The following entries are from the CompTIA appendix. Duplicate abbreviations are intentionally retained where CompTIA lists more than one meaning. The expansion is preserved as printed, including wording that may differ from common technical usage.

| Acronym | Official expansion | Source PDF page |
|---|---|---:|
| `DLP` | Data Loss Prevention | 17 |
| `EDR` | Endpoint Detection and Response | 18 |
| `HIDS` | Host-based Intrusion Detection System | 18 |
| `HIPS` | Host-based Intrusion Prevention System | 18 |
| `IDS` | Intrusion Detection System | 18 |
| `IPS` | Intrusion Prevention System | 18 |
| `MaaS` | Monitoring as a Service | 18 |
| `MSP` | Managed Service Provider | 18 |
| `MSSP` | Managed Security Service Provider | 18 |
| `NIDS` | Network-based Intrusion Detection System | 19 |
| `NIPS` | Network-based Intrusion Prevention System | 19 |
| `SCAP` | Security Content Automation Protocol | 19 |
| `SIEM` | Security Information and Event Management | 20 |
| `SOAR` | Security Orchestration, Automation, Response | 20 |
| `SOC` | Security Operations Center | 20 |
| `WIDS` | Wireless Intrusion Detection System | 20 |
| `WIPS` | Wireless Intrusion Prevention System | 20 |
| `XDR` | Extended Detection and Response | 20 |

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

## Exam traps

- Containment limits damage; eradication removes the cause/artifact; recovery restores trusted operations.
- A plan (IRP) defines procedures; a team (CIRT/CERT) executes/co-ordinates them.
- Chain of custody documents evidence control; a hash helps verify evidence integrity but does not prove how it was collected.
- Preserve volatile evidence before shutdown when incident procedures and safety allow.
- STIX = structured content; TAXII = exchange protocol.

## Supplementary concepts

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

The following entries are from the CompTIA appendix. Duplicate abbreviations are intentionally retained where CompTIA lists more than one meaning. The expansion is preserved as printed, including wording that may differ from common technical usage.

| Acronym | Official expansion | Source PDF page |
|---|---|---:|
| `IR` | Incident Response | 18 |
| `IRP` | Incident Response Plan | 18 |
| `STIX` | Structured Threat Information eXchange | 20 |
| `TAXII` | Trusted Automated eXchange of Indicator Information | 20 |

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

## Supplementary concepts

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

The following entries are from the CompTIA appendix. Duplicate abbreviations are intentionally retained where CompTIA lists more than one meaning. The expansion is preserved as printed, including wording that may differ from common technical usage.

| Acronym | Official expansion | Source PDF page |
|---|---|---:|
| `CASB` | Cloud Access Security Broker | 17 |
| `CSP` | Cloud Service Provider | 17 |
| `IaaS` | Infrastructure as a Service | 18 |
| `IaC` | Infrastructure as Code | 18 |
| `PaaS` | Platform as a Service | 19 |
| `SaaS` | Software as a Service | 19 |
| `SASE` | Secure Access Service Edge | 19 |
| `SD-WAN` | Software-defined Wide Area Network | 19 |
| `SWG` | Secure Web Gateway | 20 |
| `VPC` | Virtual Private Cloud | 20 |
| `WAF` | Web Application Firewall | 20 |

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

## Supplementary concepts

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

The following entries are from the CompTIA appendix. Duplicate abbreviations are intentionally retained where CompTIA lists more than one meaning. The expansion is preserved as printed, including wording that may differ from common technical usage.

| Acronym | Official expansion | Source PDF page |
|---|---|---:|
| `BIOS` | Basic Input/Output System | 17 |
| `CMS` | Content Management System | 17 |
| `EFS` | Encrypted File System | 18 |
| `ERP` | Enterprise Resource Planning | 18 |
| `FPGA` | Field Programmable Gate Array | 18 |
| `GPU` | Graphics Processing Unit | 18 |
| `HA` | High Availability | 18 |
| `HDD` | Hard Disk Drive | 18 |
| `ICS` | Industrial Control Systems | 18 |
| `IoT` | Internet of Things | 18 |
| `MBR` | Master Boot Record | 18 |
| `MDM` | Mobile Device Management | 18 |
| `NGFW` | Next-generation Firewall | 19 |
| `NTFS` | New Technology File System | 19 |
| `OS` | Operating System | 19 |
| `OT` | Operational Technology | 19 |
| `RAID` | Redundant Array of Inexpensive Disks | 19 |
| `RTOS` | Real-time Operating System | 19 |
| `SAN` | Storage Area Network | 19 |
| `SCADA` | Supervisory Control and Data Acquisition | 19 |
| `SDK` | Software Development Kit | 19 |
| `SDN` | Software-defined Networking | 20 |
| `SE Linux` | Security-enhanced Linux | 20 |
| `SoC` | System on Chip | 20 |
| `SSD` | Solid State Drive | 20 |
| `UEFI` | Unified Extensible Firmware Interface | 20 |
| `UEM` | Unified Endpoint Management | 20 |
| `UTM` | Unified Threat Management | 20 |
| `VDE` | Virtual Desktop Environment | 20 |
| `VDI` | Virtual Desktop Infrastructure | 20 |
| `VM` | Virtual Machine | 20 |

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

## Supplementary concepts

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

The following entries are from the CompTIA appendix. Duplicate abbreviations are intentionally retained where CompTIA lists more than one meaning. The expansion is preserved as printed, including wording that may differ from common technical usage.

| Acronym | Official expansion | Source PDF page |
|---|---|---:|
| `BYOD` | Bring Your Own Device | 17 |
| `CAPTCHA` | Completely Automated Public Turing Test to Tell Computers and Humans Apart | 17 |
| `CCTV` | Closed-circuit Television | 17 |
| `COPE` | Corporate Owned, Personally Enabled | 17 |
| `CYOD` | Choose Your Own Device | 17 |
| `HVAC` | Heating, Ventilation Air Conditioning | 18 |
| `PTZ` | Pan-tilt-zoom | 19 |
| `UPS` | Uninterruptable Power Supply | 20 |

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

## Supplementary concepts

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

The following entries are from the CompTIA appendix. Duplicate abbreviations are intentionally retained where CompTIA lists more than one meaning. The expansion is preserved as printed, including wording that may differ from common technical usage.

| Acronym | Official expansion | Source PDF page |
|---|---|---:|
| `DPO` | Data Privacy Officer | 17 |
| `FDE` | Full Disk Encryption | 18 |
| `GDPR` | General Data Protection Regulation | 18 |
| `NDA` | Non-disclosure Agreement | 19 |
| `PHI` | Personal Health Information | 19 |
| `PII` | Personally Identifiable Information | 19 |
| `SQL` | Structured Query Language | 20 |
| `XML` | Extensible Markup Language | 20 |

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

## Supplementary concepts

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

The following entries are from the CompTIA appendix. Duplicate abbreviations are intentionally retained where CompTIA lists more than one meaning. The expansion is preserved as printed, including wording that may differ from common technical usage.

| Acronym | Official expansion | Source PDF page |
|---|---|---:|
| `ALE` | Annualized Loss Expectancy | 17 |
| `ARO` | Annualized Rate of Occurrence | 17 |
| `AUP` | Acceptable Use Policy | 17 |
| `BCP` | Business Continuity Planning | 17 |
| `BIA` | Business Impact Analysis | 17 |
| `BPA` | Business Partners Agreement | 17 |
| `COOP` | Continuity of Operation Planning | 17 |
| `CP` | Contingency Planning | 17 |
| `DRP` | Disaster Recovery Plan | 18 |
| `MOA` | Memorandum of Agreement | 18 |
| `MOU` | Memorandum of Understanding | 18 |
| `MSA` | Master Service Agreement | 18 |
| `MTBF` | Mean Time Between Failures | 18 |
| `MTTF` | Mean Time to Failure | 18 |
| `MTTR` | Mean Time to Recover | 19 |
| `PCI DSS` | Payment Card Industry Data Security Standard | 19 |
| `RPO` | Recovery Point Objective | 19 |
| `RTO` | Recovery Time Objective | 19 |
| `SLA` | Service-level Agreement | 20 |
| `SLE` | Single Loss Expectancy | 20 |
| `SOW` | Statement of Work | 20 |
| `WO` | Work Order | 20 |

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

## Exam traps

- SAST = static/no execution; DAST = running application; SCA = third-party component/dependency analysis.
- UAT = user/business acceptance, not a security certification.
- API key ≠ robust user identity; enforce authorization on every object/action.
- XML is a data format; XML parser configuration can create XXE risk.
- SQLi prevention uses parameterized queries; XSS prevention uses context-aware output encoding/safe DOM handling.
- SDLC security is continuous, not a final-stage scan only.

## Supplementary concepts

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

The following entries are from the CompTIA appendix. Duplicate abbreviations are intentionally retained where CompTIA lists more than one meaning. The expansion is preserved as printed, including wording that may differ from common technical usage.

| Acronym | Official expansion | Source PDF page |
|---|---|---:|
| `API` | Application Programming Interface | 17 |
| `BASH` | Bourne Again Shell | 17 |
| `DBA` | Database Administrator | 17 |
| `HTML` | Hypertext Markup Language | 18 |
| `OID` | Object Identifier | 19 |
| `RACE` | Research and Development in Advanced Communications Technologies in Europe | 19 |
| `RAD` | Rapid Application Development | 19 |
| `SDLC` | Software Development Lifecycle | 19 |
| `SDLM` | Software Development Lifecycle Methodology | 19 |
| `UAT` | User Acceptance Testing | 20 |
| `VBA` | Visual Basic | 20 |

---

**Study rule:** learn the technical distinction in the explanation above, then use the official acronym list as a recognition checklist. Do not memorize an acronym expansion as a substitute for understanding the mechanism.
