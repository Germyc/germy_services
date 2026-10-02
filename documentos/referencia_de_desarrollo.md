# Referencia de desarrollo — Germy Services

Guía operativa para diagnosticar, cotizar e implementar las propuestas de la landing (`index.html`) siguiendo el método de venta local descrito en *Como vender páginas web a los comercios del barrio de burzaco.md*.

**Uso:** cada prospecto recorre las mismas fases: Detección → Diagnóstico → Propuesta → Implementación → Entrega y postventa. No saltear fases: el diagnóstico define el paquete, y el paquete define el alcance escrito.

---

## 0. Paquetes de referencia (los de la landing)

| # | Paquete | Ideal para | Entregables core | Forma de cobrar |
| :-- | :-- | :-- | :-- | :-- |
| 1 | **Presencia local** | Oficios, profesionales, comercios simples | Landing (servicios), mapa, horarios, botón WhatsApp, formulario, dominio + config básica | Implementación + mantenimiento opcional |
| 2 | **Catálogo que consulta** | Repuestos, indumentaria, mueblerías, corralones, mayoristas | Paquete 1 + productos/categorías, fotos, filtros simples, consulta por WhatsApp | Implementación mayor + carga inicial limitada |
| 3 | **Turnos o reservas** | Salud, estética, gimnasios, salones, gastronomía | Paquete 1 + CTA fuertes + turnos/reservas o integración de agenda | Implementación + mensual |
| 4 | **Tienda online** | Venta repetible con logística definida | Catálogo, carrito, pagos, envíos, stock básico, capacitación | Proyecto por etapas + soporte mensual |

**Regla de selección:** si el comercio todavía no ordenó catálogo, stock, pagos y entregas → **no** ofrecer paquete 4. Empezar por 1 o 2.

---

## 1. Detección del prospecto (antes de contactar)

Señales para priorizar (de la guía de venta):

- [ ] Instagram/Facebook activos pero **sin sitio propio**.
- [ ] Ficha de Google **sin web, sin horarios actualizados o sin enlace a WhatsApp**.
- [ ] Sitio viejo, lento o incómodo desde el celular.
- [ ] Rubros donde una consulta vale dinero: odontólogos, abogados, arquitectos, talleres, inmobiliarias, electricistas, casas de repuestos, corralones, mueblerías, gimnasios, estéticas, salones, gastronómicos, indumentaria.
- [ ] Buena reputación + reseñas, pero presencia digital pobre (indica negocio que funciona y con interés/presupuesto).

Registro mínimo por prospecto: `nombre · contacto · tiene web? · problema detectado · redes · reseñas · potencial (1-5) · paquete sugerido`.

---

## 2. Fase de diagnóstico (reunión de 15 minutos)

### 2.1 Preguntas guía (hacer primero, hablar después)

1. ¿De dónde vienen hoy las consultas? (Instagram, WhatsApp, boca a boca, Google, otro)
2. ¿Qué productos o servicios dejan mejor margen?
3. ¿Cuánto tarda alguien en responder el WhatsApp? ¿Quién responde?
4. ¿Qué dudas se repiten siempre? (precio, horario, stock, ubicación, turnos)
5. ¿Cuántas consultas se pierden a la semana más o menos?
6. ¿Hay catálogo ordenado? ¿Fotos propias? ¿Precios actualizados?
7. ¿Se toman turnos? ¿Cómo se agenda hoy? (cuaderno, WhatsApp, app)
8. ¿Se vende y se entrega? ¿Cómo se cobra y qué zona se reparte?
9. ¿Alguien puede aportar contenido (logo, fotos, lista de servicios)?

### 2.2 Qué revisar (evidencia, no opiniones)

- [ ] Ficha de Google Business: categoría, horarios, fotos, enlace, reseñas.
- [ ] Búsqueda de su rubro + zona en incógnito (¿aparece? ¿quién aparece?).
- [ ] Perfil de Instagram: enlace, coherencia de datos, frecuencia de publicación.
- [ ] Sitio actual (si existe): velocidad, comportamiento en celular, datos de contacto visibles.
- [ ] Capturas de pantalla de todo lo anterior (guardarlas: son el "mostrar el problema").

### 2.3 Conectar el problema con una pérdida concreta

Forma correcta: *"Si alguien busca esto a las 22 h, hoy no sabe horario, ubicación ni qué ofrecer"*.
Nunca criticar agresivamente; describir fricción y consecuencia.

### 2.4 Diagnóstico → paquete recomendado

