CMMC / NIST SP 800-171 Mapping

Quick-reference mapping of the architecture to selected NIST SP 800-171 Rev. 2 requirements used by CMMC Level 2.

Informational reference only. This document is not a CMMC assessment, certification, compliance determination, or production security assessment.

Access Control (AC)
Control	Requirement	Architecture Support
3.1.1	Limit system access to authorized users, processes, and devices	IAM, security groups, Conditional Access, Zero Trust
3.1.2	Limit system access to authorized transactions and functions	Role-based access and application permissions
3.1.3	Control CUI flow	Data classification, network boundaries, AI access controls
3.1.5	Employ least privilege	Security groups, restricted administration, role-based access
3.1.7	Prevent non-privileged users from executing privileged functions	Administrative separation and IAM
3.1.12	Monitor and control remote access sessions	Cloudflare ZTNA / controlled remote access
3.1.13	Cryptographically protect remote access sessions	HTTPS / encrypted remote access
Identification & Authentication (IA)
Control	Requirement	Architecture Support
3.5.1	Identify system users, processes, and devices	Enterprise identity provider
3.5.2	Authenticate organizational users and devices	IAM / authentication controls
3.5.3	Use multifactor authentication	MFA / Conditional Access
3.5.7	Enforce minimum password complexity	Enterprise identity policy
3.5.10	Store and transmit only cryptographically protected passwords	Protected identity infrastructure
Audit & Accountability (AU)
Control	Requirement	Architecture Support
3.3.1	Create and retain system audit logs	Application, identity, network, and security logging
3.3.2	Ensure users can be uniquely traced to actions	Enterprise identity / authenticated sessions
3.3.3	Review and update logged events	SIEM / security monitoring
3.3.4	Alert on audit-processing failures	Monitoring / security alerts
3.3.5	Correlate audit records	Centralized logging / SIEM
3.3.8	Protect audit information	Access-controlled logging infrastructure
Configuration Management (CM)
Control	Requirement	Architecture Support
3.4.1	Establish and maintain baseline configurations	Documented architecture and configurations
3.4.2	Establish and enforce security configuration settings	Firewall, IAM, ZTNA, application configuration
3.4.3	Track, review, approve, and document changes	Change-management process
3.4.4	Analyze security impact of changes	Change-review process
3.4.6	Employ least functionality	Approved services, models, and integrations
3.4.8	Implement deny-by-default / allow-by-exception	Firewall and network restrictions
System & Communications Protection (SC)
Control	Requirement	Architecture Support
3.13.1	Monitor and control communications at system boundaries	Firewall / Zero Trust / network controls
3.13.2	Employ architectural designs to protect CUI	Segmentation / controlled AI path
3.13.5	Implement subnetworks for publicly accessible components	Network segmentation
3.13.8	Protect CUI during transmission	HTTPS / encrypted connections
3.13.11	Terminate network connections at the end of sessions	ZTNA / application session controls
3.13.16	Protect CUI at rest	Encryption / approved storage
System & Information Integrity (SI)
Control	Requirement	Architecture Support
3.14.1	Identify, report, and correct system flaws	Vulnerability management
3.14.2	Provide protection from malicious code	Endpoint/security controls
3.14.3	Monitor security alerts and advisories	SIEM / security monitoring
3.14.6	Monitor inbound and outbound communications	Firewall / network monitoring
3.14.7	Identify unauthorized use	IAM / logging / monitoring
Risk Assessment (RA)
Control	Requirement	Architecture Support
3.11.1	Periodically assess security risks	GenAI risk assessment
3.11.2	Scan for vulnerabilities	Vulnerability management
3.11.3	Remediate vulnerabilities according to risk	Risk-based remediation
Security Assessment (CA)
Control	Requirement	Architecture Support
3.12.1	Periodically assess security controls	Security assessment process
3.12.2	Develop plans to correct deficiencies	Remediation / POA&M process
3.12.3	Monitor security controls continuously	Continuous monitoring
3.12.4	Develop and maintain system security plans	Architecture and security documentation
AI / GenAI Considerations

The architecture also introduces AI-specific risks that should be considered alongside traditional cybersecurity controls:

Risk	Relevant Areas
CUI submitted to AI	AC, SC, MP, SI
Prompt injection	SI, RA, CA
Sensitive information in outputs	AC, SC, SI
Unauthorized AI usage	AC, IA, AU
Model/provider risk	RA, SA, SR
AI supply-chain risk	RA, SA, SR
Hallucination / unreliable output	RA, CA, AI RMF
Excessive AI permissions	AC, IA
Insufficient logging	AU, SI
Human overreliance	AT, RA, AI RMF
Additional CMMC Readiness Considerations

The architecture is only one part of a broader security program. A real assessment would also consider:

System Security Plan (SSP)
Asset inventory
CUI identification and scoping
Policies and procedures
Access reviews
MFA configuration
Configuration baselines
Network and firewall configurations
Vulnerability management
Security logs
Incident response
Risk assessments
Security assessments
Remediation tracking
Training records
Supplier and service-provider considerations
Framework Relationship
NIST AI RMF
     │
     ├── AI Governance
     ├── AI Risk Management
     └── GenAI Risk
             │
             ▼
      Secure AI Architecture
             │
             ├── IAM
             ├── Zero Trust
             ├── Network Security
             ├── Monitoring
             └── Data Protection
                     │
                     ▼
             CMMC / NIST 800-171


This document is intended as an informational quick reference showing how enterprise GenAI architecture concepts can relate to cybersecurity requirements relevant to defense-industry environments.

References
NIST SP 800-171 Rev. 2
NIST SP 800-171A
CMMC Level 2
NIST AI RMF
NIST AI 600-1 — Generative AI Profile
