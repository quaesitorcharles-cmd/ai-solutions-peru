# Preguntas sobre el Código — Evaluación Parcial
## AI Solutions Perú | Desarrollo Web IDAT Ciclo 1

> **Nota de verificación:** El guion de exposición **sí coincide** con el código real.
> Los elementos mencionados en el informe están presentes en los archivos HTML.
> Lo que sigue cubre *cada elemento* del código que el profesor puede señalar en pantalla.

---

## BLOQUE 1 — La declaración DOCTYPE y la etiqueta `<html>`

**P: ¿Qué significa `<!DOCTYPE html>` y por qué va al inicio?**
> Es la declaración del tipo de documento. Le dice al navegador que el archivo está escrito en HTML5. Debe ir en la primera línea, antes de cualquier otra cosa, para que el navegador entre en "modo estándar" y no en "modo quirks" (que es un modo de compatibilidad con páginas antiguas que renderiza de forma diferente).

**P: ¿Para qué sirve el atributo `lang="es"` en la etiqueta `<html>`?**
> Indica el idioma del contenido de la página. Los lectores de pantalla usan ese dato para pronunciar el texto correctamente (en español, no en inglés). También lo usan los motores de búsqueda y las herramientas de traducción automática del navegador, que detectan si el idioma de la página coincide con el del usuario y ofrecen traducirla.

---

## BLOQUE 2 — La sección `<head>`

**P: ¿Cuál es la diferencia entre `<head>` y `<header>`?**
> Son completamente distintas. `<head>` es invisible para el usuario: contiene metadatos, el título de la pestaña, el enlace al CSS y otros datos técnicos que el navegador necesita pero no muestra en pantalla. `<header>` es visible: es la etiqueta semántica que representa el encabezado visual de la página, donde va el logo y el menú.

**P: ¿Qué hace `<meta charset="UTF-8">`?**
> Define la codificación de caracteres del documento. UTF-8 es el estándar universal que incluye todos los caracteres de todos los idiomas: letras con tilde (á, é, ó, ú), ñ, signos de interrogación y exclamación invertidos (¿, ¡), y miles de símbolos más. Sin esta línea, esos caracteres podrían verse mal o como símbolos extraños.

**P: ¿Para qué sirve `<meta name="viewport" content="width=device-width, initial-scale=1.0">`?**
> Controla cómo se escala la página en dispositivos móviles. `width=device-width` indica que el ancho del área visible debe ser igual al ancho de la pantalla del dispositivo, en lugar del ancho de escritorio por defecto (que sería unos 980px). `initial-scale=1.0` establece el nivel de zoom inicial en 1, sin zoom. Sin esta línea, en un celular la página se vería muy pequeña y habría que hacer zoom para leerla.

**P: ¿Qué hace `<meta name="description">`?**
> Define la descripción corta de la página que aparece debajo del título en los resultados de Google. El navegador no la muestra en pantalla, pero es muy importante para el SEO. La escribí con las palabras clave principales del negocio: "soluciones de IA", "Lima", "Perú", "chatbots", para que la página aparezca cuando alguien busca esos términos.

**P: ¿Qué hace `<meta name="keywords">`?**
> Era muy usada antes para indicar las palabras clave de la página a los buscadores. Hoy en día Google ya no la toma en cuenta para el posicionamiento, porque se abusó de ella. La incluí de todas formas como buena práctica, aunque su impacto en SEO actual es mínimo.

**P: ¿Para qué sirve la etiqueta `<title>`?**
> Define el texto que aparece en la pestaña del navegador y como título en los resultados de búsqueda de Google. Es diferente del `<h1>` que el usuario ve en la página. En mi sitio usé el formato "Nombre de la página | AI Solutions Perú" para que en cada pestaña sea fácil identificar qué página es.

**P: ¿Cómo se vincula el CSS externo al HTML?**
> Con la etiqueta `<link>` dentro del `<head>`. El atributo `rel="stylesheet"` indica que es una hoja de estilos, y `href="css/styles.css"` es la ruta relativa al archivo. El navegador lo descarga y aplica los estilos antes de mostrar la página al usuario.

---

## BLOQUE 3 — El `<header>` y la navegación `<nav>`

