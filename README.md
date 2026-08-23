# 1. Nombre del proyecto
La Vendicion Records - Recomendador Musical

# 2. Descripción
**¿Qué hace tu recomendador?**
Es un mini sitio web diseñado para introducir a nuevos oyentes al concepto del sello discográfico independiente español "La Vendicion Records". Recomienda un "Top 3" de canciones iniciales, detalla brevemente la historia del sello, y sugiere 3 álbumes imprescindibles para entender su impacto en la música urbana.

**Preguntas de mi fase "PIENSO":**
*   **¿Qué voy a recomendar?** Canciones y álbumes del sello La Vendicion.
*   **¿A quién va dirigida la página?** A fans del rap, trap y reggaetón underground que quieran conocer los orígenes de esta ola en España.
*   **¿Qué información tendrá cada recomendación?** Título de la obra, una imagen de portada, una breve reseña justificando la elección y un botón para escucharla.
*   **¿Qué quiero que suceda cuando el usuario interactúe con mi página?** Que pueda navegar fluidamente por las secciones, visualizar imágenes en el carrusel, leer las reseñas y ver la entrevista final adaptada a cualquier tamaño de pantalla.

# 3. Tecnologías
*   HTML5 (Enfoque en semántica: `<article>`, `<header>`, `<footer>`, `<aside>`)
*   CSS3 (Estilos personalizados: variables de color, tipografía y transiciones)
*   Bootstrap 5 (Layout: Navbar, Grid System `row/col`, Cards, Carousel, Ratio)
*   JavaScript (Variables básicas y operaciones en consola)
*   Git (Control de versiones, mínimo 5 commits)
*   GitHub (Alojamiento del repositorio)
*   IA utilizada: ChatGPT / Claude / Gemini (como tutor de apoyo)

---

# 4. Proceso con IA (Registro de Prompts)

| # | ¿Qué necesitábamos? | Prompt | ¿Qué respondió? | ¿Qué utilicé? | ¿Qué aprendí? |
|---|---|---|---|---|---|
| 1 | Planificar página y Layout Base | "Actúa como tutor web. Estoy creando un recomendador sobre La Vendicion con HTML y Bootstrap. Ayúdame a crear la estructura de 3 tarjetas usando la grilla. No uses CSS ni JS." | Me dio el código base de `<div class="row">` y `<div class="col-md-4">` con tarjetas estándar de Bootstrap. | Utilicé la lógica de las clases `col-md-4` y las clases de la tarjeta (`card`, `card-body`). | Aprendí que Bootstrap divide la pantalla en 12 columnas y 12/3 = 4. |
| 2 | Componente Carrusel | "Necesito hacer un carrusel de 4 imágenes para mi sección de historia usando solo Bootstrap, sin programar JS por mi cuenta." | Me entregó la estructura del componente Carousel con los atributos `data-bs-ride="carousel"`. | Usé toda la estructura de controles y contenedores, pero cambié los `div` internos por `<figure>`. | Aprendí que Bootstrap usa atributos `data-bs-*` para dar interactividad HTML sin tocar JS. |
| 3 | Video Responsivo | "Tengo un iframe de YouTube pero se deforma en celular. ¿Cómo lo hago responsivo solo con clases de Bootstrap?" | Me explicó el uso de las clases de proporción (Ratio). | Envolví mi iframe en un contenedor `<figure class="ratio ratio-16x9">`. | Comprendí que el framework puede calcular matemáticamente las proporciones (16:9) automáticamente. |
| 4 | JavaScript Variables | "Estoy aprendiendo JS. Dame un ejemplo de cómo guardar datos de un álbum usando variables de texto, número y booleanos, e imprimirlos en consola." | Me dio un ejemplo usando `let` y `console.log()` con concatenación de cadenas. | Tomé la estructura y creé mis propias variables (nombreAlbum, añoLanzamiento, etc.). | Entendí la diferencia de tipos de datos y cómo concatenar texto con variables numéricas. |

**¿Cuál fue el prompt más útil y por qué?**
El prompt 3 (Video Responsivo) fue el más útil. Yo intentaba usar `width="100%"` en el iframe, lo que arruinaba la altura. La IA me explicó el concepto de la clase `ratio` de Bootstrap, lo cual resolvió un problema complejo de diseño responsivo de forma muy elegante y con una sola línea de código.

---

# 5. Código generado vs. código propio

*   **¿Qué generó la IA?**
    La IA me proporcionó los "esqueletos" de las clases de Bootstrap (la estructura de las grillas, la sintaxis exacta del Navbar, las clases del Carrusel y las utilidades de flexbox como `d-flex` y `mt-auto`). También me dio el ejemplo de sintaxis para `console.log` en JS.
*   **¿Qué modificamos nosotros?**
    Yo escribí todo el contenido original (textos, reseñas, títulos, rutas de imágenes). Modifiqué profundamente el código de la IA para restaurar la semántica HTML5 (cambiando sus `<div>` genéricos por `<article>`, `<section>`, `<aside>` y `<figure>`). En CSS, desarrollé yo mismo el esquema de colores (rojo sangre y oscuro) y los efectos *hover*. En JavaScript, diseñé las variables específicas y las operaciones lógicas de mi temática.

---

# 6. Aprendizaje

**¿Qué concepto nuevo comprendí gracias a la IA?**
Comprendí la lógica matemática de los sistemas de grillas en el diseño web. Antes no entendía por qué a veces los elementos saltaban a la siguiente línea, pero al aprender que el límite es "12 columnas por fila", pude planificar mejor si quería tarjetas verticales (3 de 4 columnas) o tarjetas horizontales (1 imagen de 4 columnas + texto de 8 columnas).

---

# 7. Reflexión

**¿Hubo algún momento en que la IA generó código que no comprendía? ¿Qué hicimos?**
Sí. Cuando quise hacer que los botones de "Escuchar ahora" reprodujeran un sonido, la IA me generó una función de JavaScript que usaba `document.querySelector` y `.addEventListener('click', function() {...})`. 
Recordé la regla del documento: **PAUSA, PREGUNTA, COMPRENDE, DECIDE**. Al preguntarle, me explicó que eso era "Manipulación del DOM". Como aún no hemos visto ese tema en el bootcamp, decidí descartar ese código para no usar algo que no sé explicar por mí mismo. Resolví el requisito limitándome a usar `console.log` para mostrar la información del álbum, apegándome a mi nivel actual.
