---
version: alpha
name: Sistema de Design Karina Gutiérrez Rangel
description: "Sistema de diseño de la marca: estética de collage con intervención fotográfica, puente entre orden estructural y gesto expresivo, apoyado en magentas rojizos, café y una base cálida casi blanca."
colors:
  primary: "#882435"            # Magenta rojizo: botones de acción (CTA), acentos, títulos e identidad de marca
  secondary: "#AE5362"          # Magenta claro: énfasis puntual
  link: "#0088CC"               # Azul cielo: enlaces e interactivos secundarios
  button-secondary: "#AAC5B4"   # Gris azul: fondo de botones secundarios y fantasma
  on-surface: "#451A14"         # Café: texto principal y color de mayor contraste
  text-tertiary: "#808080"      # Gris medio: texto terciario y elementos deshabilitados
  surface: "#F7F4D5"            # Blanco cáscara (el "blanco" de la marca): fondo principal
  overlay: "rgba(136,36,53,0.45)" # REVISAR: bloque semitransparente en tono de marca (magenta); nunca negro o gris neutro difuso
typography:
  display:                      # Título display, el más grande
    fontFamily: PerecScripte2
    fontSize: 40px
    fontWeight: 400             # Peso de la script; peso dado por la forma de la fuente
    lineHeight: 48px
  h1:
    fontFamily: Neue Haas Grotesk Display Pro
    fontSize: 40px
    fontWeight: 700
    lineHeight: 48px            # REVISAR: interlineado asumido
  h2:
    fontFamily: Neue Haas Grotesk Display Pro
    fontSize: 40px
    fontWeight: 400             # "roman", la versión más gruesa de la familia
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
rounded:
  none: 0px                     # Esquinas rectas por defecto, lo estructural
  full: 50%                     # Círculos perfectos: marcos de imagen, avatares, puntos de acento
spacing:
  base: 8px                     # Unidad base de espaciado interno de componentes
  xs: 4px                       # REVISAR: medio paso de la base
  sm: 8px
  md: 16px                      # REVISAR: nivel asumido (múltiplo de la base)
  lg: 24px                      # REVISAR: nivel asumido
  xl: 32px                      # REVISAR: nivel asumido
  xxl: 64px                     # REVISAR: nivel asumido
  gutter: 24px                  # REVISAR: separación entre columnas de la rejilla
  section: 64px                 # REVISAR: ritmo vertical entre bloques
  content-max: 1280px           # Ancho máximo de contenido
  grid-columns: "12"            # Rejilla en escritorio
  grid-columns-tablet: "8"      # Rejilla en tableta
  grid-columns-mobile: "1"      # Rejilla en móvil
components:
  button-primary:
    backgroundColor: "{colors.primary}"
    textColor: "{colors.surface}"   # El "blanco" de la marca (#F7F4D5) o {colors.on-surface} según el fondo
    typography: "{typography.label-button}"
    rounded: "{rounded.none}"
    padding: 16px               # REVISAR: padding asumido (múltiplo de la base)
    height: 48px                # REVISAR: altura asumida
  button-primary-hover:
    backgroundColor: "{colors.surface}"   # Hover: invierte contraste (fondo ↔ texto)
    textColor: "{colors.primary}"
  button-secondary:
    backgroundColor: "{colors.button-secondary}"
    textColor: "{colors.on-surface}"   # REVISAR: color de texto propuesto (no está en el documento)
    typography: "{typography.label-button}"
    rounded: "{rounded.none}"
    padding: 16px               # REVISAR: padding asumido
    height: 48px                # REVISAR: altura asumida
  link:
    textColor: "{colors.link}"
    typography: "{typography.link}"
    underline: "solo en hover, nunca en reposo"
  card:                         # Tarjeta de bloque plano; puede ser blanca o café
    backgroundColor: "{colors.surface}"   # o {colors.on-surface} para tarjetas de color café
    textColor: "{colors.on-surface}"
    rounded: "{rounded.none}"
    spacing-internal: "múltiplos de {spacing.base}"
    image: "puede sangrar un borde como intervención controlada"
  headline:                     # Tipografía como componente, sustituye a la ilustración
    typography: "{typography.display}"
    width: "ancho completo del bloque"
  photo-intervention:           # Componente distintivo del sistema
    treatment: "duotono {colors.primary} / {colors.on-surface}"
    grid: "rompe parcialmente la rejilla (bleed)"
    accent: "pequeño elemento orgánico (línea, recorte o forma) que señala el momento de intervenir"
---

# Sistema de Diseño

## Overview

Mi marca encarna una estética de **collage, con intervención de la fotografía**, centrada en la exploración de la imaginación. Tiendo un puente entre la experiencia funcional —que debe seguir siendo legible, sin saturación— y el gesto expresivo. Se apoya en colores que hacen contraste entre sí pero son sutiles, y transmite **dinamismo, creatividad y pasión en las texturas**.