**P: ¿Por qué el `<nav>` tiene el atributo `aria-label="Navegacion principal"`?**
> Porque puede haber múltiples elementos `<nav>` en una misma página (el menú principal, la paginación, el menú del footer). El atributo `aria-label` le da un nombre descriptivo a cada uno para que los lectores de pantalla puedan diferenciarlos y anunciarlos correctamente al usuario: "Navegación principal", en lugar de solo "Navegación".

**P: ¿Por qué algunos enlaces del menú tienen `class="activo"`?**
> Para marcar visualmente qué página está activa en el menú. En el CSS, la clase `activo` tiene un estilo diferente (como un subrayado o un color distinto) que le indica al usuario en qué página está. En cada archivo HTML, el enlace correspondiente a esa página es el que tiene esa clase.

**P: ¿Por qué el enlace de "Contacto" tiene una clase diferente (`btn-nav`) además de las otras?**
> Porque "Contacto" es la llamada a la acción principal del menú, visualmente destacada como un botón con fondo de color. La clase `btn-nav` en el CSS le da ese estilo de botón. Esto es una práctica común en diseño web: resaltar el CTA (Call to Action) más importante del menú.

**P: ¿Por qué el menú usa `<ul>` con `<li>` y `<a>` en lugar de solo poner los `<a>` directamente?**
> Porque semánticamente el menú de navegación es una lista de opciones, y la estructura correcta para una lista es `<ul>` (lista desordenada) con `<li>` para cada elemento. Esto también beneficia la accesibilidad: los lectores de pantalla anuncian "lista de 7 elementos" y el usuario puede navegar entre ellos más fácilmente.

---

## BLOQUE 4 — La sección `<section class="hero">`

**P: ¿Qué es la sección "hero" y por qué se llama así?**
> El "hero" es la sección principal de la página de inicio, la primera que ve el usuario al entrar. Se llama así en el mundo del diseño web porque es el elemento más prominente de la página: generalmente ocupa gran parte de la pantalla, tiene un mensaje corto e impactante y un botón de llamada a la acción. En mi caso tiene el eslogan de la empresa y dos botones.

**P: ¿Por qué usaste `<span>` dentro del `<h2>` del hero?**
> Para aplicar un color diferente solo a una parte del texto del título, sin crear un elemento de bloque nuevo. `<span>` es un contenedor en línea (inline) sin significado semántico propio, que sirve para aplicar estilos a una porción específica de texto dentro de otro elemento. En mi caso, la palabra "Inteligencia Artificial" dentro del h2 tiene el color cian del sitio.

**P: ¿Cuál es la diferencia entre `<a href="contacto.html" class="btn-primario">` y un `<button>`?**
> Un `<a>` con estilo de botón sirve para navegar a otra página o sección (es un enlace). Un `<button>` sirve para ejecutar una acción dentro de la misma página, como enviar un formulario. En el hero usé `<a>` con clase de botón porque "Solicitar Demo Gratis" lleva al usuario a contacto.html, es una navegación. El `<button type="submit">` del formulario sí es un botón real porque envía el formulario.

---

## BLOQUE 5 — Los `<article class="tarjeta">`

**P: ¿Por qué usaste `<article>` para las tarjetas de servicios y no `<div>` o `<section>`?**
> Porque `<article>` representa un bloque de contenido autónomo y completo en sí mismo: cada tarjeta de servicio tiene su propio título, descripción y enlace, y podría existir independientemente del resto de la página. `<section>` agrupa contenido relacionado dentro de la página, pero su contenido no necesariamente es autónomo. Y `<div>` no tiene ningún significado semántico.

**P: ¿Por qué hay una `<ul>` con `<li>` dentro de cada tarjeta de servicio?**
> Para listar las características de cada servicio como puntos. Es una lista desordenada `<ul>` porque el orden de las características no importa. Semánticamente es correcto representar una lista de características con `<ul>/<li>`, en lugar de separar los puntos con `<br>` o con párrafos individuales.

