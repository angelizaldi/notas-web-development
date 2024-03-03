---


---

<h1 id="css">CSS</h1>
<p><strong>Cascading style sheet</strong> (CSS) es un lenguaje para darle formato a los elementos HTML de una página web.</p>
<p>Los estilos se aplican en cascada, es decir, si se determina un estilo a un elemento padre (como <code>&lt;body&gt;</code>) entonces el mismo estilo se aplicará a todos los elementos hijos (como <code>&lt;p&gt;</code>, <code>&lt;h1&gt;</code>, etc.). Los estilos de cada elemento hijo se pueden especificar individualmente. La prioridad es como sigue:</p>
<ol>
<li>Inline - Elementos hijos, como <code>&lt;p&gt;</code>, <code>&lt;h1&gt;</code>, etc. usando el atributo <code>style</code>.</li>
<li>Inline - Elementos padre, como <code>&lt;body&gt;</code>, usando el atributo <code>style</code>.</li>
<li>Internal - Estilo a nivel de página con el elemento <code>&lt;style&gt;</code>. <strong>Importante</strong>: para que <code>&lt;style&gt;</code> realmente sobrescriba a <code>&lt;link rel="stylesheet&gt;</code>, se debe definir después de <code>&lt;link rel="stylesheet&gt;</code>. Se usar para establacer los estilos desde el mismo documento HTML.</li>
<li>External - Estilos de archivos externos <code>.css</code> con el elemento <code>&lt;link&gt;</code>, usando el atributo <code>rel="stylesheet"</code>. Se puede usar para establecer los estilos a múltiples archivos con una sola hoja de estilo. <strong>Importante</strong>: Si un mismo elemento HTML se definió en diferentes hojas de estilo, entonces se utiliza el de la última hoja de estilo.</li>
</ol>
<p><strong>Importante</strong>: Lo recomendable es determinar los estilos de manera externa, es decir, con archivos CSS.</p>
<h2 id="desde-un-archivo-externo">Desde un archivo externo:</h2>
<p>Para añadir estilos desde un archivo externo, es recomendado agregar una carpeta a la carpeta del proyecto, con el nombre “css”, ahí se agregan las hojas de estilo que deben de tener la extensión <code>.css</code>. Posteriormente en la página de html se debe de agregar un <code>&lt;link rel="stylesheet&gt;</code> en la etiqueta <code>&lt;head&gt;</code> que haga referencia a la hoja de estilos.</p>
<pre class=" language-html"><code class="prism  language-html"><span class="token doctype">&lt;!DOCTYPE html&gt;</span>
<span class="token tag"><span class="token tag"><span class="token punctuation">&lt;</span>html</span><span class="token punctuation">&gt;</span></span>
	<span class="token tag"><span class="token tag"><span class="token punctuation">&lt;</span>head</span><span class="token punctuation">&gt;</span></span>
		...
		<span class="token tag"><span class="token tag"><span class="token punctuation">&lt;</span>link</span> <span class="token attr-name">href</span><span class="token attr-value"><span class="token punctuation">=</span><span class="token punctuation">"</span>path/to/file.css<span class="token punctuation">"</span></span> <span class="token attr-name">rel</span><span class="token attr-value"><span class="token punctuation">=</span><span class="token punctuation">"</span>stylesheet<span class="token punctuation">"</span></span><span class="token punctuation">&gt;</span></span>
	<span class="token tag"><span class="token tag"><span class="token punctuation">&lt;/</span>head</span><span class="token punctuation">&gt;</span></span>
	<span class="token tag"><span class="token tag"><span class="token punctuation">&lt;</span>body</span><span class="token punctuation">&gt;</span></span>
		...
	<span class="token tag"><span class="token tag"><span class="token punctuation">&lt;/</span>body</span><span class="token punctuation">&gt;</span></span>
<span class="token tag"><span class="token tag"><span class="token punctuation">&lt;/</span>html</span><span class="token punctuation">&gt;</span></span>
</code></pre>
<p><strong>Importante</strong>: Si un mismo elemento HTML se definió en diferentes hojas de estilo, entonces se utiliza el de la última hoja de estilo en la etiqueta <code>&lt;head&gt;</code>.</p>
<h2 id="sintaxis-general">Sintaxis general:</h2>
<p>Para establecer los estilos, se tiene que especificar el <em>selector</em> y entre llaves poner los atributos con sus respectivos valores, los atributos se separan por punto y coma y los valores se establecen con dos puntos. Las definiciones para distintos <em>selectors</em> se pueden separar con salto de línea.</p>
<pre class=" language-css"><code class="prism  language-css"><span class="token selector">selector </span><span class="token punctuation">{</span><span class="token property">property1</span><span class="token punctuation">:</span> value<span class="token number">1</span><span class="token punctuation">;</span> <span class="token property">property2</span><span class="token punctuation">:</span> value<span class="token number">2</span><span class="token punctuation">;</span> <span class="token number">...</span><span class="token punctuation">}</span>
</code></pre>
<ul>
<li><em>selector</em> es un elemento HTML, existen otras formas de definirlos.</li>
<li><em>property</em> es el nombre de una propiedad de CSS.</li>
<li><em>value</em> son los valores de <em>property</em>.</li>
</ul>
<p><strong>Ejemplo</strong>:</p>
<pre class=" language-css"><code class="prism  language-css"><span class="token selector">h1 </span><span class="token punctuation">{</span>
	<span class="token property">attr</span><span class="token punctuation">:</span> val<span class="token punctuation">;</span> 
	<span class="token property">attr</span><span class="token punctuation">:</span> val, 
	<span class="token number">...</span>
<span class="token punctuation">}</span>

<span class="token selector">p </span><span class="token punctuation">{</span>
	<span class="token property">attr</span><span class="token punctuation">:</span> val<span class="token punctuation">;</span> 
	<span class="token property">attr</span><span class="token punctuation">:</span> val, 
	<span class="token number">...</span>
<span class="token punctuation">}</span>

</code></pre>
<ul>
<li>En ese ejemplo los <em>selectors</em> son <code>h1</code> y <code>p</code> que corresponden a nombres de elementos de HTML. Tener en cuenta que existen otras formas de definir los <em>selectors</em>.</li>
<li><em>attr</em> y <em>val</em> son atributos y valores de css respectivamente.</li>
</ul>
<p>No es necesario identar ni poner saltos de línea, lo anterior se puede poner como:</p>
<pre class=" language-css"><code class="prism  language-css"><span class="token selector">h1 </span><span class="token punctuation">{</span><span class="token property">attr</span><span class="token punctuation">:</span> val<span class="token punctuation">;</span> <span class="token property">attr</span><span class="token punctuation">:</span> val, <span class="token number">...</span><span class="token punctuation">}</span>
<span class="token selector">p </span><span class="token punctuation">{</span><span class="token property">attr</span><span class="token punctuation">:</span> val<span class="token punctuation">;</span> <span class="token property">attr</span><span class="token punctuation">:</span> val, <span class="token number">...</span><span class="token punctuation">}</span>
</code></pre>
<h2 id="comentarios.">Comentarios.</h2>
<p>Para insertar comentarios en hojas de estilo (incluyendo la etiqueta <code>&lt;style&gt;</code>) se usa:</p>
<pre class=" language-css"><code class="prism  language-css"><span class="token comment">/* esto es un comentario */</span>
</code></pre>
<ul>
<li>Los comentarios pueden abarcar partes de líneas, líneas completas o múltiples líneas, todos con la misma sintaxis.</li>
</ul>
<h2 id="selectores.">Selectores.</h2>
<p>Un selector determina el elemento HTML que se le dará estilo. Existen varias formas de definir los selectores. A continuación se describen brevemente algunos de ellos.</p>
<ul>
<li><strong>Selectores simples</strong>: Seleccionan con base en el nombre, id o clase de un elemento HTML.</li>
<li><strong>Selectores combinados</strong>: Selecciona elementos con base a la relación entre ellos.</li>
<li><strong>Selectores de pseudo-clase</strong>: Seleccionan elementos con base a un estado específico.</li>
<li><strong>Selectores de pseudo-elementos</strong>: Seleccionar y dan estilo a una parte de un elemento.</li>
<li><strong>Selectores de atributos</strong>: Seleccionan elementos con base a un atributo o un valor de un atributo.</li>
</ul>
<h3 id="selectores-simples">Selectores simples:</h3>
<p>Seleccionan con base en el nombre, id o clase, y se aplican a todos los elementos que tengan ese nombre, id o clase.</p>
<pre class=" language-css"><code class="prism  language-css"><span class="token comment">/* Ejemplo selector por nombre */</span>
<span class="token selector">h1 </span><span class="token punctuation">{</span>
<span class="token property">attr</span><span class="token punctuation">:</span> val<span class="token punctuation">;</span> 
<span class="token property">attr</span><span class="token punctuation">:</span> val, 
<span class="token number">...</span>
<span class="token punctuation">}</span>

