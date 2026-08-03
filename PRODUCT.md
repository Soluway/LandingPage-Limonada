# Product

<!-- impeccable:product-schema 1 -->

## Platform

web

## Users

Dueños y encargados de negocios que trabajan con turnos en Argentina: estética (peluquerías, barberías, salones de uñas/belleza), salud (consultorios, kinesiología) y servicios profesionales. Situación típica: gestionan la agenda a mano — WhatsApp, cuaderno o Excel — y pierden tiempo coordinando, sufren ausencias y no tienen visibilidad del negocio. No son técnicos; evalúan desde el celular.

## Product Purpose

Limonada es un SaaS de gestión de turnos y agenda. Reemplaza la coordinación manual por WhatsApp con una página pública de reservas (el cliente final agenda solo), agenda centralizada, recordatorios automáticos y visión del negocio (múltiples profesionales/sucursales, comisiones). Éxito: que el dueño deje de coordinar turnos a mano y los clientes finales reserven solos.

## Positioning

Simplicidad extrema. Configurado en minutos, sin curva de aprendizaje y sin features que sobran — contra suites recargadas (AgendaPro, Booksy) y contra el statu quo (WhatsApp + cuaderno). La landing vende exactamente eso: lo simple que es empezar y usar.

## Operating Context

- App del producto: https://app.limonada.online (CTA de la landing apunta ahí).
- El cliente final del negocio reserva desde el celular vía un link público que el negocio comparte (WhatsApp/Instagram).
- Mercado argentino: voseo, precios en pesos. Planes actuales (confirmados por Tiziano 2026-08-02, pisan cualquier valor anterior del repo): Starter gratis, Pro $44.500/mes, Business $93.900/mes.
- Contacto/soporte: soluway.group@gmail.com — es la ÚNICA casilla real que existe; no hay mail propio de Limonada todavía.

## Capabilities and Constraints

- Funcionalidad confirmada (según producto/copy existente): página pública de reservas por link, agenda en tiempo real, recordatorios automáticos, múltiples profesionales y sucursales, reportes/comisiones.
- NO existen aún en la app (confirmado por Tiziano 2026-08-02): pagos con MercadoPago, sincronización con Google Calendar, notificaciones por WhatsApp, exportación PDF/CSV, roles diferenciados de equipo. Son roadmap — NO publicarlos como claims en ninguna pieza hasta que Tiziano confirme que shippearon. Las notificaciones existentes son por email.
- Landing: archivo estático único (index.html) servido por GitHub Pages con dominio custom (CNAME). Sin build step. Todo inline.
- Repo git: nunca pushear a `origin`; solo al fork `ziano`.

## Brand Commitments

- Paleta REAL (confirmada por Tiziano 2026-08-02): amarillo limón `#F5C518`, primary dark `#D4A800`, negro tinta `#111111`, fondos crema `#FFFDF0`/`#FFFBEB`, border `#F0E68C`, gold texto accesible `#966D09` (el histórico `#B8860B` falla WCAG como texto), success `#10B981`. Tokens completos en `../../AplicacionLimonada/design-system/limonada/MASTER.md`.
- Logo oficial: `Gemini_Generated_Image_4uuu84uuu84uuu84-Photoroom.png` (raíz del repo). No inventar logos.
- Tipografías: Poppins (headings) + Open Sans (body). Open Sans tiene excepción registrada en `.impeccable/config.json`.
- Voz: voseo argentino, directo, sin jerga técnica ni palabras infladas.
- Requisito explícito del dueño: que el diseño NO parezca generado por IA (sin glows de color, side-tabs, grids decorativos genéricos, emojis como íconos).

## Evidence on Hand

- **Pre-lanzamiento: no hay usuarios reales todavía.** No existen testimonios, logos de clientes, ni métricas de resultados publicables. NADA de eso se fabrica: ni "X% menos ausencias", ni cantidades de negocios, ni citas. Los testimonios con nombre que tenía la landing vieja se eliminaron por no verificables (2026-08-02).
- La evidencia disponible es el producto mismo: la demo/representación de la agenda y el flujo de reserva.

## Product Principles

1. La simplicidad es el producto: si la landing se siente complicada, contradice la promesa.
2. El producto se muestra, no se afirma: demo antes que claims (no hay métricas reales que citar).
3. Mobile primero: el dueño evalúa desde el celular, igual que reserva su cliente.
4. Honestidad comercial: cero prueba social inventada hasta tener usuarios reales.
5. Argentina no es un detalle: voseo, pesos, WhatsApp como contexto cultural.
