**Cloud Security Incident Response & PCI DSS Remediation (Google Cloud)**

**Project Overview**  
This project simulates a cloud security incident investigation using Google Cloud Security Command Center. The objective was to identify high-severity misconfigurations and remediate PCI DSS 3.2.1 compliance violations following a simulated breach scenario.


**Business Context** 

A multinational retail organization operating across 28 countries experienced potential exposure of cloud resources. A compliance-driven investigation was initiated to identify misconfigurations and reduce attack surface risk.


**Key Findings**

1. IAM Misconfiguration

- Default service account with excessive permissions
- Overly permissive API scopes

2. Network Security Exposure

- Public IP assigned to VM
- SSH (22) and RDP (3389) open to 0.0.0.0/0
- Firewall logging disabled

3. Storage Security Risk

- Public bucket ACL
- Uniform bucket-level access not enforced


**Remediation Actions**

- Rebuilt compromised VM from clean snapshot
- Removed public IP assignment
- Implemented IAP-restricted SSH access
- Enabled firewall logging
- Enforced uniform bucket-level access
- Revalidated compliance through Security Command Center


**Compliance Alignment**

- PCI DSS 3.2.1
- NIST Cybersecurity Framework
- ISO 27001 Control Domains (Access Control, Logging & Monitoring)


**Key Governance Takeaways**

- Cloud misconfigurations significantly increase breach probability
- Logging and monitoring are essential for audit defensibility
- Compliance validation must follow remediation
- IAM governance is foundational to cloud security maturity