**P: ¿Qué hace `href="servicios.html#chatbots"` en el enlace "Saber más"?**
> La `#chatbots` es un ancla. El enlace lleva al usuario a la página servicios.html y además lo posiciona automáticamente en la sección que tiene `id="chatbots"`. Es como un enlace directo a una sección específica dentro de una página. El usuario no tiene que desplazarse manualmente hasta esa sección.

---

## BLOQUE 6 — La lista ordenada `<ol>`

**P: ¿Cuándo usaste `<ol>` en lugar de `<ul>` y por qué?**
> En la página de inicio, en la sección "¿Por qué elegirnos?", listé los 5 pasos del proceso: diagnóstico, propuesta, implementación, capacitación y soporte. Usé `<ol>` (lista ordenada) porque el orden de esos pasos importa: el diagnóstico siempre va primero, luego la propuesta, y así sucesivamente. Si el orden no importara, hubiera usado `<ul>`.

---

## BLOQUE 7 — `<figure>`, `<img>` y `<figcaption>`

**P: ¿Por qué envolviste las imágenes en `<figure>` y no las pusiste solas?**
> Porque `<figure>` es el contenedor semántico para contenido visual (imágenes, gráficos, videos) que tiene una relación con el contenido principal pero podría moverse sin afectar el flujo del texto. `<figcaption>` dentro del `<figure>` proporciona la descripción o leyenda de la imagen. Esta es la forma semánticamente correcta de poner imágenes con descripción, en lugar de poner un `<p>` o un `<span>` debajo de la imagen.

**P: ¿Qué hace el atributo `alt` en las imágenes? Dame un ejemplo del código real.**
> El atributo `alt` proporciona una descripción textual de la imagen que aparece cuando la imagen no carga, y que los lectores de pantalla leen en voz alta para describir la imagen a personas con discapacidad visual. En mi código, por ejemplo: `alt="Equipo de AI Solutions Perú trabajando en soluciones de inteligencia artificial"`. Es descriptivo, no genérico como "imagen" o "foto".

**P: ¿Para qué sirven los atributos `width` y `height` en las imágenes?**
> Para reservar el espacio que ocupará la imagen antes de que termine de cargarse. Así el navegador puede calcular el layout de la página desde el principio y el contenido no "salta" cuando la imagen aparece. También es bueno para el rendimiento porque evita el efecto de "salto de contenido" (CLS, Cumulative Layout Shift) que penaliza el posicionamiento en Google.

---

## BLOQUE 8 — La tabla de planes (`planes.html`)

**P: ¿Qué hace `<caption>` en la tabla?**
> Da un título a la tabla que aparece encima de ella y la describe semánticamente. En mi código dice "Comparativa de planes de AI Solutions Perú — vigencia 2026". Los lectores de pantalla la anuncian antes de empezar a leer la tabla para que el usuario sepa qué información va a encontrar.

**P: ¿Para qué sirve el atributo `scope="col"` en los `<th>` del `<thead>`?**
> Le indica a los lectores de pantalla que ese encabezado corresponde a toda la columna de abajo. Cuando el lector de pantalla llega a una celda de datos en el `<tbody>`, puede anunciar también el encabezado de su columna gracias al `scope`. Sin `scope`, el lector de pantalla no puede hacer esa asociación automáticamente en tablas más complejas.

**P: ¿Qué hace `colspan="4"` en el `<tfoot>`?**
> Hace que esa celda se extienda a lo ancho de 4 columnas, que es el número total de columnas de la tabla. Lo usé en el `<tfoot>` para que la nota aclaratoria sobre los precios ocupe toda la fila, ya que el texto es una nota general que aplica a todas las columnas, no solo a una.

**P: ¿Qué hace `class="plan-destacado"` en algunas celdas?**
> Es una clase CSS que aplico a todas las celdas de la columna "Pro" para resaltarla visualmente como el plan más recomendado. En el CSS esa clase tiene un fondo de color diferente que distingue esa columna del resto.

---

## BLOQUE 9 — La lista de definiciones `<dl>` en planes.html

**P: En el código de `planes.html` hay una sección con `<dl>`, `<dt>` y `<dd>`. ¿Qué es cada uno?**
> `<dl>` es una lista de descripción o definición. Dentro tiene pares de `<dt>` (definition term, el término) y `<dd>` (definition description, la descripción). En mi caso, cada `<dt>` es una pregunta frecuente y su `<dd>` es la respuesta. Es la estructura semánticamente más correcta para ese tipo de contenido pregunta-respuesta o término-definición.

