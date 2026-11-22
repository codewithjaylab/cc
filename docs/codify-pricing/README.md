# Codify Business: real configurator prices

These figures come from the API behind Codify's pricing configurator (`POST /api/precio`), queried on Nov 22, 2026 with 91 combinations. All amounts are MXN, before VAT, per month. The full responses are in [`api-responses.json`](api-responses.json).

> **How they were obtained:** the website's configurator requests the price live from `/api/precio` while the visitor answers, with no sign-up or captcha. I replayed those same requests with the form's options, one per second. I did not submit the final contact form (`/api/lead`), because it creates a real lead and notifies their sales team. The price doesn't depend on that step.

## How they calculate the price

Baseline: **a medical/dental office, WhatsApp only, 10 conversations a day = $1,590**.

| Variable | Effect on price |
|---|---|
| **Conversations per day** (the biggest driver) | 10: $1,590 · 25: $1,990 · 60: $2,790 · 150: $4,790 · 300: $7,890 · over 300: $11,190 |
| **Modules** (at 10 conversations a day) | scheduling +$100 · sales +$100 · collections +$0 · quotes +$200 · purchasing +$200 · operations +$300 · ads +$300 · SEO +$900 · social media +$2,100 |
| Modules at higher volume | **Each module's price rises with conversations.** "Sales and follow-up" costs +$100 at 10 a day, +$1,400 at 150 and +$4,000 at 450 on the enterprise plan |
| Social media, by posts per week | 3: +$1,900 · 5: +$2,100 · 7: +$2,400 |
| SEO, by articles per month | 4: +$900 · 8: +$1,000 · 12: +$1,200 |
| Ads, by ad spend | Doesn't change the price at low volume (always +$300) |
| **Channels** | WhatsApp + Instagram costs the same as WhatsApp alone. From the 3rd channel, **+$800**, and then it stops rising |
| **Branches** | 2: +$200 · 3: +$1,100 · 4: +$2,100 |
| **Integrations** | +$200 each (calendar, spreadsheets, CRM, POS, payments or own system); all 6 together, +$1,000 |
| **Employees** | 1 to 15 doesn't change the price. **From 16 people it switches to the "enterprise" plan**: $11,290 with just 10 conversations a day (7× more) |
| **Average ticket** (what each customer pays) | Under $300: $1,490 · $300 to $20,000: $1,590 · over $20,000: $1,690. **They price by customer value** |
| **Industry** | Same configuration ranges from $2,290 to $2,790: distributors and wholesale cost more (1,000-product catalog); real estate, stores, construction and car sales, +$200 |
| **Voice** (billed separately) | 4 calls a day: $3,190 (600 min) · 10: $7,390 (1,500 min) · 22: $14,390 (3,000 min) · 40: $21,490 (4,500 min, "custom"). Extra minute: $5.90 |
| **AI videos** (billed separately) | 2: $690 · 4: $1,090 · 8: $1,890 · 16: $3,490 a month. Extra video: $390 |
| Prepayment | 5 % for 3 months, 10 % for 6 and 15 % for 12 (assistant only, not voice or videos) |
| Usage top-up | +50 % usage at a fixed price ($390 on the base plan, $3,590 at 300 conversations a day) |
| Minimum term | 0 months in every case |

## Findings

1. **Real prices are about $100 higher than the public table.** For example, $1,590 versus the published $1,490 for 10 conversations a day. The $1,490 price only shows up when the ticket is under $300.
2. **Each module's price depends on volume.** The "+$100 / +$200" on the pricing page is the floor. At 150 conversations a day, sales costs $1,400 and quotes $1,000.
3. **The biggest revenue drivers are voice and the jump to "enterprise".** At 10 calls a day, voice already costs 4.6× the assistant. And having 16+ people multiplies the base price by 7.
4. **There is value-based pricing:** the average ticket and the industry change the price even when the work is the same.
5. **Instagram is free with WhatsApp.** A good hook: "the same agent everywhere".
6. **Typical combinations:** barbershop $1,890 · medical office with scheduling $1,790 · dentist with social media $4,490 · restaurant with 2 branches $5,890 · real estate with everything $24,770 (including voice and videos) · 30-person company $27,380 · 80-person company maxed out $64,970.

## Full tables

### 1. Volume (dental office, WhatsApp only, no modules)

