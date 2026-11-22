# Plan: AI-agent agency

A plan to launch an agency that sells "teams of AI agents" to SMBs. It uses Codify Business's model as a reference ([analysis](codify-analysis.md)) and aims to differentiate from it.

> Figures are starting assumptions, in MXN + VAT. They need to be validated with the first 10 customers.

---

## 0. Agency name (tentative)

| Option | Domain to check | Read |
|---|---|---|
| **VendeMás Business** | `vendemasbusiness.com` | Direct and results-oriented ("vende más" = "sell more"); sounds like a business tool for SMBs |
| **Vende Más Studio** | `vende-mas-studio.com` / `vendemas.studio` | More creative, agency-like; pairs well with content and marketing |

Both reinforce the core promise: **sell more**, not "have AI". That fits this plan's positioning: measurable sales cases and reporting in money.

**To validate before deciding:**
- Whether the `.com` / `.mx` domain is available (with and without the hyphen; without it is easier to spell out over the phone)
- Available handles on Instagram, TikTok and WhatsApp Business
- Trademark search with IMPI, Mexico's trademark office (class 35: advertising and business; class 42: software and technology services)
- No conflict with existing brands with similar names ("Vende Más")
- A quick test with 5 to 10 business owners: which one they remember and which one they trust more

## 1. Value proposition

**In one sentence:** "Your business answers, quotes, collects and follows up on its own, 24/7, and you only approve what matters. If it doesn't hit your goals in 30 days, we refund you."

**What we copy because it works:**
- The **orchestrator + specialist agents** architecture, where the customer "hires" agents one at a time
- A **personalized demo in under 24 h** before asking for money
- **Public pricing** by volume and modules, with setup included
- A **guarantee tied to 3 signed goals** and a **monthly report in money**
- Accounts always in the customer's name, guest access only, and a human approving sensitive actions

**How we differentiate (pick 1 or 2):**
1. **Vertical first.** Start with 1 or 2 industries and be the best at them, instead of 15 at once. Candidates with money, heavy WhatsApp use and repeatable processes: **dental and aesthetic clinics**, **real estate agencies**, **distributors and hardware stores** (wholesale quotes and orders).
2. **Measurable sales cases.** Codify only publishes SEO and TikTok cases. We publish conversation → appointment → sale cases, with CRM data.
3. **Deep integrations with the industry's software** (dental scheduling, real-estate CRM, the distributor's ERP or spreadsheet) from day one.
4. **A different geography:** another Mexican city, Colombia, Spain or the US Hispanic market.

---

## 2. Agent catalog (phases 1 and 2)

| Phase | Agent | Minimum deliverable |
|---|---|---|
| 1 | **Customer service and sales (WhatsApp + IG)** | Answers FAQs from the customer's knowledge base, qualifies leads, hands off to a human with a summary |
| 1 | **Scheduling and reminders** | Books in Google Calendar or the industry's system, confirms 24 h ahead, reschedules |
| 1 | **Follow-up and reactivation** | Messages people who said "I'll think about it" and reactivates inactive customers with approved templates |
| 1 | **Orchestrator + owner's channel** | Takes the owner's instructions via Telegram or a dashboard, requests approvals and sends the daily summary |
| 2 | PDF quotes | Builds the quote from the customer's catalog and branding; the owner approves it in one tap |
| 2 | Collections | Sends payment links (Stripe / Mercado Pago), reminds about payments and receives proof of payment |
| 2 | Voice | Answers calls, books appointments and leaves a summary on WhatsApp |
| 2 | Marketing / content | Weekly carousels and videos, reviewed by the owner before publishing |
| 2 | Google reviews | Asks for a review after the visit and replies to reviews |
| 3 | Custom / Enterprise | Purchasing, inventory, ERP, reports |

---

## 3. Proposed pricing

Position ourselves **slightly above** Codify in the chosen vertical, justified by specialization and sales cases. Don't compete on price.

