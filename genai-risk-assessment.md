GenAI Risk Assessment

Quick reference for common risks when deploying enterprise GenAI in defense-industry environments.

Note: Conceptual reference only. This is not a formal security or compliance assessment.

Risk	Impact	Example Mitigation
CUI / sensitive data exposure	🔴 High	Data classification, DLP, access controls
Prompt injection	🔴 High	Input controls, testing, monitoring
Hallucination / inaccurate output	🟠 Medium–High	Human review, evaluation, validation
Unauthorized access	🔴 High	IAM, MFA, conditional access, Zero Trust
Data leakage	🔴 High	Network controls, DLP, logging
Model/provider risk	🟠 Medium–High	Approved providers, vendor assessment
AI supply-chain risk	🟠 Medium–High	Review models, plugins, APIs, dependencies
Overreliance on AI	🟠 Medium	User training, human oversight
Malicious/unsafe output	🟠 Medium–High	Output validation, monitoring
Configuration changes	🟡 Medium	Change management, testing, approval
Key Controls

The architecture can help address these risks through:

Identity & access management
Zero Trust / ZTNA
Network segmentation
Data governance
Approved AI services
Logging & monitoring
Security testing
Human oversight
Incident response
Risk Management

AI risks should be reviewed continuously as:

Models change → threats evolve → new use cases appear → controls are updated

Related Frameworks
NIST AI RMF
NIST AI 600-1 Generative AI Profile
CMMC Level 2
NIST SP 800-171

Goal: Provide a quick starting point for identifying and discussing GenAI risks before deployment.
