---
version: alpha
name: Sistema de Diseño Karina Gutiérrez Rangel v2
description: "Sistema de diseño en evolución: scroll editorial de láminas de color sólido, estética orgánica y amigable, larga respiración entre bloques, magentas de marca sobre base cálida."
colors:
  primary: "#B2255A"            # Magenta de marca: CTA, acentos, títulos e identidad
  secondary: "#AE5362"          # Magenta claro: énfasis puntual
  link: "#0088CC"               # Azul cielo: enlaces e interactivos secundarios
  button-secondary: "#AAC5B4"   # Gris azul: fondo de botones secundarios y fantasma
  on-surface: "#451A14"         # Café: texto principal y mayor contraste
  text-tertiary: "#808080"      # Gris medio: texto terciario y deshabilitados
  surface: "#F7F4D5"            # Blanco de marca: fondo principal
  surface-alt: "#EFEAD3"        # REVISAR: crema más profunda para testimonios y bloques diferenciados
  overlay: "rgba(178,37,90,0.45)" # REVISAR: bloque sólido semitransparente en tono de marca (magenta); nunca negro difuso
typography:
  display:                      # Título display, el más grande
    fontFamily: PerecScripte2
    fontSize: 40px
    fontWeight: 400
    lineHeight: 48px
  h1:
    fontFamily: Neue Haas Grotesk Display Pro
    fontSize: 40px
    fontWeight: 700
    lineHeight: 48px            # REVISAR: interlineado asumido
  h2:
    fontFamily: Neue Haas Grotesk Display Pro
    fontSize: 40px
    fontWeight: 400             # "roman", reservada a los títulos más importantes
    lineHeight: 48px            # REVISAR: interlineado asumido
  h3:                           # Subsecciones
    fontFamily: Neue Haas Grotesk Display Pro
    fontSize: 16px
    fontWeight: 700
    lineHeight: 24px            # REVISAR: interlineado asumido
  body:
    fontFamily: Neue Haas Grotesk Display Pro
    fontSize: 20px
    fontWeight: 400
    lineHeight: 30px
  list-item:
    fontFamily: Neue Haas Grotesk Display Pro
    fontSize: 20px
    fontWeight: 500             # Versión "medium"
    lineHeight: 30px            # REVISAR: interlineado asumido (igual al cuerpo)
  small:
    fontFamily: Neue Haas Grotesk Display Pro
    fontSize: 16px
    fontWeight: 400
    lineHeight: 24px            # REVISAR: interlineado asumido
  label-button:
    fontFamily: PerecScripte2
    fontSize: 19.216px
    fontWeight: 400
    lineHeight: 24px            # REVISAR: interlineado asumido
  link:
    fontFamily: Neue Haas Grotesk Display Pro
    fontSize: 20px
    fontWeight: 400
    lineHeight: 30px            # REVISAR: interlineado asumido (igual al cuerpo)
spacing:
  base: 8px                     # Unidad base de espaciado interno de componentes
  xs: 4px                       # REVISAR: medio paso de la base
  sm: 8px
  md: 16px                      # REVISAR: nivel asumido (múltiplo de la base)
  lg: 24px                      # REVISAR: nivel asumido
  xl: 32px                      # REVISAR: nivel asumido
  xxl: 64px                     # Múltiplos de 64px: separación entre láminas (confirmado por el documento)
  gutter: 24px                  # REVISAR: separación entre columnas de la rejilla
  section: 64px                 # Márgenes amplios entre secciones: múltiplos de 64px (confirmado)
  content-max: 1280px           # Ancho máximo de contenido
  grid-columns: "12"            # Rejilla en escritorio; bloques de texto 5-6 columnas centradas o a un lado
  grid-columns-tablet: "8"      # Rejilla en tableta
  grid-columns-mobile: "1"      # Rejilla en móvil; el producto va siempre primero
