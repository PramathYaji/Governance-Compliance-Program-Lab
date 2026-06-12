# Enterprise Cybersecurity Governance Program
### Acme Cloud Services | SOC 2 Readiness & NIST CSF 2.0 Alignment

![Governance](https://img.shields.io/badge/Framework-NIST%20CSF%202.0-blue)
![CIS](https://img.shields.io/badge/Controls-CIS%20v8-green)
![SOC2](https://img.shields.io/badge/Compliance-SOC%202%20Type%20II-orange)
![Status](https://img.shields.io/badge/Status-Active-brightgreen)

---

## Executive Summary

This repository documents a complete enterprise cybersecurity governance program designed and implemented for **Acme Cloud Services**, a 500-employee SaaS company with $75M in annual revenue. The engagement focused on two primary objectives: preparing the organization for SOC 2 Type II certification and establishing a formal cybersecurity governance program aligned with NIST CSF 2.0 and CIS Controls v8.

The program encompasses a full governance charter, seven enterprise security policies, a 40+ item risk register, control mapping across three frameworks, gap analysis findings, and board-level executive reporting. All deliverables were developed as if performed during an active consulting engagement and are intended to demonstrate GRC practitioner competency at the Governance Analyst, Risk Analyst, and Junior GRC Consultant level.

---

## Business Scenario

**Client:** Acme Cloud Services
**Industry:** Software-as-a-Service (SaaS)
**Employees:** 500
**Annual Revenue:** $75M
**Headquarters:** Austin, TX

**Technology Environment:**
- Microsoft 365 (Exchange Online, SharePoint, Teams, Intune)
- Azure Cloud (primary production hosting)
- Amazon Web Services (secondary workloads, DR)
- Active Directory / Azure Active Directory
- Customer-facing web applications (multi-tenant SaaS platform)
- Fully remote workforce (500 employees, 12 countries)

**Business Trigger:**
Acme Cloud Services received a formal request from three enterprise customers requiring evidence of SOC 2 Type II certification within 18 months as a condition of contract renewal. The CISO and VP of Engineering escalated this to the Board, which authorized a formal GRC program buildout. A governance analyst was engaged to design and implement the program from the ground up.

**Engagement Constraints:**
- No existing formal security governance program
- No documented risk register or risk treatment framework
- Partial policy library (outdated, unreviewed policies)
- No control framework mapping
- No audit readiness documentation
- 18-month customer deadline for SOC 2 Type II

---

## Governance Objectives

1. Establish a formal cybersecurity governance charter and committee structure
2. Develop and publish a complete enterprise security policy library
3. Build and maintain an enterprise risk register with ownership and treatment plans
4. Map existing and planned controls to NIST CSF 2.0, CIS Controls v8, and SOC 2 TSCs
5. Conduct a gap analysis to identify compliance deficiencies and prioritization
6. Implement control effectiveness testing and remediation tracking
7. Produce board-level risk reporting and executive dashboards
8. Build an audit-ready evidence repository using CISO Assistant and OpenGRC

---

## Frameworks Used

| Framework | Version | Purpose |
|---|---|---|
| NIST Cybersecurity Framework | 2.0 | Primary governance and control structure |
| CIS Controls | v8 | Prescriptive technical and operational controls |
| SOC 2 Trust Services Criteria | 2017 (Updated) | Certification preparation and compliance mapping |
| NIST SP 800-30 | Rev 1 | Risk assessment methodology |
| NIST SP 800-53 | Rev 5 | Supporting control reference |

---

## Project Methodology

The engagement followed a structured five-phase methodology modeled on industry-standard GRC consulting practice:

### Phase 1 — Discovery & Scoping (Weeks 1–3)
- Stakeholder interviews with CISO, CTO, VP Engineering, VP Operations, Legal Counsel
- Asset inventory review and environment documentation
- Policy and documentation gap analysis (preliminary)
- Existing control identification via questionnaires and system walk-throughs
- Scope definition for SOC 2 system boundary

### Phase 2 — Governance Framework Design (Weeks 4–6)
- Governance charter development and stakeholder review
- Security committee structure design
- Policy library development (7 core policies)
- Roles and responsibilities matrix creation
- Governance meeting cadence and escalation path defined

### Phase 3 — Risk Assessment (Weeks 7–10)
- Risk assessment methodology documentation
- Risk universe development by category
- Likelihood and impact scoring with risk owners
- Inherent and residual risk calculation
- Risk treatment strategy assignment
- Executive risk register review and approval

### Phase 4 — Control Mapping & Gap Analysis (Weeks 11–16)
- NIST CSF 2.0 control mapping (60+ controls)
- CIS Controls v8 mapping and maturity scoring
- SOC 2 TSC crosswalk development
- Control effectiveness assessment (50+ controls tested)
- Gap analysis findings development and prioritization

### Phase 5 — Reporting & Remediation (Weeks 17–20)
- Remediation tracker build and owner assignment
- Board risk report development
- KPI/KRI dashboard creation
- CISO Assistant and OpenGRC platform configuration
- Evidence repository organization

---

## Risk Assessment Approach

Risk scoring follows **NIST SP 800-30 Rev 1** qualitative methodology adapted for enterprise GRC practice:

```
Risk Score = Likelihood × Impact
```

| Score | Likelihood | Impact |
|---|---|---|
| 1 | Very Unlikely (once per 5+ years) | Negligible (minimal operational impact) |
| 2 | Unlikely (once per 2–5 years) | Minor (limited operational impact) |
| 3 | Possible (once per year) | Moderate (significant operational impact) |
| 4 | Likely (multiple times per year) | Major (serious business impact) |
| 5 | Very Likely (monthly or more) | Critical (existential business impact) |

| Risk Level | Score Range |
|---|---|
| Low | 1–5 |
| Medium | 6–12 |
| High | 13–25 |

Risk owners were assigned at the business unit level. Treatment strategies follow the standard Accept / Mitigate / Transfer / Avoid taxonomy with documented rationale.

---

## Compliance Mapping Approach

Control mapping was performed using a unified control framework approach:

1. **Anchor Framework:** NIST CSF 2.0 (Govern, Identify, Protect, Detect, Respond, Recover)
2. **Prescriptive Layer:** CIS Controls v8 mapped to each NIST CSF control
3. **Compliance Layer:** SOC 2 TSCs (Security, Availability, Confidentiality) mapped as applicable
4. **Implementation Status:** Implemented / Partially Implemented / Not Implemented / Not Applicable
5. **Maturity Level:** CIS IG1 / IG2 / IG3 used as maturity indicator

Where a control satisfied requirements across multiple frameworks, it was documented once and cross-referenced — reducing control sprawl and enabling efficient audit evidence collection.

---

## Governance Deliverables

### Governance Framework
| Deliverable | Description |
|---|---|
| `governance-charter.md` | 6-page governance charter with authority, scope, and committee structure |
| `governance-committee-structure.md` | Detailed committee membership, roles, and meeting cadences |
| `security-governance-framework.md` | Program-level governance model aligned to NIST CSF 2.0 |

### Policies
| Policy | Description |
|---|---|
| `acceptable-use-policy.md` | AUP covering all Acme assets and systems |
| `access-control-policy.md` | IAM policy aligned to least privilege and Zero Trust principles |
| `password-policy.md` | Password standards including MFA requirements |
| `incident-response-policy.md` | IR policy with NIST 800-61 aligned lifecycle |
| `vendor-risk-management-policy.md` | Third-party risk program policy |
| `change-management-policy.md` | Change control policy for production systems |
| `data-classification-policy.md` | Four-tier data classification scheme |

### Risk Management
| Deliverable | Description |
|---|---|
| `enterprise-risk-register.xlsx` | 40+ risks across 10 categories with scoring, treatment, and ownership |
| `risk-management-policy.md` | Enterprise risk management policy |
| `risk-treatment-plan.md` | Detailed treatment actions for High and Medium risks |
| `risk-assessment-methodology.md` | Documented scoring methodology and process |

### Compliance Mapping
| Deliverable | Description |
|---|---|
| `nist-csf-control-mapping.xlsx` | 60+ controls mapped to NIST CSF 2.0 functions and categories |
| `cis-controls-mapping.xlsx` | CIS Controls v8 with implementation status and maturity |
| `soc2-crosswalk.xlsx` | SOC 2 TSC compliance matrix |
| `gap-analysis-report.md` | 10 High + 10 Medium findings with remediation roadmap |

### Control Assessments
| Deliverable | Description |
|---|---|
| `control-assessment-results.xlsx` | 50+ controls tested for design and operational effectiveness |
| `remediation-tracker.xlsx` | 25 remediation actions with owner, priority, and status |
| `control-testing-methodology.md` | Testing approach, sampling criteria, and evidence standards |

### Executive Reporting
| Deliverable | Description |
|---|---|
| `board-risk-report.md` | Board-level risk briefing document |
| `executive-summary.md` | Program status executive summary |
| `compliance-dashboard.xlsx` | Visual compliance status dashboard |
| `security-kpi-kri-dashboard.md` | KPI/KRI metrics with targets and actuals |

---

## Key Findings

**Risk Posture:**
- 12 High risks identified across Identity & Access, Cloud Security, and Third-Party Risk categories
- 18 Medium risks with active remediation plans
- Top risk: Inadequate MFA coverage on privileged accounts (Likelihood 5 × Impact 5 = 25)

**Compliance Gaps:**
- **NIST CSF:** 34% of controls Not Implemented; 28% Partially Implemented
- **CIS Controls:** 18 of 56 safeguards at IG1 not yet implemented
- **SOC 2:** 14 Common Criteria gaps requiring remediation before audit readiness

**Control Testing:**
- 52 controls assessed; 61% rated Effective, 23% Partially Effective, 16% Ineffective
- Highest failure rate: Detection controls (Detect function — 40% ineffective)
- Logging and monitoring gaps identified across Azure, AWS, and on-premises environments

**Quick Wins Identified:**
- MFA enforcement for all M365 users (2-week implementation)
- Privileged Access Workstation policy for admin accounts
- Automated vulnerability scanning for internet-facing assets
- Vendor security questionnaire process (CAIQ-based)

---

## Lessons Learned

1. **Governance Before Technology:** Building the charter and committee structure first created the authority needed to enforce policy adoption. Without executive sponsorship documented formally, policy compliance is aspirational at best.

2. **Risk Register as a Living Document:** Initial resistance from business owners changed once they saw the risk register used in board reporting. Ownership becomes real when executives are named publicly.

3. **Control Overlap is a Feature, Not a Bug:** Mapping NIST CSF, CIS, and SOC 2 together revealed that ~60% of controls satisfy multiple frameworks simultaneously. This dramatically reduced the audit evidence burden.

4. **Gap Analysis Drives Prioritization:** Organizations often want to "do everything." The gap analysis forced a conversation about acceptable risk, finite resources, and sequencing — which produced a realistic 18-month roadmap rather than a wish list.

5. **Detection is Consistently Underfunded:** Across 12 engagements, detection and response capabilities are consistently the weakest. Acme's investment pattern — heavy on prevention, light on detection — is industry-typical and industry-dangerous.

---

## Skills Demonstrated

| Skill Area | Specifics |
|---|---|
| **Governance Design** | Charter development, committee structure, RACI, policy authoring |
| **Risk Management** | NIST 800-30 methodology, risk register, treatment planning, ownership |
| **Compliance Mapping** | NIST CSF 2.0, CIS Controls v8, SOC 2 TSC crosswalk |
| **Control Assessment** | Design effectiveness, operational effectiveness, evidence evaluation |
| **GRC Tooling** | CISO Assistant, OpenGRC platform configuration and workflow |
| **Executive Reporting** | Board presentations, KPI/KRI dashboards, risk trending |
| **Policy Development** | 7 enterprise-grade security policies with full lifecycle |
| **Gap Analysis** | Current state assessment, findings development, remediation roadmaps |

---

## Tools & Technologies

- **GRC Platforms:** CISO Assistant, OpenGRC
- **Frameworks:** NIST CSF 2.0, CIS Controls v8, SOC 2 TSC, NIST SP 800-30, NIST SP 800-53
- **Documentation:** Markdown, Microsoft Excel
- **Environment Assessed:** Microsoft 365, Azure, AWS, Active Directory

---

*This repository was developed as a professional portfolio project demonstrating enterprise GRC competency. All company names, personnel, and specific data points are fictional.*
