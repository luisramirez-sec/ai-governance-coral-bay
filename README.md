# AI Governance Program: Coral Bay Credit Union

An end-to-end AI governance, risk, and compliance project for a fictional 200-person credit union running AI in member service, lending, anti-money-laundering monitoring, and email security.

> Coral Bay Credit Union is a fictional company created for this project. All systems, vendors, and figures are illustrative.

## The scenario

| System | What it does | Risk tier |
| --- | --- | --- |
| Ask Coral | Member service chatbot on a vendor large language model; can look up balances | High |
| QuickDecision | Vendor model that recommends approve or decline on consumer loans | High |
| SentinelFlow | Machine learning model that scores transactions for anti-money-laundering alerts | High |
| Shadow AI | Staff pasting member data into public chatbots | High |
| MailShield | Email security tool using machine learning, initially missing from the inventory | Medium |

## Deliverables

| # | Deliverable | Framework or skill |
| --- | --- | --- |
| 1 | [AI inventory and shadow AI discovery plan](01-ai-inventory.md) | AI inventory, risk tiering |
| 2 | [System cards for Ask Coral and QuickDecision](02-system-cards.md) | NIST AI Risk Management Framework (Map) |
| 3 | [Regulatory classification memo](03-classification-memo.md) | Equal Credit Opportunity Act and Regulation B, Fair Credit Reporting Act, Gramm-Leach-Bliley Act, Colorado SB 26-189, EU AI Act |
| 4 | [Acceptable use policy, AI governance policy, Statement of Applicability](04-policies-and-statement-of-applicability.md) | ISO/IEC 42001 (Annex A) |
| 5 | [Red-team report](05-red-team-report.md) | OWASP Top 10 for LLM Applications, prompt injection testing |
| 6 | [Vendor review, fairness test, incident example](06-vendor-fairness-monitoring.md) | Third-party AI risk, adverse impact ratio, AI incident response |

## Key findings

- **Human review doesn't catch what a model misses.** The anti-money-laundering model is high risk even with analyst review, because analysts only see what it flags.
- **AI hides inside tools a company already owns.** The email security tool had been listed as "not AI."
- **Prompt instructions are not a security control.** In hands-on testing, I extracted a live AI app's hidden instructions in 3 attempts.
- **The loan model failed the four-fifths screen** (adverse impact ratio 0.75), triggering a fair lending review.
- **The chatbot vendor received a conditional approval,** pending contract terms banning training on member data and disclosing its model provider.

## Status

Labs 1 to 6 complete (October 2026). In progress: a 15-risk register, control crosswalk, and one-page board report, plus a local prompt injection test with promptfoo.

## About me

Luis Ramirez: security analyst with an email threat detection background and anti-money-laundering compliance experience in banking. CAMS, CompTIA Security+.