| Case | Plan | Assistant/month | Voice | Videos | **Total/month** | Assistant, 12 months prepaid |
|---|---|---|---|---|---|---|
| 10 conversations/day | business | $1,590 | — | — | **$1,590** | $1,352 |
| 25 conversations/day | business | $1,990 | — | — | **$1,990** | $1,692 |
| 60 conversations/day | business | $2,790 | — | — | **$2,790** | $2,372 |
| 150 conversations/day | business | $4,790 | — | — | **$4,790** | $4,072 |
| 300 conversations/day | business | $7,890 | — | — | **$7,890** | $6,707 |
| 450 conversations/day | business | $11,190 | — | — | **$11,190** | $9,512 |

### 2. Each module alone (dental office, 10 conv/day)

| Case | Plan | Assistant/month | Voice | Videos | **Total/month** | Assistant, 12 months prepaid |
|---|---|---|---|---|---|---|
| scheduling | business | $1,690 | — | — | **$1,690** | $1,437 |
| sales | business | $1,690 | — | — | **$1,690** | $1,437 |
| quotes | business | $1,790 | — | — | **$1,790** | $1,522 |
| collections | business | $1,590 | — | — | **$1,590** | $1,352 |
| purchasing | business | $1,790 | — | — | **$1,790** | $1,522 |
| operations | business | $1,890 | — | — | **$1,890** | $1,607 |
| social media | business | $3,690 | — | — | **$3,690** | $3,137 |
| SEO | business | $2,490 | — | — | **$2,490** | $2,117 |
| ads | business | $1,890 | — | — | **$1,890** | $1,607 |

### 3. Social media: posts per week

| Case | Plan | Assistant/month | Voice | Videos | **Total/month** | Assistant, 12 months prepaid |
|---|---|---|---|---|---|---|
| 3/week | business | $3,490 | — | — | **$3,490** | $2,967 |
| 5/week | business | $3,690 | — | — | **$3,690** | $3,137 |
| 7/week | business | $3,990 | — | — | **$3,990** | $3,392 |

### 4. SEO: articles per month

| Case | Plan | Assistant/month | Voice | Videos | **Total/month** | Assistant, 12 months prepaid |
|---|---|---|---|---|---|---|
| 4/month | business | $2,490 | — | — | **$2,490** | $2,117 |
| 8/month | business | $2,590 | — | — | **$2,590** | $2,202 |
| 12/month | business | $2,790 | — | — | **$2,790** | $2,372 |

### 5. Ads: monthly ad spend

| Case | Plan | Assistant/month | Voice | Videos | **Total/month** | Assistant, 12 months prepaid |
|---|---|---|---|---|---|---|
| $3,000 | business | $1,890 | — | — | **$1,890** | $1,607 |
| $12,000 | business | $1,890 | — | — | **$1,890** | $1,607 |
| $35,000 | business | $1,890 | — | — | **$1,890** | $1,607 |
| $80,000 | business | $1,890 | — | — | **$1,890** | $1,607 |

### 6. Number of channels

| Case | Plan | Assistant/month | Voice | Videos | **Total/month** | Assistant, 12 months prepaid |
|---|---|---|---|---|---|---|
| whatsapp | business | $1,590 | — | — | **$1,590** | $1,352 |
| whatsapp + instagram | business | $1,590 | — | — | **$1,590** | $1,352 |
| whatsapp + instagram + messenger | business | $2,390 | — | — | **$2,390** | $2,032 |
| whatsapp + instagram + messenger + web | business | $2,390 | — | — | **$2,390** | $2,032 |
| whatsapp + instagram + messenger + web + correo | business | $2,390 | — | — | **$2,390** | $2,032 |

### 7. Branches

| Case | Plan | Assistant/month | Voice | Videos | **Total/month** | Assistant, 12 months prepaid |
|---|---|---|---|---|---|---|
| 1 | business | $1,590 | — | — | **$1,590** | $1,352 |
| 2 | business | $1,790 | — | — | **$1,790** | $1,522 |
| 3 | business | $2,690 | — | — | **$2,690** | $2,287 |
| 4 | business | $3,690 | — | — | **$3,690** | $3,137 |

### 8. Each integration

| Case | Plan | Assistant/month | Voice | Videos | **Total/month** | Assistant, 12 months prepaid |
|---|---|---|---|---|---|---|
| calendar | business | $1,790 | — | — | **$1,790** | $1,522 |
| spreadsheets | business | $1,790 | — | — | **$1,790** | $1,522 |
| CRM | business | $1,790 | — | — | **$1,790** | $1,522 |
| POS / inventory | business | $1,790 | — | — | **$1,790** | $1,522 |
| payment links | business | $1,790 | — | — | **$1,790** | $1,522 |
| own system (API) | business | $1,790 | — | — | **$1,790** | $1,522 |
| all six | business | $2,590 | — | — | **$2,590** | $2,202 |