---

## BLOQUE 10 — El formulario de `contacto.html`

**P: ¿Qué hace `action="#"` en la etiqueta `<form>`?**
> El atributo `action` indica a dónde se envían los datos del formulario cuando el usuario hace clic en enviar. El valor `#` es un placeholder: significa que el formulario no tiene un servidor real al que enviar datos, porque este es un sitio estático sin backend. En un proyecto real, aquí iría la URL del script del servidor que procesa el formulario.

**P: ¿Qué significa `method="post"` en el `<form>`?**
> Indica el método HTTP con el que se envían los datos. `post` envía los datos en el cuerpo de la petición HTTP, de forma que no se ven en la URL. Es el método correcto para formularios con datos sensibles como nombres, correos y mensajes. El otro método es `get`, que añade los datos a la URL y se usa para búsquedas.

**P: ¿Cuál es la diferencia entre `<fieldset>` y `<legend>`?**
> `<fieldset>` agrupa campos relacionados dentro de un formulario y dibuja un borde alrededor de ellos. `<legend>` es el título de ese grupo y aparece en el borde superior del fieldset. En mi formulario hay tres fieldsets: "Datos Personales", "Sobre tu Empresa" y "¿Cómo podemos ayudarte?". Mejoran la organización visual y la accesibilidad porque los lectores de pantalla anuncian el legend al entrar a cada grupo.

**P: ¿Por qué algunos inputs tienen el atributo `required`?**
> Porque son campos obligatorios. Con el atributo `required`, el navegador valida automáticamente que el campo no esté vacío antes de permitir enviar el formulario. Si el usuario intenta enviar sin llenarlo, el navegador muestra un mensaje de error. Esto es validación del lado del cliente, que es más rápida para el usuario aunque no reemplaza la validación del servidor.

**P: ¿Qué diferencia hay entre `type="text"`, `type="email"`, `type="tel"` y `type="number"` en los inputs?**
> El tipo le indica al navegador qué clase de dato espera el campo. `text` acepta cualquier texto sin validación. `email` valida que lo escrito tenga formato de correo electrónico (que contenga @ y dominio) antes de permitir enviar. `tel` en móviles abre el teclado numérico del teléfono. `number` solo acepta números y muestra flechas para incrementar o decrementar el valor. En mi formulario también usé los atributos `min="0"` y `step="50"` en el campo de presupuesto para limitar los valores válidos.

**P: ¿Para qué sirve el atributo `placeholder` en un input?**
> Muestra un texto de ejemplo dentro del campo cuando está vacío, para orientar al usuario sobre qué debe escribir. Por ejemplo, `placeholder="Ej: Juan García Pérez"` en el campo de nombre, o `placeholder="tucorreo@empresa.com"` en el campo de email. El texto desaparece cuando el usuario empieza a escribir. No reemplaza al `<label>`, que siempre debe estar presente.

**P: ¿Cuál es la diferencia entre `<input>` y `<textarea>`?**
> `<input>` es para texto en una sola línea. `<textarea>` es para texto multilínea, como el campo de mensaje del formulario. `<textarea>` también puede tener el atributo `maxlength` para limitar la cantidad de caracteres, que en mi código usé con un valor de 1000.

**P: ¿Para qué sirve `<select>` con `<option>`?**
> `<select>` crea un menú desplegable de opciones. Cada `<option>` es una opción dentro de ese menú. El atributo `value` de cada `<option>` es el valor que se envía al servidor cuando el usuario selecciona esa opción; el texto entre las etiquetas es lo que el usuario ve en pantalla. En mi formulario lo usé para el país, el sector, los empleados, el servicio y cómo nos encontraron.

**P: ¿Por qué la primera opción de cada `<select>` tiene `value=""`?**
> Es una opción vacía que sirve como instrucción de selección: "— Selecciona tu país —". El value vacío hace que, si el `<select>` tiene el atributo `required`, el formulario no se pueda enviar hasta que el usuario elija una opción real. Es una práctica común para forzar al usuario a hacer una selección consciente.

