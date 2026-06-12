# Cybersecurity Governance Committee Structure
## Acme Cloud Services
**Document ID:** GOV-COMMITTEE-001
**Version:** 1.0
**Owner:** CISO
**Last Reviewed:** 2024-10-01

---

## 1. Overview

This document provides the detailed operating structure for the Cybersecurity Governance Committee (CGC) and its subordinate working groups as established by the Cybersecurity Governance Charter (GOV-CHARTER-001).

---

## 2. Governance Hierarchy

```
Board of Directors
└── Audit Committee
    └── CISO (Executive Sponsor)
        └── Cybersecurity Governance Committee (CGC)
            ├── IAM Working Group
            ├── Cloud Security Working Group
            ├── Vendor Risk Working Group
            └── Incident Response Working Group
```

---

## 3. CGC Operating Procedures

### 3.1 Meeting Agenda Template (Quarterly)

**Standing Agenda Items:**
1. Approval of prior meeting minutes (5 min)
2. Risk Register Review — New, changed, or closed risks (20 min)
3. Control Assessment Update — Testing results and gaps (15 min)
4. Remediation Tracker Status — Open items, blockers, escalations (15 min)
5. Compliance Status — SOC 2, NIST CSF program metrics (10 min)
6. Policy Review — Any policies due for review (10 min)
7. Open Issues / Exception Requests (10 min)
8. Action Items and Owners (5 min)

### 3.2 Voting Procedures

- Decisions require simple majority of voting members present
- CISO holds tie-breaking authority
- Abstentions are permitted and recorded
- All votes are documented in meeting minutes

### 3.3 Documentation Requirements

- Meeting minutes published within 5 business days
- Action items tracked in GRC platform
- Decisions documented with rationale
- Materials distributed 5 business days prior to meeting

---

## 4. Working Group Charters

### 4.1 Identity and Access Management Working Group

**Purpose:** Oversee the implementation and effectiveness of identity and access management controls across all Acme Cloud Services environments.

**Membership:**
| Role | Member |
|---|---|
| Chair | IT Operations Manager |
| Member | Azure/M365 Administrator |
| Member | HR Representative |
| Member | Application Security Lead |
| Advisor | CISO (as needed) |

**Meeting Cadence:** Bi-weekly

**Key Responsibilities:**
- Review and update IAM policies and procedures
- Monitor privileged access reviews (quarterly minimum)
- Oversee user lifecycle management (joiner/mover/leaver process)
- Manage MFA deployment and enforcement
- Review access exception requests
- Track IAM-related findings from control assessments

**Key Metrics Owned:**
- MFA adoption rate (target: 100% all users)
- Privileged account count (target: < 50 total)
- Orphaned account elimination rate
- Access review completion rate (target: 100% quarterly)
- Time-to-deprovision for terminated employees (target: same business day)

---

### 4.2 Cloud Security Working Group

**Purpose:** Maintain and improve the security posture of Acme Cloud Services' Azure and AWS cloud environments.

**Membership:**
| Role | Member |
|---|---|
| Chair | Lead Cloud Architect |
| Member | Azure Security Engineer |
| Member | AWS Administrator |
| Member | DevSecOps Lead |
| Advisor | CTO (as needed) |

**Meeting Cadence:** Bi-weekly

**Key Responsibilities:**
- Monitor cloud security posture management (CSPM) findings
- Manage cloud configuration baseline standards
- Oversee container and Kubernetes security
- Review and approve cloud architecture changes with security implications
- Track vulnerability remediation for cloud-hosted assets
- Manage cloud native security tooling (Defender for Cloud, AWS Security Hub)

**Key Metrics Owned:**
- Cloud security posture score (target: > 85/100 in CSPM tool)
- Critical cloud misconfigurations open (target: 0)
- Storage buckets with public access (target: 0)
- Encryption coverage for data at rest (target: 100%)
- Network segmentation compliance (target: 100%)

---

### 4.3 Vendor Risk Working Group

**Purpose:** Manage the security risk posed by third-party vendors, suppliers, and partners who access, process, or store Acme Cloud Services data.

