---
name: Limonada Landing
description: Volante de barrio impreso a dos tintas — amarillo fluo y negro sobre papel cálido con grano.
colors:
  ink-yellow: "#F5C518"
  gold-pass: "#D4A800"
  ink-black: "#111111"
  paper: "#F8F1DE"
  paper-deep: "#F0E6C8"
  card-white: "#FFFDF4"
  ink-body: "#3B3629"
  gold-text: "#7A5A06"
  stamp-green: "#0E7A55"
typography:
  # escala óptica del volante: material impreso, cada pieza afina su cuerpo.
  # Enumerada del build shippeado (verdict: ship) — superficies nuevas prefieren
  # los escalones núcleo: 13.5 / 16.5 / 20 y los clamps de display.
  scale:
    micro: "10px"
    stamp: "10.5px"
    tag: "11px"
    caption: "12px"
    captionPlus: "12.5px"
    navlink: "13px"
    label: "13.5px"
    small: "14px"
    smallPlus: "14.5px"
    ui: "15px"
    bodySmall: "15.5px"
    input: "16px"
    body: "16.5px"
    ctaLarge: "17px"
    lead: "18px"
    leadPlus: "19px"
    titleCard: "20px"
    stubNumeral: "32px"
    price: "42px"
    pasoNumeral: "44px"
  display:
    fontFamily: "Poppins, sans-serif"
    fontSize: "clamp(3rem, 8.5vw, 6rem)"
    fontWeight: 800
    lineHeight: 0.95
    letterSpacing: "-0.02em"
  headline:
    fontFamily: "Poppins, sans-serif"
    fontSize: "clamp(2rem, 5vw, 3.4rem)"
    fontWeight: 800
    lineHeight: 0.95
    letterSpacing: "-0.02em"
  closer:
    fontFamily: "Poppins, sans-serif"
    fontSize: "clamp(2.6rem, 7vw, 4.6rem)"
    fontWeight: 800
    lineHeight: 0.95
    letterSpacing: "-0.02em"
  body:
    fontFamily: "Open Sans, sans-serif"
    fontSize: "16.5px"
    fontWeight: 400
    lineHeight: 1.6
  label:
    fontFamily: "Poppins, sans-serif"
    fontSize: "13.5px"
    fontWeight: 700
    letterSpacing: "0.05em"
rounded:
  none: "0"
  bubble: "12px"
  bubble-tail: "3px"
spacing:
  gutter: "24px"
  card: "26px"
  section: "96px"
  section-mobile: "72px"
components:
  button-ticket:
    backgroundColor: "{colors.ink-yellow}"
    textColor: "{colors.ink-black}"
    rounded: "{rounded.none}"
    padding: "15px 30px"
  button-ticket-on-yellow:
    backgroundColor: "{colors.paper}"
    textColor: "{colors.ink-black}"
    rounded: "{rounded.none}"
    padding: "15px 30px"
  button-line:
    backgroundColor: "transparent"
    textColor: "{colors.ink-black}"
    rounded: "{rounded.none}"
    padding: "15px 30px"
  button-line-hover:
    backgroundColor: "{colors.ink-black}"
    textColor: "{colors.paper}"
  card-paper:
    backgroundColor: "{colors.card-white}"
    textColor: "{colors.ink-body}"
    rounded: "{rounded.none}"
    padding: "30px 26px"
  sello-wait:
    backgroundColor: "{colors.ink-yellow}"
    textColor: "{colors.ink-black}"
    rounded: "{rounded.none}"
    padding: "4px 9px"
---

# Design System: Limonada Landing

## Overview

**Creative North Star: "El Volante de Barrio"**

La landing es un volante de barrio impreso a dos tintas en una risograph: tinta amarillo fluo y tinta negra sobre papel cálido con grano visible. Todo lo que aparece en pantalla se comporta como material de imprenta — tickets troquelados, recibos, sellos de goma, puntos líder de lista de precios — nunca como "UI de SaaS". El mundo rechaza explícitamente el hero de screenshot flotante sobre degradado, los glows de color y toda superficie vidriosa o levitante.