**P: ¿Por qué hay un `<button type="submit">` y no un `<input type="submit">`?**
> Ambos envían el formulario, pero `<button>` permite poner HTML dentro (texto, iconos, spans con estilos), mientras que `<input type="submit">` solo acepta texto plano. Usé `<button type="submit">` porque quería poder darle estilo más fácilmente y poner el texto del botón con la flecha "→" al final.

---

## BLOQUE 11 — El `<video>` y el `<audio>` en `nosotros.html`

**P: Muéstrame el código del video. ¿Para qué sirve cada atributo?**
> El código es:
> ```html
> <video width="700" height="394" controls
>        poster="https://placehold.co/700x394/...?text=Video">
>     <source src="media/video-institucional.mp4" type="video/mp4">
>     Tu navegador no soporta la reproducción de video HTML5.
> </video>
> ```
> - `width` y `height`: dimensiones en píxeles del reproductor.
> - `controls`: muestra los controles nativos del navegador (play, pausa, volumen, barra de progreso).
> - `poster`: imagen que se muestra antes de que el usuario reproduzca el video, como una miniatura.
> - `<source src type>`: indica el archivo de video y su tipo MIME para que el navegador sepa cómo decodificarlo.
> - El texto "Tu navegador no soporta..." es el contenido de respaldo que se muestra si el navegador no puede reproducir el video.

**P: ¿Por qué usas `<source>` dentro de `<video>` en lugar de poner `src` directamente en `<video>`?**
> Usando `<source>` como elemento hijo se pueden poner múltiples fuentes con diferentes formatos, por ejemplo MP4 y WebM. El navegador prueba cada `<source>` en orden y usa el primero que pueda reproducir. Esto mejora la compatibilidad: si el navegador no soporta MP4, prueba con WebM. En mi caso solo tengo una fuente pero la estructura con `<source>` es la más correcta y escalable.

---

## BLOQUE 12 — El `<iframe>` del mapa en `contacto.html`

**P: ¿Qué hace `<iframe>` y para qué lo usaste?**
> `<iframe>` incrusta un documento HTML externo dentro de la página actual. En mi caso lo usé para mostrar el mapa de Google Maps en la página de Contacto, usando el código de embebido que proporciona Google Maps. El mapa aparece dentro del sitio sin necesidad de que el usuario salga de la página.

**P: ¿Para qué sirve el atributo `title` en el `<iframe>`?**
> Para la accesibilidad. Sin `title`, un lector de pantalla llegaría al iframe y no sabría qué contiene. Con `title="Ubicación de AI Solutions Perú en San Isidro, Lima"`, el lector de pantalla puede anunciar correctamente el propósito del iframe cuando el usuario navega hasta él con el teclado.

**P: ¿Para qué sirve `allowfullscreen` en el iframe?**
> Permite que el mapa de Google Maps se pueda ver en pantalla completa. Sin este atributo, el botón de pantalla completa del mapa estaría deshabilitado. Es un permiso que el documento padre le otorga al iframe.

---

## BLOQUE 13 — El `<footer>` y la etiqueta `<address>`

**P: ¿Por qué usaste `<address>` en el footer?**
> Porque `<address>` es la etiqueta semántica específica para información de contacto. En el contexto del `<footer>`, representa los datos de contacto de la empresa: dirección física, teléfono y correo electrónico. El significado semántico de `<address>` hace que los motores de búsqueda y lectores de pantalla identifiquen esa información como datos de contacto, lo cual puede aparecer en los resultados de búsqueda de Google como datos estructurados.

**P: ¿Qué hace `<a href="tel:+5119876543">`?**
> Es un enlace de teléfono. En dispositivos móviles, cuando el usuario toca ese enlace, el celular ofrece marcarlo directamente. El prefijo `tel:` le indica al navegador que es un número de teléfono. En escritorio generalmente abre la aplicación de teléfono si hay una configurada.

**P: ¿Qué hace `<a href="mailto:info@aisolutionsperu.com">`?**
> Es un enlace de correo electrónico. Cuando el usuario hace clic, el sistema operativo abre el cliente de correo predeterminado (Outlook, Thunderbird, Gmail) con ese correo ya puesto como destinatario. El prefijo `mailto:` le indica al navegador que es una dirección de email.