| Si el problema principal es… | Paquete sugerido |
| :-- | :-- |
| No aparece en Google / no tiene web / todo vive en Instagram | **1. Presencia local** |
| Catálogo grande que hoy se responde uno por uno por WhatsApp | **2. Catálogo que consulta** |
| Turnos y reservas manejados por mensajes perdidos | **3. Turnos o reservas** |
| Venta repetible, stock ordenado y logística definida | **4. Tienda online** |
| Catálogo + logística pero sin stock/pagos ordenados | Empezar por **2**, escalar a **4** por etapas |

### 2.5 Cierre del diagnóstico

Pregunta de cierre:

> "Si te preparo esta versión con servicios, mapa, horarios, WhatsApp y una sección para que Google la indexe, ¿te serviría para empezar a captar consultas sin depender sólo de redes?"

Siguiente paso siempre chico: reserva de fecha, envío de propuesta o demo de 10 minutos. **No cerrar el proyecto entero parado en el mostrador.**

---

## 3. Fase de propuesta (qué poner por escrito)

Estructura mínima de toda propuesta:

1. **Alcance:** páginas/secciones entregadas (nombre por nombre).
2. **Rondas de cambios incluidas:** 2 (estándar de la landing).
3. **Qué aporta el comercio:** logo, fotos, textos/base de servicios, datos de contacto, accesos.
4. **Dominio y hosting:** titularidad del cliente, aclarado explícitamente.
5. **Fecha de entrega estimada**, condicionada a recibir el material.
6. **Pago:** adelanto para iniciar + saldo al aprobar antes de publicar.
7. **Soporte inicial y precio de mantenimiento mensual** (opcional, con beneficios concretos).
8. **No incluido:** fotografía profesional, pauta publicitaria, carga ilimitada de productos, redacción extensa, integraciones especiales.

No regalar el desarrollo completo "para probar": auditoría breve, llamada o maqueta de portada sin costo sí; desarrollo con anticipo y condiciones.

---

## 4. Fase de implementación

### 4.1 Base común (todos los paquetes)

1. **Repo y entorno**
   - Repositorio por cliente (GitHub) o monorepo con carpetas `clients/<slug>/`.
   - HTML/CSS/JS estático por defecto; sin frameworks salvo necesidad real.
   - Ambiente de preview antes de publicar (rama `preview` o Vercel preview).
2. **Estructura base del sitio**
   - `index.html` con: servicios, sobre el negocio, ubicación/mapa, horarios, contacto, CTA WhatsApp fijo.
   - Navegación simple (1 clic a WhatsApp desde cualquier punto).
3. **WhatsApp**
   - Link `https://wa.me/<numero>?text=...` con mensaje pre-cargado por sección.
   - Texto sugerido: *"Hola, vi [negocio] y quiero consultar por [servicio/producto]"*.
   - Botón visible sin scrollear (móvil) + `float` en pantallas chicas.
4. **SEO local**
   - `<title>` con rubro + zona; `meta description`; `lang="es"`.
   - JSON-LD (`LocalBusiness` o tipo específico: `Dentist`, `Restaurant`, `AutoRepair`…): nombre, dirección, teléfono, `openingHours`, `areaServed`, `url`.
   - H1 único; encabezados jerárquicos; `alt` en todas las imágenes.
   - Archivos `robots.txt` + `sitemap.xml`; favicon.
   - Coherencia de NAP (nombre, dirección, teléfono) idéntica a la ficha de Google.
5. **Rendimiento y móvil**
   - Imágenes en WebP, comprimidas; lazy loading; sin JS innecesario.
   - Objetivo: carga cómoda en 3G/4G y texto legible sin zoom.
6. **Accesibilidad**
   - Contraste AA, foco visible, skip link, elementos `<button>/<a>` reales, `prefers-reduced-motion`.
7. **Despliegue**
   - Dominio propio **a nombre del cliente** + hosting configurado (Vercel / GitHub Pages).
   - HTTPS activo; accesos entregados al cliente.
8. **Indexación**
   - Google Search Console: verificar dominio, enviar sitemap.
   - Ficha de Google: actualizar enlace web, horarios y categoría.
9. **QA antes de publicar** (checklist §5).

### 4.2 Paquete 1 — Presencia local

**Diagnóstico específico**
- ¿Aparece buscando "rubro + ciudad"? ¿Qué dice su ficha de Google?
- ¿Los datos de contacto están en el primer pantallazo?
- ¿Tiene fotos propias o solo de Instagram?

