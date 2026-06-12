# Security Governance Framework
## Acme Cloud Services
**Document ID:** GOV-FRAMEWORK-001
**Version:** 1.1
**Owner:** CISO
**Aligned To:** NIST CSF 2.0
**Last Reviewed:** 2024-10-01

---

## 1. Framework Overview

Acme Cloud Services' Security Governance Framework defines the architecture of the enterprise cybersecurity program. It establishes how the six functions of NIST CSF 2.0 — Govern, Identify, Protect, Detect, Respond, and Recover — are operationalized within the organization's specific business context.

This framework serves as the architectural blueprint that connects governance intent (the Charter) to operational execution (policies, controls, and procedures).

---

## 2. NIST CSF 2.0 Alignment Model

### 2.1 Function Mapping

| CSF Function | Primary Owner | Supporting Owner | Program Component |
|---|---|---|---|
| **GOVERN** | CISO | Board / CEO | Governance program, charter, committee structure |
| **IDENTIFY** | GRC Analyst | IT Operations | Asset management, risk register, supply chain |
| **PROTECT** | IT Operations | Engineering | IAM, data security, platform controls, training |
| **DETECT** | Security Operations | IT Operations | SIEM, EDR, vulnerability management, monitoring |
| **RESPOND** | Security Operations | Legal / Comms | IR plan, playbooks, communications |
| **RECOVER** | IT Operations | Engineering | BCP, DR, resilience testing |

### 2.2 Govern Function (New in CSF 2.0)

NIST CSF 2.0 elevated Govern to a first-class function, recognizing that governance is the foundation from which all other functions derive. Acme's program implements the Govern function through:

**GV.OC — Organizational Context**
- Annual review of mission, stakeholder expectations, and regulatory obligations
- Legal and compliance register maintained by VP Legal
- Customer contract security requirements tracked and assessed annually

**GV.RM — Risk Management Strategy**
- Board-approved risk appetite statement
- Documented risk scoring methodology (NIST SP 800-30)
- Enterprise risk register reviewed quarterly
- Risk treatment strategies formally documented for all High/Medium risks

**GV.RR — Roles, Responsibilities, and Authorities**
- RACI matrix maintained for all governance activities
- Security job descriptions include cybersecurity responsibilities
- Executive accountability documented in governance charter

**GV.PO — Policy**
- Policy library of 7 core policies, reviewed annually
- Policy exception process documented and enforced
- All policies version-controlled in GRC platform

**GV.OV — Oversight**
- Quarterly CGC reviews with documented minutes
- Annual program effectiveness assessment
- Board receives quarterly CISO briefings

**GV.SC — Cybersecurity Supply Chain Risk Management**
- Vendor risk tiering framework (Tier 1–4)
- Annual assessments for Tier 1/2 vendors
- Security requirements in all vendor contracts

---

## 3. Program Maturity Model

Acme's program uses a 5-level maturity model to assess and track program improvement:

| Level | Name | Description |
|---|---|---|
| 1 | Initial | Ad hoc; undocumented; reactive |
| 2 | Developing | Partially documented; inconsistently applied |
| 3 | Defined | Documented; consistently applied; owned |
| 4 | Managed | Measured; metrics-driven; proactive |
| 5 | Optimizing | Continuous improvement; benchmarked; automated |

**Target Maturity Levels by Function:**

| CSF Function | Current Maturity | 12-Month Target | 24-Month Target |
|---|---|---|---|
| Govern | 2 | 3 | 4 |
| Identify | 2 | 3 | 4 |
| Protect | 3 | 4 | 4 |
| Detect | 2 | 3 | 4 |
| Respond | 2 | 3 | 4 |
| Recover | 1 | 2 | 3 |

---

## 4. Control Architecture

The framework uses a three-layer control architecture:

### 4.1 Layer 1 — Governance Controls
- Policies, standards, and procedures
- Risk appetite and tolerance statements
- Governance committee oversight
- Executive accountability structures

### 4.2 Layer 2 — Operational Controls
- Technical security configurations
- Access management and identity controls
- Vulnerability management and patching
- Security monitoring and alerting

### 4.3 Layer 3 — Assurance Controls
- Control effectiveness testing
- Internal and external audits
- Penetration testing
- Compliance assessments

---

## 5. Metrics and Performance Measurement

### 5.1 Key Performance Indicators (KPIs)

| KPI | Metric | Target | Frequency |
|---|---|---|---|
| Policy Coverage | % employees acknowledging policies | 100% | Annual |
| MFA Adoption | % accounts with MFA enabled | 100% | Monthly |
| Vulnerability SLA | % critical vulns patched within SLA | 100% | Monthly |
| Awareness Training | % completion rate | 100% | Annual |
| Control Implementation | % controls implemented | 85% | Quarterly |

### 5.2 Key Risk Indicators (KRIs)

| KRI | Metric | Threshold | Frequency |
|---|---|---|---|
| Open High Risks | Count of High/Critical open risks | > 5 triggers escalation | Monthly |
| Overdue Remediation | Count of past-due remediation items | > 3 triggers escalation | Monthly |
| Failed Control Tests | % controls failing operational effectiveness | > 20% triggers review | Quarterly |
| Vendor Assessment Overdue | Count of expired Tier 1/2 assessments | > 0 triggers escalation | Monthly |
| Privileged Accounts | Count of active privileged accounts | > 60 triggers review | Monthly |

---

## 6. Integration with Enterprise Risk Management

The cybersecurity governance framework is integrated with Acme's enterprise risk management (ERM) program through:

- Cybersecurity risk register feeds into the enterprise risk register
- CISO participates in quarterly ERM committee meetings
- Top cybersecurity risks included in Board ERM reporting
- Risk appetite for cybersecurity aligned with enterprise risk appetite
- Cyber insurance coverage reviewed annually against risk register

---

## 7. Continuous Improvement Process

```
Plan → Do → Check → Act (PDCA)
  ↓       ↓       ↓        ↓
Strategy  Controls  Assess  Remediate
Charter   Deploy    Test    Improve
Policies  Train     Audit   Update
```

**Annual Review Activities:**
- Framework gap assessment vs. NIST CSF 2.0 current profile
- Peer benchmarking against similar SaaS companies
- Lessons learned from incidents and near-misses
- Threat landscape review (emerging risks and threat actors)
- Customer security requirement review
- Regulatory landscape review (new and changing obligations)
