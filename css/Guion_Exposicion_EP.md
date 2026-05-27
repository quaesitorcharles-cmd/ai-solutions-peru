# Guion de Exposición — Evaluación Parcial
## Desarrollo Web · AI Solutions Perú
### Estudiante: Carlos Eduardo | Docente: Franz Chuje Panaifo | IDAT Ciclo 1

---

# PARTE 1: GUION PARA EXPONER

---

## APERTURA (30–40 segundos)

> "Buenos días / Buenas tardes. Mi nombre es Carlos Eduardo y voy a presentar mi propuesta de sitio web estático para una empresa llamada AI Solutions Perú, una empresa ficticia dedicada a ofrecer soluciones de Inteligencia Artificial a empresas en Lima y Latinoamérica."

> "El sitio fue construido completamente con HTML5 y una hoja de estilos CSS externa. No usé ningún framework ni librería adicional, solo un editor de texto."

> "Voy a presentar el proyecto siguiendo la estructura del informe: primero el contexto del negocio, luego los fundamentos web, después el HTML5 utilizado y finalmente el CSS."

---

## SECCIÓN 1 — PRESENTACIÓN DEL PROYECTO (1–2 minutos)

> "Elegí una empresa de Inteligencia Artificial porque me permitía justificar de manera natural el uso de todos los elementos que pide el curso."

> "Por ejemplo, los planes de precios de la empresa encajan perfectamente con una tabla HTML comparativa. Los servicios que ofrece la empresa se listan usando listas y tarjetas. El formulario de contacto permite captar clientes. Y la página 'Nosotros' tiene video y audio, porque una empresa de tecnología podría tener un video institucional y un podcast."

**Mostrar o mencionar las 8 páginas:**

| Página | Archivo |
|--------|---------|
| Inicio | index.html |
| Servicios | servicios.html |
| Planes | planes.html |
| Casos de Éxito | casos.html |
| Nosotros | nosotros.html |
| Blog | blog.html |
| Contacto | contacto.html |
| Mapa del Sitio | sitemap.html |

> "Todas las páginas comparten el mismo header con el menú de navegación y el mismo footer. Esto fue posible gracias a un único archivo CSS externo: cualquier cambio en styles.css se refleja automáticamente en las 8 páginas."

---

## SECCIÓN 2 — FUNDAMENTOS WEB (2–3 minutos)

### 2.1 Navegadores

> "Durante el desarrollo probé el sitio principalmente en Chrome y Edge, que usan el mismo motor de renderizado: Blink. También consideré Firefox, que usa Gecko, y Safari, que usa WebKit para dispositivos Apple. Para asegurar compatibilidad evité propiedades CSS experimentales y me limité a HTML5 estándar."

### 2.2 Dominio y Hosting

> "Para el dominio elegí aisolutionsperu.com. Escogí la extensión .com porque tiene mayor reconocimiento internacional que las extensiones regionales, y el nombre incluye las palabras clave de la empresa, lo que ayuda al posicionamiento en buscadores."

> "En cuanto al hosting, para una fase inicial recomendaría un hosting compartido, porque el sitio es estático y no tiene base de datos. El costo estaría entre 3 y 8 dólares mensuales. Proveedores como Hostinger o SiteGround ofrecen certificado SSL gratuito, lo que activa el HTTPS y mejora la confianza del visitante."

### 2.3 Mapa del Sitio

> "El sitio tiene una arquitectura plana: todas las páginas están al mismo nivel y se puede llegar a cualquiera desde el menú principal. Esto reduce el número de clics que necesita el usuario para encontrar lo que busca."

> "Además, incluí una página sitemap.html que lista todas las páginas del sitio. Sirve tanto para que el usuario se oriente como para que los motores de búsqueda puedan indexar el sitio más fácilmente."

### 2.4 Elementos Gráficos

> "La paleta del sitio combina violeta #7C3AED, azul oscuro #0F172A y cian #06B6D4. Elegí estos colores porque transmiten tecnología, innovación y confianza, que son los valores de una empresa de IA."