**Codify reference** (their real configurator, see [codify-pricing/](codify-pricing/README.md)): 10 conversations a day $1,590 · 25: $1,990 · 60: $2,790 · 150: $4,790 · 300: $7,890. Modules from +$100 to +$300 (social media +$2,100), rising with volume. From 16 employees, the enterprise plan starts at $11,290. Voice is billed separately: about $7,400 for 10 calls a day.

**What to copy from how they charge:**
- Conversation volume as the main variable, with clear tiers.
- Modules that cost more as volume grows, not a flat price.
- An adjustment for customer value (average ticket and industry).
- WhatsApp and Instagram together for the price of one channel, as a hook.
- Voice as a separate, high-margin product.
- A clear jump to "enterprise" based on the customer's size.

| Plan | Includes | Price/month |
|---|---|---|
| **Essential** | Customer service and sales, scheduling, up to 30 conversations a day, 1 channel | $1,990 |
| **Growth** | Essential, plus follow-up and reactivation, quotes, collections, 2 channels, up to 100 conversations a day | $4,990 |
| **Full team** | Orchestrator, all agents, CRM/ERP integration, SLA, up to 300 conversations a day | from $11,900 |

- **Add-ons:** voice (from $1,190 for 150 min), content ($1,900), extra number or branch ($300).
- **Setup:** free on monthly plans with a 3-month minimum, or $4,900 with no minimum. This protects CAC; to be validated.
- **Prepayment:** 10 % off for 6 months and 15 % off for 12.
- **Meta fees:** paid by the customer, directly to Meta.

**Target unit cost:** LLM, infrastructure and WhatsApp under 15 % of the price. Support and improvements: 1 to 2 hours per customer per month. **Target gross margin: 70 % or more.**

---

## 4. Tech stack

| Layer | Recommended option | Alternatives |
|---|---|---|
| WhatsApp channel | WhatsApp Business Platform (Cloud API) via a BSP (360dialog, Twilio) | — |
| Orchestration | **Our own code** (TypeScript/Python) with an agent SDK and tool use | n8n for prototypes and simple integrations |
| Models | Claude (Sonnet for conversation, Haiku for classification and routing) | GPT, Gemini |
| Memory and knowledge | Postgres + pgvector (Supabase), one knowledge base per customer | — |
| Voice | Real-time voice provider with a local number (Vapi, Retell or Twilio + TTS) | — |
| Scheduling | Google Calendar API and the vertical's own system | Cal.com |
| Payments | Stripe and Mercado Pago (payment links) | — |
| CRM | HubSpot / Pipedrive via API, or our own lightweight CRM | — |
| Owner's channel | Telegram bot and a web dashboard (approvals, pause, metrics) | — |
| Observability | A log of every agent action, automated evals and alerts | — |

**Principles:** one isolated tenant per customer, versioned prompts and rules, human approval for discounts, charges and bulk sends, a pause button, and data export (CSV/JSON) if the customer leaves.

---

## 5. Sales and delivery process

1. **Lead** comes in through SEO, content, affiliates or outbound.
2. **Web configurator** (2 min) that shows the estimated price and the benefits for their industry.
3. **Demo in under 24 h:** a personalized page and a test chat with their information (catalog, prices, hours). Generated semi-automatically from a vertical template plus what the customer sends.
4. **15–20 min call:** exact price and **3 measurable goals**. Examples: 95 % of messages answered in under 1 minute, 20 appointments a month, reactivate 50 customers.
5. **Contract and access** (48 h). Number verification with Meta.
6. **Go-live** in 5 to 10 business days, with 45 minutes of training for the team.
7. **Operations:** a summary every Friday, a monthly report in money (people served, appointments, sales, hours saved, ROI), changes within 48 h.
8. **Expansion:** propose the next agent on day 60 and day 90.

