# Security and Vulnerability Management Prompts
*Aligned with OWASP Top Ten 2021, NIST SP 800-53, and MITRE ATT&CK frameworks for robust security practices.*

This category includes prompts to identify, assess, and remediate security vulnerabilities, ensure secure coding, and manage secrets. Each prompt is designed to be actionable, neutral, and adaptable to any codebase, with references to industry standards for prioritization and implementation.

## 1. Holistic Security Audit and Automated Remediation
Act as a Senior Security Engineer adhering to OWASP Top Ten 2021 and NIST SP 800-53. Conduct a comprehensive audit of the codebase to identify vulnerabilities, including injection attacks (SQL, XSS), broken authentication, sensitive data exposure, security misconfigurations, insecure deserialization, and known vulnerable components. Detect hardcoded secrets, API keys, or credentials using tools like TruffleHog or equivalent regex patterns. Implement automated fixes for high-confidence issues (e.g., escaping inputs, updating libraries). Flag complex vulnerabilities (e.g., business logic flaws) with detailed explanations referencing CWE IDs. Provide a prioritized remediation plan with code snippets and secure configuration examples. Apply changes directly where safe.  
**Usage**: Run in an IDE with static analysis tools (e.g., SonarQube, Semgrep) or integrate with SAST pipelines.  
**Standards**: OWASP Top Ten A01-A10, NIST SP 800-53 (SC-7, IA-5), CWE Top 25.

## 2. Secure Coding Practices and Dependency Audit
Review the codebase for compliance with secure coding standards (e.g., CERT Secure Coding, OWASP Secure Coding Practices). Assess authentication, authorization, input validation, data sanitization, encryption (e.g., TLS 1.3, AES-256), logging, and error handling. Identify outdated or vulnerable dependencies using tools like Dependabot or OWASP Dependency-Check. Recommend updates to secure versions, alternative libraries, or removal of unused dependencies. Highlight secure code patterns as exemplars. Structure the response with sections for vulnerabilities, dependency status, secure coding assessment, and actionable recommendations with code snippets.  
**Usage**: Apply during code reviews, pre-commit hooks, or CI/CD security scans.  
**Standards**: OWASP Secure Coding Practices, NIST SP 800-53 (SI-7), MITRE ATT&CK (T1190).

## 3. Secrets Management and Secure Storage
Scan the code repository for embedded secrets (e.g., API keys, passwords, tokens) using regex patterns or tools like GitGuardian. Remove detected secrets securely and implement storage solutions like environment variables, secret vaults (e.g., AWS Secrets Manager, HashiCorp Vault), or Kubernetes Secrets. Provide configuration examples and migration steps. Recommend least-privilege access controls for secret retrieval.  
**Usage**: Use in pre-commit hooks or repository scans to prevent secret leaks.  
**Standards**: OWASP A04:2021 (Insecure Design), NIST SP 800-53 (AC-6, IA-5).

## 4. Input Validation and Injection Prevention
Audit user input handling (forms, APIs, CLI) for validation and sanitization gaps per OWASP Injection Prevention Cheat Sheet. Identify risks like SQL injection, XSS, or command injection. Refactor to use parameterized queries, input whitelisting, and libraries like DOMPurify. Provide annotated code examples and test cases to validate fixes.  
**Usage**: Integrate with unit tests or dynamic analysis tools (e.g., OWASP ZAP).  
**Standards**: OWASP A03:2021 (Injection), CWE-89, CWE-79.

## 5. Authentication and Authorization Fortification
Evaluate authentication (e.g., OAuth 2.1, OpenID Connect) and authorization (e.g., RBAC, ABAC) mechanisms against NIST 800-63B guidelines. Identify weaknesses in session management, token handling (e.g., JWT security), or password hashing (e.g., use Argon2 or bcrypt). Implement secure cookies with HttpOnly, Secure, and SameSite attributes. Provide corrected code examples and configuration snippets.  
**Usage**: Apply to authentication modules or during security audits.  
**Standards**: OWASP A07:2021 (Authentication Failures), NIST 800-63B, CWE-287.

## 6. Secure Logging and Error Handling
Review logging and error handling to prevent sensitive data exposure (e.g., stack traces, PII) per OWASP Logging Cheat Sheet. Implement structured logging (e.g., JSON format) and secure storage (e.g., encrypted log sinks). Provide examples for anonymizing sensitive data and handling errors without leaking information.  
**Usage**: Use in logging frameworks or error-handling middleware.  
**Standards**: OWASP A09:2021 (Logging Failures), NIST SP 800-53 (AU-2, AU-3).

## 7. Security Test Suite Development
Develop automated security tests for vulnerabilities, secrets exposure, session integrity, and injection vectors using frameworks like OWASP ZAP or Burp Suite. Include manual testing procedures for complex scenarios (e.g., business logic flaws). Provide integration instructions for CI/CD pipelines and code snippets for unit tests targeting security-critical areas.  
**Usage**: Integrate into CI/CD pipelines or run locally for security validation.  
**Standards**: OWASP Testing Guide, NIST SP 800-53 (CA-8), CWE-1215.

## 8. Zero Trust Architecture Integration
Assess the codebase for alignment with Zero Trust principles (e.g., NIST SP 800-207). Implement continuous verification for all requests, micro-segmentation for APIs, and mutual TLS authentication. Provide configuration examples for identity providers (e.g., Keycloak) and policy enforcement points.  
**Usage**: Apply to distributed systems or cloud-native applications.  
**Standards**: NIST SP 800-207, OWASP A01:2021 (Broken Access Control).

---

*Last updated: July 12, 2025*
(edited)















