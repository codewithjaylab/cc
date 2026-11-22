# Estudio de mercado: agencia de agentes de IA para pymes en México

**Proyecto:** VendeMás Business / Vende Más Studio (nombre tentativo, ver el [plan](plan-agencia-agentes.md))
**Fecha:** 22-nov-2026 · **Alcance:** México, pymes de servicios que atienden a sus clientes por WhatsApp
**Método:** investigación de escritorio con fuentes públicas (INEGI/DataMéxico, Meta, medios y proveedores), más los [precios reales de Codify](precios/README.md) obtenidos de su configurador. No incluye entrevistas a clientes; se proponen en la sección 8.

> Las cifras de terceros (sobre todo blogs de proveedores) se marcan como tales. Las estimaciones propias se marcan como **supuesto**.

---

## 1. Resumen ejecutivo

- **El mercado existe y crece:** México tiene **~5.47 millones de unidades económicas** (Censo Económico 2024). Entre el 47 % y el 64 % de las pymes dice usar ya alguna IA, pero casi siempre de forma básica. El mercado de IA conversacional en México se estima en **~US$319 M en 2025 y ~US$959 M en 2030** (~20 % de crecimiento anual, MarketsandMarkets).
- **WhatsApp es el canal:** según Meta, el **92 % de las mipymes** usa WhatsApp Business y más del 80 % de los adultos conversa con algún negocio por WhatsApp cada semana. Según Kantar, el 71 % prefiere la mensajería para tratar con empresas.
- **La competencia está fragmentada en tres tipos:** agencias que lo hacen todo por el cliente (Codify, SmartLeads, Kosmo…), software que el negocio configura solo (Leadsales, Kommo, ManyChat, Whaticket…) y freelancers con n8n/Make. Los precios de las agencias van de **~$1,000 a $25,000 MXN al mes**. El rango más común para una pyme es **$2,000–$6,000**.
- **El hueco:** casi nadie vende **resultados de ventas medidos por giro**. Las agencias generalistas atienden "a todos" y el software deja al dueño solo con la configuración.
- **Giro recomendado para empezar:** **consultorios dentales y clínicas** (76 mil unidades, ticket alto, dolor claro de citas y faltas). Como segundo giro, **inmobiliarias** (ticket muy alto, leads que se enfrían en minutos). Las estéticas y barberías son un mercado enorme (311 mil), pero con ticket bajo: conviene un producto más automatizado, más adelante.
- **Riesgos principales:** las políticas de Meta (desde el 15-ene-2026 no se permiten chatbots de IA de propósito general en la API; los de atención y ventas del negocio sí), el alza de tarifas de Meta (marketing +~30 % en México desde oct-2026) y el **escepticismo sobre el ROI de la IA** en México (Expansión, jul-2026).

---

## 2. Tamaño del mercado

### 2.1 Arriba hacia abajo (contexto)

| Indicador | Valor | Fuente |
|---|---|---|
| Unidades económicas (privadas + paraestatales) | 5,468,180 | INEGI, Censo Económico 2024 (definitivos) |
| Personal ocupado | 27,965,433 | INEGI, CE 2024 |
| Mipymes que usan WhatsApp Business | 92 % | Meta (feb-2025), cifra de la propia empresa |
| Pymes que usan alguna IA | 47 %–64 % | Microsoft Encuesta Pymes 2025 (64 % MX), otros estudios |
| Mercado de IA conversacional en México | US$318.6 M (2025) → US$958.8 M (2030) | MarketsandMarkets |
| Mercado de IA conversacional en LatAm | ~US$1.1 B (2025) → ~US$3.3 B (2030) | MarketsandMarkets |
| IA agéntica empresarial en México | US$103.7 M (2024) → US$935.4 M (2030) | Computer Weekly |

### 2.2 Abajo hacia arriba por giro (lo que de verdad podemos vender)

Las unidades económicas salen de DataMéxico/DENUE (may-2026). El % accesible, el precio y los ingresos son **supuestos** que hay que validar.

| Giro | Unidades | Concentración | % accesible (supuesto)* | Precio prom./mes (supuesto) | Mercado accesible al año (MXN) |
|---|---|---|---|---|---|
| Consultorios dentales | 76,188 | Edomex 10.2k · CDMX 7.5k · Jal 4.8k | 10 % → 7,600 | $2,500 | **~$228 M** |
| Salones y clínicas de belleza | 310,869 | Edomex 47.1k · CDMX 25.3k · Jal 24.8k | 5 % → 15,500 | $1,900 | **~$354 M** |
| Preparación de alimentos (restaurantes, rama 7225) | 740,231 | Edomex 93.2k · CDMX 57.2k · Ver 51.8k | 3 % → 22,200 | $3,000 | **~$800 M** |
| Inmobiliarias y corredores (rama 5312) | 8,243 | — | 30 % → 2,500 | $4,500 | **~$135 M** |
| **Total de 4 giros** | | | **~47,800 negocios** | | **~$1,500 M MXN al año** |

