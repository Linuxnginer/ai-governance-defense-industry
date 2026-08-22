NIST AI RMF Mapping

Quick reference showing how this GenAI architecture can support the NIST AI RMF, NIST AI 600-1, and defense-industry security considerations.

Note: This is a conceptual reference project, not a compliance certification or production architecture.

AI RMF
Function	Architecture / Governance Examples
GOVERN	AI policies, approved use cases, roles, access control, accountability
MAP	Users, data, system boundaries, stakeholders, AI risks
MEASURE	Security testing, AI evaluation, monitoring, logging
MANAGE	Risk mitigation, human oversight, incident response, continuous improvement
GenAI Risks

Key areas to consider:

Prompt injection
Sensitive data / CUI exposure
Hallucination and unreliable outputs
Privacy
Unauthorized access
Model/provider risk
AI supply-chain risk
Human overreliance
Defense Industry Alignment

The architecture can support considerations related to:

CMMC Level 2
NIST SP 800-171
Zero Trust
Identity & Access Management
Audit & Accountability
System & Communications Protection
Configuration Management
System & Information Integrity
Quick Relationship
NIST AI RMF
     │
     ├── AI Governance
     ├── AI Risk
     └── GenAI Management
             │
             ▼
       Secure AI Architecture
             │
             ├── Zero Trust
             ├── IAM
             ├── Network Security
             └── Monitoring
                    │
                    ▼
          CMMC / NIST 800-171


Goal: Provide a quick starting point for organizations exploring secure enterprise GenAI and AI governance in defense-related environments.

Status: Reference / learning project — not a compliance determination.
