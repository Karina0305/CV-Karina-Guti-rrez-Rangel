---
version: alpha
name: Sistema de Diseño Karina Gutiérrez Rangel v3
description: "Sistema en evolución: recorrido por zonas autocontenidas (cada una una 'parada' con su color, fotografía intervenida y tipografía protagonista), collage editorial con directorio de navegación e insignias circulares."
colors:
  primary: "#FFD8D9"            # Rosa: principal; CTA, acentos, títulos e identidad
  secondary: "#004952"          # Azul oscuro: para énfasis puntual
  on-surface: "#1D273B"         # Negro azulado: texto principal y mayor contraste
  surface: "#FFF7F8"            # Rosa claro: fondo principal
  link: "#0088CC"               # REVISAR: no listado en el documento reducido; se conserva para enlaces e interactivos secundarios
  button-secondary: "#AAC5B4"   # REVISAR: no listado en el documento reducido; se conserva para botones secundarios y fantasma
  text-tertiary: "#808080"      # REVISAR: no listado en el documento reducido; se conserva para texto terciario y deshabilitados
  overlay: "rgba(0,73,82,0.55)"         # REVISAR: bloque semitransparente azul oscuro (propuesto, coherente con la paleta)
  overlay-alt: "rgba(170,197,180,0.55)" # REVISAR: bloque semitransparente gris azul (propuesto, coherente con la paleta)
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
  zone-title:                   # Títulos de zona: condensados, bold, mayúsculas (REVISAR: medidas asumidas)
    fontFamily: Neue Haas Grotesk Display Pro
    fontSize: 40px
    fontWeight: 700
    lineHeight: 48px
    textTransform: uppercase
    letterSpacing: 0.02em
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
  xxl: 64px                     # REVISAR: nivel asumido
  gutter: 24px                  # REVISAR: separación entre columnas de la rejilla
  section: 64px                 # REVISAR: separación vertical entre zonas
  content-max: 1280px           # Ancho máximo de contenido
  grid-columns: "12"            # Rejilla en escritorio; cada zona rompe columna cuando la foto lo pide
  grid-columns-tablet: "8"      # Rejilla en tableta (composición interna simplificada)
  grid-columns-mobile: "1"      # Rejilla en móvil; las zonas se apilan en orden narrativo
rounded:
  none: 0px                     # Esquinas rectas por defecto en componentes funcionales
  full: 50%                     # Círculos perfectos: insignias, íconos de navegación, sellos/badges
components:
  button-primary:
    backgroundColor: "{colors.primary}"
    textColor: "{colors.on-surface}"     # rosa claro de fondo → texto oscuro para alto contraste (REVISAR)
    typography: "{typography.label-button}"
    rounded: "{rounded.none}"
    padding: 16px               # REVISAR: padding asumido
    height: 48px                # REVISAR: altura asumida
  button-primary-hover:
    backgroundColor: "{colors.on-surface}"   # Hover: invierte contraste (fondo ↔ texto)
    textColor: "{colors.surface}"
  button-secondary:
    backgroundColor: "{colors.button-secondary}"
    textColor: "{colors.on-surface}"
    typography: "{typography.label-button}"
    rounded: "{rounded.none}"
    padding: 16px               # REVISAR: padding asumido
    height: 48px                # REVISAR: altura asumida
  link:
    textColor: "{colors.link}"
    typography: "{typography.link}"
    underline: "solo en hover, nunca en reposo"
  nav-directory:                # "Directorio": mapa de zonas al inicio del recorrido
    badge: "círculo {rounded.full} con ícono o sello propio de la zona"
    label: "etiqueta corta"
    role: "ancla de orientación; permite saltar a cada zona"
  card:                         # Tarjeta de evento/proyecto: bloque sólido + foto intervenida superpuesta
    backgroundColor: "{colors.primary}"   # o {colors.on-surface}: siempre un tono sólido
    textColor: "{colors.on-surface}"      # (o {colors.surface} sobre fondos oscuros)
    rounded: "{rounded.none}"
    photo: "fotografía de intervención superpuesta, sin fondo blanco de respiro"
    rule: "alto contraste entre tarjetas contiguas"
  headline:                     # Tipografía como componente: título de zona a ancho completo
    typography: "{typography.zone-title}"
    width: "full-width del bloque"
    role: "elemento gráfico principal que ancla el inicio de cada parada"
  badge:
    shape: "círculo {rounded.full}"
    content: "ícono o sello distintivo de la zona"
    role: "hilo conductor visual entre secciones"
  icon-accent:                  # Insignias/sellos de acento, uno por zona
    shape: "círculo o dibujado a mano (flechas, estrellas simples, subrayados irregulares)"
    rule: "un solo elemento por sección, nunca saturado"
  photo-intervention:           # Componente distintivo
    treatment: "duotono con la paleta de marca ({colors.primary} / {colors.secondary})"   # REVISAR: tonos exactos del duotono
    grid: "rompe parcialmente la rejilla al pasar de una zona a otra"
    overlay: "{colors.overlay} o {colors.overlay-alt} sobre imágenes; nunca negros difusos"
