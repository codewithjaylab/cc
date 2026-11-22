# Plan: agencia de agentes de IA

Un plan para lanzar una agencia que vende "equipos de agentes de IA" a pymes. Toma como referencia el modelo de Codify Business ([análisis](analisis-codifybusiness.md)) y busca diferenciarse de él.

> Las cifras son supuestos de arranque, en MXN + IVA. Hay que validarlas con los primeros 10 clientes.

---

## 1. Propuesta de valor

**Una frase:** "Tu negocio contesta, cotiza, cobra y da seguimiento solo, 24/7, y tú solo apruebas lo importante. Si en 30 días no cumple tus metas, te devolvemos dinero."

**Lo que copiamos porque funciona:**
- La arquitectura de **orquestador + agentes especialistas** que el cliente "contrata" uno a uno
- La **demo personalizada en menos de 24 h** antes de pedir dinero
- **Precio público** por volumen y módulos, e instalación incluida
- **Garantía con 3 metas firmadas** y **reporte mensual en dinero**
- Las cuentas siempre a nombre del cliente, con acceso como invitado y un humano aprobando lo delicado

**Cómo nos diferenciamos (elegir 1 o 2):**
1. **Vertical primero.** Empezar con 1 o 2 giros y ser los mejores en ellos, en lugar de 15 giros a la vez. Candidatos con dinero, mucho WhatsApp y procesos repetibles: **clínicas dentales y estéticas**, **inmobiliarias**, **distribuidoras y ferreterías** (cotizaciones y pedidos de mayoreo).
2. **Casos de ventas medibles.** Codify solo publica casos de SEO y TikTok. Nosotros publicamos casos de conversaciones a cita a venta, con datos del CRM.
3. **Integraciones profundas con el software del giro** (agenda dental, CRM inmobiliario, ERP o Excel de la distribuidora) desde el primer día.
4. **Geografía** distinta: otra ciudad de México, Colombia, España o EE. UU. hispano.

---

## 2. Catálogo de agentes (fase 1 y fase 2)

| Fase | Agente | Entregable mínimo |
|---|---|---|
| 1 | **Atención y ventas (WhatsApp + IG)** | Responde FAQ con la base de conocimiento del cliente, califica leads, pasa a un humano con resumen |
| 1 | **Agenda y recordatorios** | Agenda en Google Calendar o el sistema del giro, confirma 24 h antes, reagenda |
| 1 | **Seguimiento y reactivación** | Escribe a quien dijo "lo pienso" y reactiva clientes inactivos con plantillas aprobadas |
| 1 | **Orquestador + canal del dueño** | Recibe órdenes del dueño por Telegram o un panel, pide aprobaciones y manda el resumen diario |
| 2 | Cotizaciones en PDF | Arma la cotización con el catálogo y la marca del cliente; el dueño la aprueba en un toque |
| 2 | Cobranza | Envía links de pago (Stripe / Mercado Pago), recuerda pagos y recibe comprobantes |
| 2 | Voz | Contesta llamadas, agenda y deja un resumen en WhatsApp |
| 2 | Marketing / contenido | Carruseles y videos semanales, revisados por el dueño antes de publicarse |
| 2 | Reseñas de Google | Pide la reseña después de la visita y contesta las reseñas |
| 3 | A la medida / Enterprise | Compras, inventario, ERP, reportes |

---

## 3. Precios propuestos

Hay que posicionarse **ligeramente por encima** de Codify en el vertical elegido, justificado por la especialización y por casos de ventas. No hay que competir por precio.

| Plan | Incluye | Precio/mes |
|---|---|---|
| **Esencial** | Atención y ventas, agenda, hasta 30 conversaciones al día, 1 canal | $1,990 |
| **Crecimiento** | Esencial, más seguimiento y reactivación, cotizaciones, cobranza, 2 canales, hasta 100 conversaciones al día | $4,990 |
| **Equipo completo** | Orquestador, todos los agentes, integración con CRM/ERP, SLA, hasta 300 conversaciones al día | desde $11,900 |

