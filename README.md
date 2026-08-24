# La Vendición Records — Mi Recomendador Personal

## 📌 Descripción

Mini sitio web que recomienda contenido del sello discográfico independiente **La Vendición Records** (música urbana, España). El sitio recorre la historia del sello, sus canciones y álbumes más representativos, y su proyección a futuro, pensado tanto como entrega de bootcamp como pieza de portafolio.

El recomendador funciona a través de:
- **Inicio**: 3 canciones destacadas ("Si mañana me muero", "Soy Bichote - Remix", "Rifle Bisexual")
- **¿Qué es La Vendición?**: historia del sello (fundado en diciembre 2015 por Yung Beef) y línea de tiempo de hitos 2016–2026
- **Imprescindibles**: 3 álbumes clave para entender el concepto del sello
- **¿Qué sigue?**: actualidad y futuro del sello (Infierno Festival, nuevos lanzamientos, nuevas promesas)
- **Footer**: enlaces a redes sociales del sello

## 🛠 Tecnologías

- HTML5 semántico
- CSS3 (variables personalizadas, tipografías de Google Fonts, efectos hover)
- Bootstrap 5 (navbar, container, row/col, cards, botones, carousel, badge)
- JavaScript básico (variables `let`, tipos string/number/boolean, `console.log()`)
- Git y GitHub
- Herramienta de IA como tutor/asistente durante el proceso

## 🤖 Proceso con IA

Trabajé con la IA como tutor, no como generador de código: en cada etapa (HTML, Bootstrap, CSS, JavaScript) le pedí explícitamente que no me diera la solución completa, sino que me guiara con preguntas, pistas y explicaciones, y que me detuviera a explicar cualquier concepto nuevo antes de seguir.

### Prompt 1 — Planificar la página (etapa HTML)
**Necesitaba:** entender cómo dividir mi proyecto "Mi recomendador personal" en pasos pequeños, respetando que solo conocía HTML, CSS, Bootstrap básico y variables de JavaScript.
**Qué respondió la IA:** propuso empezar por el esqueleto HTML semántico (`header`, `main`, `section`, `footer`) antes de meter contenido, y guiarme con preguntas en vez de darme el código completo.
**Qué utilicé:** la estructura de 5 secciones (Inicio, ¿Qué es La Vendición?, Imprescindibles, ¿Qué sigue?, Footer) que yo mismo propuse a partir de esa guía.
**Qué aprendí:** la diferencia entre HTML semántico (`header`, `main`, `section`, `article`) y usar `<div>` genéricos para todo — y por qué la jerarquía de anidación (qué va dentro de qué) importa aunque el navegador no siempre marque error si está mal.

### Prompt 2 — HTML (depuración de estructura)
**Necesitaba:** validar que mi anidación de etiquetas fuera correcta después de escribir mi primer boceto.
**Qué respondió la IA:** en vez de corregirlo directamente, me hizo preguntas guía para que yo mismo detectara que mis `<section>` habían quedado fuera de `<main>`, y que mi `<footer>` estaba fuera de `<body>`.
**Qué utilicé:** corregí la anidación yo mismo comparando línea por línea.
**Qué aprendí:** que el navegador no siempre "avisa" cuando algo está mal (como una clase de Bootstrap sin conectar, o una etiqueta mal anidada) — el paso de PROBAR en el navegador es indispensable, no opcional.

### Prompt 3 — Bootstrap
**Necesitaba:** incorporar Bootstrap sin perder de vista qué estaba haciendo cada clase, ya que en clase solíamos copiar/pegar código sin detenernos a entenderlo.
**Qué respondió la IA:** explicó cada clase nueva (`container`, `row`, `col`, `card`, `navbar`, `carousel`, `badge`) respondiendo siempre: qué significa, para qué sirve, si es de HTML/CSS/Bootstrap, por qué se usa ahí, y qué pasa si se quita.
**Qué utilicé:** el patrón completo de Bootstrap en las 4 secciones — cards verticales en Inicio, cards horizontales en Imprescindibles (para diferenciarlas visualmente), un carousel en Historia, y un badge tipo "noticia" en Futuro, más un iframe de YouTube embebido con la clase `ratio-16x9`.
**Qué aprendí:** cómo funciona la cascada de CSS (por qué el CSS de Bootstrap va antes que mi `styles.css` en el `<head>`), y la diferencia entre HTML semántico (`<article>`) y clases puramente visuales de Bootstrap (`card`) — y por qué conviene usarlos juntos, no uno en lugar del otro.

