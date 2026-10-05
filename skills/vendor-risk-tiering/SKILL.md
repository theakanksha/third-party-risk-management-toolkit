---
name: vendor-risk-tiering
description: Assigns a third party (vendor, supplier, SaaS provider, contractor) an inherent-risk tier from 1 to 4 and recommends the matching depth of due diligence. Use when the user is onboarding a vendor, asks how risky a vendor is, asks which questionnaire or assessment a vendor needs, or wants to prioritise a vendor inventory.
---

# Vendor risk tiering

Tier a third party by its **inherent risk** — the risk it brings before any controls are
assessed — so that due-diligence effort goes where it matters. The tier drives what to ask
for next, not a judgement of whether the vendor is secure.

## 1. Gather the facts

Ask only for what is missing. If the user already described the vendor, extract the answers
and confirm them in one short list rather than re-asking.

| Factor | What to find out |
| --- | --- |
| Data | What data the vendor stores, processes or can see: none, internal, confidential, regulated (personal data, health, payment card, financial) |
| Volume | Roughly how many records or people are affected |
| Access | Network or system access: none, user-level SaaS login, API integration, privileged or on-premise access |
| Criticality | What breaks, and how fast, if the vendor is unavailable for a day or a week |
| Substitutability | How hard it would be to replace the vendor |
| Regulatory scope | Whether the service falls under a regulation or contractual obligation (for example GDPR, HIPAA, PCI DSS, DORA, SOX) |
| Fourth parties | Whether the vendor relies on its own subcontractors for this service |
| Geography | Where data is stored and where the vendor operates |

If the user cannot answer a factor, assume the higher-risk value and say so.

## 2. Score

Score each dimension 0–3, then take the tier from the **highest** applicable rule. A single
severe factor is enough to raise the tier — do not average it away.

| Score | Data sensitivity | Access | Business impact |
| --- | --- | --- | --- |
| 0 | No company data | No access | Negligible |
| 1 | Internal, non-sensitive | User-level SaaS login | Minor inconvenience |
| 2 | Confidential, or small volumes of personal data | API or system integration | A business process degrades |
| 3 | Regulated data, or large volumes of personal data | Privileged, network-level or physical access | A critical service stops, or a regulatory breach |

| Tier | Rule | Meaning |
| --- | --- | --- |
| **1 – Critical** | Any dimension scores 3 | Full due diligence before contract |
| **2 – High** | Any dimension scores 2 | Standard due diligence |
| **3 – Moderate** | Any dimension scores 1 | Light-touch review |
| **4 – Low** | All dimensions score 0 | Register only |

Raise the tier by one (to a maximum of Tier 1) when the vendor is hard to replace **and**
scores 2 on business impact, or when the service is in regulatory scope.

## 3. Recommend the due diligence

| Tier | Assessment | Evidence to request | Reassess |
| --- | --- | --- | --- |
| 1 | Full questionnaire (for example SIG Core or CAIQ) plus a review call | SOC 2 Type II or ISO/IEC 27001 certificate with scope, latest penetration test summary, business continuity and incident response plans, subprocessor list | Annually, plus continuous monitoring |
| 2 | Standard questionnaire (for example SIG Lite) | SOC 2 or ISO 27001 report, or equivalent policies | Every 1–2 years |
| 3 | Short questionnaire or attestation | Security policy or trust-centre link | Every 2–3 years |
| 4 | None | — | On contract change |

## 4. Output

Reply with:

1. **Tier** and one sentence on why.
2. **Score table** — each dimension, its score, and the fact that drove it.
3. **Assumptions** — every factor you assumed instead of being told.
4. **Next steps** — the assessment and evidence from section 3.
5. **What would change the tier** — the one or two facts that, if different, would move it.

Keep the rubric visible so the user can disagree with a single score instead of the whole
result. This is a starting point for the organisation's own risk policy; if the user has a
policy with different tiers or thresholds, use theirs.