- **Extras:** voz (desde $1,190 por 150 min), contenido ($1,900), número o sucursal extra ($300).
- **Instalación:** gratis en mensual con permanencia mínima de 3 meses, o $4,900 sin permanencia. Esto protege el CAC; es una decisión a validar.
- **Pago adelantado:** 10 % de descuento por 6 meses y 15 % por 12.
- **Costos de Meta:** a cargo del cliente, que los paga directamente.

**Costo unitario objetivo:** LLM, infraestructura y WhatsApp por menos del 15 % del precio. Soporte y mejoras: 1 a 2 horas por cliente al mes. **Margen bruto objetivo: 70 % o más.**

---

## 4. Stack técnico

| Capa | Opción recomendada | Alternativas |
|---|---|---|
| Canal WhatsApp | WhatsApp Business Platform (Cloud API) vía un BSP (360dialog, Twilio) | — |
| Orquestación | **Código propio** (TypeScript/Python) con un SDK de agentes y tool use | n8n para prototipos e integraciones simples |
| Modelos | Claude (Sonnet para conversación, Haiku para clasificación y ruteo) | GPT, Gemini |
| Memoria y conocimiento | Postgres + pgvector (Supabase), una base de conocimiento por cliente | — |
| Voz | Proveedor de voz en tiempo real con número local (Vapi, Retell o Twilio + TTS) | — |
| Agenda | Google Calendar API y el sistema del vertical | Cal.com |
| Pagos | Stripe y Mercado Pago (links de pago) | — |
| CRM | HubSpot / Pipedrive vía API, o un CRM ligero propio | — |
| Canal del dueño | Bot de Telegram y un panel web (aprobaciones, pausa, métricas) | — |
| Observabilidad | Bitácora de cada acción del agente, evaluaciones automáticas y alertas | — |

**Principios:** un tenant aislado por cliente, prompts y reglas versionados, aprobación humana para descuentos, cobros y envíos masivos, botón de pausa, y exportación de datos (CSV/JSON) si el cliente se va.

---

## 5. Proceso de venta y entrega

1. **Lead** llega por SEO, contenido, afiliados o prospección.
2. **Configurador web** (2 min) que muestra el precio estimado y los beneficios por giro.
3. **Demo en menos de 24 h**: página personalizada y un chat de prueba con su información (catálogo, precios, horarios). Se genera de forma semiautomática con una plantilla del vertical y la información que manda el cliente.
4. **Llamada de 15 a 20 min**: precio exacto y **3 metas medibles**. Ejemplos: el 95 % de los mensajes contestados en menos de 1 minuto, 20 citas al mes, reactivar a 50 clientes.
5. **Contrato y accesos** (48 h). Verificación del número con Meta.
6. **Go-live** en 5 a 10 días hábiles, con 45 minutos de capacitación al equipo.
7. **Operación**: resumen cada viernes, reporte mensual en dinero (atendidos, citas, ventas, horas ahorradas, ROI), cambios en 48 h.
8. **Expansión**: en el día 60 y en el día 90 se propone el siguiente agente.

**Garantía:** si no se cumplen las 3 metas en 30 días, se devuelve el 50 % del primer mes.
**SLA:** lo crítico (el agente no contesta o dice algo grave) en menos de 2 h; las fallas de función, el mismo día hábil.

---

## 6. Adquisición de clientes

| Canal | Acción concreta | Meta a 90 días |
|---|---|---|
| **SEO/AEO** | 20 artículos del vertical con "respuesta rápida", landings por giro y ciudad, guía de precios | 2,000 visitas al mes |
| **Demo viva** | Nuestro propio agente atendiendo el WhatsApp y el teléfono de la agencia: el producto se vende solo | 100 % de los leads atendidos por él |
| **Prospección directa** | Lista de negocios del vertical (Google Maps); mensaje con un video de 60 s de "tu negocio atendido por IA" | 30 demos |
| **Contenido** | TikTok/Reels con casos y "antes y después" de conversaciones reales (anonimizadas) | 3 publicaciones por semana |
| **Afiliados** | Contadores, agencias de marketing y proveedores del vertical: 10 a 20 % durante 12 meses | 5 afiliados activos |
| **Alianzas** | Proveedores de software del vertical (agenda dental, CRM inmobiliario) | 1 alianza |

