# Analysis of codifybusiness.com

Source: a scrape of 68 public pages from https://codifybusiness.com (Nov 22, 2026).
The text of each page is in [`scraping/raw/`](scraping/raw) (complete) and [`scraping/clean/`](scraping/clean) (without the repeated menu and footer). The site is in Spanish; quotes below are translated.

## 1. What it is

Codify Business is an agency based in Mexico City (founder: Emilio Cisneros) that sells **"a team of AI agents"** to SMBs and companies in Mexico, Latin America and Spain.

- **Promise:** "A team of AI agents that serves customers, sells and works for your business 24 hours a day. A lead agent coordinates all of them and you only approve what matters."
- **Positioning:** "Your AI advisor, not a software vendor." They sell results (zero unanswered messages, appointments, sales), not technology.
- **Mascot / live demo:** "Codi", their own lead agent. Visitors can talk to it by voice in the browser, by phone or by chat. It works as both the demo and the salesperson.

## 2. Product architecture: orchestrator + specialists

| Agent | What it does |
|---|---|
| **Lead agent (orchestrator)** | Receives everything, routes tasks, asks the owner for approval |
| Customer service and sales | WhatsApp, Instagram, Messenger, web; books, follows up and collects payment (Stripe / Mercado Pago) |
| Voice | Answers calls, books appointments, sends a summary over WhatsApp |
| Marketing | Scripts, avatar videos, carousels, daily posting on TikTok/IG/FB |
| Quotes | Branded PDF quotes in seconds |
| Purchasing | Compares suppliers, checks stock, prepares purchase orders |
| Scheduling and collections | Reminders, confirmations, polite payment collection |
| Operations and reporting | Expenses from a photo of the receipt, daily sales summary |
| Google and AI search (SEO/AEO) | Blog posts, Google Business Profile, mentions in ChatGPT |
| Custom | Inventory, after-sales, recruiting, invoices, reviews… |

They also sell services that are not agents: custom CRM, custom software (from $35,000), websites (from $9,900), consulting ("AI Advisor", $29,900/month; single session $9,900) and an AI workshop for teams ($24,900 for 3 hours).

## 3. Pricing (MXN + VAT, effective Nov 6, 2026)

**Reference packages**
- **Starter** (sales + WhatsApp): $1,490 – $2,090/month
- **Growth** (+ autonomous marketing): $5,280 – $8,080/month
- **Enterprise** (orchestrator, quotes, purchasing, ERP/CRM, SLA; 16+ employees): from $11,690/month

**Base price by volume:** 10 conversations a day $1,490 · 25 $1,890 · 60 $2,590 · 150 $4,590 · 300 $7,890 · over 300, custom.

**Modules:** scheduling +$100 · sales and follow-up +$200 · quotes +$300 · collections +$100 · purchasing +$200 · operations +$200 · social media +$1,900 · SEO/AI search +$700 · ads +$200.

**Add-ons:** voice from 150 min for $1,090 to 1,000 min for $5,090 · AI videos from 2/month for $590 to 30/month for $6,490 · extra number or branch from $200 · pause $490/month.

**Commercial rules**
- Setup always free, no lock-in (30 days' notice to cancel)
- Discounts only for prepaying: 5/10/15 % for 3/6/12 months
- Usage shown as a "battery": alerts at 80 % and 100 %; the agent never stops answering; +50 % top-ups
- If the customer uses less than 40 % for 3 months, they lower the price without being asked
- Meta's messaging fees are paid separately, by the customer, directly to Meta

## 4. Sales funnel and process

1. **2-minute configurator:** the customer picks their industry and modules and sees the price live. They can also talk to Codi.
2. **Free demo in under 24 h:** a page built for their business, with a chat to try the assistant for 7 days. It is not connected to their real number.
3. **15-minute call** with the exact price. If AI isn't a good fit, they say so.
4. **Contract within 48 h** with **3 measurable goals**. Guest access only, never passwords.
5. **Go-live** on their number through WhatsApp's official API, plus 45 minutes of training for the team.
6. **Continuous improvement:** unlimited changes in month one, then 4 a month, delivered within 48 h.
7. **Monthly report in pesos** with ROI ("for every $1 you paid, you logged $9 in sales"), plus a summary every Friday.

**30-day guarantee:** if the 3 goals aren't met, they refund 50 % of the first month.
**Support:** critical issues handled in under 2 h any day; high-priority ones the same business day.

## 5. Customer acquisition

- **Aggressive SEO/AEO:** 30+ blog posts with buying intent ("how much does an AI agent cost in Mexico", "WhatsApp chatbot prices", "n8n vs Make vs Zapier"), landing pages per industry (15 verticals) and per city (Mexico City). Every page opens with a "Quick answer" designed to be quoted by LLMs.
- **Case studies with verifiable data** (Search Console and TikTok): R&R Legal went from 20 to 348 clicks and closed 7 clients; Urbanus went from 0 to 6,337 impressions; attorney Luz Cisneros has 60k TikTok views.
- **Affiliates:** 10 % (1–4 clients), 15 % (5+) and 20 % (10+) for 12 months. For customers: one free month per referral.
- **Live voice demo** (Codi) and a 4-minute video sales letter from the founder.

## 6. Technology we can infer

WhatsApp Business Platform (official API) · n8n / Make / Zapier (compared on their blog) · ChatGPT/OpenAI, Gemini and Claude models · Google Calendar · CRMs: HubSpot, Zoho, Pipedrive, Salesforce · payments: Stripe and Mercado Pago · voice with a phone number · avatar video · Telegram or a dashboard as the "owner's channel", because since 2026 WhatsApp only allows business-topic assistants · one isolated environment per customer.

## 7. Strengths and gaps (opportunities)

**Strengths:** public, granular pricing; demo in 24 h; guarantee tied to goals; report in pesos; trust signals (accounts in the customer's name, a human in charge); and a very polished SEO/AEO machine.

**Gaps a new agency could go after:**
- All 3 case studies are about **marketing/SEO** (law firms, a permits agency). There are no published cases for WhatsApp sales, voice or purchasing, which is their core product.
- Very focused on Mexico City and Mexican Spanish. There is room in other cities, in Spain or in the US Hispanic market.
- They offer everything to everyone (15 verticals, plus software, consulting and workshops). A **vertical** agency can win on depth: integrations with the industry's software, regulatory compliance, proven templates.
- The entry price is low ($1,490), so margins depend on highly automated operations. To compete, differentiate on value, not on price.
