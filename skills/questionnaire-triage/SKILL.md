---
name: questionnaire-triage
description: Reviews a completed vendor security questionnaire (SIG, CAIQ, VSA, HECVAT or a custom one) and flags weak, missing, contradictory or unsupported answers, with a follow-up question and the evidence to request for each. Use when the user shares or pastes questionnaire responses, asks whether a vendor's answers are acceptable, or wants follow-up questions for a vendor.
---

# Questionnaire triage

Find the answers that need a follow-up, so a reviewer spends time on the gaps instead of
reading every "Yes". Treat the questionnaire as the vendor's claims, not as verified facts.

## 1. Read the input

Accept a pasted table, a spreadsheet or a document. For each question, capture the question,
the answer, any comment, and any evidence the vendor referenced. If the user gives the
vendor's tier or the data it handles, weigh findings against it — a gap in encryption matters
far more for a vendor holding regulated data.

## 2. Check every answer for these problems

| Problem | Example |
| --- | --- |
| **Unsupported claim** | "Yes, we encrypt all data" with no detail or evidence |
| **Vague answer** | "Industry standard", "as appropriate", "where applicable" |
| **N/A without reason** | "N/A" on a control that clearly applies to the service |
| **Contradiction** | "No subprocessors" but cloud hosting is mentioned elsewhere |
| **Policy without practice** | A policy exists, but nothing says it is enforced, tested or reviewed |
| **Stale evidence** | Certificate, audit or penetration test older than 12 months, or expired |
| **Scope gap** | Certification scope does not cover the product or location in use |
| **Plain "No"** | A control is missing outright |

## 3. Domains to cover

Group findings by domain, and note any domain the questionnaire did not ask about at all:

- Governance and security policy
- Asset and data management, including data classification and retention
- Identity and access management: MFA, privileged access, joiners and leavers
- Encryption in transit and at rest, and key management
- Vulnerability management and patching
- Secure development, for software vendors
- Logging, monitoring and incident response, including breach notification timelines
- Business continuity and disaster recovery
- Third-party (fourth-party) management and subprocessors
- Physical security, where relevant
- Privacy and regulatory compliance
- Independent assurance: SOC 2, ISO/IEC 27001, penetration testing

Where it helps the reader, name the related area of a public framework (ISO/IEC 27001
Annex A, NIST CSF 2.0, SOC 2 Trust Services Criteria). Name the area, not a clause number
you are unsure of.

## 4. Rate each finding

| Severity | Use when |
| --- | --- |
| **High** | A missing or failing control that could directly expose the data or service in scope |
| **Medium** | The control exists but is weak, unproven or partly in scope |
| **Low** | A documentation or hygiene gap with little direct exposure |

## 5. Output

1. **Summary** — two or three sentences: overall quality of the responses and the biggest concerns.
2. **Findings table** — domain, question (short), answer (short), problem, severity,
   follow-up question to send, evidence to request. High severity first.
3. **Not covered** — domains the questionnaire skipped that matter for this vendor.
4. **Recommendation** — accept, accept with conditions, or hold pending answers.

Write follow-up questions so they can be sent to the vendor unchanged: specific, one ask per
question, and answerable with a fact or a document. Never invent answers the vendor did not
give; if a response is missing, list it as missing.