**Membership:**
| Role | Member |
|---|---|
| Chair | VP Legal / Procurement Lead |
| Member | GRC Analyst |
| Member | Finance Representative |
| Member | Engineering Liaison |
| Advisor | CISO (for high-risk vendors) |

**Meeting Cadence:** Monthly

**Key Responsibilities:**
- Maintain the vendor inventory and risk tiering
- Conduct annual security assessments for Tier 1 vendors
- Review vendor SOC 2 reports, ISO 27001 certificates, and security questionnaires
- Ensure security requirements are in all vendor contracts
- Track vendor security incidents and breaches
- Manage subprocessor disclosures for GDPR/CCPA compliance

**Vendor Risk Tiers:**
| Tier | Definition | Review Frequency |
|---|---|---|
| Tier 1 | Access to customer PII or production systems | Annual + event-triggered |
| Tier 2 | Access to internal sensitive data or corporate systems | Annual |
| Tier 3 | Access to non-sensitive internal systems only | Every 2 years |
| Tier 4 | No data access (generic commodity suppliers) | Questionnaire only |

**Key Metrics Owned:**
- Vendor assessment completion rate (target: 100% for Tier 1/2 annually)
- Vendors with expired assessments (target: 0)
- Vendors without security addendum in contract (target: 0)
- Open vendor security findings (target: 0 critical, < 5 high)

---

### 4.4 Incident Response Working Group

**Purpose:** Maintain Acme Cloud Services' readiness to detect, respond to, and recover from cybersecurity incidents.

**Membership:**
| Role | Member |
|---|---|
| Chair | Security Operations Lead |
| Member | IT Operations Manager |
| Member | Legal / Privacy Counsel |
| Member | VP Communications |
| Member | Engineering Lead On-call |
| Advisor | CISO |

**Meeting Cadence:** Monthly + post-incident as needed

**Key Responsibilities:**
- Maintain and update incident response playbooks
- Schedule and conduct tabletop exercises (minimum annually)
- Manage security tooling (SIEM, EDR, email security)
- Coordinate with threat intelligence sources
- Own the security incident log and post-incident reviews
- Manage relationships with IR retainer provider
- Conduct simulated phishing campaigns (quarterly)

**Playbooks Maintained:**
- Ransomware / Destructive Malware
- Business Email Compromise (BEC)
- Data Breach / Unauthorized Disclosure
- DDoS / Availability Attack
- Insider Threat
- Cloud Account Compromise
- Third-Party Breach Affecting Acme

**Key Metrics Owned:**
- Mean Time to Detect (MTTD) — target: < 4 hours for critical
- Mean Time to Respond (MTTR) — target: < 24 hours for critical
- Tabletop exercises completed (target: 2/year)
- Phishing simulation click rate (target: < 5%)
- Incident playbook currency (target: all reviewed within 12 months)

---

## 5. RACI Matrix

| Activity | Board | CEO | CISO | CGC | WG Chairs | Risk Owners | All Staff |
|---|---|---|---|---|---|---|---|
| Approve Charter | A | C | R | C | I | I | — |
| Approve Policies | I | I | R | A | C | C | I |
| Risk Acceptance (High) | A | C | R | A | I | I | — |
| Risk Acceptance (Medium) | I | I | A | C | I | R | — |
| Control Testing | — | — | A | C | R | C | — |
| Security Awareness Training | — | — | A | C | — | — | R |
| Incident Response | I | I | A | C | R | C | C |
| Policy Compliance | I | I | A | C | C | R | R |
| Vendor Assessments | — | — | A | C | R | C | — |
| Board Risk Reporting | A | I | R | C | I | I | — |

*R = Responsible, A = Accountable, C = Consulted, I = Informed*

---

## 6. Committee Communication Plan

| Audience | Frequency | Format | Owner |
|---|---|---|---|
| Board of Directors | Quarterly | Risk briefing presentation | CISO |
| Executive Team | Monthly | Risk report memo | CISO |
| CGC Members | Quarterly + monthly | Meeting agenda + materials | CISO / Program Manager |
| Working Group Members | Per working group cadence | Meeting notes + action tracker | WG Chair |
| All Employees | Quarterly | Security newsletter | Security Awareness Team |
| Customers (SOC 2 report) | Annually | SOC 2 Type II report | CISO + External Auditor |