> "Para las imágenes usé JPG y PNG. JPG para fotografías porque ocupa menos espacio. PNG para el logo porque soporta fondo transparente. El video es MP4, el audio es MP3, y para el mapa de contacto usé un iframe de Google Maps."

---

## SECCIÓN 3 — HTML5 EN EL SITIO (3–4 minutos)

### 3.1 Etiquetas Semánticas

> "La decisión central del proyecto fue priorizar etiquetas semánticas sobre el uso genérico de div. Las etiquetas semánticas le dan significado al contenido, no solo estructura visual."

> "Usé header para el encabezado de cada página, que contiene el logo y el menú. Usé nav dentro del header exclusivamente para el menú de navegación. Usé main para envolver el contenido principal de cada página. Usé section para separar las distintas partes temáticas y article para cada bloque de contenido autónomo, como las tarjetas de servicios o los testimonios."

> "También usé aside para los bloques de llamada a la acción, footer para el pie de página, figure y figcaption para las imágenes con descripción, blockquote y cite en la página de Casos de Éxito para las citas textuales de clientes, y address para los datos de contacto."

> "Un caso particular es la lista de preguntas frecuentes: usé dl, dt y dd, que es la lista de definiciones de HTML. La pregunta es el dt y la respuesta es el dd."

> "Respecto a los encabezados, usé h1 solo para el nombre de la empresa, h2 para los títulos de cada sección, h3 para subtítulos internos y h4 para elementos secundarios. Es importante no saltar niveles para mantener la jerarquía."

### 3.2 Accesibilidad

> "La accesibilidad permite que el sitio sea usable por personas con discapacidades visuales, auditivas o motrices. Apliqué cuatro prácticas básicas:"

> "Primero, el atributo lang='es' en la etiqueta html de cada página, para que los lectores de pantalla sepan en qué idioma está el contenido. Segundo, el atributo alt en todas las imágenes, con una descripción textual. Tercero, etiquetas label vinculadas a cada campo del formulario usando el atributo for que coincide con el id del input. Y cuarto, mantener la jerarquía de encabezados en orden, de h1 a h4 sin saltar niveles."

### 3.3 Elementos Complejos: Tabla, Formulario y Multimedia

> "En planes.html construí una tabla comparativa con la estructura completa: thead para los encabezados, tbody para los datos y tfoot para una nota al pie sobre los precios. Usé el atributo scope='col' en los th para que los lectores de pantalla puedan asociar cada celda con su columna."

> "El formulario de contacto tiene tres secciones organizadas con fieldset y legend: datos personales, información de la empresa y el mensaje. Usé varios tipos de input: text, email, tel, number, además de select y textarea. Cada label está vinculado a su input con el atributo for."

> "En la página Nosotros puse un video con la etiqueta video, con el atributo poster para mostrar una imagen antes de reproducir, y con la etiqueta source adentro. También hay un audio para el podcast, de la misma manera. Y en Contacto tengo un iframe de Google Maps con el atributo title para que los lectores de pantalla lo anuncien correctamente."

---

## SECCIÓN 4 — HOJA DE ESTILOS CSS (1–2 minutos)

> "Todo el diseño del sitio vive en un solo archivo: css/styles.css. No usé estilos en línea ni etiquetas style dentro del HTML, cumpliendo con el requisito del curso de CSS externo."

> "Organicé el archivo en bloques comentados: reset, header, navegación, secciones, botones, tarjetas, tablas, formulario, footer y media queries. Esto hace el archivo más fácil de leer y mantener. Actualmente supera las 700 líneas."

> "Para las tarjetas de servicios y el equipo usé display flex con flex-wrap wrap. Esto permite que las tarjetas se acomoden automáticamente según el ancho de la pantalla, sin tener que calcular columnas fijas."

> "Para móviles incluí una media query con max-width de 768px. Dentro de ella el header pasa a disposición vertical, el menú permite saltos de línea y el título del hero se reduce. Es una solución básica pero suficiente para que el sitio no se rompa en pantallas pequeñas."

---

## CIERRE (30 segundos)

> "Como mejoras futuras, me gustaría reemplazar las imágenes de relleno por fotografías reales e implementar un menú hamburguesa para móviles, lo que requeriría incorporar JavaScript en una siguiente versión."

