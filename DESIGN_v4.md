---
version: alpha
name: Sistema de Diseño Karina Gutiérrez Rangel v4
description: "Sistema inspirado en el microsite KAWAII 2026 (ASOBISYSTEM): recorrido por zonas tipo festival, una sola familia tipográfica (Filson Soft), paleta rosa/azul oscuro y tarjetas inclinadas con fotografía en duotono."
colors:
  primary: "#FFD8D9"            # Rosa: CTA, acentos, títulos e identidad de marca
  secondary: "#004952"          # Azul oscuro: énfasis puntual, interactivos secundarios y acentos de zona
  on-surface: "#1D273B"         # Negro azulado: texto principal y mayor contraste
  surface: "#FFF7F8"            # Rosa claro: fondo principal
  link: "#004952"               # REVISAR: no listado; se usa el azul oscuro, que el documento destina a interactivos secundarios
  button-secondary: "#004952"   # REVISAR: propuesto — azul oscuro como estado alterno de botones
  text-tertiary: "#808080"      # REVISAR: conservado del set anterior para texto terciario/deshabilitados
  overlay: "rgba(0,73,82,0.55)"         # REVISAR: bloque semitransparente azul oscuro sobre imágenes
  overlay-alt: "rgba(255,216,217,0.85)" # REVISAR: bloque semitransparente rosa sobre imágenes
typography:
  family: Filson Soft           # Una sola familia con pesos; redondeada, cálida y contemporánea
  display:                      # Título display, el más grande
    fontFamily: Filson Soft
    fontSize: 44px
    fontWeight: 700             # Bold
    lineHeight: 52px
  h1:
    fontFamily: Filson Soft
    fontSize: 32px
    fontWeight: 700             # Bold
    lineHeight: 40px            # REVISAR: interlineado asumido
  h2:
    fontFamily: Filson Soft
    fontSize: 24px
    fontWeight: 600             # SemiBold → se mapea a Medium (REVISAR: no existe el peso SemiBold en los assets)
    lineHeight: 32px            # REVISAR: interlineado asumido
  h3:                           # Subsecciones
    fontFamily: Filson Soft
    fontSize: 18px
    fontWeight: 600             # SemiBold → se mapea a Medium (REVISAR)
    lineHeight: 26px            # REVISAR: interlineado asumido
  zone-title:                   # Título de zona: Filson Soft Bold, mayúsculas (REVISAR: medidas asumidas)
    fontFamily: Filson Soft
    fontSize: 32px
    fontWeight: 700
    lineHeight: 40px
    textTransform: uppercase
    letterSpacing: 0.02em
  body:
    fontFamily: Filson Soft
    fontSize: 16px
    fontWeight: 400             # Regular
    lineHeight: 24px
  list-item:
    fontFamily: Filson Soft
    fontSize: 16px
    fontWeight: 500             # Medium
    lineHeight: 24px            # REVISAR: interlineado asumido (igual al cuerpo)
  small:
    fontFamily: Filson Soft
    fontSize: 13px
    fontWeight: 400
    lineHeight: 18px            # REVISAR: interlineado asumido
  label-button:
    fontFamily: Filson Soft
    fontSize: 15px
    fontWeight: 700             # Bold
    lineHeight: 20px            # REVISAR: interlineado asumido
    letterSpacing: 0.04em       # Tracking ligeramente abierto para el tono lúdico
  link:
    fontFamily: Filson Soft
    fontSize: 16px
    fontWeight: 500             # Medium
    lineHeight: 24px            # REVISAR: interlineado asumido (igual al cuerpo)
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
  grid-columns: "12"            # Rejilla en escritorio; las zonas inclinan/superponen/rompen columna
  grid-columns-tablet: "8"      # Rejilla en tableta (composición interna simplificada)
  grid-columns-mobile: "1"      # Rejilla en móvil; las zonas se apilan en orden narrativo
rounded:
  none: 0px                     # Esquinas rectas por defecto en componentes funcionales
  full: 50%                     # Círculos perfectos: insignias, badges de navegación, marcadores de parada