### 9. Size (employees)

| Case | Plan | Assistant/month | Voice | Videos | **Total/month** | Assistant, 12 months prepaid |
|---|---|---|---|---|---|---|
| 1 people | business | $1,590 | — | — | **$1,590** | $1,352 |
| 3 people | business | $1,590 | — | — | **$1,590** | $1,352 |
| 10 people | business | $1,590 | — | — | **$1,590** | $1,352 |
| 30 people | enterprise | $11,290 | — | — | **$11,290** | $9,597 |
| 80 people | enterprise | $11,290 | — | — | **$11,290** | $9,597 |

### 10. Voice: calls per day

| Case | Plan | Assistant/month | Voice | Videos | **Total/month** | Assistant, 12 months prepaid |
|---|---|---|---|---|---|---|
| 4 calls/day | business | $1,590 | $3,190 (600 min) | — | **$4,780** | $1,352 |
| 10 calls/day | business | $1,590 | $7,390 (1,500 min) | — | **$8,980** | $1,352 |
| 22 calls/day | business | $1,590 | $14,390 (3,000 min) | — | **$15,980** | $1,352 |
| 40 calls/day | business | $1,590 | $21,490 (4,500 min) | — | **$23,080** | $1,352 |

### 11. AI videos per month

| Case | Plan | Assistant/month | Voice | Videos | **Total/month** | Assistant, 12 months prepaid |
|---|---|---|---|---|---|---|
| 2 videos | business | $1,590 | — | $690 | **$2,280** | $1,352 |
| 4 videos | business | $1,590 | — | $1,090 | **$2,680** | $1,352 |
| 8 videos | business | $1,590 | — | $1,890 | **$3,480** | $1,352 |
| 16 videos | business | $1,590 | — | $3,490 | **$5,080** | $1,352 |

### 12. Average ticket

| Case | Plan | Assistant/month | Voice | Videos | **Total/month** | Assistant, 12 months prepaid |
|---|---|---|---|---|---|---|
| $200 | business | $1,490 | — | — | **$1,490** | $1,267 |
| $650 | business | $1,590 | — | — | **$1,590** | $1,352 |
| $2,500 | business | $1,590 | — | — | **$1,590** | $1,352 |
| $10,000 | business | $1,590 | — | — | **$1,590** | $1,352 |
| $50,000 | business | $1,690 | — | — | **$1,690** | $1,437 |

### 13. Industry (same config: 25 conv/day, scheduling + sales)

| Case | Plan | Assistant/month | Voice | Videos | **Total/month** | Assistant, 12 months prepaid |
|---|---|---|---|---|---|---|
| Medical/dental office | business | $2,290 | — | — | **$2,290** | $1,947 |
| Beauty salon, spa or barbershop | business | $2,290 | — | — | **$2,290** | $1,947 |
| Restaurant, café or food | business | $2,290 | — | — | **$2,290** | $1,947 |
| Real estate | business | $2,490 | — | — | **$2,490** | $2,117 |
| Law, accounting or notary firm | business | $2,390 | — | — | **$2,390** | $2,032 |
| Auto repair shop | business | $2,390 | — | — | **$2,390** | $2,032 |
| School, academy or courses | business | $2,290 | — | — | **$2,290** | $1,947 |
| Physical or online store | business | $2,490 | — | — | **$2,490** | $2,117 |
| Gym, yoga or sports | business | $2,290 | — | — | **$2,290** | $1,947 |
| Hotel, tours or events | business | $2,290 | — | — | **$2,290** | $1,947 |
| Veterinary or pets | business | $2,290 | — | — | **$2,290** | $1,947 |
| Construction, remodeling or installations | business | $2,490 | — | — | **$2,490** | $2,117 |
| Distributor, factory or wholesale | business | $2,790 | — | — | **$2,790** | $2,372 |
| Agency, consulting or insurance | business | $2,390 | — | — | **$2,390** | $2,032 |
| Car or motorcycle sales | business | $2,490 | — | — | **$2,490** | $2,117 |
| Other | business | $2,290 | — | — | **$2,290** | $1,947 |

### 14. Typical combinations