> "El principal aprendizaje de este proyecto fue confirmar la utilidad de un único archivo CSS para todas las páginas: cualquier cambio se propaga inmediatamente a las 8 páginas, lo que evita inconsistencias y facilita el mantenimiento."

> "Eso es todo. Quedo a disposición para cualquier pregunta."

---
---

# PARTE 2: POSIBLES PREGUNTAS DEL PROFESOR

*Organizadas por tema, con tu respuesta sugerida.*

---

## BLOQUE A — Preguntas sobre los Fundamentos Web

**P1: ¿Por qué elegiste el dominio .com y no .pe?**
> Porque .com tiene mayor reconocimiento internacional. Al ser una empresa que quiere llegar a toda Latinoamérica, .com proyecta más alcance que una extensión regional como .pe, que es más apropiada para negocios exclusivamente peruanos.

**P2: ¿Qué diferencia hay entre un hosting compartido y un VPS?**
> En el hosting compartido, el servidor físico es compartido entre muchos clientes y los recursos (CPU, RAM, almacenamiento) se distribuyen entre todos. Es más barato pero puede ser más lento si otros sitios consumen muchos recursos. Un VPS es un servidor virtual privado: aunque físicamente se comparte la máquina, el sistema operativo y los recursos están aislados, lo que da más control y rendimiento. Para un sitio estático sin mucho tráfico, el hosting compartido es suficiente e ideal por su costo.

**P3: ¿Qué es el SSL y para qué sirve?**
> SSL es el protocolo que permite cifrar la comunicación entre el navegador del usuario y el servidor. Cuando un sitio tiene SSL activo, la URL empieza con HTTPS en lugar de HTTP y aparece el candado en el navegador. Esto protege los datos que el usuario envía, como los que llena en el formulario de contacto, y también genera confianza. Hoy en día los navegadores marcan como "no seguro" los sitios sin SSL.

**P4: ¿Cuál es la diferencia entre un mapa del sitio para el usuario y un sitemap XML para buscadores?**
> El sitemap.html que yo hice es para el usuario: es una página en HTML que lista todas las páginas del sitio de forma visual y navegable. El sitemap.xml es un archivo técnico en formato XML dirigido a los motores de búsqueda como Google. Contiene las URLs del sitio con metadatos como la fecha de última modificación, para que los bots de búsqueda puedan rastrear e indexar el contenido más eficientemente. En mi proyecto solo implementé el primero, el visual.

**P5: ¿Por qué elegiste Chrome y Edge como navegadores principales para probar?**
> Porque ambos usan el motor de renderizado Blink, que es el más extendido actualmente. Chrome tiene la mayor cuota de mercado global y Edge es el navegador que viene por defecto en Windows, que es el sistema operativo más común. Probar en ambos garantiza que el sitio funciona bien para la mayoría de usuarios. También tomé en cuenta Firefox (Gecko) y Safari (WebKit), aunque no los usé activamente para el desarrollo.

**P6: ¿Qué significa que tu sitio es estático?**
> Un sitio estático es aquel en el que las páginas ya existen como archivos HTML listos, y el servidor simplemente las entrega al navegador sin procesarlas. No hay base de datos ni lenguaje de servidor que genere el contenido al vuelo. En mi caso, las 8 páginas son archivos .html fijos. Un sitio dinámico, en cambio, genera el HTML en el momento de la solicitud usando lenguajes como PHP o Python y consultas a una base de datos.

---

## BLOQUE B — Preguntas sobre HTML5

**P7: ¿Por qué es importante usar etiquetas semánticas en lugar de solo usar div?**
> Porque las etiquetas semánticas le dan significado al contenido. Un div no dice nada sobre lo que contiene. En cambio, un header indica que ahí está el encabezado, un nav indica navegación, un main indica el contenido principal. Esto beneficia a tres cosas: la accesibilidad (los lectores de pantalla entienden mejor la estructura), el SEO (los motores de búsqueda dan más valor al contenido correctamente marcado) y el mantenimiento del código (es mucho más fácil de leer y modificar).

