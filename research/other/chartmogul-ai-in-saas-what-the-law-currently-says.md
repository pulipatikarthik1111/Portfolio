# ChartMogul — AI in SaaS: What the Law Currently Says (summary)

Source: `https://chartmogul.com/blog/ai-in-saas-what-the-law-currently-says/`  
Collected: 2026-04-15

## Executive summary

The post frames **GDPR** as the “core rulebook” whenever AI touches **personal data**, and the **EU AI Act** as a newer **risk-based** layer governing AI systems themselves. For many SaaS use cases (chatbots, assistants, content generation), obligations often land in **“limited risk”** territory (mostly **transparency**), unless the system becomes **high risk** (then stricter requirements apply). Practically: build lightweight AI governance, do vendor due diligence, and keep prompts/data minimized and documented.

## Key takeaways (high-signal)

### GDPR applies whenever personal data is processed (AI or not)
Examples of personal data in AI workflows: names, emails, identifiers, CRM exports, support tickets, call transcripts, prompts with user/employee details.

**GDPR concepts highlighted:**
- **Lawful basis**: document lawful basis (often legitimate interest / contractual necessity).
- **Purpose limitation**: if prompts are used for training, that is a separate purpose that must be disclosed/justified.
- **Data minimization**: send only the minimum necessary data into AI systems (affects prompt design and tool choice).
- **Transparency**: users should understand when AI is used and how their data is involved.
- **Vendor governance**: controller/processor roles → DPAs, security requirements.
- **International transfers**: if data leaves EEA → SCCs + transfer impact assessment.
- **Accountability**: be able to explain data used, purpose, vendor, safeguards, retention.

### EU AI Act adds a risk-based classification
Four categories:
- **Unacceptable risk (prohibited)**: e.g., certain social scoring, some emotion inference in workplaces/education/law enforcement.
- **High risk**: systems affecting health/safety/fundamental rights (strict requirements: risk mgmt, documentation, logging, human oversight).
- **Limited risk**: common in SaaS (chatbots/content-gen/assistants) → **transparency obligations**.
- **Minimal risk**: no special obligations beyond existing law.

Roles:
- **Provider**: develops/places AI on market.
- **Deployer**: uses AI operationally (many SaaS companies when embedding third-party AI).

Sanctions (as stated):
- Up to **€35M or 7%** global turnover for most serious violations; other tiers include **3%** or **1%**.

### Where GDPR + EU AI Act intersect (practical)
- Personal data in AI → GDPR
- High-risk system → EU AI Act obligations stack on top of GDPR
- Vendor logs/retains prompts → GDPR purpose limitation considerations
- User-facing AI features → EU AI Act transparency

## Operational checklist (useful for procurement/security review)

- **Map workflows**: what AI is used for, where it’s embedded, and who uses it.
- **Data mapping**: what personal data enters prompts/inputs, where inference runs, retention policies.
- **Minimize/redact prompts**: keep personal data out when possible.
- **Vendor due diligence questions**:
  - Where is inference performed?
  - Do you retain or train on prompts?
  - Who are your subprocessors?
  - Safeguards for model drift/updates?
  - EU AI Act deployer documentation available?
- **Internal guidance**: rules to prevent employees pasting sensitive data into public tools.
- **Human-in-the-loop**: define where human oversight is required.

## GTM note (why this matters for outbound)

Enterprise buyers increasingly ask how AI features work and what data they touch. Having clear, documented answers becomes a **trust + sales differentiator** in security/procurement reviews.

