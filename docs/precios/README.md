# Precios reales del configurador de Codify Business

Las cifras salen de la API que usa su configurador (`POST /api/precio`), consultada el 22-nov-2026 con 91 combinaciones. Todas están en MXN, sin IVA y al mes. Las respuestas completas están en [`respuestas-api.json`](respuestas-api.json).

> **Cómo se obtuvieron:** el configurador de la web pide el precio en vivo a `/api/precio` mientras el usuario contesta, sin registro ni captcha. Repliqué esas mismas peticiones con las opciones del formulario, a una por segundo. No envié el formulario final de contacto (`/api/lead`), porque crea un lead real y avisa a su equipo de ventas. El precio no depende de ese paso.

## Cómo calculan el precio

Tomando como referencia un **consultorio, solo WhatsApp y 10 conversaciones al día = $1,590**:

| Variable | Efecto en el precio |
|---|---|
| **Conversaciones al día** (lo que más pesa) | 10: $1,590 · 25: $1,990 · 60: $2,790 · 150: $4,790 · 300: $7,890 · más de 300: $11,190 |
| **Módulos** (con 10 conversaciones al día) | agenda +$100 · ventas +$100 · cobranza +$0 · cotizaciones +$200 · compras +$200 · operación +$300 · anuncios +$300 · SEO +$900 · redes +$2,100 |
| Módulos con más volumen | **El precio de cada módulo sube con las conversaciones.** "Ventas y seguimiento" cuesta +$100 con 10 al día, +$1,400 con 150 y +$4,000 con 450 en el plan empresa |
| Redes, según publicaciones a la semana | 3: +$1,900 · 5: +$2,100 · 7: +$2,400 |
| SEO, según artículos al mes | 4: +$900 · 8: +$1,000 · 12: +$1,200 |
| Anuncios, según inversión | No cambia el precio con poco volumen (+$300 siempre) |
| **Canales** | WhatsApp e Instagram cuestan lo mismo que solo WhatsApp. Desde el 3.er canal, **+$800**, y después ya no sube |
| **Sucursales** | 2: +$200 · 3: +$1,100 · 4: +$2,100 |
| **Integraciones** | +$200 cada una (calendario, hojas, CRM, punto de venta, pagos o sistema propio); las 6 juntas, +$1,000 |
| **Empleados** | De 1 a 15 no cambia. **Desde 16 personas pasa al plan "empresa"**: $11,290 con solo 10 conversaciones al día (7 veces más) |
| **Ticket promedio** (lo que paga cada cliente) | Menos de $300: $1,490 · de $300 a $20,000: $1,590 · más de $20,000: $1,690. **Cobran según el valor del cliente** |
| **Giro** | Con la misma configuración, de $2,290 a $2,790: distribuidoras y mayoreo cuestan más (catálogo de 1,000 productos); inmobiliarias, tiendas, construcción y autos, +$200 |
| **Voz** (se cobra aparte) | 4 llamadas al día: $3,190 (600 min) · 10: $7,390 (1,500 min) · 22: $14,390 (3,000 min) · 40: $21,490 (4,500 min, "a la medida"). Minuto extra: $5.90 |
| **Videos con IA** (se cobran aparte) | 2: $690 · 4: $1,090 · 8: $1,890 · 16: $3,490 al mes. Video extra: $390 |
| Pago adelantado | 5 % por 3 meses, 10 % por 6 y 15 % por 12 (solo sobre el asistente, no sobre voz ni videos) |
| Recarga de uso | Recarga de +50 % de uso a un precio fijo ($390 en el plan base, $3,590 con 300 conversaciones al día) |
| Permanencia | 0 meses en todos los casos |

## Hallazgos

1. **Los precios reales son unos $100 más altos que la tabla pública.** Por ejemplo, $1,590 frente a los $1,490 publicados para 10 conversaciones al día. El precio de $1,490 solo aparece si el ticket es menor a $300.
2. **El precio de cada módulo depende del volumen.** Los "+$100 / +$200" de la página de precios son el mínimo. Con 150 conversaciones al día, ventas cuesta $1,400 y cotizaciones $1,000.
3. **Lo que más dinero genera son la voz y el salto a "empresa".** Con 10 llamadas al día, la voz ya cuesta 4.6 veces más que el asistente. Y tener 16 personas o más multiplica el precio base por 7.
4. **Hay elementos de precio por valor del cliente:** el ticket promedio y el giro cambian el precio aunque el trabajo sea el mismo.
5. **Instagram sale gratis junto con WhatsApp.** Es un buen gancho: "el mismo agente en todos lados".
6. **Rangos de las combinaciones típicas:** barbería $1,890 · consultorio con agenda $1,790 · dentista con redes $4,490 · restaurante con 2 sucursales $5,890 · inmobiliaria con todo $24,770 (con voz y videos) · empresa de 30 personas $27,380 · empresa de 80 personas al máximo $64,970.

