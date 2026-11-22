# Market study: AI-agent agency for SMBs in Mexico

**Project:** VendeMás Business / Vende Más Studio (tentative name, see the [plan](agency-plan.md))
**Date:** Nov 22, 2026 · **Scope:** Mexico, service SMBs that talk to their customers over WhatsApp
**Method:** desk research with public sources (INEGI/DataMéxico, Meta, press and vendors), plus [Codify's real prices](codify-pricing/README.md) taken from its configurator. No customer interviews yet; they are proposed in section 8.

> Third-party figures (especially vendor blogs) are marked as such. Our own estimates are marked as **assumption**. Amounts are in MXN unless stated otherwise.

---

## 1. Executive summary

- **The market exists and is growing:** Mexico has **~5.47 million business units** (2024 Economic Census). Between 47 % and 64 % of SMBs say they already use some AI, but almost always at a basic level. The conversational AI market in Mexico is estimated at **~US$319M in 2025 and ~US$959M in 2030** (~20 % annual growth, MarketsandMarkets).
- **WhatsApp is the channel:** according to Meta, **92 % of micro and small businesses** use WhatsApp Business, and over 80 % of adults chat with a business on WhatsApp every week. According to Kantar, 71 % prefer messaging to deal with companies.
- **Competition is fragmented into three types:** done-for-you agencies (Codify, SmartLeads, Kosmo…), self-serve software the business configures itself (Leadsales, Kommo, ManyChat, Whaticket…) and freelancers using n8n/Make. Agency prices range from **~$1,000 to $25,000 a month**. The most common range for an SMB is **$2,000–$6,000**.
- **The gap:** almost nobody sells **sales results measured by industry**. Generalist agencies serve "everyone", and software leaves the owner alone with the setup.
- **Recommended starting vertical:** **dental offices and clinics** (76k units, high ticket, a clear appointments/no-shows pain). Second vertical: **real estate agencies** (very high ticket, leads that go cold within minutes). Beauty salons and barbershops are a huge market (311k) but with a low ticket: better served later by a more automated product.
- **Main risks:** Meta's policies (since Jan 15, 2026, general-purpose AI chatbots are banned from the API; business customer-service and sales bots are allowed), rising Meta fees (marketing +~30 % in Mexico since Oct 2026) and **skepticism about AI's ROI** in Mexico (Expansión, Jul 2026).

---

## 2. Market size

### 2.1 Top-down (context)

| Indicator | Value | Source |
|---|---|---|
| Business units (private + state-owned) | 5,468,180 | INEGI, 2024 Economic Census (final results) |
| People employed | 27,965,433 | INEGI, 2024 Economic Census |
| Micro/small businesses using WhatsApp Business | 92 % | Meta (Feb 2025), the company's own figure |
| SMBs using some AI | 47 %–64 % | Microsoft SMB Survey 2025 (64 % in Mexico), other studies |
| Conversational AI market, Mexico | US$318.6M (2025) → US$958.8M (2030) | MarketsandMarkets |
| Conversational AI market, Latin America | ~US$1.1B (2025) → ~US$3.3B (2030) | MarketsandMarkets |
| Enterprise agentic AI, Mexico | US$103.7M (2024) → US$935.4M (2030) | Computer Weekly |

### 2.2 Bottom-up by vertical (what we can actually sell)

Business units come from DataMéxico/DENUE (May 2026). The addressable %, price and revenue are **assumptions** to validate.

| Vertical | Units | Concentration | Addressable % (assumption)* | Avg. price/month (assumption) | Addressable market per year (MXN) |
|---|---|---|---|---|---|
| Dental offices | 76,188 | State of Mexico 10.2k · Mexico City 7.5k · Jalisco 4.8k | 10 % → 7,600 | $2,500 | **~$228M** |
| Beauty salons and clinics | 310,869 | State of Mexico 47.1k · Mexico City 25.3k · Jalisco 24.8k | 5 % → 15,500 | $1,900 | **~$354M** |
| Food preparation (restaurants, branch 7225) | 740,231 | State of Mexico 93.2k · Mexico City 57.2k · Veracruz 51.8k | 3 % → 22,200 | $3,000 | **~$800M** |
| Real estate agencies and brokers (branch 5312) | 8,243 | — | 30 % → 2,500 | $4,500 | **~$135M** |
| **Total, 4 verticals** | | | **~47,800 businesses** | | **~$1,500M MXN per year** |

\* "Addressable" means it has enough message volume (10+ a day), can pay and is in an area we serve. Most are micro-businesses (99.8 % of salons have fewer than 10 employees, per a third party), so the addressable % is deliberately low.

### 2.3 Realistic target (SOM)

- **Year 1:** 40 customers × $4,500 ARPA = **~$2.2M MXN ARR**, i.e. 0.15 % of the 4 verticals' addressable market. Conservative and reachable with a single vertical.
- **Year 3:** 300 customers in 2 verticals = ~$16M MXN ARR (assumption).

---

## 3. The customer

**Primary profile:** the owner of a service business with 2 to 15 people, who **handles customers on WhatsApp from their own phone**, replies late at night and has no full-time receptionist, or has one covering only ~48 of the week's 168 hours.

**Biggest pains** (from the Codify analysis and the sources):
1. Unanswered or late-answered messages, especially at night and on weekends.
2. Unconfirmed appointments, no-shows and gaps in the schedule.
3. Prospects who say "I'll think about it" and never get a follow-up.
4. Quoting and collecting payments by hand.
5. Lack of time: according to Expansión (Mar 2026), 53 % of SMBs don't have time to run their business.

**What they compare us to (price anchor):**
- **A receptionist:** the 2026 minimum wage is **$315.04 a day ≈ $9,582 a month** ($13,410 in the northern border zone), before social security (IMSS) and benefits. An assistant at $2,000–$4,500 a month costs 20–45 % of that and works 24/7.
- **Doing it for free:** WhatsApp Business quick replies, or a nephew who "knows tech".

**Expected objections:** "AI makes mistakes", "my customers want to talk to a person", "I tried a bot and it was bad" and "I don't see the return". The last one shows up in a Jul 2026 Expansión piece: *Mexico, skeptical of AI: it doesn't see value that justifies the investment*. That's why the free demo, the goal-based guarantee and the report in money are key.

---

## 4. Competition

### 4.1 Landscape

| Type | Examples | Price (MXN/month unless noted) | Strength | Weakness |
|---|---|---|---|---|
| **Done-for-you AI agency** | **Codify Business** | $1,590–$11,190 by volume; enterprise from $11,290; voice and videos extra ([details](codify-pricing/README.md)) | Orchestrator, 24 h demo, guarantee, very strong SEO/AEO | Generalist (16 industries); its case studies are about marketing, not sales |
| | SmartLeads | $2,900 / $5,900 / $9,900 | Setup included | High entry price |
| | Kosmo IA | from $4,497 | Capacity based on new customers | Expensive for a micro-business |
| | Pezeta | $999 – $9,999 | Low entry price | Little differentiation |
| | Simplixy | $12,900–$35,900 one-time, plus API | No monthly fee | No ongoing improvement |
| **Self-serve software** | Leadsales (Mexico) | $2,363 – $3,240 | CRM and shared inbox, Mexican brand | The customer does the work; not all integrations are official |
| | Kommo | ~USD, per user | 200+ integrations, pipeline | Learning curve |
| | Treble | Quote-based (B2B) | Flows for mid-size companies | Not built for micro-businesses |
| | ManyChat / Whaticket / Aurora Inbox | US$29–39/month / $1,800 | Cheap | You build it yourself; AI is capped or billed extra |
| **Freelancers / n8n / Make** | Many | $5k–$30k per project | Cheap upfront | No support or measurement; breaks |
| **Native from Meta** | WhatsApp Business AI features / Meta AI | Free or low | Already in the app | Generic, no integrations or reporting |

Prices from vendor blogs (Kosmo, SmartLeads, Aurora, Leadsales) are reference points, not verified quotes.

### 4.2 Proposed positioning

```
              Generalist ◄──────────────────────► Vertical specialist
                  │                                        │
 Done for you     │  Codify, SmartLeads, Kosmo    ★ VendeMás (dental / real estate)
                  │                                        │
 Self-serve       │  ManyChat, Whaticket, Kommo   Vertical software (dental scheduling,
                  │  Leadsales                    real-estate CRMs) → potential partners
```

**Message:** "We don't sell a bot: we deliver more appointments and more sales, measured in pesos, for your industry."

---

## 5. Choosing the vertical (scoring matrix)

Scale of 1 to 5 (5 = best). Weights in parentheses.

| Criterion | Dental / clinics | Real estate | Beauty / barbershops | Restaurants | Distributors |
|---|---|---|---|---|---|
| WhatsApp volume (20 %) | 4 | 5 | 5 | 5 | 3 |
| Ticket and ability to pay (20 %) | 4 | 5 | 2 | 2 | 5 |
| Clear, measurable pain (20 %) | 5 (no-shows, appointments) | 5 (cold leads) | 4 | 3 | 4 (quoting) |
| Market size (15 %) | 4 | 2 | 5 | 5 | 3 |
| Ease of delivery (15 %) | 4 (scheduling) | 3 (CRM, listing portals) | 5 | 2 (kitchen, POS) | 2 (ERP) |
| Specialized competition (10 %) | 3 | 3 | 2 (AgendaPro, etc.) | 2 | 4 |
| **Weighted score** | **4.10** | **4.05** | **3.9** | **3.3** | **3.6** |

**Recommendation:** start with **dental offices and clinics** in **Mexico City and the State of Mexico**, which together have ~17.6k dental offices. Add **real estate agencies** as the second vertical (higher ticket and higher price per customer). Beauty can become a self-serve "lite" product line later.

---

## 6. Price: what the market will pay

| Segment | Observed range | Proposal (see the plan) |
|---|---|---|
| Micro-business, 1 channel, low volume | $999 – $1,890 | Don't compete here at first |
| SMB with scheduling and follow-up | $1,990 – $4,500 | **Essential $1,990 / Growth $4,990** |
| SMB with several branches or high volume | $5,000 – $12,000 | Growth + add-ons |
| Enterprise (16+ people, integrations) | $11,000 – $65,000 | Full team from $11,900 |

**Costs the customer pays** (Meta, per message since Jul 2025): marketing templates rose ~30 % in Mexico on Oct 1, 2026, and utility templates are now charged even inside the 24 h window, from that same date. **Explain this in the proposal** and design the agent to rely mainly on service messages, which are free when the customer writes first.

---

## 7. Market and regulatory risks

| Risk | Details | Mitigation |
|---|---|---|
| WhatsApp policy | Since Jan 15, 2026, **general-purpose** AI chatbots are banned from the Business API. Business customer-service and sales bots are still allowed | The customer-facing agent only talks about the business; the "owner's assistant" lives in Telegram or a dashboard |
| Meta fees | They rise and change model frequently | Flag it in the proposal, optimize for service messages, and the customer pays Meta directly |
| ROI skepticism | The Mexican market doubts AI's value | Demo with their data, goal-based guarantee and report in pesos |
| Meta launches its own business AI | Free, native competition | Differentiate on integrations, vertical focus, measurement and a human in charge |
| Personal data | LFPDPPP, Mexico's data protection law (and health data in clinics: sensitive data) | Privacy notice, consent, minimal clinical data in the chat, isolated tenant |
| Competitors copying us | Low barriers to entry | Vertical case studies, proven templates, partnerships with the vertical's software vendors |

---

## 8. Primary validation (next step)

1. **15 interviews** with dental office owners in Mexico City / State of Mexico (30 min each). Questions: how many messages a day, who answers and when, how many no-shows a week, what a consultation or treatment is worth, what they've tried and how much they'd pay.
2. **Smoke test:** a "Dental AI agent" landing page with pricing and a free demo, plus $3–5k MXN in Meta ads. Measure cost per lead and conversion to demo.
3. **Mystery shopper:** message 50 dental offices on WhatsApp at 9 p.m. and measure how many answer and how fast. Our own data point for the pitch ("X % of dentists in your area don't answer at night").
4. **3 pilots** at a discount in exchange for a case study with data (appointments, no-shows, sales).

---

## Sources

- INEGI, 2024 Economic Census (final results): https://www.inegi.org.mx/contenidos/saladeprensa/boletines/2025/ce/CE2024_def.pdf
- INEGI, SMB statistics 2025: https://www.inegi.org.mx/contenidos/saladeprensa/aproposito/2025/EAP_MIPYMES_25.pdf
- DataMéxico, dental offices: https://www.economia.gob.mx/datamexico/es/profile/industry/offices-of-dentists
- DataMéxico, beauty salons and clinics: https://www.economia.gob.mx/datamexico/es/profile/industry/personal-care-services
- DataMéxico, restaurants: https://www.economia.gob.mx/datamexico/es/profile/industry/restaurants-and-other-eating-places
- DataMéxico, real estate agents and brokers: https://www.economia.gob.mx/datamexico/es/profile/industry/real-estate-agents-and-brokers
- Microsoft, SMB Survey 2025: https://news.microsoft.com/source/latam/noticias-de-microsoft/encuesta-pymes-2025-54-de-las-pymes-en-las-americas-usa-ia/
- Xataka, 2.5 million companies using AI: https://www.xataka.com.mx/robotica-e-ia/mexico-tiene-2-5-millones-empresas-usando-ia-problema-que-mayoria-solo-usa-para-basico
- Expansión, 53 % of SMBs lack time: https://expansion.mx/tecnologia/2026/03/12/53-de-las-pymes-carece-de-tiempo-para-operar-su-negocio-la-ia-emerge-como-solucion
- Expansión, Mexico skeptical of AI: https://expansion.mx/tecnologia/2026/07/15/mexico-esceptico-ia-no-ve-valor-justifique-inversion
- Expansión, Mexicans trust WhatsApp to talk to businesses: https://expansion.mx/tecnologia/2025/03/11/mexicanos-confia-whatsapp-comunicarse-empresas
- Mobile Time, WhatsApp Business and SMBs in Mexico: https://mobiletime.la/noticias/28/02/2025/whatsapp-business-pymes-mexico/
- MarketsandMarkets, conversational AI in Mexico: https://www.marketsandmarkets.com/Market-Reports/geography/conversational-ai-market/Mexico
- MarketsandMarkets, conversational AI in Latin America: https://www.marketsandmarkets.com/Market-Reports/geography/conversational-ai-market/Latin-America
- Computer Weekly, agentic AI in Mexico: https://www.computerweekly.com/es/noticias/366630151/Mercado-de-IA-agentica-empresarial-en-Mexico-alcanzaria-9354-MDD-en-2030
- Meta, WhatsApp Business Platform pricing: https://developers.facebook.com/docs/whatsapp/pricing
- Gupshup, October 2026 changelog (Mexico rates): https://partner-docs.gupshup.io/changelog/october-2026
- TechCrunch, WhatsApp bans general-purpose chatbots: https://techcrunch.com/2025/10/18/whatssapp-changes-its-terms-to-bar-general-purpose-chatbots-from-its-platform/
- respond.io, scope of the ban: https://respond.io/es/blog/whatsapp-general-purpose-chatbots-ban
- 2026 minimum wage (BBVA): https://www.bbva.mx/educacion-financiera/banca-digital/portabilidad-de-nomina/portabilidad-salario-minimo-mexico.html
- Competitor prices (vendor blogs): https://smartdevs.com.mx/smartleads/blog/cuanto-cuesta-chatbot-whatsapp-ia-mexico/ · https://kosmo.com.mx/blog/mejores-chatbots-whatsapp-mexico · https://chatbot.pezetasolutions.com/ · https://simplixy.com.mx/precio-chatbot-whatsapp-mexico/ · https://www.aurorainbox.com/en/2025/05/17/how-much-does-a-whatsapp-chatbot-cost-in-mexico/ · https://leadsales.io/blog/leadsales-vs-kommo/
- Codify Business, configurator prices: [docs/codify-pricing/](codify-pricing/README.md)
