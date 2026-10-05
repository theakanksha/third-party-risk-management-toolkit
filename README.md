# Third-Party Risk Management Toolkit

A Claude plugin for third-party (vendor) risk management. It helps security, procurement and
GRC teams decide how much scrutiny a vendor needs, review the vendor's security
questionnaire, understand external attack-surface findings, and ask the vendor to fix what
matters. It works from what you share in the conversation and needs no account, API key or
connector.

## Skills

| Skill | What it does |
| --- | --- |
| `vendor-risk-tiering` | Scores a vendor's inherent risk on data sensitivity, access and business impact, assigns Tier 1–4, and recommends the matching due diligence |
| `questionnaire-triage` | Reviews a completed SIG, CAIQ, VSA, HECVAT or custom questionnaire and flags unsupported, vague, contradictory or missing answers, with follow-up questions |
| `external-attack-surface-explainer` | Explains scan or security-rating findings (TLS, SPF/DKIM/DMARC, exposed services, CVEs, leaked credentials) in business terms, with confidence checks |
| `remediation-request-writer` | Drafts a remediation email or ticket with severities, due dates and closure evidence, plus reminder and escalation versions |

## Example prompts

- "We're onboarding a payroll SaaS that will hold employee bank details and connect to our
  HR system over an API. What tier is it and what should we ask for?"
- "Here are a vendor's CAIQ answers. Which ones need a follow-up?"
- "Our scan says the vendor's domain has DMARC set to p=none and RDP open on one IP. Does
  that matter for a marketing-analytics vendor?"
- "Write a remediation request to the vendor for these three findings, response due in
  five business days."

## Install

From Anthropic's directory: search for **Third-Party Risk Management Toolkit** on claude.ai
or in Cowork and add it. It also loads in Claude Code through account sync.

From this repository in Claude Code:

```bash
claude plugin marketplace add theakanksha/third-party-risk-management-toolkit
claude plugin install third-party-risk-management-toolkit@third-party-risk-management-toolkit
```

## Notes

- The rubrics, due dates and severity levels are common starting points. Replace them with
  your organisation's own policy where one exists; the skills use yours when you share it.
- The output supports a risk decision; it is not legal, audit or compliance advice.
- The plugin only interprets findings you provide. It does not scan or probe any third
  party's systems.
- No data leaves the conversation: the plugin contains instructions only, with no scripts,
  connectors or network calls.

## License

[MIT](LICENSE)