**Guarantee:** if the 3 goals aren't met in 30 days, we refund 50 % of the first month.
**SLA:** critical issues (the agent doesn't answer or says something serious) in under 2 h; broken features the same business day.

---

## 6. Customer acquisition

| Channel | Concrete action | 90-day goal |
|---|---|---|
| **SEO/AEO** | 20 vertical articles with a "quick answer", landing pages per industry and city, a pricing guide | 2,000 visits a month |
| **Live demo** | Our own agent handling the agency's WhatsApp and phone: the product sells itself | 100 % of leads handled by it |
| **Outbound** | A list of businesses in the vertical (Google Maps); a message with a 60-second "your business, served by AI" video | 30 demos |
| **Content** | TikTok/Reels with cases and before/after views of real (anonymized) conversations | 3 posts a week |
| **Affiliates** | Accountants, marketing agencies and the vertical's suppliers: 10–20 % for 12 months | 5 active affiliates |
| **Partnerships** | Software vendors in the vertical (dental scheduling, real-estate CRM) | 1 partnership |

---

## 7. Team

| Stage | Role | Responsibility |
|---|---|---|
| 0–10 customers | Founder (sales + product) | Demos, closing, agent design |
| 0–10 customers | Agent engineer | Platform, integrations, evals |
| 10–30 customers | Customer success / implementer | Onboarding, changes, reports |
| 10–30 customers | Content/SEO (part-time or with our own agents) | Blog, social media, case studies |
| 30+ customers | Sales (SDR) | Prospecting and booking demos |

We use our own agents internally: demos, reports, content and prospecting. It's part of the pitch.

---

## 8. Roadmap (90 days)

**Weeks 1–2: foundation**
- Choose the vertical and the city. Interview 10 business owners.
- Name, domain, verified WhatsApp Business, standard contract, privacy notice (LFPDPPP, Mexico's data protection law).

**Weeks 3–6: MVP**
- Minimal platform: WhatsApp, orchestrator, customer-service agent with scheduling, owner's dashboard and action log.
- Vertical template: knowledge base, flows and evals.
- Personalized demo generator and pricing configurator on the website.
- Our own agent on the agency's WhatsApp.

**Weeks 7–10: first customers**
- 3 to 5 pilot customers at 50 % off in exchange for a case study and data.
- Measure: response time, appointments, conversions and cost per conversation.
- Iterate on prompts, tools and the monthly report.

**Weeks 11–13: scale**
- Publish 2 case studies with real numbers.
- Launch the phase-2 agents (quotes and collections).
- Start the affiliate program and systematic outbound.

---

## 9. Key metrics

- **Business:** MRR, number of customers, ARPA, monthly churn (goal: under 4 %), CAC, payback (goal: under 3 months), NRR (goal: over 110 % through agent upsells).
- **Product:** % of conversations resolved without a human, response time, escalation rate, serious errors (goal: 0), cost per conversation.
- **Customer value:** attributed appointments or sales, hours saved, ROI in the monthly report.

**12-month goal (illustrative):** 40 customers with an ARPA of $4,500, i.e. about **$180k MXN in MRR**.

---

## 10. Risks and mitigations

| Risk | Mitigation |
|---|---|
| Meta policies (since 2026 WhatsApp only allows business assistants) | The customer-facing agent stays on business topics; the owner's channel lives in Telegram or the dashboard; official API only |
| Hallucinations or harmful answers | Answer only from approved information, automated evals, human approval for sensitive actions, a pause button |
| LLM or voice costs spiking | A usage "battery" model, routing to cheaper models, per-plan limits |
| Sales depending on the founder | Configurator, automated demos and our own sales agent |
| Price competition | Vertical specialization, integrations and measurable sales cases |
| Personal data (LFPDPPP / GDPR) | Privacy notice, isolated tenant, export and deletion on exit, least privilege |

---

## 11. Immediate next steps

1. Decide the **vertical** and **geography** (section 1).
2. Validate pricing with 10 interviews.
3. Choose between **VendeMás Business** and **Vende Más Studio** (section 0) and register the domain and trademark.
4. Start the technical MVP (section 4). This repo can host the orchestrator and agent code.