rounded:
  soft: 16px                    # Radio base de esquinas suaves en tarjetas, botones e imágenes
  soft-lg: 24px                 # Radio mayor para tarjetas e imágenes grandes (rango 16-24px)
  pill: 999px                   # Píldora completa para CTAs centrales y botones principales
components:
  button-primary:
    backgroundColor: "{colors.primary}"
    textColor: "{colors.surface}"
    typography: "{typography.label-button}"
    rounded: "{rounded.pill}"
    padding: 16px               # REVISAR: padding asumido
    height: 52px                # REVISAR: altura asumida
  button-primary-hover:
    backgroundColor: "{colors.surface}"   # Hover: invierte contraste (fondo ↔ texto)
    textColor: "{colors.primary}"
  button-secondary:
    backgroundColor: "{colors.button-secondary}"
    textColor: "{colors.on-surface}"
    typography: "{typography.label-button}"
    rounded: "{rounded.soft}"
    padding: 16px               # REVISAR: padding asumido
    height: 48px                # REVISAR: altura asumida
  link:
    textColor: "{colors.link}"
    typography: "{typography.link}"
    underline: "solo en hover, nunca en reposo"
  card:
    backgroundColor: "{colors.surface}"
    textColor: "{colors.on-surface}"
    rounded: "{rounded.soft}"
    icon: "un solo ícono o imagen de acento por tarjeta"
    maxLines: "3-4 líneas de texto corto"
  testimonial:
    backgroundColor: "{colors.surface-alt}"
    textColor: "{colors.on-surface}"
    rounded: "{rounded.soft}"         # (o {rounded.soft-lg} para tarjetas grandes)
    avatar: "foto circular pequeña (48px)"
    content: "nombre, rol/ocupación y cita breve"
  product-floating:
    photo: "recorte sobre fondo transparente o sólido"
    shadow: "0 8px 20px rgba(69,26,20,0.18)"   # REVISAR: sombra suave y realista, solo anclaje físico
    tilt: "centrada o ligeramente inclinada (-6deg) — REVISAR"
    blob: "forma orgánica de color sólido detrás, una sola por sección ({colors.secondary} — REVISAR)"
  icon-benefit:
    shape: "estrella o check"
    color: "{colors.primary}"
    flat: true                     # plano, un solo color, sin relieve ni brillo
---

# Sistema de Diseño

## Overview

Mi sistema evoluciona hacia un **scroll editorial de bloques horizontales completos**: cada sección ocupa la pantalla como una **"lámina" independiente** al estilo de un storytelling de producto, sección por sección. La rejilla es limpia y de mucho aire: **prioriza la respiración entre elementos sobre la densidad de contenido**.

Defiendo el orden y la legibilidad con una filosofía funcional, pero ahora con un tono **más orgánico y amigable**: esquinas suaves, píldoras y acentos decorativos puntuales (blobs y estrellas). El espacio en blanco es protagonista y nunca se llena por llenar: cada sección tiene **un solo mensaje central** y el resto del espacio existe para que ese mensaje respire.

## Colors

