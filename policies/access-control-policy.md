# Access Control Policy
## Acme Cloud Services
**Document ID:** POL-AC-001
**Version:** 2.0
**Classification:** Internal – Restricted
**Owner:** CISO
**Last Reviewed:** 2024-09-15
**Next Review:** 2025-09-15
**Approved By:** CGC

---

## 1. Purpose

This Access Control Policy establishes the requirements for managing logical access to Acme Cloud Services information systems, data, and network resources. The policy ensures that access is granted based on business need, the principle of least privilege, and the concept of need-to-know, aligned with Zero Trust architecture principles.

---

## 2. Scope

This policy applies to:
- All information systems, applications, databases, cloud platforms, and network resources owned or managed by Acme
- All user accounts, service accounts, system accounts, and privileged accounts
- All employees, contractors, and third parties with access to Acme systems
- Identity providers including Azure Active Directory (Entra ID) and AWS IAM
- All access methods including direct login, VPN, API keys, and service-to-service authentication

---

## 3. Roles and Responsibilities

| Role | Responsibility |
|---|---|
| CISO | Policy ownership and enforcement |
| IT Operations Manager | Access provisioning, review management, technical controls |
| System Owners | Approving access to their systems; participating in access reviews |
| HR | Triggering joiner/mover/leaver process; communicating personnel changes |
| Managers | Requesting and approving access for direct reports; certifying access reviews |
| Users | Using only authorized access; reporting unauthorized access |

---

## 4. Policy Statements

### 4.1 Access Authorization and Provisioning

**4.1.1 Access Request Process**
All access to Acme systems must be formally requested, approved, and documented before provisioning. Access requests must include:
- System or resource being requested
- Business justification for access
- Access level required (read, write, admin)
- Duration (permanent or time-limited)
- Approved by: the user's manager AND the system owner

Access is provisioned only by authorized IT Operations staff following receipt of documented approval.

**4.1.2 Least Privilege**
Users must be granted the minimum level of access required to perform their job function. Broad or administrative access must be justified by specific business need and approved by the system owner. Role-based access control (RBAC) is the preferred mechanism for access provisioning.

**4.1.3 Separation of Duties**
Where feasible, access roles must enforce separation of duties to prevent any single individual from having the ability to perform conflicting functions (e.g., approving and executing financial transactions; developing and deploying production code without independent review).

**4.1.4 Default Deny**
New user accounts have no access by default. Access is added incrementally based on documented business need. Systems must be configured to deny access unless explicitly permitted.

### 4.2 User Account Management

**4.2.1 Unique Accounts**
Each user must have a unique, individually assigned account. Shared accounts are prohibited except where technically unavoidable, in which case a formal exception must be approved by the CISO.

**4.2.2 Account Types**
Acme maintains the following account types:

| Account Type | Description | Requirements |
|---|---|---|
| Standard User | Regular employee/contractor access | MFA required |
| Privileged User | IT admin, security, or elevated access | MFA required; PAW preferred; activity logged |
| Service Account | Application-to-application authentication | No interactive login; rotated credentials; owner assigned |
| Emergency/Break-Glass | Emergency administrative access | Sealed credential; dual authorization to open; all activity reviewed |
| Contractor/Vendor | Third-party access | Time-limited; MFA required; scoped to specific systems |
| Guest | Temporary access for visitors or evaluators | Expires after 30 days; no access to sensitive systems |

**4.2.3 Joiner Process**
New employees and contractors receive access on or after their official start date. HR must notify IT Operations no less than 2 business days prior to a new start. Access is provisioned to role-based access groups as approved by the hiring manager. System-specific access beyond role defaults requires separate authorization.

**4.2.4 Mover Process**
When an employee changes roles, the following must occur within 2 business days:
- Previous role access revoked
- New role access provisioned
- Manager notification to IT Operations of role change is required

**4.2.5 Leaver Process (Termination)**
Upon notification of employee departure (voluntary or involuntary):
- **Involuntary termination:** All access revoked immediately at time of termination
- **Voluntary termination:** All access revoked on last day of employment
- Active directory account disabled; shared mailbox access removed
- Physical and logical access badges/credentials deactivated
- Company devices collected prior to or on last day
- HR is responsible for notifying IT Operations of all departures

IT Operations must confirm account deprovisioning within 4 business hours of notification. HR and IT Operations jointly maintain an offboarding checklist.