\* "Accesible" significa que tiene volumen de mensajes (10 o más al día), puede pagar y está en una zona que atendemos. La mayoría son microempresas (el 99.8 % de los salones tiene menos de 10 empleados, según un tercero), así que el % accesible es bajo a propósito.

### 2.3 Meta realista (SOM)

- **Año 1:** 40 clientes × $4,500 de ARPA = **~$2.2 M MXN de ARR**, es decir, el 0.15 % del mercado accesible de los 4 giros. Es conservador y alcanzable con un solo vertical.
- **Año 3:** 300 clientes en 2 giros = ~$16 M MXN de ARR (supuesto).

---

## 3. El cliente

**Perfil principal:** dueño o dueña de un negocio de servicios con 2 a 15 personas, que **atiende a sus clientes por WhatsApp desde su propio celular**, contesta tarde por la noche y no tiene recepcionista de tiempo completo, o tiene una que cubre solo ~48 de las 168 horas de la semana.

**Problemas que más pesan** (del análisis de Codify y de las fuentes):
1. Mensajes sin contestar o contestados tarde, sobre todo de noche y en fin de semana.
2. Citas que no se confirman, faltas y huecos en la agenda.
3. Interesados que dicen "lo pienso" y nunca reciben seguimiento.
4. Cotizar y cobrar a mano.
5. Falta de tiempo: según una nota de Expansión (mar-2026), el 53 % de las pymes carece de tiempo para operar su negocio.

**Contra qué nos compara (precio de referencia):**
- **Una recepcionista:** el salario mínimo de 2026 es **$315.04 al día ≈ $9,582 al mes** ($13,410 en la frontera norte), antes de IMSS y prestaciones. Un asistente de $2,000–$4,500 al mes cuesta entre el 20 % y el 45 % de eso y atiende 24/7.
- **Hacerlo gratis:** WhatsApp Business con respuestas rápidas, o un sobrino que "le sabe".

**Objeciones esperadas:** "la IA se equivoca", "mis clientes quieren hablar con una persona", "ya lo intenté con un bot y fue malo" y "no veo el retorno". Este último aparece en una nota de Expansión de jul-2026: *México, escéptico de la IA: no ve valor que justifique la inversión*. Por eso son clave la demo gratis, la garantía con metas y el reporte en dinero.

---

## 4. Competencia

### 4.1 Mapa

| Tipo | Ejemplos | Precio (MXN/mes salvo que se indique) | Fortaleza | Debilidad |
|---|---|---|---|---|
| **Agencia "hecho para ti" con IA** | **Codify Business** | $1,590–$11,190 por volumen; empresa desde $11,290; voz y videos aparte ([detalle](precios/README.md)) | Orquestador, demo en 24 h, garantía, SEO/AEO muy fuerte | Generalista (16 giros); sus casos de éxito son de marketing, no de ventas |
| | SmartLeads | $2,900 / $5,900 / $9,900 | Configuración incluida | Precio de entrada alto |
| | Kosmo IA | desde $4,497 | Cupo por clientes nuevos | Caro para un micronegocio |
| | Pezeta | $999 – $9,999 | Precio de entrada bajo | Poca diferenciación |
| | Simplixy | $12,900–$35,900 pago único, más API | Sin mensualidad | No hay mejora continua |
| **Software (el dueño lo configura)** | Leadsales (MX) | $2,363 – $3,240 | CRM y bandeja compartida, marca mexicana | El cliente hace el trabajo; no todas sus integraciones son oficiales |
| | Kommo | ~USD, por usuario | Más de 200 integraciones, pipeline | Curva de aprendizaje |
| | Treble | Cotización (B2B) | Flujos para empresas medianas | No es para micronegocios |
| | ManyChat / Whaticket / Aurora Inbox | US$29–39 al mes / $1,800 | Baratos | Hay que armarlo; la IA tiene tope o se paga aparte |
| **Freelancers / n8n / Make** | Muchos | $5k–$30k de proyecto | Barato al inicio | Sin soporte ni medición; se rompe |
| **Nativo de Meta** | Funciones de IA de WhatsApp Business / Meta AI | Gratis o bajo | Ya viene en la app | Genérico, sin integraciones ni reporte |