## Tablas completas

### 1. Volumen (consultorio, solo WhatsApp, sin módulos)

| Caso | Plan | Asistente/mes | Voz | Videos | **Total/mes** | Asistente pagando 12 meses |
|---|---|---|---|---|---|---|
| 10 conversaciones/día | negocio | $1,590 | — | — | **$1,590** | $1,352 |
| 25 conversaciones/día | negocio | $1,990 | — | — | **$1,990** | $1,692 |
| 60 conversaciones/día | negocio | $2,790 | — | — | **$2,790** | $2,372 |
| 150 conversaciones/día | negocio | $4,790 | — | — | **$4,790** | $4,072 |
| 300 conversaciones/día | negocio | $7,890 | — | — | **$7,890** | $6,707 |
| 450 conversaciones/día | negocio | $11,190 | — | — | **$11,190** | $9,512 |

### 2. Cada módulo solo (consultorio, 10 conv/día)

| Caso | Plan | Asistente/mes | Voz | Videos | **Total/mes** | Asistente pagando 12 meses |
|---|---|---|---|---|---|---|
| agenda | negocio | $1,690 | — | — | **$1,690** | $1,437 |
| ventas | negocio | $1,690 | — | — | **$1,690** | $1,437 |
| cotizaciones | negocio | $1,790 | — | — | **$1,790** | $1,522 |
| cobranza | negocio | $1,590 | — | — | **$1,590** | $1,352 |
| compras | negocio | $1,790 | — | — | **$1,790** | $1,522 |
| operacion | negocio | $1,890 | — | — | **$1,890** | $1,607 |
| redes | negocio | $3,690 | — | — | **$3,690** | $3,137 |
| seo | negocio | $2,490 | — | — | **$2,490** | $2,117 |
| anuncios | negocio | $1,890 | — | — | **$1,890** | $1,607 |

### 3. Redes: publicaciones/semana

| Caso | Plan | Asistente/mes | Voz | Videos | **Total/mes** | Asistente pagando 12 meses |
|---|---|---|---|---|---|---|
| 3/semana | negocio | $3,490 | — | — | **$3,490** | $2,967 |
| 5/semana | negocio | $3,690 | — | — | **$3,690** | $3,137 |
| 7/semana | negocio | $3,990 | — | — | **$3,990** | $3,392 |

### 4. SEO: artículos/mes

| Caso | Plan | Asistente/mes | Voz | Videos | **Total/mes** | Asistente pagando 12 meses |
|---|---|---|---|---|---|---|
| 4/mes | negocio | $2,490 | — | — | **$2,490** | $2,117 |
| 8/mes | negocio | $2,590 | — | — | **$2,590** | $2,202 |
| 12/mes | negocio | $2,790 | — | — | **$2,790** | $2,372 |

### 5. Anuncios: inversión mensual

| Caso | Plan | Asistente/mes | Voz | Videos | **Total/mes** | Asistente pagando 12 meses |
|---|---|---|---|---|---|---|
| $3,000 | negocio | $1,890 | — | — | **$1,890** | $1,607 |
| $12,000 | negocio | $1,890 | — | — | **$1,890** | $1,607 |
| $35,000 | negocio | $1,890 | — | — | **$1,890** | $1,607 |
| $80,000 | negocio | $1,890 | — | — | **$1,890** | $1,607 |

### 6. Número de canales

| Caso | Plan | Asistente/mes | Voz | Videos | **Total/mes** | Asistente pagando 12 meses |
|---|---|---|---|---|---|---|
| whatsapp | negocio | $1,590 | — | — | **$1,590** | $1,352 |
| whatsapp + instagram | negocio | $1,590 | — | — | **$1,590** | $1,352 |
| whatsapp + instagram + messenger | negocio | $2,390 | — | — | **$2,390** | $2,032 |
| whatsapp + instagram + messenger + web | negocio | $2,390 | — | — | **$2,390** | $2,032 |
| whatsapp + instagram + messenger + web + correo | negocio | $2,390 | — | — | **$2,390** | $2,032 |

### 7. Sucursales

| Caso | Plan | Asistente/mes | Voz | Videos | **Total/mes** | Asistente pagando 12 meses |
|---|---|---|---|---|---|---|
| 1 | negocio | $1,590 | — | — | **$1,590** | $1,352 |
| 2 | negocio | $1,790 | — | — | **$1,790** | $1,522 |
| 3 | negocio | $2,690 | — | — | **$2,690** | $2,287 |
| 4 | negocio | $3,690 | — | — | **$3,690** | $3,137 |

### 8. Cada integración