Priorizo el orden y la legibilidad con una filosofía funcional: layouts con pausas de espacio y tipografía con propósito. El sistema está pensado para la exploración de creativos y desarrolladores; hay un **equilibrio entre el aire y la saturación** de elementos. En una frase: un conjunto de elementos pero con orden y espacio, con componentes con ornamentación.

## Colors

La paleta se construye sobre dos magentas de marca y una base cálida de alto contraste. Los colores contrastan entre sí pero se mantienen sutiles.

- **Primary ({colors.primary}, #882435):** el color principal. Botones de acción (CTA), acentos, títulos e identidad de marca.
- **Secondary ({colors.secondary}, #AE5362):** variante sutil del magenta para énfasis puntual.
- **Link ({colors.link}, #0088CC):** el color de los enlaces y de los elementos interactivos secundarios.
- **Botón secundario/fantasma ({colors.button-secondary}, #AAC5B4):** fondo de los botones secundarios y fantasma.
- **Texto principal / on-surface ({colors.on-surface}, #451A14):** el texto principal y el color de mayor contraste.
- **Texto terciario / deshabilitados ({colors.text-tertiary}, #808080):** texto terciario y elementos deshabilitados. No se usa para texto de cuerpo.
- **Superficie / blanco ({colors.surface}, #F7F4D5):** el "blanco" de la marca, el fondo principal.
- **Overlay ({colors.overlay}):** REVISAR: bloque semitransparente en tono de marca propuesto (magenta). La regla del documento: los overlays usan tonos de marca, nunca negro o gris neutro difuso.

> REVISAR: {colors.link} sobre la superficie cálida tiene contraste ≈ 3.5:1, por debajo de AA 4.5:1 para texto normal. Aceptable para interactivos, pero conviene revisarlo si se usa en cuerpo.

## Typography

Dos familias con roles claros: **Neue Haas Grotesk Display Pro** como fuente principal —cuerpo de texto, navegación y contenido general— y **PerecScripte2** como secundaria —títulos, botones y énfasis. La versión **roman** de Neue Haas Grotesk Display Pro (la más gruesa) queda reservada para los títulos más importantes.

- **Display ({typography.display}):** PerecScripte2 a 40px, interlineado 48px. El título más grande.
- **H1 ({typography.h1}):** Neue Haas Grotesk Display Pro a 40px, peso 700.
- **H2 ({typography.h2}):** Neue Haas Grotesk Display Pro roman a 40px.
- **H3 · subsecciones ({typography.h3}):** Neue Haas Grotesk Display Pro a 16px, peso 700.
- **Cuerpo ({typography.body}):** Neue Haas Grotesk Display Pro a 20px, interlineado 30px.
- **Ítems de lista ({typography.list-item}):** Neue Haas Grotesk Display Pro medium a 20px.
- **Texto pequeño ({typography.small}):** Neue Haas Grotesk Display Pro a 16px.
- **Etiqueta de botón ({typography.label-button}):** PerecScripte2 a 19.216px.
- **Enlaces ({typography.link}):** Neue Haas Grotesk Display Pro a 20px.

La jerarquía siempre se logra con **tamaño, peso y color, nunca con opacidad**. El cuerpo nunca baja de 16px, y la versión roman de Neue Haas Grotesk Display Pro se usa con moderación, solo para los titulares más importantes.

## Layout

El layout se construye como una **rejilla estructural intervenida**: la base es ordenada y predecible, pero permito que ciertos elementos —principalmente fotográficos— rompan esa retícula como una intervención intencional, nunca accidental. Es el puente entre la exploración de collage y la funcionalidad: **la estructura nunca se pierde, pero tampoco se vuelve rígida**.

- Espaciado interno de componentes sobre la unidad base de {spacing.base} (8px); el espacio interno de las tarjetas se calcula en múltiplos de la base para evitar saturación.
- El ancho máximo de contenido es {spacing.content-max} (1280px).
- En escritorio: rejilla de {spacing.grid-columns} (12) columnas; la mayoría de los bloques respeta la columna, pero las imágenes de intervención sangran fuera de ella (bleed parcial) para marcar el momento de "ruptura" dentro de la narrativa **observar → intervenir → resolver**.
- En tableta: rejilla de {spacing.grid-columns-tablet} (8) columnas, conservando el mismo principio de orden con puntos de fuga fotográficos.
- En móvil: colapso a una sola columna ({spacing.grid-columns-mobile}); la intervención fotográfica deja de sangrar y se contiene dentro del margen, priorizando la legibilidad sobre el gesto expresivo.
- **El espacio en blanco no es "aire vacío":** es la pausa que hace legible el contraste entre orden y textura; su presencia se calcula tanto como cualquier otro elemento.

El sistema es **mobile-first** y prioriza la legibilidad funcional sobre el gesto expresivo en pantallas pequeñas. Hitos responsivos:

- **Móvil (320–599px):** rejilla de una columna; la intervención fotográfica se contiene dentro del margen (sin sangrado), manteniendo el orden como prioridad.
- **Tableta (600–1023px):** rejilla de 8 columnas que permite reintroducir sangrados parciales controlados en las imágenes de intervención.
- **Escritorio (1024–1279px):** rejilla completa de 12 columnas con el sistema de ruptura narrativa (observar → intervenir → resolver) totalmente visible.
- **Escritorio amplio (1280px+):** el contenido se mantiene centrado en el máximo de {spacing.content-max}, pero las intervenciones fotográficas pueden sangrar hasta el viewport completo, reforzando el momento de "intervención" como el punto de mayor impacto visual de la sección.

## Elevation & Depth

El sistema **evita el volumen simulado**: sin sombras difusas, degradados ni neumorfismo. La sensación de profundidad se logra por **superposición**: capas de fotografía intervenida sobre bloques de color plano, generando contraste duro entre la superficie fotográfica y la superficie tipográfica/gráfica.

- Las fotografías, cuando actúan como "intervención", se recortan o se tratan con **duotono usando la paleta de marca** (magenta {colors.primary} / café {colors.on-surface}); nunca en color natural sin intervenir. Esto refuerza que la imagen fue "tocada" por el sistema, no solo insertada.
- Las sombras, cuando existen, son **mínimas y sirven únicamente de anclaje físico** a elementos flotantes, nunca decorativas. REVISAR: propuesta `0 4px 12px rgba(0,0,0,0.15)`.
- Los overlays son bloques semitransparentes en los tonos de marca (ver {colors.overlay}), evitando negros o grises neutros difusos.

## Shapes

Las esquinas son **rectas (0px) por defecto** ({rounded.none}), reforzando el carácter funcional y ordenado del sistema. La excepción son los elementos que representan intervención humana o fotográfica:

- **Círculos perfectos ({rounded.full}, 50%)** para marcos de imagen, avatares o puntos de acento.
- **Recortes orgánicos** (formas irregulares tipo collage), reservados **exclusivamente** para el tratamiento fotográfico, nunca para componentes de interfaz funcional (botones, inputs, tarjetas).

Esta distinción es la **regla central del sistema de formas**: lo estructural es recto; lo interventor es orgánico. Nunca se mezclan en el mismo elemento.

## Components

- **Botones:** el principal {components.button-primary} es de esquinas rectas ({rounded.none}), con fondo {colors.primary} (magenta rojizo) y texto en el blanco de marca {colors.surface} (#F7F4D5) o en café {colors.on-surface} (#451A14) según el fondo. Tipografía en PerecScripte2 ({typography.label-button}), sin sutileza. El hover **invierte el contraste** (fondo ↔ texto) en vez de oscurecer tonos ({components.button-primary-hover}).
- **Secundarios/fantasma ({components.button-secondary}):** fondo {colors.button-secondary} (gris azul). REVISAR: el color de texto no está especificado en el documento; se propone {colors.on-surface}.
- **Bloques/tarjetas ({components.card}):** tarjetas de fondo plano (blanco {colors.surface} o café {colors.on-surface}) con espacio interno generoso (múltiplos de {spacing.base}) para evitar saturación. Cuando una tarjeta incluye imagen, la fotografía puede sangrar uno de los bordes como gesto de intervención controlada.
- **Tipografía como componente ({components.headline}):** los títulos display ({typography.display}, PerecScripte2) pueden ocupar el ancho completo del bloque como elemento gráfico principal, sustituyendo el rol que normalmente tendría una ilustración, especialmente en las secciones de apertura ("observar").
- **Intervención fotográfica ({components.photo-intervention}):** el componente distintivo del sistema. Una fotografía en duotono (magenta {colors.primary}/café {colors.on-surface}) que rompe parcialmente la rejilla, siempre acompañada de un pequeño elemento de acento (línea, recorte o forma orgánica) que señala visualmente el momento de "intervenir" en la narrativa. Se usa con moderación: **un momento de intervención fuerte por sección**, no saturado.
- **Enlaces e interactivos secundarios ({components.link}):** en azul cielo {colors.link}, subrayado **solo en hover**, nunca en reposo.

## Do's and Don'ts

**Sí**

- Usa la rejilla como base siempre; toda ruptura debe ser intencional y legible como parte de la narrativa (observar → intervenir → resolver).
- Trata toda fotografía con duotono de marca antes de insertarla; nunca fotografías sin intervenir.
- Reserva las formas orgánicas exclusivamente para el tratamiento fotográfico.
- Aplica alto contraste tipográfico siempre.
- Deja que el espacio en blanco funcione como pausa narrativa, no como relleno.

**No**

- No uses sombras difusas, degradados ni neumorfismo.
- No apliques recortes orgánicos a componentes funcionales de interfaz.
- No insertes fotografía de stock sin intervención de color/tratamiento.
- No rompas la rejilla en más de un punto por sección.
- No uses grises medios para texto de cuerpo.