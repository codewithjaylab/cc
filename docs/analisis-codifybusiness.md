# Análisis de codifybusiness.com

Fuente: scraping de 68 páginas públicas de https://codifybusiness.com (22-nov-2026).
El texto de cada página está en [`scraping/texto/`](scraping/texto) (completo) y en [`scraping/limpio/`](scraping/limpio) (sin menú ni pie repetidos).

## 1. Qué es

Codify Business es una agencia de CDMX (fundador: Emilio Cisneros) que vende **"un equipo de agentes de IA"** a pymes y empresas de México, LatAm y España.

- **Promesa:** "Un equipo de agentes de IA que atiende, vende y trabaja por tu negocio las 24 horas. Un agente principal coordina a todos y tú solo apruebas lo importante."
- **Posicionamiento:** "Tu asesor de IA, no un vendedor de software". Venden resultados (cero mensajes sin contestar, citas, ventas), no tecnología.
- **Mascota/demo viva:** "Codi", su propio agente principal. Se le puede hablar por voz desde el navegador, por teléfono o por chat. Hace las veces de demo y de vendedor.

## 2. Arquitectura de producto: orquestador + especialistas

| Agente | Qué hace |
|---|---|
| **Agente principal (orquestador)** | Recibe todo, reparte tareas, pide aprobación al dueño |
| Atención y ventas | WhatsApp, Instagram, Messenger, web; agenda, sigue y cobra (Stripe / Mercado Pago) |
| Voz | Contesta llamadas, agenda, manda resumen por WhatsApp |
| Marketing | Guiones, videos con avatar, carruseles, publicación diaria en TikTok/IG/FB |
| Cotizaciones | PDF con la marca del cliente en segundos |
| Compras | Compara proveedores, revisa existencias, prepara órdenes de compra |
| Agenda y cobranza | Recordatorios, confirmaciones, cobro amable |
| Operación y reportes | Gastos por foto de ticket, resumen diario de ventas |
| Google y las IA (SEO/AEO) | Blogs, perfil de Google, menciones en ChatGPT |
| A la medida | Inventario, postventa, reclutamiento, facturas, reseñas… |

Además venden servicios que no son agentes: CRM a la medida, software a la medida (desde $35,000), página web (desde $9,900), consultoría ("Asesor de IA", $29,900/mes; sesión de $9,900) y taller de IA para equipos ($24,900 por 3 h).

## 3. Precios (MXN + IVA, vigentes desde el 6-nov-2026)

**Paquetes de referencia**
- **Starter** (ventas + WhatsApp): $1,490 – $2,090/mes
- **Growth** (+ marketing autónomo): $5,280 – $8,080/mes
- **Enterprise** (orquestador, cotizaciones, compras, ERP/CRM, SLA; desde 16 personas): desde $11,690/mes

**Base por volumen:** 10 conversaciones al día $1,490 · 25 $1,890 · 60 $2,590 · 150 $4,590 · 300 $7,890 · más de 300, a la medida.

**Módulos:** agenda +$100 · ventas y seguimiento +$200 · cotizaciones +$300 · cobranza +$100 · compras +$200 · operación +$200 · redes +$1,900 · SEO/IA +$700 · anuncios +$200.

**Extras:** voz de 150 min $1,090 a 1,000 min $5,090 · videos con IA de 2/mes $590 a 30/mes $6,490 · número o sucursal extra desde $200 · pausa $490/mes.

**Reglas comerciales**
- Instalación gratis siempre, sin plazo forzoso (aviso de 30 días)
- Descuentos solo por pago adelantado: 5/10/15 % por 3/6/12 meses
- Uso visto como "batería": avisos al 80 y al 100 %; nunca dejan de contestar; recarga de +50 %
- Si el cliente usa menos del 40 % durante 3 meses, le bajan el precio sin que lo pida
- Mensajes de Meta, pagados aparte por el cliente directamente a Meta

## 4. Embudo y proceso de venta

1. **Configurador** de 2 minutos: el cliente elige giro y módulos y ve el precio en vivo. También pueden hablar con Codi.
2. **Demo gratis en menos de 24 h**: una página hecha para su negocio, con un chat para probar el asistente durante 7 días. No se conecta a su número real.
3. **Llamada de 15 minutos** con el precio exacto. Si la IA no le conviene, se lo dicen.
4. **Contrato en 48 h** con **3 metas medibles**. Acceso como invitado, nunca con contraseñas.
5. **Encendido** en su número por la vía oficial de WhatsApp, más 45 minutos de capacitación al equipo.
6. **Mejora continua**: cambios ilimitados el primer mes y después 4 al mes, entregados en 48 h.
7. **Reporte mensual en pesos** con ROI ("por cada $1 registraste $9"), más un resumen cada viernes.

**Garantía de 30 días:** si no se cumplen las 3 metas, devuelven el 50 % del primer mes.
**Soporte:** lo crítico se atiende en menos de 2 h cualquier día; lo alto, el mismo día hábil.

## 5. Adquisición

- **SEO/AEO agresivo:** más de 30 artículos de blog con intención de compra ("cuánto cuesta un agente de IA en México", "chatbot de WhatsApp precios", "n8n vs Make vs Zapier"), landings por giro (15 industrias) y por ciudad (CDMX). Cada página abre con una "Respuesta rápida" pensada para que la citen los LLM.
- **Casos con datos verificables** (Search Console y TikTok): R&R Legal pasó de 20 a 348 clics y cerró 7 clientes; Urbanus pasó de 0 a 6,337 apariciones; Lic. Luz Cisneros suma 60 mil vistas en TikTok.
- **Afiliados:** 10 % (1 a 4 clientes), 15 % (desde 5) y 20 % (desde 10) durante 12 meses. Para clientes: un mes gratis por cada recomendado.
- **Demo viva por voz** (Codi) y un video VSL de 4 minutos del fundador.

## 6. Tecnología que se deduce

WhatsApp Business Platform (API oficial) · n8n / Make / Zapier (los comparan en el blog) · modelos ChatGPT/OpenAI, Gemini y Claude · Google Calendar · CRM: HubSpot, Zoho, Pipedrive, Salesforce · pagos: Stripe y Mercado Pago · voz con número telefónico · video con avatar · Telegram o un panel como "canal del dueño", porque desde 2026 WhatsApp solo permite asistentes de temas del negocio · un entorno aislado por cliente.

## 7. Fortalezas y huecos (oportunidades)

**Fortalezas:** precios públicos y granulares, demo en 24 h, garantía con metas, reporte en pesos, confianza (cuentas a nombre del cliente, humano al mando) y una máquina de SEO/AEO muy trabajada.

**Huecos que una agencia nueva podría atacar:**
- Los 3 casos de éxito son de **marketing/SEO** (despachos legales, gestoría). No hay casos publicados de ventas por WhatsApp, voz ni compras, que es su producto central.
- Muy centrada en CDMX y en el español de México. Hay espacio en otras ciudades, en España o en EE. UU. hispano.
- Ofrecen todo para todos (15 giros, más software, consultoría y talleres). Una agencia **vertical** puede ganar en profundidad: integraciones con el software del giro, cumplimiento normativo, plantillas probadas.
- El precio de entrada es bajo ($1,490), así que el margen depende de una operación muy automatizada. Para competir hay que diferenciarse en valor, no en precio.
