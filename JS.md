---


---

<h1 id="js">JS</h1>
<p>Es un lenguaje para manipular los elementos de HTML y CSS. El código se pone dentro de las etiquetas <code>&lt;script&gt;</code> de HTML, la cual puede ir dentro de <code>&lt;body&gt;</code> o <code>&lt;head&gt;</code>. También se puede almacenar en archivos externos con la extensión <em>.js</em> y usar dentro del documento HTML con la etiqueta  <code>&lt;script&gt;</code> y el atributo <em>src</em>. Se puede usar tantos <code>&lt;script&gt;</code> como sean necesarios. Es recomendado utilizar archivos externos.</p>
<p>Las sentencias en JavaScript se separan con “;”. No es estrictamente necesario usarlo si cada sentencia se escribe en su propia línea, pero como quiera es buena práctica hacerlo.</p>
<br>
<h2 id="impresión-datos">Impresión datos:</h2>
<ul>
<li>Escribir en un elemento HTML: <code>innerHTML</code>.</li>
<li>Escribir dentro del output de HTML: <code>document.write()</code>.</li>
<li>Escribir dentro de un alert box: <code>window.alert()</code>.  Muestra una ventana con un mensaje.</li>
<li>Escribir dentro de la consola del navegador: <code>console.log()</code>, se pueden poner varios objetos separados por coma, y se imprimirá como si estuvieran concatenados por un espacio.</li>
</ul>
<br>
<h2 id="solicitud-de-datos">Solicitud de datos</h2>
<p>Para solicitar al usuario ingresar datos, se puede usar la función <code>prompt()</code>.</p>
<br>
<h2 id="incorporación-en-una-página-web">Incorporación en una página web:</h2>
<p>Existen 3 formas de incorporar JS en una página web:</p>
<h3 id="inline">Inline</h3>
<p>Cualquier elemento de HTML puede recibir un script, sin embargo no es considerado una buena práctica escribir scripts de esta manera. Ejemplo de un script inline:</p>
<pre class=" language-html"><code class="prism  language-html"><span class="token tag"><span class="token tag"><span class="token punctuation">&lt;</span>button</span>  <span class="token attr-name">onclick</span><span class="token attr-value"><span class="token punctuation">=</span><span class="token punctuation">"</span>alert(<span class="token punctuation">'</span>Hello, world!<span class="token punctuation">'</span>)<span class="token punctuation">"</span></span><span class="token punctuation">&gt;</span></span>Click  me!<span class="token tag"><span class="token tag"><span class="token punctuation">&lt;/</span>button</span><span class="token punctuation">&gt;</span></span>
</code></pre>
<ul>
<li>Los atributos donde se suelen escribir inline scripts son:
<ul>
<li><code>onclick</code>, <code>onload</code>, <code>onmouseover</code>, <code>Onmouseout</code>, <code>Onfocus</code>, <code>Onblur</code>.</li>
</ul>
</li>
</ul>
<br>
<h3 id="script-interno">Script interno:</h3>
<p>Son scripts que se suelen escribir dentro de los tags <code>&lt;head&gt;</code> o <code>&lt;body&gt;</code>, aunque lo más común es hacerlo en el body, y se escriben entre <code>&lt;script&gt; ... &lt;/script&gt;</code>. Ejemplo:</p>
<pre class=" language-html"><code class="prism  language-html"><span class="token tag"><span class="token tag"><span class="token punctuation">&lt;</span>script</span><span class="token punctuation">&gt;</span></span><span class="token script language-javascript">  
	console<span class="token punctuation">.</span><span class="token function">log</span><span class="token punctuation">(</span><span class="token string">'Welcome  to 30DaysOfJavaScript'</span><span class="token punctuation">)</span>  
</span><span class="token tag"><span class="token tag"><span class="token punctuation">&lt;/</span>script</span><span class="token punctuation">&gt;</span></span>
</code></pre>
<br>
<h3 id="script-externo">Script externo:</h3>
<p>Son scripts que se suelen escribir dentro de los tags <code>&lt;head&gt;</code> o <code>&lt;body&gt;</code>, aunque lo más común es hacerlo en el body, y se escriben en el atributo  src del tag <code>&lt;script&gt; ... &lt;/script&gt;</code>. Ejemplo:</p>
<pre class=" language-html"><code class="prism  language-html"><span class="token tag"><span class="token tag"><span class="token punctuation">&lt;</span>script</span> <span class="token attr-name">src</span><span class="token attr-value"><span class="token punctuation">=</span><span class="token punctuation">"</span>introduction.js<span class="token punctuation">"</span></span><span class="token punctuation">&gt;</span></span><span class="token script language-javascript"></span><span class="token tag"><span class="token tag"><span class="token punctuation">&lt;/</span>script</span><span class="token punctuation">&gt;</span></span>
</code></pre>
<ul>
<li>Se pueden insertar múltiples scripts de este tipo.</li>
</ul>
<br>
<h2 id="comentarios">Comentarios:</h2>
<p>Para escribir comentarios se una línea usar <code>//</code>, para escribir comentarios de múltiples líneas usar <code>/* ... */</code>:</p>
<pre class=" language-js"><code class="prism  language-js"><span class="token comment">// un comentario</span>

<span class="token comment">/*
Comentario
de multiples
líneas
*/</span>
</code></pre>
<hr>
<h2 id="operadores">Operadores:</h2>
<h3 id="operadores-aritméticos">Operadores aritméticos</h3>

<table>
<thead>
<tr>
<th>Operador</th>
<th>Descripción</th>
</tr>
</thead>
<tbody>
<tr>
<td><code>+</code></td>
<td>Suma</td>
</tr>
<tr>
<td><code>-</code></td>
<td>Resta</td>
</tr>
<tr>
<td><code>*</code></td>
<td>Multiplicación</td>
</tr>
<tr>
<td><code>**</code></td>
<td>Exponenciación (ES2016)</td>
</tr>
<tr>
<td><code>/</code></td>
<td>División</td>
</tr>
<tr>
<td><code>%</code></td>
<td>Módulo (Residuo)</td>
</tr>
<tr>
<td><code>++</code></td>
<td>Incremento</td>
</tr>
<tr>
<td><code>--</code></td>
<td>Decremento</td>
</tr>
</tbody>
</table><br>
<h3 id="operadores-de-asignación">Operadores de asignación:</h3>

<table>
<thead>
<tr>
<th>Operador</th>
<th>Ejemplo</th>
<th>Igual que</th>
</tr>
</thead>
<tbody>
<tr>
<td><code>=</code></td>
<td><code>x = y</code></td>
<td><code>x = y</code></td>
</tr>
<tr>
<td><code>+=</code></td>
<td><code>x += y</code></td>
<td><code>x = x + y</code></td>
</tr>
<tr>
<td><code>-=</code></td>
<td><code>x -= y</code></td>
<td><code>x = x - y</code></td>
</tr>
<tr>
<td><code>*=</code></td>
<td><code>x *= y</code></td>
<td><code>x = x * y</code></td>
</tr>
<tr>
<td><code>/=</code></td>
<td><code>x /= y</code></td>
<td><code>x = x / y</code></td>
</tr>
<tr>
<td><code>%=</code></td>
<td><code>x %= y</code></td>
<td><code>x = x % y</code></td>
</tr>
<tr>
<td><code>**=</code></td>
<td><code>x **= y</code></td>
<td><code>x = x ** y</code></td>
</tr>
</tbody>
</table><br>
<h3 id="operadores-de-comparación">Operadores de comparación:</h3>

<table>
<thead>
<tr>
<th>Operador</th>
<th>Descripción</th>
</tr>
</thead>
<tbody>
<tr>
<td><code>==</code></td>
<td>igual a</td>
</tr>
<tr>
<td><code>===</code></td>
<td>Igual valor e igual tipo</td>
</tr>
<tr>
<td><code>!=</code></td>
<td>no es igual</td>
</tr>
<tr>
<td><code>!==</code></td>
<td>No es igual al valor o no es igual al tipo</td>
</tr>
<tr>
<td><code>&gt;</code></td>
<td>mayor que</td>
</tr>
<tr>
<td><code>&lt;</code></td>
<td>menor que</td>
</tr>
<tr>
<td><code>&gt;=</code></td>
<td>mayor o igual que</td>
</tr>
<tr>
<td><code>&lt;=</code></td>
<td>menor o igual que</td>
</tr>
<tr>
<td><code>?</code></td>
<td>operador ternario</td>
</tr>
</tbody>
</table><p>El operador ternario es como un <em>if-else</em>:</p>
<pre class=" language-js"><code class="prism  language-js"><span class="token punctuation">(</span>condition<span class="token punctuation">)</span> <span class="token operator">?</span> val_true<span class="token punctuation">:</span> val_false 
</code></pre>
<ul>
<li>Dependiendo de si <em>condition</em> es <code>true</code> o <code>false</code>, entonces se retorna <code>val_true</code> o <code>val_false</code>.</li>
</ul>
<br>
<h3 id="operadores-lógicos">Operadores lógicos:</h3>

<table>
<thead>
<tr>
<th>Operador</th>
<th>Descripción</th>
</tr>
</thead>
<tbody>
<tr>
<td><code>&amp;&amp;</code></td>
<td>lógico Y</td>
</tr>
<tr>
<td><code>||</code></td>
<td>lógico O</td>
</tr>
<tr>
<td><code>!</code></td>
<td>lógico NO</td>
</tr>
</tbody>
</table><br>
<h3 id="operadores-bitwise">Operadores bitwise</h3>

<table>
<thead>
<tr>
<th>Operador</th>
<th>Descripción</th>
<th>Ejemplo</th>
<th>Igual que</th>
<th>Resultado</th>
<th>Decimal</th>
</tr>
</thead>
<tbody>
<tr>
<td><code>&amp;</code></td>
<td>AND</td>
<td><code>5 &amp; 1</code></td>
<td><code>0101 &amp; 0001</code></td>
<td>0001</td>
<td>1</td>
</tr>
<tr>
<td><code>|</code></td>
<td>OR</td>
<td><code>5 | 1</code></td>
<td><code>0101 | 0001</code></td>
<td>0101</td>
<td>5</td>
</tr>
<tr>
<td><code>~</code></td>
<td>NOT</td>
<td><code>~ 5</code></td>
<td><code>~0101</code></td>
<td>1010</td>
<td>10</td>
</tr>
<tr>
<td><code>^</code></td>
<td>XOR</td>
<td><code>5 ^ 1</code></td>
<td><code>0101 ^ 0001</code></td>
<td>0100</td>
<td>4</td>
</tr>
<tr>
<td><code>&lt;&lt;</code></td>
<td><em>left shift</em></td>
<td><code>5 &lt;&lt; 1</code></td>
<td><code>0101 &lt;&lt; 1</code></td>
<td>1010</td>
<td>10</td>
</tr>
<tr>
<td><code>&gt;&gt;</code></td>
<td><em>right shift</em></td>
<td><code>5 &gt;&gt; 1</code></td>
<td><code>0101 &gt;&gt; 1</code></td>
<td>0010</td>
<td>2</td>
</tr>
<tr>
<td><code>&gt;&gt;&gt;</code></td>
<td><em>unsigned right shift</em></td>
<td><code>5 &gt;&gt;&gt; 1</code></td>
<td><code>0101 &gt;&gt;&gt; 1</code></td>
<td>0010</td>
<td>2</td>
</tr>
</tbody>
</table><br>
<h3 id="cadenas">Cadenas:</h3>
<p>Para concatenar cadenas de utiliza el símbolo <code>+</code> o <code>+=</code>:</p>
<pre class=" language-js"><code class="prism  language-js">string1 <span class="token operator">+</span> string2 

string1 <span class="token operator">+=</span> string2 
</code></pre>
<br>
<h3 id="jerarquia-de-operaciones">Jerarquia de operaciones:</h3>

<table>
<thead>
<tr>
<th>Operador</th>
<th>Orden</th>
<th>Descripción</th>
<th>Ejemplo</th>
</tr>
</thead>
<tbody>
<tr>
<td><code>( )</code></td>
<td>21</td>
<td>Agrupación de expresiones</td>
<td><code>(3 + 4)</code></td>
</tr>
<tr>
<td><code>.</code></td>
<td>20</td>
<td>Miembro</td>
<td><code>object.name</code></td>
</tr>
<tr>
<td><code>[]</code></td>
<td>20</td>
<td>Miembro</td>
<td><code>object["name"]</code></td>
</tr>
<tr>
<td><code>()</code></td>
<td>20</td>
<td>Llamada de función</td>
<td><code>myFunction()</code></td>
</tr>
<tr>
<td><code>new</code></td>
<td>20</td>
<td>Crear</td>
<td><code>new Date()</code></td>
</tr>
<tr>
<td><code>++</code></td>
<td>18</td>
<td>Incremento de postfijo</td>
<td><code>i++</code></td>
</tr>
<tr>
<td><code>--</code></td>
<td>18</td>
<td>Decremento de postfijo</td>
<td><code>i--</code></td>
</tr>
<tr>
<td><code>++</code></td>
<td>17</td>
<td>Incremento de prefijo</td>
<td><code>++i</code></td>
</tr>
<tr>
<td><code>--</code></td>
<td>17</td>
<td>Decremento del prefijo</td>
<td><code>--i</code></td>
</tr>
<tr>
<td><code>!</code></td>
<td>17</td>
<td>Lógico NO</td>
<td><code>!(x==y)</code></td>
</tr>
<tr>
<td><code>typeof</code></td>
<td>17</td>
<td>Tipo</td>
<td><code>typeof x</code></td>
</tr>
<tr>
<td><code>**</code></td>
<td>16</td>
<td>Exponenciación</td>
<td><code>10 ** 2</code></td>
</tr>
<tr>
<td><code>*</code></td>
<td>15</td>
<td>Multiplicación</td>
<td><code>10 * 5</code></td>
</tr>
<tr>
<td><code>/</code></td>
<td>15</td>
<td>División</td>
<td><code>10 / 5</code></td>
</tr>
<tr>
<td><code>%</code></td>
<td>15</td>
<td>Residuo de la división</td>
<td><code>10 % 5</code></td>
</tr>
<tr>
<td><code>+</code></td>
<td>14</td>
<td>Adición</td>
<td><code>10 + 5</code></td>
</tr>
<tr>
<td><code>-</code></td>
<td>14</td>
<td>Sustracción</td>
<td><code>10 - 5</code></td>
</tr>
<tr>
<td><code>&lt;&lt;</code></td>
<td>13</td>
<td><em>Shift left</em></td>
<td><code>x &lt;&lt; 2</code></td>
</tr>
<tr>
<td><code>&gt;&gt;</code></td>
<td>13</td>
<td><em>Shift right</em></td>
<td><code>x &gt;&gt; 2</code></td>
</tr>
<tr>
<td><code>&gt;&gt;&gt;</code></td>
<td>13</td>
<td><em>Shift right (unsigned)</em></td>
<td><code>x &gt;&gt;&gt; 2</code></td>
</tr>
<tr>
<td><code>&lt;</code></td>
<td>12</td>
<td>Menor que</td>
<td><code>x &lt; y</code></td>
</tr>
<tr>
<td><code>&lt;=</code></td>
<td>12</td>
<td>Menor o igual que</td>
<td><code>x &lt;= y</code></td>
</tr>
<tr>
<td><code>&gt;</code></td>
<td>12</td>
<td>Mayor que</td>
<td><code>x &gt; y</code></td>
</tr>
<tr>
<td><code>&gt;=</code></td>
<td>12</td>
<td>Mayor o igual que</td>
<td><code>x &gt;= y</code></td>
</tr>
<tr>
<td><code>in</code></td>
<td>12</td>
<td>Membresía</td>
<td><code>"PI" in Math</code></td>
</tr>
<tr>
<td><code>instanceof</code></td>
<td>12</td>
<td>Instancia de un objeto</td>
<td><code>instanceof Array</code></td>
</tr>
<tr>
<td><code>==</code></td>
<td>11</td>
<td>Igual que</td>
<td><code>x == y</code></td>
</tr>
<tr>
<td><code>===</code></td>
<td>11</td>
<td>Igual estricto</td>
<td><code>x === y</code></td>
</tr>
<tr>
<td><code>!=</code></td>
<td>11</td>
<td>Desigual</td>
<td><code>x != y</code></td>
</tr>
<tr>
<td><code>!==</code></td>
<td>11</td>
<td>Desigual estricto</td>
<td><code>x !== y</code></td>
</tr>
<tr>
<td><code>&amp;</code></td>
<td>10</td>
<td>Bitwise AND</td>
<td><code>x &amp; y</code></td>
</tr>
<tr>
<td><code>^</code></td>
<td>9</td>
<td>Bitwise XOR</td>
<td><code>x ^ y</code></td>
</tr>
<tr>
<td><code>|</code></td>
<td>8</td>
<td>Bitwise OR</td>
<td><code>x | y</code></td>
</tr>
<tr>
<td><code>&amp;&amp;</code></td>
<td>7</td>
<td>Logical AND</td>
<td><code>x &amp;&amp; y</code></td>
</tr>
<tr>
<td><code>||</code></td>
<td>6</td>
<td>Logical OR</td>
<td><code>x || y</code></td>
</tr>
<tr>
<td><code>??</code></td>
<td>5</td>
<td><em>Nullish Coalescing</em></td>
<td><code>x ?? y</code></td>
</tr>
<tr>
<td><code>? :</code></td>
<td>4</td>
<td>Operador ternario</td>
<td><code>? "Yes" : "No"</code></td>
</tr>
<tr>
<td><code>+=</code></td>
<td>3</td>
<td>Asignación</td>
<td><code>x += y</code></td>
</tr>
<tr>
<td><code>/=</code></td>
<td>3</td>
<td>Asignación</td>
<td><code>x /= y</code></td>
</tr>
<tr>
<td><code>-=</code></td>
<td>3</td>
<td>Asignación</td>
<td><code>x -= y</code></td>
</tr>
<tr>
<td><code>*=</code></td>
<td>3</td>
<td>Asignación</td>
<td><code>x *= y</code></td>
</tr>
<tr>
<td><code>%=</code></td>
<td>3</td>
<td>Asignación</td>
<td><code>x %= y</code></td>
</tr>
<tr>
<td><code>&lt;&lt;=</code></td>
<td>3</td>
<td>Asignación</td>
<td><code>x &lt;&lt;= y</code></td>
</tr>
<tr>
<td><code>&gt;&gt;=</code></td>
<td>3</td>
<td>Asignación</td>
<td><code>x &gt;&gt;= y</code></td>
</tr>
<tr>
<td><code>&gt;&gt;&gt;=</code></td>
<td>3</td>
<td>Asignación</td>
<td><code>x &gt;&gt;&gt;= y</code></td>
</tr>
<tr>
<td><code>&amp;=</code></td>
<td>3</td>
<td>Asignación</td>
<td><code>x &amp;= y</code></td>
</tr>
<tr>
<td><code>^=</code></td>
<td>3</td>
<td>Asignación</td>
<td><code>x ^= y</code></td>
</tr>
<tr>
<td><code>|=</code></td>
<td>3</td>
<td>Asignación</td>
<td><code>x |= y</code></td>
</tr>
<tr>
<td><code>yield</code></td>
<td>2</td>
<td><em>Pause function</em></td>
<td><code>yield x</code></td>
</tr>
<tr>
<td><code>,</code></td>
<td>1</td>
<td>Coma</td>
<td><code>5 , 6</code></td>
</tr>
</tbody>
</table><br>
<hr>
<h2 id="keywords">Keywords:</h2>

<table>
<thead>
<tr>
<th>Keyword</th>
<th>Descripción</th>
</tr>
</thead>
<tbody>
<tr>
<td><code>var</code></td>
<td>Declarar una variable.</td>
</tr>
<tr>
<td><code>let</code></td>
<td>Declarar una variable de bloque.</td>
</tr>
<tr>
<td><code>const</code></td>
<td>Declarar una constante de bloque.</td>
</tr>
<tr>
<td><code>if</code></td>
<td>Sentencia de control <code>if</code>.</td>
</tr>
<tr>
<td><code>switch</code></td>
<td>Sentencia de control <code>switch</code>.</td>
</tr>
<tr>
<td><code>for</code></td>
<td>Ciclo <code>for</code>.</td>
</tr>
<tr>
<td><code>function</code></td>
<td>Declara una función.</td>
</tr>
<tr>
<td><code>return</code></td>
<td>Retorna un valor de una función.</td>
</tr>
<tr>
<td><code>try</code></td>
<td>Implementa un manejador de error para un bloque de sentencias.</td>
</tr>
</tbody>
</table><br>
<h3 id="this">This:</h3>
<p><code>this</code> se refiere a un objeto que depende de cómo fuera llamado o usado el <em>keyword</em>.</p>
<ul>
<li>En un método de objeto, <code>this</code> hace referencia al objeto.</li>
<li>Por sí solo, <code>this</code> se refiere al objeto global. En un ventana de navegador se refiera a <code>&lt;Window&gt;</code>.</li>
<li>En una función, <code>this</code> se refiere al objeto global. En un ventana de navegador se refiera a <code>&lt;Window&gt;</code>.</li>
<li>En una función, en modo estricto, <code>this</code> es <code>undefined</code>.</li>
<li>En un evento, <code>this</code> hace referencia al elemento (de HTML) que recibió el evento.</li>
<li>Métodos como <code>call()</code>, <code>apply()</code> y <code>bind()</code>, <code>this</code> puede referir a cualquier objeto.</li>
</ul>
<br>
<p><strong>Jerarquía para saber a qué objeto se refiere <code>this</code></strong>:</p>