La textura es estructural, no decorativa: una capa fija de grano SVG (`fractalNoise`) cubre toda la página, y cada campo de tinta plena (hero, demo, pasos, cierre) lleva un mottle propio en `multiply` (sobre claro) o `screen` (sobre negro) que simula la densidad irregular de la tinta. El desregistro leve — la pasada amarilla corrida 6px/5px bajo el titular negro — es la firma del mundo y aparece solo en titulares display.

**Key Characteristics:**
- Dos tintas + papel: amarillo #F5C518 y negro #111111 sobre crema #F8F1DE, con una pasada dorada #D4A800 de refuerzo.
- Bordes de 2px negros en todo; troquel dashed y puntos líder dotted como divisores.
- Sombras duras offset sin blur (la "sombra de registro"), nunca sombras difusas.
- Esquinas rectas por doctrina; rotaciones leves (±1–3°) en los artefactos de papel.
- Poppins 800 MAYÚSCULAS para display; Open Sans para cuerpo.

## Colors

Paleta de imprenta a dos tintas: dos pigmentos y el papel hacen todo el trabajo; el verde del sello es la única excepción semántica.

### Primary
- **Tinta Amarillo Fluo** (#F5C518): la tinta de pliego. Campos plenos de sección (hero, demo), fondo del botón ticket, pasada de desregistro bajo titulares negros, celda "después" en comparativas.
- **Pasada Dorada** (#D4A800): la segunda pasada de la tinta amarilla, más cargada. Solo decorativa: sombras offset sobre fondo amarillo/negro, puntos líder, tachados, subrayados de nav y footer. Nunca como color de texto.
- **Tinta Negra** (#111111): titulares, bordes de 2px, campos plenos de sección (pasos, cierre), sombra de registro sobre papel.

### Neutral
- **Papel** (#F8F1DE): fondo base del pliego y de superficies sobre tinta.
- **Papel Hundido** (#F0E6C8): texto secundario sobre tinta negra.
- **Papel de Recibo** (#FFFDF4): fondo de los artefactos de papel montados (recibo, tarjetas de tarifa) — un blanco apenas más limpio que el pliego, para que la pieza se lea "encima".
- **Tinta de Cuerpo** (#3B3629): color de texto corrido sobre claros; un negro entibiado por el papel.
- **Dorado Legible** (#7A5A06): la versión de la tinta dorada que sí funciona como texto (WCAG) — números de paso, horas de chat, notas y captions pequeñas sobre claros.

### Tertiary
- **Verde Sello** (#0E7A55): exclusivo del sello "Confirmado" en la agenda demo. Único hue fuera de las dos tintas. (Diverge del `#10B981` de marca: el build usa este verde más oscuro por legibilidad de texto pequeño; el build manda.)

### Named Rules
**The Two-Ink Rule.** Todo color en pantalla es papel, amarillo o negro (más la pasada dorada derivada del amarillo). Un tercer hue solo puede existir como tinta de sello semántico, y hoy solo existe el verde #0E7A55.

**The Legible Gold Rule.** #D4A800 (y cualquier dorado saturado) es decorativo: sombras, líneas, tachados. Texto dorado sobre claro usa siempre #7A5A06.

## Typography

**Display Font:** Poppins (sans-serif fallback) — pesos 600/700/800
**Body Font:** Open Sans (sans-serif fallback) — pesos 400/600/700

**Character:** titulares de imprenta barrial — geométricos, pesadísimos, en mayúsculas, apretados casi hasta tocarse — sobre un cuerpo humanista y legible que hace de tipografía "de texto corrido del volante".

### Hierarchy
- **Display** (800, clamp(3rem, 8.5vw, 6rem), lh 0.95, ls -0.02em, UPPERCASE): el titular del hero, máximo 11ch de ancho, con desregistro `.misreg`.
- **Headline** (800, clamp(2rem, 5vw, 3.4rem), lh 0.95, UPPERCASE): títulos de sección (`.sec-title`), máximo 20ch. El cierre escala a clamp(2.6rem, 7vw, 4.6rem).
- **Title** (700–800 Poppins, 14–20px, UPPERCASE): nombres de componentes — funcionalidades, cabezales de tarjeta, h3 de tickets.
- **Body** (400 Open Sans, 16.5px, lh 1.6): texto corrido en #3B3629, máx ~52–58ch. Baja a 15.5px bajo 520px. Los subtítulos de sección van a 18–19px, y sobre tinta amarilla suben a peso 600.
- **Label** (700 Poppins u Open Sans, 10–13.5px, ls 0.05–0.1em, UPPERCASE): nav, sellos, stamps, captions. Los labels chicos sobre claro usan #7A5A06.

### Named Rules
**The Caps Display Rule.** Todo lo que compone en Poppins va en mayúsculas (`text-transform: uppercase`), peso ≥700, interlínea 0.95 en tamaños display. Poppins nunca aparece en minúscula de texto corrido.

**The Misregistration Rule.** El desregistro (`.misreg`: pasada corrida `translate(6px, 5px)` con animación `settle` de 700ms) es exclusivo de titulares display/headline. La pasada corrida es amarilla sobre claro y sobre negro, y papel sobre campo amarillo. Nunca en cuerpo, botones ni labels.

## Layout

Pliego único de ancho contenido: `.container` de máx 1140px con gutter de 24px. Las secciones alternan campos de tinta de borde a borde (amarillo → papel → negro → papel → amarillo → papel → negro) separados siempre por reglas de 2px negras; el ritmo vertical es 96px arriba/abajo por sección (72px bajo 860px).

Las grillas son de imprenta: 4 columnas para tickets y pasos, 2 columnas para funcionalidades y comparativas, 3 para tarifas. Breakpoints observados: 1024px (gaps se achican), 860px (grillas 4→2, columnas apiladas, nav pasa a fila propia con regla dashed), 520px (todo a 1 columna, tickets apilados con troquel horizontal). Gaps grandes entre piezas de papel montadas (40–72px); dentro de una pieza el padding ronda 22–30px.

## Elevation & Depth

Cero sombras difusas. La profundidad es la de una mesa de imprenta: piezas de papel apoyadas con una sombra dura de registro — offset sólido, sin blur, del color de la tinta de abajo — y rotaciones leves (±0.6–1.2° en tarjetas, ±3° en sellos y stamps) que dicen "pegado a mano". El grano y el mottle dan la textura; el borde de 2px da el recorte.

### Shadow Vocabulary
- **Registro base** (`box-shadow: 5px 5px 0 #111111` — token `--shadow-reg`): reposo de botones ticket y piezas de papel sobre fondo claro/amarillo.
- **Registro hover** (`8px 8px 0 #111111`): el elemento se despega (`translate(-2px,-2px)`); en active se aplasta a `1px 1px 0` con `translate(3px,3px)`.
- **Registro dorado** (`5px 5px 0 #D4A800`, hover `8–9px`): botones sobre campo negro, donde la sombra negra no se vería.
- **Registro de tarjeta demo** (`7px 7px 0 #D4A800`): la agenda montada sobre campo amarillo.

### Named Rules
**The Registration Shadow Rule.** Toda sombra es un offset sólido sin blur, negra sobre claro y dorada (#D4A800) sobre negro o amarillo. Un `box-shadow` con radio de blur no existe en este mundo.

## Shapes

Esquinas rectas por doctrina: `border-radius: 0` en botones, tarjetas, tickets, sellos y stamps. Las dos únicas excepciones son materiales del mundo: las burbujas de chat del recibo (12px asimétrico, 3px en la esquina de cola) y las perforaciones circulares del troquel (círculos de 14px). El borde universal es 2px sólido #111111; el troquel y los cortes son 2px **dashed**; los puntos líder y divisores de lista son 2px **dotted** (a menudo en #D4A800). El corte inferior del recibo es un zigzag de `linear-gradient` dentado. Los ornamentos son SVG inline de imprenta (dial de reloj, círculo de semitono con `pattern` de puntos) — nunca iconos de glifo.

## Components

### Buttons (ticket)
- **Shape:** rectángulo recto (0 radius), borde 2px sólido #111111.
- **Primary (`.btn-ink`):** fondo amarillo #F5C518 (papel #F8F1DE cuando está sobre campo amarillo o en tarifa Pro), texto negro, Poppins 700 15px UPPERCASE, padding 15px 30px, sombra de registro `5px 5px 0`.
- **Hover / Active:** hover despega (`translate(-2px,-2px)` + sombra 8px); active aplasta (`translate(3px,3px)` + sombra 1px). Transición 200ms `cubic-bezier(.22,.9,.35,1)` (token `--t`).
- **Secondary (`.btn-line`):** transparente con borde negro, sin sombra; hover invierte a fondo negro / texto papel.

### Chips (sellos de goma)
- **Style (`.sello`):** Poppins 700 10px UPPERCASE ls 0.09em, borde 1.5px `currentColor`, rotación -3°, sin radius.
- **States:** `ok` verde #0E7A55; `wait` texto negro sobre amarillo con borde negro; `done` tinta de cuerpo al 60% de opacidad.

### Cards / Containers (piezas de papel)
- **Corner Style:** recto (0).
- **Background:** #FFFDF4 (recibo, tarifas) o #F8F1DE (agenda); la tarifa destacada va en amarillo pleno.
- **Shadow Strategy:** sombra de registro (ver Elevation); la pieza destacada la lleva en reposo, las demás la ganan en hover.
- **Border:** 2px sólido #111111 siempre.
- **Internal Padding:** 26–30px.
- **Rotación:** la pieza "montada" rota levemente (-1.2° recibo, 1° agenda, -0.6° tarifa Pro).

### Navigation
- **Masthead:** borde inferior 2px negro sobre papel; logo Poppins 800 20px; links Poppins 600 13.5px UPPERCASE ls 0.05em con subrayado 2px transparente que pasa a #D4A800 en hover. En móvil la nav baja a fila propia sobre regla dashed. Footer: links con subrayado 2px dorado permanente, hover con fondo amarillo.

### Ticket Stub Strip (signature)
La tira de 4 tickets troquelados del hero: grilla sin gap con borde 2px, divisores internos 2px dashed y perforaciones circulares de 14px en las uniones (mitad color del campo de arriba, mitad papel). Número de paso Poppins 800 32px en #7A5A06; el último ticket se invierte a tinta negra plena. Hover: `translateY(-4px)`. Bajo 860px pierde perforaciones y pasa a 2×2; bajo 520px se apila con troquel horizontal.

### Focus
`:focus-visible` universal: outline 3px sólido #111111, offset 3px. `prefers-reduced-motion` anula animaciones y fija el desregistro en su posición final.

## Do's and Don'ts

### Do:
- **Do** encerrar toda pieza en borde 2px sólido #111111 y separar secciones con reglas de 2px.
- **Do** usar la sombra de registro (offset sólido, sin blur; negra sobre claro, #D4A800 sobre oscuro) como única fuente de profundidad.
- **Do** rotar levemente (±0.6–3°) las piezas de papel montadas y los sellos.
- **Do** componer display en Poppins 800 UPPERCASE, lh 0.95, y reservar `.misreg` para titulares.
- **Do** usar dashed para troquel/cortes y dotted para puntos líder y divisores de lista.
- **Do** dibujar ornamentos como SVG inline de lenguaje de imprenta (semitonos, diales, círculos de tinta).

### Don't:
- **Don't** usar gradientes de color, glows, sombras difusas ni superficies vidriosas — el mundo rechaza el hero SaaS de screenshot flotante.
- **Don't** redondear esquinas de botones, tarjetas, tickets o sellos; el radius solo existe en burbujas de chat (12px) y perforaciones.
- **Don't** usar #D4A800 ni ningún dorado saturado como color de texto; texto dorado es #7A5A06.
- **Don't** introducir hues fuera de las dos tintas salvo el verde de sello #0E7A55, y solo con rol semántico.
- **Don't** usar iconos de glifo, icon fonts ni emojis como íconos; la iconografía del mundo es tipográfica y de SVG de imprenta.
- **Don't** animar más allá del `settle` del desregistro y las transiciones de 200ms de despegue/aplastado; siempre respetando `prefers-reduced-motion`.