components:
  button-primary:
    backgroundColor: "{colors.primary}"
    textColor: "{colors.on-surface}"     # rosa de fondo → texto negro azulado para alto contraste
    typography: "{typography.label-button}"
    rounded: "{rounded.none}"
    padding: 16px               # REVISAR: padding asumido
    height: 48px                # REVISAR: altura asumida
  button-primary-hover:
    backgroundColor: "{colors.on-surface}"   # Hover: invierte contraste (fondo ↔ texto)
    textColor: "{colors.surface}"
  button-primary-hover-alt:
    backgroundColor: "{colors.secondary}"    # Estado alterno: azul oscuro (REVISAR)
    textColor: "{colors.surface}"
  button-secondary:
    backgroundColor: "{colors.button-secondary}"
    textColor: "{colors.surface}"
    typography: "{typography.label-button}"
    rounded: "{rounded.none}"
    padding: 16px               # REVISAR: padding asumido
    height: 48px                # REVISAR: altura asumida
  link:
    textColor: "{colors.link}"
    typography: "{typography.link}"
    underline: "solo en hover, nunca en reposo"
  nav-directory:                # Directorio / mapa de zonas al inicio del recorrido
    badge: "círculo {rounded.full} con ícono o sello propio de la zona"
    label: "etiqueta corta"
    role: "ancla de orientación; permite saltar a cada zona (como un índice de festival)"
  card:                         # Tarjeta de bloque sólido + fotografía de intervención superpuesta
    backgroundColor: "{colors.primary}"   # o {colors.on-surface} / {colors.secondary}: siempre un tono sólido
    textColor: "{colors.on-surface}"      # (o {colors.surface} sobre fondos oscuros)
    rounded: "{rounded.none}"
    photo: "fotografía de intervención superpuesta, sin fondo blanco de respiro"
    dynamism: "algunas tarjetas se superponen o inclinan unos grados (recorte de collage)"
    rule: "alto contraste entre tarjetas contiguas"
  headline:                     # Tipografía como componente: título de zona a ancho completo
    typography: "{typography.zone-title}"
    width: "full-width del bloque"
    role: "elemento gráfico principal que ancla el inicio de cada parada"
  badge:
    shape: "círculo {rounded.full}"
    content: "ícono o sello distintivo de la zona"
    role: "hilo conductor visual entre secciones"
  icon-accent:                  # Insignias y acentos, uno por zona
    shape: "círculo o dibujado a mano (flechas, estrellas simples, subrayados irregulares)"
    rule: "un solo elemento por sección, nunca saturado"
  photo-intervention:           # Componente distintivo
    treatment: "duotono con la paleta de marca ({colors.primary} / {colors.secondary})"   # REVISAR: tonos exactos
    grid: "rompe parcialmente la rejilla al pasar de una zona a otra"
    overlay: "{colors.overlay} o {colors.overlay-alt} sobre imágenes; nunca negros difusos"
---

# Sistema de Diseño

## Overview

Mi marca encarna una estética de **collage, con intervención de la fotografía** y centrada en la exploración de la imaginación: un puente entre la experiencia funcional —legible, sin saturación— y el gesto expresivo. La estructura y el **dinamismo** toman como referencia el microsite **KAWAII 2026 de ASOBISYSTEM**: un festival urbano organizado por zonas, con navegación lúdica entre secciones, mucha fotografía y un ritmo visual muy dinámico.

Priorizo el orden y la legibilidad con una filosofía funcional: layouts con pausas de espacio y tipografía con propósito, para creativos y desarrolladores. En una frase: un conjunto de elementos, pero con orden y espacio, con componentes con ornamentación.

## Colors

La paleta se construye sobre un **rosa de marca** y una **base de neutros de alto contraste**, con un **azul oscuro** como contrapunto. Cada zona del recorrido tiene su propia combinación dentro de la paleta para que se sienta como una parada distinta.

