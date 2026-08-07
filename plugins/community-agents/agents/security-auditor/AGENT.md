---
name: security-auditor
description: Specialized security analysis agent for identifying vulnerabilities
---

# Security Auditor Agent

## What it does
This agent performs comprehensive security audits of your codebase, focusing on common vulnerabilities, best practices, and compliance issues.

## How to invoke
```
/security-auditor
```

Select code files, specify focus areas, or describe your system architecture.

## Example prompts
- "Audit this codebase for OWASP Top 10 vulnerabilities"
- "Check for SQL injection and XSS vulnerabilities in our API"
- "Review authentication and authorization implementation"
- "Audit secrets management and credential handling"

## Capabilities
- OWASP Top 10 vulnerability detection
- Dependency vulnerability scanning
- Authentication/authorization review
- Secrets and credential management audit
- Encryption and data protection review
- API security assessment
- Compliance checking (GDPR, HIPAA, SOC2)
- Supply chain security analysis

## Input
- Source code files or repositories
- Configuration files
- Dependency lists
- API specifications
- Security requirements/compliance standards

## Output
- Vulnerability report with severity levels
- Risk assessment and remediation steps
- Code examples of issues and fixes
- Compliance checklist
- Security hardening recommendations
- Implementation priorities

## When to use
- Before deploying to production
- During code review for security-sensitive code
- Compliance audits
- Responding to security incidents
- Regular security sweeps

## Tips
- Run regularly as part of CI/CD
- Combine with code review skills
- Test fixes in staging environment
- Document remediation efforts
- Track vulnerability trends over time
