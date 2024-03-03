---


---

<h1 id="html">HTML</h1>
<p><em>Hyper Text Markup  Language</em> (HTML) Es un lenguaje de marcado (<em>markup  language</em>) para  la creación de páginas web. Principalmente funciona para describir la estructura de la pagína web y definir sus elementos indicando a los navegadores cómo mostrar el contenido.</p>
<p>La página principal de una página web normalmente se llama “<em>index.html</em>”. Es recomendado usar ese nombre.</p>
<p>Los documentos html terminan con la extencioón <code>.htm</code> o <code>.html</code>.</p>
<h2 id="documentos-html.">Documentos HTML.</h2>
<p>La estructura básica de cualquier documento HTML:</p>
<pre class=" language-html"><code class="prism  language-html"><span class="token doctype">&lt;!DOCTYPE html&gt;</span>
<span class="token tag"><span class="token tag"><span class="token punctuation">&lt;</span>html</span><span class="token punctuation">&gt;</span></span>
	<span class="token tag"><span class="token tag"><span class="token punctuation">&lt;</span>head</span><span class="token punctuation">&gt;</span></span>
		content
	<span class="token tag"><span class="token tag"><span class="token punctuation">&lt;/</span>head</span><span class="token punctuation">&gt;</span></span>
	<span class="token tag"><span class="token tag"><span class="token punctuation">&lt;</span>body</span><span class="token punctuation">&gt;</span></span>
		content
	<span class="token tag"><span class="token tag"><span class="token punctuation">&lt;/</span>body</span><span class="token punctuation">&gt;</span></span>
<span class="token tag"><span class="token tag"><span class="token punctuation">&lt;/</span>html</span><span class="token punctuation">&gt;</span></span>
</code></pre>
<ul>
<li><code>&lt;!DOCTYPE html&gt;</code>: Todos los documentos deben empezar por esa declaración, representa el tipo de documento y debe de aparecer una vez al inicio, esa es la declaración para HTML5.</li>
<li>El documento en sí se pone dentro de <code>&lt;html&gt;</code>.</li>
<li>En <code>&lt;head&gt;</code> va meta información.</li>
<li>La parte visible de la página es la que va en <code>&lt;body&gt;</code>.</li>
</ul>
<h2 id="comentarios">Comentarios:</h2>
<p>Para hacer comentarios en HTML se usa:</p>
<pre class=" language-html"><code class="prism  language-html"><span class="token comment">&lt;!-- esto es un comentario --&gt;</span>
</code></pre>
<ul>
<li>Los comentarios se pueden poner entre líneas o abarcar más de una línea.</li>
</ul>
<h2 id="elementos.">Elementos.</h2>
<p>Un elemento de HTML se define por una etiqueta de inicio, contenido y una etiqueta de cierre</p>
<pre class=" language-html"><code class="prism  language-html"><span class="token tag"><span class="token tag"><span class="token punctuation">&lt;</span>tagname</span><span class="token punctuation">&gt;</span></span> content <span class="token tag"><span class="token tag"><span class="token punctuation">&lt;/</span>tagname</span><span class="token punctuation">&gt;</span></span>
</code></pre>
<ul>
<li><em>tagname</em> es el nombre del elemento. Los nombres no son sensibles a mayúsculas y minúsculas pero se recomienda ponerlos en minúsculas.</li>
<li><strong>Importante</strong>: Aunque algunos elementos se pueden poner sin una etiqueta de cierre, es recomendable poner una etiqueta se apertura y cierre a todos los elementos.</li>
<li>No todas las etiquetas tienen contenido y etiquetas de cierre, a ese tipo de etiquetas se les llama <em>etiquetas vacías</em>, ese tipo se etiquetas se pueden cerrar como: <br> <code>&lt;tagname/&gt;</code></li>
</ul>
<h3 id="atributos">Atributos</h3>
<p>Todos los elementos  tienen atributos que proveen de información extra sobre los elementos.  Los atributos se ponen dentro de la etiqueta de apertura en la forma <code>name="value"</code>:</p>
<pre class=" language-html"><code class="prism  language-html"><span class="token tag"><span class="token tag"><span class="token punctuation">&lt;</span>tagname</span> <span class="token attr-name">attr</span><span class="token attr-value"><span class="token punctuation">=</span><span class="token punctuation">"</span>val<span class="token punctuation">"</span></span> <span class="token attr-name">attr2</span><span class="token attr-value"><span class="token punctuation">=</span><span class="token punctuation">"</span>val<span class="token punctuation">"</span></span> <span class="token attr-name">...</span><span class="token punctuation">&gt;</span></span> content <span class="token tag"><span class="token tag"><span class="token punctuation">&lt;/</span>tagname</span><span class="token punctuation">&gt;</span></span>
</code></pre>
<ul>
<li>Los atributos se separan por espacio.</li>
<li><strong>Importante</strong>: Se recomienda encerrar entre comillas los valores. Se pueden usar comillas dobles o simples, es más común usar dobles, pero es indiferente.</li>
</ul>
<h4 id="atributos-globales.">Atributos globales.</h4>
<p>Los atributos globales son atributos comunes en todos los elementos de HTML, aunque algunos de ellos puede que no tengan efecto en determinados elementos. Los elementos globales más importantes son:</p>
<ul>
<li><code>id</code>: Este atributo identifica de forma única un elemento dentro de una página web. A menudo se utiliza para apuntar a elementos específicos con CSS o JavaScript.</li>
<li><code>class</code>: Este atributo asigna uno o más nombres de clase a un elemento. Las clases se utilizan para agrupar elementos y aplicarles estilos en función de sus características compartidas.</li>
<li><code>style</code>: Este atributo aplica estilos CSS en línea a un elemento. Los estilos en línea tienen prioridad sobre los estilos definidos en una hoja de estilos.</li>
<li><code>title</code>: Este atributo proporciona información adicional sobre un elemento, como información sobre las herramientas o una descripción.</li>
<li><code>lang</code>: Este atributo especifica el idioma del contenido dentro de un elemento. Es importante para la accesibilidad y la optimización de los motores de búsqueda.</li>
<li><code>dir</code>: Este atributo indica la dirección del texto de un elemento, ya sea de izquierda a derecha (ltr) o de derecha a izquierda (rtl).</li>
</ul>
<blockquote>
<p>Para una lista completa visitar la  <a href="https://developer.mozilla.org/en-US/docs/Web/HTML/Global_attributes#list_of_global_attributes">documentación</a>.</p>
</blockquote>
<h4 id="style.">style.</h4>
<p>Los estilos CSS de los elementos se pueden definir en el atributo <code>style</code>, en el que se pueden especificar colores, fuentes, tamaños, etc.  Las propiedades se separan por punto y coma <code>;</code> y los valores se determinan usando dos puntos <code>:</code>.</p>
<pre class=" language-html"><code class="prism  language-html"><span class="token tag"><span class="token tag"><span class="token punctuation">&lt;</span>tagname</span><span class="token style-attr language-css"><span class="token attr-name"> <span class="token attr-name">style</span></span><span class="token punctuation">="</span><span class="token attr-value"><span class="token property">property1</span><span class="token punctuation">:</span>value<span class="token punctuation">;</span> <span class="token property">property2</span><span class="token punctuation">:</span>value<span class="token punctuation">;</span> <span class="token number">...</span></span><span class="token punctuation">"</span></span><span class="token punctuation">&gt;</span></span> content <span class="token tag"><span class="token tag"><span class="token punctuation">&lt;/</span>tagname</span><span class="token punctuation">&gt;</span></span>
</code></pre>
<ul>
<li>Los propiedades son propiedades de CSS y los valores son valores de CSS.</li>
<li><strong>Importante</strong>: En general se recomienda establecer los estilos desde páginas de estilos de CSS.</li>
</ul>
<p>Algunas propiedades importantes son (para más información consulta CSS):</p>
<ul>
<li><code>color</code>: Color del texto del elemento.</li>
<li><code>background-color</code>: Color de fondo del elemento.</li>
<li><code>font-size</code>: Tamaño de la fuente.</li>
<li><code>font-family</code>: Fuente del texto del elemento.</li>
<li><code>border</code>: Borde del elemento, tiene tres valores, tamaño, estilo de la línea y color.</li>
<li><code>padding</code>: Espacio entre el elemento y el borde.</li>
<li><code>margin</code>: Espacio afuera del borde.</li>
<li><code>text-align</code>: Alineación del texto.</li>
<li><code>width</code>: Ancho en pixeles.</li>
<li><code>height</code>: Alto en pixeles.</li>
</ul>
<h4 id="class">class:</h4>
<p>Las clases son un atributo de los elementos HTML usados para especificar la <em>clase</em> de un elemento, múltiples elementos pueden compartir la misma clase. Se suele usar para definir estilos para una clase o para que JavaScript pueda acceder y manipular elementos de alguna clase.</p>
<pre class=" language-html"><code class="prism  language-html"><span class="token tag"><span class="token tag"><span class="token punctuation">&lt;</span>tagname</span>  <span class="token attr-name">class</span><span class="token attr-value"><span class="token punctuation">=</span><span class="token punctuation">"</span>name<span class="token punctuation">"</span></span><span class="token punctuation">&gt;</span></span> content <span class="token tag"><span class="token tag"><span class="token punctuation">&lt;/</span>tagname</span><span class="token punctuation">&gt;</span></span>
</code></pre>
<ul>
<li><em>name</em> es el nombre de la clase, si es una clase CSS se tuvo que haber especificado en <code>&lt;style&gt;</code> o en una hoja de estilo.</li>
<li>Es posible que el elemento pertenezca a más de una clase, para ello separar con espacios: <br> <code>&lt;tagname class="class1 class2 ..."&gt; content &lt;/tagname&gt;</code></li>
</ul>
<h4 id="id">id:</h4>
<p>El id es un atributo de los elementos HTML usado para especificar un id único a un elemento. No puede haber dos o más elementos con el mismo id. Se suele usar para especificar un estilo único en una hoja de estilos o usado por JavaScript para manipular un elemento en específico.</p>
<pre class=" language-html"><code class="prism  language-html"><span class="token tag"><span class="token tag"><span class="token punctuation">&lt;</span>tagname</span>  <span class="token attr-name">id</span><span class="token attr-value"><span class="token punctuation">=</span><span class="token punctuation">"</span>name<span class="token punctuation">"</span></span><span class="token punctuation">&gt;</span></span> content <span class="token tag"><span class="token tag"><span class="token punctuation">&lt;/</span>tagname</span><span class="token punctuation">&gt;</span></span>
</code></pre>
<ul>
<li><em>name</em> es el nombre del id. Debe tener al menos un carácter, no puede empezar por números y no debe tener espacios en blanco.</li>
</ul>
<h3 id="elementos-comunes">Elementos comunes:</h3>
<h4 id="encabezados">Encabezados:</h4>
<p>Establecen los encabezados de la página para estructurar el contenido de la página web.</p>
<p>Elementos:</p>
<ul>
<li><code>&lt;h1&gt;</code>.</li>
<li><code>&lt;h2&gt;</code>.</li>
<li><code>&lt;h3&gt;</code>.</li>
<li><code>&lt;h4&gt;</code>.</li>
<li><code>&lt;h5&gt;</code>.</li>
<li><code>&lt;h6&gt;</code>.</li>
</ul>
<h4 id="parágrafos">Parágrafos:</h4>
<p>Los parágrafos empiezan en una nueva línea y usualmente son un bloque de texto. Los parágrafos ignoran saltos de línea, espacios en blanco continuos y se autoajustan al tamaño de la ventana.</p>
<p>Elementos:</p>
<ul>
<li><code>&lt;p&gt;</code>: Parágrafo que ignora saltos de línea y espacios y el texto se autoajusta al ancho de la ventana.</li>
<li><code>&lt;pre&gt;</code>: Parágrafo que conserva los saltos de línea, espacios y ancho del texto.</li>
<li><code>&lt;br&gt;</code>: Salto de línea.</li>
<li><code>&lt;hr&gt;</code>: Línea horizontal.</li>
</ul>
<h3 id="bookmarks">Bookmarks:</h3>
<p>Para crear <em>bookmarks</em> se utiliza el atributo id de cualquier elemento, ahí se define el nombre del bookmark, después en cualquier otra parte de la página para ir al bookmark se utiliza el elemento <code>&lt;a&gt;</code> y en el atributo <code>href</code> se utiliza <code>"#name"</code>, es decir el nombre del <em>bookmark</em> precedido por un <code>#</code>.</p>
<pre class=" language-html"><code class="prism  language-html"><span class="token comment">&lt;!-- Asignar id al elemento --&gt;</span>
<span class="token tag"><span class="token tag"><span class="token punctuation">&lt;</span>element</span> <span class="token attr-name">id</span><span class="token attr-value"><span class="token punctuation">=</span><span class="token punctuation">"</span>name<span class="token punctuation">"</span></span><span class="token punctuation">&gt;</span></span>