---

# Sistema de Diseño

## Overview

Mi marca encarna una estética de **collage, con intervención de la fotografía** y centrada en la exploración de la imaginación: un puente entre la experiencia funcional —legible, sin saturación— y el gesto expresivo. La estructura ya no es una página lineal: es un **recorrido por "zonas" autocontenidas**, donde cada sección es una **"parada" distinta** dentro de un mismo recorrido creativo, cada una con su propia combinación de color, fotografía intervenida y tipografía protagonista.

Priorizo el orden y la legibilidad con una filosofía funcional: layouts con pausas de espacio y tipografía con propósito, para creativos y desarrolladores. En una frase: un conjunto de elementos, pero con orden y espacio, con componentes con ornamentación.

## Colors

La paleta se reduce a **cuatro colores de marca**: un **rosa principal** (#FFD8D9), un **azul oscuro** (#004952) para el énfasis, el **negro azulado** (#1D273B) como texto de máximo contraste y el **rosa claro** (#FFF7F8) como fondo. Cada **zona** del recorrido puede tener su propio fondo sólido dominante (rosa claro, negro azulado o azul oscuro) para que se sienta como una parada distinta dentro del mismo sistema.

- **Primary ({colors.primary}, #FFD8D9):** rosa. Botones de acción (CTA), acentos, títulos e identidad de marca. REVISAR: es un rosa muy claro; al usarlo como fondo, el texto va en {colors.on-surface} para alto contraste.
- **Secondary ({colors.secondary}, #004952):** azul oscuro, para énfasis puntual.
- **Texto principal / on-surface ({colors.on-surface}, #1D273B):** negro azulado, texto principal y mayor contraste.
- **Superficie / rosa claro ({colors.surface}, #FFF7F8):** fondo principal.
- **De apoyo (REVISAR):** no aparecen en el documento reducido, pero se conservan por necesidad funcional — {colors.link} #0088CC para enlaces e interactivos, {colors.button-secondary} #AAC5B4 para botones secundarios y fantasma, {colors.text-tertiary} #808080 para deshabilitados, y los overlays {colors.overlay} / {colors.overlay-alt} para contenido sobre imágenes.

> REVISAR: {colors.link} sobre el rosa claro (#FFF7F8) contrasta ≈ 3.9:1 (bajo AA 4.5:1 para texto normal). Aceptable para interactivos, no para cuerpo.

## Typography

Dos familias con roles claros: **Neue Haas Grotesk Display Pro** como fuente principal —cuerpo, navegación y contenido general— y **PerecScripte2** como secundaria —títulos, botones y énfasis. La versión **roman** de la familia principal (la más gruesa) queda reservada para los títulos más importantes.

- **Display ({typography.display}):** PerecScripte2 a 40px, interlineado 48px.
- **H1 ({typography.h1}):** Neue Haas a 40px, peso 700.
- **H2 ({typography.h2}):** Neue Haas roman a 40px.
- **Título de zona ({typography.zone-title}):** Neue Haas condensada, bold, en mayúsculas, a ancho completo — REVISAR: medidas asumidas.
- **H3 · subsecciones ({typography.h3}):** Neue Haas a 16px, peso 700.
- **Cuerpo ({typography.body}):** Neue Haas a 20px, interlineado 30px.
- **Ítems de lista ({typography.list-item}):** Neue Haas medium a 20px.
- **Texto pequeño ({typography.small}):** Neue Haas a 16px.
- **Etiqueta de botón ({typography.label-button}):** PerecScripte2 a 19.216px.
- **Enlaces ({typography.link}):** Neue Haas a 20px.

La jerarquía siempre se logra con **tamaño, peso y color, nunca con opacidad**. El cuerpo nunca baja de 16px y la versión roman se usa con moderación.

## Layout

El layout es un **recorrido por "zonas"**: en lugar de un scroll único y lineal, la estructura se divide en **bloques temáticos autocontenidos** —cada sección una "parada" distinta dentro del recorrido creativo— con su propia combinación de color, fotografía intervenida y tipografía protagonista.

- Unidad base de {spacing.base} (8px) para el espaciado interno de componentes.
- Ancho máximo de contenido: {spacing.content-max} (1280px).
- **Escritorio:** rejilla de {spacing.grid-columns} (12) columnas; cada zona tiene su **propia composición interna** (texto + imagen a la izquierda, imagen flotante a la derecha, tarjetas en mosaico), rompiendo la columna cuando la fotografía de intervención lo pide, igual que en un collage editorial.
- **Punto de entrada de cada zona:** siempre hay un título grande o un **mapa visual de navegación** (directorio de secciones), para saber en qué parte del recorrido se está aunque el estilo visual cambie.
- **Tableta:** rejilla de {spacing.grid-columns-tablet} (8) columnas; se conservan las zonas pero la composición interna se simplifica a una sola combinación por bloque.
- **Móvil:** una columna; las zonas se apilan en el **mismo orden narrativo** (observar → intervenir → resolver) que en escritorio.
- **El espacio en blanco separa zonas con la misma fuerza que un cambio de color:** cada "parada" se siente como un respiro antes de la siguiente.

Hitos responsivos (mobile-first):

- **Móvil (320–599px):** el directorio de navegación se convierte en lista vertical o carrusel horizontal de badges; cada zona ocupa el ancho completo y se apila en orden narrativo, con la fotografía de intervención **contenida dentro del margen** (sin sangrado).
- **Tableta (600–1023px):** el directorio se muestra como rejilla de 2–3 badges por fila; las zonas combinan texto e imagen en pares.
- **Escritorio (1024–1279px):** sistema completo: directorio visible como mapa de secciones, zonas con composición interna variable y fotografía de intervención rompiendo la rejilla libremente.
- **Escritorio amplio (1280px+):** contenido centrado en {spacing.content-max}, pero el fondo sólido de cada zona puede extenderse a todo el viewport (full-bleed), reforzando la sensación de "parada" independiente.

## Elevation & Depth

El sistema es **plano y de alto contraste, sin degradados ni sombras difusas**. La profundidad se logra por **superposición de capas**: fotografía intervenida —tratada en **duotono con la paleta de marca**— colocada sobre bloques de color sólido, generando contraste duro entre superficie fotográfica y superficie gráfica.

- **Elementos flotantes** (fotografías de intervención, insignias o "stickers" de acento): llevan una **sombra mínima y realista**, solo para dar anclaje físico (propuesta `0 4px 12px rgba(0,0,0,0.15)` — REVISAR), nunca decorativa.
- **Overlays:** bloques semitransparentes coherentes con la paleta (azul oscuro {colors.overlay} o gris azul {colors.overlay-alt}), evitando negros difusos.
- **Cada zona** puede tener su propio fondo sólido dominante (rosa claro, negro azulado o azul oscuro), reforzando que es una parada distinta dentro del mismo sistema.
- Se descarta el lenguaje de neumorfismo, glassmorphism y blur decorativo.

## Shapes

Las esquinas son **rectas (0px) por defecto** ({rounded.none}) en los componentes funcionales de interfaz (tarjetas, botones estándar, inputs), reforzando el carácter ordenado y legible del sistema. Se permiten **dos excepciones puntuales**:

- **Círculos perfectos ({rounded.full}, 50%)** para insignias, íconos de navegación entre zonas o marcadores tipo "sello/badge" que señalan cada parada del recorrido.
- **Recortes orgánicos hechos a mano**, reservados exclusivamente para el tratamiento fotográfico de intervención (nunca para componentes de interfaz).

Los **badges circulares funcionan como el hilo conductor visual entre zonas**: cada sección puede tener su propio ícono o sello distintivo, dando la sensación de recorrer puntos de interés dentro de un mismo mapa creativo.

## Components

- **Botones:** el principal {components.button-primary} es de **esquinas rectas ({rounded.none})**, fondo {colors.primary} (rosa) y texto en {colors.on-surface} (negro azulado) para alto contraste. Tipografía en PerecScripte2, bold y sin sutileza. El hover **invierte el contraste** (fondo ↔ texto) ({components.button-primary-hover}).
- **Enlaces ({components.link}):** color {colors.link}, subrayado **solo en hover**, nunca en reposo.
- **Navegación por zonas ({components.nav-directory}):** un "directorio" o mapa de secciones al inicio del recorrido, con **badges circulares** y etiquetas cortas, que permite saltar directamente a cada zona temática. Funciona como ancla de orientación dentro del sistema.
- **Tarjetas de evento/proyecto ({components.card}):** cada zona presenta su contenido en tarjetas de **bloque sólido con fotografía de intervención superpuesta y texto directo** (sin fondo blanco de "respiro"). Alto contraste entre tarjetas contiguas.
- **Tipografía como componente ({components.headline}):** los títulos de zona (condensados, bold, mayúsculas) ocupan el ancho completo del bloque y funcionan como elemento gráfico principal, anclando visualmente el inicio de cada "parada" del recorrido.
- **Insignias/sellos de acento ({components.badge}, {components.icon-accent}):** íconos circulares o dibujados a mano (flechas, estrellas simples, subrayados irregulares) como acento puntual de cada zona — **un solo elemento por sección**, nunca saturado.
- **Fotografía de intervención ({components.photo-intervention}):** el componente distintivo: imágenes en **duotono de marca** que **rompen parcialmente la rejilla** al pasar de una zona a otra, marcando visualmente la transición entre "paradas" del recorrido.

## Do's and Don'ts

**Sí**

- Organiza el contenido en zonas/bloques autocontenidos, cada uno con su propia combinación de color dentro de la paleta de marca.
- Usa un componente de navegación tipo directorio para orientar el recorrido entre zonas.
- Trata toda fotografía con duotono de marca antes de insertarla como intervención.
- Reserva las formas orgánicas y recortes exclusivamente para el tratamiento fotográfico.
- Usa insignias circulares como hilo conductor visual entre secciones.
- Aplica alto contraste tipográfico siempre.

**No**

- No uses degradados suaves ni sombras difusas de estilo "material design".
- No repitas la misma combinación de color en dos zonas consecutivas: cada parada debe sentirse distinta.
- No apliques formas orgánicas a componentes funcionales de interfaz.
- No uses fotografía sin intervenir (sin duotono/tratamiento de color).
- No compitas con más de un titular gigante por zona/vista.
- No uses grises medios para texto de cuerpo.