---

## 7. Equipo

| Etapa | Rol | Responsabilidad |
|---|---|---|
| 0–10 clientes | Fundador/a (ventas + producto) | Demos, cierre, diseño de agentes |
| 0–10 clientes | Ingeniero/a de agentes | Plataforma, integraciones, evaluaciones |
| 10–30 clientes | Customer success / implementador | Onboarding, cambios, reportes |
| 10–30 clientes | Contenido/SEO (puede ser medio tiempo o con agentes propios) | Blog, redes, casos |
| 30+ clientes | Ventas (SDR) | Prospección y agenda de demos |

Usamos nuestros propios agentes internamente: demo, reportes, contenido y prospección. Es parte del pitch.

---

## 8. Hoja de ruta (90 días)

**Semanas 1–2: fundación**
- Elegir el vertical y la ciudad. Entrevistar a 10 dueños de negocio.
- Nombre, dominio, WhatsApp Business verificado, contrato tipo, aviso de privacidad (LFPDPPP).

**Semanas 3–6: MVP**
- Plataforma mínima: WhatsApp, orquestador, agente de atención con agenda, panel del dueño y bitácora.
- Plantilla del vertical: base de conocimiento, flujos y evaluaciones.
- Generador de demos personalizadas y configurador de precio en la web.
- Agente propio en el WhatsApp de la agencia.

**Semanas 7–10: primeros clientes**
- 3 a 5 clientes piloto con un 50 % de descuento a cambio de caso de estudio y datos.
- Medir: tiempo de respuesta, citas, conversiones y costo por conversación.
- Iterar los prompts, las herramientas y el reporte mensual.

**Semanas 11–13: escalar**
- Publicar 2 casos con números reales.
- Lanzar los agentes de fase 2 (cotizaciones y cobranza).
- Arrancar el programa de afiliados y la prospección sistemática.

---

## 9. Métricas clave

- **Negocio:** MRR, número de clientes, ARPA, churn mensual (meta: menos del 4 %), CAC, payback (meta: menos de 3 meses), NRR (meta: más del 110 % con upsell de agentes).
- **Producto:** % de conversaciones resueltas sin humano, tiempo de respuesta, tasa de escalamiento, errores graves (meta: 0), costo por conversación.
- **Valor para el cliente:** citas o ventas atribuidas, horas ahorradas, ROI del reporte mensual.

**Meta a 12 meses (ilustrativa):** 40 clientes con un ARPA de $4,500, es decir, unos **$180k MXN de MRR**.

---

## 10. Riesgos y cómo mitigarlos

| Riesgo | Mitigación |
|---|---|
| Políticas de Meta (desde 2026 WhatsApp solo permite asistentes del negocio) | El agente de clientes se limita al negocio; el canal del dueño vive en Telegram o en el panel; se usa solo la API oficial |
| Alucinaciones o respuestas dañinas | Responder solo con información aprobada, evaluaciones automáticas, aprobación humana para lo delicado, botón de pausa |
| Costos de LLM o voz que se disparan | Modelo de "batería" de uso, ruteo a modelos baratos, límites por plan |
| Dependencia del fundador en ventas | Configurador, demos automáticas y agente vendedor propio |
| Competencia en precio | Especialización vertical, integraciones y casos de ventas medibles |
| Datos personales (LFPDPPP / RGPD) | Aviso de privacidad, tenant aislado, exportación y borrado al salir, mínimo privilegio |

---

## 11. Próximos pasos inmediatos

1. Decidir el **vertical** y la **geografía** (sección 1).
2. Validar los precios con 10 entrevistas.
3. Definir el nombre y la marca.
4. Arrancar el MVP técnico (sección 4). Este repo puede alojar el código del orquestador y de los agentes.