La paleta se apoya en un **magenta de marca más vibrante** (#B2255A) y la base cálida de siempre. Regla rectora nueva: **un solo tono sólido por sección; nunca mezcla de dos o más colores dentro del mismo bloque de fondo** (el ritmo cromático se logra cambiando de color entre secciones).

- **Primary ({colors.primary}, #B2255A):** magenta de marca. Botones de acción (CTA), acentos, títulos e identidad. REVISAR: actualizado del rojizo #882435 al magenta #B2255A.
- **Secondary ({colors.secondary}, #AE5362):** variante sutil para énfasis puntual.
- **Link ({colors.link}, #0088CC):** enlaces e interactivos secundarios.
- **Botón secundario/fantasma ({colors.button-secondary}, #AAC5B4):** fondo de botones secundarios y fantasma.
- **Texto principal / on-surface ({colors.on-surface}, #451A14):** texto principal y color de mayor contraste.
- **Texto terciario / deshabilitados ({colors.text-tertiary}, #808080):** texto terciario y deshabilitados. Nunca para cuerpo.
- **Superficie / blanco de marca ({colors.surface}, #F7F4D5):** fondo principal.
- **Superficie alterna ({colors.surface-alt}, #EFEAD3):** REVISAR: crema más profunda propuesta para testimonios y bloques que deben diferenciarse del fondo general sin competir.
- **Overlay ({colors.overlay}, rgba(178,37,90,0.45)):** REVISAR: bloque sólido semitransparente en tono de marca para separar contenido sobre imágenes. Nunca negros difusos ni overlays con transición.

> REVISAR: {colors.link} sobre la superficie cálida tiene contraste ≈ 3.5:1 (bajo AA 4.5:1 para texto normal). Aceptable para interactivos, no para cuerpo.

## Typography

Dos familias con roles claros: **Neue Haas Grotesk Display Pro** como fuente principal —cuerpo, navegación y contenido general— y **PerecScripte2** como secundaria —títulos, botones y énfasis. La versión **roman** de la familia principal (la más gruesa) queda reservada para los títulos más importantes.

- **Display ({typography.display}):** PerecScripte2 a 40px, interlineado 48px. El más grande.
- **H1 ({typography.h1}):** Neue Haas a 40px, peso 700.
- **H2 ({typography.h2}):** Neue Haas roman a 40px.
- **H3 · subsecciones ({typography.h3}):** Neue Haas a 16px, peso 700.
- **Cuerpo ({typography.body}):** Neue Haas a 20px, interlineado 30px.
- **Ítems de lista ({typography.list-item}):** Neue Haas medium a 20px.
- **Texto pequeño ({typography.small}):** Neue Haas a 16px.
- **Etiqueta de botón ({typography.label-button}):** PerecScripte2 a 19.216px.
- **Enlaces ({typography.link}):** Neue Haas a 20px.

La jerarquía siempre se logra con **tamaño, peso y color, nunca con opacidad**. El cuerpo nunca baja de 16px y la versión roman se usa con moderación.

## Layout

El layout es un **scroll editorial de láminas completas**: cada sección es una "página" propia (storytelling de producto) y el usuario las descubre al hacer scroll. La rejilla es limpia y aireada.

- Unidad base de {spacing.base} (8px) para componentes; las secciones grandes se separan con **márgenes amplios en múltiplos de {spacing.section} (64px)** para que cada bloque respire como una página propia.
- Ancho máximo de contenido: {spacing.content-max} (1280px).
- **Escritorio:** rejilla de {spacing.grid-columns} (12) columnas; los bloques de texto suelen ocupar **5–6 columnas centradas o alineadas a un lado**, dejando el resto para producto flotante o ilustración.
- **Tableta:** rejilla de {spacing.grid-columns-tablet} (8) columnas, mismo espíritu de bloques apilables.
- **Móvil:** una sola columna con el **producto siempre primero (arriba)** y el texto de soporte debajo, priorizando el gesto visual sobre la explicación.
- **El espacio en blanco es protagonista:** nunca se llena por llenar; una sola idea central por sección.

Hitos responsivos (mobile-first):

- **Móvil (320–599px):** cada sección ocupa el ancho completo; el producto flotante va primero, luego el título y al final el texto. El blob decorativo se reduce, pero no desaparece.
- **Tableta (600–1023px):** las secciones combinan texto e imagen lado a lado (2 columnas), conservando el orden de lectura de escritorio.
- **Escritorio (1024–1279px):** composición completa: texto y producto flotante en columnas separadas, con el blob orgánico de fondo a tamaño completo.
- **Escritorio amplio (1280px+):** el contenido se mantiene centrado en {spacing.content-max}, pero los fondos de color sólido se extienden a todo el viewport (full-bleed), reforzando la sensación de "láminas" de color que se revelan al navegar.

## Elevation & Depth

El sistema es **plano y sin degradados de ningún tipo**: la profundidad se logra únicamente por **superposición de capas sólidas y sombra mínima**, nunca por transición de color. Cada fondo es **un solo tono sólido por sección** (nunca mezclas de dos o más colores en el mismo bloque).

- **Producto flotante:** las fotografías de producto (cápsulas, empaques) se recortan sobre fondo transparente o sólido y flotan con una **sombra suave y realista** (propuesta `0 8px 20px rgba(69,26,20,0.18)` — REVISAR), únicamente como **anclaje físico**, nunca decorativa ni exagerada.
- **Íconos:** estrellas y checks son ilustraciones **planas de un solo color**, sin relieve ni brillo simulado.
- **Sobre imágenes:** se usan **bloques de color sólido semitransparente** del sistema (ver {colors.overlay}) — nunca negros difusos ni overlays con transición.
- Se descarta por completo el lenguaje de **neumorfismo, glassmorphism y blur decorativo**.

## Shapes

Las esquinas son **suaves y consistentes ({rounded.soft} 16px – {rounded.soft-lg} 24px)** en tarjetas, botones e imágenes, reforzando el carácter orgánico y amigable de la marca. **Nunca esquinas rectas (0px)**: se sentirían demasiado técnicas para este tono.

- **Píldora completa ({rounded.pill}, 999px):** los botones principales la usan cuando actúan como **llamada a la acción central**.
- **Blobs orgánicos:** formas tipo blob permitidas como **fondo decorativo** detrás de producto — **una sola por sección**.
- **Estrellas/destellos:** acento de marca recurrente en íconos; nunca más de un elemento orgánico decorativo por sección.

## Components

- **Botones:** el principal {components.button-primary} es en **píldora completa ({rounded.pill})**, fondo {colors.primary} y texto en alto contraste ({colors.surface}). Tipografía **bold, sin sutileza**. El hover **invierte el contraste** (fondo ↔ texto) o **oscurece levemente el tono** sólido ({components.button-primary-hover}); nunca degradado. Los secundarios ({components.button-secondary}) usan radio suave {rounded.soft}.
- **Enlaces ({components.link}):** color {colors.link}, subrayado **solo en hover**, nunca en reposo.
- **Bloques/tarjetas ({components.card}):** fondo plano, esquinas suaves {rounded.soft}, usadas para agrupar beneficios, ingredientes o testimonios. Cada tarjeta tiene **un solo ícono o imagen de acento y texto corto** — nunca más de 3–4 líneas.
- **Producto flotante ({components.product-floating}):** el componente distintivo del sistema. Fotografía de producto recortada, centrada o ligeramente inclinada, con **sombra suave de anclaje**, sobre un **blob orgánico de color sólido** a modo de fondo decorativo.
- **Íconos de beneficio ({components.icon-benefit}):** estrellas o checks planos de un solo color, en listas cortas (signos, beneficios, ingredientes), siempre acompañados de texto breve, **nunca solos**.
- **Testimonios ({components.testimonial}):** tarjeta con **foto circular pequeña**, nombre, rol/ocupación y una cita breve; el fondo sólido se diferencia del fondo de la sección para que destaquen sin competir ({colors.surface-alt}).

## Do's and Don'ts

**Sí**

- Usa fondos sólidos de un solo color por sección; cambia de color entre secciones para marcar el ritmo del scroll.
- Deja mucho aire alrededor de cada bloque de texto y producto.
- Usa sombra suave únicamente como anclaje físico de producto flotante.
- Aplica esquinas suaves de forma consistente en todos los componentes.
- Usa un solo elemento orgánico (blob, estrella) como acento decorativo por sección.

**No**

- No uses degradados en ningún fondo, botón, ícono o texto.
- No mezcles dos colores sólidos dentro del mismo bloque de fondo.
- No uses sombras duras ni difusas exageradas.
- No apliques esquinas rectas (0px): rompe el tono orgánico de la marca.
- No compitas con más de un elemento decorativo orgánico por sección.