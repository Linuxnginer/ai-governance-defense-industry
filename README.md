# AI Governance & Defense Industry

NIST AI RMF • NIST AI 600-1 • CMMC • NIST SP 800-171

[ARCHITECTURE DIAGRAM]

A conceptual reference architecture exploring secure enterprise
GenAI access, AI governance, and cybersecurity considerations
for defense-related environments.

## Documentation

- Architecture Overview
- Data Flow
- AI RMF Mapping
- GenAI Risk Assessment
- CMMC / NIST 800-171 Mapping

The project brings together concepts from:

NIST AI RMF
NIST AI 600-1 — Generative AI Profile
CMMC Level 2
NIST SP 800-171
Zero Trust
Identity & Access Management
Enterprise GenAI security
Architecture

The reference architecture demonstrates a controlled path from an authorized user to an enterprise GenAI service:

User → Identity & Conditional Access → Zero Trust → Firewall → OpenWebUI → AI Security Controls → Azure OpenAI → Approved Model

The architecture focuses on controlling access, protecting sensitive information, monitoring activity, and establishing governance around enterprise AI usage.

AI Governance

The documentation maps the architecture to the four NIST AI RMF functions:

GOVERN — policies, accountability, roles, and AI governance
MAP — AI system context, data, stakeholders, and risks
MEASURE — testing, evaluation, monitoring, and risk measurement
MANAGE — risk mitigation, response, human oversight, and continuous improvement
Defense Industry Considerations

The project also explores how GenAI security controls can support environments that handle Controlled Unclassified Information (CUI) and operate under CMMC / NIST SP 800-171 requirements.

Disclaimer

This is a conceptual reference and learning project. It is not a production architecture, security assessment, CMMC certification, or representation of any specific defense contractor's environment.

The goal is to provide a starting point that others can learn from, adapt, and build upon when exploring secure enterprise GenAI and AI governance.

Repository

See the docs/ directory for the detailed AI RMF, GenAI risk, CMMC/NIST, architecture, and data-flow documentation.
