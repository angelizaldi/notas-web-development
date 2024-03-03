# HTML

_Hyper Text Markup  Language_ (HTML) Es un lenguaje de marcado (_markup  language_) para  la creación de páginas web. Principalmente funciona para describir la estructura de la pagína web y definir sus elementos indicando a los navegadores cómo mostrar el contenido.

La página principal de una página web normalmente se llama "_index.html_". Es recomendado usar ese nombre.

Los documentos html terminan con la extencioón `.htm` o `.html`.

## Documentos HTML.

La estructura básica de cualquier documento HTML:
```html
<!DOCTYPE html>
<html>
	<head>
		content
	</head>
	<body>
		content
	</body>
</html>
```
-   `<!DOCTYPE html>`: Todos los documentos deben empezar por esa declaración, representa el tipo de documento y debe de aparecer una vez al inicio, esa es la declaración para HTML5.
-   El documento en sí se pone dentro de `<html>`.
-   En `<head>` va meta información.
-   La parte visible de la página es la que va en `<body>`.

## Comentarios:

Para hacer comentarios en HTML se usa:
```html
<!-- esto es un comentario -->
```
-   Los comentarios se pueden poner entre líneas o abarcar más de una línea.
    

## Elementos.

Un elemento de HTML se define por una etiqueta de inicio, contenido y una etiqueta de cierre
```html
<tagname> content </tagname>
```
- _tagname_ es el nombre del elemento. Los nombres no son sensibles a mayúsculas y minúsculas pero se recomienda ponerlos en minúsculas.
- **Importante**: Aunque algunos elementos se pueden poner sin una etiqueta de cierre, es recomendable poner una etiqueta se apertura y cierre a todos los elementos.
- No todas las etiquetas tienen contenido y etiquetas de cierre, a ese tipo de etiquetas se les llama _etiquetas vacías_, ese tipo se etiquetas se pueden cerrar como: <br> `<tagname/>`

### Atributos

Todos los elementos  tienen atributos que proveen de información extra sobre los elementos.  Los atributos se ponen dentro de la etiqueta de apertura en la forma `name="value"`:
```html
<tagname attr="val" attr2="val" ...> content </tagname>
```
-   Los atributos se separan por espacio.
-   **Importante**: Se recomienda encerrar entre comillas los valores. Se pueden usar comillas dobles o simples, es más común usar dobles, pero es indiferente.

#### Atributos globales.

Los atributos globales son atributos comunes en todos los elementos de HTML, aunque algunos de ellos puede que no tengan efecto en determinados elementos. Los elementos globales más importantes son:

- `id`: Este atributo identifica de forma única un elemento dentro de una página web. A menudo se utiliza para apuntar a elementos específicos con CSS o JavaScript.
- `class`: Este atributo asigna uno o más nombres de clase a un elemento. Las clases se utilizan para agrupar elementos y aplicarles estilos en función de sus características compartidas.
- `style`: Este atributo aplica estilos CSS en línea a un elemento. Los estilos en línea tienen prioridad sobre los estilos definidos en una hoja de estilos.
- `title`: Este atributo proporciona información adicional sobre un elemento, como información sobre las herramientas o una descripción.
- `lang`: Este atributo especifica el idioma del contenido dentro de un elemento. Es importante para la accesibilidad y la optimización de los motores de búsqueda.
- `dir`: Este atributo indica la dirección del texto de un elemento, ya sea de izquierda a derecha (ltr) o de derecha a izquierda (rtl).