### 4.3 Privileged Access Management

**4.3.1 Privileged Account Controls**
Privileged accounts (local admin, domain admin, Azure Global Admin, AWS root/admin) are subject to:
- Just-in-time (JIT) provisioning preferred; standing privileged access requires CGC approval
- Multi-factor authentication mandatory — hardware token or authenticator app (not SMS)
- Privileged Access Workstation (PAW) use strongly recommended for all domain and cloud admin activity
- All privileged session activity logged to a separate, tamper-resistant log repository
- Privileged accounts must not be used for email, web browsing, or non-administrative tasks

**4.3.2 Privileged Account Inventory**
IT Operations maintains an up-to-date inventory of all privileged accounts. The inventory is reviewed monthly. Maximum allowed privileged accounts: 50 total across all systems and platforms.

**4.3.3 Service Account Governance**
Service accounts must:
- Have a named human owner responsible for the account
- Use a managed identity or secrets manager where technically feasible (not hardcoded credentials)
- Have credentials rotated at least every 90 days
- Be documented in the service account register with purpose, owner, and rotation schedule

### 4.4 Multi-Factor Authentication (MFA)

MFA is required for:
- All user accounts accessing Acme systems
- All VPN connections
- All cloud console access (Azure Portal, AWS Console)
- All administrative functions
- All access to systems processing customer data or Confidential/Restricted data

MFA methods in order of preference:
1. Hardware security key (FIDO2 / YubiKey)
2. Authenticator application (Microsoft Authenticator, Google Authenticator)
3. Push notification via authenticator app
4. TOTP (time-based one-time password)

SMS-based MFA is not permitted for privileged accounts or access to Confidential/Restricted data due to SIM-swap risk. SMS may be used as a fallback for standard user accounts only with CISO approval.

### 4.5 Remote Access

- All remote access to internal systems must use an approved VPN (Microsoft Always On VPN or approved equivalent)
- Split-tunnel VPN is not permitted for access to sensitive systems
- Remote Desktop Protocol (RDP) and SSH must not be exposed directly to the internet; access is through VPN or jump host only
- Cloud console and M365 access from managed devices does not require VPN but must use conditional access policies enforced via Azure AD

### 4.6 Third-Party and Vendor Access

- Vendor access is provisioned only upon completion of a signed security addendum and vendor risk assessment
- Vendor access is time-limited (default: 90 days; must be renewed with business justification)
- Vendor accounts are subject to MFA requirements
- Vendor access must be scoped to specific systems required for their engagement only
- Vendor sessions may be recorded for critical systems; vendors are informed of this in their contract
- Vendor accounts are reviewed monthly by the Vendor Risk Working Group

### 4.7 Access Reviews

**Periodic Access Reviews:**
- Standard user access: Reviewed by managers quarterly
- Privileged user access: Reviewed by IT Operations and CISO monthly
- Service account inventory: Reviewed by IT Operations monthly
- Vendor/contractor access: Reviewed monthly by system owners

Managers who do not complete access reviews within the designated window are escalated to their VP. The CGC reviews access review completion rates quarterly.

**Access Review Process:**
1. IT Operations exports access list for each system
2. Manager/system owner reviews and certifies or removes access
3. IT Operations executes approved removals within 2 business days
4. Results documented in GRC platform

### 4.8 Authentication Standards

- Password requirements are defined in the Password Policy (POL-PW-001)
- Session timeouts: 15 minutes inactivity for privileged accounts; 60 minutes for standard accounts
- Account lockout: 5 failed attempts triggers 30-minute lockout; 10 failed attempts triggers manual unlock by IT
- Authentication logs retained for minimum 12 months

---

## 5. Exceptions

Exceptions to this policy require written request submitted to CISO. Shared accounts, non-MFA access, and extended privilege standing require quarterly exception review by the CGC.

---

## 6. Enforcement

Violations including unauthorized access, shared credentials, or provisioning access without approval are grounds for disciplinary action up to and including termination and referral to law enforcement.

---

## 7. Review Cycle

Annual review by CISO; immediate review following any access-related security incident or significant environment change.

---

## 8. Related Documents

- Password Policy (POL-PW-001)
- Vendor Risk Management Policy (POL-VRM-001)
- Incident Response Policy (POL-IR-001)
- Data Classification Policy (POL-DC-001)
- Acceptable Use Policy (POL-AUP-001)
