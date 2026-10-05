---
name: external-attack-surface-explainer
description: Explains external attack-surface findings about a vendor or organisation — TLS and certificate issues, email authentication (SPF, DKIM, DMARC), DNS, exposed ports and services, outdated software and CVEs, leaked credentials, web security headers, breach history — in plain business language, with what to ask the vendor. Use when the user shares a scan result, security rating or finding and asks what it means, whether it matters, or how to raise it with the vendor.
---

# External attack-surface explainer

Turn a technical finding from an external scan or security rating into something a vendor
risk manager can act on: what it is, why it matters for this relationship, how sure we are,
and what to ask.

Only interpret findings the user provides. Do not run, script or suggest active scanning,
probing or exploitation of a third party's systems — that requires the owner's written
authorisation.

## 1. For each finding, answer four questions

1. **What is it?** One or two plain sentences, no jargon.
2. **Why does it matter?** The realistic consequence: what an attacker could do, and what
   it would mean for the user's data or service.
3. **How sure are we?** External findings are often wrong about ownership or severity. Name
   the likely false positives (see section 3).
4. **What should we ask?** One question to send the vendor, and the evidence that would
   close the finding.

## 2. Common findings

| Finding | Plain meaning | Typical concern |
| --- | --- | --- |
| Expired, self-signed or weak TLS certificate; old TLS versions (1.0/1.1) | Connections to the site may be readable or spoofable | Data in transit, user trust |
| Missing or permissive SPF, DKIM or DMARC (`p=none`) | Others can send email that appears to come from the vendor's domain | Phishing and invoice fraud using the vendor's name |
| Exposed remote access or database ports (RDP, SSH, SMB, databases, admin panels) | A door to internal systems is visible from the internet | Ransomware and data theft often start here |
| Outdated software or known CVEs | Public software with published weaknesses | Higher if the CVE is listed in CISA's Known Exploited Vulnerabilities catalogue |
| Leaked credentials | Employee logins appeared in a public breach dump | Account takeover, especially without MFA |
| Missing web security headers (HSTS, CSP, X-Frame-Options) | Browser-side protections are not switched on | Usually low on its own; context matters |
| Dangling DNS or subdomain takeover risk | A subdomain points to a resource nobody owns any more | Attackers can host content on the vendor's domain |
| Past breach or incident | The vendor was publicly reported as breached | Ask how it was handled and what changed |

## 3. Confidence checks

Before treating a finding as real, consider:

- **Ownership** — is the IP address, domain or subdomain actually the vendor's, or shared
  hosting, a CDN, a parked domain or a marketing agency's site?
- **Relevance** — does the asset relate to the service the user buys? A finding on a
  brochure website matters less than one on the product login.
- **Freshness** — when was it observed? It may already be fixed.
- **Compensating controls** — an exposed port may be restricted by an allow-list, or a
  service may require MFA.

Say plainly when confidence is low, and phrase the vendor question as verification rather
than accusation.

## 4. Output

For one finding, answer the four questions in section 1 in a short paragraph each.

For several, give a table — finding, plain meaning, business impact, confidence, question
for the vendor — ordered by impact, then a two-sentence overall view of the vendor's
external hygiene. Explain impact in terms of this relationship; avoid quoting raw scores
without explaining them.