...

<span class="token comment">&lt;!-- Crear una referencia al elemento --&gt;</span>
<span class="token tag"><span class="token tag"><span class="token punctuation">&lt;</span>a</span> <span class="token attr-name">href</span><span class="token attr-value"><span class="token punctuation">=</span><span class="token punctuation">"</span>#name<span class="token punctuation">"</span></span><span class="token punctuation">&gt;</span></span> content <span class="token tag"><span class="token tag"><span class="token punctuation">&lt;/</span>a</span><span class="token punctuation">&gt;</span></span>
</code></pre>
<ul>
<li>Los bookmarks se suelen crear para los elementos de encabezados, tablas, imágenes, entre otros.</li>
<li>Si se quiere establecer un bookmark en otro archivo html usar en <code>href</code>: <br> <code>"path/filename.html#name"</code></li>
</ul>
<h3 id="elementos-para-layout">Elementos para Layout</h3>
<p>Son elementos que definen las diferentes partes de una página web:</p>
<ul>
<li><code>&lt;header&gt;</code>: Indica el encabezado de una página o una sección.</li>
<li><code>&lt;nav&gt;</code>: Define un conjunto de link de navegación.</li>
<li><code>&lt;section&gt;</code>: Define una sección en un documento.</li>
<li><code>&lt;article&gt;</code>: Define un contenido auto-contenido independiente.</li>
<li><code>&lt;aside&gt;</code>: Define contenido lateral.</li>
<li><code>&lt;footer&gt;</code>: Define un pie de página del documento o sección.</li>
<li><code>&lt;details&gt;</code>: Define detalles adicionales.</li>
<li><code>&lt;summary&gt;</code>: Define un título para el elemento <code>&lt;details&gt;</code>.</li>
</ul>
<h2 id="elementos-de-html">Elementos de HTML</h2>
<p><code>&lt;html&gt;</code>: Representa la raíz de un documento HTML. Permite los elementos <code>&lt;head&gt;</code> y <code>&lt;body&gt;</code>.</p>
<pre class=" language-html"><code class="prism  language-html"><span class="token tag"><span class="token tag"><span class="token punctuation">&lt;</span>html</span><span class="token punctuation">&gt;</span></span> 
	<span class="token tag"><span class="token tag"><span class="token punctuation">&lt;</span>head</span><span class="token punctuation">&gt;</span></span> 
		content 
	<span class="token tag"><span class="token tag"><span class="token punctuation">&lt;/</span>head</span><span class="token punctuation">&gt;</span></span> 
	<span class="token tag"><span class="token tag"><span class="token punctuation">&lt;</span>body</span><span class="token punctuation">&gt;</span></span> 
		content 
	<span class="token tag"><span class="token tag"><span class="token punctuation">&lt;/</span>body</span><span class="token punctuation">&gt;</span></span> 
<span class="token tag"><span class="token tag"><span class="token punctuation">&lt;/</span>html</span><span class="token punctuation">&gt;</span></span>
</code></pre>
<p><strong>Atributos de &lt;html&gt;</strong>:</p>
<ul>
<li>Para una lista completa visitar la  <a href="https://developer.mozilla.org/en-US/docs/Web/HTML/Element/html#attributes">documentación</a>.</li>
<li><code>lang</code>: Indica el idioma de la página web, es recomendado indicarlo. Para consultar los posibles valores, visitar <a href="https://www.w3schools.com/tags/ref_language_codes.asp">esta página</a></li>
</ul>
<h3 id="head">&lt;head&gt;</h3>
<p>Provee información general acerca del documento, incluyendo el título, enlaces a scripts de JS y hojas de estilo de CSS, entre otros datos. Los elementos que se indiquen no se visualizan en el navegador web.</p>
<pre class=" language-html"><code class="prism  language-html"><span class="token tag"><span class="token tag"><span class="token punctuation">&lt;</span>head</span><span class="token punctuation">&gt;</span></span>  
	content
<span class="token tag"><span class="token tag"><span class="token punctuation">&lt;/</span>head</span><span class="token punctuation">&gt;</span></span> 
</code></pre>
<ul>
<li>Para más información consultar la <a href="https://developer.mozilla.org/en-US/docs/Web/HTML/Element/head">documentación</a></li>
</ul>
<br>
<h4 id="titulos">Titulos:</h4>
<p><code>&lt;title&gt;</code>: Indica el título de un documento, es el nombre que aparecerá en la pestaña del navegador al tener la página abierta. Importante. Todos los documentos deben de tener un título. También es el nombre que aparecerá en los resultados de los buscadores.</p>
<pre class=" language-html"><code class="prism  language-html"><span class="token tag"><span class="token tag"><span class="token punctuation">&lt;</span>head</span><span class="token punctuation">&gt;</span></span>
	<span class="token tag"><span class="token tag"><span class="token punctuation">&lt;</span>title</span><span class="token punctuation">&gt;</span></span> Título <span class="token tag"><span class="token tag"><span class="token punctuation">&lt;/</span>title</span><span class="token punctuation">&gt;</span></span>
<span class="token tag"><span class="token tag"><span class="token punctuation">&lt;/</span>head</span><span class="token punctuation">&gt;</span></span> 
</code></pre>
<ul>
<li>Para más información consultar la <a href="https://developer.mozilla.org/en-US/docs/Web/HTML/Element/title">documentación</a></li>
<li><strong>Importante</strong>: Todos los documentos deben de tener un título que debe estar dentro de <code>&lt;head&gt;</code>.</li>
</ul>
<br>
<p><strong>Atributos</strong>:</p>
<ul>
<li>lang : Lenguaje del elemento.</li>
</ul>
<br>
<h4 id="metadata">Metadata:</h4>
<p><code>&lt;meta&gt;</code>: Provee información sobre el documento. No tiene etiqueta de cierre. Algunos usos es especificar el conjunto de caracteres a usar en la página, descripción de la página, keywords, autor del documento, etc. Se pone un meta por cada información que se quiera proveer.</p>
<pre class=" language-html"><code class="prism  language-html"><span class="token tag"><span class="token tag"><span class="token punctuation">&lt;</span>head</span><span class="token punctuation">&gt;</span></span>
	<span class="token tag"><span class="token tag"><span class="token punctuation">&lt;</span>meta</span> <span class="token attr-name">attrs</span><span class="token punctuation">/&gt;</span></span>