**Pasos de implementación**
1. One-pager responsive: hero (rubro + propuesta + CTA), servicios, testimonios/reseñas (si existen), zona de cobertura, FAQ breve.
2. Sección de contacto: mapa embebido (Google Maps embed), horarios en tabla, dirección, teléfono.
3. Formulario simple (o solo CTA WhatsApp si el cliente no revisa email).
4. Datos estructurados `LocalBusiness` + enlace desde la ficha de Google.
5. Dominio y hosting del cliente; redirección del dominio viejo si existía (301).
6. Entrega: accesos + mini capacitación (cómo cambiar horarios/promo).

**Plazo orientativo:** 3–7 días hábiles desde recibir material.

### 4.3 Paquete 2 — Catálogo que consulta

**Diagnóstico específico**
- ¿Cuántos productos/SKUs? ¿Hay fotos utilizables? ¿Precios actualizados?
- ¿Cómo responde hoy las consultas de stock/precio? ¿Cuánto tiempo consume?
- ¿Hay categorías naturales? ¿Los más consultados están destacados?

**Pasos de implementación**
1. Definir taxonomía: categorías → subcategorías → items (máx. 2 niveles para no complicar).
2. Definir el contrato de datos del producto: `nombre, categoria, precio, foto, destacado, disponible, notas`. Mantenerlo en JSON/planilla para carga y mantenimiento.
3. Construir listado + detalle (o card completa con todo lo necesario).
4. Filtros simples (categoría, precio, disponibilidad) y búsqueda por texto.
5. CTA por producto: WhatsApp con mensaje pre-cargado *“Hola, consulto por [producto] [precio]”*.
6. Carga inicial limitada acordada por escrito (p. ej. hasta 30 productos); el resto se agrega aparte.
7. Implementar la misma estructura base y SEO del §4.1; `ItemList`/`Product` en JSON-LD si aporta.
8. Definir el flujo de actualización con el cliente (planilla → publicación, o panel simple).

**Plazo orientativo:** 1–2 semanas (más carga inicial).

### 4.4 Paquete 3 — Turnos o reservas

**Diagnóstico específico**
- ¿Cómo agenda hoy? ¿Cuántos mensajes para cerrar un turno?
- Horarios de atención, duración de cada servicio, días sin agenda.
- ¿Quién administra la agenda? ¿Usa algún sistema que se pueda integrar?

**Pasos de implementación**
1. Mapear servicios: nombre, duración, precio (si aplica), profesional/área.
2. Elegir mecanismo de turno (en orden de complejidad):
   - **a)** CTA WhatsApp con mensaje pre-cargado de turno (mínimo viable, sin backend).
   - **b)** Formulario de solicitud de turno + confirmación por WhatsApp.
   - **c)** Agenda integrada / embed (Calendly, Google Calendar o sistema propio) con confirmación.
3. Flujo de confirmación y recordatorio (WhatsApp o email) definido con el cliente.
4. Reglas: anticipación mínima, política de cancelación, cupos.
5. Pantallas: servicios + precios, horarios disponibles, “Pedir turno” visible siempre.
6. Base SEO local del §4.1 (fundamental: “turno de [servicio] en [zona]”).
7. Capacitación al personal para responder/completar turnos.

**Plazo orientativo:** 1–2 semanas según integración.

### 4.5 Paquete 4 — Tienda online

**Diagnóstico específico (gate de entrada)**
- ¿Catálogo ordenado con precios y fotos?
- ¿Stock confiable y forma de actualizarlo?
- ¿Cómo cobra hoy? (transferencia, Mercado Pago, efectivo contra entrega)
- ¿Qué zona entrega, en cuánto tiempo, costo de envío?
- ¿Cómo gestiona pedidos, cambios y devoluciones hoy?
- Si algo de lo anterior falla → **no arrancar**; resolver primero (posible paquete 2).

**Pasos de implementación**
1. **Etapa A — Catálogo y front:** estructura del paquete 2 + fichas de producto completas (variedad, medidas, stock).
2. **Etapa B — Carrito y checkout:** carrito persistente, datos de compra, método de pago (Mercado Pago / transferencia), costos de envío o retiro en local.
3. **Etapa C — Pedidos y stock:** panel de administración básico (ver/crear/editar pedidos, marcar estado, ajustar stock), notificación de nuevo pedido.
4. **Etapa D — Operación:** política de envíos y devoluciones publicada, guía de uso para el comercio, copias de seguridad.
5. Seguridad: HTTPS, dependencias actualizadas, no exponer claves en el front, validación de datos.
6. SEO de productos + `Product`/`Offer` en JSON-LD.
7. Capacitación: carga de productos, gestión de pedidos, respuestas tipo.

**Plazo orientativo:** por etapas, 3–6 semanas en total, con entregas parciales y pagos por etapa.

---

## 5. Checklist de QA previo a publicar

