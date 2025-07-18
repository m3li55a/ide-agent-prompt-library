
# Snowflake GDPR/CCPA Compliance Review Checklist

## Objective
Conduct a comprehensive compliance review of the current Snowflake implementation, specifically for **GDPR and CCPA**.

---

## 1. Data Handling and PII Management

### Tasks:
- Identify and classify PII stored in Snowflake (e.g., name, email, IP address, user identifiers).
- Evaluate anonymization or pseudonymization:
  - Are masking policies, external tokenization, or hashing used?
  - Are **Dynamic Data Masking** and **Row Access Policies** enforced?
- Review consent management mechanisms:
  - Is there a `user_consent` or equivalent metadata table?
  - Are queries/processes gated by consent status?

### ✅ Action:
Provide SQL queries or metadata inspection queries to validate these.

---

## 2. Encryption Validation

### Data at Rest:
- Confirm Snowflake's default **AES-256** encryption is active.
- Check if **customer-managed keys (CMK)** or **Snowflake-managed keys (SMK)** are used.

### Data in Transit:
- Verify **TLS 1.2+** is enforced for all client and API connections.

### ✅ Action:
Include configuration checks or documentation references to confirm.

---

## 3. GDPR Compliance Checklist

| Checklist Item | Status | Notes |
|----------------|--------|-------|
| PII classification complete | Pass/Fail |  |
| Masking/tokenization applied | Pass/Fail |  |
| Consent stored and managed | Pass/Fail |  |
| Consent-aware querying | Pass/Fail |  |
| Access controls (RBAC) enforced | Pass/Fail |  |
| Data encrypted at rest (AES-256) | Pass/Fail |  |
| TLS encryption in transit | Pass/Fai

## Complete prompt list below, when directing the agent, best practice is not to chain your prompts in one attempt, take a step-by-step approach which allows you to continue to fine-tune your input to accomplish the output desired.

As a senior GRC specialist, identify and classify PII data stored in Snowflake (e.g., name, email, IP address, identifiers). Specifically, answer the following:

## Assess PII anonymization or pseudonymization strategies:

Are masking policies, external tokenization, or hashing techniques used?

Are Dynamic Data Masking and Row Access Policies in place?

## Review consent management:

Is there metadata tracking of consent (e.g., in a user_consent table)?

Are queries or processes gated based on user consent?

## Action: Provide SQL queries or metadata checks to validate these practices.

## Encryption Validation

Confirm data-at-rest encryption:

Is Snowflake's default AES-256 encryption used?

Are customer-managed keys (CMK) or Snowflake-managed keys (SMK) configured?

Confirm data-in-transit encryption:

Validate that TLS 1.2 or higher is enforced for client connections and integrations.

## Action: Provide SQL/config checks to confirm these settings.

Compliance Checklist & Evaluation

## Generate a Snowflake-specific GDPR checklist covering:

PII discovery

Masking/tokenization

Consent control enforcement

Access control & RBAC

Encryption at rest/in transit

Logging & audit trail (QUERY_HISTORY, ACCESS_HISTORY)

## Action: For each item, mark Pass or Fail, and explain why.

Remediation Recommendations
For each “Fail”, provide:

A concise description of the issue.

Recommended changes (e.g., masking policy, UDF for hashing).

SQL/code samples to implement the fix.