<span class="token tag"><span class="token tag"><span class="token punctuation">&lt;/</span>head</span><span class="token punctuation">&gt;</span></span>  
</code></pre>
<ul>
<li>No tiene contenido.</li>
<li>Se recomienda usar el siguiente <em>meta</em> en todos los documentos HTML, para controlar las dimensiones y escala de la página, particularmente en dispositivos móviles: <br> <code>&lt;meta name="viewport" content="width=device-width, initial-scale=1.0"&gt;</code></li>
<li>Para más información consultar la <a href="https://developer.mozilla.org/en-US/docs/Web/HTML/Element/meta">documentación</a></li>
</ul>
<br>
<p><strong>Atributos</strong>:</p>
<ul>
<li><code>charset</code>:Permite indicar el conjunto de caracteres que tendrá la página web. Algunos valores posibles son:
<ul>
<li><code>"utf-8"</code></li>
</ul>
</li>
<li><code>name</code>: Nombre de la característica meta. Como keywords, description, author. Para una lista completa visitar la <a href="https://developer.mozilla.org/en-US/docs/Web/HTML/Element/meta/name#standard_metadata_names_defined_in_the_html_specification">documentación</a>. Valores comunes:
<ul>
<li><code>author</code>: El nombre del autor del documento.</li>
<li><code>description</code>: Un resumen breve y preciso del contenido de la página.</li>
<li><code>keywords</code>: Palabras relevantes para el contenido de la página separadas por comas.</li>
</ul>
</li>
<li><code>content</code>: Contenido del atributo <code>name</code>.</li>
</ul>
<h4 id="estilos-css">Estilos CSS:</h4>
<p><code>&lt;style&gt;</code>: Establece el estilo CSS general de la página.</p>
<pre class=" language-html"><code class="prism  language-html"><span class="token tag"><span class="token tag"><span class="token punctuation">&lt;</span>head</span><span class="token punctuation">&gt;</span></span>
	<span class="token tag"><span class="token tag"><span class="token punctuation">&lt;</span>style</span><span class="token punctuation">&gt;</span></span><span class="token style language-css">   
		content  
	</span><span class="token tag"><span class="token tag"><span class="token punctuation">&lt;/</span>style</span><span class="token punctuation">&gt;</span></span>
<span class="token tag"><span class="token tag"><span class="token punctuation">&lt;/</span>head</span><span class="token punctuation">&gt;</span></span> 
</code></pre>
<ul>
<li>Para más información consultar la <a href="https://developer.mozilla.org/en-US/docs/Web/HTML/Element/style">documentación</a></li>
<li>El contenido son los estilos CSS, de la misma manera como se definirían en una hoja de estilo. Ejemplo</li>
</ul>
<pre class=" language-html"><code class="prism  language-html"><span class="token tag"><span class="token tag"><span class="token punctuation">&lt;</span>head</span><span class="token punctuation">&gt;</span></span>
	<span class="token tag"><span class="token tag"><span class="token punctuation">&lt;</span>style</span><span class="token punctuation">&gt;</span></span><span class="token style language-css">   
		<span class="token selector">h1: </span><span class="token punctuation">{</span>
			<span class="token property">attr</span><span class="token punctuation">:</span> val<span class="token punctuation">;</span> 
			<span class="token property">attr</span><span class="token punctuation">:</span> val<span class="token punctuation">;</span>
			<span class="token number">...</span>
		<span class="token punctuation">}</span>
		<span class="token number">...</span>   
	</span><span class="token tag"><span class="token tag"><span class="token punctuation">&lt;/</span>style</span><span class="token punctuation">&gt;</span></span>
<span class="token tag"><span class="token tag"><span class="token punctuation">&lt;/</span>head</span><span class="token punctuation">&gt;</span></span> 
</code></pre>
<br>
<h4 id="links">Links:</h4>
<p><code>&lt;link&gt;</code>: Especifica la relación entre un documento actual y un archivo externo. Se suele utilizar para enlazar con hojas de estilos. No tiene etiqueta de cierre.</p>
<pre class=" language-html"><code class="prism  language-html"><span class="token tag"><span class="token tag"><span class="token punctuation">&lt;</span>head</span><span class="token punctuation">&gt;</span></span>
	<span class="token tag"><span class="token tag"><span class="token punctuation">&lt;</span>link</span> <span class="token punctuation">/&gt;</span></span> 
<span class="token tag"><span class="token tag"><span class="token punctuation">&lt;/</span>head</span><span class="token punctuation">&gt;</span></span> 
</code></pre>
<ul>
<li>Para más información consultar la <a href="https://developer.mozilla.org/en-US/docs/Web/HTML/Element/link">documentación</a></li>
</ul>
<p><strong>Atributos</strong>:</p>
<ul>
<li><code>rel</code>: Indica la relación del documento enlazado con el actual. Si es una hoja se estilos se utiliza stylesheet.
<ul>
<li><code>"stylesheet"</code>: Enlaces a una hoja de estilo externa. Este es el uso más común del atributo rel.</li>
<li><code>"alternate"</code>: Enlaces a una versión alternativa del documento. Esto se puede usar para proporcionar diferentes versiones del documento para diferentes idiomas, dispositivos u otros criterios.</li>
<li><code>"icon"</code>: Enlaces a un icono del documento. Este icono suele mostrarse en la barra de pestañas del navegador y en las listas de marcadores.</li>
</ul>
</li>
<li><code>href</code>: URL o ruta al archivo externo.</li>
<li><code>type</code>: Es usado para definir el tipo de contenido al que se enlaza. El valor debe de ser un tipo MIME, como “text/html”, “text/css”, “image/x-icon”, etc.</li>
</ul>
<br>
<h4 id="js-scripts">JS Scripts</h4>
<p><code>&lt;script&gt;</code>: Puede contener sentencias de JavaScript o apuntar a un script externo.</p>
<pre class=" language-html"><code class="prism  language-html"><span class="token tag"><span class="token tag"><span class="token punctuation">&lt;</span>head</span><span class="token punctuation">&gt;</span></span>
	<span class="token tag"><span class="token tag"><span class="token punctuation">&lt;</span>script</span><span class="token punctuation">&gt;</span></span><span class="token script language-javascript">
		content
	</span><span class="token tag"><span class="token tag"><span class="token punctuation">&lt;/</span>script</span><span class="token punctuation">&gt;</span></span> 
<span class="token tag"><span class="token tag"><span class="token punctuation">&lt;/</span>head</span><span class="token punctuation">&gt;</span></span> 
</code></pre>
<ul>
<li><em>content</em> es directamente el código de JavaScript. En caso de que sea un script externo no es necesario poner nada.</li>
<li>Para más información consultar la <a href="https://developer.mozilla.org/en-US/docs/Web/HTML/Element/script">documentación</a></li>
</ul>
<p><strong>Atributos</strong>:</p>
<ul>
<li><code>href</code>: URL de un script externo. Puede ser ruta relativas o absolutas.</li>
</ul>
<br>
<h4 id="url-base">URL Base</h4>
<p><code>&lt;base&gt;</code>: Establece el URL base para todos los documentos, imágenes, etc. relativos en el proyecto. Solo puede haber un elemento <code>&lt;base&gt;</code> en el documento. Debe de tener al menos un atributo <code>href</code> o <code>target</code>.</p>
<pre class=" language-html"><code class="prism  language-html"><span class="token tag"><span class="token tag"><span class="token punctuation">&lt;</span>head</span><span class="token punctuation">&gt;</span></span>
	<span class="token tag"><span class="token tag"><span class="token punctuation">&lt;</span>base</span><span class="token punctuation">/&gt;</span></span>
<span class="token tag"><span class="token tag"><span class="token punctuation">&lt;/</span>head</span><span class="token punctuation">&gt;</span></span> 
</code></pre>
<ul>
<li>No tiene contenido ni etiqueta de cierre.</li>
<li>Para más información consultar la <a href="https://developer.mozilla.org/en-US/docs/Web/HTML/Element/base">documentación</a></li>
</ul>
<p><strong>Atributos</strong>:</p>
<ul>
<li>
<p><code>href</code>: URL base.</p>
</li>
<li>
<p><code>target</code>: Objetivo base.</p>
</li>
<li>
<p><code>&lt;blockquote&gt;</code>: Define una sección que es una cita de otra fuente: <code>&lt;blockquote cite="URL"&gt; texto &lt;/blockquote&gt;</code> </p><blockquote> ejemplo </blockquote><p></p>
<ul>
<li>cite: URL o ruta del documento original.</li>
</ul>
</li>
<li>
<p><code>&lt;q&gt;</code> - Quotation: Define una cita pequeña, el texto se pondrá entre comillas. <q> ejemplo </q> <br> <code>&lt;q&gt; content &lt;/q&gt;</code></p>
</li>
<li>
<p><code>&lt;abbr&gt;</code> - Abbrevation: Define una abreviación o acrónimos. Puede ser de utilidad para navegadores, sistemas de traducción y buscadores: <abbr> Ejm </abbr> <br> <code>&lt;abbr&gt; content &lt;/abbr&gt;</code></p>
</li>
<li>
<p><code>&lt;address&gt;</code>: Define la información de contacto del autor o dueño de un documento o artículo. Normalmente se mostrará en cursiva: </p><address> Ejemplo </address> <br> <code>&lt;address&gt; content &lt;/address&gt;</code><p></p>
</li>
<li>
<p><code>&lt;cite&gt;</code>: Define el título de un trabajo creativo, como libros, poemas, canciones, películas, pinturas, esculturas, etc. Normalmente se muestra en cursiva: <cite> ejemplo </cite> <br> <code>&lt;cite&gt; content &lt;/cite&gt;</code></p>
</li>
<li>
<p><code>&lt;bdo&gt;</code> - Bi-Dideractional Override: Pone el texto en sentido contrario: <bdo> ejemplo </bdo> <br> <code>&lt;bdo&gt; content &lt;/bdo&gt;</code></p>
</li>
</ul>
<h3 id="body">&lt;body&gt;</h3>
<p>Representa el contenido de un documento HTML. Será el contenido que se visualizará en la página web. <strong>Importante</strong>: Solo puede haber un elemento <code>&lt;body&gt;</code> en cada documento.</p>
<pre class=" language-html"><code class="prism  language-html"><span class="token tag"><span class="token tag"><span class="token punctuation">&lt;</span>body</span><span class="token punctuation">&gt;</span></span>  
	content