| Caso | Plan | Asistente/mes | Voz | Videos | **Total/mes** | Asistente pagando 12 meses |
|---|---|---|---|---|---|---|
| calendario | negocio | $1,790 | — | — | **$1,790** | $1,522 |
| hojas | negocio | $1,790 | — | — | **$1,790** | $1,522 |
| crm | negocio | $1,790 | — | — | **$1,790** | $1,522 |
| pos | negocio | $1,790 | — | — | **$1,790** | $1,522 |
| pagos | negocio | $1,790 | — | — | **$1,790** | $1,522 |
| sistema | negocio | $1,790 | — | — | **$1,790** | $1,522 |
| todas | negocio | $2,590 | — | — | **$2,590** | $2,202 |

### 9. Tamaño (empleados)

| Caso | Plan | Asistente/mes | Voz | Videos | **Total/mes** | Asistente pagando 12 meses |
|---|---|---|---|---|---|---|
| 1 personas | negocio | $1,590 | — | — | **$1,590** | $1,352 |
| 3 personas | negocio | $1,590 | — | — | **$1,590** | $1,352 |
| 10 personas | negocio | $1,590 | — | — | **$1,590** | $1,352 |
| 30 personas | empresa | $11,290 | — | — | **$11,290** | $9,597 |
| 80 personas | empresa | $11,290 | — | — | **$11,290** | $9,597 |

### 10. Voz: llamadas/día

| Caso | Plan | Asistente/mes | Voz | Videos | **Total/mes** | Asistente pagando 12 meses |
|---|---|---|---|---|---|---|
| 4 llamadas/día | negocio | $1,590 | $3,190 (600 min) | — | **$4,780** | $1,352 |
| 10 llamadas/día | negocio | $1,590 | $7,390 (1500 min) | — | **$8,980** | $1,352 |
| 22 llamadas/día | negocio | $1,590 | $14,390 (3000 min) | — | **$15,980** | $1,352 |
| 40 llamadas/día | negocio | $1,590 | $21,490 (4500 min) | — | **$23,080** | $1,352 |

### 11. Videos IA/mes

| Caso | Plan | Asistente/mes | Voz | Videos | **Total/mes** | Asistente pagando 12 meses |
|---|---|---|---|---|---|---|
| 2 videos | negocio | $1,590 | — | $690 | **$2,280** | $1,352 |
| 4 videos | negocio | $1,590 | — | $1,090 | **$2,680** | $1,352 |
| 8 videos | negocio | $1,590 | — | $1,890 | **$3,480** | $1,352 |
| 16 videos | negocio | $1,590 | — | $3,490 | **$5,080** | $1,352 |

### 12. Ticket promedio

| Caso | Plan | Asistente/mes | Voz | Videos | **Total/mes** | Asistente pagando 12 meses |
|---|---|---|---|---|---|---|
| $200 | negocio | $1,490 | — | — | **$1,490** | $1,267 |
| $650 | negocio | $1,590 | — | — | **$1,590** | $1,352 |
| $2,500 | negocio | $1,590 | — | — | **$1,590** | $1,352 |
| $10,000 | negocio | $1,590 | — | — | **$1,590** | $1,352 |
| $50,000 | negocio | $1,690 | — | — | **$1,690** | $1,437 |

### 13. Giro (misma config: 25 conv, agenda+ventas)

| Caso | Plan | Asistente/mes | Voz | Videos | **Total/mes** | Asistente pagando 12 meses |
|---|---|---|---|---|---|---|
| Consultorio, clínica o dentista | negocio | $2,290 | — | — | **$2,290** | $1,947 |
| Estética, spa o barbería | negocio | $2,290 | — | — | **$2,290** | $1,947 |
| Restaurante, café o comida | negocio | $2,290 | — | — | **$2,290** | $1,947 |
| Inmobiliaria o bienes raíces | negocio | $2,490 | — | — | **$2,490** | $2,117 |
| Despacho legal, contable o notaría | negocio | $2,390 | — | — | **$2,390** | $2,032 |
| Taller o servicio automotriz | negocio | $2,390 | — | — | **$2,390** | $2,032 |
| Escuela, academia o cursos | negocio | $2,290 | — | — | **$2,290** | $1,947 |
| Tienda física o en línea | negocio | $2,490 | — | — | **$2,490** | $2,117 |
| Gimnasio, yoga o deportes | negocio | $2,290 | — | — | **$2,290** | $1,947 |
| Hotel, tours o eventos | negocio | $2,290 | — | — | **$2,290** | $1,947 |
| Veterinaria o mascotas | negocio | $2,290 | — | — | **$2,290** | $1,947 |
| Construcción, remodelación o instalaciones | negocio | $2,490 | — | — | **$2,490** | $2,117 |
| Distribuidora, fábrica o mayoreo | negocio | $2,790 | — | — | **$2,790** | $2,372 |
| Agencia, consultoría o seguros | negocio | $2,390 | — | — | **$2,390** | $2,032 |
| Venta de autos o motos | negocio | $2,490 | — | — | **$2,490** | $2,117 |
| Otro | negocio | $2,290 | — | — | **$2,290** | $1,947 |