**P: ¿Por qué algunos enlaces del footer tienen `target="_blank"`?**
> Para que se abran en una pestaña nueva del navegador. Lo usé en los enlaces a redes sociales externas (LinkedIn, Instagram, YouTube, WhatsApp). La razón es que al abrir un sitio externo en la misma pestaña, el usuario abandona el sitio. Con `target="_blank"` el sitio externo se abre en una pestaña nueva y el usuario puede volver fácilmente al sitio original.

**P: ¿Qué es `&copy;` en el footer?**
> Es una entidad HTML que representa el símbolo de copyright ©. En HTML ciertos caracteres especiales tienen que escribirse como entidades para que el navegador los interprete correctamente y no los confunda con código. `&copy;` es el código estándar para el símbolo de derechos de autor.

---

## BLOQUE 14 — Clases CSS y estructura de `<div>`

**P: ¿Para qué sirve `<div class="contenedor">`? ¿Por qué aparece en casi todas las secciones?**
> El `<div class="contenedor">` es un contenedor que en el CSS tiene un `max-width` y `margin: auto` que centra el contenido horizontalmente y limita su ancho máximo (por ejemplo, a 1100px). Sin ese div, el contenido se extendería de borde a borde en pantallas anchas, lo que lo haría difícil de leer. Es una técnica estándar de diseño web llamada "contenedor centrado".

**P: ¿Para qué sirve `<div class="grid-articulos">`?**
> Es un div al que en el CSS le aplico `display: flex` con `flex-wrap: wrap`. Sirve como contenedor de las tarjetas, y el flexbox hace que las tarjetas se organicen automáticamente en filas y columnas según el espacio disponible.

**P: ¿Para qué sirve `<div class="titulo-seccion">`?**
> Agrupa el h2, la línea decorativa y el subtítulo de cada sección para darles un estilo coherente en todas las páginas. En el CSS les aplico el mismo centrado y espaciado. Es un patrón de diseño que uso consistentemente en todas las secciones.

**P: ¿Para qué sirve `<div class="linea-color">`?**
> Es un div vacío que en el CSS tiene un ancho pequeño, una altura de pocos píxeles y un background-color con el color cian del sitio. Funciona como un separador visual decorativo debajo de cada título de sección. Se usa bastante en diseño web moderno como acento visual.

---

## BLOQUE 15 — Verificación del guion vs código

**¿El guion coincide con el código?**

Sí, con los siguientes matices:

1. **Los colores** — el guion menciona #7C3AED (violeta), #06B6D4 (cian) y #0F172A (azul oscuro). Esos son exactamente los valores que aparecen en el código HTML en los `placehold.co` y corresponden al CSS.

2. **Los 8 HTML** — el guion los menciona y todos existen: index.html, servicios.html, planes.html, casos.html, nosotros.html, blog.html, contacto.html, sitemap.html.

3. **El formulario** — el guion menciona 3 fieldsets. El código tiene exactamente 3: "Datos Personales", "Sobre tu Empresa" y "¿Cómo podemos ayudarte?".

4. **Los tipos de input** — el guion menciona text, email, tel, number, select y textarea. El código tiene todos esos más `<button type="submit">`.

5. **La tabla** — el guion menciona thead, tbody, tfoot y scope="col". Todo está en el código de planes.html.

6. **El video** — el guion menciona el atributo `poster`. El código lo tiene: `poster="https://placehold.co/700x394/..."`.

7. **El iframe** — el guion menciona el atributo `title`. El código lo tiene: `title="Ubicación de AI Solutions Perú en San Isidro, Lima"`.

8. **Una cosa adicional no mencionada en el guion:** el formulario también tiene un campo `<select id="pais">` (país) que no fue mencionado en el informe. Si el profesor lo señala: "Lo agregué para capturar en qué país está el cliente, ya que la empresa atiende toda Latinoamérica. No lo mencioné en el informe porque quise resumir los tipos principales."

---

*Preparado con base en la lectura directa de los archivos del proyecto.*