<span class="token tag"><span class="token tag"><span class="token punctuation">&lt;/</span>body</span><span class="token punctuation">&gt;</span></span> 
</code></pre>
<ul>
<li>Para más información consultar la <a href="https://developer.mozilla.org/en-US/docs/Web/HTML/Element/body">documentación</a>.</li>
</ul>
<br>
<h4 id="contenedor-de-bloque">Contenedor de bloque:</h4>
<p><code>&lt;div&gt;</code>: Sirve para crear secciones o agrupar contenido en un documento HTML. Es un contenedor de otros elementos HTML. Se puede usar para darle estilo a bloques de contenido.</p>
<pre class=" language-html"><code class="prism  language-html"><span class="token tag"><span class="token tag"><span class="token punctuation">&lt;</span>body</span><span class="token punctuation">&gt;</span></span> 
	<span class="token tag"><span class="token tag"><span class="token punctuation">&lt;</span>div</span><span class="token punctuation">&gt;</span></span>
		content
	<span class="token tag"><span class="token tag"><span class="token punctuation">&lt;/</span>div</span><span class="token punctuation">&gt;</span></span> 
<span class="token tag"><span class="token tag"><span class="token punctuation">&lt;/</span>body</span><span class="token punctuation">&gt;</span></span> 
</code></pre>
<ul>
<li>Para más información consultar la <a href="https://developer.mozilla.org/en-US/docs/Web/HTML/Element/div">documentación</a>.</li>
</ul>
<br>
<h4 id="contenedor-inline">Contenedor Inline</h4>
<p><code>&lt;span&gt;</code>: Es un contenedor en línea, sirve para aplicar estilo al texto o agrupar elementos en línea.</p>
<pre class=" language-html"><code class="prism  language-html"><span class="token tag"><span class="token tag"><span class="token punctuation">&lt;</span>body</span><span class="token punctuation">&gt;</span></span> 
	<span class="token tag"><span class="token tag"><span class="token punctuation">&lt;</span>span</span><span class="token punctuation">&gt;</span></span>
		content
	<span class="token tag"><span class="token tag"><span class="token punctuation">&lt;/</span>span</span><span class="token punctuation">&gt;</span></span> 
<span class="token tag"><span class="token tag"><span class="token punctuation">&lt;/</span>body</span><span class="token punctuation">&gt;</span></span> 
</code></pre>
<ul>
<li>Para más información consultar la <a href="https://developer.mozilla.org/en-US/docs/Web/HTML/Element/span">documentación</a>.</li>
</ul>
<br>
<h4 id="parrafos">Parrafos:</h4>
<p><code>&lt;p&gt;</code>: Es el elemento para distribuir texto en párrafos. Puede contener cero o más elementos en línea. No se respetan saltos de línea en el código.</p>
<pre class=" language-html"><code class="prism  language-html"><span class="token tag"><span class="token tag"><span class="token punctuation">&lt;</span>body</span><span class="token punctuation">&gt;</span></span>
	<span class="token tag"><span class="token tag"><span class="token punctuation">&lt;</span>p</span><span class="token punctuation">&gt;</span></span> text <span class="token tag"><span class="token tag"><span class="token punctuation">&lt;/</span>p</span><span class="token punctuation">&gt;</span></span> 
<span class="token tag"><span class="token tag"><span class="token punctuation">&lt;/</span>body</span><span class="token punctuation">&gt;</span></span> 
</code></pre>
<ul>
<li><em>text</em> es cualquier texto que irá en el párrafo.</li>
<li>Para más información consultar la <a href="https://developer.mozilla.org/en-US/docs/Web/HTML/Element/p">documentación</a>.</li>
</ul>
<p><strong>Atributos</strong>:</p>
<ul>
<li><code>title</code>: Texto que aparecerá al poner el cursor sobre el párrafo.</li>
<li><code>style</code>: Determina el estilo del párrafo.</li>
</ul>
<hr>
<p><code>&lt;pre&gt;</code>: Define un texto que preserva saltos de línea y espacios en blanco.</p>
<pre class=" language-html"><code class="prism  language-html"><span class="token tag"><span class="token tag"><span class="token punctuation">&lt;</span>body</span><span class="token punctuation">&gt;</span></span>
	<span class="token tag"><span class="token tag"><span class="token punctuation">&lt;</span>pre</span><span class="token punctuation">&gt;</span></span> text <span class="token tag"><span class="token tag"><span class="token punctuation">&lt;/</span>pre</span><span class="token punctuation">&gt;</span></span> 
<span class="token tag"><span class="token tag"><span class="token punctuation">&lt;/</span>body</span><span class="token punctuation">&gt;</span></span> 
</code></pre>
<ul>
<li><em>text</em> es cualquier texto que irá en el párrafo.</li>
<li>Para más información consultar la <a href="https://developer.mozilla.org/en-US/docs/Web/HTML/Element/p">documentación</a>.</li>
</ul>
<br>
<h4 id="títulos">Títulos:</h4>
<p><code>h<em>group</em></code>: Son elementos de grupos de cabecera, representan el encabezado de una sección. Definen un título que participa en la estructura del documento. Incluyen de las etiquetas <code>&lt;h1&gt;</code> a <code>&lt;h6&gt;</code>, siendo <code>&lt;h1&gt;</code> el encabezado principal. Agregan un salto de línea automáticamente.</p>
<pre class=" language-html"><code class="prism  language-html"><span class="token tag"><span class="token tag"><span class="token punctuation">&lt;</span>body</span><span class="token punctuation">&gt;</span></span> 
	<span class="token tag"><span class="token tag"><span class="token punctuation">&lt;</span>h1</span><span class="token punctuation">&gt;</span></span> Encabezado 1<span class="token tag"><span class="token tag"><span class="token punctuation">&lt;/</span>h1</span><span class="token punctuation">&gt;</span></span>
	<span class="token tag"><span class="token tag"><span class="token punctuation">&lt;</span>h2</span><span class="token punctuation">&gt;</span></span> Encabezado 2<span class="token tag"><span class="token tag"><span class="token punctuation">&lt;/</span>h2</span><span class="token punctuation">&gt;</span></span>
	<span class="token tag"><span class="token tag"><span class="token punctuation">&lt;</span>h3</span><span class="token punctuation">&gt;</span></span> Encabezado 3<span class="token tag"><span class="token tag"><span class="token punctuation">&lt;/</span>h3</span><span class="token punctuation">&gt;</span></span>
	<span class="token tag"><span class="token tag"><span class="token punctuation">&lt;</span>h4</span><span class="token punctuation">&gt;</span></span> Encabezado 4<span class="token tag"><span class="token tag"><span class="token punctuation">&lt;/</span>h4</span><span class="token punctuation">&gt;</span></span>
	<span class="token tag"><span class="token tag"><span class="token punctuation">&lt;</span>h5</span><span class="token punctuation">&gt;</span></span> Encabezado 5<span class="token tag"><span class="token tag"><span class="token punctuation">&lt;/</span>h5</span><span class="token punctuation">&gt;</span></span>
	<span class="token tag"><span class="token tag"><span class="token punctuation">&lt;</span>h6</span><span class="token punctuation">&gt;</span></span> Encabezado 6<span class="token tag"><span class="token tag"><span class="token punctuation">&lt;/</span>h6</span><span class="token punctuation">&gt;</span></span>
<span class="token tag"><span class="token tag"><span class="token punctuation">&lt;/</span>body</span><span class="token punctuation">&gt;</span></span> 
</code></pre>
<ul>
<li>Para más información consultar la <a href="https://developer.mozilla.org/en-US/docs/Web/HTML/Element/hgroup">documentación</a>.</li>
</ul>
<br>
<h4 id="saltos-de-línea">Saltos de línea:</h4>
<p><code>&lt;br&gt;</code>: Es un salto de línea (<em>line break</em>) que produce un salto de línea en el texto. No tiene contenido por lo que se cierra como <code>&lt;/&gt;</code> en una sola etiqueta.</p>
<pre class=" language-html"><code class="prism  language-html"><span class="token tag"><span class="token tag"><span class="token punctuation">&lt;</span>body</span><span class="token punctuation">&gt;</span></span> 
	<span class="token tag"><span class="token tag"><span class="token punctuation">&lt;</span>br</span><span class="token punctuation">/&gt;</span></span> 