### 14. Combinaciones típicas

| Caso | Plan | Asistente/mes | Voz | Videos | **Total/mes** | Asistente pagando 12 meses |
|---|---|---|---|---|---|---|
| Barbería solo WhatsApp | negocio | $1,890 | — | — | **$1,890** | $1,607 |
| Consultorio con agenda | negocio | $1,790 | — | — | **$1,790** | $1,522 |
| Dentista: agenda+ventas+redes | negocio | $4,490 | — | — | **$4,490** | $3,817 |
| Restaurante 2 sucursales | negocio | $5,890 | — | — | **$5,890** | $5,007 |
| Despacho contable | negocio | $1,890 | — | — | **$1,890** | $1,607 |
| Taller: cotizaciones+agenda | negocio | $2,490 | — | — | **$2,490** | $2,117 |
| Tienda en línea: ventas+operación, 3 canales | negocio | $4,790 | — | — | **$4,790** | $4,072 |
| Distribuidora: cotizaciones+compras+cobranza | negocio | $3,590 | — | — | **$3,590** | $3,052 |
| Inmobiliaria con todo | negocio | $14,890 | $8,090 (1500 min) | $1,790 | **$24,770** | $12,657 |
| Empresa 30 personas: equipo completo | empresa | $19,490 | $7,890 (1500 min) | — | **$27,380** | $16,567 |
| Empresa 80 personas: todo al máximo | empresa | $38,290 | $21,490 (4500 min) | $5,190 | **$64,970** | $32,547 |

**Desglose de las combinaciones grandes:**

*Consultorio con agenda*

- Tu asistente: 10 conversaciones al día en WhatsApp: $1,590
- Agenda y recordatorios: $100
- Conexión con Google Calendar u otra agenda: $100

*Dentista: agenda+ventas+redes*

- Tu asistente: 25 conversaciones al día en WhatsApp, Instagram: $1,990
- Agenda y recordatorios: $0
- Ventas y seguimiento: $300
- Redes sociales (5 publicaciones a la semana): $2,200

*Restaurante 2 sucursales*

- Tu asistente: 60 conversaciones al día en WhatsApp, Instagram, 2 sucursales: $3,690
- Operación y reportes: $400
- Redes sociales (5 publicaciones a la semana): $1,800

*Despacho contable*

- Tu asistente: 10 conversaciones al día en WhatsApp: $1,690
- Agenda y recordatorios: $0
- Ventas y seguimiento: $100
- Cobranza: $100

*Taller: cotizaciones+agenda*

- Tu asistente: 25 conversaciones al día en WhatsApp: $1,990
- Agenda y recordatorios: $100
- Agente de cotizaciones: $400

*Tienda en línea: ventas+operación, 3 canales*

- Tu asistente: 60 conversaciones al día en WhatsApp, Instagram, Chat en tu página: $3,090
- Ventas y seguimiento: $800
- Cobranza: $100
- Operación y reportes: $400
- Conexión con Punto de venta o inventario, Enlaces de pago: $400

*Distribuidora: cotizaciones+compras+cobranza*

- Tu asistente: 25 conversaciones al día en WhatsApp: $2,290
- Ventas y seguimiento: $500
- Agente de cotizaciones: $400
- Cobranza: $0
- Agente de compras y proveedores: $200
- Conexión con Google Sheets o Excel: $200

*Inmobiliaria con todo*

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

*Empresa 30 personas: equipo completo*

- Plan Empresarial: orquestador central, conexión a CRM o ERP y soporte con SLA (150 conversaciones al día, 2 sucursales): $16,490
- Agenda y recordatorios: $200
- Ventas y seguimiento: $2,000
- Cobranza: $200
- Operación y reportes: $300
- Conexión con Punto de venta o inventario, Tu sistema propio (API): $300

*Empresa 80 personas: todo al máximo*

- Plan Empresarial: orquestador central, conexión a CRM o ERP y soporte con SLA (450 conversaciones al día, 4 sucursales): $25,090
- Agenda y recordatorios: $600
- Ventas y seguimiento: $4,000
- Cobranza: $500
- Operación y reportes: $800
- Redes sociales (7 publicaciones a la semana): $900
- Google y las IA (SEO) (12 artículos al mes): $600
- Anuncios: $100
- Conexión con Google Calendar u otra agenda, Google Sheets o Excel, Punto de venta o inventario, Enlaces de pago, Tu sistema propio (API): $5,700