**P8: ¿Cuál es la diferencia entre section y article?**
> Section agrupa contenido relacionado temáticamente dentro de una página, pero ese contenido no tiene sentido fuera del contexto del sitio. Article, en cambio, es un bloque de contenido autónomo que podría existir independientemente: una noticia, un artículo de blog, una tarjeta de producto. En mi sitio usé section para delimitar las áreas de cada página (como "servicios" o "equipo") y article para cada tarjeta de servicio individual o cada testimonio de cliente.

**P9: ¿Para qué sirve el atributo scope en una tabla?**
> El atributo scope en una celda th indica si ese encabezado corresponde a una columna (scope="col") o a una fila (scope="row"). Esto es importante para la accesibilidad: cuando un lector de pantalla lee una celda de datos, puede anunciar también el encabezado al que pertenece gracias al scope. Sin este atributo, una persona que usa lector de pantalla podría no entender qué columna o fila corresponde a cada dato.

**P10: ¿Cuál es la diferencia entre thead, tbody y tfoot en una tabla?**
> Son tres secciones lógicas de la tabla. thead contiene las filas de encabezado, tbody contiene los datos principales y tfoot contiene los datos del pie, como totales o notas aclaratorias. Además de organizar semánticamente el contenido, tienen una ventaja práctica: si la tabla es muy larga y se imprime, el thead y el tfoot se repiten en cada página impresa automáticamente.

**P11: ¿Por qué vinculaste cada label con su input y cómo se hace?**
> Vinculé cada label con su input usando el atributo for en el label y el atributo id en el input, ambos con el mismo valor. Por ejemplo, `<label for="nombre">` y `<input id="nombre">`. Esto tiene dos beneficios: primero, si el usuario hace clic en el texto del label, el cursor salta automáticamente al campo de entrada, lo cual mejora la usabilidad especialmente en móviles. Segundo, los lectores de pantalla anuncian el texto del label cuando el usuario llega al campo con el teclado.

**P12: ¿Qué hace el atributo poster en la etiqueta video?**
> El atributo poster indica la URL de una imagen que se muestra como portada del video antes de que el usuario lo reproduzca. Si no se incluye, el navegador muestra el primer fotograma del video, que puede ser negro o una imagen poco atractiva. Con poster puedo mostrar una imagen representativa del contenido mientras el video no está reproduciéndose.

**P13: ¿Qué diferencia hay entre ol, ul y dl?**
> ol es una lista ordenada (numerada), se usa cuando el orden de los elementos importa, como los pasos de un proceso. ul es una lista desordenada (con viñetas), se usa cuando el orden no importa, como una lista de servicios. dl es una lista de definiciones o descripción, que tiene pares de término (dt) y definición (dd). La usé para las preguntas frecuentes: la pregunta es el dt y la respuesta el dd.

**P14: ¿Por qué pusiste el atributo title en el iframe del mapa?**
> Para la accesibilidad. Un iframe carga contenido externo embebido, y sin el atributo title, un lector de pantalla no puede describir qué hay dentro del iframe. Al poner title="Mapa de ubicación de AI Solutions Perú", el lector de pantalla puede anunciarlo correctamente cuando el usuario navega por teclado hasta el mapa.

---

## BLOQUE C — Preguntas sobre CSS

**P15: ¿Por qué usaste un solo archivo CSS para las 8 páginas?**
> Porque el CSS externo permite la separación de responsabilidades: el HTML se encarga de la estructura y el CSS de la presentación. Al tener un único archivo, cualquier cambio en el diseño (como modificar un color o un tamaño de fuente) se aplica automáticamente a todas las páginas. Si tuviera CSS dentro de cada HTML, tendría que repetir el mismo cambio 8 veces, lo que aumenta el riesgo de inconsistencias y hace el mantenimiento más difícil.