<span class="token comment">/* Ejemplo selector por clase */</span>
<span class="token selector">className </span><span class="token punctuation">{</span>
<span class="token property">attr</span><span class="token punctuation">:</span> val<span class="token punctuation">;</span> 
<span class="token property">attr</span><span class="token punctuation">:</span>val, 
<span class="token number">...</span>
<span class="token punctuation">}</span>

<span class="token comment">/* Ejemplo selector por id */</span>
<span class="token selector">idName </span><span class="token punctuation">{</span>
<span class="token property">attr</span><span class="token punctuation">:</span> val<span class="token punctuation">;</span> 
<span class="token property">attr</span><span class="token punctuation">:</span>val, 
<span class="token number">...</span>
<span class="token punctuation">}</span>
</code></pre>
<h4 id="selector-de-elemento">Selector de elemento:</h4>
<p>Basado en el nombre del elemento HTML, el estilo se aplica a todos los elementos con el mismo nombre, respetando la jerarquía</p>
<pre class=" language-css"><code class="prism  language-css"><span class="token comment">/* Ejemplo selector por nombre */</span>
<span class="token selector">element </span><span class="token punctuation">{</span><span class="token property">property</span><span class="token punctuation">:</span> value<span class="token punctuation">;</span> <span class="token number">...</span><span class="token punctuation">}</span>
</code></pre>
<ul>
<li><em>element</em> es el nombre de algún elemento HTML, como <code>&lt;p&gt;</code>, <code>&lt;h1&gt;</code>, etc.</li>
<li>Se pueden poner más de un elemento separados por coma: <br> <code>element1, element2, ... {property: value; ...}</code></li>
</ul>
<h4 id="selector-id">Selector id:</h4>
<p>Utiliza el atributo <em>id</em> de un elemento HTML para seleccionar un elemento específico. Se utiliza junto el símbolo <code>#</code>, ejemplo:</p>
<pre class=" language-css"><code class="prism  language-css"><span class="token comment">/* Ejemplo selector por id */</span>
<span class="token selector"><span class="token id">#id</span> </span><span class="token punctuation">{</span><span class="token property">property</span><span class="token punctuation">:</span> value<span class="token punctuation">;</span> <span class="token number">...</span><span class="token punctuation">}</span>
</code></pre>
<ul>
<li>El nombre <em>id</em> debe tener al menos un carácter, no puede empezar por números y no debe tener espacios en blanco.</li>
</ul>
<p>En el elemento HTML usar el atributo <em>id</em> y el nombre del identificador sin la almohadilla (<em>#</em>) al inicio.</p>
<pre class=" language-html"><code class="prism  language-html"><span class="token tag"><span class="token tag"><span class="token punctuation">&lt;</span>element</span> <span class="token attr-name">id</span><span class="token attr-value"><span class="token punctuation">=</span><span class="token punctuation">"</span>name<span class="token punctuation">"</span></span><span class="token punctuation">&gt;</span></span> ... <span class="token tag"><span class="token tag"><span class="token punctuation">&lt;/</span>element</span><span class="token punctuation">&gt;</span></span>
</code></pre>
<h4 id="selector-de-clase">Selector de clase:</h4>
<p>Utilizando el atributo <em>class</em> de los elementos de HTML, para seleccionar elementos de una misma clase. Se utiliza agregando un punto (<code>.</code>) al inicio:</p>
<pre class=" language-css"><code class="prism  language-css"><span class="token selector"><span class="token class">.ClassName</span> </span><span class="token punctuation">{</span><span class="token property">property</span><span class="token punctuation">:</span>value<span class="token punctuation">;</span> <span class="token number">...</span><span class="token punctuation">}</span>
</code></pre>
<ul>
<li><em>className</em> es el nombre de la clase.</li>
<li>Se pueden poner más de uno separando con coma. <br> <code>.ClassName1, .ClassName2, ... {property:value; ...}</code></li>
</ul>
<p>Es posible especificar el estilo a un mismo tipo de elemento que comparte la misma clase. Para más información revisar sub-clases:</p>
<pre class=" language-css"><code class="prism  language-css"><span class="token selector">element<span class="token class">.ClassName</span></span><span class="token punctuation">{</span><span class="token property">property</span><span class="token punctuation">:</span>value<span class="token punctuation">;</span> <span class="token number">...</span><span class="token punctuation">}</span>
</code></pre>
<ul>
<li><em>element</em> es el nombre de algún elemento HTML, como <code>&lt;p&gt;</code>, <code>&lt;h1&gt;</code>, etc.</li>
<li><em>className</em> es el nombre de la clase.</li>
</ul>
<p>En los elementos HTML usar el atributo <em>class</em> y el nombre de la clase sin el punto al inicio.</p>
<pre class=" language-html"><code class="prism  language-html"><span class="token tag"><span class="token tag"><span class="token punctuation">&lt;</span>elemento</span> <span class="token attr-name">class</span><span class="token attr-value"><span class="token punctuation">=</span><span class="token punctuation">"</span>ClassName<span class="token punctuation">"</span></span><span class="token punctuation">&gt;</span></span> ... <span class="token tag"><span class="token tag"><span class="token punctuation">&lt;/</span>element</span><span class="token punctuation">&gt;</span></span>
</code></pre>
<ul>
<li>Es posible que el elemento pertenezca a más de una clase, para ello separar con espacios: <br> <code>&lt;tagname class="class1 class2 ..."&gt; content &lt;/tagname&gt;</code>.</li>
</ul>
<h4 id="selector-universal">Selector universal:</h4>
<p>Selecciona todos los elementos de HTML en el documento, para ello se utiliza un asterisco:</p>
<pre class=" language-css"><code class="prism  language-css"><span class="token selector">*  </span><span class="token punctuation">{</span><span class="token property">property</span><span class="token punctuation">:</span>value<span class="token punctuation">;</span> <span class="token number">...</span><span class="token punctuation">}</span>
</code></pre>
<ul>
<li>El selector universal es utilizado raramente.</li>
</ul>
<h3 id="selectores-combinados">Selectores combinados:</h3>
<h4 id="sub-clases">Sub-clases</h4>
<p>Basado en el nombre de algún elemento y una clase en específico, es decir solo los elementos que pertenezcan a una clase en específico.</p>
<pre class=" language-css"><code class="prism  language-css"><span class="token selector">element<span class="token class">.subclass</span> </span><span class="token punctuation">{</span><span class="token property">property</span><span class="token punctuation">:</span>value<span class="token punctuation">;</span> <span class="token number">...</span><span class="token punctuation">}</span>
</code></pre>
<ul>
<li><em>element</em> es el nombre de cualquier elemento de HTML y <em>subclass</em> es el nombre de la subclase.</li>
</ul>
<h4 id="selectores-combinados-1">Selectores combinados:</h4>
<p>Un <em>combinator</em> explica la relación entre selectores, existe 4 <em>combinators</em>:</p>
<ul>
<li><strong>Descendant selector</strong> (espacio).</li>
<li><strong>Child selector</strong> (<code>&gt;</code>): Selecciona elementos que son elementos hijos directos de otro elemento. Solo selecciona los elementos que están un nivel por debajo del elemento especificado.</li>
<li><strong>Adjacent sibling selector</strong> (<code>+</code>): Selecciona los elementos que están inmediatamente después de otro elemento. Solo selecciona los elementos que están directamente al lado del elemento especificado, no más abajo en el árbol DOM.</li>
<li><strong>General sibling selector</strong> (<code>~</code>): Selecciona elementos que están después de otro elemento, pero no necesariamente inmediatamente después. Selecciona todos los elementos del elemento especificado, incluidos los que están separados por otros elementos.</li>
<li>Para ver más información revisar <a href="https://www.w3schools.com/css/css_combinators.asp">esta página</a>.</li>
</ul>
<h5 id="descendant-selector">Descendant selector:</h5>
<p>Selecciona elementos que son descendientes de otro elemento. Los descendientes pueden ser hijos directos o hijos anidados (nietos, bisnietos, etc.).</p>
<pre class=" language-css"><code class="prism  language-css"><span class="token selector">first_element second_element <span class="token class">...</span></span><span class="token punctuation">{</span><span class="token property">property</span><span class="token punctuation">:</span>value<span class="token punctuation">;</span> <span class="token number">...</span><span class="token punctuation">}</span>
</code></pre>
<ul>
<li>los elementos están jerarquizados, <em>second_element</em> está dentro de <em>firs_telement</em>. pero no necesariamente es un hijo directo, puede estar en cualquier nivel de profundidad.</li>
</ul>
<pre class=" language-css"><code class="prism  language-css"><span class="token comment">/* Ejemplo de descendant selector */</span>
 <span class="token selector">div p </span><span class="token punctuation">{</span>
  <span class="token property">color</span><span class="token punctuation">:</span> red<span class="token punctuation">;</span>
<span class="token punctuation">}</span>
</code></pre>
<ul>
<li>Selecciona todos los elementos <code>&lt;p&gt;</code> dentro de los elementos <code>&lt;div&gt;</code> y se modifica el color.</li>
</ul>
<h5 id="child-selector">Child selector:</h5>
<p>Selecciona elementos que son elementos hijos directos de otro elemento. Solo selecciona los elementos que están un nivel por debajo del elemento especificado.</p>
<pre class=" language-css"><code class="prism  language-css"><span class="token selector">parent_element &gt; child_element </span><span class="token punctuation">{</span><span class="token property">property</span><span class="token punctuation">:</span>value<span class="token punctuation">;</span> <span class="token number">...</span><span class="token punctuation">}</span>
</code></pre>
<ul>
<li><em>child_element</em> es un hijo directo de <em>parent_element</em>.</li>
</ul>
<pre class=" language-css"><code class="prism  language-css"><span class="token comment">/* Ejemplo de child selector */</span>
<span class="token selector">ul &gt; li </span><span class="token punctuation">{</span>
  <span class="token property">font-weight</span><span class="token punctuation">:</span> bold<span class="token punctuation">;</span>
<span class="token punctuation">}</span>
</code></pre>
<ul>
<li>Selecciona los elementos <code>&lt;il&gt;</code> que son hijos directo de <code>&lt;ul&gt;</code>.</li>
</ul>
<h5 id="adjacent-sibling-selector">Adjacent sibling selector:</h5>
<p>Selecciona el elemento que está inmediatamente posterior a otro elemento, no los que están adentro, sino después. Si hay más de un elemento del tipo <code>element1</code> solo seleccionará el primero, para seleccionar más de uno usar el <em>general sibling selector</em>.</p>
<pre class=" language-css"><code class="prism  language-css"><span class="token selector">element1 + element2 </span><span class="token punctuation">{</span><span class="token property">property</span><span class="token punctuation">:</span>value<span class="token punctuation">;</span> <span class="token number">...</span><span class="token punctuation">}</span>
</code></pre>
<ul>
<li><em>element1</em> y <em>element2</em> están contiguos.</li>
</ul>
<pre class=" language-css"><code class="prism  language-css"><span class="token comment">/* Ejemplo de adjacent sibling selector */</span>
<span class="token selector">h1 + p </span><span class="token punctuation">{</span>
  <span class="token property">margin-top</span><span class="token punctuation">:</span> <span class="token number">0</span><span class="token punctuation">;</span>
<span class="token punctuation">}</span>
</code></pre>
<ul>
<li>Selecciona el primer elemento <code>&lt;p&gt;</code> que está después de los elementos <code>&lt;h1&gt;</code>.</li>
</ul>
<h5 id="general-sibling-selector">General sibling selector:</h5>
<p>Selecciona elementos que están después de otro elemento, pero no necesariamente inmediatamente después. Selecciona <strong>todos</strong> los elementos del elemento especificado, incluidos los que están separados por otros elementos.</p>
<pre class=" language-css"><code class="prism  language-css"><span class="token selector">element1 ~ element2 </span><span class="token punctuation">{</span><span class="token property">property</span><span class="token punctuation">:</span>value<span class="token punctuation">;</span> <span class="token number">...</span><span class="token punctuation">}</span>
</code></pre>
<ul>
<li><em>element2</em> está posterior a <em>element1</em>, pueden ser uno o más y deben estar al mismo nivel que <em>element1</em>, no adentro.</li>
</ul>
<pre class=" language-css"><code class="prism  language-css"><span class="token comment">/* Ejemplo de general sibling selector */</span>
<span class="token selector">h2 ~ p </span><span class="token punctuation">{</span>
  <span class="token property">font-size</span><span class="token punctuation">:</span> <span class="token number">16</span>px<span class="token punctuation">;</span>
<span class="token punctuation">}</span>
</code></pre>
<ul>
<li>Todos los elementos <code>&lt;p&gt;</code> que están después de un encabezado <code>&lt;h2&gt;</code>.</li>
</ul>
<h3 id="pseudo-clases">Pseudo clases:</h3>
<p>Son usados para definir un estado especial de un elemento (como los <em>visited</em>, <em>hover</em>, etc. de <code>&lt;a&gt;</code>). Utilizan dos puntos y se pueden combinar con las clases. Algunas pseudo-clases son:</p>
<pre class=" language-css"><code class="prism  language-css"><span class="token selector">element<span class="token pseudo-class">:pseudo-class</span> </span><span class="token punctuation">{</span><span class="token property">property</span><span class="token punctuation">:</span>value<span class="token punctuation">;</span> <span class="token number">...</span><span class="token punctuation">}</span>
</code></pre>
<ul>
<li><code>:active</code>: Link activo (al momento de tenerlo presionado)</li>
<li><code>:hover</code>: Al colocar el cursor encima del elemento.</li>
<li><code>:first-child</code>: Específica un elemento que es el primer hijo de otro elemento.</li>
<li><code>:lang</code>: Permite definir reglas especiales para diferentes idiomas.</li>
<li>Existen muchos más, revisa <a href="https://www.w3schools.com/css/css_pseudo_classes.asp">este link</a>.</li>
</ul>
<h3 id="pseudo-elementos">Pseudo elementos:</h3>
<p>Se utilizan para dar formato a partes específicas de un elemento, como la primera letra, la primera línea, insertar contenido antes o después del contenido de un elemento, entre otros. Se utiliza dobles dos puntos:</p>
<pre class=" language-css"><code class="prism  language-css"><span class="token selector">element :: psudo-element </span><span class="token punctuation">{</span><span class="token number">...</span><span class="token punctuation">}</span>
</code></pre>
<ul>
<li><code>::after</code>: Permite insertar contenido después del contenido actual de un elemento.</li>
<li><code>::before</code>: Permite insertar contenido después del contenido actual de un elemento.</li>
<li><code>::first-letter</code>: Permite estilizar la primer letra del contenido de un elemento.</li>
<li><code>::first-ine</code>: Permite estilizar la primer letra del contenido de un elemento.</li>
<li><code>::marker</code>: Permite seleccionar las viñetas de un elemento. Las viñetas son como las de las listas, tanto numeradas como no numeradas.</li>
<li><code>::selection</code>: Permite estilizar el texto seleccionado del contenido de un elemento.</li>
<li>Para más información visitar <a href="https://www.w3schools.com/css/css_pseudo_elements.asp">este link</a></li>
</ul>
<p>Para insertar contenido generalmente se hará uso de la propiedad <code>content</code> poniendo entre comillas en contenido que se quiere agregar, por ejemplo:</p>
<pre class=" language-css"><code class="prism  language-css"><span class="token selector">element :: after </span><span class="token punctuation">{</span>
	<span class="token property">content</span><span class="token punctuation">:</span> <span class="token string">"something"</span>
<span class="token punctuation">}</span>
</code></pre>
<h3 id="selectores-de-atributo">Selectores de atributo:</h3>
<p>Se utiliza para dar estilo a todos los elementos que comparten algún atributo en particular, los atributos son de los de HTML, además se puede especificar algún valor en particular.</p>
<pre class=" language-css"><code class="prism  language-css"><span class="token selector">element<span class="token attribute">[attr_name]</span> </span><span class="token punctuation">{</span> <span class="token number">...</span> <span class="token punctuation">}</span>

<span class="token selector">element<span class="token attribute">[attr_name="val"]</span> </span><span class="token punctuation">{</span> <span class="token number">...</span> <span class="token punctuation">}</span>
</code></pre>
<ul>
<li><code>element</code> es el nombre del elemento y <code>attr_name</code> es el nombre del atributo. Opcionalmente se puede especificar una valor para el atributo.</li>
</ul>
<p>Además, se pueden especificar otro tipo de patrones, por ejemplo:</p>
<pre class=" language-css"><code class="prism  language-css"><span class="token comment">/* Atributo contenga la palabra */</span>
<span class="token selector">element_name<span class="token attribute">[attr_name~="word"]</span> </span><span class="token punctuation">{</span> <span class="token number">...</span> <span class="token punctuation">}</span>

<span class="token comment">/* Atributo contenga una de las dos palabras. */</span>
<span class="token selector">element_name<span class="token attribute">[attr_name |= "word1-word2"]</span> </span><span class="token punctuation">{</span> <span class="token number">...</span> <span class="token punctuation">}</span>

<span class="token comment">/* Atributo comience por la palabra. */</span>
<span class="token selector">element_name<span class="token attribute">[attr_name ^= "word1"]</span> </span><span class="token punctuation">{</span> <span class="token number">...</span> <span class="token punctuation">}</span>

<span class="token comment">/* Atributo termine por la palabra. */</span>
<span class="token selector">element_name<span class="token attribute">[attr_name $= "word1"]</span> </span><span class="token punctuation">{</span> <span class="token number">...</span> <span class="token punctuation">}</span>

<span class="token comment">/* Atributo contiene la palabra. */</span>
<span class="token selector">element_name<span class="token attribute">[attr_name *= "word1"]</span> </span><span class="token punctuation">{</span> <span class="token number">...</span> <span class="token punctuation">}</span>
</code></pre>
<p></p>
<h2 id="box-model">Box-model:</h2>
<p><img src="https://developer.mozilla.org/en-US/docs/Learn/CSS/Building_blocks/The_box_model/box-model.png" alt="Box model."></p>
<p>En html cada elemento está dentro de una caja que consiste de varias capas:</p>
<ul>
<li><em>Content</em>: Es donde estará como tal el contenido.</li>
<li><em>Padding</em>: Es el espacio entre el contenido y algún borde que se pueda poner.</li>
<li><em>Border</em>: Es el espacio que abarcará algún borde que se quiera poner. además de poder indicar su ancho se puede indicar el tipo de borde y el color:</li>
<li><em>Margin</em>: Es el espacio entre el borde y otros elementos de la página.</li>
</ul>
<h3 id="formas-de-definirlos">Formas de definirlos:</h3>
<p>Al definir los argumentos de <em>border</em>, <em>padding</em> y <em>margin</em> se puede hacer:</p>
<ul>
<li><strong>Un solo valor</strong>: Aplica el mismo valor a <em>top</em>, <em>bottom</em>, <em>right</em> y <em>left</em>. <br> <code>property all</code></li>
<li><strong>Dos valores</strong>: Un valor diferente para <em>top</em> y <em>bottom</em> y otro para <em>right</em> y <em>left</em>:	<br> <code>property top-bottom right-left</code></li>
<li><strong>Tres valores</strong>: Un valor diferente para <em>top</em>, otro para <em>bottom</em> y otro para <em>right</em> y <em>left</em>: <br> <code>property top right-left bottom</code></li>
<li><strong>Cuatro valores</strong>: Propiedades individuales: Cada propiedad en el siguiente orden <br> <code>property top right bottom left</code></li>
<li>Centrado horizontalmente, verticalmente o ambas.</li>
<li>El valor <strong>auto</strong> centra horizontalmente el elemento dentro de su contendor (aplica en margin), al <em>top</em> y <em>bottom</em> asigna 0, se puede especificar el <em>top</em> y <em>bottom</em> usando dos valores.</li>
<li>Propiedades individuales: Cada propiedad se puede especificar individualmente (las siguientes son las propiedades abreviadas):
<ul>
<li><em>margin-top</em>.</li>
<li><em>margin-bottom</em>.</li>
<li><em>margin-left</em>.</li>
<li><em>margin-right</em>.</li>
<li><em>border-top</em>.</li>
<li><em>border-bottom</em>.</li>
<li><em>border-left</em>.</li>
<li><em>border-right</em>.</li>
<li><em>padding-top</em>.</li>
<li><em>padding-bottom</em>.</li>
<li><em>padding-left</em>.</li>
<li><em>padding-right</em>.</li>
</ul>
</li>
<li>existen propiedades específicas para cada lado, como:
<ul>
<li><em>property-top-width</em>.</li>
<li><em>property-bottom-width</em>.</li>
<li><em>property-right-width</em>.</li>
<li><em>property-left-width</em>.</li>
</ul>
</li>
</ul>
<h2 id="flexbox.">Flexbox.</h2>
<p>Permite acomodar elementos dentro de un elemento contenedor, de manera más amigable que con la propiedad <code>float</code> o <code>position</code>. Para ello dentro del elemento contenedor se utiliza la propiedad <code>display</code> con el valor <code>flex</code>.</p>
<pre class=" language-css"><code class="prism  language-css"><span class="token selector">selector </span><span class="token punctuation">{</span>
<span class="token property">display</span><span class="token punctuation">:</span> flex<span class="token punctuation">;</span>
<span class="token number">...</span>
<span class="token punctuation">}</span>
</code></pre>
<ul>
<li><em>flex</em> no es el único valor válido, para más información visitar la <a href="https://developer.mozilla.org/en-US/docs/Web/CSS/display">documentación</a>.</li>
</ul>
<h2 id="estados-de-links">Estados de Links:</h2>
<p>Los links se pueden personalizar en diversos estados:</p>
<ul>
<li><em>a:link</em>: Link normal, sin visitar.</li>
<li><em>a:visited</em>: Link que ya se visitó.</li>
<li><em>a:hover</em>: Link al poner el cursor sobre él.</li>
<li><em>a:active</em>: Al momento de estar presionando sobre él.</li>
<li><strong>IMPORTANTE</strong>: Se debe respetar cierto orden al definir los estados:</li>
<li><em>a:hover</em> debe de ir después de <em>a:link</em> y <em>a:visited</em>.</li>
<li><em>a:active</em> debe de ir después de <em>a:hover</em>.</li>
</ul>
<h2 id="propiedades">Propiedades:</h2>
<p>En esta sección se enlistan algunas de las propiedades de CSS más importantes.</p>
<h3 id="generales">Generales:</h3>
<ul>
<li><code>display</code> - <code>{block, inline, inline-block, flex, none}</code>: Es para modificar la forma como se muestra un elemento. Modifica si se muestra como <em>inline</em> o <em>block</em>, pero no modifica el tipo de elemento que es, por ejemplo, un elemento <em>inline</em> con “<em>display: block</em>” no puede tener otros elementos <em>block</em> adentro. Para más información visitar la <a href="https://developer.mozilla.org/en-US/docs/Web/CSS/display">documentación</a>.</li>
<li><code>inline-block</code>: Permite establecer un alto y ancho del elemento y <em>top/bottom</em> de <em>margin/padding</em> son respetados (no pasa con <em>inline</em>). Además, no agrega un salto de línea después del elemento.
<ul>
<li><code>none</code>: No muestra el elemento y además elimina el espacio que ocuparía.</li>
<li><code>flex</code>: Consulta Flexbox.</li>
</ul>
</li>
<li><code>position</code> - <code>{static, relative, fixed, bsolute, sticky}</code> (default: <code>static</code>): Especifica el método de posicionamiento de un elemento. Para más información visitar la <a href="https://developer.mozilla.org/en-US/docs/Web/CSS/position">documentación</a>.
<ul>
<li><code>static</code>: No es posicionada de alguna manera especial y no se ve afectado por las propiedades <em>top</em>, <em>bottom</em>, <em>left</em> y <em>right</em>.</li>
<li><code>relative</code>: Se posiciona relativamente a su posición normal, es decir la posición por default. Especificando <em>top</em>, <em>bottom</em>, <em>left</em> y <em>right</em> provoca que se ajuste desde su posición normal.</li>
<li><code>fixed</code>: Se posiciona relativo al <em>viewport</em> (pantalla disponible). Siempre se ve incluso si da scroll a la página en cualquier dirección se utiliza las propiedades top, bottom, left y right.</li>
<li><code>absolute</code>: Se posiciona relativo a su elemento padre. Si el elemento no está dentro de algún otro elemento, entonces se considera el elemento .</li>
<li><code>sticky</code>: Se posiciona de manera estática, pero si se hace scroll cuando llegue a su posición determinada en top, bottom, left o right se comportará como elemento fijo.</li>
</ul>
</li>
<li><code>z-index</code>: Es un índice para indicar la posición de elementos apilados (que aparezcan en frente, detrás, etc.), solo funciona con elementos con position <em>absolute</em>, <em>relative</em>, <em>fixed</em> o <em>sticky</em>. Puede ser cero, positivos o negativos. Para más información visitar la <a href="https://developer.mozilla.org/en-US/docs/Web/CSS/z-index">documentación</a>.</li>
</ul>
<p><img src="https://miro.medium.com/v2/resize:fit:720/format:webp/1*uGPV3qEF7yBq4PD0zua19A.png" alt="{{Indice Z."></p>
<ul>
<li><code>overflow</code> - <code>{visible, hidden, scroll, auto}</code>: Para indicar que ocurre con el contenido que es muy grande para caber en un área. Es necesario especificar la propiedad height. Existen variantes solo para un eje como <code>overflow-x</code> y <code>overflow-y</code>. Para más información visitar la <a href="https://developer.mozilla.org/en-US/docs/Web/CSS/overflow">documentación</a>.
<ul>
<li><em>visible</em>: Se desborda el contenido.</li>
<li><em>hidden</em>: No se muestra el contenido que no cabe.</li>
<li><em>scroll</em>: Se puede hacer _scroll _ en el contenido para visualizarlo dentro del contenedor.</li>
<li><em>auto</em>: Similar a <em>scroll</em>.</li>
</ul>
</li>
<li><code>float</code> - <code>{left, right, none, inherit}</code>: Se utiliza para posicionar y dar formato a contenido, por ejemplo, colocar una imagen a lado de un texto. Para más información visitar la <a href="https://developer.mozilla.org/en-US/docs/Web/CSS/float">documentación</a>.</li>
<li><code>clear</code> - <code>{none, left, right, both, inherit}</code>: Se utiliza cuando se usa la propiedad <code>float</code>, para indicar que se quiere el elemento por debajo del elemento <em>float</em>.  Para más información visitar la <a href="https://developer.mozilla.org/en-US/docs/Web/CSS/clear">documentación</a>.</li>
</ul>
<h4 id="flexbox">Flexbox:</h4>
<p>Propiedades cuando se utiliza <code>display: flex</code>. Todas estas propiedades se definen en el mismo elemento contenedor, donde se definió <code>display: flex</code>. Para más información visitar la <a href="https://developer.mozilla.org/en-US/docs/Learn/CSS/CSS_layout/Flexbox">documentación</a>.</p>
<ul>
<li><code>flex-direction</code> - <code>{row, row-reverse, column, column-reverse}</code>: Determina como se acomodan los elementos del contenedor <em>flexbox</em>.</li>
<li><code>flex-wrap</code> - <code>{wrap, nowrap, wrap-reverse}</code>: Define si los elementos aparecen en una línea (<em>no-wrap</em>) o en múltiples líneas (<em>wrap</em>).</li>
<li><code>flex-flow</code> - <code>direction wrap</code>: Es una versión abreviada de las propiedades <em>flex-direction</em> y <em>flex-wrap</em>. Los valores posibles son los mismos que los respectivos de ambas propiedades, primero indicando <em>direction</em> y posteriormente <em>wrap</em>.</li>
<li><code>justify-content</code> - <code>{flex-start, flex-end, center, space-between, space-around, space-evenly}</code>: Define como los elementos son alineados con respecto al eje principal (<em>direction</em>) dentro de un contenedor <em>flexbox</em>. Los que empieza con <em>space</em> distribuyen los elementos en el eje.</li>
<li><code>align-items</code> - <code>{flex-start, flex-end, center, baseline, stretch}</code> (defult: <code>stretch</code>): Define cómo los elementos se alinean de acuerdo al eje secundario.</li>
<li><code>align-content</code> - <code>{flex-start, flex-end, center, space-between, space-around, space-evenly}</code>: Define cómo cada línea se alinea dentro del contenedor, solo aplica si <code>flex-wrap: wrap</code> está definido y si se tiene múltiples líneas.</li>
</ul>
<p>Las siguientes propiedades se aplican en los elementos interiores.</p>
<ul>
<li><code>order</code> - <em>integer</em>: Orden de los elementos.</li>
<li><code>flex-grow</code> - <em>integer</em>: Define cuánto puede crecer un elemento si hay espacio disponible.</li>
<li><code>flex-basis</code> - <em>auto</em>, <em>lenght</em>: Define el tamaño inicial de un elemento en el flexbox.</li>
<li><code>align.self</code> - <code>{flex-start, flex-end, center, baseline, stretch}</code>: Similar a <code>align-items</code>, pero para un item individual. Define cómo el elemento se alinea de acuerdo al eje secundario.</li>
</ul>
<h3 id="texto">Texto:</h3>
<p>Propiedades para el formato de texto.</p>
<h4 id="color">Color:</h4>
<ul>
<li><code>color</code> - <em>color</em>: Especifica el color del elemento, principalmente el color de texto.</li>
</ul>
<h4 id="alineación-del-texto">Alineación del texto:</h4>
<ul>
<li><code>text-align</code> - <code>{left, right, center, justify</code>} (default: <code>left</code>): Alineación del texto horizontalmente.</li>
<li><code>text-align-last</code> - <code>{left, right, center, justify}</code> (default: <code>left</code>): Especifica la alineación de la última línea de un texto.</li>
<li><code>direction</code> - <code>{rtl, ltf}</code> (default: <code>ltf</code>): Dirección del texto:
<ul>
<li><em>rtl</em>: Derecha a izquierda.</li>
<li><em>ltf</em>: Izquierda a derecha.</li>
</ul>
</li>
<li><code>vertical-align</code> - <code>{baseline, text-top, text-bottom, sub, sup}</code> (default: <code>baseline</code>): Alineación vertical del texto.
<ul>
<li><em>baseline</em>: Alineación normal.</li>
<li><em>text-top</em>: Alineación superior.</li>
<li><em>text-bottom</em>: Alineación inferior.</li>
<li><em>sub</em>: Alineación inferior, es menor que <em>text-bottom</em>.</li>
<li><em>sup</em>: Alineación superior, es mayor que <em>text-top</em>.</li>
</ul>
</li>
</ul>
<h4 id="otros">Otros:</h4>
<ul>
<li><code>unicode-bidi</code>: Se usa junto con <em>direction</em>, para establecer si el texto puede soportar múltiples lenguajes en el mismo documento.</li>
</ul>
<h4 id="decoraciones">Decoraciones:</h4>
<p>Particularmente útil para links.</p>
<ul>
<li><code>text-decoration-line</code> - <em>{overline, line-through, underline}</em>: Añade una línea al texto, ya sea arriba, abajo o en medio, se puede poner más de un valor, separado por espacios, para combinar los valores.</li>
<li><code>text-decoration-color</code> - <em>color</em>: Color de la <em>decoration line</em>.</li>
<li><code>text-decoration-style</code> - <code>{dotted, dashed, solid, double, groove, ridge, inset, outset, none, hidde}</code>: Estilo de la línea de la <em>decoration line</em>.</li>
<li><code>text-decoration-thickness</code> - <em>length</em>, <em>%</em>, <em>auto</em>: Ancho de la línea de la <em>decoration line</em>.</li>
<li><code>text-decoration</code> - <code>line color style thickness</code>: Versión abreviada donde se especifican todas las propiedades en una sola.</li>
</ul>
<h4 id="mayúsculasminúsculas">Mayúsculas/Minúsculas:</h4>
<ul>
<li><code>text-transform</code> - <code>{uppercase, lowercase, capitalize}</code>: Se usa para transformar el texto a mayúsculas, minúsculas o para poner en mayúsculas la primera letra de cada palabra.</li>
</ul>
<h4 id="sangría-y-espacios">Sangría y espacios:</h4>
<ul>
<li><code>text-indent</code> - <code>length</code>: Sangría de la primera línea de un texto.</li>
<li><code>letter-spacing</code> - <code>length</code>: Espacio entre caracteres de un texto. Acepta valores negativos</li>
<li><code>line-height</code> - <code>length</code>: Espacio entre líneas de un texto.</li>
<li><code>word-spacing</code> - <code>length</code>, <code>normal</code> (default: <code>normal</code>): Espacio entre palabras de un texto.</li>
<li><code>white-space</code> - <code>{normal, nowrap, pre, pre-wrap, pre-line}</code>: Especifica como se manejan los espacios en blanco:
<ul>
<li><em>normal</em>: Más de un espacio se combinan en uno, se ignoran los saltos de línea y el texto se ajusta al tamaño de la ventana.</li>
<li><em>nowrap</em>: Similar a <em>normal</em>, pero el texto no se ajusta al tamaño de la ventana.</li>
<li><em>pre</em>: Se conservan el número de espacios en blanco y los saltos en línea solo en líneas nuevas.</li>
</ul>
</li>
</ul>
<h4 id="fuentes">Fuentes:</h4>
<p>Existen cinco familias de fuentes genéricas:</p>
<ul>
<li><em>Serif</em>: Times New Roman, Georgia, Garamond, etc.</li>
<li><em>Sans-serif</em>: Arial, Verdana, Helvetica, etc.</li>
<li><em>Monospace</em>: Courier New, Lucida Console, Mocano.</li>
<li><em>Cursive</em>: Brush Script MT, Lucida Handwriting, etc.</li>
<li><em>Fantasy</em>: Copperplate, papyrus, etc.</li>
</ul>
<p>Las propiedades son:</p>
<ul>
<li><code>font-family</code>: Nombre de la fuente, si el nombre tiene espacios poner entre comillas dobles. Es recomendado poner varias, separadas por coma.</li>
<li><code>font-style</code> - <code>{normal, italic, oblique}</code>: Específica si poner el texto en cursiva.</li>
<li><code>font-weight</code> - <code>{thin, extra light, light, normal, medium, semi bold, bold, extra bold, ultra bold}</code> o <code>number</code>: Ancho de la fuente, también puede ser un número, más o menos entre 100 y 900.</li>
<li><code>font-variant</code> - <code>{normal, small-caps}</code>: Especifica si la fuente debe de ser “small-caps”, que son en mayúsculas, pero de un tamaño menor al de las mayúsculas normales.</li>
<li><code>font-size</code> - <code>length</code> (default: 16px): Establece el tamaño de la fuente, aparte de establecerla con unidades normales se puede establecer como:
<ul>
<li><em>em</em>: Permite que los usuarios modifiquen el tamaño en los menús de sus navegadores. <code>1em</code> equivale a 16px que es el tamaño por default se recomienda paralelamente establecer <code>font-size: 100%</code>, en <code>&lt;body&gt;</code> y en el resto usar <em>em</em>. Ejemplo: <code>1em</code>.</li>
<li><em>vw</em>: El tamaño de la fuente se autoajusta al tamaño de la venta. <code>1vw</code> equivale a 1% del <em>viweport width</em>, es decir si el <em>viewport</em> es de 50cm entonces <code>1vw</code> es <em>0.5cm</em>.</li>
</ul>
</li>
<li><code>font</code> - <code>style variant weight size family</code>: Versión abreviada donde se pueden especificar varias propiedades en una sola, <code>font-size</code> y <code>font-family</code> son obligatorias.</li>
</ul>
<h5 id="web-safe-fonts">Web safe fonts:</h5>
<p>Son fuentes que son seguras y la mayoría de los navegadores y dispositivos pueden usar:</p>
<ul>
<li>Arial (sans-serif)</li>
<li>Verdana (sans-serif)</li>
<li>Helvetica (sans-serif)</li>
<li>Tahoma (sans-serif)</li>
<li>Trebuchet MS (sans-serif)</li>
<li>Times New Roman (serif)</li>
<li>Georgia (serif)</li>
<li>Garamond (serif)</li>
<li>Courier New (monospace)</li>
<li>Brush Script MT (cursive)</li>
</ul>
<h4 id="google-fonts">Google fonts:</h4>
<p>Para usar fuentes de Google se debe de crear un <code>&lt;link&gt;</code> en <code>&lt;head&gt;</code> y en CSS hacer referencia a la fuente con la propiedad <code>font-family</code>, usando el nombre de la fuente entre comillas dobles: <code>"font-name"</code>.</p>
<p><strong>Importante</strong>: Se recomienda poner otra fuente en caso de que la fuente de Google falle.</p>
<h2 id="contadores">Contadores</h2>
<p>Los contadores son como variables que son incrementadas por ciertas reglas de CSS, se utilizan 4 propiedades:</p>
<ul>
<li><code>counter-reset</code>: Crea o resetea un contador.</li>
<li><code>counter-increment</code>: Incrementa el valor de un contador.</li>
<li><code>content</code>: Inserta el contador generado</li>
<li><code>counter()</code>/<code>counters()</code>: Agrega el valor del contador a un elemento.</li>
</ul>
<p><strong>Ejemplo</strong>:</p>
<pre class=" language-css"><code class="prism  language-css"><span class="token selector">body </span><span class="token punctuation">{</span>
<span class="token comment">/* crea el contador "section" */</span>
  <span class="token property">counter-reset</span><span class="token punctuation">:</span> section<span class="token punctuation">;</span>
<span class="token punctuation">}</span>

<span class="token selector">h2<span class="token pseudo-element">::before</span> </span><span class="token punctuation">{</span>
<span class="token comment">/* indica que se incremente el contador "section" */</span>
  <span class="token property">counter-increment</span><span class="token punctuation">:</span> section<span class="token punctuation">;</span>
<span class="token comment">/* Agrega el valor del contador, counter() no va entre comillas*/</span>
  <span class="token property">content</span><span class="token punctuation">:</span> <span class="token string">"Section "</span> <span class="token function">counter</span><span class="token punctuation">(</span>section<span class="token punctuation">)</span> <span class="token string">": "</span><span class="token punctuation">;</span>
<span class="token punctuation">}</span>
</code></pre>
<h2 id="backgrounds">Backgrounds:</h2>
<p>Propiedades relacionadas con el fondo de un elemento.</p>
<ul>
<li><code>background-color</code> - <code>color</code> (default: <code>transparent</code>): Especifica el color de fondo de un elemento.</li>
<li><code>opacity</code> - <code>num: [0.0, 1.0]</code> (default: <code>1</code>): Especifica la transparencia de un elemento, donde 0 es transparente. <strong>Importante</strong>: Esta propiedad se hereda a los elementos hijos, para ello mejor determina la transparencia en el color.</li>
<li><code>background-image</code> - <code>function</code>, <code>none</code> (default: <code>none</code>): Establece el _background _con una imagen para un elemento, la imagen se repite para cubrir todo el elemento. Algunas opciones son:</li>
<li><code>url()</code>: Especifica una dirección o ruta a una imagen. La url se pone entre comillas dobles, es preferible tener la imagen en la misma carpeta del proyecto en una subcarpeta llamada <em>img</em>.</li>
<li><code>linear-gradient()</code>: Especifica un fondo gradiente lineal.</li>
<li><code>radial-gradient()</code>: Especifica un fondo gradiente radial.</li>
<li><code>background-repeat</code> - <code>{repeat-x, repear-y, no-repeat}</code> (default: <code>repeat</code>): Controla como repetir la imagen en <code>background-image</code>. Por default se repite tanto horizontalmente como verticalmente.  Las opciones son:
<ul>
<li><em>repeat-x</em>: Para que se repita solo de manera horizontal.</li>
<li><em>repeat-y</em>: Repite la imagen solo de manera vertical.</li>
<li><em>no-repeat</em>: Para que no se repita la imagen.</li>
</ul>
</li>
<li><code>background-position</code> - <code>% %</code> o 2 de las sig. Opciones <code>{top, bottom, left, right, center}</code> (default: <code>0% 0%</code>): Indica la posición de la imagen de <code>background-image</code>, particularmente útil si <code>background-repeat: no-repeat</code>. Se puede definir como:
<ul>
<li>Un porcentaje con respecto al eje horizontal y vertical: <code>background-position: x% y%;</code></li>
<li>Una combinación de las <em>keywords</em> para el eje vertical y horizontal: <code>background-position: y_keyword x_keyword;</code></li>
</ul>
</li>
<li><code>background-attachment</code> - <code>{fixed, scroll}</code> (default: <code>scroll</code>): Indica si la imagen debe de moverse al hacer <em>scroll</em> o quedarse fija.</li>
<li><code>background</code> - <code>color image repeat position attachment</code>: Versión abreviada, donde se especifican todas las propiedades del <em>background</em> en una sola propiedad, el orden no importa.</li>
</ul>
<p><strong>Otros</strong>:</p>
<ul>
<li><code>background-size</code>: Tamaño de la imagen.</li>
<li><code>background-origin</code>: _Origin _(ubicación de la imagen) de la imagen.</li>
<li><code>background-clip</code>: Define la extensión (área) del _background _dentro del elemento.</li>
</ul>
<h2 id="listas">Listas:</h2>
<p>Propiedades de lista:</p>
<ul>
<li><code>list-style-type</code>: Estilo del <em>marker</em>, el valor depende de si es <code>&lt;ol&gt;</code> o <code>&lt;ul&gt;</code>.
<ul>
<li><code>&lt;ul&gt;</code>: valores posibles <code>{circle, square, none}</code>.</li>
<li><code>&lt;ol&gt;</code>:</li>
</ul>
</li>
<li><code>list-style-image</code> - <code>function</code>: Utiliza una imagen como <em>marker</em>, usando la función <code>url()</code>.</li>
<li><code>list-style-position</code> - <code>{outside, inside}</code>: Para indicar si el texto debe tener sangría con respecto al <em>marker</em> (cuando un elemento de la lista abarca dos o más líneas).</li>
<li><code>list-style</code> - <code>type position image</code>: Versión abreviada para establecer varias propiedades en una, el orden importa.</li>
<li><code>padding</code> - <code>number</code>: Se utiliza para definir qué tanta sangría tienen los elementos.</li>
</ul>
<h2 id="tablas">Tablas:</h2>
<h3 id="selectores">Selectores:</h3>
<ul>
<li><code>tr:hover</code>: Para que se resalte una fila al pasar el mouse por encima.</li>
<li><code>tr:nth-child()</code>: Para seleccionar las filas pares (<em>even</em>) o impares (<em>odd</em>) incluyendo el encabezado.</li>
</ul>
<h3 id="general">General:</h3>
<ul>
<li><code>text-align</code> - <code>{left, right, center}</code>: Alineación del texto. Se especifica en <code>&lt;td&gt;</code> o <code>&lt;th&gt;</code>.</li>
<li><code>vertical-align</code> - <code>{top, bottom, middle}</code>: Alineación vertical del texto. Se especifica en <code>&lt;td&gt;</code> o <code>&lt;th&gt;</code>.</li>
<li><code>padding</code> - <code>length</code> Espacio ente los bordes y el contenido de la tabla. Se especifica en <code>&lt;td&gt;</code> o <code>&lt;th&gt;</code>.</li>
</ul>
<h3 id="bordes">Bordes</h3>
<p>Los bordes se definen para <code>&lt;table&gt;,</code> <code>&lt;th&gt;</code> y <code>&lt;td&gt;</code>.</p>
<ul>
<li><code>border</code> - <code>width style color</code>: Establece varias propiedades del borde. Se pueden usar propiedades específicas para solo especificar un borde, ejemplo:<br>
o	<code>border-bottom</code>.</li>
<li><code>border-collapse</code> - <code>{separate, collapse}</code> (default: <code>separate</code>): Como <code>&lt;th&gt;</code> y <code>&lt;td&gt;</code> tienen bordes independientes, entonces puede parecer como si tuvieran doble borde, para evitar eso usar <code>collapse</code>.</li>
</ul>
<h2 id="borders">Borders:</h2>
<p>Especifican las propiedades de los bordes de los elementos. <strong>Importante</strong>: Las siguientes propiedades serán la general para todos los lados, pero existen las mismas propiedades para cada lado individual.</p>
<ul>
<li><code>border-style</code> - <code>{dotted, dashed, solid, double, groove, ridge, inset, outset, none, hidde}</code> (defult: <code>none</code>). Estilo del borde. Para visualizar cada estilo consulta la imagen.</li>
<li><code>border-width</code> - 1 a 4 de <code>lenght</code> o <code>{thin, medium, thick}</code>: Ancho del borde. Puede ser un tamaño específico o un valor predefinido. Se puede especificar todos los lados o lados específicos. Para más información consulta Box-model.</li>
<li><code>border-color</code> - 1 a 4 de  <code>color</code>: Color del borde. Si no se especifica hereda el color del elemento padre. Se puede especificar todos los lados o lados específicos. Para más información consulta Box-model.</li>
<li><code>border</code> - <code>color style width</code>: Versión abreviada, donde se especifican algunas propiedades del <em>border</em> en una sola propiedad.</li>
<li><code>border-radius</code> <code>\- 1 a 4 de</code>number<code>(default:</code>0`): Define el radio de las esquinas, es para hacer redondeadas las esquinas. Se puede usar pixeles (<em>px</em>) o porcentajes (<em>%</em>). Se puede especificar todos los lados o lados específicos. Para más información consulta Box-model.</li>
</ul>
<p><strong>Ejemplo</strong>:<br>
Tabla con desplazador horizontal:</p>
<pre class=" language-css"><code class="prism  language-css">&lt;div style=<span class="token string">"overflow-x: auto;"</span>&gt;
&lt;table&gt;
<span class="token number">...</span> table content <span class="token number">...</span>
&lt;/table&gt;
&lt;/div&gt; 
</code></pre>
<p><strong>Estilos de bordes</strong>:</p>
<p><img src="https://www.w3.org/community/webed/wiki/images/a/af/Cssed_borderstyles.png" alt="Estilos de bordes."></p>
<h2 id="margin">Margin:</h2>
<p>Especifican el ancho del espacio que hay entre un elemento y el resto de los elementos.<br>
<strong>Importante</strong>: Los elementos que están juntos pueden colapsar su <em>margin</em>, es decir si hay dos elementos, cada uno con su <em>margin</em> especificado, puede que solo se muestre el de mayor ancho, porque se colapsaron los <em>margins</em>, no se mostraría la suma de ambos, sino solo el mayor, eso pasa verticalmente, se colapsan los <em>margins</em> verticales de los elementos en el de mayor <em>margin</em>.</p>
<ul>
<li><code>margin-top</code> - <code>length</code>, <code>inherit</code>, <code>Percentage%</code>: Ancho de la parte superior.</li>
<li><code>margin-bottom</code> - <code>length</code>, <code>inherit</code>, <code>Percentage%</code>: Ancho de la parte inferior.</li>
<li><code>margin-left</code> - <code>length</code>, <code>inherit</code>, <code>Percentage%</code>: Ancho de la parte izquierda.</li>
<li><code>margin-right</code> - <code>length</code>, <code>inherit</code>, <code>Percentage%</code>: Ancho de la parte derecha.</li>
<li><code>margin</code> - 4 de <code>length</code>, <code>auto</code>, <code>inherit</code>: Versión abreviada, se tiene que indicar cada propiedad o por pares, revisa Box-model para más información.</li>
</ul>
<h2 id="padding">Padding:</h2>
<p>Especifica el ancho entre el contenido y el borde de un elemento.</p>
<p><strong>Importante</strong> el <em>padding</em> influye en la propiedad <em>width</em> de los elementos, por lo que el <em>width</em> final de un elementos será <em>width + padding</em> (izquierdo y derecho), para evitar eso usar la propiedad <code>box-sizing</code>.</p>
<ul>
<li><code>padding-top</code> - <code>length</code>, <code>inherit</code>, <code>Percentage%</code>: Ancho de la parte superior.</li>
<li><code>padding-bottom</code> - <code>length</code>, <code>inherit</code>, <code>Percentage%</code>: Ancho de la parte inferior.</li>
<li><code>padding-left</code> - <code>length</code>, <code>inherit</code>, <code>Percentage%</code>: Ancho de la parte izquierda.</li>
<li><code>padding-right</code> - <code>length</code>, <code>inherit</code>, <code>Percentage%</code>: Ancho de la parte derecha.</li>
<li><code>padding</code> - 4 de <code>length</code>, <code>auto</code>: Versión abreviada, se tiene que indicar cada propiedad o por pares, revisa Box-model para más información.</li>
</ul>
<h2 id="outline">Outline:</h2>
<p>Es una línea que se pone alrededor de los elementos, entre el <em>border</em> y el <em>margin</em>, se usa para resaltar algunos elementos. No forma parte de la dimensión del elemento y puede que se encime con otros elementos:</p>
<ul>
<li><code>outline-style</code> - <code>{dotted, dashed, solid, double, groove, ridge, inset, outset, none, hidde}</code> (defult: <code>none</code>). Estilo del <em>outline</em>. Para ver como se ve cada estilo consulta más abajo la imagen.</li>
<li><code>outline-color</code> - 4 de <code>color</code>: Color del outline. Puede ser un tamaño específico o un valor predefinido en cierta unidad.</li>
<li><code>outlone-width</code> - <code>length</code> o <code>{thin, medium, thick}</code>: Ancho del <em>outline</em>. Puede ser un tamaño específico o un valor predefinido en cierta unidad.</li>
<li><code>outline-offset</code> - <code>length</code>: Especifica un espacio transparente entre el <em>border</em> y el <em>outline</em>.</li>
<li><code>outline</code> - <code>width style color</code>: Versión abreviada para definir el ancho, estilo y color al mismo tiempo. No importa el orden.</li>
</ul>
<p><img src="https://storage.googleapis.com/dycr-web/image/topic/css/outline-view.png" alt="Outline."></p>
<h2 id="imágenes.">Imágenes.</h2>
<p>Algunas propiedades del elemento <code>&lt;img&gt;</code>:</p>
<ul>
<li><code>opacity</code> - <code>number: [0,1]</code>: Transparencia de la imagen, siendo 0 completamente transparente.</li>
</ul>
<p><strong>Selectores</strong>:</p>
<ul>
<li><code>img:hover {}</code>:</li>
</ul>
<h2 id="estilo-del-cursor">Estilo del cursor:</h2>
<p>Se refiere al tipo de cursor que aparece al poner el mouse sobre un elemento:</p>
<ul>
<li><code>cursor</code> - <code>{auto, crosshair, default, e-resize, help, move, n-resize, ne-resize, nw-resize, pointer, progress, s-resize, se-resize, sw-resize, text, w-resize, wait}</code>: Para ver cómo se ve cada uno visita <a href="https://cssreference.io/property/cursor/">esta pagína</a> (coloca el cursor sobre el texto).<br>
.</li>
</ul>
<h2 id="alto-y-ancho">Alto y ancho:</h2>
<p>Propiedades relacionadas con el alto y ancho del contenido de un elemento, sin incluir <em>padding</em>, <em>border</em> ni <em>margin</em>:</p>
<ul>
<li><code>width</code> -  <code>length</code>, <code>auto</code>, <code>Percentage%</code>, <code>initial</code>, <code>inherit</code> (default: <code>auto</code>): Ancho del elemento. Las opciones son:
<ul>
<li><em>auto</em>: Valor por default. El navegador calcula el ancho</li>
<li><em>lenght</em>. Define el ancho en unidades, como px, pt, cm, etc.</li>
<li><em>%</em>: Define el ancho como porcentaje del bloque contenedor.</li>
<li><em>initial</em>: Define el ancho a su valor por default.</li>
<li><em>inherit</em>: Hereda el ancho de su elemento padre.</li>
</ul>
</li>
<li><code>height</code> \ <code>length</code>, <code>auto</code>, <code>Percentage%</code>, <code>initial</code>, <code>inherit</code> (default: <code>auto</code>): Alto del elemento. Las opciones son:
<ul>
<li><em>auto</em>: Valor por default. El navegador calcula el ancho</li>
<li><em>lenght</em>. Define el ancho en unidades, como px, pt, cm, etc.</li>
<li><em>%</em>: Define el ancho como porcentaje del bloque contenedor.</li>
<li><em>initial</em>: Define el ancho a su valor por default.</li>
<li><em>inherit</em>: Hereda el ancho de su elemento padre.</li>
</ul>
</li>
<li><code>max-width</code> - <code>none</code>, <code>length</code>, <code>Percentage%</code> (default: <code>none</code>): Establece el ancho máximo de un elemento. Si la pantalla es menor a ese ancho el elemento se ajusta
<ul>
<li><code>none</code>: Define que no hay un ancho máximo.</li>
<li><code>lenght</code>. Define el ancho máximo en unidades, como px, pt, cm, etc.</li>
<li><code>%</code>: Define el ancho máximo como porcentaje del bloque contenedor.</li>
</ul>
</li>
<li><code>max-height</code> - <code>none</code>, <code>length</code>, <code>Percentage%</code> (default: <code>none</code>): Establece el alto máximo de un elemento. Si la pantalla es menor a ese alto el elemento se ajusta
<ul>
<li><code>none</code>: Define que no hay un ancho máximo.</li>
<li><code>lenght</code>. Define el ancho máximo en unidades, como px, pt, cm, etc.</li>
<li><code>%</code>: Define el ancho máximo como porcentaje del bloque contenedor.</li>
</ul>
</li>
</ul>
<p><strong>Otros</strong>:</p>
<ul>
<li><code>max-height</code>: Alto máximo.</li>
<li><code>min-height</code>: Alto mínimo.</li>
<li><code>min-width</code>: Ancho mínimo.</li>
</ul>
<h2 id="posición">Posición:</h2>
<p>Propiedades relacionadas con la propiedad <em>position</em>, se ponen después de haber especificado en tipo de posicionamiento.</p>
<ul>
<li><code>top</code> - <code>auto</code>, <code>length</code>: Define la posición del elemento de acuerdo a su parte superior.</li>
<li><code>left</code> - <code>auto</code>, <code>length</code>: Define la posición del elemento de acuerdo a su parte izquierda.</li>
<li><code>right</code> - <code>auto</code>, <code>length</code>: Define la posición del elemento de acuerdo a su parte derecha.</li>
<li><code>bottom</code> - <code>auto</code>, <code>length</code>: Define la posición del elemento de acuerdo a su parte inferior.</li>
</ul>
<h2 id="anexos">Anexos</h2>
<h3 id="colores">Colores:</h3>
<p>Hay diversas formas de determinar el color:</p>
<ul>
<li><strong>Nombre</strong>: aproximadamente hay 140 nombres con colores para revisar los nombres visitar <a href="https://htmlcolorcodes.com">esta página</a>.</li>
<li><strong>RGB</strong>: Se puede poner un código rgb para determinar el color, indicando sus componentes rojo, verde y azul, en valores entre 0 y 255 cada uno, de la siguiente manera: <br> <code>color:rgb(r,g,b)</code></li>
<li><strong>RGBA</strong>: Es con código rgb con transparencia, la transparencia se define con un número entre 0 y 1 en el argumento <em>alpha</em>, siendo uno completamente opaco: <br> <code>color:rgba(r,g,b,alpha)</code></li>
<li><strong>HSL</strong>: Es un código donde se indican el <em>hue</em>, <em>saturation</em> y <em>lightness</em>, <em>hue</em> va de 0 a 360, donde 0 es rojo, 120 es verde y 240 es azul. <em>Saturation</em> es un porcentaje de 0% a 100%, de gris a <em>full color</em> y <em>lightness</em> es un porcentaje de 0% a 100% de negro a blanco. Se ponen así tal cual, con el %: <br> <code>color:hsl(h,s,l)</code></li>
<li><strong>HSLA</strong>: Es con código <em>hsl</em> con transparencia, la transparencia se define con un número entre 0 y 1 en el argumento <em>alpha</em>, siendo 1 completamente opaco.: <br> <code>color:hsl(h,s,l,alpha)</code></li>
<li><strong>Hexadecimal</strong>: Código hexadecimal, que son combinaciones de números de 0 al 9 y las letras de la A a la F, que representan los valores rojo, verde y azul, similar a rgb, por ejemplo: <br> <code>#rrggbb</code></li>
<li><strong>Hexadecimal de 3 dígitos</strong>: Existe una versión alterna a la forma hexadecimal con tres dígitos. Representa a los colores rojo, verde y azul, pero solo cuando ambos componentes de <em>rr</em>, <em>gg</em> y <em>bb</em> son los mismo, por ejemplo <code>#ff00cc</code> se podría representar como <code>#f0c</code>: <br> <code>color: #rgb</code></li>
</ul>
<h3 id="lenght">Lenght</h3>
<p>Es un número seguido de una unidad. Formas de especificar longitudes y anchos:</p>
<ul>
<li><strong>Longitudes absolutas</strong>: Son longitudes fijas y aparecerán justo como se indiquen. Un número acompañado de una unidad, las unidades son:
<ul>
<li><em>pt</em>: Puntos</li>
<li><em>cm</em>: Centímetros</li>
<li><em>mm</em>: Milímetros.</li>
<li><em>in</em>: Pulgadas (1in = 96px = 2.54cm)</li>
<li><em>px</em>: Pixeles, es relativo al dispositivo. (1px = 1/96th of 1in)</li>
<li><em>pt</em>: Puntos (1pt = 1/72 of 1in)</li>
<li><em>pc</em>: Picas (1pc = 12 pt)</li>
</ul>
</li>
<li><strong>Longitudes relativas</strong>: Se especifica la longitud relativa a otra longitud:
<ul>
<li><em>em</em>: Relativo al tamaño de la fuente del elemento.</li>
<li><em>ex</em>: Relativo con la altura de la fuente actual (rara vez se usa).</li>
<li><em>ch</em>: En relación con el ancho del “0” (cero).</li>
<li><em>rem</em>: En relación con el tamaño de fuente del elemento raíz.</li>
<li><em>vw</em>: En relación con el 1% del ancho de la ventana gráfica*.</li>
<li><em>vh</em>: En relación con el 1% de la altura de la ventana gráfica*.</li>
<li><em>vmin</em>: En relación con el 1% de la dimensión más pequeña de la ventana gráfica*.</li>
<li><em>vmax</em>: En relación con el 1% de la dimensión más grande de la ventana gráfica*.</li>
<li><em>%</em>: En relación con el elemento primario.</li>
</ul>
</li>
</ul>