| Case | Plan | Assistant/month | Voice | Videos | **Total/month** | Assistant, 12 months prepaid |
|---|---|---|---|---|---|---|
| Barbershop, WhatsApp only | business | $1,890 | — | — | **$1,890** | $1,607 |
| Medical office with scheduling | business | $1,790 | — | — | **$1,790** | $1,522 |
| Dentist: scheduling + sales + social | business | $4,490 | — | — | **$4,490** | $3,817 |
| Restaurant, 2 branches | business | $5,890 | — | — | **$5,890** | $5,007 |
| Accounting firm | business | $1,890 | — | — | **$1,890** | $1,607 |
| Auto shop: quotes + scheduling | business | $2,490 | — | — | **$2,490** | $2,117 |
| Online store: sales + operations, 3 channels | business | $4,790 | — | — | **$4,790** | $4,072 |
| Distributor: quotes + purchasing + collections | business | $3,590 | — | — | **$3,590** | $3,052 |
| Real estate, everything | business | $14,890 | $8,090 (1,500 min) | $1,790 | **$24,770** | $12,657 |
| 30-person company: full team | enterprise | $19,490 | $7,890 (1,500 min) | — | **$27,380** | $16,567 |
| 80-person company: everything maxed | enterprise | $38,290 | $21,490 (4,500 min) | $5,190 | **$64,970** | $32,547 |

**Line items for the larger combinations** (labels as returned by Codify's API, in Spanish):

*Medical office with scheduling*

- Tu asistente: 10 conversaciones al día en WhatsApp: $1,590
- Agenda y recordatorios: $100
- Conexión con Google Calendar u otra agenda: $100

*Dentist: scheduling + sales + social*

- Tu asistente: 25 conversaciones al día en WhatsApp, Instagram: $1,990
- Agenda y recordatorios: $0
- Ventas y seguimiento: $300
- Redes sociales (5 publicaciones a la semana): $2,200

*Restaurant, 2 branches*

- Tu asistente: 60 conversaciones al día en WhatsApp, Instagram, 2 sucursales: $3,690
- Operación y reportes: $400
- Redes sociales (5 publicaciones a la semana): $1,800

*Accounting firm*

- Tu asistente: 10 conversaciones al día en WhatsApp: $1,690
- Agenda y recordatorios: $0
- Ventas y seguimiento: $100
- Cobranza: $100

*Auto shop: quotes + scheduling*

- Tu asistente: 25 conversaciones al día en WhatsApp: $1,990
- Agenda y recordatorios: $100
- Agente de cotizaciones: $400

*Online store: sales + operations, 3 channels*

- Tu asistente: 60 conversaciones al día en WhatsApp, Instagram, Chat en tu página: $3,090
- Ventas y seguimiento: $800
- Cobranza: $100
- Operación y reportes: $400
- Conexión con Punto de venta o inventario, Enlaces de pago: $400

*Distributor: quotes + purchasing + collections*

- Tu asistente: 25 conversaciones al día en WhatsApp: $2,290
- Ventas y seguimiento: $500
- Agente de cotizaciones: $400
- Cobranza: $0
- Agente de compras y proveedores: $200
- Conexión con Google Sheets o Excel: $200

*Real estate, everything*

- Tu asistente: 150 conversaciones al día en WhatsApp, Instagram, Messenger, Chat en tu página, Correo, 2 sucursales: $6,990
- Agenda y recordatorios: $200
- Ventas y seguimiento: $1,400
- Agente de cotizaciones: $1,000
- Cobranza: $200
- Agente de compras y proveedores: $200
- Operación y reportes: $400
- Redes sociales (7 publicaciones a la semana): $1,400
- Google y las IA (SEO) (8 artículos al mes): $900
- Anuncios: $300
- Conexión con Google Calendar u otra agenda, Tu CRM: $1,900

*30-person company: full team*

- Plan Empresarial: orquestador central, conexión a CRM o ERP y soporte con SLA (150 conversaciones al día, 2 sucursales): $16,490
- Agenda y recordatorios: $200
- Ventas y seguimiento: $2,000
- Cobranza: $200
- Operación y reportes: $300
- Conexión con Punto de venta o inventario, Tu sistema propio (API): $300

*80-person company: everything maxed*

- Plan Empresarial: orquestador central, conexión a CRM o ERP y soporte con SLA (450 conversaciones al día, 4 sucursales): $25,090
- Agenda y recordatorios: $600
- Ventas y seguimiento: $4,000
- Cobranza: $500
- Operación y reportes: $800
- Redes sociales (7 publicaciones a la semana): $900
- Google y las IA (SEO) (12 artículos al mes): $600
- Anuncios: $100
- Conexión con Google Calendar u otra agenda, Google Sheets o Excel, Punto de venta o inventario, Enlaces de pago, Tu sistema propio (API): $5,700