- **Primary ({colors.primary}, #FFD8D9):** rosa. Botones de acción (CTA), acentos, títulos e identidad de marca. REVISAR: al ser un rosa muy claro, el texto sobre él va en {colors.on-surface}.
- **Secondary ({colors.secondary}, #004952):** azul oscuro. Énfasis puntual, elementos interactivos secundarios y detalles de acento dentro de las zonas.
- **Texto principal / on-surface ({colors.on-surface}, #1D273B):** negro azulado, texto principal y mayor contraste.
- **Superficie / rosa claro ({colors.surface}, #FFF7F8):** fondo principal.
- **De apoyo (REVISAR):** no aparecen en el documento, se conservan por necesidad funcional — {colors.link} (azul oscuro) para enlaces, {colors.button-secondary} (azul oscuro) para botones secundarios, {colors.text-tertiary} para deshabilitados y overlays {colors.overlay} (azul oscuro) / {colors.overlay-alt} (rosa) para contenido sobre imágenes.

> REVISAR: {colors.link} (azul oscuro #004952) sobre el rosa claro (#FFF7F8) tiene contraste ≈ 12:1, muy por encima de AA; es seguro para cuerpo. Los overlays usan solo rosa o azul oscuro, nunca negros o grises difusos.

## Typography

Una sola familia tipográfica con distintos pesos para dar dinamismo: **Filson Soft**. Es una fuente **redondeada, cálida y contemporánea**, coherente con el carácter lúdico y a la vez ordenado de la marca; funciona tanto para titulares grandes como para cuerpo de texto sin perder personalidad.

- **Display ({typography.display}):** Filson Soft Bold a 44px, interlineado 52px.
- **H1 ({typography.h1}):** Filson Soft Bold a 32px.
- **H2 ({typography.h2}):** Filson Soft SemiBold a 24px. REVISAR: el peso SemiBold se mapea a Medium (no existe en los assets).
- **H3 · subsecciones ({typography.h3}):** Filson Soft SemiBold a 18px.
- **Título de zona ({typography.zone-title}):** Filson Soft Bold, mayúsculas, a ancho completo — REVISAR: medidas asumidas.
- **Cuerpo ({typography.body}):** Filson Soft Regular a 16px, interlineado 24px.
- **Ítems de lista ({typography.list-item}):** Filson Soft Medium a 16px.
- **Texto pequeño ({typography.small}):** Filson Soft Regular a 13px.
- **Etiqueta de botón ({typography.label-button}):** Filson Soft Bold a 15px, con tracking ligeramente abierto para reforzar el tono lúdico.
- **Enlaces ({typography.link}):** Filson Soft Medium a 16px.

La jerarquía siempre se logra con **tamaño, peso y color, nunca con opacidad**. El cuerpo nunca baja de 13px, y Filson Soft Bold se usa con moderación, solo para los titulares más importantes y las llamadas a la acción.

## Layout

El layout se organiza como un **recorrido por zonas**, tomando como referencia la estructura de **KAWAII 2026**: en lugar de un scroll lineal uniforme, la página se divide en **bloques temáticos autocontenidos** —"paradas" dentro de un mismo recorrido creativo—, cada una con su propia combinación de color dentro de la paleta, fotografía intervenida y tipografía protagonista.

- Unidad base de {spacing.base} (8px) para el espaciado interno de componentes.
- Ancho máximo de contenido: {spacing.content-max} (1280px).
- **Escritorio:** rejilla de {spacing.grid-columns} (12) columnas; cada zona tiene su propia composición interna, y los bloques pueden **inclinarse, superponerse o romper la columna** para reforzar el dinamismo — a diferencia de una rejilla estrictamente uniforme.
- **Punto de entrada:** al inicio del recorrido hay siempre un **mapa o directorio de navegación** (índice de zonas) con badges o etiquetas que permiten saltar directamente a cada sección, igual que en un microsite de festival.
- **Tableta:** rejilla de {spacing.grid-columns-tablet} (8) columnas, conservando las zonas pero simplificando su composición interna.
- **Móvil:** una sola columna, apilando cada zona en el mismo orden narrativo que en escritorio, priorizando siempre la legibilidad.
- **El espacio en blanco separa zonas con la misma fuerza que un cambio de color:** cada parada se siente como un respiro dinámico antes de la siguiente, nunca como un vacío neutro.

Hitos responsivos (mobile-first):

- **Móvil (320–599px):** el directorio de navegación se convierte en un **carrusel horizontal de badges**; cada zona ocupa el ancho completo y se apila en orden narrativo, con la fotografía de intervención contenida dentro del margen.
- **Tableta (600–1023px):** el directorio se muestra como rejilla de 2–3 badges por fila; las zonas combinan texto e imagen en pares.
- **Escritorio (1024–1279px):** sistema completo: directorio visible como mapa de secciones, zonas con composición interna variable, tarjetas ligeramente inclinadas o superpuestas y fotografía de intervención rompiendo la rejilla libremente.
- **Escritorio amplio (1280px+):** contenido centrado en {spacing.content-max}, pero el fondo sólido de cada zona puede extenderse a todo el viewport (full-bleed), reforzando la sensación de "parada" independiente y dinámica.

## Elevation & Depth

El sistema es **plano y de alto contraste, sin degradados suaves ni sombras difusas**. La profundidad se logra únicamente por **superposición de capas sólidas**: fotografía intervenida —tratada en **duotono con la paleta de marca**— colocada sobre bloques de color sólido, generando contraste duro entre superficie fotográfica y superficie gráfica.

- Para reforzar el dinamismo, algunos elementos **flotan con una ligera inclinación o se superponen parcialmente** entre sí (como recortes de collage), siempre con una **sombra mínima y realista** que sirve únicamente de anclaje físico (propuesta `0 4px 12px rgba(29,39,59,0.18)` — REVISAR), nunca decorativa.
- **Overlays:** bloques semitransparentes en **rosa o azul oscuro** ({colors.overlay} / {colors.overlay-alt}), evitando negros o grises difusos.
- **No se usa ningún tipo de degradado** en fondos, botones ni tipografía.

## Shapes

Las esquinas son **rectas (0px) por defecto** ({rounded.none}) en los componentes funcionales de interfaz (tarjetas, botones estándar, inputs), reforzando el carácter ordenado del sistema. Se permiten **dos excepciones puntuales**:

- **Círculos perfectos ({rounded.full}, 50%)** para insignias, badges de navegación entre zonas o marcadores que señalan cada parada del recorrido.
- **Recortes orgánicos hechos a mano**, reservados exclusivamente para el tratamiento fotográfico de intervención.

Los **badges circulares funcionan como hilo conductor visual entre zonas**, dando la sensación de recorrer distintos puntos de interés dentro de un mismo mapa creativo — el mismo principio dinámico del sitio de referencia.

## Components

- **Botones:** el principal {components.button-primary} es de **esquinas rectas ({rounded.none})**, fondo {colors.primary} (rosa #FFD8D9) y texto en {colors.on-surface} (negro azulado #1D273B). Tipografía Filson Soft Bold, sin sutileza. El hover **invierte el contraste** (fondo ↔ texto) o **cambia a azul oscuro** {colors.secondary} como estado alterno ({components.button-primary-hover} / {components.button-primary-hover-alt}).
- **Enlaces ({components.link}):** color {colors.link} (azul oscuro), subrayado **solo en hover**, nunca en reposo.
- **Navegación por zonas ({components.nav-directory}):** directorio o mapa de secciones al inicio del recorrido, con **badges circulares** y etiquetas cortas, que permite saltar directamente a cada zona temática — el ancla de orientación del sistema.
- **Bloques/tarjetas ({components.card}):** cada zona presenta su contenido en tarjetas de **bloque sólido con fotografía de intervención superpuesta y texto directo**. Para dar dinamismo, algunas tarjetas **se superponen ligeramente o se inclinan unos grados**, simulando recortes de collage colocados a mano.
- **Tipografía como componente ({components.headline}):** los títulos de zona (Filson Soft Bold, mayúsculas) ocupan el ancho completo del bloque y funcionan como elemento gráfico principal, anclando el inicio de cada parada.
- **Insignias y acentos ({components.badge}, {components.icon-accent}):** íconos circulares o dibujados a mano (flechas, estrellas simples, subrayados irregulares) como acento puntual de cada zona — **un solo elemento por sección**, nunca saturado.
- **Fotografía de intervención ({components.photo-intervention}):** el componente distintivo: imágenes en **duotono de marca** que **rompen parcialmente la rejilla** al pasar de una zona a otra, marcando visualmente la transición entre paradas.

## Do's and Don'ts

**Sí**

- Organiza el contenido en zonas o bloques autocontenidos, cada uno con su propia combinación de color dentro de la paleta.
- Usa un componente de navegación tipo directorio para orientar el recorrido entre zonas.
- Trata toda fotografía con duotono de marca antes de insertarla como intervención.
- Permite ligeras inclinaciones o superposiciones entre tarjetas para reforzar el dinamismo tipo collage.
- Reserva las formas orgánicas y recortes exclusivamente para el tratamiento fotográfico.
- Usa insignias circulares como hilo conductor visual entre secciones.
- Aplica alto contraste tipográfico siempre.

**No**

- No uses degradados suaves ni sombras difusas de estilo material design.
- No repitas la misma combinación de color en dos zonas consecutivas: cada parada debe sentirse distinta.
- No apliques formas orgánicas a componentes funcionales de interfaz.
- No uses fotografía sin intervenir (sin duotono o tratamiento de color).
- No compitas con más de un titular gigante por zona o vista.
- No uses grises medios para texto de cuerpo.