Los precios de los blogs de proveedores (Kosmo, SmartLeads, Aurora, Leadsales) son referencias, no cotizaciones verificadas.

### 4.2 Posicionamiento propuesto

```
            Generalista ◄──────────────────────► Especialista por giro
                 │                                        │
 Hecho para ti   │  Codify, SmartLeads, Kosmo    ★ VendeMás (dental / inmobiliario)
                 │                                        │
 Lo configuras   │  ManyChat, Whaticket, Kommo   Software vertical (agendas dentales,
 tú              │  Leadsales                    CRMs inmobiliarios) → posibles aliados
```

**Mensaje:** "No vendemos un bot: te entregamos más citas y más ventas, medidas en pesos, para tu giro."

---

## 5. Elección de giro (matriz de puntuación)

Escala de 1 a 5 (5 = mejor). Ponderación entre paréntesis.

| Criterio | Dental / clínicas | Inmobiliarias | Belleza / barberías | Restaurantes | Distribuidoras |
|---|---|---|---|---|---|
| Volumen de WhatsApp (20 %) | 4 | 5 | 5 | 5 | 3 |
| Ticket y capacidad de pago (20 %) | 4 | 5 | 2 | 2 | 5 |
| Dolor claro y medible (20 %) | 5 (faltas, citas) | 5 (leads fríos) | 4 | 3 | 4 (cotizar) |
| Tamaño del mercado (15 %) | 4 | 2 | 5 | 5 | 3 |
| Facilidad de entrega (15 %) | 4 (agenda) | 3 (CRM, portales) | 5 | 2 (cocina, POS) | 2 (ERP) |
| Competencia especializada (10 %) | 3 | 3 | 2 (AgendaPro, etc.) | 2 | 4 |
| **Puntaje ponderado** | **4.10** | **4.05** | **3.9** | **3.3** | **3.6** |

**Recomendación:** empezar con **consultorios dentales y clínicas** en **CDMX y Estado de México**, que juntos suman ~17.6 mil consultorios dentales. Sumar **inmobiliarias** como segundo giro (más ticket y más precio por cliente). Belleza puede ser una línea "lite" de autoservicio más adelante.

---

## 6. Precio: qué está dispuesto a pagar el mercado

| Segmento | Rango observado | Propuesta (ver el plan) |
|---|---|---|
| Micronegocio, 1 canal, poco volumen | $999 – $1,890 | No competir aquí al inicio |
| Pyme con agenda y seguimiento | $1,990 – $4,500 | **Esencial $1,990 / Crecimiento $4,990** |
| Pyme con varias sucursales o mucho volumen | $5,000 – $12,000 | Crecimiento + extras |
| Empresa (16 personas o más, integraciones) | $11,000 – $65,000 | Equipo completo desde $11,900 |

**Costos que paga el cliente** (Meta, por mensaje desde jul-2025): las plantillas de marketing subieron ~30 % en México el 1-oct-2026, y las de utilidad se cobran incluso dentro de la ventana de 24 h desde esa misma fecha. Hay que **explicarlo desde la propuesta** y diseñar el agente para usar sobre todo mensajes de servicio, que son gratis cuando el cliente escribe primero.

---

## 7. Riesgos de mercado y regulatorios

| Riesgo | Detalle | Mitigación |
|---|---|---|
| Política de WhatsApp | Desde el 15-ene-2026 se prohíben los chatbots de IA de **propósito general** en la Business API. Los de atención y ventas del negocio siguen permitidos | El agente de clientes solo habla del negocio; el "asistente del dueño" vive en Telegram o en un panel |
| Tarifas de Meta | Suben y cambian de modelo con frecuencia | Avisarlo en la propuesta, optimizar para mensajes de servicio y que el cliente pague directo a Meta |
| Escepticismo sobre el ROI | El mercado mexicano duda del valor de la IA | Demo con sus datos, garantía con metas y reporte en pesos |
| Meta lanza su propia IA para negocios | Competencia gratis y nativa | Diferenciarse con integraciones, giro, medición y humano al mando |
| Datos personales | LFPDPPP (y datos de salud en clínicas: datos sensibles) | Aviso de privacidad, consentimiento, mínimo de datos clínicos en el chat, tenant aislado |
| Copia por la competencia | Barreras de entrada bajas | Casos por giro, plantillas probadas, alianzas con software del giro |

---

## 8. Validación primaria (siguiente paso)