<span class="token tag"><span class="token tag"><span class="token punctuation">&lt;/</span>body</span><span class="token punctuation">&gt;</span></span> 
</code></pre>
<ul>
<li>Para más información consultar la <a href="https://developer.mozilla.org/en-US/docs/Web/HTML/Element/br">documentación</a>.</li>
</ul>
<br>
<h4 id="líneas-divisoras-de-texto">Líneas divisoras de texto:</h4>
<p><code>&lt;hr&gt;</code>: “Horizontal rule” agrega una línea horizontal para crear divisiones en elementos de la página. No tiene contenido por lo que se cierra como <code>&lt;/&gt;</code> en una sola etiqueta.</p>
<pre class=" language-html"><code class="prism  language-html"><span class="token tag"><span class="token tag"><span class="token punctuation">&lt;</span>body</span><span class="token punctuation">&gt;</span></span>
	<span class="token tag"><span class="token tag"><span class="token punctuation">&lt;</span>hr</span><span class="token punctuation">/&gt;</span></span> 
<span class="token tag"><span class="token tag"><span class="token punctuation">&lt;/</span>body</span><span class="token punctuation">&gt;</span></span> 
</code></pre>
<ul>
<li>Para más información consultar la <a href="https://developer.mozilla.org/en-US/docs/Web/HTML/Element/hr">documentación</a>.</li>
</ul>
<br>
<h4 id="formato-de-texto">Formato de texto:</h4>
<p>A continuación se enlistan diversas etiquetas que sirven para darle formato al texto en etiquetas como <code>&lt;p&gt;</code> o <code>&lt;span&gt;</code>.</p>
<ul>
<li><code>&lt;b&gt;</code> - Bold: Texto en negritas: <b>ejemplo</b> <br> <code>&lt;b&gt; texto &lt;/b&gt;</code></li>
<li><code>&lt;strong&gt;</code> - Strong: Es para indicar que el texto es importante. El formato es el mismo que el de negritas, pero el significado es distinto: <strong>ejemplo</strong> <br> - <code>&lt;strong&gt; texto &lt;/strong&gt;</code></li>
<li><code>&lt;i&gt;</code> - Italic: Es para poner un texto en cursiva/itálica: <i>ejemplo</i> <br> <code>&lt;i&gt; texto &lt;/i&gt;</code></li>
<li><code>&lt;em&gt;</code> - Emphasize: Es para enfatizar un texto, el resultado es similar a itálica, pero el significado es distinto: <em>ejemplo</em>  <br> <code>&lt;em&gt; texto &lt;/em&gt;</code></li>
<li><code>&lt;del&gt;</code> - Deleted: Es para tachar un texto: <del>ejemplo</del> <br> <code>&lt;del&gt; texto &lt;/del&gt;</code></li>
<li><code>&lt;ins&gt;</code> - Inserted: Es insertar un texto, pero se ve como un texto subrayado: <ins>ejemplo</ins>  <br> <code>&lt;ins&gt; texto &lt;/ins&gt;</code></li>
<li><code>&lt;sub&gt;</code> - Subscript: Es para que un texto aparezca como subíndice: X<sub>ejemplo</sub>  <br> <code>&lt;sub&gt; texto &lt;/sub&gt;</code></li>
<li><code>&lt;sup&gt;</code> - Superscript: Es para que un texto aparezca como superíndice: X<sup>ejemplo</sup>  <br> <code>&lt;sup&gt; texto &lt;/sup&gt;</code></li>
<li><code>&lt;small&gt;</code> - Small: Pone un texto de un tamaño menor: <small>ejemplo</small> <br> <code>&lt;small&gt; texto &lt;/small&gt;</code></li>
<li><code>&lt;mark&gt;</code> - Mark: Es para resaltar un texto, somo si estuviera subrayado con un marcador: <mark>ejemplo</mark> <br> <code>&lt;mark&gt; texto &lt;/mark&gt;</code></li>
</ul>
<br>
<h4 id="formato-como-código.">Formato como código.</h4>
<ul>
<li><code>&lt;kbd&gt;</code>: Se utiliza para definir acciones con el teclado, como indicar al usuario que presiones ciertas teclas. Lo único que hace esta etiqueta es cambiar el formato del contenido: <kbd>ejemplo</kbd>  <br> <code>&lt;kbd&gt; content &lt;/kbd&gt;</code></li>
<li><code>&lt;samp&gt;</code>: Se utiliza para definir mostrar el output de un programa de computadora. Lo único que hace esta etiqueta es cambiar el formato del contenido: <samp>ejemplo</samp> <br> <code>&lt;samp&gt; content &lt;/samp&gt;</code></li>
<li><code>&lt;code&gt;</code>: Es para definir el texto como si fuera código. Lo único que hace esta etiqueta es cambiar el formato del contenido: <code>ejemplo</code> <br> <code>&lt;code&gt; content &lt;/code&gt;</code></li>
<li><code>&lt;var&gt;</code>: Es para definir variables en programación o matemáticas. Lo único que hace esta etiqueta es cambiar el formato del contenido: <var>ejemplo</var>  <br> <code>&lt;var&gt; content &lt;/var&gt;</code></li>
</ul>
<br>
<h4 id="citas">Citas:</h4>
<ul>
<li><code>&lt;blockquote&gt;</code>: Define una sección que es una cita de otra fuente: <code>&lt;blockquote cite="URL"&gt; texto &lt;/blockquote&gt;</code> <blockquote> ejemplo </blockquote>
<ul>
<li>cite: URL o ruta del documento original.</li>
</ul>
</li>
<li><code>&lt;q&gt;</code> - Quotation: Define una cita pequeña, el texto se pondrá entre comillas. <q> ejemplo </q> <br> <code>&lt;q&gt; content &lt;/q&gt;</code></li>
<li><code>&lt;abbr&gt;</code> - Abbrevation: Define una abreviación o acrónimos. Puede ser de utilidad para navegadores, sistemas de traducción y buscadores: <abbr> Ejm </abbr> <br> <code>&lt;abbr&gt; content &lt;/abbr&gt;</code></li>
<li><code>&lt;address&gt;</code>: Define la información de contacto del autor o dueño de un documento o artículo. Normalmente se mostrará en cursiva: <code>&lt;address&gt; content &lt;/address&gt;</code> <address> Ejemplo </address></li>
<li><code>&lt;cite&gt;</code>: Define el título de un trabajo creativo, como libros, poemas, canciones, películas, pinturas, esculturas, etc. Normalmente se muestra en cursiva: <cite> ejemplo </cite> <br> <code>&lt;cite&gt; content &lt;/cite&gt;</code></li>
<li><code>&lt;bdo&gt;</code> - Bi-Dideractional Override: Pone el texto en sentido contrario: <bdo> ejemplo </bdo> <br> <code>&lt;bdo&gt; content &lt;/bdo&gt;</code></li>
</ul>
<br>
<h4 id="links-1">Links:</h4>
<p><code>&lt;a&gt;</code>: Agrega un link. Cualquier elemento HTML puede ser un link.</p>
<pre class=" language-html"><code class="prism  language-html"><span class="token tag"><span class="token tag"><span class="token punctuation">&lt;</span>body</span><span class="token punctuation">&gt;</span></span>
	<span class="token tag"><span class="token tag"><span class="token punctuation">&lt;</span>a</span> <span class="token attr-name">href</span><span class="token attr-value"><span class="token punctuation">=</span><span class="token punctuation">"</span>url<span class="token punctuation">"</span></span> <span class="token attr-name">target</span><span class="token attr-value"><span class="token punctuation">=</span><span class="token punctuation">"</span>value<span class="token punctuation">"</span></span><span class="token punctuation">&gt;</span></span> link <span class="token tag"><span class="token tag"><span class="token punctuation">&lt;/</span>a</span><span class="token punctuation">&gt;</span></span> 
<span class="token tag"><span class="token tag"><span class="token punctuation">&lt;/</span>body</span><span class="token punctuation">&gt;</span></span> 
</code></pre>
<ul>
<li><em>link</em> es la parte que será visible al usuario y que al presionar sobre ella se abrirá el link.</li>
<li>Para más información consultar la <a href="https://developer.mozilla.org/en-US/docs/Web/HTML/Element/a">documentación</a>.</li>
</ul>
<p><strong>Atributos</strong>:</p>
<ul>
<li><code>href</code>: URL de la página o ruta de otro archivo HTML.</li>
<li><code>target</code>: Especifica cómo desplegar la URL. Algunos valores posibles son:
<ul>
<li><code>_self</code> (default): Abre la url en la misma pestaña que la actual.</li>
<li><code>_blank</code>: Abre la url en una pestaña nueva, aunque dependiendo de la configuración de los usuarios del navegador puede ser una ventana nueva.</li>
<li><code>_parent</code>: Abre el url en el <em>parent frame</em>.</li>
<li><code>_top</code>: Abre el url en el cuerpo completo de la ventana.</li>
</ul>
</li>
</ul>
<br>
<h4 id="imágenes.">Imágenes.</h4>
<p><code>&lt;img&gt;</code>: Agrega una imagen a la página web. No tiene contenido por lo que se cierra como <code>&lt;/&gt;</code> en una sola etiqueta.</p>
<pre class=" language-html"><code class="prism  language-html"><span class="token tag"><span class="token tag"><span class="token punctuation">&lt;</span>body</span><span class="token punctuation">&gt;</span></span>
	<span class="token tag"><span class="token tag"><span class="token punctuation">&lt;</span>img</span> <span class="token attr-name">scr</span><span class="token attr-value"><span class="token punctuation">=</span><span class="token punctuation">"</span>URL<span class="token punctuation">"</span></span><span class="token punctuation">/&gt;</span></span>