### Prompt 4 — CSS
**Necesitaba:** darle identidad visual al sitio (estética Y2K/DIY/infernal, con colores rojo sangre, morado y rosa) sin perder legibilidad ni cumplir por cumplir.
**Qué respondió la IA:** propuso trabajar con variables CSS (`:root`) para la paleta de colores, y fue explicando cada propiedad nueva (`text-shadow`, `object-fit`, `border-left` para simular una línea de tiempo, `:hover` y `transition` para los botones) antes de aplicarla.
**Qué utilicé:** el sistema de variables de color, la combinación de dos tipografías (Bungee para títulos grandes con estética "sucia" tipo trap, y una fuente legible para el cuerpo), y el efecto de card "hundida" en el mismo tono del fondo con borde morado, que decidí yo mismo tras comparar dos direcciones posibles (card más clara vs. más oscura que el fondo).
**Qué aprendí:** que `!important` sirve para sobrescribir estilos "insistentes" de Bootstrap, pero que abusar de él hace perder el control de la cascada — se usa como excepción puntual, no como costumbre.

## ✍️ Código generado por IA vs. código propio

- **Generado con guía de la IA:** la sintaxis base de componentes de Bootstrap que nunca había usado a fondo (carousel, badge, iframe responsive con `ratio`), y la explicación de propiedades CSS nuevas.
- **Modificado/decidido por mí:** todo el contenido real (historia del sello, canciones, álbumes, línea de tiempo de hitos), la paleta de colores y su aplicación específica, la elección de tipografías, la estructura de las 5 secciones, y las decisiones de diseño (por ejemplo, pedir explícitamente que las cards de Imprescindibles usaran un layout distinto a las de Inicio para diferenciarlas).

## ⭐ Prompt que más me ayudó

El de la etapa de **Bootstrap**, porque obligó a la IA a explicar cada clase con la misma estructura de 5 preguntas (qué es, para qué sirve, de dónde viene, por qué se usa, qué pasa si se quita). Eso evitó que terminara con "código que se ve bonito pero no puedo explicar" — que era justo mi mayor miedo al empezar esta actividad.

## 🌱 Evolución de un prompt

**Prompt inicial:** *"Hazme una página de películas."*

**Prompt mejorado (adaptado a mi proyecto):**
*"Actúa como tutor de desarrollo web para principiantes. Estoy creando un sitio web llamado 'Mi recomendador personal' sobre el sello discográfico La Vendición Records, utilizando HTML, CSS, Bootstrap y variables básicas de JavaScript. Ya conozco HTML, CSS, Bootstrap y variables en JavaScript, pero todavía no conozco funciones, ciclos ni manipulación del DOM. Ayúdame a dividir el proyecto en pasos pequeños, sin generar todo el código de una vez."*

**Qué mejoró:** el prompt inicial no dice nada sobre el nivel del estudiante ni sobre cómo quiere que la IA le ayude — cualquier respuesta genérica hubiera servido, aunque no la entendiera. El prompt mejorado fija el rol de la IA (tutor, no generador), mi tema real, mis límites de conocimiento explícitos, y pide un proceso paso a paso en vez de una solución de una sola vez.

## 💡 Aprendizaje

Uno de los conceptos que más comprendí gracias a la IA fue la diferencia entre **estructura (HTML)**, **layout/componentes (Bootstrap)** y **estilo (CSS)** — antes tendía a verlo todo como "una sola cosa que hace que la página se vea bien". Ahora puedo explicar, por ejemplo, que `<article>` le da significado semántico a una recomendación, `card` le da su apariencia visual gracias a Bootstrap, y mi `styles.css` es lo que la hace sentir parte de mi identidad (colores, tipografía, bordes).

## 🔍 Reflexión

Sí hubo momentos donde la IA generó código que no comprendía del todo a la primera — por ejemplo, las clases `d-flex flex-column text-center` que aparecieron en mis cards sin que las hubiera pedido explícitamente. En vez de dejarlas sin más, pregunté qué hacía cada una antes de seguir usándolas. También tuve errores reales de depuración fuera del código en sí: un video de YouTube que no cargaba por copiar mal el ID del embed, y más de un conflicto de Git (`commit-m` sin espacio, y un push rechazado por ramas divergentes) que resolví entendiendo la diferencia entre mi repositorio local y el remoto en GitHub, en vez de solo copiar un comando sin saber qué hacía.



## 🔗 Repositorio

*(https://github.com/alexanderurvinacolin-creator/La-Vendicion-Website)*