<table>
<thead>
<tr>
<th>Precedencia</th>
<th>Objeto</th>
</tr>
</thead>
<tbody>
<tr>
<td>1</td>
<td><code>bind()</code></td>
</tr>
<tr>
<td>2</td>
<td><code>apply()</code> y<code>call()</code></td>
</tr>
<tr>
<td>3</td>
<td>Método de objeto</td>
</tr>
<tr>
<td>4</td>
<td>Ambiente global</td>
</tr>
</tbody>
</table><br>
<h3 id="objetos">Objetos:</h3>

<table>
<thead>
<tr>
<th>Operador</th>
<th>Descripción</th>
</tr>
</thead>
<tbody>
<tr>
<td><code>typeof</code></td>
<td>Devuelve el tipo de dato de una variable.</td>
</tr>
<tr>
<td><code>instanceof</code></td>
<td>Devuelve <code>true</code> si un objeto es una instancia de un tipo de objeto.</td>
</tr>
</tbody>
</table><h4 id="typeof">typeof</h4>
<p>Retorna el tipo de dato que es una variable o un valor.</p>
<pre class=" language-js"><code class="prism  language-js"><span class="token comment">// Verificar el tipo de dato de "x"</span>
<span class="token keyword">typeof</span> x
</code></pre>
<ul>
<li><em>x</em> es una variable o valor.</li>
<li>Los posibles valores que retorna son:
<ul>
<li>“string”</li>
<li>“number”</li>
<li>“boolean”</li>
<li>“undefined”</li>
<li>“object”</li>
<li>“function”.</li>
</ul>
</li>
</ul>
<p>Para ver si un objeto es del tipo <code>Array</code> usar el método <code>Array.isArray()</code>:</p>
<pre class=" language-js"><code class="prism  language-js"><span class="token comment">// Verificar si "a" es un array</span>
Array<span class="token punctuation">.</span><span class="token function">isArray</span><span class="token punctuation">(</span>a<span class="token punctuation">)</span>
</code></pre>
<ul>
<li><em>a</em> es cualquier objeto.</li>
</ul>
<p>Para otro tipo de datos como <code>Map</code>, <code>Set</code>, <code>Date</code>, etc. se puede usar la propiedad <code>.constructor</code> que retorna el constructor de todo tipo de variables:</p>
<pre class=" language-js"><code class="prism  language-js"><span class="token comment">// Verificar el tipo de dato de otra clase de objetos</span>
x<span class="token punctuation">.</span>constuctor 
</code></pre>
<br>
<h4 id="instanceof">instanceOf</h4>
<p>Verifica que un objeto sea una instancia de una clase específica:</p>
<pre class=" language-js"><code class="prism  language-js"><span class="token comment">// Verificar si obj es una instancia de type</span>
obj instanceOf <span class="token class-name">type</span> 
</code></pre>
<ul>
<li><em>type</em> es el nombre de una clase, ya sea una estándar o una creada por el usuario.</li>
</ul>
<blockquote>
<p><strong>Nota</strong>: Las instancias de clases que son “clases hijas”, también serán instancias de las clases padre.</p>
</blockquote>
<br>
<hr>
<h2 id="tipos-de-datos.">Tipos de datos.</h2>
<p>Existen 8 tipos básico en JavaScript, los primeros 7 se conocen como “primitivos”, algunas características de los tipos primitivos y no primitivos:</p>
<ul>
<li><code>boolean</code>: Los valores <code>true</code> y <code>false</code>.</li>
<li><code>null</code>: Una palabra clave especial que indica un valor nulo (no tiene valor). Como JavaScript distingue entre mayúsculas y minúsculas, null no es lo mismo que <em>Null</em>, <em>NULL</em> o cualquier otra variante.</li>
<li><code>undefined</code>: Una propiedad cuyo valor no está definido. Las variables no inicializadas y las funciones que no retornan nada son <code>undefined</code>.</li>
<li><code>number</code>: Un número entero o de coma flotante.</li>
<li><code>bigint</code>: Un entero con precisión arbitraria.</li>
<li><code>string</code>: Una secuencia de caracteres que representan un valor de texto.</li>
<li><code>symbol</code>: Un tipo de datos cuyas instancias son únicas e inmutables.</li>
<li><code>Object</code>: -.</li>
</ul>
<h3 id="clasificación-de-tipos-de-datos">Clasificación de tipos de datos:</h3>
<ul>
<li><strong>Primitivos</strong>: No se pueden modificar* una vez creados (inmutables) y se pueden comparar entre sí usando operadores de comparación.</li>
<li><strong>No primitivos</strong>: Se pueden modificar una vez creados y no se pueden comparar entre sí con operadores de comparación, sin embargo se puede verificar si hacen referencia al mismo objeto.</li>
<li><strong>Iterables</strong>: Son objetos que se pueden iterar usando <code>for...of loop</code>:
<ul>
<li>Arrays.</li>
<li>Strings.</li>
<li>Maps.</li>
<li>Sets.</li>
<li><em>Generators</em>.</li>
<li><em>Async generators</em>.</li>
<li>Objetos <em>Arguments</em>.</li>
<li>NodeLists.</li>
<li>Colecciones DOM.</li>
</ul>
</li>
</ul>
<p>*No confundir con que se puedan modificar las variables con tipos primitivos, es diferente. Por ejemplo:</p>
<pre class=" language-js"><code class="prism  language-js"><span class="token keyword">let</span> myString <span class="token operator">=</span> <span class="token string">"Hola"</span> 

myString<span class="token punctuation">[</span><span class="token number">0</span><span class="token punctuation">]</span> <span class="token operator">=</span> <span class="token string">"B"</span> <span class="token comment">// No se puede </span>

myString <span class="token operator">=</span> <span class="token string">"Adios"</span> <span class="token comment">// Sí se puede </span>
</code></pre>
<br> 
<hr>
<h3 id="number">number</h3>
<p>Solo existe un tipo de dato numérico. Se escriben con o sin decimales. Se pueden escribir números con notación científica:</p>
<pre class=" language-js"><code class="prism  language-js">\\ Número sin decimales 
<span class="token number">1000</span> 

\\ Número con decimales 
<span class="token number">1000.0</span> 

\\ Números en notación científica 
<span class="token number">10e3</span> 
<span class="token number">10e-3</span> 
<span class="token number">10E3</span> 
<span class="token number">10E-3</span> 
</code></pre>
<ul>
<li>Todos los números en JS son <em>float64</em>.</li>
</ul>
<br>
<h4 id="números-especiales">Números especiales:</h4>
<p>Algunos valores especiales son:</p>
<ul>
<li><code>NaN</code>: Representa que un objeto no es un número.</li>
<li><code>infinity</code>: Para representar un número muy grande, también es el valor devuelto en operaciones indefinidas.</li>
</ul>
<blockquote>
<p><strong>Importante</strong>: Para usar esos valores espaciales revisar las <a href="#propiedades-est%C3%A1ticas-de-number">propiedades</a> de <code>number</code>.</p>
</blockquote>
<br>
<h4 id="propiedades-estáticas-de-number">Propiedades estáticas de <code>number</code>:</h4>
<p>Para utilizar números especiales y otros valores usar las siguientes propiedades, directamente sobre el objeto <code>number</code>, no sobre las instancias:</p>

<table>
<thead>
<tr>
<th>Propiedad</th>
<th>Descripción</th>
</tr>
</thead>
<tbody>
<tr>
<td><code>number.MAX_VALUE</code></td>
<td>Devuelve el mayor número posible en JavaScript</td>
</tr>
<tr>
<td><code>number.MIN_VALUE</code></td>
<td>Devuelve el número más pequeño posible en JavaScript</td>
</tr>
<tr>
<td><code>number.POSITIVE_INFINITY</code></td>
<td>Representa infinito (devuelto al desbordamiento)</td>
</tr>
<tr>
<td><code>number.NEGATIVE_INFINITY</code></td>
<td>Representa el infinito negativo (devuelto en el desbordamiento)</td>
</tr>
<tr>
<td><code>number.NaN</code></td>
<td>Representa un valor “<em>Not-a-Number</em>”</td>
</tr>
</tbody>
</table><blockquote>
<p>Para una lista completa visitar la  <a href="https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Number#static_properties">documentación</a>.</p>
</blockquote>
<br>
<p><strong>Ejemplo</strong>: En este ejemplo se imprime el valor máximo posible:</p>
<pre class=" language-js"><code class="prism  language-js">console<span class="token punctuation">.</span><span class="token function">log</span><span class="token punctuation">(</span>number<span class="token punctuation">.</span>MAX_VALUE<span class="token punctuation">)</span>
</code></pre>
<br>
<h4 id="métodos-estáticos-de-number">Métodos estáticos de <code>number</code>:</h4>
<p>Se aplican directamente sobre el objeto <code>number</code>.</p>

<table>
<thead>
<tr>
<th>Método</th>
<th>Descripción</th>
</tr>
</thead>
<tbody>
<tr>
<td><code>number.parseFloat()</code></td>
<td>Analiza un argumento de cadena y devuelve un número de coma flotante.</td>
</tr>
<tr>
<td><code>number.parseInt()</code></td>
<td>Analiza un argumento de cadena y devuelve un entero de la base o radix especificada.</td>
</tr>
<tr>
<td><code>number.isFinite()</code></td>
<td>Determina si el valor pasado es un número finito.</td>
</tr>
<tr>
<td><code>number.isInteger()</code></td>
<td>Determina si el valor pasado es un número entero.</td>
</tr>
<tr>
<td><code>number.isNaN()</code></td>
<td>Determina si el valor pasado es NaN.</td>
</tr>
<tr>
<td><code>number.isSafeInteger()</code></td>
<td>Determina si el valor proporcionado es un número entero seguro.</td>
</tr>
</tbody>
</table><blockquote>
<p>Para una lista completa visitar la  <a href="https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Number#static_methods">documentación</a>.</p>
</blockquote>
<br>
<p><strong>Ejemplo</strong>: En este ejemplo se verifica si un número es un entero:</p>
<pre class=" language-js"><code class="prism  language-js"><span class="token keyword">const</span> x <span class="token operator">=</span> <span class="token number">25.5</span>
console<span class="token punctuation">.</span><span class="token function">log</span><span class="token punctuation">(</span>number<span class="token punctuation">.</span><span class="token function">isInteger</span><span class="token punctuation">(</span>x<span class="token punctuation">)</span><span class="token punctuation">)</span>
</code></pre>
<br>
<h4 id="métodos-de-instancia-de-number">Métodos de instancia de <code>number</code>:</h4>
<p>Se aplican sobre instancias de <code>number</code>.</p>
<blockquote>
<p>Para una lista completa visitar la  <a href="https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Number#instance_methods">documentación</a>.</p>
</blockquote>
<br>
<ul>
<li><code>number.toString(radix=10)</code> - <code>string</code>: Retorna un número como una cadena.
<ul>
<li><strong><code>radix</code></strong> - <code>number</code>: Número del 2 al 36 para indicar la base numérica.</li>
</ul>
</li>
</ul>
<br>
<ul>
<li><code>number.toFixed(digits)</code> - <code>string</code>: Retorna un número como una cadena con un número específico de decimales.
<ul>
<li><strong><code>digits</code></strong> - <code>number</code>: Número de decimales a incluir en la cadena.</li>
</ul>
</li>
</ul>
<br>
<ul>
<li><code>number.toPrecision(digits)</code> - <code>string</code>: Retorna un número como una cadena con una longitud específica, agregando ceros si es necesario.
<ul>
<li><strong><code>digits</code></strong> - <code>number</code>: Número de decimales a incluir en la cadena.</li>
</ul>
</li>
</ul>
<br>
<ul>
<li><code>number.toExponential(fractionDigits)</code> - <code>number</code>: Retorna el número en notación exponencial.
<ul>
<li><strong><code>fractionDigits</code></strong> - <code>number</code>: Número de dígitos después del punto decimal.</li>
</ul>
</li>
</ul>
<br>
<hr>
<h3 id="string">string</h3>
<p>Es un objeto que representa cadenas de caracteres. Las cadenas de caracteres pueden escribirse dentro de comillas simples, dobles o <em>backsticks</em>.</p>
<pre class=" language-js"><code class="prism  language-js"><span class="token comment">// Todas las siguientes opciones son válidas para escribir una cadena</span>
<span class="token keyword">const</span> foo <span class="token operator">=</span> <span class="token string">"my string 1"</span> 
<span class="token keyword">const</span> bar <span class="token operator">=</span> <span class="token string">'my string 2'</span>
<span class="token keyword">const</span> baz <span class="token operator">=</span> <span class="token template-string"><span class="token string">`my string 3`</span></span>
</code></pre>
<p>Es posible crear una cadena con el <em>wrapper</em> <code>String()</code>, pero no es necesario hacerlo de esta forma:</p>
<pre class=" language-js"><code class="prism  language-js"><span class="token comment">// Ejemplo usando String()</span>
<span class="token keyword">const</span> foo <span class="token operator">=</span> <span class="token keyword">new</span> <span class="token class-name">String</span><span class="token punctuation">(</span><span class="token string">"foo"</span><span class="token punctuation">)</span><span class="token punctuation">;</span> 
</code></pre>
<p>Se puede dividir una cadena en múltiples líneas usando el operador de concatenación:</p>
<pre class=" language-js"><code class="prism  language-js"><span class="token keyword">const</span> foo <span class="token operator">=</span> <span class="token string">"una línea"</span> <span class="token operator">+</span> 
	<span class="token string">"otra línea"</span> 
</code></pre>
<p>Otra forma de hacer una cadena de múltiples líneas es con:</p>
<pre class=" language-js"><code class="prism  language-js"><span class="token keyword">const</span> foo <span class="token operator">=</span> "una línea \ 
	otra línea" 
</code></pre>
<p>Las cadenas se pueden indexar usando corchetes y el índice del caracter:</p>
<pre class=" language-js"><code class="prism  language-js"><span class="token comment">// foo es string</span>
foo<span class="token punctuation">[</span>ind<span class="token punctuation">]</span>
</code></pre>
<ul>
<li><em>ind</em> es el índice del carácter, comienza en cero.</li>
<li>Indexar cadenas no siempre funciona correctamente.</li>
</ul>
<h4 id="cadenas-unicode">Cadenas unicode:</h4>
<p>Para crear cadenas con caracteres unicode usar <code>"\u"</code> seguido de al menos 4 dígitos hexadecimales, por ejemplo:</p>
<pre class=" language-js"><code class="prism  language-js"><span class="token keyword">const</span> foo <span class="token operator">=</span> <span class="token string">"\u00A9"</span> 
</code></pre>
<ul>
<li>Para revisar los códigos unicode visitar <a href="https://symbl.cc/en/unicode/table/">esta página</a>.</li>
</ul>
<h4 id="secuencias-de-escape">Secuencias de escape:</h4>
<p>Para insertar una secuencia de escape usar:</p>

<table>
<thead>
<tr>
<th>Code</th>
<th>Result</th>
<th>Description</th>
</tr>
</thead>
<tbody>
<tr>
<td><code>\'</code></td>
<td>’</td>
<td>Comilla simple</td>
</tr>
<tr>
<td><code>\"</code></td>
<td>"</td>
<td>Comilla doble</td>
</tr>
<tr>
<td><code>\\</code></td>
<td>\</td>
<td>Barra invertida</td>
</tr>
<tr>
<td><code>\b</code></td>
<td></td>
<td>Retroceso</td>
</tr>
<tr>
<td><code>\n</code></td>
<td></td>
<td>Nueva línea</td>
</tr>
<tr>
<td><code>\r</code></td>
<td></td>
<td>Retorno de carro</td>
</tr>
<tr>
<td><code>\t</code></td>
<td></td>
<td>Tabulador horizontal</td>
</tr>
<tr>
<td><code>\v</code></td>
<td></td>
<td>Tabulador vertical</td>
</tr>
</tbody>
</table><p>*Notar que se puede usar " " y ’ ’ simultáneamente para poder escribir cadenas con comillas dobles o simples en una cadena.</p>
<p><strong>Ejemplo</strong>: En el siguiente ejemplo se utiliza la secuencia <code>"\n"</code>, así como se ejemplifica el uso de comillas simples y dobles de manera simultánea.</p>
<pre class=" language-js"><code class="prism  language-js"><span class="token comment">// Uso de secuencias de escape</span>
myString <span class="token operator">=</span> <span class="token string">'La fórmula es: \n "E=mc**2"'</span>
</code></pre>
<h4 id="string-templates">String Templates:</h4>
<p>Otra forma de definir una cadena es con <em>backsticks</em>, de esta forma es posible incluir variables en la cadena, así como definir cadenas en múltiples líneas:</p>
<pre class=" language-js"><code class="prism  language-js"><span class="token comment">// Multiples líneas con backsticks</span>
<span class="token keyword">const</span> foo <span class="token operator">=</span> <span class="token template-string"><span class="token string">`una línea \ 
	otra línea`</span></span> 
