# cybersecurity-vapt-capstone
A hands-on vulnerability assessment and penetration testing project conducted in a controlled DVWA lab, documenting security findings, risk ratings, and remediation recommendations.
# Cybersecurity Capstone Project
## Vulnerability Assessment and Penetration Testing (VAPT)

### Project Overview
This capstone project involved conducting a vulnerability assessment and controlled penetration testing exercise against an intentionally vulnerable web application in a local lab environment.

The objective was to identify security weaknesses, validate their impact, assess associated risks, and provide practical remediation recommendations.

### Lab Environment
- **Operating System:** Kali Linux
- **Target Application:** Damn Vulnerable Web Application (DVWA)
- **Deployment:** Local Docker-based lab
- **Tools:** Nmap, Burp Suite
- **Assessment Type:** Web Application Vulnerability Assessment and Penetration Testing

### Scope
The assessment focused on:
- Reconnaissance and service identification
- Web application enumeration
- Vulnerability identification and validation
- Controlled exploitation in the lab
- Risk assessment using CVSS
- Security recommendations and reporting

All testing was performed in an authorized, isolated lab environment.

### Key Findings
| Finding | Risk |
|---|---|
| Exposed configuration backup containing database credentials | High |
| SQL Injection | Medium |
| OS Command Injection | Medium |
| Directory listing in `/docs/` | Informational |

### Technical Highlights
- Identified an exposed configuration backup containing database credentials.
- Validated SQL Injection and retrieved database-related information.
- Confirmed OS Command Injection by executing `whoami` in the application context, which returned `www-data`.
- Identified directory listing enabled on the `/docs/` path.
- Documented findings, impact, risk ratings, and remediation guidance.

### Methodology
1. Reconnaissance
2. Service and application enumeration
3. Vulnerability identification
4. Controlled validation
5. Risk assessment
6. Documentation and remediation recommendations

### Risk Assessment
Findings were evaluated using the Common Vulnerability Scoring System (CVSS v3.1). Risk ratings reflect the observed behavior and impact within the lab environment.

### MITRE ATT&CK Mapping
Relevant techniques considered during the assessment include:

- **T1190** — Exploit Public-Facing Application
- **T1059** — Command and Scripting Interpreter
- **T1552.001** — Credentials In Files

These mappings provide context for the observed attack techniques and are not claims of a separate detection or incident-response exercise.

### Remediation Summary
- Remove exposed backup files from web-accessible directories.
- Rotate any credentials found in exposed files.
- Use parameterized queries to prevent SQL Injection.
- Avoid passing user input directly to operating system commands.
- Disable directory listing where it is not required.
- Apply secure configuration and access-control practices.

### Project Deliverables
- Capstone assessment report
- Findings summary
- Testing methodology
- Supporting screenshots and evidence
- Risk ratings and remediation recommendations

### Disclaimer
This project was conducted solely for educational purposes in a controlled and intentionally vulnerable lab. No unauthorized systems were tested.