1. **15 entrevistas** con dueños de consultorios dentales en CDMX/Edomex (30 min). Preguntas: cuántos mensajes al día, quién contesta y a qué hora, cuántas faltas por semana, cuánto vale una consulta o tratamiento, qué han probado y cuánto pagarían.
2. **Prueba de humo:** landing "Agente para dentistas" con precio y demo gratis, más $3–5 mil en anuncios de Meta. Medir el costo por lead y la conversión a demo.
3. **Cliente oculto:** escribir por WhatsApp a 50 consultorios a las 21:00 y medir el tiempo de respuesta y cuántos contestan. Es un dato propio para el pitch ("el X % de los dentistas de tu zona no contesta de noche").
4. **3 pilotos** con descuento a cambio de un caso de estudio con datos (citas, faltas, ventas).

---

## Fuentes

- INEGI, Censos Económicos 2024 (resultados definitivos): https://www.inegi.org.mx/contenidos/saladeprensa/boletines/2025/ce/CE2024_def.pdf
- INEGI, Estadísticas a propósito de las mipymes 2025: https://www.inegi.org.mx/contenidos/saladeprensa/aproposito/2025/EAP_MIPYMES_25.pdf
- DataMéxico, consultorios dentales: https://www.economia.gob.mx/datamexico/es/profile/industry/offices-of-dentists
- DataMéxico, salones y clínicas de belleza: https://www.economia.gob.mx/datamexico/es/profile/industry/personal-care-services
- DataMéxico, restaurantes: https://www.economia.gob.mx/datamexico/es/profile/industry/restaurants-and-other-eating-places
- DataMéxico, inmobiliarias y corredores: https://www.economia.gob.mx/datamexico/es/profile/industry/real-estate-agents-and-brokers
- Microsoft, Encuesta Pymes 2025: https://news.microsoft.com/source/latam/noticias-de-microsoft/encuesta-pymes-2025-54-de-las-pymes-en-las-americas-usa-ia/
- Xataka, 2.5 millones de empresas usando IA: https://www.xataka.com.mx/robotica-e-ia/mexico-tiene-2-5-millones-empresas-usando-ia-problema-que-mayoria-solo-usa-para-basico
- Expansión, 53 % de las pymes carece de tiempo: https://expansion.mx/tecnologia/2026/03/12/53-de-las-pymes-carece-de-tiempo-para-operar-su-negocio-la-ia-emerge-como-solucion
- Expansión, México escéptico de la IA: https://expansion.mx/tecnologia/2026/07/15/mexico-esceptico-ia-no-ve-valor-justifique-inversion
- Expansión, mexicanos confían en WhatsApp para comunicarse con empresas: https://expansion.mx/tecnologia/2025/03/11/mexicanos-confia-whatsapp-comunicarse-empresas
- Mobile Time, WhatsApp Business y pymes en México: https://mobiletime.la/noticias/28/02/2025/whatsapp-business-pymes-mexico/
- MarketsandMarkets, IA conversacional en México: https://www.marketsandmarkets.com/Market-Reports/geography/conversational-ai-market/Mexico
- MarketsandMarkets, IA conversacional en LatAm: https://www.marketsandmarkets.com/Market-Reports/geography/conversational-ai-market/Latin-America
- Computer Weekly, IA agéntica en México: https://www.computerweekly.com/es/noticias/366630151/Mercado-de-IA-agentica-empresarial-en-Mexico-alcanzaria-9354-MDD-en-2030
- Meta, precios de WhatsApp Business Platform: https://developers.facebook.com/docs/whatsapp/pricing
- Gupshup, changelog de octubre de 2026 (tarifas en México): https://partner-docs.gupshup.io/changelog/october-2026
- TechCrunch, WhatsApp prohíbe los chatbots de propósito general: https://techcrunch.com/2025/10/18/whatssapp-changes-its-terms-to-bar-general-purpose-chatbots-from-its-platform/
- respond.io, alcance de la prohibición: https://respond.io/es/blog/whatsapp-general-purpose-chatbots-ban
- Salario mínimo 2026 (BBVA): https://www.bbva.mx/educacion-financiera/banca-digital/portabilidad-de-nomina/portabilidad-salario-minimo-mexico.html
- Precios de competidores (blogs de proveedores): https://smartdevs.com.mx/smartleads/blog/cuanto-cuesta-chatbot-whatsapp-ia-mexico/ · https://kosmo.com.mx/blog/mejores-chatbots-whatsapp-mexico · https://chatbot.pezetasolutions.com/ · https://simplixy.com.mx/precio-chatbot-whatsapp-mexico/ · https://www.aurorainbox.com/en/2025/05/17/how-much-does-a-whatsapp-chatbot-cost-in-mexico/ · https://leadsales.io/blog/leadsales-vs-kommo/
- Codify Business, precios del configurador: [docs/precios/](precios/README.md)
