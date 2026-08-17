# AI Governance Defense Industry

## CMMC Level 2 / NIST SP 800-171 Rev. 2-Aligned AI Security Architecture

A reference architecture and evidence model for governing enterprise AI systems in defense and aerospace environments.

This project demonstrates how identity, access control, AI authorization, connector permissions, CUI data flows, auditability, and security documentation can be mapped to applicable **CMMC Level 2 / NIST SP 800-171 Rev. 2** security requirements.

> **Important:** This repository is a reference implementation. It does not constitute a CMMC certification, assessment, attestation, or guarantee of compliance.

---

## Objective

The objective is to demonstrate a traceable relationship between:

**Architecture → CMMC Requirement → Implementation → Evidence → Assessment Test → Readiness**

The project begins with an enterprise AI identity and access architecture based on:

```text
User
  │
  ▼
Microsoft Entra ID
  │
  ├── SSO
  ├── MFA
  ├── Conditional Access
  └── SCIM
  │
  ▼
Security Group
  │
  ▼
Enterprise AI Platform
  │
  ▼
AI Connectors
  │
  ▼
Authorized Data
```

The architecture is then extended with:

* CUI boundary definition
* CMMC control mapping
* Audit and accountability
* Evidence collection
* System Security Plan documentation
* Assessment procedures
* Readiness tracking

---

## Compliance Baseline

### Primary baseline

**CMMC Level 2**

Mapped against:

**NIST SP 800-171 Rev. 2**

The CMMC-oriented mapping uses the NIST SP 800-171 Rev. 2 requirement identifiers and control families.

Example:

```text
AC.L2-3.1.1
```

Where:

* `AC` = Access Control
* `L2` = CMMC Level 2
* `3.1.1` = NIST SP 800-171 Rev. 2 requirement

### Version note

NIST SP 800-171 Rev. 2 has been withdrawn and superseded by Rev. 3. This repository intentionally uses Rev. 2 for the primary CMMC Level 2 mapping and will maintain a separate Rev. 3 crosswalk rather than mixing requirement versions.

---

# Architecture

The architecture focuses on controlling AI access to protected enterprise information.

```text
                         USER
                           │
                           ▼
                 ┌──────────────────┐
                 │ Microsoft Entra  │
                 │       ID         │
                 │                  │
                 │ SSO              │
                 │ MFA              │
                 │ Conditional      │
                 │ Access           │
                 │ SCIM             │
                 └────────┬─────────┘
                          │
                          ▼
                 ┌──────────────────┐
                 │ Security Groups  │
                 │ / RBAC           │
                 └────────┬─────────┘
                          │
                          ▼
                 ┌──────────────────┐
                 │ Enterprise AI    │
                 │ Platform         │
                 └────────┬─────────┘
                          │
                          ▼
                 ┌──────────────────┐
                 │ AI Connectors    │
                 │ / APIs           │
                 └────────┬─────────┘
                          │
                          ▼
                 ┌──────────────────┐
                 │ Authorized CUI   │
                 │ Data Sources     │
                 └──────────────────┘

              ┌──────────────────────────┐
              │ Audit & Accountability   │
              │                          │
              │ Authentication events    │
              │ Authorization events     │
              │ AI activity              │
              │ Connector activity       │
              │ CUI access               │
              └──────────────────────────┘
```

---

# Control Families Demonstrated

## AC — Access Control

* `AC.L2-3.1.1` — Authorized access
* `AC.L2-3.1.2` — Authorized functions
* `AC.L2-3.1.3` — CUI flow enforcement
* `AC.L2-3.1.5` — Least privilege

## AU — Audit & Accountability

* `AU.L2-3.3.1` — Audit records
* `AU.L2-3.3.2` — Individual traceability

## IA — Identification & Authentication

* `IA.L2-3.5.3` — Multifactor authentication
* `IA.L2-3.5.6` — Disable identifiers/authenticators

## CA — Security Assessment

* `CA.L2-3.12.4` — System Security Plan

These requirements are part of the NIST SP 800-171 Rev. 2 control families and requirement structure.

---

# Evidence Model

Each mapped requirement follows the same evidence lifecycle:

```text
Requirement
     │
     ▼
Architecture Component
     │
     ▼
Technical Implementation
     │
     ▼
Evidence
     │
     ▼
Assessment Procedure
     │
     ▼
Readiness Status
```

Evidence may include:

* Configuration exports
* Access-control policies
* Security-group membership
* MFA policies
* Connector configurations
* Data-flow diagrams
* Authentication logs
* Authorization logs
* Audit records
* Access reviews
* System Security Plan
* Incident records
* Test results

The goal is not simply to document that a control exists, but to demonstrate how its implementation can be **verified**.

---

# CMMC Readiness

This repository uses the following readiness states:

| Status                 | Meaning                                                 |
| ---------------------- | ------------------------------------------------------- |
| `NOT_STARTED`          | No implementation or evidence established               |
| `PLANNED`              | Implementation approach defined                         |
| `IMPLEMENTED`          | Technical implementation exists                         |
| `EVIDENCE_READY`       | Required evidence has been collected                    |
| `ASSESSMENT_READY`     | Implementation and evidence are prepared for assessment |
| `REMEDIATION_REQUIRED` | Gap identified                                          |
| `NOT_APPLICABLE`       | Applicability formally determined and documented        |

`ASSESSMENT_READY` does **not** mean CMMC certified.

A CMMC assessment evaluates whether the applicable requirements have actually been implemented, supported by examination, interview, and testing activities. DoD assessment guidance emphasizes implementation rather than simply selecting a particular technology solution.

---

# Project Structure

```text
ai-governance-defense-industry/
│
├── README.md
│
├── architecture/
│   └── 01-iam-ai-cmmc.md
│
├── cmmc/
│   ├── AC-access-control.md
│   ├── AU-audit-accountability.md
│   ├── IA-identification-authentication.md
│   └── CA-security-assessment.md
│
├── evidence/
│   ├── AC/
│   ├── AU/
│   ├── IA/
│   └── CA/
│
└── mappings/
    ├── cmmc-control-matrix.md
    └── cmmc-readiness.md
```

---

# Scope

The initial implementation focuses on:

1. Enterprise identity
2. AI authorization
3. Least privilege
4. CUI data-flow control
5. Authentication
6. Auditability
7. User traceability
8. Identity lifecycle
9. System Security Plan documentation
10. Evidence readiness

Future phases will expand the mapping across the complete CMMC Level 2 requirement set.

---

## References

* NIST SP 800-171 Rev. 2
* NIST SP 800-171A
* CMMC Level 2 requirements
* DoD CMMC/DFARS policy

The official NIST publication identifies the SP 800-171 Rev. 2 control families and provides supplemental material including the security requirements and SSP templates.