</code></pre>
<p>Para incluir valores de variables en una cadena se utiliza <code>${...}</code>:</p>
<pre class=" language-js"><code class="prism  language-js"><span class="token comment">// Uso de template strings</span>
<span class="token keyword">const</span> x <span class="token operator">=</span> <span class="token number">2</span>
<span class="token keyword">const</span> foo <span class="token operator">=</span> <span class="token template-string"><span class="token string">`Dos al cuadrado: </span><span class="token interpolation"><span class="token interpolation-punctuation punctuation">${</span>x<span class="token operator">**</span><span class="token number">2</span><span class="token interpolation-punctuation punctuation">}</span></span><span class="token string">`</span></span> 
</code></pre>
<ul>
<li>Dentro de los corchetes se pueden poner variables, cálculos, etc.</li>
</ul>
<h4 id="propiedades-de-instancia-de-string">Propiedades de instancia de <code>string</code>:</h4>
<ul>
<li><code>string.length</code> - <code>number</code>: Retorna la longitud de la cadena.</li>
</ul>
<blockquote>
<p>Para más información visitar la  <a href="https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/String#instance_properties">documentación</a>.</p>
</blockquote>
<h4 id="métodos-de-instancia-de-string">Métodos de instancia de <code>string</code>:</h4>
<blockquote>
<p>Para una lista completa visitar la  <a href="https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/String#instance_methods">documentación</a>.</p>
</blockquote>
<h5 id="información">Información:</h5>
<ul>
<li><code>string.includes(searchString, position=0)</code> - <code>string</code>: Retorna <code>true</code> si la cadena contiene un patrón, en caso contrario retorna <code>false</code>.
<ul>
<li><code>searchString</code> - <code>string</code>: Cadena a buscar.</li>
<li><code>position</code> - <code>number</code>: Posición inicial desde donde buscar.</li>
</ul>
</li>
</ul>
<br>
<ul>
<li><code>string.startsWith(searchString, position=0)</code> - <code>string</code>: Retorna <code>true</code> si la cadena empieza por patrón, en caso contrario retorna <code>false</code>.
<ul>
<li><code>searchString</code> - <code>string</code>: Cadena a buscar.</li>
<li><code>position</code> - <code>number</code>: Posición inicial desde donde buscar.</li>
</ul>
</li>
</ul>
<br>
<ul>
<li><code>string.endsWith(searchString, position=0)</code> - <code>string</code>: Retorna <code>true</code> si la cadena empieza por patrón, en caso contrario retorna <code>false</code>.
<ul>
<li><code>searchString</code> - <code>string</code>: Cadena a buscar.</li>
<li><code>position</code> - <code>number</code>: Posición inicial desde donde buscar.</li>
</ul>
</li>
</ul>
<h5 id="subcadenas">Subcadenas:</h5>
<ul>
<li><code>string.slice(start, end = -1)</code> - <code>string</code>: Extraer parte de una cadena indicando su posición inicial y final.
<ul>
<li><code>start</code>, <code>end</code> - <code>number</code>: Posición inicial y final respectivamente, los índices comienzan en cero y end es exclusivo. Se pueden usar índices negativos para indicar desde el final de la cadena.</li>
</ul>
</li>
</ul>
<br>
<ul>
<li><code>string.substring(start, end = -1)</code> - <code>string</code>: Extraer parte de una cadena indicando su posición inicial y final.
<ul>
<li><code>start</code>, <code>end</code> - <code>number</code>: Posición inicial y final respectivamente, los índices comienzan en cero y end es exclusivo. No se pueden usar índices negativos.</li>
</ul>
</li>
</ul>
<br>
<ul>
<li><code>string.charAt(indice)</code> - <code>string</code>: Retorna el carácter en la posición indicada.
<ul>
<li><code>indice</code> - <code>number</code>: Índice del carácter, comienza en cero.</li>
</ul>
</li>
</ul>
<br>
<ul>
<li><code>string.charCodeAt(indice)</code> - <code>string</code>: Retorna el código UTF-16 del carácter en la posición indicada.
<ul>
<li><code>indice</code> - <code>number</code>: Índice del carácter, comienza en cero.</li>
</ul>
</li>
</ul>
<br>
<h5 id="buscar-y-reemplazar">Buscar y reemplazar:</h5>
<ul>
<li><code>string.replace(regexp|substr, newSubStr|function, flags)</code> - <code>string</code>: Devuelve una cadena reemplazando todas o algunas coincidencias de un patrón. No modifica la cadena sobre la cual se llamó al método, sino que retorna una nueva cadena.
<ul>
<li><code>regexp|substr</code> - <code>RegExp</code> o <code>string</code>: Patrón a reemplazar.</li>
<li><code>newSubStr|function</code> - <code>string</code> o <code>Function</code>: Cadena que reemplazará al patrón o una función para crear la nueva cadena.</li>
<li><code>flags</code> - <code>string</code>: Combinación de flags para modificar el comportamiento del método, algunas opciones son:
<ul>
<li><code>g</code>: Para que reemplace todos los patrones encontrados.</li>
<li><code>i</code>: Para ignorar mayúsculas.</li>
</ul>
</li>
</ul>
</li>
</ul>
<br>
<ul>
<li><code>string.search(regexp)</code> - <code>number</code>: Retorna la posición de la primera coincidencia de un patrón, si no se encuentra retorna -1.
<ul>
<li><code>regexp</code> - <code>RegExp</code>: Regular expression a buscar.</li>
</ul>
</li>
</ul>
<br>
<ul>
<li><code>string.match(regexp)</code> - <code>object</code>: Retorna todas las coincidencias con un patrón en una cadena.
<ul>
<li><code>regexp</code> - <code>RegExp</code>: Regular expression a buscar.</li>
<li>El objeto retornado tiene como propiedades:
<ul>
<li><code>Input</code>: Cadena donde se está buscando.</li>
<li><code>Index</code>: índice donde se encontró la coincidencia.</li>
<li><code>0</code>: Coincidencia encontrada.</li>
<li><code>1, 2, ...</code>: Grupos capturados.</li>
</ul>
</li>
</ul>
</li>
</ul>
<br>
<ul>
<li><code>position=0]) [string.indexOf(searchString, [position=0])</code> - <code>number</code>: Retorna la posición de la primera coincidencia de un patrón, si no se encuentra retorna -1.
<ul>
<li><code>searchString</code> - <code>string</code>: Cadena a buscar.</li>
<li><code>position</code> - <code>number</code>: Posición inicial desde donde buscar.</li>
</ul>
</li>
</ul>
<br>
<ul>
<li><code>string.lastIndexOf(searchString, position=0)</code> - <code>number</code>: Retorna la posición de la última coincidencia de un patrón, si no se encuentra retorna -1.
<ul>
<li><code>searchString</code> - <code>string</code>: Cadena a buscar.</li>
<li><code>position</code> - <code>number</code>: Posición máxima desde donde buscar.</li>
</ul>
</li>
</ul>
<br>
<h5 id="manipulación">Manipulación:</h5>
<ul>
<li><code>string.toUpperCase()</code> - <code>string</code>: Convierte la cadena a mayúsculas.
<ul>
<li>No tiene argumentos.</li>
</ul>
</li>
</ul>
<br>
<ul>
<li><code>string.toLowerCase()</code> - <code>string</code>: Convierte la cadena a minúsculas.
<ul>
<li>No tiene argumentos.</li>
</ul>
</li>
</ul>
<br>
<h5 id="concatenación-y-splits">Concatenación y splits:</h5>
<ul>
<li><code>string.concat(str1, str2, /* ..., */ strN)</code> - <code>string</code>: Concatena dos o más cadenas y retorna una nueva. Se puede usar como alternativa del operador +.
<ul>
<li><code>(str1, ..., strN</code> - <code>string</code>: Cadenas a concatenar.</li>
</ul>
</li>
</ul>
<br>
<ul>
<li><code>string.split(separator, limit)</code> - <code>Array</code>: Retorna una cadena separada por un carácter en un array.
<ul>
<li><code>separator</code> - <code>string</code> o <code>RegExp</code>: Separador de la cadena.</li>
<li><code>limit</code> - <code>number</code>: Especifica el número máximo de <em>splits</em> a realizar.</li>
</ul>
</li>
</ul>
<br>
<h5 id="trims-y-pads">Trims y Pads:</h5>
<ul>
<li><code>string.trim()</code> - <code>string</code>: Elimina los espacios en blanco a ambos extremos de la cadena.
<ul>
<li>No tiene argumentos.</li>
</ul>
</li>
</ul>
<br>
<ul>
<li><code>string.trimStart()</code> - <code>string</code>: Elimina los espacios en blanco al inicio de la cadena.
<ul>
<li>No tiene argumentos.</li>
</ul>
</li>
</ul>
<br>
<ul>
<li><code>string.trimEnd()</code> - <code>string</code>: Elimina los espacios en blanco al final de la cadena.
<ul>
<li>No tiene argumentos.</li>
</ul>
</li>
</ul>
<br>
<ul>
<li><code>string.padStart(targetLength, padString)</code> - <code>string</code>: Agrega un patrón al inicio de una cadena para que tenga una longitud deseada. El patrón se repetirá si es necesario.
<ul>
<li><code>tagerLenght</code> - <code>number</code>: Longitud deseada.</li>
<li><code>padString</code> - <code>string</code>: Cadena a agregar al inicio de la cadena. Si es muy grande se truncará.</li>
</ul>
</li>
</ul>
<br>
<ul>
<li><code>string.padEnd(targetLength, padString)</code> - <code>string</code>: Agrega un patrón al final de una cadena para que tenga una longitud deseada. El patrón se repetirá si es necesario.
<ul>
<li><code>tagerLenght</code> - <code>number</code>: Longitud deseada.</li>
<li><code>padString</code> - <code>string</code>: Cadena a agregar al final de la cadena. Si es muy grande se truncará.</li>
</ul>
</li>
</ul>
<h3 id="boolean">boolean:</h3>
<p>Un valor booleano puede representar dos valores, <code>true</code> o <code>false</code>. Todos los valores al ser evaluados como <em>bool</em> se consideran <code>true</code> (truthy), excepto algunos cuantos, los valores que son evaluados como <code>false</code> (falsy) son:</p>
<ul>
<li>Valor <code>false</code>.</li>
<li>Número cero (<code>0</code>).</li>
<li>Cadenas vacías (<code>''</code>).</li>
<li>Valor <code>undefined</code>.</li>
<li>Valor <code>null</code>.</li>
<li>Valor <code>NaN</code>.</li>
</ul>
<blockquote>
<p><strong>Importante</strong>: arrays y objetos vacíos no se evaluan como <code>false</code>.</p>
</blockquote>
<h3 id="object">object:</h3>
<p>Es una lista de cero o más pares propiedad-valor. Se escriben entre llaves, cada elemento se declara en una par <em>property:“value”</em>. Los objetos se suelen declarar como constantes:</p>
<pre class=" language-js"><code class="prism  language-js"><span class="token comment">// Plantilla básica de un objeto</span>
<span class="token keyword">const</span> myObject <span class="token operator">=</span> <span class="token punctuation">{</span>property1<span class="token punctuation">:</span> <span class="token string">"value1"</span><span class="token punctuation">,</span> property2<span class="token punctuation">:</span> "value2<span class="token punctuation">,</span> <span class="token operator">...</span><span class="token punctuation">}</span><span class="token punctuation">;</span> 
</code></pre>
<ul>
<li><em>myObject</em> es el nombre del objeto.</li>
<li><em>propertyi</em> es el nombre de cada propiedad. Los nombres no son necesarios ponerlos como cadenas, pero también es posible hacerlo así, incluso puede ser una cadena vacía.</li>
<li><em>valuei</em>: Es el valor de cada elemento, pueden ser de diferentes tipos incluso arrays, funciones u otros objetos. Si es numérico no es necesario ponerlo entre comillas.
<ul>
<li>Si el valor es una función la propiedad será un tipo método.</li>
</ul>
</li>
</ul>
<p>Otra forma de crear un objeto es con:</p>
<pre class=" language-js"><code class="prism  language-js"><span class="token keyword">let</span> myObject <span class="token operator">=</span> <span class="token keyword">new</span> <span class="token class-name">Object</span><span class="token punctuation">(</span><span class="token punctuation">)</span> 
</code></pre>
<p>Es posible agregar nuevas propiedades y métodos de manera dinámica de la siguiente manera:</p>
<pre class=" language-js"><code class="prism  language-js">myObject<span class="token punctuation">.</span>new_property <span class="token operator">=</span> value <span class="token comment">// Solo válido con nombres no complejos ni raros </span>

myObject<span class="token punctuation">.</span><span class="token function-variable function">new_method</span> <span class="token operator">=</span> <span class="token keyword">function</span><span class="token punctuation">(</span>args<span class="token punctuation">)</span> <span class="token punctuation">{</span> expressions <span class="token punctuation">}</span> 
</code></pre>
<h4 id="acceder-a-propiedades-y-métodos">Acceder a propiedades y métodos:</h4>
<p>Para acceder a las propiedades de cada objeto usar:</p>
<pre class=" language-js"><code class="prism  language-js"><span class="token comment">// Solo válido con nombres no complejos ni raros</span>
myObject<span class="token punctuation">.</span>property<span class="token punctuation">;</span>  

 <span class="token comment">// Válido para nombres más complejos</span>
myObject<span class="token punctuation">[</span><span class="token string">"property"</span><span class="token punctuation">]</span><span class="token punctuation">;</span> 
</code></pre>
<p>Para acceder a los métodos de cada objeto usar:</p>
<pre class=" language-js"><code class="prism  language-js">objectName<span class="token punctuation">.</span><span class="token function">method</span><span class="token punctuation">(</span>args<span class="token punctuation">)</span><span class="token punctuation">;</span> 
</code></pre>
<h4 id="eliminar-propiedades-o-métodos">Eliminar propiedades o métodos:</h4>
<p>Para eliminar una propiedad o método se usa la palabra reservada <code>delete</code>:</p>
<pre class=" language-js"><code class="prism  language-js"><span class="token comment">// Eliminar una propiedad</span>
<span class="token keyword">delete</span> myObject<span class="token punctuation">.</span>property<span class="token punctuation">;</span> 

<span class="token comment">// Eliminar una propiedad</span>
<span class="token keyword">delete</span> myObject<span class="token punctuation">[</span><span class="token string">"property"</span><span class="token punctuation">]</span><span class="token punctuation">;</span> 

<span class="token comment">// Eliminar con base al índice</span>
<span class="token keyword">delete</span> myObject<span class="token punctuation">[</span>index<span class="token punctuation">]</span><span class="token punctuation">;</span> 

<span class="token comment">// Eliminar un método</span>
<span class="token keyword">delete</span> myObject<span class="token punctuation">.</span>method<span class="token punctuation">;</span> 
</code></pre>
<h4 id="verificar-membresía">Verificar membresía:</h4>
<p>Se puede usar el operador <code>in</code> para verificar que exista una propiedad en un objeto:</p>
<pre class=" language-js"><code class="prism  language-js"><span class="token comment">// Verificar membresia</span>
property <span class="token keyword">in</span> myObject
</code></pre>
<ul>
<li><em>property</em> tiene que ser <code>string</code>, <code>number</code> o <code>symbol</code>.</li>
</ul>
<p>Otra forma de verificar si un objeto tiene una propiedad específica es con el método <code>.hasOwnProperty()</code>.</p>
<pre class=" language-js"><code class="prism  language-js"><span class="token comment">// Verificar membresia</span>
myObject<span class="token punctuation">.</span><span class="token function">hasOwnProperty</span><span class="token punctuation">(</span><span class="token string">'name'</span><span class="token punctuation">)</span><span class="token punctuation">:</span> 
</code></pre>
<ul>
<li><em>myObject</em> es el nombre del objeto.</li>
<li><em>name</em> es el nombre de la propiedad que se quiere verificar si existe en <em>myObject</em>.</li>
</ul>
<h4 id="desempacar">Desempacar:</h4>
<p>Para desempacar objetos el nombre de las variables debe de ser el mismo que el nombre de las propiedades.</p>
<pre class=" language-js"><code class="prism  language-js"><span class="token keyword">let</span> <span class="token punctuation">{</span>propName1<span class="token punctuation">,</span> propName2<span class="token punctuation">,</span> <span class="token operator">...</span><span class="token punctuation">}</span> <span class="token operator">=</span> myObject 
</code></pre>
<p>Se pueden asignar valores por default a propiedades que se sabe que no existen en el objeto.</p>
<pre class=" language-js"><code class="prism  language-js"><span class="token keyword">let</span> <span class="token punctuation">{</span>propName1<span class="token punctuation">,</span> propName2<span class="token punctuation">,</span> propName3 <span class="token operator">=</span> <span class="token string">"value"</span><span class="token punctuation">,</span> <span class="token operator">...</span><span class="token punctuation">}</span> <span class="token operator">=</span> myObject 
</code></pre>
<p>Se puede renombrar las variables al momento de desempacar usando:</p>
<pre class=" language-js"><code class="prism  language-js"><span class="token keyword">let</span> <span class="token punctuation">{</span>prop1<span class="token punctuation">:</span> newName1<span class="token punctuation">,</span> prop2<span class="token punctuation">:</span> newName2<span class="token punctuation">,</span> <span class="token operator">...</span><span class="token punctuation">}</span> <span class="token operator">=</span> myObject 
</code></pre>
<p>Es posible desempacar un objeto incluso al llamar a una función:</p>
<pre class=" language-js"><code class="prism  language-js"><span class="token comment">// Definir objeto</span>
<span class="token keyword">const</span> triangulo <span class="token operator">=</span> <span class="token punctuation">{</span> 
  base<span class="token punctuation">:</span> <span class="token number">10</span><span class="token punctuation">,</span> 
  altura<span class="token punctuation">:</span> <span class="token number">20</span> 
<span class="token punctuation">}</span> 

<span class="token comment">// Definir función</span>
<span class="token keyword">const</span> <span class="token function-variable function">area</span> <span class="token operator">=</span> <span class="token punctuation">(</span><span class="token punctuation">{</span>base<span class="token punctuation">,</span> altura<span class="token punctuation">}</span><span class="token punctuation">)</span> <span class="token operator">=&gt;</span> <span class="token punctuation">{</span> 
  <span class="token keyword">return</span> <span class="token punctuation">(</span>base <span class="token operator">*</span> altura<span class="token punctuation">)</span> <span class="token operator">/</span> <span class="token number">2</span>
<span class="token punctuation">}</span>

<span class="token comment">// Utilizar la función</span>
console<span class="token punctuation">.</span><span class="token function">log</span><span class="token punctuation">(</span><span class="token function">area</span><span class="token punctuation">(</span>triangulo<span class="token punctuation">)</span><span class="token punctuation">)</span> 
</code></pre>
<ul>
<li>En este ejemplo, se puede pasar a la función un objeto que tenga las propiedades <code>base</code> y <code>altura</code>, automáticamente se desempacará.</li>
</ul>
<h4 id="copiar-objetos">Copiar objetos:</h4>
<p>Se puede usar operador <em>spread</em> (<code>...</code>) para crear una copia de un objeto.</p>
<pre class=" language-js"><code class="prism  language-js"><span class="token keyword">const</span> persona <span class="token operator">=</span> <span class="token punctuation">{</span> 
  nombre<span class="token punctuation">:</span> <span class="token string">'Juan'</span><span class="token punctuation">,</span>
  edad<span class="token punctuation">:</span> <span class="token number">25</span><span class="token punctuation">,</span> 
  nacionalidad<span class="token punctuation">:</span> <span class="token string">'Mexicano'</span>
<span class="token punctuation">}</span> 

<span class="token keyword">const</span> copiaPersona <span class="token operator">=</span> <span class="token punctuation">{</span><span class="token operator">...</span>persona<span class="token punctuation">}</span> 
</code></pre>
<ul>
<li>El valor de una propiedad se puede modificar usando: <br> <code>const copiaPersona = {...persona, property: newVal}</code></li>
</ul>
<h4 id="métodos">Métodos:</h4>
<p>Los objetos también tienen métodos, se almacenan como propiedades cuyos valores son funciones.</p>
<pre class=" language-js"><code class="prism  language-js"><span class="token comment">// Plantilla de como definir métodos en un objeto</span>
<span class="token keyword">const</span> myObject <span class="token operator">=</span> <span class="token punctuation">{</span><span class="token operator">...</span><span class="token punctuation">,</span> methodName<span class="token punctuation">:</span> <span class="token keyword">function</span> <span class="token punctuation">(</span>args<span class="token punctuation">)</span> <span class="token punctuation">{</span>expresions<span class="token punctuation">}</span><span class="token punctuation">}</span><span class="token punctuation">;</span> 
</code></pre>
<ul>
<li>Dentro de la definición de la función se puede usar <code>this.property</code> para acceder a las propiedades del objeto <code>myObject</code>.</li>
</ul>
<p>Para utilizar los métodos de un objeto usar:</p>
<pre class=" language-js"><code class="prism  language-js">objectName<span class="token punctuation">.</span><span class="token function">methodName</span><span class="token punctuation">(</span>args<span class="token punctuation">)</span> 
</code></pre>
<ul>
<li>Si no se ponen los paréntesis retornará la definición del método (el código fuente del método).</li>
</ul>
<p>Se puede utilizar métodos de otros objetos en un objeto aparte siempre y cuando tengan la misma estructura (las mismas propiedades) usando <code>.call()</code> y <code>.apply()</code>:</p>
<pre class=" language-js"><code class="prism  language-js"><span class="token comment">// Utilizar un método en otro objeto</span>
obj1<span class="token punctuation">.</span>methodName<span class="token punctuation">.</span><span class="token function">call</span><span class="token punctuation">(</span>obj2<span class="token punctuation">)</span>

<span class="token comment">// Utilizar un método con argumentos en otro objeto</span>
obj1<span class="token punctuation">.</span>method_name<span class="token punctuation">.</span><span class="token function">call</span><span class="token punctuation">(</span>obj2<span class="token punctuation">,</span> arg1<span class="token punctuation">,</span> arg2<span class="token punctuation">,</span> …<span class="token punctuation">)</span>  
</code></pre>
<ul>
<li><code>methodName</code> es un método de <em>obj1</em>, pero se utilizará en <em>obj2</em>.</li>
</ul>
<p>El método <code>apply()</code> que es muy similar a <code>call()</code>, la única diferencia es que para pasar los argumentos del método en <code>apply()</code> se debe de hacer dentro de un <code>array</code>.</p>
<pre class=" language-js"><code class="prism  language-js"><span class="token comment">// Utilizar un método en otro objeto</span>
obj1<span class="token punctuation">.</span>methodName<span class="token punctuation">.</span><span class="token function">apply</span><span class="token punctuation">(</span>obj2<span class="token punctuation">)</span> 

<span class="token comment">// Utilizar un método con argumentos en otro objeto</span>
obj1<span class="token punctuation">.</span>methodName<span class="token punctuation">.</span><span class="token function">call</span><span class="token punctuation">(</span>obj2<span class="token punctuation">,</span> myArray<span class="token punctuation">)</span>
</code></pre>
<ul>
<li><code>methodName</code> es un método de <em>obj1</em>, pero se utilizará en <em>obj2</em>.</li>
<li><em>myArray</em> es un arreglo con los argumentos de <code>methodName</code>.</li>
</ul>
<h4 id="métodos-de-object">Métodos de object</h4>
<blockquote>
<p>Falta agregar</p>
</blockquote>
<h3 id="arrays">Arrays:</h3>
<p>Es un objeto especial que permite almacenar múltiples valores en una sola variable. Se escriben entre corchetes, separando los elementos con comas.</p>
<pre class=" language-js"><code class="prism  language-js"><span class="token comment">// Plantilla básica de como declarar un array</span>
<span class="token keyword">const</span> myArray <span class="token operator">=</span> <span class="token punctuation">[</span>val1<span class="token punctuation">,</span> val2<span class="token punctuation">,</span> <span class="token operator">...</span><span class="token punctuation">]</span><span class="token punctuation">;</span> 
</code></pre>
<ul>
<li>Es común que los arrays se declaren como constantes.</li>
<li>Los elementos del array pueden ser de diferentes tipos.</li>
<li>Se pueden dejar elementos vacíos, pero es recomendable indicar que se está dejando un elemento vacío con un comentario: <br> <code>const myArray = [val1, val2, /* empty */, ...];</code></li>
</ul>
<p>Otra forma de crear un array en con</p>
<pre class=" language-js"><code class="prism  language-js">cont myArray <span class="token operator">=</span> <span class="token keyword">new</span> <span class="token class-name">Array</span><span class="token punctuation">(</span>val1<span class="token punctuation">,</span> val2<span class="token punctuation">,</span> <span class="token operator">...</span><span class="token punctuation">)</span> 
</code></pre>
<ul>
<li>Lo anterior es igual a usar los corchetes <code>[]</code>.</li>
</ul>
<p>Se puede crear un array con elementos vacíos, pero de determinada longitud, con:</p>
<pre class=" language-js"><code class="prism  language-js"><span class="token keyword">const</span> myArray <span class="token operator">=</span> <span class="token keyword">new</span> <span class="token class-name">Array</span><span class="token punctuation">(</span>num<span class="token punctuation">)</span><span class="token punctuation">;</span> 
</code></pre>
<ul>
<li><em>num</em> es un valor numérico entero.</li>
</ul>
<h4 id="seleccionar-elementos">Seleccionar elementos:</h4>
<p>Para seleccionar elementos de un array usar:</p>
<pre class=" language-js"><code class="prism  language-js"><span class="token comment">// Seleccionar elementos de un array</span>
myArray<span class="token punctuation">[</span>ind<span class="token punctuation">]</span> 
</code></pre>
<ul>
<li><em>ind</em> es el índice del elemento. La indexación comienza en cero.</li>
<li>Para acceder al último elemento se puede usar: <br> <code>myArray[myArray.lenght - 1]</code></li>
</ul>
<h4 id="agregar-y-modificar-elementos">Agregar y modificar elementos:</h4>
<p>Para agregar o modificar elementos simplemente seleccionar su índice y asignar un nuevo valor:</p>
<pre class=" language-js"><code class="prism  language-js">myArray<span class="token punctuation">[</span>ind<span class="token punctuation">]</span> <span class="token operator">=</span> new_val 
</code></pre>
<h4 id="concatenar-arrays">Concatenar arrays:</h4>
<p>Se puede usar el operador <em>spread</em> (<code>...</code>), para crear un array que sea la concatenación de varios arrays:</p>
<pre class=" language-js"><code class="prism  language-js"><span class="token comment">// Definir arrays</span>
<span class="token keyword">const</span> pares <span class="token operator">=</span> <span class="token punctuation">[</span><span class="token number">0</span><span class="token punctuation">,</span> <span class="token number">2</span><span class="token punctuation">,</span> <span class="token number">4</span><span class="token punctuation">,</span> <span class="token number">6</span><span class="token punctuation">,</span> <span class="token number">8</span><span class="token punctuation">]</span> 
 
<span class="token keyword">const</span> impares <span class="token operator">=</span> <span class="token punctuation">[</span><span class="token number">1</span><span class="token punctuation">,</span> <span class="token number">3</span><span class="token punctuation">,</span> <span class="token number">5</span><span class="token punctuation">,</span> <span class="token number">7</span><span class="token punctuation">,</span> <span class="token number">9</span><span class="token punctuation">]</span> 

<span class="token comment">// Concatenar arrays </span>
<span class="token keyword">const</span> enteros <span class="token operator">=</span> <span class="token punctuation">[</span><span class="token operator">...</span>pares<span class="token punctuation">,</span> <span class="token operator">...</span>impares<span class="token punctuation">]</span> 
</code></pre>
<h4 id="modificar-longitud">Modificar longitud:</h4>
<p>Se puede modificar la longitud de un array existente con:</p>
<pre class=" language-js"><code class="prism  language-js">myArray<span class="token punctuation">.</span>length <span class="token operator">=</span> num 
</code></pre>
<ul>
<li><em>num</em> es un valor numérico entero.</li>
<li>Si <em>num</em> es menor al número de elementos actual, entonces se truncará el array.</li>
<li>Si <em>num</em> es <code>0</code>, entonces se vaciará el array.</li>
</ul>
<h4 id="desempacar-1">Desempacar:</h4>
<p>Para desempacar un <code>array</code> en varias variables usar:</p>
<pre class=" language-js"><code class="prism  language-js">Let <span class="token punctuation">[</span>var1<span class="token punctuation">,</span> var2<span class="token punctuation">,</span> <span class="token operator">...</span><span class="token punctuation">]</span> <span class="token operator">=</span> MyArray 
</code></pre>
<ul>
<li>El número de variables debe ser igual al número de elementos en el array.</li>
<li>Los elementos pueden ser otros arrays.</li>
<li>Si el número de variables es menor que el número de elementos en el array, entonces el resto de los elementos en el array se ignorarán.</li>
<li>Se puede omitir algún elemento con una coma: <br> <code>let [var1, ,var3, ...] = MyArray</code></li>
<li>Se puede asignar algún valor por default en caso de que el array tenga <code>undefined</code> o en caso de que algún índice no esté definido: <br> <code>let [var1, var2, var3, var4 = 'anything'] = MyArray</code></li>
<li>Si se quiere asignar solo unas cuantas variables y el resto asignarlo a otro array usar: <br> <code>let [var1, var2, ...rest] = MyArray</code></li>
</ul>
<h4 id="iteración">Iteración:</h4>
<p>Se puede iterar sobre los elementos del array usando un cíclo <em>for … of</em>:</p>
<pre class=" language-js"><code class="prism  language-js"><span class="token comment">// Ejemplo de iteración de un array</span>
<span class="token keyword">const</span> numeros <span class="token operator">=</span> <span class="token punctuation">[</span><span class="token number">1</span><span class="token punctuation">,</span> <span class="token number">2</span><span class="token punctuation">,</span> <span class="token number">3</span><span class="token punctuation">,</span> <span class="token number">4</span><span class="token punctuation">,</span> <span class="token number">5</span><span class="token punctuation">]</span><span class="token punctuation">;</span>  

<span class="token keyword">for</span> <span class="token punctuation">(</span><span class="token keyword">const</span> numero <span class="token keyword">of</span> numeros<span class="token punctuation">)</span> <span class="token punctuation">{</span>  

	console<span class="token punctuation">.</span><span class="token function">log</span><span class="token punctuation">(</span>numero<span class="token punctuation">)</span><span class="token punctuation">;</span>  

<span class="token punctuation">}</span> 
</code></pre>
<blockquote>
<p>Revisar también los métodos de iteración.</p>
</blockquote>
<p>Alternativamente se puede iterar con los índices:</p>
<pre class=" language-js"><code class="prism  language-js"><span class="token keyword">const</span> numeros <span class="token operator">=</span> <span class="token punctuation">[</span><span class="token number">1</span><span class="token punctuation">,</span> <span class="token number">2</span><span class="token punctuation">,</span> <span class="token number">3</span><span class="token punctuation">,</span> <span class="token number">4</span><span class="token punctuation">,</span> <span class="token number">5</span><span class="token punctuation">]</span><span class="token punctuation">;</span>  

<span class="token keyword">for</span> <span class="token punctuation">(</span><span class="token keyword">let</span> i<span class="token operator">=</span><span class="token number">0</span><span class="token punctuation">;</span> i<span class="token operator">&lt;</span>numeros<span class="token punctuation">.</span>lenght<span class="token punctuation">;</span> i<span class="token operator">++</span><span class="token punctuation">)</span> <span class="token punctuation">{</span>  

	console<span class="token punctuation">.</span><span class="token function">log</span><span class="token punctuation">(</span>numeros<span class="token punctuation">[</span>i<span class="token punctuation">]</span><span class="token punctuation">)</span><span class="token punctuation">;</span>  

<span class="token punctuation">}</span> 
</code></pre>
<ul>
<li>Para iterar el array de manera inversa usar: <br> <code>for (let i=numeros.lenght-1; i&gt;=0; i--) {...}</code></li>
</ul>
<p>Se puede iterar sobre arrays anidados, donde cada elemento son del mismo tamaño de la siguiente manera:</p>
<pre class=" language-js"><code class="prism  language-js"><span class="token keyword">for</span> <span class="token punctuation">(</span><span class="token keyword">const</span> <span class="token punctuation">[</span>ele1<span class="token punctuation">,</span> ele2<span class="token punctuation">]</span> <span class="token keyword">of</span> myArray<span class="token punctuation">)</span> <span class="token punctuation">{</span> 
		<span class="token operator">...</span> 
	<span class="token punctuation">}</span> 
</code></pre>
<ul>
<li>En este ejemplo, cada array interno es de dos elementos.</li>
<li>Si el número de variables es menor al número de elementos en los array internos, entonces solo se tomarán el número de variables, ignorando el resto.</li>
</ul>
<h4 id="crear-copia-de-array">Crear copia de array:</h4>
<p>Se puede usar el operador <em>spread</em> (<code>...</code>), para crear una copia de un array:</p>
<pre class=" language-js"><code class="prism  language-js"><span class="token comment">// definir el array</span>
<span class="token keyword">const</span> vocales <span class="token operator">=</span> <span class="token punctuation">[</span><span class="token string">'a'</span><span class="token punctuation">,</span> <span class="token string">'e'</span><span class="token punctuation">,</span> <span class="token string">'i'</span><span class="token punctuation">,</span> <span class="token string">'o'</span><span class="token punctuation">,</span> <span class="token string">'u'</span><span class="token punctuation">]</span>

<span class="token comment">// crear copia</span>
<span class="token keyword">const</span> letras <span class="token operator">=</span> <span class="token punctuation">[</span><span class="token operator">...</span>vocales<span class="token punctuation">]</span> 
</code></pre>
<h4 id="arrays-multidimensionales">Arrays multidimensionales</h4>
<p>Se pueden crear array cuyos elementos sean otros arrays, para ello, cada elemento se debe indicar que es un array y posteriormente usar la notación [i][j] para ir llenando el array. Ejemplo para un array de dos dimensiones:</p>
<pre class=" language-js"><code class="prism  language-js"><span class="token keyword">const</span> a <span class="token operator">=</span> <span class="token keyword">new</span> <span class="token class-name">Array</span><span class="token punctuation">(</span><span class="token number">4</span><span class="token punctuation">)</span><span class="token punctuation">;</span> 
<span class="token keyword">for</span> <span class="token punctuation">(</span><span class="token keyword">let</span> i <span class="token operator">=</span> <span class="token number">0</span><span class="token punctuation">;</span> i <span class="token operator">&lt;</span> <span class="token number">4</span><span class="token punctuation">;</span> i<span class="token operator">++</span><span class="token punctuation">)</span> <span class="token punctuation">{</span> 

  <span class="token comment">// Indicar que cada elemento será un array de 4 elementos </span>
  a<span class="token punctuation">[</span>i<span class="token punctuation">]</span> <span class="token operator">=</span> <span class="token keyword">new</span> <span class="token class-name">Array</span><span class="token punctuation">(</span><span class="token number">4</span><span class="token punctuation">)</span><span class="token punctuation">;</span> 
  <span class="token keyword">for</span> <span class="token punctuation">(</span><span class="token keyword">let</span> j <span class="token operator">=</span> <span class="token number">0</span><span class="token punctuation">;</span> j <span class="token operator">&lt;</span> <span class="token number">4</span><span class="token punctuation">;</span> j<span class="token operator">++</span><span class="token punctuation">)</span> <span class="token punctuation">{</span> 

    <span class="token comment">// Ir llenando el array por "fila" y "columna". </span>
    a<span class="token punctuation">[</span>i<span class="token punctuation">]</span><span class="token punctuation">[</span>j<span class="token punctuation">]</span> <span class="token operator">=</span> <span class="token template-string"><span class="token string">`[</span><span class="token interpolation"><span class="token interpolation-punctuation punctuation">${</span>i<span class="token interpolation-punctuation punctuation">}</span></span><span class="token string">, </span><span class="token interpolation"><span class="token interpolation-punctuation punctuation">${</span>j<span class="token interpolation-punctuation punctuation">}</span></span><span class="token string">]`</span></span><span class="token punctuation">;</span> 
  <span class="token punctuation">}</span> 
<span class="token punctuation">}</span> 
</code></pre>
<h4 id="propiedades-de-instancia-de-array">Propiedades de instancia de <code>Array</code></h4>
<ul>
<li><code>Array.length</code> - <code>number</code>: Retorna la longitud del array.</li>
</ul>
<h4 id="métodos-estáticos-de-array">Métodos estáticos de <code>Array</code></h4>
<blockquote>
<p>Para una lista completa visitar la  <a href="https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Array#static_methods">documentación</a>.</p>
</blockquote>
<ul>
<li><code>Array.from(arrayLike, mapFn, thisArg)</code> - <code>Array</code>: Retorna un array desde cualquier objeto que tenga la propiedad <code>lenght</code> o un objeto iterable.
<ul>
<li><code>arrayLike</code> - <code>iterable</code> o <code>array-like</code>: Objeto el cual convertir a un array.</li>
<li><code>mapFn</code> - <code>Function</code>: Función a aplicar a cada elemento de <code>arrayLike</code>. La función debe de tomar los argumentos <code>element</code> e <code>index</code> y debe de retornar el elemento: <br> <code>function myFunction(element, index) { ... }</code></li>
<li><code>thisArg</code> - <code>any</code>: valor a usar como <code>this</code> dentro de <code>mapFn</code>.</li>
</ul>
</li>
</ul>
<br>
<ul>
<li><code>Array.isArray(value)</code> - <code>boolean</code>: Indica si un objeto x es un array o no.
<ul>
<li><code>value</code> - <code>any</code>: Valor a verificar.</li>
</ul>
</li>
</ul>
<br>
<h4 id="métodos-de-instancia-de-array">Métodos de instancia de <code>Array</code></h4>
<blockquote>
<p>Para una lista completa visitar la  <a href="https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Array#instance_methods">documentación</a>.</p>
</blockquote>
<h5 id="conversión">Conversión:</h5>
<ul>
<li><code>Array.toString()</code> - <code>string</code>: Convierte un array a una cadena, con los elementos separados por coma.
<ul>
<li>No tiene argumentos.</li>
</ul>
</li>
</ul>
<h5 id="agregar-y-eliminar-elementos">Agregar y eliminar elementos:</h5>
<ul>
<li><code>Array.push(element1, element2, /* …, */ elementN)</code> - <code>number</code>: Agrega un elemento o varios al final del array in-place. Retorna la nueva longitud del array.
<ul>
<li><code>element1, ..., elementN</code> - <code>any</code>: Elemento o elementos a agregar al final del array.</li>
</ul>
</li>
</ul>
<br>
<ul>
<li><code>Array.unshift(element1, element2, /* …, */ elementN)</code> - <code>number</code>: Agrega un elemento o varios al inicio del array, recorriendo el resto de los elementos del array in-place. Retorna la nueva longitud del array.
<ul>
<li><code>element1, ..., elementN</code> - <code>any</code>: Elemento o elementos a agregar al inicio del array.</li>
</ul>
</li>
</ul>
<br>
<ul>
<li><code>Array.pop()</code> - <code>any</code>: Elimina y retorna el último elemento del array.
<ul>
<li>No tiene argumentos.</li>
</ul>
</li>
</ul>
<br>
<ul>
<li><code>Array.shift()</code> - <code>any</code>: Elimina y retorna el primer elemento del array, recorre el resto de los elementos una posición.
<ul>
<li>No tiene argumentos.</li>
</ul>
</li>
</ul>
<br>
<ul>
<li><code>Array.splice(start, deleteCount, item1, item2, /* …, */ itemN)</code> - <code>None</code>: Reemplaza, remueve o agrega elementos nuevos al array in-place.
<ul>
<li><code>start</code> - <code>number</code>: Índice desde el cual empezar a modificar el array.</li>
<li><code>deleteCount</code> - <code>number</code>: Entero que indicar cuántos elementos eliminar desde start. Por default son todos, desde start.</li>
<li><code>item1, ..., itemN</code> - <code>any</code>: Valores a agregar desde start. Si no se especifican solo se eliminarán.</li>
</ul>
</li>
</ul>
<br>
<h5 id="buscar-elementos">Buscar elementos:</h5>
<ul>
<li><code>Array.indexOf(item, position=0)</code> - <code>number</code>: Retorna la posición de la primera coincidencia de un valor, si no se encuentra retorna -1.
<ul>
<li><code>item</code> - <code>any</code>: Valor a buscar.</li>
<li><code>position</code> - <code>number</code>: Posición inicial desde donde buscar.</li>
</ul>
</li>
</ul>
<br>
<ul>
<li><code>Array.lastIndexOf(item, position=0)</code> - <code>number</code>: Retorna la posición de la última coincidencia de un valor, si no se encuentra retorna -1.
<ul>
<li><code>item</code> - <code>any</code>: Valor a buscar.</li>
<li><code>position</code> - <code>number</code>: Posición inicial desde donde buscar.</li>
</ul>
</li>
</ul>
<br>
<ul>
<li><code>Array.includes(value)</code> - <code>boolean</code>: Indica si un elemento está en el array.
<ul>
<li><code>value</code> - <code>any</code>: Valor a buscar.</li>
</ul>
</li>
</ul>
<br>
<ul>
<li><code>Array.find(callbackFn, thisArg)</code> - <code>any</code>: Retorna el primer elemento que cumple una condición. La función debe de retornar una condición que evalue a <code>true</code> o <code>false</code>.
<ul>
<li><code>callbackFn</code> - <code>Function</code>: Función a ser ejecutada una vez por cada elemento. Esa función tiene tres argumentos value, index y array, los cuales se pueden usar dentro de la función: <br> <code>function myFunction(value, index, array) {...}</code>.</li>
<li><code>thisArg</code> - <code>any</code>: valor a usar como <code>this</code> dentro de callbackFn.</li>
<li>No es necesario declarar la función con los tres.</li>
</ul>
</li>
</ul>
<br>
<ul>
<li><code>Array.findIndex(callbackFn)</code> - <code>number</code>: Retorna el índice del primer elemento que cumple una condición.
<ul>
<li><code>callbackFn</code> - <code>Function</code>: Función a ser ejecutada una vez por cada elemento. Esa función tiene tres argumentos value, index y array, los cuales se pueden usar dentro de la función: <br> <code>function myFunction(value, index, array) {...}</code>.</li>
<li>No es necesario declarar la función con los tres.</li>
</ul>
</li>
</ul>
<br>
<h5 id="concatenar-y-splits">Concatenar y splits:</h5>
<ul>
<li><code>Array.concat(value1, value2, /* …, */ valueN)</code> - <code>Array</code>: Concatena arrays o valores.
<ul>
<li><code>value1, ..., valueN</code> - <code>any</code>: Arrays o valores a concatenar.</li>
</ul>
</li>
</ul>
<br>
<ul>
<li><code>Array.join(separator)</code> - <code>string</code>: Convierte un array a una cadena, con los elementos separados por un separador.
<ul>
<li><code>separators</code> - <code>string</code>: Separador a usar.</li>
</ul>
</li>
</ul>
<br>
<h5 id="slice">Slice:</h5>
<ul>
<li><code>Array.slice(start = 0, end)</code> - <code>Array</code>: Retorna una porción de un array indicando el principio y el final (exclusivo).
<ul>
<li><code>start</code> - <code>number</code>: índice desde el cual empezar a hacer el slice. Empieza en cero. Se pueden usar índices negativos para empezar desde un desplazamiento desde el final.</li>
<li><code>end</code> - <code>number</code>: índice en el cual terminar el slice, sin incluir este índice. Empieza en cero. Se pueden usar índices negativos para indicar un desplazamiento desde el final.</li>
</ul>
</li>
</ul>
<br>
<h5 id="ordenar">Ordenar</h5>
<ul>
<li><code>Array.sort()</code> - <code>undefined</code>: Ordena un array de texto de manera ascendente in-place.
<ul>
<li>No tiene argumentos.</li>
<li>Para ordenar arrays numéricos de manera ascendente usar: <br> <code>X.sort(function(a, b){return a - b})</code></li>
<li>Y de manera descendente: <br> <code>X.sort(function(a, b){return b - a})</code></li>
<li>Para ordenar un array numérico de manera aleatoria (shuffle) usar: <br> <code>X.sort(function(a, b){return 0.5 - Math.random()})</code></li>
</ul>
</li>
</ul>
<br>
<ul>
<li><code>Array.reverse()</code> - <code>undefined</code>: Modifica el orden del array de manera contraria in-place.
<ul>
<li>No tiene argumentos.</li>
</ul>
</li>
</ul>
<br>
<p>Para ordenar los objetos en un array:</p>
<pre class=" language-js"><code class="prism  language-js">objArr<span class="token punctuation">.</span><span class="token function">sort</span><span class="token punctuation">(</span><span class="token keyword">function</span> <span class="token punctuation">(</span>a<span class="token punctuation">,</span> b<span class="token punctuation">)</span> <span class="token punctuation">{</span>  
	<span class="token keyword">if</span> <span class="token punctuation">(</span>a<span class="token punctuation">[</span><span class="token string">'key'</span><span class="token punctuation">]</span> <span class="token operator">&lt;</span> b<span class="token punctuation">[</span><span class="token string">'key'</span><span class="token punctuation">]</span><span class="token punctuation">)</span> <span class="token keyword">return</span> <span class="token operator">-</span><span class="token number">1</span>  
	<span class="token keyword">if</span> <span class="token punctuation">(</span>a<span class="token punctuation">[</span><span class="token string">'key'</span><span class="token punctuation">]</span> <span class="token operator">&gt;</span> b<span class="token punctuation">[</span><span class="token string">'key'</span><span class="token punctuation">]</span><span class="token punctuation">)</span> <span class="token keyword">return</span> <span class="token number">1</span>  
	<span class="token keyword">return</span> <span class="token number">0</span>  
<span class="token punctuation">}</span><span class="token punctuation">)</span>
</code></pre>
<br>
<h5 id="rellenar">Rellenar:</h5>
<ul>
<li><code>Array.fill(value, start, end)</code> - <code>Array</code>: Rellena con un valor desde una posición inicial hasta una posición final.
<ul>
<li><code>value</code> - <code>any</code>: Valor con el que se rellenará el array.</li>
<li><code>start</code>, <code>end</code> - <code>number</code>: Posición inicial y final respectivamente.</li>
</ul>
</li>
</ul>
<br>
<h5 id="máximos-y-mínimos">Máximos y mínimos:</h5>
<p>No hay métodos built-in para encontrar valores extremos, pero se puede crear las siguientes funciones para encontrar tales valores:</p>
<p><strong>Máximo</strong>:</p>
<pre class=" language-js"><code class="prism  language-js"><span class="token keyword">function</span> <span class="token function">myArrayMax</span><span class="token punctuation">(</span>arr<span class="token punctuation">)</span> <span class="token punctuation">{</span>
	<span class="token keyword">return</span> Math<span class="token punctuation">.</span>max<span class="token punctuation">.</span><span class="token function">apply</span><span class="token punctuation">(</span><span class="token keyword">null</span><span class="token punctuation">,</span> arr<span class="token punctuation">)</span><span class="token punctuation">;</span>
<span class="token punctuation">}</span>
</code></pre>
<p><strong>Mínimo</strong>:</p>
<pre class=" language-js"><code class="prism  language-js"><span class="token keyword">function</span> <span class="token function">myArrayMin</span><span class="token punctuation">(</span>arr<span class="token punctuation">)</span> <span class="token punctuation">{</span>
	<span class="token keyword">return</span> Math<span class="token punctuation">.</span>min<span class="token punctuation">.</span><span class="token function">apply</span><span class="token punctuation">(</span><span class="token keyword">null</span><span class="token punctuation">,</span> arr<span class="token punctuation">)</span><span class="token punctuation">;</span>
<span class="token punctuation">}</span>
</code></pre>
<br>
<h5 id="iteración-1">Iteración:</h5>
<ul>
<li><code>Array.forEach(callbackFn)</code> - <code>undefined</code>: Llama a una función una vez por cada elemento en el array.
<ul>
<li><code>callbackFn</code> - <code>Function</code>: Función a ser ejecutada una vez por cada elemento. Esa función tiene tres argumentos <code>value</code> (elementos del array), <code>index</code> (índice del los elementos) y <code>array</code> (el array mismo), los cuales se pueden usar dentro de la función: <br> <code>function myFunction(value, index, array) {...}</code></li>
<li>No es necesario declarar la función con los tres, pero <code>value</code> sí es obligatorio.</li>
</ul>
</li>
</ul>
<br>
<ul>
<li><code>Array.keys()</code> - <code>Iterator</code>: Retorna los elementos como un objeto iterable.
<ul>
<li>No tiene argumentos.</li>
</ul>
</li>
</ul>
<br>
<ul>
<li><code>Array.entries()</code> - <code>Iterator</code>: Retorna los elementos como un objeto iterable en un formato <code>index, value</code>.
<ul>
<li>No tiene argumentos.</li>
</ul>
</li>
</ul>
<br>
<h5 id="funciones">Funciones</h5>
<ul>
<li><code>Array.map(callbackFn)</code> - <code>Array</code>: Aplica a una función a cada elemento y retorna un array nuevo.
<ul>
<li><code>callbackFn</code> - <code>Function</code>: Función a ser ejecutada una vez por cada elemento. Esa función tiene tres argumentos value (elementos del array), index (índice del aray) y array (el array mismo), los cuales se pueden usar dentro de la función: <br> <code>function callbackFn (value, index, array) {...}</code>.
<ul>
<li>No es necesario declarar la función con los tres.</li>
</ul>
</li>
</ul>
</li>
</ul>
<br>
<ul>
<li><code>Array.filter(callbackFn)</code> - <code>Array</code>: Crea un nuevo array solo con los elementos que cumplen cierta condición (evalua a true). La función debe de retornar el resultado de la condición.
<ul>
<li><code>callbackFn</code> - <code>Function</code>: Función a ser ejecutada una vez por cada elemento. Esa función tiene tres argumentos value (elementos del array), index (índice del value) y self (el array mismo), los cuales se pueden usar dentro de la función: <br> <code>function callbackFn (value, index, self) {...}</code>
<ul>
<li>No es necesario declarar la función con los tres.</li>
</ul>
</li>
</ul>
</li>
</ul>
<br>
<ul>
<li><code>Array.reduce(callbackFn, initialValue)</code> - <code>number</code>: Itera sobre cada elemento, opera sobre ellos para reducirlos a un solo número.
<ul>
<li><code>callbackFn</code> - <code>Function</code>: Función a ser ejecutada una vez por cada elemento. Esa función tiene tres argumentos accumulator, currentValue e index, los cuales se pueden usar dentro de la función: <br> <code>function callbackFn (accumulator, currentValue, index) {...}</code>
<ul>
<li>No es necesario declarar la función con los tres.</li>
</ul>
</li>
<li><code>initialValue</code> - <code>any</code>: Es el valor inicial que tendrá el accumulator en la primera iteración. Si no se específica será array<code>0</code>. No tiene que ser un número, pueden ser otros tipos como cadenas o arrays.</li>
</ul>
</li>
</ul>
<br>
<ul>
<li><code>Array.reduceRight(callbackFn)</code> - <code>number</code>: Itera sobre cada elemento, opera sobre ellos para reducirlos a un solo número, de derecha a izquierda.
<ul>
<li><code>callbackFn</code> - <code>Function</code>: Función a ser ejecutada una vez por cada elemento. Esa función tiene tres argumentos value, index y array, los cuales se pueden usar dentro de la función: <br> <code>function callbackFn (value, index, array) {...}</code>
<ul>
<li>No es necesario declarar la función con los tres.</li>
</ul>
</li>
</ul>
</li>
</ul>
<br>
<ul>
<li><code>Array.every(callbackFn)</code> - <code>string</code>: Verifica que todos los elementos cumplan una condición, iterando elemento por elemento. La función debe de retornar una condición que evalue a <code>true</code> o <code>false</code>.
<ul>
<li><code>callbackFn</code> - <code>Function</code>: Función a ser ejecutada una vez por cada elemento. Esa función tiene tres argumentos value, index y array, los cuales se pueden usar dentro de la función: <br> <code>function callbackFn (value, index, array) {...}</code>
<ul>
<li>No es necesario declarar la función con los tres.</li>
</ul>
</li>
</ul>
</li>
</ul>
<br>
<ul>
<li><code>Array.some(callbackFn)</code> - <code>string</code>: Verifica que algunos de los elementos cumplan una condición, iterando elemento por elemento. La función debe de retornar una condición que evalúe a <code>true</code> o <code>false</code>.
<ul>
<li><code>callbackFn</code> - <code>Function</code>: Función a ser ejecutada una vez por cada elemento. Esa función tiene tres argumentos value, index y array, los cuales se pueden usar dentro de la función: <br> <code>function callbackFn (value, index, array) {...}</code>
<ul>
<li>No es necesario declarar la función con los tres.</li>
</ul>
</li>
</ul>
</li>
</ul>
<br>
<h3 id="sets.">Sets.</h3>
<p>Los <em>sets</em> son una colección de valores únicos. Para crear un <code>Set</code> usar:</p>
<pre class=" language-js"><code class="prism  language-js"><span class="token keyword">const</span> mySet <span class="token operator">=</span> <span class="token keyword">new</span> <span class="token class-name">Set</span><span class="token punctuation">(</span><span class="token punctuation">[</span>val1<span class="token punctuation">,</span> val2<span class="token punctuation">,</span> <span class="token operator">...</span><span class="token punctuation">]</span><span class="token punctuation">)</span> 
</code></pre>
<ul>
<li>Se puede pasar un <code>Array</code> al constructor <code>Set()</code>. Si el array tiene valores repetidos se eliminarán.</li>
<li>Se puede crear un <code>Set</code> vacío simplemente indicando el constructor.</li>
</ul>
<h4 id="iteración-2">Iteración:</h4>
<p>Se puede iterar directamente sobre los elementos del set usando un cíclo <code>for ... of</code>:</p>
<pre class=" language-js"><code class="prism  language-js"><span class="token keyword">for</span> <span class="token punctuation">(</span><span class="token keyword">const</span> val <span class="token keyword">of</span> mySet<span class="token punctuation">)</span> <span class="token punctuation">{</span>  

	console<span class="token punctuation">.</span><span class="token function">log</span><span class="token punctuation">(</span>val<span class="token punctuation">)</span><span class="token punctuation">;</span>  

<span class="token punctuation">}</span>
</code></pre>
<ul>
<li>La iteración respeta el orden de inserción.</li>
</ul>
<h4 id="operaciones-de-sets">Operaciones de sets:</h4>
<p>Existen de manera nativa métodos para realizar operaciones entre <em>sets</em>, pero a continuación se presentan unas alternativas.</p>
<blockquote>
<p>Para una lista completa visitar la  <a href="https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Set#instance_methods">documentación</a>.</p>
</blockquote>
<h5 id="unión">Unión:</h5>
<p>Para hacer la unión de <em>sets</em>, se tiene que hacer previo a tener los <em>sets</em>, es decir, se necesitan los objetos como <em>arrays</em> y utilizar:</p>
<pre class=" language-js"><code class="prism  language-js"><span class="token comment">// Concatenar los arrays</span>
<span class="token keyword">let</span> foo <span class="token operator">=</span> <span class="token punctuation">[</span><span class="token operator">...</span>a<span class="token punctuation">,</span> <span class="token operator">...</span>b<span class="token punctuation">]</span> 

<span class="token comment">// Convertir a Set el array foo</span>
<span class="token keyword">let</span> MySet <span class="token operator">=</span> <span class="token keyword">new</span> <span class="token class-name">Set</span><span class="token punctuation">(</span>foo<span class="token punctuation">)</span> 
</code></pre>
<ul>
<li><em>a</em> y <em>b</em> son <code>Array</code> previamente declarados e inicializados.</li>
</ul>
<h5 id="intersección">Intersección:</h5>
<p>Para hacer la intersección de <em>sets</em>, se tiene que hacer previo a tener los <em>sets</em>, es decir, se necesitan los objetos como <em>arrays</em> y utilizar:</p>
<pre class=" language-js"><code class="prism  language-js"><span class="token comment">// Convertir a Set el array 'b'</span>
<span class="token keyword">let</span> bar <span class="token operator">=</span> <span class="token keyword">new</span> <span class="token class-name">Set</span><span class="token punctuation">(</span>b<span class="token punctuation">)</span> 

<span class="token comment">// Filtrar el array 'a' con base al Set 'bar'</span>
<span class="token keyword">let</span> foo <span class="token operator">=</span> a<span class="token punctuation">.</span><span class="token function">filter</span><span class="token punctuation">(</span><span class="token punctuation">(</span>val<span class="token punctuation">)</span> <span class="token operator">=&gt;</span> bar<span class="token punctuation">.</span><span class="token function">has</span><span class="token punctuation">(</span>val<span class="token punctuation">)</span><span class="token punctuation">)</span> 

<span class="token comment">// Convertir a Set el array foo</span>
<span class="token keyword">let</span> MySet <span class="token operator">=</span> <span class="token keyword">new</span> <span class="token class-name">Set</span><span class="token punctuation">(</span>foo<span class="token punctuation">)</span> 
</code></pre>
<ul>
<li><em>a</em> y <em>b</em> son <code>Array</code> previamente declarados e inicializados.</li>
</ul>
<h5 id="diferencia">Diferencia:</h5>
<p>Para hacer la diferencia de <em>sets</em>, se tiene que hacer previo a tener los <em>sets</em>, es decir, se necesitan los objetos como <em>arrays</em> y utilizar:</p>
<pre class=" language-js"><code class="prism  language-js"><span class="token comment">// Convertir a Set el array 'b'</span>
<span class="token keyword">let</span> bar <span class="token operator">=</span> <span class="token keyword">new</span> <span class="token class-name">Set</span><span class="token punctuation">(</span>b<span class="token punctuation">)</span> 

<span class="token comment">// Filtrar el array 'a' con base al Set 'bar'</span>
<span class="token keyword">let</span> foo <span class="token operator">=</span> a<span class="token punctuation">.</span><span class="token function">filter</span><span class="token punctuation">(</span><span class="token punctuation">(</span>num<span class="token punctuation">)</span> <span class="token operator">=&gt;</span> <span class="token operator">!</span>bar<span class="token punctuation">.</span><span class="token function">has</span><span class="token punctuation">(</span>num<span class="token punctuation">)</span><span class="token punctuation">)</span> 

<span class="token comment">// Convertir a Set el array foo</span>
<span class="token keyword">let</span> MySet <span class="token operator">=</span> <span class="token keyword">new</span> <span class="token class-name">Set</span><span class="token punctuation">(</span>foo<span class="token punctuation">)</span> 
</code></pre>
<ul>
<li><em>a</em> y <em>b</em> son <code>Array</code> previamente declarados e inicializados.</li>
</ul>
<h4 id="propiedades-de-instancia-de-set">Propiedades de instancia de <code>Set</code></h4>
<ul>
<li><code>Set.size</code> - <code>number</code>: Retorna la longitud del set.</li>
</ul>
<br>
<h4 id="métodos-de-instancia-de-set">Métodos de instancia de <code>Set</code></h4>
<blockquote>
<p>Para una lista completa visitar la  <a href="https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Set#instance_methods">documentación</a>.</p>
</blockquote>
<ul>
<li><code>Set.add(value)</code> - <code>Array</code>: Agrega un elemento al set.
<ul>
<li><code>value</code> - <code>any</code>: Elemento a agregar al set.</li>
</ul>
</li>
</ul>
<br>
<ul>
<li><code>Set.delete(value)</code> - <code>string</code>: Elimina un elemento específico del set, retorna un valor booleano dependiendo si el valor estaba en el set o no.
<ul>
<li><code>value</code> - <code>any</code>: Elemento a eliminar del set.</li>
</ul>
</li>
</ul>
<br>
<ul>
<li><code>Set.clear()</code> - <code>string</code>: Elimina todos los elementos de un <code>Set</code>.
<ul>
<li>No tiene argumentos.</li>
</ul>
</li>
</ul>
<br>
<ul>
<li><code>Set.has(value)</code> - <code>string</code>: Retorna un valor booleano dependiendo si el valor está en el set o no.
<ul>
<li><code>value</code> - <code>any</code>: Elemento a buscar en el set.</li>
</ul>
</li>
</ul>
<br>
<ul>
<li><code>Set.values</code> - <code>Iterator</code>: Retorna un iterator con los valores del set.
<ul>
<li>No tiene argumntos.</li>
</ul>
</li>
</ul>
<br>
<ul>
<li><code>Set.forEach(callbackFn, thisArg)</code> - <code>undefined</code>: Llama a una función una vez por cada elemento en el set.
<ul>
<li><code>callbackFn</code> - <code>Function</code>: Función a ser ejecutada una vez por cada elemento. Esa función tiene tres argumentos value, index y array, los cuales se pueden usar dentro de la función: <br> <code>function callbackFn (value, key, set) {...}</code>.
<ul>
<li>No es necesario declarar la función con los tres.</li>
</ul>
</li>
<li><code>thisArg</code> - <code>any</code>: valor a usar como <code>this</code> dentro de callbackFn.</li>
</ul>
</li>
</ul>
<br>
<h3 id="maps.">Maps.</h3>
<p>Un <em>map</em> contiene pares <em>key-value</em>, donde <em>key</em> puede ser de cualquier tipo de dato (a diferencia de <code>object</code>, que debe de ser <em>string</em> o <em>symbol</em>). Un <code>map</code> mantiene el orden como fueron insertados los elementos.</p>
<pre class=" language-js"><code class="prism  language-js"><span class="token keyword">const</span> x <span class="token operator">=</span> <span class="token keyword">new</span> <span class="token class-name">Map</span><span class="token punctuation">(</span><span class="token punctuation">)</span> 
</code></pre>
<ul>
<li>Puedes pasar un <code>Array</code> al constructor <code>Map()</code>. El <em>array</em> debe estar anidado, donde cada elemento sea otro <em>array</em> con dos elementos, el primero será la llave y el segundo será el valor.<br>
-Se puede crear un map vacío simplemente indicando el constructor.</li>
</ul>
<p>Se recomienda usar Maps sobre Objetos en los siguientes escenarios:</p>
<ul>
<li>Utilizar <code>map</code> sobre <code>object</code> cuando las llaves son desconocidas durante el tiempo de ejecución, y cuando todas las llaves son del mismo tipo y todos los valores son del mismo tipo.</li>
<li>Utilizar <code>map</code> si es necesario almacenar valores primitivos como claves, ya que el objeto trata cada clave como una cadena, ya sea un valor numérico, un valor booleano o cualquier otro valor primitivo.</li>
<li>Utilizar <code>object</code> cuando haya una lógica que opere en los elementos individuales.</li>
</ul>
<h4 id="iteración-3">Iteración</h4>
<p>Para iterar por un <code>Map</code>, se puede usar el cíclo <code>for ... of</code>:</p>
<pre class=" language-js"><code class="prism  language-js"><span class="token keyword">for</span> <span class="token punctuation">(</span><span class="token keyword">const</span> <span class="token punctuation">[</span>key<span class="token punctuation">,</span> value<span class="token punctuation">]</span> <span class="token keyword">of</span> map_name<span class="token punctuation">)</span><span class="token punctuation">{</span> 
	<span class="token comment">// code block</span>
<span class="token punctuation">}</span>	 
</code></pre>
<ul>
<li>Se itera de acuerdo al orden de inserción.</li>
</ul>
<p>También es posible iterar solo por las llaves:</p>
<pre class=" language-js"><code class="prism  language-js"><span class="token keyword">for</span> <span class="token punctuation">(</span><span class="token keyword">const</span> key <span class="token keyword">of</span> map_name<span class="token punctuation">)</span><span class="token punctuation">{</span> 
	<span class="token comment">// code block</span>
<span class="token punctuation">}</span>	 
</code></pre>
<h4 id="propiedades-de-instancia-de-map">Propiedades de instancia de <code>Map</code></h4>
<ul>
<li><code>Map.size</code> - <code>number</code>: Retorna la longitud del <em>map</em>.</li>
</ul>
<br>
<h4 id="métodos-de-estáticos-de-map">Métodos de estáticos de <code>Map</code></h4>
<blockquote>
<p>Para una lista completa visitar la  <a href="https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Map#instance_methods">documentación</a></p>
</blockquote>
<h4 id="métodos-de-instancia-de-map">Métodos de instancia de <code>Map</code></h4>
<blockquote>
<p>Para una lista completa visitar la  <a href="https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Map#static_methods">documentación</a></p>
</blockquote>
<ul>
<li><code>Map.set(key, value)</code> - <code>Map</code>: Agrega o actualiza valores en el map.
<ul>
<li><code>key</code> - <code>any</code>: Llave a agregar o actualizar.</li>
<li><code>value</code> - <code>any</code>: Valor de key.</li>
</ul>
</li>
</ul>
<br>
<ul>
<li><code>Map.get(key)</code> - <code>any</code>: Retorna el valor de una llave.
<ul>
<li><code>key</code> - <code>any</code>: Nombre de la llave.</li>
</ul>
</li>
</ul>
<br>
<ul>
<li><code>Map.delete(key)</code> - <code>Map</code>: Elimina un elemento específico del map, retorna un valor booleano dependiendo si el valor estaba en sel set o no.
<ul>
<li><code>key</code> - <code>any</code>: Elemento a eliminar del map.</li>
</ul>
</li>
</ul>
<br>
<ul>
<li><code>Set.has(key)</code> - <code>string</code>: Retorna un valor booleano dependiendo si la llave está en el map o no.
<ul>
<li><code>key</code> - <code>any</code>: Elemento a buscar en el set.</li>
</ul>
</li>
</ul>
<br>
<ul>
<li><code>Map.entries()</code> - <code>Iterator</code>: Retorna un iterator con los <code>key, value</code> del map.
<ul>
<li>No tiene argumentos.</li>
</ul>
</li>
</ul>
<br>
<ul>
<li><code>Map.forEach(callbackFn, thisArg)</code> - <code>None</code>: Llama a una función una vez por cada elemento en el map.
<ul>
<li><code>callbackFn</code> - <code>Function</code>: Función a ser ejecutada una vez por cada elemento. Esa función tiene tres argumentos value, index y array, los cuales se pueden usar dentro de la función: <br> <code>function callbackFn (value, key, set) {...}</code>.
<ul>
<li>No es necesario declarar la función con los tres.</li>
</ul>
</li>
<li><code>thisArg</code> - <code>any</code>: valor a usar como <code>this</code> dentro de callbackFn.</li>
</ul>
</li>
</ul>
<br>
<h3 id="date">Date</h3>
<p>Permite trabajar con fechas y tiempo. Para crear una fecha se suele declarar como una constante de la siguiente manera:</p>
<pre class=" language-js"><code class="prism  language-js"><span class="token keyword">const</span> x <span class="token operator">=</span> <span class="token keyword">new</span> <span class="token class-name">Date</span><span class="token punctuation">(</span><span class="token punctuation">)</span> 
</code></pre>
<ul>
<li><code>Date()</code> se puede especificar de las siguientes maneras:
<ul>
<li><code>new Date()</code>: Retorna la fecha y hora del navegador.</li>
<li><code>new Date(year, month, day)</code>: Se específica las partes individualmente, solo las partes de fecha.</li>
<li><code>new Date(year, month, day, hours, minutes, seconds, milliseconds)</code>: Se específica las partes individualmente.</li>
<li><code>new Date(milliseconds)</code>: Milisegundos desde 1/1/1970 (Unix epoch).</li>
<li><code>new Date(date-string)</code>: Cadena con una fecha. Algunos formatos de cadenas válidos son:
<ul>
<li><code>YYYY-MM-DDTHH:mm:ss.sssZ</code>: ISO, Los tiempos y zona horaria son opcionales.</li>
<li><code>MM/DD/YYYY</code> o <code>DD/MM/YYYY</code>: Dependiendo del formato local.</li>
<li><code>MMM DD YYYY</code> o <code>DD MMM YYYY</code>: En este caso los meses son nombres completos o abreviados, no sensibles a mayúsculas, no números.</li>
</ul>
</li>
</ul>
</li>
</ul>
<h4 id="métodos-estáticos-de-date">Métodos estáticos de <code>Date</code></h4>
<blockquote>
<p>Para una lista completa visitar la  <a href="https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Date#static_methods">documentación</a></p>
</blockquote>
<ul>
<li><code>Date.now()</code> - <code>number</code>: Devuelve el valor numérico correspondiente al actual número de milisegundos transcurridos desde el 1 de Enero de 1970.
<ul>
<li>No tiene argumentos.</li>
<li>La manera como se usa es: <br> <code>let date = new Date(Date.now())</code>;.</li>
</ul>
</li>
</ul>
<br>
<ul>
<li><code>Date.parse(dateString)</code> - <code>number</code>: Convierte una cadena que representa una fecha a milisegundos desde 01/01/1970.
<ul>
<li><code>dateString</code> - <code>string</code>: Cadena en ISO.</li>
</ul>
</li>
</ul>
<br>
<h4 id="métodos-de-instancia-de-date">Métodos de instancia de <code>Date</code></h4>
<blockquote>
<p>Para una lista completa visitar la  <a href="https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Date#instance_methods">documentación</a></p>
</blockquote>
<h5 id="conversión-1">Conversión:</h5>
<ul>
<li><code>Date.toString()</code> - <code>string</code>: Retorna la fecha como cadena.
<ul>
<li>No tiene argumentos.</li>
</ul>
</li>
</ul>
<br>
<ul>
<li><code>Date.toUTCString()</code> - <code>string</code>: Retorna la fecha como cadena UTC.
<ul>
<li>No tiene argumentos.</li>
</ul>
</li>
</ul>
<br>
<ul>
<li><code>Date.toDateString()</code> - <code>string</code>: Retorna la fecha como cadena con mejor formato para lectura.
<ul>
<li>No tiene argumentos.</li>
</ul>
</li>
</ul>
<br>
<ul>
<li><code>Date.toISOString()</code> - <code>string</code>: Retorna la fecha como cadena en formato ISO.
<ul>
<li>No tiene argumentos.</li>
</ul>
</li>
</ul>
<br>
<h5 id="partes-de-fechas">Partes de fechas:</h5>
<p>Los siguientes métodos retornan partes de una fecha, no tienen argumentos y todos retornan <code>number</code>. Se utilizan sobre instancias de <code>Date</code>.</p>

<table>
<thead>
<tr>
<th>Método</th>
<th>Descripción</th>
</tr>
</thead>
<tbody>
<tr>
<td><code>.getFullYear()</code></td>
<td>Recupera el año como un número de cuatro dígitos (<em>yyyy</em>)</td>
</tr>
<tr>
<td><code>.getMonth()</code></td>
<td>Recupera el mes como un número (0-11)</td>
</tr>
<tr>
<td><code>.getDate()</code></td>
<td>Recupera el día como un número (1-31)</td>
</tr>
<tr>
<td><code>.getHours()</code></td>
<td>Recupera la hora (0-23)</td>
</tr>
<tr>
<td><code>.getMinutes()</code></td>
<td>Recupera el minuto (0-59)</td>
</tr>
<tr>
<td><code>.getSeconds()</code></td>
<td>Recupera el segundo (0-59)</td>
</tr>
<tr>
<td><code>.getMilliseconds()</code></td>
<td>Recupera el milisegundo (0-999)</td>
</tr>
<tr>
<td><code>.getTime()</code></td>
<td>Recupera el <em>unix epoch</em> (milisegundos desde el 1 de enero de 1970)</td>
</tr>
<tr>
<td><code>.getDay()</code></td>
<td>Recupera el día de la semana como un número (0-6)</td>
</tr>
</tbody>
</table><p>Los siguientes métodos se usan para trabajar con fechar UTC:</p>

<table>
<thead>
<tr>
<th>Método</th>
<th>Descripción</th>
</tr>
</thead>
<tbody>
<tr>
<td><code>getUTCDate()</code></td>
<td>Igual que <code>getDate()</code>, pero devuelve la fecha UTC.</td>
</tr>
<tr>
<td><code>getUTCDay()</code></td>
<td>Igual que <code>getDay()</code>, pero devuelve el día UTC.</td>
</tr>
<tr>
<td><code>getUTCFullYear()</code></td>
<td>Igual que <code>getFullYear()</code>, pero devuelve el año UTC.</td>
</tr>
<tr>
<td><code>getUTCHours()</code></td>
<td>Igual que <code>getHours()</code>, pero devuelve la hora UTC.</td>
</tr>
<tr>
<td><code>getUTCMilliseconds()</code></td>
<td>Igual que <code>getMilliseconds()</code>, pero devuelve los milisegundos UTC.</td>
</tr>
<tr>
<td><code>getUTCMinutes()</code></td>
<td>Igual que <code>getMinutes()</code>, pero devuelve los minutos UTC.</td>
</tr>
<tr>
<td><code>getUTCMonth()</code></td>
<td>Igual que <code>getMonth()</code>, pero devuelve el mes UTC.</td>
</tr>
<tr>
<td><code>getUTCSeconds()</code></td>
<td>Igual que <code>getSeconds()</code>, pero devuelve los segundos UTC.</td>
</tr>
</tbody>
</table><h5 id="establecer-partes-de-fechas">Establecer partes de fechas:</h5>
<p>Los siguientes métodos sirven para establecer una parte de una fecha ya existente, todos reciben como argumento <code>number</code> y son <em>in-place</em>, por lo que retornan <code>undefined</code>:</p>

<table>
<thead>
<tr>
<th>Método</th>
<th>Descripción</th>
</tr>
</thead>
<tbody>
<tr>
<td><code>setDate()</code></td>
<td>Establece el día como un número (1-31)</td>
</tr>
<tr>
<td><code>setFullYear()</code></td>
<td>Establece el año (opcionalmente mes y día)</td>
</tr>
<tr>
<td><code>setHours()</code></td>
<td>Establece la hora (0-23)</td>
</tr>
<tr>
<td><code>setMilliseconds()</code></td>
<td>Establece los milisegundos (0-999)</td>
</tr>
<tr>
<td><code>setMinutes()</code></td>
<td>Establece los minutos (0-59)</td>
</tr>
<tr>
<td><code>setMonth()</code></td>
<td>Establece el mes (0-11)</td>
</tr>
<tr>
<td><code>setSeconds()</code></td>
<td>Establece de los segundos (0-59)</td>
</tr>
<tr>
<td><code>setTime()</code></td>
<td>Establece la hora (milisegundos desde el 1 de enero de 1970)</td>
</tr>
</tbody>
</table><h3 id="math">Math</h3>
<p>Este objeto permite realizar operaciones matemáticas en números (<code>number</code>).</p>
<h4 id="propiedades-estáticas-de-math">Propiedades estáticas de <code>Math</code>:</h4>
<blockquote>
<p>Para una lista completa visitar la  <a href="https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Math#static_properties">documentación</a></p>
</blockquote>

<table>
<thead>
<tr>
<th>Propiedad</th>
<th>Descripción</th>
</tr>
</thead>
<tbody>
<tr>
<td><code>Math.E</code></td>
<td>Devuelve el número de Euler</td>
</tr>
<tr>
<td><code>Math.PI</code></td>
<td>Devuelve el número Pi</td>
</tr>
<tr>
<td><code>Math.SQRT2</code></td>
<td>Devuelve la raíz cuadrada de 2</td>
</tr>
<tr>
<td><code>Math.SQRT1_2</code></td>
<td>Devuelve la raíz cuadrada de 1</td>
</tr>
<tr>
<td><code>Math.LN2</code></td>
<td>Devuelve el logaritmo natural de 2</td>
</tr>
<tr>
<td><code>Math.LN10</code></td>
<td>Devuelve el logaritmo natural de 10</td>
</tr>
<tr>
<td><code>Math.LOG2E</code></td>
<td>Devuelve el logaritmo base 2 de E</td>
</tr>
<tr>
<td><code>Math.LOG10E</code></td>
<td>Devuelve el logaritmo base 10 de E</td>
</tr>
</tbody>
</table><h4 id="métodos-estáticos-de-math">Métodos estáticos de <code>Math</code></h4>
<blockquote>
<p>Para una lista completa visitar la  <a href="https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Math#static_methods">documentación</a></p>
</blockquote>
<h5 id="redondeo">Redondeo:</h5>
<p>Todos los métodos reciben <code>number</code> como argumento y retornan <code>number</code>.</p>

<table>
<thead>
<tr>
<th>Método</th>
<th>Descripción</th>
</tr>
</thead>
<tbody>
<tr>
<td><code>Math.round(x)</code></td>
<td>Devuelve un número redondeado a su entero más cercano.</td>
</tr>
<tr>
<td><code>Math.ceil(x)</code></td>
<td>Devuelve un número redondeado hacia arriba a su entero más cercano.</td>
</tr>
<tr>
<td><code>Math.floor(x)</code></td>
<td>Devuelveun número redondeado hacia abajo a su entero más cercano.</td>
</tr>
<tr>
<td><code>Math.trunc(x)</code></td>
<td>Devuelve la parte entera de <code>x</code> (nuevo en ES6).</td>
</tr>
</tbody>
</table><br>
<h5 id="misceláneos">Misceláneos:</h5>
<p>Todos los métodos reciben <code>number</code> como argumento y retornan <code>number</code>.</p>

<table>
<thead>
<tr>
<th>Método</th>
<th>Descripción</th>
</tr>
</thead>
<tbody>
<tr>
<td><code>Math.power(x,y)</code></td>
<td>Retorna <code>x</code> elevado a la <code>y</code>.</td>
</tr>
<tr>
<td><code>Math.sqrt(x)</code></td>
<td>Retorna la raíz cuadrada de <code>x</code>.</td>
</tr>
<tr>
<td><code>Math.cbrt(x)</code></td>
<td>Retorna la raíz cúbica de <code>x</code>.</td>
</tr>
<tr>
<td><code>Math.abs(x)</code></td>
<td>Retorna el valor absoluto de <code>x</code>.</td>
</tr>
<tr>
<td><code>Math.sign(x)</code></td>
<td>Retorna el signo de <code>x</code>, como -1, 0 o 1.</td>
</tr>
</tbody>
</table><br>
<h5 id="logaritmo-y-exponenciales">Logaritmo y exponenciales:</h5>
<p>Todos los métodos reciben <code>number</code> como argumento y retornan <code>number</code>.</p>

<table>
<thead>
<tr>
<th>Método</th>
<th>Descripción</th>
</tr>
</thead>
<tbody>
<tr>
<td><code>Math.log(x)</code></td>
<td>Retorna el logaritmo natural de <code>x</code>.</td>
</tr>
<tr>
<td><code>Math.log(x)</code></td>
<td>Retorna el logaritmo base 2 de <code>x</code>.</td>
</tr>
<tr>
<td><code>Math.log(x)</code></td>
<td>Retorna el logaritmo base 10 de <code>x</code>.</td>
</tr>
<tr>
<td><code>Math.exp(x)</code></td>
<td>Retorna e elevado a <code>x</code>, donde <code>x</code> es el argumento, y e es el número de Euler.</td>
</tr>
<tr>
<td><code>Math.expm1(x)</code></td>
<td>Retorna <code>exp(x)-1</code>.</td>
</tr>
</tbody>
</table><br>
<h5 id="mínimos-y-máximos">Mínimos y máximos:</h5>
<p>Todos los métodos reciben <code>number</code> como argumento y retornan <code>number</code>.</p>

<table>
<thead>
<tr>
<th>Método</th>
<th>Descripción</th>
</tr>
</thead>
<tbody>
<tr>
<td><code>Math.min(value1, value2, /* …, */ valueN)</code></td>
<td>Retorna el valor mínimo de una serie de valores.</td>
</tr>
<tr>
<td><code>Math.max(value1, value2, /* …, */ valueN)</code></td>
<td>Retorna el valor máximo de una serie de valores.</td>
</tr>
</tbody>
</table><br>
<h5 id="números-aleatorios">Números aleatorios:</h5>
<p>Todos los métodos reciben <code>number</code> como argumento y retornan <code>number</code>.</p>

<table>
<thead>
<tr>
<th>Método</th>
<th>Descripción</th>
</tr>
</thead>
<tbody>
<tr>
<td><code>Math.random()</code></td>
<td>Retorna un número entre 0 y 1 (sin incluir el 1).</td>
</tr>
</tbody>
</table><p>Para retornar enteros aleatorios usar:</p>
<pre class=" language-js"><code class="prism  language-js"><span class="token comment">// Retorna aleatorios entre 0 y N-1-</span>
Math<span class="token punctuation">.</span><span class="token function">floor</span><span class="token punctuation">(</span>Math<span class="token punctuation">.</span><span class="token function">random</span><span class="token punctuation">(</span><span class="token punctuation">)</span> <span class="token operator">*</span> N<span class="token punctuation">)</span><span class="token punctuation">;</span> 
</code></pre>
<p>Para enteros entre dos números usar (incluye ambos extremos):</p>
<pre class=" language-js"><code class="prism  language-js"><span class="token keyword">function</span> <span class="token function">getRndInteger</span><span class="token punctuation">(</span>min<span class="token punctuation">,</span> max<span class="token punctuation">)</span> <span class="token punctuation">{</span>
	<span class="token keyword">return</span> Math<span class="token punctuation">.</span><span class="token function">floor</span><span class="token punctuation">(</span>Math<span class="token punctuation">.</span><span class="token function">random</span><span class="token punctuation">(</span><span class="token punctuation">)</span> <span class="token operator">*</span> <span class="token punctuation">(</span>max <span class="token operator">-</span> min<span class="token punctuation">)</span> <span class="token punctuation">)</span> <span class="token operator">+</span> min<span class="token punctuation">;</span>
<span class="token punctuation">}</span>
</code></pre>
<br>
<h5 id="trigonométricas">Trigonométricas:</h5>
<p>Todos los métodos reciben <code>number</code> como argumento y retornan <code>number</code>.</p>

<table>
<thead>
<tr>
<th>Método</th>
<th>Descripción</th>
</tr>
</thead>
<tbody>
<tr>
<td><code>Math.sin(x)</code></td>
<td>Retorna el seno de <code>x</code>.</td>
</tr>
<tr>
<td><code>Math.cos(x)</code></td>
<td>Retorna el coseno de <code>x</code>.</td>
</tr>
<tr>
<td><code>Math.tan(x)</code></td>
<td>Retorna la tangente de <code>x</code>.</td>
</tr>
<tr>
<td><code>Math.asin(x)</code></td>
<td>Retorna el seno inverso de <code>x</code>.</td>
</tr>
<tr>
<td><code>Math.acos(x)</code></td>
<td>Retorna el coseno inverso de <code>x</code>.</td>
</tr>
<tr>
<td><code>Math.atan(x)</code></td>
<td>Retorna la tangente inversa de <code>x</code>.</td>
</tr>
</tbody>
</table><br>
<h5 id="trigonométricas-1">Trigonométricas:</h5>
<p>Todos los métodos reciben <code>number</code> como argumento y retornan <code>number</code>.</p>

<table>
<thead>
<tr>
<th>Método</th>
<th>Descripción</th>
</tr>
</thead>
<tbody>
<tr>
<td><code>Math.sinh(x)</code></td>
<td>Retorna el seno hiperbólico de <code>x</code>.</td>
</tr>
<tr>
<td><code>Math.cosh(x)</code></td>
<td>Retorna el coseno hiperbólico de <code>x</code>.</td>
</tr>
<tr>
<td><code>Math.tanh(x)</code></td>
<td>Retorna la tangente hiperbólica de <code>x</code>.</td>
</tr>
<tr>
<td><code>Math.asinh(x)</code></td>
<td>Retorna el seno hiperbólico inverso de <code>x</code>.</td>
</tr>
<tr>
<td><code>Math.acosh(x)</code></td>
<td>Retorna el coseno hiperbólico inverso de <code>x</code>.</td>
</tr>
<tr>
<td><code>Math.atanh(x)</code></td>
<td>Retorna la tangente hiperbólica inversa de <code>x</code>.</td>
</tr>
</tbody>
</table><h3 id="json">JSON</h3>
<p>JSON es un formato de texto basado en la sintaxis de los objetos de JavaScript, utilizado para almacenar y transportar datos. Se considera un tipo de dato semiestructurado. Las llaves de los objetos JSON deben de ir entre comillas</p>
<p>Debido a la similitud entre JSON y los objetos de JS, se pueden convertir uno al otro.</p>
<h4 id="json-a-object">JSON a object</h4>
<ul>
<li><code>JSON.parse(json, reviver)</code> - <code>object</code>: Convierte una cadena que represente un JSON a un objeto .
<ul>
<li><code>json</code> - <code>string</code>: Cadena a convertir a objeto.</li>
<li><code>reviver</code> - <code>function</code>: Una función para transformar los valores antes de construir el objeto. La función recibe dos argumentos <em>key</em> y <em>value</em>. La función funciona iterativamente por cada valor <em>key-value</em>, y lo que debe de retornar es el nuevo valor que tendrá el <em>key</em>.</li>
</ul>
</li>
</ul>
<br>
<h4 id="object-a-json">object a JSON</h4>
<ul>
<li><code>JSON.stringify(obj, replacer, space)</code> - <code>string</code>: Convierte un objeto a una cadena JSON.
<ul>
<li><code>obj</code> - <code>object</code>: Objeto a convertir a cadena.</li>
<li><code>replacer</code> - <code>Function</code> o <code>Array</code>: Modifica el output:.
<ul>
<li><code>Array</code>: Si es un array debe de incluir los nombres de las propiedades que el output debe de tener. Los elementos en el array deben de ser cadenas o números.</li>
<li><code>Función</code>: Una función para transformar los valores antes de construir el objeto. La función recibe dos argumentos <em>key</em> y <em>value</em>. La función funciona iterativamente por cada valor <em>key-value</em>, y lo que debe de retornar es el nuevo valor que tendrá el <em>key</em>.</li>
</ul>
</li>
<li><code>space</code> - <code>number</code> o <code>string</code>: Espacios a añadir para hacer leíble el JSON.
<ul>
<li><code>number</code>: Número de espacios a usar como identación.</li>
<li><code>string</code>: Cualquier carácter a usar para añadir espacios en blancos como ‘/t’, ‘/n’, ’ ', etc. O cualquier carácter.</li>
</ul>
</li>
</ul>
</li>
</ul>
<br>
<h2 id="variables.">Variables.</h2>
<p>Existen dos tipos de valores en JavaScript:</p>
<ul>
<li>Variables: Valores que pueden cambiar a lo largo del programa.</li>
<li>Literales: Valores fijos, que no cambian de valor.</li>
</ul>
<p>Dependiendo del tipo de valor se utilizar diferentes <em>keywords</em> para su declaración:</p>
<ul>
<li><code>var</code>: Una variable que sea compatible con navegadores antiguos, en genral no se recomienda usar. No tiene <em>block scope</em> y pueden ser redeclaradas. No tienen que ser declaradas antes de usarlas, se recomienda como quiera declararlas al inicio del script.</li>
<li><code>let</code>: Una variable. Tienen <em>block scope</em> y no pueden ser redeclaradas (en el mismo bloque). Tienen que ser declaradas antes de usarlas.</li>
<li><code>const</code>: Una literal. Tienen <em>block scope</em> y no pueden ser redefinidas ni redeclaradas (en el mismo block). Se les debe de asignar un valor al ser declaradas, no posteriormente. Tienen que se declaradas antes de usarlas. Si es un array los elementos del array sí se pueden modificar, pero el array mismo no se puede redeclarar.</li>
</ul>
<h3 id="declaración-de-variables">Declaración de variables:</h3>
<p>Las variables son contenedores de datos, hay diferentes formas de declarar una variable, se puede inicializar la variable desde que se declara o posteriormente (solo con <code>var</code> y <code>let</code>).</p>
<pre class=" language-js"><code class="prism  language-js"><span class="token comment">// Declarar e inicializar </span>
<span class="token keyword">var</span> x <span class="token operator">=</span> val 
<span class="token keyword">let</span> x <span class="token operator">=</span> val 
<span class="token keyword">const</span> x <span class="token operator">=</span> val 

<span class="token comment">// Primero declarar, luego inicializar </span>
<span class="token keyword">var</span> x 
x <span class="token operator">=</span> val 

<span class="token comment">// Primero declarar, luego inicializar </span>
<span class="token keyword">let</span> x 
x <span class="token operator">=</span> val 
</code></pre>
<ul>
<li>Los nombres de las variables son sensibles a mayúsculas y minúsculas.</li>
<li>Los nombres de las variables deben empezar con una letra, el símbolo “$” o guión bajo ("_"), seguido por letras, números, “$” o “_”.</li>
<li>Se recomienda usar “<em>camelCase</em>” para nombrar variables.</li>
<li>No se pueden usar <em>keywords</em> como nombres.</li>
<li>Las variables no inicializadas tienen por default el valor <code>undefined</code>.</li>
</ul>
<p>Es posible declarar más de una variable en una sola línea separando por coma:</p>
<pre class=" language-js"><code class="prism  language-js"><span class="token keyword">let</span> varName1 <span class="token operator">=</span> val1<span class="token punctuation">,</span> varName2 <span class="token operator">=</span> val2<span class="token punctuation">,</span> <span class="token operator">...</span>
</code></pre>
<p>Para borrar el contenido de una variable usar:</p>
<pre class=" language-js"><code class="prism  language-js"><span class="token keyword">var</span> <span class="token operator">=</span> undefined 
</code></pre>
<h3 id="modo-estricto">Modo estricto:</h3>
<p>Es un modo para indicar que todas las variables debieron haber sido declaradas antes de usarlas, para ello usar lo siguiente al inicio del script.</p>
<pre class=" language-js"><code class="prism  language-js"><span class="token string">"use strict"</span> 
</code></pre>
<ul>
<li>Debe de ir entre comillas.</li>
<li>También se puede poner dentro de una función.</li>
</ul>
<h3 id="conversión-2">Conversión</h3>
<p>Para convertir un tipo de dato a otro se puede utilizar funciones o JavaScript lo puede hacer automáticamente.</p>
<ul>
<li><code>parseFloat(string)</code> - <code>number</code>: Convierte una cadena a un valor numérico flotante.
<ul>
<li><code>string</code> - <code>string</code>: Cadena que contenga valores numéricos.</li>
</ul>
</li>
</ul>
<br>
<ul>
<li><code>parseInt(string, radix)</code> - <code>number</code>: Convierte una cadena a un valor numérico entero. Si se pasa un número flotante lo truncará al primer entero que encuentre.
<ul>
<li><code>string</code> - <code>string</code>: Cadena que contenga valores numéricos.</li>
<li><code>Radix</code> - <code>Numero</code>: Número entre 2 y 36 que representa la base del sistema numérico a convertir.</li>
</ul>
</li>
</ul>
<br>
<p>Otra técnica es utilizar el operador <code>+</code> antes de la cadena para poder hacer operaciones entre cadenas numéricas, por ejemplo:</p>
<pre class=" language-js"><code class="prism  language-js"><span class="token comment">// Operaciones entre cadenas numéricas</span>
<span class="token operator">+</span><span class="token string">"1.1"</span> <span class="token operator">+</span> <span class="token operator">+</span><span class="token string">"1.1"</span><span class="token punctuation">;</span> <span class="token comment">// 2.2</span>
</code></pre>
<br>
<ul>
<li><code>String(x)</code> - <code>string</code>: Convierte algo a una cadena. Es el constructor de <code>string</code>, la primer letra va en mayúscula.
<ul>
<li><code>x</code> - <code>number</code>, <code>Date</code>, <code>string</code>: Valor o expresión a convertir a cadena.</li>
</ul>
</li>
</ul>
<br>
<h2 id="scopes.">Scopes.</h2>
<p>Un <em>scope</em> se refiere el ambiente en donde están disponibles las variables.</p>
<h3 id="block-scope">Block scope:</h3>
<p>Es un ambiente local que se define entre <code>{ }</code>, cualquier variable dentro del <em>block scope</em> no es accesible fuera de él:</p>
<pre class=" language-js"><code class="prism  language-js"><span class="token comment">// Ejemplo de un block scope</span>
<span class="token punctuation">{</span> 
	<span class="token comment">// block scope </span>
	<span class="token keyword">let</span> foo <span class="token operator">=</span> <span class="token string">"val"</span> 
<span class="token punctuation">}</span> 
</code></pre>
<ul>
<li>La variable <em>foo</em> solo está disponible dentro del ambiente del bloque.</li>
</ul>
<blockquote>
<p><strong>Importante</strong>: Los <em>block scopes</em> incluye a bloques como <code>if-else</code>, <code>for loops</code>, etc.</p>
</blockquote>
<blockquote>
<p><strong>Importante</strong>: Solo <code>let</code> y <code>const</code> tienen <em>block scope</em>, si se declara una variable con <code>var</code> dentro de un <em>block scope</em> si se puede acceder a su valor fuera de él.</p>
</blockquote>
<p>Es posible ponerle un nombre (<a href="#labels">label</a>) a ese bloque de código usando:</p>
<pre class=" language-js"><code class="prism  language-js"><span class="token comment">// Nombrando un block scope</span>
name<span class="token punctuation">:</span> <span class="token punctuation">{</span> 
	<span class="token comment">// block scope </span>
	expression 
<span class="token punctuation">}</span> 
</code></pre>
<h3 id="local-scope">Local scope:</h3>
<p>Es el ambiente dentro del cuerpo de las funciones. Las variables en este ambiente solo se pueden acceder dentro del mismo ambiente.</p>
<pre class=" language-js"><code class="prism  language-js"><span class="token comment">// Ejemplo de un block scope</span>
<span class="token keyword">function</span> <span class="token function">myFuction</span><span class="token punctuation">(</span><span class="token punctuation">)</span><span class="token punctuation">{</span>
	<span class="token keyword">let</span> foo <span class="token operator">=</span> <span class="token string">"val"</span>
<span class="token punctuation">}</span>
</code></pre>
<ul>
<li>La variable <em>foo</em> solo está disponible dentro del cuerpo de la función.</li>
</ul>
<h3 id="global-scope">Global scope:</h3>
<p>Es el ambiente definido de manera general, afuera de cualquier función. Las variables globales son accesibles desde cualquier parte del script.</p>
<h2 id="estructuras-de-control">Estructuras de control</h2>
<h3 id="if-else">If-else</h3>
<p>Las sentencias condicionales se utilizan para realizar diferentes acciones dependiendo  de que se satisfagan determinadas condiciones.</p>
<pre class=" language-js"><code class="prism  language-js"><span class="token comment">// Plantilla básica de un bloque if-else if-else</span>
<span class="token keyword">if</span> <span class="token punctuation">(</span>condition<span class="token punctuation">)</span><span class="token punctuation">{</span> 

	<span class="token comment">// code block </span>

<span class="token punctuation">}</span> <span class="token keyword">else</span> <span class="token keyword">if</span> <span class="token punctuation">(</span>condition<span class="token punctuation">)</span><span class="token punctuation">{</span> 

	<span class="token comment">// code block </span>

<span class="token punctuation">}</span> <span class="token keyword">else</span> <span class="token punctuation">{</span> 

	<span class="token comment">// code block </span>
<span class="token punctuation">}</span> 
</code></pre>
<ul>
<li><em>condition</em> son expresiones que resulten en un valor <code>boolean</code>. En JavaScript cualquier expresión automáticamente se evalua como <code>false</code> o <code>true</code>.  Revisar <a href="#boolean">Boolean</a>.</li>
</ul>
<p>Recordar que se puede usar el operador ternario <code>?</code> para hacer un <em>if-else</em> sencillo:</p>
<pre class=" language-js"><code class="prism  language-js">condition <span class="token operator">?</span> value_true<span class="token punctuation">:</span>value_false 
</code></pre>
<ul>
<li>No es necesario escribir todo en una sola línea.</li>
</ul>
<h3 id="switch">Switch:</h3>
<p>Permite anidar varias sentencias <em>if-else</em>:</p>
<pre class=" language-js"><code class="prism  language-js"><span class="token comment">// Plantilla básica de switch</span>
<span class="token keyword">switch</span><span class="token punctuation">(</span>expression<span class="token punctuation">)</span> <span class="token punctuation">{</span> 

	<span class="token keyword">case</span> a<span class="token punctuation">:</span> 
	<span class="token comment">// code block </span>
	<span class="token keyword">break</span><span class="token punctuation">;</span> 

	<span class="token keyword">case</span> b<span class="token punctuation">:</span> 
	<span class="token comment">// code block </span>
	<span class="token keyword">break</span><span class="token punctuation">;</span> 
	
	<span class="token operator">...</span>

	<span class="token keyword">default</span><span class="token punctuation">:</span> 
	<span class="token comment">// code block </span>

<span class="token punctuation">}</span> 
</code></pre>
<ul>
<li>Se evalua <em>expression</em>. Dependiendo del valor que haya tomado <em>expression</em> se ejecuta el caso asociado.</li>
<li>Si no hay ninguna coincidencia se ejecuta el caso <code>default</code>. Este bloque es opcional.</li>
</ul>
<blockquote>
<p><strong>Importante</strong>: Si no se pone la sentencia break, seguirá ejecutandose los siguientes casos.</p>
</blockquote>
<p>Si se requiere que dos o más casos compartan un bloque de código utilizar:</p>
<pre class=" language-js"><code class="prism  language-js"><span class="token keyword">switch</span><span class="token punctuation">(</span>expression<span class="token punctuation">)</span> <span class="token punctuation">{</span> 

	<span class="token keyword">case</span> a<span class="token punctuation">:</span>
	<span class="token keyword">case</span> b<span class="token punctuation">:</span> 
	<span class="token comment">// code block </span>
	<span class="token keyword">break</span><span class="token punctuation">;</span> 

	<span class="token keyword">case</span> c<span class="token punctuation">:</span> 
	<span class="token comment">// code block </span>
	<span class="token keyword">break</span><span class="token punctuation">;</span> 
	
	<span class="token operator">...</span>

	<span class="token keyword">default</span><span class="token punctuation">:</span> 
	<span class="token comment">// code block </span>

<span class="token punctuation">}</span>
</code></pre>
<ul>
<li>En este ejemplo <em>a</em> y <em>b</em> comparten el mismo bloque de código.</li>
</ul>
<p>Si se quiere usar comparaciones en los casos, entonces dentro de swith se debe usar <code>true</code> y poner las comparaciones en cada caso:</p>
<pre class=" language-js"><code class="prism  language-js"><span class="token keyword">switch</span><span class="token punctuation">(</span><span class="token boolean">true</span><span class="token punctuation">)</span> <span class="token punctuation">{</span> 

	<span class="token keyword">case</span> comparisson1<span class="token punctuation">:</span> 
	<span class="token comment">// code block </span>
	<span class="token keyword">break</span><span class="token punctuation">;</span> 

	<span class="token keyword">case</span> comparisson2<span class="token punctuation">:</span> 
	<span class="token comment">// code block </span>
	<span class="token keyword">break</span><span class="token punctuation">;</span> 

	<span class="token keyword">default</span><span class="token punctuation">:</span> 
	<span class="token comment">// code block </span>
<span class="token punctuation">}</span> 
</code></pre>
<ul>
<li><em>comparissoni</em> son expresiones que evaluadas resultan en valores booleanos.</li>
</ul>
<h3 id="for-loop.">For loop.</h3>
<p>Permite ejecutar un bloque de código cierta cantidad de veces</p>
<pre class=" language-js"><code class="prism  language-js"><span class="token comment">// Plantilla básica de un ciclo for</span>
<span class="token keyword">for</span> <span class="token punctuation">(</span>begin<span class="token punctuation">;</span>condition<span class="token punctuation">;</span>step<span class="token punctuation">)</span> <span class="token punctuation">{</span> 
	<span class="token comment">// code block </span>
<span class="token punctuation">}</span>
</code></pre>
<ul>
<li><em>begin</em> establece el valor inicial del iterador, por ejemplo: <code>let i=0</code>. Es posible declarar más de un valor, separándolos por coma. Se pueden declarar e inicializar afuera del <em>for loop</em>.</li>
<li><em>condition</em> establece una condición de hasta cuando iterar, por ejemplo: <code>i&lt;10</code>.</li>
<li><em>step</em> establece cómo incrementar el iterador, para ello se utilizan valores como <code>i++</code>, <code>i--</code>, <code>i+=2</code>, etc. Es posible llevar control del iterador dentro del código.</li>
</ul>
<h4 id="iterar-un-objeto">Iterar un objeto</h4>
<p>Otra forma de definir un <em>for loop</em> es para que itere sobre las propiedades de un objeto.</p>
<pre class=" language-js"><code class="prism  language-js"><span class="token keyword">for</span> <span class="token punctuation">(</span><span class="token keyword">let</span> value <span class="token keyword">in</span> object<span class="token punctuation">)</span><span class="token punctuation">{</span> 
	<span class="token comment">// code block </span>
<span class="token punctuation">}</span> 
</code></pre>
<ul>
<li><em>value</em> se tiene que declarar con <code>let</code> o <code>const</code>.</li>
<li>Si <em>object</em> es <code>object</code> iterará sobre los <em>keys</em>.</li>
<li>Si <em>object</em> es <code>array</code> iterará sobre cada valor. <br> <strong>Importante</strong>: La iteración sobre arrays no sigue el mismo orden que el orden del array, por lo que si el orden importa podría haber resultados indeseados. Es preferible usar el método de iteración del array o usar un for of loop.</li>
</ul>
<h4 id="iterar-un-iterable">Iterar un iterable</h4>
<p>Otra forma de definir un for loop es para iterar sobre los valores de un iterable:</p>
<pre class=" language-js"><code class="prism  language-js"><span class="token keyword">for</span> <span class="token punctuation">(</span><span class="token keyword">let</span> variable <span class="token keyword">of</span> iterable<span class="token punctuation">)</span><span class="token punctuation">{</span> 
	<span class="token comment">// code block </span>
<span class="token punctuation">}</span> 
</code></pre>
<ul>
<li><em>value</em> se tiene que declarar con <code>let</code> o <code>const</code>.</li>
<li><em>iterable</em> es un objeto iterable, revisar <a href="#clasificaci%C3%B3n-de-tipos-de-datos">clasificación de tipos de datos</a>.</li>
<li>Si <em>iterable</em> es un array anidado, entonces se puede desempacar con una estructura similar a: <br> <code>for (const [val1, val2, ...] of iterable)</code>.</li>
</ul>
<h4 id="sentencias">Sentencias:</h4>
<p>Para cualquier tipo de <em>for loop</em> existen dos sentencias para modificar el comportamiento del ciclo:</p>
<ul>
<li><code>break</code>: Detiene la ejecución del ciclo.</li>
<li><code>continue</code>: Detiene la ejecución de una iteración y pasa a la siguiente.</li>
</ul>
<h3 id="while-loop.">While loop.</h3>
<p>Permite ejecutar un bloque de código de manera iterativa mientras una condición sea verdadera:</p>
<pre class=" language-js"><code class="prism  language-js"><span class="token comment">// Plantilla básica de un ciclo while</span>
<span class="token keyword">while</span> <span class="token punctuation">(</span>condition<span class="token punctuation">)</span> <span class="token punctuation">{</span> 

	<span class="token comment">// code block </span>

<span class="token punctuation">}</span> 
</code></pre>
<ul>
<li><em>condition</em> es cualquier expresión que resulte en un valor <code>boolean</code>.</li>
<li>Si <em>condition</em> depende de una variable ese valor se debe de actualizar dentro del bloque de código.</li>
<li>El bloque de código se ejecutará cero o más veces, dependiendo de si se cumple la condición.</li>
</ul>
<p>Si se requiere que el código se ejecute al menos una vez usar:</p>
<pre class=" language-js"><code class="prism  language-js"><span class="token keyword">do</span> <span class="token punctuation">{</span> 

	<span class="token comment">// code block </span>

<span class="token punctuation">}</span> 
<span class="token keyword">while</span> <span class="token punctuation">(</span>condition<span class="token punctuation">)</span> 
</code></pre>
<ul>
<li><em>condition</em> es cualquier expresión que resulte en un valor <code>boolean</code>.</li>
<li>Si <em>condition</em> depende de una variable ese valor se debe de actualizar dentro del bloque de código.</li>
<li>El bloque de código se ejecutará cero o más veces, dependiendo de si se cumple la condición.</li>
</ul>
<h4 id="sentencias-1">Sentencias:</h4>
<p>Para cualquier tipo de ciclo <em>while</em> existen dos sentencias para modificar el comportamiento del ciclo:</p>
<ul>
<li><code>break</code>: Detiene la ejecución del ciclo.</li>
<li><code>continue</code>: Detiene la ejecución de una iteración y pasa a la siguiente.</li>
</ul>
<h3 id="labels">Labels:</h3>
<p>Los <em>labels</em> permiten etiquetar sentencias completas, y cada vez que se haga referencia al <em>label</em>, se estará haciendo referencia a toda la sentencia. Son particularmente útiles con las sentencias <code>break</code> y <code>continue</code> y <em>loops</em> aninados, de tal forma que se pueda salir o pasar a la siguiente iteración del <em>loop</em> externo desde el <em>loop</em> interno:</p>
<pre class=" language-js"><code class="prism  language-js"><span class="token comment">// Ejemplo de uso de labels para salir de un for-loop anidado</span>
outerLoop<span class="token punctuation">:</span> <span class="token keyword">for</span> <span class="token punctuation">(</span><span class="token keyword">let</span> i <span class="token operator">=</span> <span class="token number">0</span><span class="token punctuation">;</span> i <span class="token operator">&lt;</span> <span class="token number">10</span><span class="token punctuation">;</span> i<span class="token operator">++</span><span class="token punctuation">)</span> <span class="token punctuation">{</span>  
	innerLoop<span class="token punctuation">:</span> <span class="token keyword">for</span> <span class="token punctuation">(</span><span class="token keyword">let</span> j <span class="token operator">=</span> <span class="token number">0</span><span class="token punctuation">;</span> j <span class="token operator">&lt;</span> <span class="token number">10</span><span class="token punctuation">;</span> j<span class="token operator">++</span><span class="token punctuation">)</span> <span class="token punctuation">{</span>  
		<span class="token keyword">if</span> <span class="token punctuation">(</span>i <span class="token operator">===</span> <span class="token number">5</span> <span class="token operator">&amp;&amp;</span> j <span class="token operator">===</span> <span class="token number">5</span><span class="token punctuation">)</span> <span class="token punctuation">{</span>  

			<span class="token keyword">break</span> outerLoop<span class="token punctuation">;</span>  
		<span class="token punctuation">}</span>  
	<span class="token punctuation">}</span> 
<span class="token punctuation">}</span>
</code></pre>
<ul>
<li>En este ejemplo se está usando el <em>label</em> <code>outerLoop</code> para salir del <em>for loop</em> externo desde el <em>for loop</em> interno.</li>
</ul>
<h2 id="funciones-1">Funciones:</h2>
<p>Son un bloque de código que realiza cierta acción, que se ejecuta cuando es llamada, la sintaxis es:</p>
<pre class=" language-js"><code class="prism  language-js"><span class="token keyword">function</span> <span class="token function">functionName</span><span class="token punctuation">(</span>args<span class="token punctuation">,</span> <span class="token operator">...</span><span class="token punctuation">)</span> <span class="token punctuation">{</span>
	expressions
	<span class="token keyword">return</span>  obj
<span class="token punctuation">}</span>
</code></pre>
<ul>
<li><code>functionName</code> es el nombre de la función. Los nombres son sensibles a mayúsculas y minúsculas. El nombre debe empezar con una letra, el símbolo $ o guión bajo (_), seguido por letras, números, $ o _.</li>
<li><em>args</em> son los argumentos de la función separados por coma.</li>
<li>La función se deja de ejecutar cuando llega a <code>return</code>.   Si no se indica qué objeto retornar se retorna <code>undefined</code> por default.</li>
<li>Modificaciones en objetos y <em>arrays</em> dentro de la función modifica los valores fuera de ella.</li>
<li>Las funciones no necesariamente tienen que ser declaradas antes de usarlas.</li>
<li>Para llamar a la función usar: <br> <code>functionName(args, ...)</code></li>
</ul>
<h3 id="argumentos">Argumentos</h3>
<p>Los argumentos de una función se almacenan automáticamente en un array llamado <code>arguments</code> el cual se puede utilizar para acceder a los argumentos por su posición en lugar de por su nombre</p>
<p>Se puede pasar una cantidad indeterminada de argumentos a una función con la sintaxis <code>...TheArgs</code>:</p>
<pre class=" language-js"><code class="prism  language-js"><span class="token comment">// Ejemplo de uso de ...theArgs</span>
<span class="token keyword">function</span>  <span class="token function">multiply</span><span class="token punctuation">(</span>multiplier<span class="token punctuation">,</span> <span class="token operator">...</span>theArgs<span class="token punctuation">)</span> <span class="token punctuation">{</span>  
	<span class="token keyword">return</span>  theArgs<span class="token punctuation">.</span><span class="token function">map</span><span class="token punctuation">(</span><span class="token punctuation">(</span>x<span class="token punctuation">)</span> <span class="token operator">=&gt;</span> multiplier <span class="token operator">*</span> x<span class="token punctuation">)</span><span class="token punctuation">;</span>  
<span class="token punctuation">}</span>
</code></pre>
<ul>
<li><code>TheArgs</code> será un array dentro de la función. No estrictamente se tiene que llamar de esa manera.</li>
<li>Este argumento se debe de poner al final de los parámetros y todos los argumentos que por posición no tengan un correspondiente parámetro formarán parte de  <code>TheArgs</code>.</li>
<li>Otra alternativa para pasar una cantidad indeterminada de argumentos es declarando la función sin ningún parámetro, y dentro de la función usar el objeto  <code>arguments</code>, para acceder a ellos.</li>
</ul>
<h3 id="funciones-anónimas">Funciones anónimas:</h3>
<p>Son funciones con una sintaxis más simple, se suelen asignar a una variable.</p>
<pre class=" language-js"><code class="prism  language-js"><span class="token keyword">let</span> <span class="token function-variable function">var_name</span>  <span class="token operator">=</span> <span class="token keyword">function</span> <span class="token punctuation">(</span>args<span class="token punctuation">)</span><span class="token punctuation">{</span>
	expression
<span class="token punctuation">}</span><span class="token punctuation">;</span>

<span class="token comment">// Posteriormente se puede usar esa  variable para llamar la funciones</span>
<span class="token function">var_name</span><span class="token punctuation">(</span>args<span class="token punctuation">)</span>
</code></pre>
<h3 id="arrow-functions">Arrow functions</h3>
<p>Son funciones anónimas  con una sintaxis abreviada:</p>
<pre class=" language-js"><code class="prism  language-js"><span class="token punctuation">(</span>args<span class="token punctuation">)</span> <span class="token operator">=&gt;</span> expression<span class="token punctuation">;</span>
</code></pre>
<ul>
<li>Automáticamente se retornará  <em>expression</em>.</li>
<li>Es válido si la función solo tiene una sentencia.</li>
<li>Si la función solo tiene un argumento no es necesario poner los paréntesis.</li>
<li>Si la función no tiene argumentos poner los paréntesis vacíos.</li>
<li>Se pueden pasar una cantidad indeterminada de argumentos con el operador spread (<code>...theArgs</code>), el cual se usará como un <em>array</em> dentro de la función.</li>
<li>No tiene <code>this</code>, <code>arguments</code>, <code>super</code> o <code>new.target</code>.</li>
<li>Si se requiere que la función tenga más de una expresión usar llaves:</li>
</ul>
<pre class=" language-js"><code class="prism  language-js"><span class="token punctuation">(</span>args<span class="token punctuation">)</span> <span class="token operator">=&gt;</span> <span class="token punctuation">{</span>
	expressions
	<span class="token operator">...</span>
<span class="token punctuation">}</span>
</code></pre>
<p>Si es necesario que la función tenga nombre se puede asignar a una variable de la siguiente manera:</p>
<pre class=" language-js"><code class="prism  language-js"><span class="token keyword">const</span>  <span class="token function-variable function">my_arrow_function</span> <span class="token operator">=</span> <span class="token punctuation">(</span>args<span class="token punctuation">)</span> <span class="token operator">=&gt;</span> expression<span class="token punctuation">;</span>
</code></pre>
<ul>
<li>En lugar de <code>const</code>, se puede usar <code>let</code>.</li>
<li>Posteriormente se puede usar el nombre para llamar la función: <code>my_arrow_function(args)</code>.</li>
</ul>
<h3 id="jsdoc--comments">JSDoc  Comments:</h3>
<p>Estos bloques de comentarios se utilizan con fines de documentación y, a menudo, se denominan “comentarios JSDoc”. Estos bloques de comentarios se colocan inmediatamente antes de la función o método que describen.</p>
<p>Los elementos que lo conforman:</p>
<ul>
<li><code>/** ... */</code>: Esta sintaxis se usa para iniciar un bloque de comentarios multilínea en estilo JSDoc.</li>
<li><code>* ...</code>: Cada línea dentro del bloque de comentarios comienza con un asterisco (*) seguido de la descripción o anotación.</li>
<li><code>@param</code>: Esta anotación se utiliza para describir los parámetros de la función. Incluye el nombre del parámetro, su tipo y una descripción de lo que representa.</li>
<li><code>@returns</code>: Esta anotación (no utilizada en el ejemplo proporcionado) se puede utilizar para describir el tipo de retorno de la función y lo que devuelve la función.</li>
<li><code>@description</code>: Esta anotación (que tampoco se utiliza en el ejemplo proporcionado) se puede utilizar para proporcionar una descripción de alto nivel de lo que hace la función.</li>
</ul>
<p>Ejemplo:</p>
<pre class=" language-js"><code class="prism  language-js"><span class="token comment">/**
* Descripción de la función.
* @param {datatype} argName1 - Descripción del argumento.
* @param {datatype} argName2 - Descripción del argumento.
...
* @returns {datatype} - Descripción del valor retornado.
*/</span>
<span class="token keyword">function</span>  <span class="token function">myFuncition</span><span class="token punctuation">(</span>args<span class="token punctuation">)</span> <span class="token punctuation">{</span>
	<span class="token comment">// fuction  body</span>
<span class="token punctuation">}</span>
</code></pre>
<h3 id="closures.">Closures.</h3>
<p>Los closures son funciones anidadas cuya función interna conserva acceso a las variables de su función contenedora incluso después de que esta última ha terminado de ejecutarse. Para que un <em>closure</em> sea útil la función interna debe ser retornada (preferentemente, para conservar el <em>closure</em>) o llamada  por la función externa en algún momento, aunque por definición no es necesario que esto sea así, basta con que se utilicen variables de la función externa en la función interna para que sea un <em>closure</em>.</p>
<p>Las variables y funciones definidas en la función externa vivirán más tiempo que la duración de la ejecución de la función externa, si la función interna logra sobrevivir más allá de la vida de la función externa. Un <em>closure</em> se crea cuando la función interna se pone de alguna manera a disposición de cualquier alcance fuera de la función externa.</p>
<pre class=" language-js"><code class="prism  language-js"><span class="token keyword">function</span>  <span class="token function">outerFunction</span><span class="token punctuation">(</span><span class="token punctuation">)</span> <span class="token punctuation">{</span>
	<span class="token keyword">var</span>  outerVariable <span class="token operator">=</span> <span class="token string">'Soy una variable de la función externa'</span><span class="token punctuation">;</span>
		<span class="token keyword">function</span>  <span class="token function">innerFunction</span><span class="token punctuation">(</span><span class="token punctuation">)</span> <span class="token punctuation">{</span>
			console<span class="token punctuation">.</span><span class="token function">log</span><span class="token punctuation">(</span>outerVariable<span class="token punctuation">)</span><span class="token punctuation">;</span>
			<span class="token punctuation">}</span>
	<span class="token keyword">return</span>  innerFunction<span class="token punctuation">;</span>
<span class="token punctuation">}</span>

<span class="token keyword">var</span>  closureExample <span class="token operator">=</span> <span class="token function">outerFunction</span><span class="token punctuation">(</span><span class="token punctuation">)</span><span class="token punctuation">;</span>

<span class="token comment">// Retorna: "Soy una variable de la función externa"</span>
<span class="token function">closureExample</span><span class="token punctuation">(</span><span class="token punctuation">)</span><span class="token punctuation">;</span> 
</code></pre>
<ul>
<li>Para que un <em>closure</em> efectivamente sea preservado el resultado de la función externa se debe de asignar a una variable y posteriormente usar esta variable como una función como se nota en el ejemplo.</li>
<li>Notar que lo anterior captura la esencia de los <em>closure</em>, a pesar de que la función externa ya se ejecutó, la función interna (conservada en la variable <code>closureExample</code>) sigue teniendo acceso a las variables de la función externa independiente de en qué momento se llama a la función interna. Lo anterior solo aplica si la función externa retorna a la función interna.</li>
<li>Si la función interna es retornada por la función externa: Se genera un <em>closure</em> diferente cada vez que se asigna el resultado de la función externa a una variable y esos <em>closures</em> se almacenan en memoria.</li>
<li>Si la función interna no es retornada por la función externa: Se libera la memoria de los <em>closure</em> al terminar la ejecución de las funciones internas.</li>
</ul>
<p>En caso de que ambas funciones tengan argumentos, para pasarlos se puede hacer de las siguientes maneras:</p>
<pre class=" language-js"><code class="prism  language-js"><span class="token keyword">function</span>  <span class="token function">outside</span><span class="token punctuation">(</span>x<span class="token punctuation">)</span> <span class="token punctuation">{</span>  
	<span class="token keyword">function</span>  <span class="token function">inside</span><span class="token punctuation">(</span>y<span class="token punctuation">)</span> <span class="token punctuation">{</span>  
		<span class="token keyword">return</span> x <span class="token operator">+</span> y<span class="token punctuation">;</span>  
	<span class="token punctuation">}</span>  
<span class="token keyword">return</span>  inside<span class="token punctuation">;</span>  
<span class="token punctuation">}</span>  

<span class="token comment">// Se define primero la externa y luego la interna  </span>
<span class="token keyword">const</span> fnInside <span class="token operator">=</span> <span class="token function">outside</span><span class="token punctuation">(</span><span class="token number">3</span><span class="token punctuation">)</span><span class="token punctuation">;</span> 
console<span class="token punctuation">.</span><span class="token function">log</span><span class="token punctuation">(</span><span class="token function">fnInside</span><span class="token punctuation">(</span><span class="token number">5</span><span class="token punctuation">)</span><span class="token punctuation">)</span><span class="token punctuation">;</span> <span class="token comment">// 8</span>

<span class="token comment">// Se define ambas al mismo tiempo  </span>
console<span class="token punctuation">.</span><span class="token function">log</span><span class="token punctuation">(</span><span class="token function">outside</span><span class="token punctuation">(</span><span class="token number">3</span><span class="token punctuation">)</span><span class="token punctuation">(</span><span class="token number">5</span><span class="token punctuation">)</span><span class="token punctuation">)</span><span class="token punctuation">;</span> <span class="token comment">// 8</span>
</code></pre>
<h4 id="closures-anidados.">Closures anidados.</h4>
<p>En funciones anidadas de más niveles, las funciones internas tienen acceso a todas las variables de las funciones superiores a ella. En caso de que haya variables con mismos nombres, entonces las variables más internas tienen preferencia sobre las variables más externas.</p>
<h3 id="funciones-callback.">Funciones callback.</h3>
<p>Son funciones que se utilizan como argumento de otra función y desde esa otra función se llama a la función.</p>
<h4 id="settimeout">setTimeout</h4>
<p><code>setTimeout(functionRef, delay)</code>: Es una función especial que ejecuta una función después de cierto tiempos.</p>
<ul>
<li><code>functionRef</code>  es el nombre de la función que se ejecutará.</li>
<li><code>delay</code> es el número de milisegundos que pasará antes de ejecutar la función.</li>
<li>En caso de que la función tenga parámetros se deben de pasar después del argumento <code>delay</code>.</li>
</ul>
<h4 id="setinterval">setInterval</h4>
<p><code>setInterval(func, time)</code>: Es una función especial que ejecuta una función cada cierto tiempo.</p>
<ul>
<li><code>func</code> - <code>Function</code> o <code>string</code>:  es el nombre de la función que se ejecutará. Opcionalmente, en lugar de pasar una función, se puede pasar una cadena con código, el cual será ejecutado en cada intervalo.</li>
<li><code>delay</code> - <code>number</code> es el intervalo en milisegundos que se pasará entre cada ejecución de la función.</li>
<li>En caso de que la función tenga parámetros se deben de pasar después del argumento <code>delay</code>.</li>
</ul>
<h2 id="clases.">Clases.</h2>
<p>Posee atributos y métodos, un objeto es una instancia de una clase. Para crear clases se usa</p>
<pre class=" language-js"><code class="prism  language-js"><span class="token keyword">class</span> <span class="token class-name">ClassName</span><span class="token punctuation">{</span>
	attri <span class="token operator">=</span> val
	<span class="token operator">...</span>

	<span class="token function">constructor</span><span class="token punctuation">(</span>args<span class="token punctuation">)</span><span class="token punctuation">{</span>
		<span class="token keyword">this</span><span class="token punctuation">.</span>_attr1 <span class="token operator">=</span> val<span class="token punctuation">;</span>
		<span class="token operator">...</span>
	<span class="token punctuation">}</span>

	<span class="token keyword">get</span> <span class="token function">getName</span><span class="token punctuation">(</span>args<span class="token punctuation">)</span><span class="token punctuation">{</span><span class="token punctuation">}</span>

	<span class="token keyword">set</span> <span class="token function">setName</span><span class="token punctuation">(</span>args<span class="token punctuation">)</span><span class="token punctuation">{</span>attr <span class="token operator">=</span> val<span class="token punctuation">}</span>

	<span class="token function">methodName</span><span class="token punctuation">(</span>args<span class="token punctuation">)</span><span class="token punctuation">{</span>expressions<span class="token punctuation">}</span>
		<span class="token operator">...</span>
	<span class="token punctuation">}</span>
</code></pre>
<ul>
<li>Los atributos se suelen nombrar con un guion bajo al principio.</li>
</ul>
<h3 id="crear-instancias">Crear instancias:</h3>
<p>Para crear una instancia de una clase usar:</p>
<pre class=" language-js"><code class="prism  language-js"><span class="token keyword">let</span> myObject <span class="token operator">=</span> <span class="token keyword">new</span> <span class="token class-name">ClassName</span><span class="token punctuation">(</span>attrs<span class="token punctuation">)</span><span class="token punctuation">;</span>
</code></pre>
<ul>
<li>Automáticamente se manda a llamar el constructor de la clase.</li>
</ul>
<h3 id="métodos-1">Métodos</h3>
<p>Son acciones que pueden realizar las instancias de una clase. Se definen como funciones dentro de la clase, sin la palabra clave function:</p>
<pre class=" language-js"><code class="prism  language-js"><span class="token keyword">class</span> <span class="token class-name">ClassName</span><span class="token punctuation">{</span>

	<span class="token operator">...</span>

	<span class="token function">methodName</span><span class="token punctuation">(</span>args<span class="token punctuation">)</span><span class="token punctuation">{</span>
		<span class="token comment">// method body</span>
	<span class="token punctuation">}</span>
	<span class="token operator">...</span>
<span class="token punctuation">}</span>
</code></pre>
<h4 id="constructor">Constructor:</h4>
<p>El <em>constructor</em> es un método especial, que es llamado automáticamente al crear una instancia de una clase. Un constructor tiene una sintaxis similar a la de una función, el cual puede recibir parámetros y definir valores a las propiedades del objeto.  El constructor generalmente se utiliza para:</p>
<ul>
<li>Inicializar las propiedades de las instancias con valores</li>
<li>Validar los valores de las propiedades</li>
<li>Crear referencias a otros objetos (como conectarse con una base de datos)</li>
</ul>
<p>Sintaxis</p>
<pre class=" language-js"><code class="prism  language-js"><span class="token function">constructor</span><span class="token punctuation">(</span>arg1<span class="token punctuation">,</span> arg2<span class="token punctuation">)</span> <span class="token punctuation">{</span>  
	<span class="token keyword">this</span><span class="token punctuation">.</span>property1 <span class="token operator">=</span> arg1  
	<span class="token keyword">this</span><span class="token punctuation">.</span>property2 <span class="token operator">=</span> arg2
	<span class="token operator">...</span>  
<span class="token punctuation">}</span>
</code></pre>
<ul>
<li><code>this</code> es un objeto especial que hace referencia a la instancia que se está creando.</li>
<li>Los parámetros pueden tener valores por default.</li>
<li>Las propiedades no tienen porque estrictamente tomar los valores de los argumentos, pueden ser operaciones entre los argumentos y otras manipulaciones.</li>
</ul>
<h4 id="métodos-set-y-get">Métodos <em>set</em> y <em>get</em>:</h4>
<p>Son métodos especiales para recuperar o establecer los valores de las propiedades de un objeto:</p>
<ul>
<li><code>get get_name(args){return this.property}</code></li>
<li><code>set set_name(args){this.property = val}</code>
<ul>
<li>No estrictamente  se tiene que asignar  un valor, por  ejemplo, si  la propiedad es un array, se puede  agregar  elementos, en  lugar de asignar  valores.</li>
<li>Para utilizar estos métodos no es necesario usar paréntesis al llamarlos. <br> <code>obj.get_name</code> <br> <code>obj.set_name = val</code></li>
</ul>
</li>
</ul>
<h4 id="método-estáticos">Método estáticos:</h4>
<p>Son métodos que se utilizan directamente sobre las clases, y no sobre las instancias/objetos. Para crear un método estático utilizar la <em>keyword</em> <code>static</code> antes del método.</p>
<pre class=" language-js"><code class="prism  language-js"><span class="token keyword">static</span> <span class="token function">methodName</span><span class="token punctuation">(</span>args<span class="token punctuation">)</span> <span class="token punctuation">{</span>
	<span class="token comment">// method body</span>
<span class="token punctuation">}</span>
</code></pre>
<ul>
<li>No necesariamente tienen que recibir argumentos.</li>
<li>Como argumento se puede recibir una instancia/objeto.</li>
<li>Para llamar al método usar: <br> <code>className.method_name(args)</code></li>
</ul>
<h3 id="atributos-estáticos">Atributos estáticos:</h3>
<p>Son atributos exclusivos de la clase, pero no de las instancias/objetos. Para crear una propiedad estática utilizar la <em>keyword</em> <code>static</code> antes del nombre de la propiedad.</p>
<pre class=" language-js"><code class="prism  language-js"><span class="token keyword">static</span> attrbName <span class="token operator">=</span> val
</code></pre>
<ul>
<li>Para acceder al valor del atributo usar: <br> <code>className.attrName</code></li>
</ul>
<h3 id="herencia">Herencia:</h3>
<p><strong>Importante</strong>: Todas las clases automáticamente heredan las clases y atributos de la clase <em>object</em>.</p>
<p>La herencia es útil para acceder a todas las propiedades y métodos de una clase padre. Para heredar los atributos y los métodos de una clase a otra usar:</p>
<pre class=" language-js"><code class="prism  language-js"><span class="token keyword">class</span> <span class="token class-name">ChildClass</span> <span class="token keyword">extends</span> <span class="token class-name">ParentClass</span> <span class="token punctuation">{</span>

	<span class="token function">constructor</span><span class="token punctuation">(</span>parentArgs<span class="token punctuation">,</span> newArgs<span class="token punctuation">,</span> <span class="token operator">...</span><span class="token punctuation">)</span><span class="token punctuation">{</span>
		<span class="token keyword">super</span><span class="token punctuation">(</span>parentArgs<span class="token punctuation">)</span>
		<span class="token keyword">this</span><span class="token punctuation">.</span>_arg1 <span class="token operator">=</span> val
		<span class="token comment">// constructor body</span>
	<span class="token punctuation">}</span>

<span class="token punctuation">}</span>
</code></pre>
<h3 id="sobreescritura">Sobreescritura:</h3>
<p>En una clase hija se puede modificar el comportamiento de un método de la clase padre, se tiene que usar el mismo nombre y los mismos argumentos:</p>
<pre class=" language-js"><code class="prism  language-js"><span class="token function">metod_parent</span><span class="token punctuation">(</span>args<span class="token punctuation">)</span><span class="token punctuation">{</span>
	<span class="token keyword">super</span><span class="token punctuation">.</span>parentMethod
	<span class="token comment">// method body</span>
<span class="token punctuation">}</span>
</code></pre>
<ul>
<li><code>parentMethod</code> es el nombre del método en la clase padre, con <code>super.method_parent</code> se llama a ese método y después se pueden agregar más cosas.</li>
</ul>
<h2 id="regexp.">RegExp.</h2>
<p>Una expresión regular es una secuencia de caracteres para formar un patrón de búsqueda. La sintaxis es:</p>
<pre class=" language-js"><code class="prism  language-js"><span class="token keyword">const</span> re <span class="token operator">=</span>  <span class="token operator">/</span>pattern<span class="token operator">/</span>flags
</code></pre>
<ul>
<li>El patrón se pone entre <code>/</code>, <em>pattern</em> se refiere a el patrón a usar, si además se quieren agregar <em>flags</em>, entonces se deben de poner después del último <code>/</code>, no importa que sea más de una <em>flag</em>.</li>
<li><strong>Importante</strong>: No se pone entre comillas, no es una cadena.</li>
</ul>
<p>Otra forma de construir una expresión regular es con:</p>
<pre class=" language-js"><code class="prism  language-js"><span class="token keyword">const</span> re <span class="token operator">=</span> <span class="token keyword">new</span> <span class="token class-name">RegExp</span><span class="token punctuation">(</span><span class="token string">"pattern"</span><span class="token punctuation">)</span><span class="token punctuation">;</span>

<span class="token keyword">const</span> re <span class="token operator">=</span> <span class="token keyword">new</span> <span class="token class-name">RegExp</span><span class="token punctuation">(</span><span class="token string">"pattern"</span><span class="token punctuation">,</span> <span class="token string">"flags"</span><span class="token punctuation">)</span><span class="token punctuation">;</span>
</code></pre>
<ul>
<li>Utilizar esta forma cuando el patrón se estará modificando durante el programa  o cuando no se conoce con antelación el patrón.</li>
<li>En flags van todas las flags a usar en la misma cadena.</li>
<li>En este paso tanto el patrón como las banderas sí son cadenas.</li>
</ul>
<p>Para utilizar metacaracteres de manera literal como parte del patrón usar <code>\</code>, antes del metacaracter, por ejemplo:</p>
<pre class=" language-js"><code class="prism  language-js"><span class="token keyword">const</span> re <span class="token operator">=</span>  <span class="token regex">/a\*b/</span>
</code></pre>
<ul>
<li>En este ejemplo se está escapando el carácter <code>*</code>, para que el patrón incluya un asterisco literalmente.</li>
</ul>
<h3 id="flags">Flags</h3>

<table>
<thead>
<tr>
<th>Flag</th>
<th>Descripción</th>
<th>Propiedad correspondiente</th>
</tr>
</thead>
<tbody>
<tr>
<td><code>d.</code></td>
<td>Generar índices para coincidencias de subcadenas.</td>
<td><code>hasIndices</code>.</td>
</tr>
<tr>
<td><code>g.</code></td>
<td>Búsqueda global.</td>
<td><code>global</code>.</td>
</tr>
<tr>
<td><code>i.</code></td>
<td>Búsqueda sin distinción entre mayúsculas y minúsculas.</td>
<td><code>ignoreCase</code>.</td>
</tr>
<tr>
<td><code>m.</code></td>
<td>Permite que ^ y $ coincidan con caracteres de nueva línea.</td>
<td><code>multiline</code>.</td>
</tr>
<tr>
<td><code>s.</code></td>
<td>Permite que “.” coincida con una nueva línea.</td>
<td><code>dotAll</code>.</td>
</tr>
<tr>
<td><code>u.</code></td>
<td>“Unicode”; tratar un patrón como una secuencia de dígitos de código Unicode.</td>
<td><code>unicode</code>.</td>
</tr>
<tr>
<td><code>v.</code></td>
<td>Una actualización al modo u con más características Unicode.</td>
<td><code>unicodeSets</code>.</td>
</tr>
<tr>
<td><code>y.</code></td>
<td>Realice una búsqueda “sticky” que coincida a partir de la posición actual en la cadena de destino.</td>
<td><code>sticky</code>.</td>
</tr>
</tbody>
</table><h3 id="métodos-de-instancias-de-regexp">Métodos de instancias de <code>RegExp</code></h3>
<p>Para usar cualquiera de los métodos siguientes primero se tuvo que haber definido el patrón . O aplicarlo directamente sobre el patrón:</p>
<pre class=" language-js"><code class="prism  language-js"><span class="token keyword">const</span> myRe <span class="token operator">=</span> <span class="token regex">/d(b+)d/g</span><span class="token punctuation">;</span>  
<span class="token comment">// Sobre el objeto</span>
<span class="token keyword">const</span> myArray <span class="token operator">=</span> myRe<span class="token punctuation">.</span><span class="token function">exec</span><span class="token punctuation">(</span><span class="token string">"cdbbdbsbz"</span><span class="token punctuation">)</span><span class="token punctuation">;</span>

<span class="token comment">// Sobre el patron</span>
<span class="token keyword">const</span> myArray <span class="token operator">=</span> <span class="token regex">/d(b+)d/g</span><span class="token punctuation">.</span><span class="token function">exec</span><span class="token punctuation">(</span><span class="token string">"cdbbdbsbz"</span><span class="token punctuation">)</span><span class="token punctuation">;</span>
</code></pre>
<ul>
<li>
<p>Tanto <code>MyArray</code> como <code>MyRe</code> tendrán unas propiedades especiales que se resumen más adelante.</p>
</li>
<li>
<p><code>RegExp.test(str)</code> - <code>string</code>: Indica si un patrón está en una cadena.</p>
<ul>
<li><code>str</code> - <code>string</code>: Cadena donde buscar el patrón.</li>
</ul>
</li>
</ul>
<br>
<ul>
<li><code>RegExp.exec(str)</code> - <code>Array</code>, <code>null</code>: Retorna las coincidencias de un patrón en una cadena.
<ul>
<li><code>str</code> - <code>string</code>: Cadena donde buscar el patrón.</li>
<li>El array que se retorna tiene propiedades extras como index, input e índices (si se estableció la flag d).</li>
</ul>
</li>
</ul>
<br>