<span class="token tag"><span class="token tag"><span class="token punctuation">&lt;/</span>body</span><span class="token punctuation">&gt;</span></span> 
</code></pre>
<ul>
<li>Lo normal es agregar las imágenes en subcarpetas del proyecto.</li>
<li>Para más información consultar la <a href="https://developer.mozilla.org/en-US/docs/Web/HTML/Element/img">documentación</a>.</li>
</ul>
<p><strong>Atributos</strong>:</p>
<ul>
<li><code>src</code>: Ruta de la imagen, desde el directorio local, es decir, partiendo del directorio donde está el proyecto. También puede ser una URL en internet.</li>
<li><code>alt</code>: Representa un texto alternativo en caso de que la imagen no se pueda mostrar correctamente, es recomendado poner un texto alternativo a todas las imágenes.</li>
<li><code>height</code>: Alto de la imagen en pixeles CSS o pixeles. Por ejemplo “10px”. Si no se especifica width entonces se determinará automáticamente.</li>
<li><code>width</code>: Ancho de la imagen en pixeles CSS o pixeles. Por ejemplo “10px”. Si no se especifica height entonces se determinará automáticamente.</li>
<li><code>title</code>: Texto que aparecerá al poner el cursor sobre la imagen.</li>
<li><code>style</code>: Define el estilo del elemento.</li>
</ul>
<h4 id="tablas">Tablas:</h4>
<p>Para crear una tabla es HTML es necesario utilizar diversas etiquetas para definir los elementos de la tabla, a continuación se muesta un ejemplo general</p>
<pre class=" language-html"><code class="prism  language-html"><span class="token tag"><span class="token tag"><span class="token punctuation">&lt;</span>table</span><span class="token punctuation">&gt;</span></span>
  <span class="token tag"><span class="token tag"><span class="token punctuation">&lt;</span>thead</span><span class="token punctuation">&gt;</span></span>
    <span class="token tag"><span class="token tag"><span class="token punctuation">&lt;</span>tr</span><span class="token punctuation">&gt;</span></span>
      <span class="token tag"><span class="token tag"><span class="token punctuation">&lt;</span>th</span><span class="token punctuation">&gt;</span></span>Name<span class="token tag"><span class="token tag"><span class="token punctuation">&lt;/</span>th</span><span class="token punctuation">&gt;</span></span>
      <span class="token tag"><span class="token tag"><span class="token punctuation">&lt;</span>th</span><span class="token punctuation">&gt;</span></span>Age<span class="token tag"><span class="token tag"><span class="token punctuation">&lt;/</span>th</span><span class="token punctuation">&gt;</span></span>
      <span class="token tag"><span class="token tag"><span class="token punctuation">&lt;</span>th</span><span class="token punctuation">&gt;</span></span>Occupation<span class="token tag"><span class="token tag"><span class="token punctuation">&lt;/</span>th</span><span class="token punctuation">&gt;</span></span>
    <span class="token tag"><span class="token tag"><span class="token punctuation">&lt;/</span>tr</span><span class="token punctuation">&gt;</span></span>
  <span class="token tag"><span class="token tag"><span class="token punctuation">&lt;/</span>thead</span><span class="token punctuation">&gt;</span></span>
  <span class="token tag"><span class="token tag"><span class="token punctuation">&lt;</span>tbody</span><span class="token punctuation">&gt;</span></span>
    <span class="token tag"><span class="token tag"><span class="token punctuation">&lt;</span>tr</span><span class="token punctuation">&gt;</span></span>
      <span class="token tag"><span class="token tag"><span class="token punctuation">&lt;</span>td</span><span class="token punctuation">&gt;</span></span>John Doe<span class="token tag"><span class="token tag"><span class="token punctuation">&lt;/</span>td</span><span class="token punctuation">&gt;</span></span>
      <span class="token tag"><span class="token tag"><span class="token punctuation">&lt;</span>td</span><span class="token punctuation">&gt;</span></span>30<span class="token tag"><span class="token tag"><span class="token punctuation">&lt;/</span>td</span><span class="token punctuation">&gt;</span></span>
      <span class="token tag"><span class="token tag"><span class="token punctuation">&lt;</span>td</span><span class="token punctuation">&gt;</span></span>Software Engineer<span class="token tag"><span class="token tag"><span class="token punctuation">&lt;/</span>td</span><span class="token punctuation">&gt;</span></span>
    <span class="token tag"><span class="token tag"><span class="token punctuation">&lt;/</span>tr</span><span class="token punctuation">&gt;</span></span>
    <span class="token tag"><span class="token tag"><span class="token punctuation">&lt;</span>tr</span><span class="token punctuation">&gt;</span></span>
      <span class="token tag"><span class="token tag"><span class="token punctuation">&lt;</span>td</span><span class="token punctuation">&gt;</span></span>Jane Smith<span class="token tag"><span class="token tag"><span class="token punctuation">&lt;/</span>td</span><span class="token punctuation">&gt;</span></span>
      <span class="token tag"><span class="token tag"><span class="token punctuation">&lt;</span>td</span><span class="token punctuation">&gt;</span></span>25<span class="token tag"><span class="token tag"><span class="token punctuation">&lt;/</span>td</span><span class="token punctuation">&gt;</span></span>
      <span class="token tag"><span class="token tag"><span class="token punctuation">&lt;</span>td</span><span class="token punctuation">&gt;</span></span>Marketing Manager<span class="token tag"><span class="token tag"><span class="token punctuation">&lt;/</span>td</span><span class="token punctuation">&gt;</span></span>
    <span class="token tag"><span class="token tag"><span class="token punctuation">&lt;/</span>tr</span><span class="token punctuation">&gt;</span></span>
    <span class="token tag"><span class="token tag"><span class="token punctuation">&lt;</span>tr</span><span class="token punctuation">&gt;</span></span>
      <span class="token tag"><span class="token tag"><span class="token punctuation">&lt;</span>td</span><span class="token punctuation">&gt;</span></span>Peter Jones<span class="token tag"><span class="token tag"><span class="token punctuation">&lt;/</span>td</span><span class="token punctuation">&gt;</span></span>
      <span class="token tag"><span class="token tag"><span class="token punctuation">&lt;</span>td</span><span class="token punctuation">&gt;</span></span>40<span class="token tag"><span class="token tag"><span class="token punctuation">&lt;/</span>td</span><span class="token punctuation">&gt;</span></span>
      <span class="token tag"><span class="token tag"><span class="token punctuation">&lt;</span>td</span><span class="token punctuation">&gt;</span></span>Accountant<span class="token tag"><span class="token tag"><span class="token punctuation">&lt;/</span>td</span><span class="token punctuation">&gt;</span></span>
    <span class="token tag"><span class="token tag"><span class="token punctuation">&lt;/</span>tr</span><span class="token punctuation">&gt;</span></span>
  <span class="token tag"><span class="token tag"><span class="token punctuation">&lt;/</span>tbody</span><span class="token punctuation">&gt;</span></span>
<span class="token tag"><span class="token tag"><span class="token punctuation">&lt;/</span>table</span><span class="token punctuation">&gt;</span></span>
</code></pre>
<p>Lo anterior se visualizaría como:</p>
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
<h5 id="estructura-general">Estructura general:</h5>
<p><code>&lt;table&gt;</code>: Crea la estructura de una tabla, es necesario usar otras etiquetas como <code>&lt;thead&gt;</code> y <code>&lt;tbody&gt;</code>.</p>
<pre class=" language-html"><code class="prism  language-html"><span class="token tag"><span class="token tag"><span class="token punctuation">&lt;</span>body</span><span class="token punctuation">&gt;</span></span>
	<span class="token tag"><span class="token tag"><span class="token punctuation">&lt;</span>table</span><span class="token punctuation">&gt;</span></span> 
		<span class="token tag"><span class="token tag"><span class="token punctuation">&lt;</span>thead</span><span class="token punctuation">&gt;</span></span>
			...
  		<span class="token tag"><span class="token tag"><span class="token punctuation">&lt;/</span>thead</span><span class="token punctuation">&gt;</span></span>
  		<span class="token tag"><span class="token tag"><span class="token punctuation">&lt;</span>tbody</span><span class="token punctuation">&gt;</span></span>
    			...
  		<span class="token tag"><span class="token tag"><span class="token punctuation">&lt;/</span>tbody</span><span class="token punctuation">&gt;</span></span> 
	<span class="token tag"><span class="token tag"><span class="token punctuation">&lt;/</span>table</span><span class="token punctuation">&gt;</span></span> 
<span class="token tag"><span class="token tag"><span class="token punctuation">&lt;/</span>body</span><span class="token punctuation">&gt;</span></span> 
</code></pre>
<ul>
<li>Para más información consultar la <a href="https://developer.mozilla.org/en-US/docs/Web/HTML/Element/table">documentación</a>.</li>
</ul>
<h5 id="título">Título</h5>
<p><code>&lt;caption&gt;</code>: Agrega un título a la tabla. Se debe poner inmediatamente después de <code>&lt;table&gt;</code>:</p>
<pre class=" language-html"><code class="prism  language-html"><span class="token tag"><span class="token tag"><span class="token punctuation">&lt;</span>body</span><span class="token punctuation">&gt;</span></span>
	<span class="token tag"><span class="token tag"><span class="token punctuation">&lt;</span>table</span><span class="token punctuation">&gt;</span></span> 
		<span class="token tag"><span class="token tag"><span class="token punctuation">&lt;</span>caption</span><span class="token punctuation">&gt;</span></span> content <span class="token tag"><span class="token tag"><span class="token punctuation">&lt;/</span>caption</span><span class="token punctuation">&gt;</span></span>
		table content ...	 
	<span class="token tag"><span class="token tag"><span class="token punctuation">&lt;/</span>table</span><span class="token punctuation">&gt;</span></span> 