**P16: ¿Cómo funciona display: flex y por qué lo usaste para las tarjetas?**
> Flexbox es un modelo de diseño CSS que organiza los elementos hijos de un contenedor en una fila o columna, distribuyendo el espacio de manera flexible. Lo usé con flex-wrap: wrap para las tarjetas de servicios y del equipo. Esto hace que las tarjetas se coloquen en fila cuando hay espacio suficiente y bajen a la siguiente fila automáticamente cuando la pantalla es más angosta. Es más práctico que calcular columnas fijas con porcentajes.

**P17: ¿Qué es una media query y para qué sirve?**
> Una media query es una condición en CSS que aplica estilos solo cuando se cumple cierta condición, generalmente relacionada con el tamaño de la pantalla. Usé @media (max-width: 768px) para aplicar estilos específicos cuando la pantalla es de 768 píxeles o menos, que es aproximadamente el ancho de una tableta o un teléfono. Dentro de esa media query cambié el header a disposición vertical, permití que el menú haga saltos de línea y reduje el tamaño del título del hero.

**P18: ¿Qué hace el reset CSS al inicio de tu hoja de estilos?**
> El reset CSS elimina o estandariza los estilos que cada navegador aplica por defecto. Por ejemplo, Chrome y Firefox pueden aplicar márgenes o rellenos diferentes a elementos como h1, p o ul. Al poner un reset al inicio, parto desde una base uniforme en todos los navegadores y puedo aplicar mis propios estilos sin que los valores por defecto interfieran de manera inesperada.

**P19: ¿Cuál es la diferencia entre padding y margin?**
> Margin es el espacio exterior de un elemento, es decir, la distancia entre ese elemento y los elementos vecinos. Padding es el espacio interior, es decir, la distancia entre el borde del elemento y su contenido. Si aplico un color de fondo, el padding se ve afectado por ese color pero el margin no.

---

## BLOQUE D — Preguntas de AUTORÍA (las que el profesor hace para verificar que fue el estudiante quien hizo el trabajo)

*Estas preguntas apuntan a detalles específicos que solo conoce quien hizo el trabajo. Prepárate para responderlas con naturalidad y sin dudar.*

**P20: ¿Qué fue lo más difícil de hacer en este proyecto?**
> Lo que más me costó fue el CSS, especialmente entender cómo funcionaba el layout con flexbox y alinear los elementos correctamente. El HTML fue más directo una vez que entendí para qué sirve cada etiqueta. El formulario también me tomó tiempo extra para entender bien la relación entre fieldset, legend y la vinculación de los labels con los inputs.

**P21: ¿En qué orden construiste el sitio? ¿Por dónde empezaste?**
> Antes de escribir código, esbocé en papel cómo iba a quedar la página principal. Luego empecé por el index.html y el styles.css de forma simultánea, porque el header y el footer son compartidos. Una vez que tuve esa base lista, construí el resto de páginas en este orden aproximado: servicios, planes, nosotros, contacto, casos de éxito, blog y finalmente sitemap.

**P22: ¿Cuántas líneas tiene tu CSS aproximadamente?**
> El archivo styles.css supera las 700 líneas. Lo organicé en bloques comentados: reset, header, navegación, secciones, botones, tarjetas, tablas, formulario, footer y media queries.

**P23: ¿Qué colores usaste y por qué esos específicamente?**
> Usé tres colores principales: violeta #7C3AED para los elementos principales como botones y títulos, cian #06B6D4 para los efectos hover y los detalles, y azul oscuro #0F172A para el header y el footer. Elegí esa paleta porque transmite tecnología e innovación, valores que se alinean con una empresa de Inteligencia Artificial. El gris claro #F8FAFC lo usé como fondo alternado para algunas secciones.

**P24: ¿Por qué usaste imágenes de placehold.co y no imágenes reales?**
> Porque AI Solutions Perú es una empresa ficticia creada para la evaluación, así que no existen fotografías reales de sus instalaciones o equipo. Placehold.co genera imágenes de relleno con texto y tamaño configurables, que funcionan perfectamente como marcadores de posición. En una implementación real, esas imágenes se reemplazarían por fotografías propias de la empresa.