> Para una lista completa visitar la  [documentación](https://developer.mozilla.org/en-US/docs/Web/HTML/Global_attributes#list_of_global_attributes).

#### style.

Los estilos CSS de los elementos se pueden definir en el atributo `style`, en el que se pueden especificar colores, fuentes, tamaños, etc.  Las propiedades se separan por punto y coma `;` y los valores se determinan usando dos puntos `:`.
```html
<tagname style="property1:value; property2:value; ..."> content </tagname>
```
-   Los propiedades son propiedades de CSS y los valores son valores de CSS.
-   **Importante**: En general se recomienda establecer los estilos desde páginas de estilos de CSS.
    
Algunas propiedades importantes son (para más información consulta CSS):

-   `color`: Color del texto del elemento.
-   `background-color`: Color de fondo del elemento.
-   `font-size`: Tamaño de la fuente.
-   `font-family`: Fuente del texto del elemento.
-   `border`: Borde del elemento, tiene tres valores, tamaño, estilo de la línea y color.
-   `padding`: Espacio entre el elemento y el borde.
-   `margin`: Espacio afuera del borde.
-   `text-align`: Alineación del texto.
-   `width`: Ancho en pixeles.
-   `height`: Alto en pixeles.

#### class:

Las clases son un atributo de los elementos HTML usados para especificar la _clase_ de un elemento, múltiples elementos pueden compartir la misma clase. Se suele usar para definir estilos para una clase o para que JavaScript pueda acceder y manipular elementos de alguna clase.
```html
<tagname  class="name"> content </tagname>
```
-   _name_ es el nombre de la clase, si es una clase CSS se tuvo que haber especificado en `<style>` o en una hoja de estilo.
-   Es posible que el elemento pertenezca a más de una clase, para ello separar con espacios: <br> `<tagname class="class1 class2 ..."> content </tagname>`

#### id:

El id es un atributo de los elementos HTML usado para especificar un id único a un elemento. No puede haber dos o más elementos con el mismo id. Se suele usar para especificar un estilo único en una hoja de estilos o usado por JavaScript para manipular un elemento en específico.
```html
<tagname  id="name"> content </tagname>
```
-   _name_ es el nombre del id. Debe tener al menos un carácter, no puede empezar por números y no debe tener espacios en blanco.

### Elementos comunes:

#### Encabezados:

Establecen los encabezados de la página para estructurar el contenido de la página web.

Elementos:
-   `<h1>`.
-   `<h2>`.
-   `<h3>`.
-   `<h4>`.
-   `<h5>`.
-   `<h6>`.
    
#### Parágrafos:

Los parágrafos empiezan en una nueva línea y usualmente son un bloque de texto. Los parágrafos ignoran saltos de línea, espacios en blanco continuos y se autoajustan al tamaño de la ventana. 

Elementos:
-   `<p>`: Parágrafo que ignora saltos de línea y espacios y el texto se autoajusta al ancho de la ventana.
-   `<pre>`: Parágrafo que conserva los saltos de línea, espacios y ancho del texto.
-   `<br>`: Salto de línea.
-   `<hr>`: Línea horizontal.


### Bookmarks:

Para crear _bookmarks_ se utiliza el atributo id de cualquier elemento, ahí se define el nombre del bookmark, después en cualquier otra parte de la página para ir al bookmark se utiliza el elemento `<a>` y en el atributo `href` se utiliza `"#name"`, es decir el nombre del _bookmark_ precedido por un `#`.
```html
<!-- Asignar id al elemento -->
<element id="name">

...

<!-- Crear una referencia al elemento -->
<a href="#name"> content </a>
```
- Los bookmarks se suelen crear para los elementos de encabezados, tablas, imágenes, entre otros.  
- Si se quiere establecer un bookmark en otro archivo html usar en `href`: <br> `"path/filename.html#name"`


### Elementos para Layout

Son elementos que definen las diferentes partes de una página web:

-   `<header>`: Indica el encabezado de una página o una sección.
-   `<nav>`: Define un conjunto de link de navegación.
-   `<section>`: Define una sección en un documento.
-   `<article>`: Define un contenido auto-contenido independiente.
-   `<aside>`: Define contenido lateral.
-   `<footer>`: Define un pie de página del documento o sección.
-   `<details>`: Define detalles adicionales.
-   `<summary>`: Define un título para el elemento `<details>`.

## Elementos de HTML

`<html>`: Representa la raíz de un documento HTML. Permite los elementos `<head>` y `<body>`.

```html
<html> 
	<head> 
		content 
	</head> 
	<body> 
		content 
	</body> 
</html>
```

**Atributos de \<html\>**: 

- Para una lista completa visitar la  [documentación](https://developer.mozilla.org/en-US/docs/Web/HTML/Element/html#attributes).
- `lang`: Indica el idioma de la página web, es recomendado indicarlo. Para consultar los posibles valores, visitar [esta página](https://www.w3schools.com/tags/ref_language_codes.asp)

### \<head\>

Provee información general acerca del documento, incluyendo el título, enlaces a scripts de JS y hojas de estilo de CSS, entre otros datos. Los elementos que se indiquen no se visualizan en el navegador web. 

```html
<head>  
	content
</head> 
```
- Para más información consultar la [documentación](https://developer.mozilla.org/en-US/docs/Web/HTML/Element/head)

<br>

#### Titulos:

`<title>`: Indica el título de un documento, es el nombre que aparecerá en la pestaña del navegador al tener la página abierta. Importante. Todos los documentos deben de tener un título. También es el nombre que aparecerá en los resultados de los buscadores. 

```html
<head>
	<title> Título </title>
</head> 
```
- Para más información consultar la [documentación](https://developer.mozilla.org/en-US/docs/Web/HTML/Element/title)
- **Importante**: Todos los documentos deben de tener un título que debe estar dentro de `<head>`. 

<br>

**Atributos**: 
- lang <str>: Lenguaje del elemento. 

<br>

#### Metadata: 

`<meta>`: Provee información sobre el documento. No tiene etiqueta de cierre. Algunos usos es especificar el conjunto de caracteres a usar en la página, descripción de la página, keywords, autor del documento, etc. Se pone un meta por cada información que se quiera proveer. 
```HTML
<head>
	<meta attrs/>
</head>  
```
- No tiene contenido. 
- Se recomienda usar el siguiente _meta_ en todos los documentos HTML, para controlar las dimensiones y escala de la página, particularmente en dispositivos móviles: <br> `<meta name="viewport" content="width=device-width, initial-scale=1.0">`
- Para más información consultar la [documentación](https://developer.mozilla.org/en-US/docs/Web/HTML/Element/meta)

<br>

**Atributos**: 
- `charset`:Permite indicar el conjunto de caracteres que tendrá la página web. Algunos valores posibles son:
	- `"utf-8"`
- `name`: Nombre de la característica meta. Como keywords, description, author. Para una lista completa visitar la [documentación](https://developer.mozilla.org/en-US/docs/Web/HTML/Element/meta/name#standard_metadata_names_defined_in_the_html_specification). Valores comunes:
	- `author`: El nombre del autor del documento. 
	- `description`: Un resumen breve y preciso del contenido de la página. 
	- `keywords`: Palabras relevantes para el contenido de la página separadas por comas. 
- `content`: Contenido del atributo `name`. 

#### Estilos CSS: 

`<style>`: Establece el estilo CSS general de la página. 
```html
<head>
	<style>   
		content  
	</style>
</head> 
```
- Para más información consultar la [documentación](https://developer.mozilla.org/en-US/docs/Web/HTML/Element/style)
- El contenido son los estilos CSS, de la misma manera como se definirían en una hoja de estilo. Ejemplo
```html
<head>
	<style>   
		h1: {
			attr: val; 
			attr: val;
			...
		}
		...   
	</style>
</head> 
```

<br>

#### Links: 

`<link>`: Especifica la relación entre un documento actual y un archivo externo. Se suele utilizar para enlazar con hojas de estilos. No tiene etiqueta de cierre.
```html
<head>
	<link /> 
</head> 
```
- Para más información consultar la [documentación](https://developer.mozilla.org/en-US/docs/Web/HTML/Element/link)

**Atributos**: 
- `rel`: Indica la relación del documento enlazado con el actual. Si es una hoja se estilos se utiliza stylesheet.
	- `"stylesheet"`: Enlaces a una hoja de estilo externa. Este es el uso más común del atributo rel.
	- `"alternate"`: Enlaces a una versión alternativa del documento. Esto se puede usar para proporcionar diferentes versiones del documento para diferentes idiomas, dispositivos u otros criterios. 
	- `"icon"`: Enlaces a un icono del documento. Este icono suele mostrarse en la barra de pestañas del navegador y en las listas de marcadores. 
- `href`: URL o ruta al archivo externo. 
- `type`: Es usado para definir el tipo de contenido al que se enlaza. El valor debe de ser un tipo MIME, como "text/html", "text/css", "image/x-icon", etc. 

<br>

#### JS Scripts

`<script>`: Puede contener sentencias de JavaScript o apuntar a un script externo. 
```html
<head>
	<script>
		content
	</script> 
</head> 
```
- _content_ es directamente el código de JavaScript. En caso de que sea un script externo no es necesario poner nada.
- Para más información consultar la [documentación](https://developer.mozilla.org/en-US/docs/Web/HTML/Element/script)

**Atributos**: 
- `href`: URL de un script externo. Puede ser ruta relativas o absolutas. 

<br>

#### URL Base 

`<base>`: Establece el URL base para todos los documentos, imágenes, etc. relativos en el proyecto. Solo puede haber un elemento `<base>` en el documento. Debe de tener al menos un atributo `href` o `target`. 
```html
<head>
	<base/>
</head> 
``` 
- No tiene contenido ni etiqueta de cierre.
- Para más información consultar la [documentación](https://developer.mozilla.org/en-US/docs/Web/HTML/Element/base)

**Atributos**: 
- `href`: URL base. 
- `target`: Objetivo base. 

- `<blockquote>`: Define una sección que es una cita de otra fuente: `<blockquote cite="URL"> texto </blockquote>` <blockquote> ejemplo </blockquote> 
	- cite: URL o ruta del documento original. 
- `<q>` \- Quotation: Define una cita pequeña, el texto se pondrá entre comillas. <q> ejemplo </q> <br> `<q> content </q>`
- `<abbr>` \- Abbrevation: Define una abreviación o acrónimos. Puede ser de utilidad para navegadores, sistemas de traducción y buscadores: <abbr> Ejm </abbr> <br> `<abbr> content </abbr>` 
- `<address>`: Define la información de contacto del autor o dueño de un documento o artículo. Normalmente se mostrará en cursiva: <address> Ejemplo </address> <br> `<address> content </address>` 
- `<cite>`: Define el título de un trabajo creativo, como libros, poemas, canciones, películas, pinturas, esculturas, etc. Normalmente se muestra en cursiva: <cite> ejemplo </cite> <br> `<cite> content </cite>` 
- `<bdo>` \- Bi-Dideractional Override: Pone el texto en sentido contrario: <bdo> ejemplo </bdo> <br> `<bdo> content </bdo>` 

### \<body\>

Representa el contenido de un documento HTML. Será el contenido que se visualizará en la página web. **Importante**: Solo puede haber un elemento `<body>` en cada documento. 

```html
<body>  
	content
</body> 
```
- Para más información consultar la [documentación](https://developer.mozilla.org/en-US/docs/Web/HTML/Element/body).

<br>

#### Contenedor de bloque: 

`<div>`: Sirve para crear secciones o agrupar contenido en un documento HTML. Es un contenedor de otros elementos HTML. Se puede usar para darle estilo a bloques de contenido. 

```html
<body> 
	<div>
		content
	</div> 
</body> 
```
- Para más información consultar la [documentación](https://developer.mozilla.org/en-US/docs/Web/HTML/Element/div).

<br>

#### Contenedor Inline 

`<span>`: Es un contenedor en línea, sirve para aplicar estilo al texto o agrupar elementos en línea. 
```html
<body> 
	<span>
		content
	</span> 
</body> 
```
- Para más información consultar la [documentación](https://developer.mozilla.org/en-US/docs/Web/HTML/Element/span).

<br>

#### Parrafos: 

`<p>`: Es el elemento para distribuir texto en párrafos. Puede contener cero o más elementos en línea. No se respetan saltos de línea en el código. 
```html
<body>
	<p> text </p> 
</body> 
```
- _text_ es cualquier texto que irá en el párrafo. 
- Para más información consultar la [documentación](https://developer.mozilla.org/en-US/docs/Web/HTML/Element/p).
 
**Atributos**: 
- `title`: Texto que aparecerá al poner el cursor sobre el párrafo. 
- `style`: Determina el estilo del párrafo. 

--- 
`<pre>`: Define un texto que preserva saltos de línea y espacios en blanco. 

```html
<body>
	<pre> text </pre> 
</body> 
```
- _text_ es cualquier texto que irá en el párrafo. 
- Para más información consultar la [documentación](https://developer.mozilla.org/en-US/docs/Web/HTML/Element/p).

<br>

#### Títulos: 

<code>h<em>group</em></code>: Son elementos de grupos de cabecera, representan el encabezado de una sección. Definen un título que participa en la estructura del documento. Incluyen de las etiquetas `<h1>` a `<h6>`, siendo `<h1>` el encabezado principal. Agregan un salto de línea automáticamente. 
```html
<body> 
	<h1> Encabezado 1</h1>
	<h2> Encabezado 2</h2>
	<h3> Encabezado 3</h3>
	<h4> Encabezado 4</h4>
	<h5> Encabezado 5</h5>
	<h6> Encabezado 6</h6>
</body> 
```
- Para más información consultar la [documentación](https://developer.mozilla.org/en-US/docs/Web/HTML/Element/hgroup). 

<br>

#### Saltos de línea: 

`<br>`: Es un salto de línea (_line break_) que produce un salto de línea en el texto. No tiene contenido por lo que se cierra como `</>` en una sola etiqueta. 
```html
<body> 
	<br/> 
</body> 
```
- Para más información consultar la [documentación](https://developer.mozilla.org/en-US/docs/Web/HTML/Element/br). 

<br>

#### Líneas divisoras de texto: 

`<hr>`: "Horizontal rule" agrega una línea horizontal para crear divisiones en elementos de la página. No tiene contenido por lo que se cierra como `</>` en una sola etiqueta. 
```html
<body>
	<hr/> 
</body> 
```
- Para más información consultar la [documentación](https://developer.mozilla.org/en-US/docs/Web/HTML/Element/hr). 

<br>


#### Formato de texto:

A continuación se enlistan diversas etiquetas que sirven para darle formato al texto en etiquetas como `<p>` o `<span>`.

- `<b>` \- Bold: Texto en negritas: <b>ejemplo</b> <br> `<b> texto </b>`
- `<strong>` \- Strong: Es para indicar que el texto es importante. El formato es el mismo que el de negritas, pero el significado es distinto: <strong>ejemplo</strong> <br> - `<strong> texto </strong>`
- `<i>` \- Italic: Es para poner un texto en cursiva/itálica: <i>ejemplo</i> <br> `<i> texto </i>`
- `<em>` \- Emphasize: Es para enfatizar un texto, el resultado es similar a itálica, pero el significado es distinto: <em>ejemplo</em>  <br> `<em> texto </em>`
- `<del>` \- Deleted: Es para tachar un texto: <del>ejemplo</del> <br> `<del> texto </del>` 
- `<ins>` \- Inserted: Es insertar un texto, pero se ve como un texto subrayado: <ins>ejemplo</ins>  <br> `<ins> texto </ins>` 
- `<sub>` \- Subscript: Es para que un texto aparezca como subíndice: X<sub>ejemplo</sub>  <br> `<sub> texto </sub>` 
- `<sup>` \- Superscript: Es para que un texto aparezca como superíndice: X<sup>ejemplo</sup>  <br> `<sup> texto </sup>` 
- `<small>` \- Small: Pone un texto de un tamaño menor: <small>ejemplo</small> <br> `<small> texto </small>` 
- `<mark>` \- Mark: Es para resaltar un texto, somo si estuviera subrayado con un marcador: <mark>ejemplo</mark> <br> `<mark> texto </mark>`

<br>

#### Formato como código. 

- `<kbd>`: Se utiliza para definir acciones con el teclado, como indicar al usuario que presiones ciertas teclas. Lo único que hace esta etiqueta es cambiar el formato del contenido: <kbd>ejemplo</kbd>  <br> `<kbd> content </kbd>` 
- `<samp>`: Se utiliza para definir mostrar el output de un programa de computadora. Lo único que hace esta etiqueta es cambiar el formato del contenido: <samp>ejemplo</samp> <br> `<samp> content </samp>`
- `<code>`: Es para definir el texto como si fuera código. Lo único que hace esta etiqueta es cambiar el formato del contenido: <code>ejemplo</code> <br> `<code> content </code>` 
- `<var>`: Es para definir variables en programación o matemáticas. Lo único que hace esta etiqueta es cambiar el formato del contenido: <var>ejemplo</var>  <br> `<var> content </var>` 

<br>

#### Citas: 

- `<blockquote>`: Define una sección que es una cita de otra fuente: `<blockquote cite="URL"> texto </blockquote>` <blockquote> ejemplo </blockquote> 
	- cite: URL o ruta del documento original. 
- `<q>` \- Quotation: Define una cita pequeña, el texto se pondrá entre comillas. <q> ejemplo </q> <br> `<q> content </q>`
- `<abbr>` \- Abbrevation: Define una abreviación o acrónimos. Puede ser de utilidad para navegadores, sistemas de traducción y buscadores: <abbr> Ejm </abbr> <br> `<abbr> content </abbr>` 
- `<address>`: Define la información de contacto del autor o dueño de un documento o artículo. Normalmente se mostrará en cursiva: `<address> content </address>` <address> Ejemplo </address>
- `<cite>`: Define el título de un trabajo creativo, como libros, poemas, canciones, películas, pinturas, esculturas, etc. Normalmente se muestra en cursiva: <cite> ejemplo </cite> <br> `<cite> content </cite>` 
- `<bdo>` \- Bi-Dideractional Override: Pone el texto en sentido contrario: <bdo> ejemplo </bdo> <br> `<bdo> content </bdo>` 

<br>

#### Links: 

`<a>`: Agrega un link. Cualquier elemento HTML puede ser un link. 
```html
<body>
	<a href="url" target="value"> link </a> 
</body> 
```
- _link_ es la parte que será visible al usuario y que al presionar sobre ella se abrirá el link. 
- Para más información consultar la [documentación](https://developer.mozilla.org/en-US/docs/Web/HTML/Element/a). 

**Atributos**: 
- `href`: URL de la página o ruta de otro archivo HTML. 
- `target`: Especifica cómo desplegar la URL. Algunos valores posibles son: 
	- `_self` (default): Abre la url en la misma pestaña que la actual. 
	- `_blank`: Abre la url en una pestaña nueva, aunque dependiendo de la configuración de los usuarios del navegador puede ser una ventana nueva. 
	- `_parent`: Abre el url en el _parent frame_. 
	- `_top`: Abre el url en el cuerpo completo de la ventana. 

<br>
 
#### Imágenes. 

`<img>`: Agrega una imagen a la página web. No tiene contenido por lo que se cierra como `</>` en una sola etiqueta. 
```html
<body>
	<img scr="URL"/>
</body> 
``` 
- Lo normal es agregar las imágenes en subcarpetas del proyecto. 
- Para más información consultar la [documentación](https://developer.mozilla.org/en-US/docs/Web/HTML/Element/img).  

**Atributos**: 
- `src`: Ruta de la imagen, desde el directorio local, es decir, partiendo del directorio donde está el proyecto. También puede ser una URL en internet. 
- `alt`: Representa un texto alternativo en caso de que la imagen no se pueda mostrar correctamente, es recomendado poner un texto alternativo a todas las imágenes. 
- `height`: Alto de la imagen en pixeles CSS o pixeles. Por ejemplo "10px". Si no se especifica width entonces se determinará automáticamente. 
- `width`: Ancho de la imagen en pixeles CSS o pixeles. Por ejemplo "10px". Si no se especifica height entonces se determinará automáticamente. 
- `title`: Texto que aparecerá al poner el cursor sobre la imagen. 
- `style`: Define el estilo del elemento. 

#### Tablas: 

Para crear una tabla es HTML es necesario utilizar diversas etiquetas para definir los elementos de la tabla, a continuación se muesta un ejemplo general

```html
<table>
  <thead>
    <tr>
      <th>Name</th>
      <th>Age</th>
      <th>Occupation</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td>John Doe</td>
      <td>30</td>
      <td>Software Engineer</td>
    </tr>
    <tr>
      <td>Jane Smith</td>
      <td>25</td>
      <td>Marketing Manager</td>
    </tr>
    <tr>
      <td>Peter Jones</td>
      <td>40</td>
      <td>Accountant</td>
    </tr>
  </tbody>
</table>
``` 

Lo anterior se visualizaría como:

<table>
  <thead>
    <tr>
      <th>Name</th>
      <th>Age</th>
      <th>Occupation</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td>John Doe</td>
      <td>30</td>
      <td>Software Engineer</td>
    </tr>
    <tr>
      <td>Jane Smith</td>
      <td>25</td>
      <td>Marketing Manager</td>
    </tr>
    <tr>
      <td>Peter Jones</td>
      <td>40</td>
      <td>Accountant</td>
    </tr>
  </tbody>
</table>

##### Estructura general:

`<table>`: Crea la estructura de una tabla, es necesario usar otras etiquetas como `<thead>` y `<tbody>`.
```html
<body>
	<table> 
		<thead>
			...
  		</thead>
  		<tbody>
    			...
  		</tbody> 
	</table> 
</body> 
``` 
- Para más información consultar la [documentación](https://developer.mozilla.org/en-US/docs/Web/HTML/Element/table). 

##### Título

`<caption>`: Agrega un título a la tabla. Se debe poner inmediatamente después de `<table>`: 

```html
<body>
	<table> 
		<caption> content </caption>
		table content ...	 
	</table> 
</body> 
``` 
- Para más información consultar la [documentación](https://developer.mozilla.org/en-US/docs/Web/HTML/Element/caption). 

##### Filas:

`<tr>` \- _Table rows_: Agrega una fila a un tabla. Se usa dentro de `<thead>` o `<tbody>` y usa otras etiquetas como `<th>` y `<td>`. 
```html
<body>
	<table> 
		<tr>
			content ...
		</tr>
	</table> 
</body>
``` 
- Para más información consultar la [documentación](https://developer.mozilla.org/en-US/docs/Web/HTML/Element/tr).  

##### Encabezados:

`<th>` \- _Table headers_: Agrega una celda con formato de encabezado de una tabla a una fila, se debe poner un elemento por cada columna. Se usa dentro de `<tr>` que representa una fila. 
```html
<body>
	<table> 
		<tr>
			<th> content </th>
			... 
		</tr>
	</table> 
</body>
``` 
- Para más información consultar la [documentación](https://developer.mozilla.org/en-US/docs/Web/HTML/Element/th). 

**Atributos**: 
- `colspan`: Es para indicar el número de columnas que debe de abarcar una sola celda, se usa para combinar celdas horizontalmente. 

##### Celdas 

`<td>` \- _Table data_: Agrega una celda con formato de datos a una fila. Es un elemento por cada columna. Se usa dentro de `<tr>` que representa una fila.  
```html
<body>
	<table> 
		<tr>
			<td> content </td>
			... 
		</tr>
	</table> 
</body>
```
- El contenido puede ser cualquier otro elemento de HTML como texto, imágenes, listas, otras tablas, etc. 
- Para más información consultar la [documentación](https://developer.mozilla.org/en-US/docs/Web/HTML/Element/td). 
 
**Atributos**: 
- `rowspan`: Es para indicar el número de filas que debe de abarcar una sola celda, se usa como para combinar celdas verticalmente. 

##### Otros elementos: 

- `<colgroup>`: Especifica un grupo de una o más columnas en una tabla para darles formato. 
- `<col>`: Específica las propiedades para cada columna dentro de un elemento `<colgroup>`. 
- `<thead>`: Agrupa los encabezados en una tabla. 
- `<tbody>`: Agrupa el contenido de una tabla. 
- `<tfoot>`: Agrupa el contenido a pie de página de una tabla. 


#### Listas: 

Existen tres tipos de listas: 

- Ordenadas. 
- No ordenadas. 
- Listas de definición. 

##### Lista no ordenada. 

`<ul>` \- _Unordered list_: Permite definir listas no ordenadas con viñetas. Se usa junto con `<li>` para definir los elementos. 
```html
<body>
	<ul>
  		<li>Item 1</li>
  		<li>Item 2</li>
  		<li>Item 3</li>
		...
	</ul>
</body>
```
- Por default se utilizan círculos pequeños negros. Para modificarlo se utiliza la propiedad `list-style-type` del atributo `style`.
- Las etiquetas `<li>` puede contener otras listas, y otros elementos como imágenes, links, etc.
- Para más información consultar la [documentación](https://developer.mozilla.org/en-US/docs/Web/HTML/Element/ul). 

##### Lista ordenada: 

`<ol>` \- Ordered list: Permite definir listas ordenadas con letras o números. Se usa junto con `<li>` para definir los elementos. 
```html
<body>
	<ol>
  		<li>Item 1</li>
  		<li>Item 2</li>
  		<li>Item 3</li>
		...
	</ol>
</body>
```
- Las etiquetas `<li>` puede contener otras listas, y otros elementos como imágenes, links, etc.
- Para más información consultar la [documentación](https://developer.mozilla.org/en-US/docs/Web/HTML/Element/ol).

 
**Atributos**: 
- `type`: Indica el tipo de símbolo, por default son números, puede see:
	- `"1"` (default): Números.
	- `"A"`: Letras en mayúsculas.
	- `"a"`: Letras en minúsculas. 
	- `"i"`: Números romanos en minúsculas.
	- `"I"`: Números romanos en mayúsculas.
- `start`: Indica desde que número iniciar el conteo, por default es desde 1.
- `reversed`: Indica que la númeración sea a la inversa. No se le debe asignar ningún valor, simplemente añadir el atributo en la etiqueta.

#### Lista de descripción: 

`<dl>`: Description list - Permite definir listas de descripción. Se usa junto con `<dd>` y `<dt>`. 
```html
<body>
	<dl>
  		<dt>Term 1</dt>
  		<dd>Description of Term 1.</dd>
  		<dt>Term 2</dt>
  		<dd>Description of Term 2.</dd>
  		...
	</dl>
</body>
```
- Adicionalmente se utilizan las siguientes etiquetas:
	- `<dt>` \- _Description term_: Específica un término o descripción en una lista de descripciones.
	- `<dd>` \- _Description description_: Provee detalles acerca de la definición de un término precedente. 
- Para más información consultar la [documentación](https://developer.mozilla.org/en-US/docs/Web/HTML/Element/dl).

#### Scripts: 

`<script>`: Puede contener sentencias de JavaScript. **Importante**: Debe de ir después de cualquier otro elemento al cual se vaya a acceder desde el script.
```html
<body>
	<script> content </script> 
</body>
```
- _content_ es directamente el código de JavaScript. 
- Otra etiqueta relacionada es:
	- `<noscript>`: Muestra un contenido alternativo para navegadores que no soportan scripts o lo tienen desactivados. <br> `<noscript> content </noscript>` 
 
#### Estructurales: 

Las siguiente etiquetas no impactan visualmente en la página, pero si en la estructura de la página. Sirven para organizar la página. 

- `<section>`: Define una sección de un documento. Una sección agrupa temáticamente contenido, generalmente con un encabezado. <br> `<section> content </section>` 
- `<article>`: Se utiliza para posts de foros, blogs, artículos, etc. <br> `<article> content </article>` 
- `<aside>`: Define un elemento que se coloca lateralmente del contenido donde es colocado. Debe tener sentido con el contenido que lo rodea. <br> `<aside> content </aside>` 
- `<header>`: Indica el encabezado de una página, también puede tener un conjunto de links de navegación. Suele tener un encabezado, logos y links de navegación. <br> `<header> content </header>` 
- `<footer>`: Define un pie de página, suele contener información del autor, derechos de autor, información de contacto, mapa del sitio, documentos relacionados, etc. <br> `<footer> content </footer>` 
- `<nav>`: Navigation - Define un conjunto de links de navegación, está pensado para agrupar un conjunto. <br> `<nav> content </nav>` 
- `<figure>`: Un contenedor de imágenes, fotos, ilustraciones, etc. Dentro de él se suele usar `<img>` y `<figcaption>` <br> `<figure> content </figure>` 
- `<figcaption>`: Inserta un caption a una imagen. <br> `<figcaption> content </figcaption>` 



## Mejores prácticas:

-   Usar minúsculas en los nombres de los elementos.
-   Cerrar todos los elementos (`</>`).
-   Poner los valores de los atributos entre comillas dobles: `attr="val"`.
-   Especificar el atributo `alt` y propiedades de CSS `height` y `width` para imágenes.
-   Evitar poner espacios entre el signo "=" al definir atributos: `attr="val"`.
-   Evitar líneas de código muy largas horizontalmente.
-   Utilizar el elemento `<title>` de `<head>`.
-   Utilizar los elementos `<html>`, `<head>` y `<body>`.    
-   Los elementos etiqueta de cierre cerrar con `<tagname/>`.
-   Indicar el atributo `lang` de `<html>`.
-   Indicar el atributo `charset` de `<meta>`.
-   Especificar `viewport` en `<meta>`.
-   Utilizar hojas de estilos en lugar de especificar los estilos en el documento HTML.
-   Utilizar nombres de archivos en minúsculas.
-   Utilizar las extensiones `.html`, `.css` y `.js` para HTML, CSS y JavaScript respectivamente.