<span class="token tag"><span class="token tag"><span class="token punctuation">&lt;/</span>body</span><span class="token punctuation">&gt;</span></span> 
</code></pre>
<ul>
<li>Para más información consultar la <a href="https://developer.mozilla.org/en-US/docs/Web/HTML/Element/caption">documentación</a>.</li>
</ul>
<h5 id="filas">Filas:</h5>
<p><code>&lt;tr&gt;</code> - <em>Table rows</em>: Agrega una fila a un tabla. Se usa dentro de <code>&lt;thead&gt;</code> o <code>&lt;tbody&gt;</code> y usa otras etiquetas como <code>&lt;th&gt;</code> y <code>&lt;td&gt;</code>.</p>
<pre class=" language-html"><code class="prism  language-html"><span class="token tag"><span class="token tag"><span class="token punctuation">&lt;</span>body</span><span class="token punctuation">&gt;</span></span>
	<span class="token tag"><span class="token tag"><span class="token punctuation">&lt;</span>table</span><span class="token punctuation">&gt;</span></span> 
		<span class="token tag"><span class="token tag"><span class="token punctuation">&lt;</span>tr</span><span class="token punctuation">&gt;</span></span>
			content ...
		<span class="token tag"><span class="token tag"><span class="token punctuation">&lt;/</span>tr</span><span class="token punctuation">&gt;</span></span>
	<span class="token tag"><span class="token tag"><span class="token punctuation">&lt;/</span>table</span><span class="token punctuation">&gt;</span></span> 
<span class="token tag"><span class="token tag"><span class="token punctuation">&lt;/</span>body</span><span class="token punctuation">&gt;</span></span>
</code></pre>
<ul>
<li>Para más información consultar la <a href="https://developer.mozilla.org/en-US/docs/Web/HTML/Element/tr">documentación</a>.</li>
</ul>
<h5 id="encabezados-1">Encabezados:</h5>
<p><code>&lt;th&gt;</code> - <em>Table headers</em>: Agrega una celda con formato de encabezado de una tabla a una fila, se debe poner un elemento por cada columna. Se usa dentro de <code>&lt;tr&gt;</code> que representa una fila.</p>
<pre class=" language-html"><code class="prism  language-html"><span class="token tag"><span class="token tag"><span class="token punctuation">&lt;</span>body</span><span class="token punctuation">&gt;</span></span>
	<span class="token tag"><span class="token tag"><span class="token punctuation">&lt;</span>table</span><span class="token punctuation">&gt;</span></span> 
		<span class="token tag"><span class="token tag"><span class="token punctuation">&lt;</span>tr</span><span class="token punctuation">&gt;</span></span>
			<span class="token tag"><span class="token tag"><span class="token punctuation">&lt;</span>th</span><span class="token punctuation">&gt;</span></span> content <span class="token tag"><span class="token tag"><span class="token punctuation">&lt;/</span>th</span><span class="token punctuation">&gt;</span></span>
			... 
		<span class="token tag"><span class="token tag"><span class="token punctuation">&lt;/</span>tr</span><span class="token punctuation">&gt;</span></span>
	<span class="token tag"><span class="token tag"><span class="token punctuation">&lt;/</span>table</span><span class="token punctuation">&gt;</span></span> 
<span class="token tag"><span class="token tag"><span class="token punctuation">&lt;/</span>body</span><span class="token punctuation">&gt;</span></span>
</code></pre>
<ul>
<li>Para más información consultar la <a href="https://developer.mozilla.org/en-US/docs/Web/HTML/Element/th">documentación</a>.</li>
</ul>
<p><strong>Atributos</strong>:</p>
<ul>
<li><code>colspan</code>: Es para indicar el número de columnas que debe de abarcar una sola celda, se usa para combinar celdas horizontalmente.</li>
</ul>
<h5 id="celdas">Celdas</h5>
<p><code>&lt;td&gt;</code> - <em>Table data</em>: Agrega una celda con formato de datos a una fila. Es un elemento por cada columna. Se usa dentro de <code>&lt;tr&gt;</code> que representa una fila.</p>
<pre class=" language-html"><code class="prism  language-html"><span class="token tag"><span class="token tag"><span class="token punctuation">&lt;</span>body</span><span class="token punctuation">&gt;</span></span>
	<span class="token tag"><span class="token tag"><span class="token punctuation">&lt;</span>table</span><span class="token punctuation">&gt;</span></span> 
		<span class="token tag"><span class="token tag"><span class="token punctuation">&lt;</span>tr</span><span class="token punctuation">&gt;</span></span>
			<span class="token tag"><span class="token tag"><span class="token punctuation">&lt;</span>td</span><span class="token punctuation">&gt;</span></span> content <span class="token tag"><span class="token tag"><span class="token punctuation">&lt;/</span>td</span><span class="token punctuation">&gt;</span></span>
			... 
		<span class="token tag"><span class="token tag"><span class="token punctuation">&lt;/</span>tr</span><span class="token punctuation">&gt;</span></span>
	<span class="token tag"><span class="token tag"><span class="token punctuation">&lt;/</span>table</span><span class="token punctuation">&gt;</span></span> 
<span class="token tag"><span class="token tag"><span class="token punctuation">&lt;/</span>body</span><span class="token punctuation">&gt;</span></span>
</code></pre>
<ul>
<li>El contenido puede ser cualquier otro elemento de HTML como texto, imágenes, listas, otras tablas, etc.</li>
<li>Para más información consultar la <a href="https://developer.mozilla.org/en-US/docs/Web/HTML/Element/td">documentación</a>.</li>
</ul>
<p><strong>Atributos</strong>:</p>
<ul>
<li><code>rowspan</code>: Es para indicar el número de filas que debe de abarcar una sola celda, se usa como para combinar celdas verticalmente.</li>
</ul>
<h5 id="otros-elementos">Otros elementos:</h5>
<ul>
<li><code>&lt;colgroup&gt;</code>: Especifica un grupo de una o más columnas en una tabla para darles formato.</li>
<li><code>&lt;col&gt;</code>: Específica las propiedades para cada columna dentro de un elemento <code>&lt;colgroup&gt;</code>.</li>
<li><code>&lt;thead&gt;</code>: Agrupa los encabezados en una tabla.</li>
<li><code>&lt;tbody&gt;</code>: Agrupa el contenido de una tabla.</li>
<li><code>&lt;tfoot&gt;</code>: Agrupa el contenido a pie de página de una tabla.</li>
</ul>
<h4 id="listas">Listas:</h4>
<p>Existen tres tipos de listas:</p>
<ul>
<li>Ordenadas.</li>
<li>No ordenadas.</li>
<li>Listas de definición.</li>
</ul>
<h5 id="lista-no-ordenada.">Lista no ordenada.</h5>
<p><code>&lt;ul&gt;</code> - <em>Unordered list</em>: Permite definir listas no ordenadas con viñetas. Se usa junto con <code>&lt;li&gt;</code> para definir los elementos.</p>
<pre class=" language-html"><code class="prism  language-html"><span class="token tag"><span class="token tag"><span class="token punctuation">&lt;</span>body</span><span class="token punctuation">&gt;</span></span>
	<span class="token tag"><span class="token tag"><span class="token punctuation">&lt;</span>ul</span><span class="token punctuation">&gt;</span></span>
  		<span class="token tag"><span class="token tag"><span class="token punctuation">&lt;</span>li</span><span class="token punctuation">&gt;</span></span>Item 1<span class="token tag"><span class="token tag"><span class="token punctuation">&lt;/</span>li</span><span class="token punctuation">&gt;</span></span>
  		<span class="token tag"><span class="token tag"><span class="token punctuation">&lt;</span>li</span><span class="token punctuation">&gt;</span></span>Item 2<span class="token tag"><span class="token tag"><span class="token punctuation">&lt;/</span>li</span><span class="token punctuation">&gt;</span></span>
  		<span class="token tag"><span class="token tag"><span class="token punctuation">&lt;</span>li</span><span class="token punctuation">&gt;</span></span>Item 3<span class="token tag"><span class="token tag"><span class="token punctuation">&lt;/</span>li</span><span class="token punctuation">&gt;</span></span>
		...
	<span class="token tag"><span class="token tag"><span class="token punctuation">&lt;/</span>ul</span><span class="token punctuation">&gt;</span></span>
<span class="token tag"><span class="token tag"><span class="token punctuation">&lt;/</span>body</span><span class="token punctuation">&gt;</span></span>
</code></pre>
<ul>
<li>Por default se utilizan círculos pequeños negros. Para modificarlo se utiliza la propiedad <code>list-style-type</code> del atributo <code>style</code>.</li>
<li>Las etiquetas <code>&lt;li&gt;</code> puede contener otras listas, y otros elementos como imágenes, links, etc.</li>
<li>Para más información consultar la <a href="https://developer.mozilla.org/en-US/docs/Web/HTML/Element/ul">documentación</a>.</li>
</ul>
<h5 id="lista-ordenada">Lista ordenada:</h5>
<p><code>&lt;ol&gt;</code> - Ordered list: Permite definir listas ordenadas con letras o números. Se usa junto con <code>&lt;li&gt;</code> para definir los elementos.</p>
<pre class=" language-html"><code class="prism  language-html"><span class="token tag"><span class="token tag"><span class="token punctuation">&lt;</span>body</span><span class="token punctuation">&gt;</span></span>
	<span class="token tag"><span class="token tag"><span class="token punctuation">&lt;</span>ol</span><span class="token punctuation">&gt;</span></span>
  		<span class="token tag"><span class="token tag"><span class="token punctuation">&lt;</span>li</span><span class="token punctuation">&gt;</span></span>Item 1<span class="token tag"><span class="token tag"><span class="token punctuation">&lt;/</span>li</span><span class="token punctuation">&gt;</span></span>
  		<span class="token tag"><span class="token tag"><span class="token punctuation">&lt;</span>li</span><span class="token punctuation">&gt;</span></span>Item 2<span class="token tag"><span class="token tag"><span class="token punctuation">&lt;/</span>li</span><span class="token punctuation">&gt;</span></span>
  		<span class="token tag"><span class="token tag"><span class="token punctuation">&lt;</span>li</span><span class="token punctuation">&gt;</span></span>Item 3<span class="token tag"><span class="token tag"><span class="token punctuation">&lt;/</span>li</span><span class="token punctuation">&gt;</span></span>
		...
	<span class="token tag"><span class="token tag"><span class="token punctuation">&lt;/</span>ol</span><span class="token punctuation">&gt;</span></span>
