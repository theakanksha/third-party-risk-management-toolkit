---
name: remediation-request-writer
description: Drafts a clear, professional remediation request to a vendor — an email or ticket listing security findings with severity, due dates and the evidence needed to close each one — plus a follow-up or escalation version. Use when the user asks to write to a vendor about findings, questionnaire gaps or audit issues, or needs a remediation plan or reminder.
---

# Remediation request writer

Write a request a vendor can act on without a meeting: what is wrong, why it matters, what
"fixed" looks like, and by when. Firm on substance, courteous in tone — the goal is a fix and
an ongoing relationship.

## 1. Collect the inputs

- The findings: from the conversation, a questionnaire review, a scan or an audit.
- Vendor name, contact name and the service in scope.
- The sender's name and role.
- Any contractual right to request remediation (security schedule, right-to-audit clause).
  Mention it only if the user confirms one exists.
- Format: email (default) or ticket.

## 2. Set due dates

Use the user's policy if they have one. Otherwise propose these common defaults and say they
are adjustable:

| Severity | Respond with a plan | Remediate |
| --- | --- | --- |
| Critical | 2 business days | 15 days |
| High | 5 business days | 30 days |
| Medium | 10 business days | 90 days |
| Low | Next review | 180 days, or accept the risk |

Shorten Critical deadlines when the issue is actively exploited.

## 3. Write the request

Structure:

1. **Subject** — `Security remediation request: <vendor> – <n> findings (response by <date>)`
2. **Opening** — one or two sentences: the review that took place and why you are writing.
3. **Findings** — for each: a short title, severity, what was observed (facts only), why it
   matters for this relationship, the requested action, the evidence that closes it, and the
   due date. Use a table or numbered list.
4. **Asks** — confirm receipt, name an owner, and send a remediation plan by the response date.
5. **Close** — offer a call to clarify, and give a contact.

Rules:

- One finding, one ask. Do not bundle unrelated fixes.
- State observations, not accusations: "we observed", not "you failed".
- Ask for evidence, not reassurance: a screenshot of the configuration, an updated
  certificate, a retest report, or a policy with its approval date.
- Leave out internal scores, other vendors' details and the user's internal deliberations.

## 4. Offer the follow-ups

After the first draft, offer:

- **Reminder** — short, for when the response date passes with no reply.
- **Escalation** — for overdue Critical or High items, addressed to the vendor's account
  owner or security lead, restating the impact and the next step (for example a risk
  acceptance review, contract remedies or suspending the integration). Write it only
  when the user asks.
- **Tracker** — a table with finding, severity, owner, due date and status, for the user's own records.