**P25: ¿Qué cambiarías o mejorarías si tuvieras más tiempo?**
> Principalmente dos cosas. Primero, implementar un menú hamburguesa para móviles, que requeriría JavaScript para mostrar y ocultar el menú al hacer clic. Segundo, sustituir las imágenes de relleno por imágenes reales con diseño más cuidado. También me gustaría profundizar en propiedades CSS como box-shadow y linear-gradient, que las usé basándome en tutoriales pero aún no las domino completamente.

**P26: Muéstrame dónde está el fieldset en tu formulario. ¿Qué contiene?**
> El formulario de contacto en contacto.html tiene tres fieldset: el primero agrupa los campos de datos personales (nombre, apellido, correo, teléfono), el segundo agrupa la información de la empresa (nombre de la empresa, sector y número de empleados) y el tercero tiene el textarea del mensaje y el botón de enviar. Cada fieldset tiene su legend con el título de esa sección.

**P27: ¿Cuántos tipos de input distintos usaste en el formulario?**
> Usé: text para nombre y apellido, email para el correo electrónico, tel para el teléfono, number para el número de empleados, select para el sector de la empresa, textarea para el mensaje y submit para el botón de envío. Son 7 tipos distintos contando el botón.

**P28: ¿Dónde usaste blockquote y por qué ahí y no en otro lugar?**
> Lo usé en la página casos.html, que es la página de testimonios de clientes. Blockquote está diseñado semánticamente para citas textuales de otra persona o fuente. Como los testimonios son frases que dicen los clientes de la empresa, el uso de blockquote es el correcto. Dentro del blockquote puse la cita y debajo un cite con el nombre del cliente y su cargo.

**P29: ¿Qué hace la etiqueta aside en tu sitio?**
> La usé para los bloques de llamada a la acción que aparecen al final de varias páginas, como el bloque que dice "¿Listo para empezar?" con un botón para ir a contacto. Aside es para contenido relacionado pero secundario respecto al contenido principal de la página. Ese bloque no es parte central del contenido, es complementario, por eso lo puse en aside.

**P30: ¿Por qué usaste dl, dt y dd para las preguntas frecuentes?**
> Porque la lista de definiciones de HTML es la más apropiada semánticamente para ese tipo de contenido. En las preguntas frecuentes tengo un par pregunta-respuesta, que es exactamente lo que representa dl: una lista de términos (dt, la pregunta) con sus respectivas definiciones o respuestas (dd). Usar una ol o una ul no representaría correctamente esa relación semántica entre la pregunta y la respuesta.

---

## BLOQUE E — Preguntas conceptuales avanzadas (para nota sobresaliente)

**P31: ¿Cuál es la diferencia entre HTML y HTML5?**
> HTML5 es la versión más reciente del lenguaje, estandarizada en 2014. Sus principales novedades respecto a versiones anteriores son las etiquetas semánticas como header, nav, main, section, article, footer y aside, que antes no existían y se usaban divs para todo. También incorpora nativamente las etiquetas audio y video, antes se necesitaba un plugin como Flash. Y añade el tipo de doctype simplificado: solo `<!DOCTYPE html>`.

**P32: ¿Qué es el SEO y cómo lo tomaste en cuenta en tu sitio?**
> SEO es la optimización para motores de búsqueda. Lo tomé en cuenta de varias formas: eligiendo un dominio con palabras clave (aisolutionsperu.com), usando etiquetas semánticas que los buscadores valoran, manteniendo una jerarquía de encabezados coherente (h1 para el nombre de la empresa, h2 para las secciones principales), poniendo alt en todas las imágenes y creando una página sitemap.html. Estas son buenas prácticas básicas de SEO.

**P33: Si tuvieras que agregar una novena página en el futuro, ¿qué necesitarías hacer?**
> Crear el archivo .html de la nueva página, copiar el header y el footer de cualquiera de las páginas existentes, agregar el enlace a la nueva página en el menú de navegación en todas las páginas, y agregar la página a la lista en sitemap.html. Como el CSS ya está en styles.css, la nueva página heredaría automáticamente todos los estilos. No habría que modificar el CSS salvo que la nueva página tenga elementos visuales nuevos.

---

*Preparado en base al informe Informe_EP_Carlos_v3.docx y la rúbrica EP.*