<span class="token tag"><span class="token tag"><span class="token punctuation">&lt;/</span>body</span><span class="token punctuation">&gt;</span></span>
</code></pre>
<ul>
<li>Las etiquetas <code>&lt;li&gt;</code> puede contener otras listas, y otros elementos como imágenes, links, etc.</li>
<li>Para más información consultar la <a href="https://developer.mozilla.org/en-US/docs/Web/HTML/Element/ol">documentación</a>.</li>
</ul>
<p><strong>Atributos</strong>:</p>
<ul>
<li><code>type</code>: Indica el tipo de símbolo, por default son números, puede see:
<ul>
<li><code>"1"</code> (default): Números.</li>
<li><code>"A"</code>: Letras en mayúsculas.</li>
<li><code>"a"</code>: Letras en minúsculas.</li>
<li><code>"i"</code>: Números romanos en minúsculas.</li>
<li><code>"I"</code>: Números romanos en mayúsculas.</li>
</ul>
</li>
<li><code>start</code>: Indica desde que número iniciar el conteo, por default es desde 1.</li>
<li><code>reversed</code>: Indica que la númeración sea a la inversa. No se le debe asignar ningún valor, simplemente añadir el atributo en la etiqueta.</li>
</ul>
<h4 id="lista-de-descripción">Lista de descripción:</h4>
<p><code>&lt;dl&gt;</code>: Description list - Permite definir listas de descripción. Se usa junto con <code>&lt;dd&gt;</code> y <code>&lt;dt&gt;</code>.</p>
<pre class=" language-html"><code class="prism  language-html"><span class="token tag"><span class="token tag"><span class="token punctuation">&lt;</span>body</span><span class="token punctuation">&gt;</span></span>
	<span class="token tag"><span class="token tag"><span class="token punctuation">&lt;</span>dl</span><span class="token punctuation">&gt;</span></span>
  		<span class="token tag"><span class="token tag"><span class="token punctuation">&lt;</span>dt</span><span class="token punctuation">&gt;</span></span>Term 1<span class="token tag"><span class="token tag"><span class="token punctuation">&lt;/</span>dt</span><span class="token punctuation">&gt;</span></span>
  		<span class="token tag"><span class="token tag"><span class="token punctuation">&lt;</span>dd</span><span class="token punctuation">&gt;</span></span>Description of Term 1.<span class="token tag"><span class="token tag"><span class="token punctuation">&lt;/</span>dd</span><span class="token punctuation">&gt;</span></span>
  		<span class="token tag"><span class="token tag"><span class="token punctuation">&lt;</span>dt</span><span class="token punctuation">&gt;</span></span>Term 2<span class="token tag"><span class="token tag"><span class="token punctuation">&lt;/</span>dt</span><span class="token punctuation">&gt;</span></span>
  		<span class="token tag"><span class="token tag"><span class="token punctuation">&lt;</span>dd</span><span class="token punctuation">&gt;</span></span>Description of Term 2.<span class="token tag"><span class="token tag"><span class="token punctuation">&lt;/</span>dd</span><span class="token punctuation">&gt;</span></span>
  		...
	<span class="token tag"><span class="token tag"><span class="token punctuation">&lt;/</span>dl</span><span class="token punctuation">&gt;</span></span>
<span class="token tag"><span class="token tag"><span class="token punctuation">&lt;/</span>body</span><span class="token punctuation">&gt;</span></span>
</code></pre>
<ul>
<li>Adicionalmente se utilizan las siguientes etiquetas:
<ul>
<li><code>&lt;dt&gt;</code> - <em>Description term</em>: Específica un término o descripción en una lista de descripciones.</li>
<li><code>&lt;dd&gt;</code> - <em>Description description</em>: Provee detalles acerca de la definición de un término precedente.</li>
</ul>
</li>
<li>Para más información consultar la <a href="https://developer.mozilla.org/en-US/docs/Web/HTML/Element/dl">documentación</a>.</li>
</ul>
<h4 id="scripts">Scripts:</h4>
<p><code>&lt;script&gt;</code>: Puede contener sentencias de JavaScript. <strong>Importante</strong>: Debe de ir después de cualquier otro elemento al cual se vaya a acceder desde el script.</p>
<pre class=" language-html"><code class="prism  language-html"><span class="token tag"><span class="token tag"><span class="token punctuation">&lt;</span>body</span><span class="token punctuation">&gt;</span></span>
	<span class="token tag"><span class="token tag"><span class="token punctuation">&lt;</span>script</span><span class="token punctuation">&gt;</span></span><span class="token script language-javascript"> content </span><span class="token tag"><span class="token tag"><span class="token punctuation">&lt;/</span>script</span><span class="token punctuation">&gt;</span></span> 
<span class="token tag"><span class="token tag"><span class="token punctuation">&lt;/</span>body</span><span class="token punctuation">&gt;</span></span>
</code></pre>
<ul>
<li><em>content</em> es directamente el código de JavaScript.</li>
<li>Otra etiqueta relacionada es:
<ul>
<li><code>&lt;noscript&gt;</code>: Muestra un contenido alternativo para navegadores que no soportan scripts o lo tienen desactivados. <br> <code>&lt;noscript&gt; content &lt;/noscript&gt;</code></li>
</ul>
</li>
</ul>
<h4 id="estructurales">Estructurales:</h4>
<p>Las siguiente etiquetas no impactan visualmente en la página, pero si en la estructura de la página. Sirven para organizar la página.</p>
<ul>
<li><code>&lt;section&gt;</code>: Define una sección de un documento. Una sección agrupa temáticamente contenido, generalmente con un encabezado. <br> <code>&lt;section&gt; content &lt;/section&gt;</code></li>
<li><code>&lt;article&gt;</code>: Se utiliza para posts de foros, blogs, artículos, etc. <br> <code>&lt;article&gt; content &lt;/article&gt;</code></li>
<li><code>&lt;aside&gt;</code>: Define un elemento que se coloca lateralmente del contenido donde es colocado. Debe tener sentido con el contenido que lo rodea. <br> <code>&lt;aside&gt; content &lt;/aside&gt;</code></li>
<li><code>&lt;header&gt;</code>: Indica el encabezado de una página, también puede tener un conjunto de links de navegación. Suele tener un encabezado, logos y links de navegación. <br> <code>&lt;header&gt; content &lt;/header&gt;</code></li>
<li><code>&lt;footer&gt;</code>: Define un pie de página, suele contener información del autor, derechos de autor, información de contacto, mapa del sitio, documentos relacionados, etc. <br> <code>&lt;footer&gt; content &lt;/footer&gt;</code></li>
<li><code>&lt;nav&gt;</code>: Navigation - Define un conjunto de links de navegación, está pensado para agrupar un conjunto. <br> <code>&lt;nav&gt; content &lt;/nav&gt;</code></li>
<li><code>&lt;figure&gt;</code>: Un contenedor de imágenes, fotos, ilustraciones, etc. Dentro de él se suele usar <code>&lt;img&gt;</code> y <code>&lt;figcaption&gt;</code> <br> <code>&lt;figure&gt; content &lt;/figure&gt;</code></li>
<li><code>&lt;figcaption&gt;</code>: Inserta un caption a una imagen. <br> <code>&lt;figcaption&gt; content &lt;/figcaption&gt;</code></li>
</ul>
<h2 id="mejores-prácticas">Mejores prácticas:</h2>
<ul>
<li>Usar minúsculas en los nombres de los elementos.</li>
<li>Cerrar todos los elementos (<code>&lt;/&gt;</code>).</li>
<li>Poner los valores de los atributos entre comillas dobles: <code>attr="val"</code>.</li>
<li>Especificar el atributo <code>alt</code> y propiedades de CSS <code>height</code> y <code>width</code> para imágenes.</li>
<li>Evitar poner espacios entre el signo “=” al definir atributos: <code>attr="val"</code>.</li>
<li>Evitar líneas de código muy largas horizontalmente.</li>
<li>Utilizar el elemento <code>&lt;title&gt;</code> de <code>&lt;head&gt;</code>.</li>
<li>Utilizar los elementos <code>&lt;html&gt;</code>, <code>&lt;head&gt;</code> y <code>&lt;body&gt;</code>.</li>
<li>Los elementos etiqueta de cierre cerrar con <code>&lt;tagname/&gt;</code>.</li>
<li>Indicar el atributo <code>lang</code> de <code>&lt;html&gt;</code>.</li>
<li>Indicar el atributo <code>charset</code> de <code>&lt;meta&gt;</code>.</li>
<li>Especificar <code>viewport</code> en <code>&lt;meta&gt;</code>.</li>
<li>Utilizar hojas de estilos en lugar de especificar los estilos en el documento HTML.</li>
<li>Utilizar nombres de archivos en minúsculas.</li>
<li>Utilizar las extensiones <code>.html</code>, <code>.css</code> y <code>.js</code> para HTML, CSS y JavaScript respectivamente.</li>
</ul>