- [ ] Se ve bien en celular (360–430 px) y en desktop.
- [ ] WhatsApp funciona con mensaje pre-cargado, probado en Android e iPhone.
- [ ] Horarios, dirección, teléfono y email correctos y visibles.
- [ ] Mapa carga y abre en la app de mapas.
- [ ] Todos los enlaces internos responden (sin 404).
- [ ] Imágenes con `alt`, comprimidas, sin desbordes de layout.
- [ ] `<title>` y `meta description` únicos; H1 único.
- [ ] JSON-LD válido (prueba con Google Rich Results Test).
- [ ] `robots.txt` y `sitemap.xml` publicados.
- [ ] HTTPS activo y dominio apuntando bien.
- [ ] Analítica / Search Console verificados (si aplica).
- [ ] Formularios: llega el aviso al cliente.
- [ ] Contenido sin placeholders ("lorem", "Mi nombre o negocio").
- [ ] Texto legal: datos del titular si el comercio lo requiere.

---

## 6. Entrega y postventa

**Al entregar:**
1. Accesos: dominio, hosting, repositorio, herramientas (todo a nombre del cliente).
2. Capacitación corta (15–30 min): qué puede cambiar él (horarios, precios, fotos) y qué se pide por WhatsApp.
3. Pedir **reseña en Google** y recomendación breve por WhatsApp.
4. Documentar el antes/después (capturas) para usarlo como prueba social.

**Plan mensual sugerido:**
- Actualización de horarios, precios y promociones.
- Cambios menores de contenido y nuevas fotos.
- Copias de seguridad y monitoreo de caídas.
- Reporte simple: visitas, clics a WhatsApp, consultas.
- Soporte por WhatsApp con respuesta prioritaria.

**Regla de cartera:** preferir muchos sitios chicos con mantenimiento mensual antes que depender de una venta grande.

---

## 7. Errores a evitar

- Vender "una página moderna" sin relacionarla con consultas, turnos, ventas o reputación.
- Enviar presupuesto sin haber entendido el negocio.
- Hablar de herramientas (WordPress, React, hosting) antes que de resultados.
- Cobrar barato sin delimitar alcance → cambios infinitos.
- Prometer "primero en Google" o resultados garantizados.
- Vender tienda online a un comercio con catálogo/stock/pagos desordenados.
- No hacer seguimiento: la venta suele llegar en el segundo o tercer contacto.

---

## 8. Plantillas de contacto

**WhatsApp (primer contacto, personalizar siempre):**

> Hola, ¿cómo estás? Soy Germán, desarrollador de Burzaco. Estoy ayudando a comercios de la zona a tener una web simple, rápida y pensada para que los encuentren en Google y consulten directo por WhatsApp.
>
> Vi una oportunidad puntual en su presencia online: *[mencioná algo real: falta de horarios, catálogo, web inexistente, sitio que no funciona bien en celular]*.
>
> Si te parece, te muestro sin compromiso una idea de 10 minutos de cómo podría quedar y qué consultas podría resolver.

**Presencial:**

> "Hola, soy Germán, soy de la zona y trabajo haciendo soluciones web para comercios. No vengo a venderte algo ahora: vi que *[problema específico]* y preparé una idea simple para que la gente encuentre sus servicios/productos y consulte por WhatsApp. ¿Con quién podría hablar cinco minutos en un horario tranquilo?"

**Demos vivas disponibles (townshop):**

| Paquete | Demo pública |
| :-- | :-- |
| Presencia local | https://townshop-one.vercel.app/landing2/ |
| Catálogo que consulta | https://townshop-one.vercel.app/landing-demos/landing-1/ |
| Tienda online | https://townshop-one.vercel.app/landing-demos/landing-3/ |
| Explorador completo | https://townshop-one.vercel.app/ |

---

## 9. Plan de arranque (próximo mes)

Objetivo: **dos casos locales bien resueltos**, no muchos leads.

1. Elegir 2 rubros (p. ej. talleres/repuestos y salud/estética).
2. Relevar 10 negocios por rubro en Google Maps e Instagram.
3. Armada la lista, seleccionar 5 con mayor potencial y hacer el diagnóstico personalizado.
4. Contactar por WhatsApp o visita en horario tranquilo; agendar reunión de 15 minutos.
5. Cerrar, entregar, documentar antes/después, pedir reseña.
6. Usar ese resultado como prueba social para el siguiente comercio.

Propuesta central:

> "Ayudo a comercios de Burzaco a convertir búsquedas y redes sociales en consultas directas por WhatsApp, con una web rápida, clara y lista para que el cliente encuentre lo importante."
