


# CSS

**Cascading style sheet** (CSS) es un lenguaje para darle formato a los elementos HTML de una página web.

Los estilos se aplican en cascada, es decir, si se determina un estilo a un elemento padre (como `<body>`) entonces el mismo estilo se aplicará a todos los elementos hijos (como `<p>`, `<h1>`, etc.). Los estilos de cada elemento hijo se pueden especificar individualmente. La prioridad es como sigue:

1.	Inline - Elementos hijos, como `<p>`, `<h1>`, etc. usando el atributo `style`.
2.	Inline - Elementos padre, como `<body>`, usando el atributo `style`.
3.	Internal - Estilo a nivel de página con el elemento `<style>`. **Importante**: para que `<style>` realmente sobrescriba a `<link rel="stylesheet>`, se debe definir después de `<link rel="stylesheet>`. Se usar para establacer los estilos desde el mismo documento HTML.
4.	External - Estilos de archivos externos `.css` con el elemento `<link>`, usando el atributo `rel="stylesheet"`. Se puede usar para establecer los estilos a múltiples archivos con una sola hoja de estilo. **Importante**: Si un mismo elemento HTML se definió en diferentes hojas de estilo, entonces se utiliza el de la última hoja de estilo.

**Importante**: Lo recomendable es determinar los estilos de manera externa, es decir, con archivos CSS.


## Desde un archivo externo:

Para añadir estilos desde un archivo externo, es recomendado agregar una carpeta a la carpeta del proyecto, con el nombre "css", ahí se agregan las hojas de estilo que deben de tener la extensión `.css`. Posteriormente en la página de html se debe de agregar un `<link rel="stylesheet>` en la etiqueta `<head>` que haga referencia a la hoja de estilos.
```html
<!DOCTYPE html>
<html>
	<head>
		...
		<link href="path/to/file.css" rel="stylesheet">
	</head>
	<body>
		...
	</body>
</html>
```

**Importante**: Si un mismo elemento HTML se definió en diferentes hojas de estilo, entonces se utiliza el de la última hoja de estilo en la etiqueta `<head>`.

## Sintaxis general:

Para establecer los estilos, se tiene que especificar el _selector_ y entre llaves poner los atributos con sus respectivos valores, los atributos se separan por punto y coma y los valores se establecen con dos puntos. Las definiciones para distintos _selectors_ se pueden separar con salto de línea.
```css
selector {property1: value1; property2: value2; ...}
```
- _selector_ es un elemento HTML, existen otras formas de definirlos.
- _property_ es el nombre de una propiedad de CSS.
- _value_ son los valores de _property_.

**Ejemplo**:

```css
h1 {
	attr: val; 
	attr: val, 
	...
}

p {
	attr: val; 
	attr: val, 
	...
}

```
- En ese ejemplo los _selectors_ son `h1` y `p` que corresponden a nombres de elementos de HTML. Tener en cuenta que existen otras formas de definir los _selectors_.
- _attr_ y _val_ son atributos y valores de css respectivamente.

No es necesario identar ni poner saltos de línea, lo anterior se puede poner como:

```css
h1 {attr: val; attr: val, ...}
p {attr: val; attr: val, ...}
```

## Comentarios.

Para insertar comentarios en hojas de estilo (incluyendo la etiqueta `<style>`) se usa:
```css
/* esto es un comentario */
```
-	Los comentarios pueden abarcar partes de líneas, líneas completas o múltiples líneas, todos con la misma sintaxis.

## Selectores.

Un selector determina el elemento HTML que se le dará estilo. Existen varias formas de definir los selectores. A continuación se describen brevemente algunos de ellos.

-	**Selectores simples**: Seleccionan con base en el nombre, id o clase de un elemento HTML.
-	**Selectores combinados**: Selecciona elementos con base a la relación entre ellos.
-	**Selectores de pseudo-clase**: Seleccionan elementos con base a un estado específico.
-	**Selectores de pseudo-elementos**: Seleccionar y dan estilo a una parte de un elemento.
-	**Selectores de atributos**: Seleccionan elementos con base a un atributo o un valor de un atributo.

### Selectores simples: 

Seleccionan con base en el nombre, id o clase, y se aplican a todos los elementos que tengan ese nombre, id o clase.

```css
/* Ejemplo selector por nombre */
h1 {
attr: val; 
attr: val, 
...
}

/* Ejemplo selector por clase */
className {
attr: val; 
attr:val, 
...
}

/* Ejemplo selector por id */
idName {
attr: val; 
attr:val, 
...
}
```

#### Selector de elemento: 

Basado en el nombre del elemento HTML, el estilo se aplica a todos los elementos con el mismo nombre, respetando la jerarquía
```css
/* Ejemplo selector por nombre */
element {property: value; ...}
```
-	_element_ es el nombre de algún elemento HTML, como `<p>`, `<h1>`, etc.
-	Se pueden poner más de un elemento separados por coma: <br> `element1, element2, ... {property: value; ...}`

#### Selector id: 

Utiliza el atributo _id_ de un elemento HTML para seleccionar un elemento específico. Se utiliza junto el símbolo `#`, ejemplo:

```css
/* Ejemplo selector por id */
#id {property: value; ...}
```
-	El nombre _id_ debe tener al menos un carácter, no puede empezar por números y no debe tener espacios en blanco.

En el elemento HTML usar el atributo _id_ y el nombre del identificador sin la almohadilla (_#_) al inicio.
```html
<element id="name"> ... </element>
```

#### Selector de clase: 

Utilizando el atributo _class_ de los elementos de HTML, para seleccionar elementos de una misma clase. Se utiliza agregando un punto (`.`) al inicio:

```css
.ClassName {property:value; ...}
```
-	_className_ es el nombre de la clase.
-	Se pueden poner más de uno separando con coma. <br> `.ClassName1, .ClassName2, ... {property:value; ...}`

Es posible especificar el estilo a un mismo tipo de elemento que comparte la misma clase. Para más información revisar sub-clases:

```css
element.ClassName{property:value; ...}
```
-	_element_ es el nombre de algún elemento HTML, como `<p>`, `<h1>`, etc.
-	_className_ es el nombre de la clase.

En los elementos HTML usar el atributo _class_ y el nombre de la clase sin el punto al inicio.
```html
<elemento class="ClassName"> ... </element>
```
-   Es posible que el elemento pertenezca a más de una clase, para ello separar con espacios: <br> `<tagname class="class1 class2 ..."> content </tagname>`.

#### Selector universal:

Selecciona todos los elementos de HTML en el documento, para ello se utiliza un asterisco:
```css
*  {property:value; ...}
```
-	El selector universal es utilizado raramente.

### Selectores combinados:

#### Sub-clases
Basado en el nombre de algún elemento y una clase en específico, es decir solo los elementos que pertenezcan a una clase en específico.
```css
element.subclass {property:value; ...}
```
-	_element_ es el nombre de cualquier elemento de HTML y _subclass_ es el nombre de la subclase.

#### Selectores combinados:

Un _combinator_ explica la relación entre selectores, existe 4 _combinators_:
-	**Descendant selector** (espacio).
-	**Child selector** (`>`): Selecciona elementos que son elementos hijos directos de otro elemento. Solo selecciona los elementos que están un nivel por debajo del elemento especificado.
-	**Adjacent sibling selector** (`+`): Selecciona los elementos que están inmediatamente después de otro elemento. Solo selecciona los elementos que están directamente al lado del elemento especificado, no más abajo en el árbol DOM.
-	**General sibling selector** (`~`): Selecciona elementos que están después de otro elemento, pero no necesariamente inmediatamente después. Selecciona todos los elementos del elemento especificado, incluidos los que están separados por otros elementos.
-	Para ver más información revisar [esta página](https://www.w3schools.com/css/css_combinators.asp).

##### Descendant selector:
Selecciona elementos que son descendientes de otro elemento. Los descendientes pueden ser hijos directos o hijos anidados (nietos, bisnietos, etc.). 

```css
first_element second_element ...{property:value; ...}
```
-	los elementos están jerarquizados, _second_element_ está dentro de _firs_telement_. pero no necesariamente es un hijo directo, puede estar en cualquier nivel de profundidad.

```css
/* Ejemplo de descendant selector */
 div p {
  color: red;
}
```
-	Selecciona todos los elementos `<p>` dentro de los elementos `<div>` y se modifica el color.

##### Child selector:

Selecciona elementos que son elementos hijos directos de otro elemento. Solo selecciona los elementos que están un nivel por debajo del elemento especificado.
```css
parent_element > child_element {property:value; ...}
```
-	_child_element_ es un hijo directo de _parent_element_.

```css
/* Ejemplo de child selector */
ul > li {
  font-weight: bold;
}
```
-	Selecciona los elementos `<il>` que son hijos directo de `<ul>`.

##### Adjacent sibling selector:

Selecciona el elemento que está inmediatamente posterior a otro elemento, no los que están adentro, sino después. Si hay más de un elemento del tipo `element1` solo seleccionará el primero, para seleccionar más de uno usar el _general sibling selector_.
```css
element1 + element2 {property:value; ...}
```
-	_element1_ y _element2_ están contiguos.

```css
/* Ejemplo de adjacent sibling selector */
h1 + p {
  margin-top: 0;
}
```
-	Selecciona el primer elemento `<p>` que está después de los elementos `<h1>`.

##### General sibling selector:

Selecciona elementos que están después de otro elemento, pero no necesariamente inmediatamente después. Selecciona **todos** los elementos del elemento especificado, incluidos los que están separados por otros elementos.
```css
element1 ~ element2 {property:value; ...}
```
-	_element2_ está posterior a _element1_, pueden ser uno o más y deben estar al mismo nivel que _element1_, no adentro.

```css
/* Ejemplo de general sibling selector */
h2 ~ p {
  font-size: 16px;
}
```
-	Todos los elementos `<p>` que están después de un encabezado `<h2>`.

### Pseudo clases:

Son usados para definir un estado especial de un elemento (como los _visited_, _hover_, etc. de `<a>`). Utilizan dos puntos y se pueden combinar con las clases. Algunas pseudo-clases son:
```css
element:pseudo-class {property:value; ...}
```
-	`:active`: Link activo (al momento de tenerlo presionado)
-	`:hover`: Al colocar el cursor encima del elemento.
-	`:first-child`: Específica un elemento que es el primer hijo de otro elemento.
-	`:lang`: Permite definir reglas especiales para diferentes idiomas.
-	Existen muchos más, revisa [este link](https://www.w3schools.com/css/css_pseudo_classes.asp).

### Pseudo elementos:

Se utilizan para dar formato a partes específicas de un elemento, como la primera letra, la primera línea, insertar contenido antes o después del contenido de un elemento, entre otros. Se utiliza dobles dos puntos:

```css
element :: psudo-element {...}
```
-	`::after`: Permite insertar contenido después del contenido actual de un elemento. 
-	`::before`: Permite insertar contenido después del contenido actual de un elemento.
-	`::first-letter`: Permite estilizar la primer letra del contenido de un elemento.
-	`::first-ine`: Permite estilizar la primer letra del contenido de un elemento.
-	`::marker`: Permite seleccionar las viñetas de un elemento. Las viñetas son como las de las listas, tanto numeradas como no numeradas.
-	`::selection`: Permite estilizar el texto seleccionado del contenido de un elemento.
-	Para más información visitar [este link](https://www.w3schools.com/css/css_pseudo_elements.asp)

Para insertar contenido generalmente se hará uso de la propiedad `content` poniendo entre comillas en contenido que se quiere agregar, por ejemplo:
```css
element :: after {
	content: "something"
}
```

### Selectores de atributo:

Se utiliza para dar estilo a todos los elementos que comparten algún atributo en particular, los atributos son de los de HTML, además se puede especificar algún valor en particular.
```css
element[attr_name] { ... }

element[attr_name="val"] { ... }
```
-	`element` es el nombre del elemento y `attr_name` es el nombre del atributo. Opcionalmente se puede especificar una valor para el atributo.


Además, se pueden especificar otro tipo de patrones, por ejemplo:
```css
/* Atributo contenga la palabra */
element_name[attr_name~="word"] { ... }

/* Atributo contenga una de las dos palabras. */
element_name[attr_name |= "word1-word2"] { ... }

/* Atributo comience por la palabra. */
element_name[attr_name ^= "word1"] { ... }

/* Atributo termine por la palabra. */
element_name[attr_name $= "word1"] { ... }

/* Atributo contiene la palabra. */
element_name[attr_name *= "word1"] { ... }
```
 
## Box-model:
 
![Box model.](https://developer.mozilla.org/en-US/docs/Learn/CSS/Building_blocks/The_box_model/box-model.png)

En html cada elemento está dentro de una caja que consiste de varias capas:
-	_Content_: Es donde estará como tal el contenido.
-	_Padding_: Es el espacio entre el contenido y algún borde que se pueda poner.
-	_Border_: Es el espacio que abarcará algún borde que se quiera poner. además de poder indicar su ancho se puede indicar el tipo de borde y el color:
-	_Margin_: Es el espacio entre el borde y otros elementos de la página.

### Formas de definirlos:

Al definir los argumentos de _border_, _padding_ y _margin_ se puede hacer:
-	**Un solo valor**: Aplica el mismo valor a _top_, _bottom_, _right_ y _left_. <br> `property all`
-	**Dos valores**: Un valor diferente para _top_ y _bottom_ y otro para _right_ y _left_:	<br> `property top-bottom right-left`
-	**Tres valores**: Un valor diferente para _top_, otro para _bottom_ y otro para _right_ y _left_: <br> `property top right-left bottom`
-	**Cuatro valores**: Propiedades individuales: Cada propiedad en el siguiente orden <br> `property top right bottom left`
-	Centrado horizontalmente, verticalmente o ambas.
-	El valor **auto** centra horizontalmente el elemento dentro de su contendor (aplica en margin), al _top_ y _bottom_ asigna 0, se puede especificar el _top_ y _bottom_ usando dos valores. 
-	Propiedades individuales: Cada propiedad se puede especificar individualmente (las siguientes son las propiedades abreviadas):
	-	_margin-top_.
	-	_margin-bottom_.
	-	_margin-left_.
	-	_margin-right_.
	-	_border-top_.
	-	_border-bottom_.
	-	_border-left_.
	-	_border-right_.
	-	_padding-top_.
	-	_padding-bottom_.
	-	_padding-left_.
	-	_padding-right_.
-	existen propiedades específicas para cada lado, como:
	-	_property-top-width_.
	-	_property-bottom-width_.
	-	_property-right-width_.
	-	_property-left-width_.


## Flexbox.

Permite acomodar elementos dentro de un elemento contenedor, de manera más amigable que con la propiedad `float` o `position`. Para ello dentro del elemento contenedor se utiliza la propiedad `display` con el valor `flex`.
```css
selector {
display: flex;
...
}
```
-	_flex_ no es el único valor válido, para más información visitar la [documentación]( https://developer.mozilla.org/en-US/docs/Web/CSS/display).

## Estados de Links:

Los links se pueden personalizar en diversos estados:
-	_a:link_: Link normal, sin visitar.
-	_a:visited_: Link que ya se visitó.
-	_a:hover_: Link al poner el cursor sobre él.
-	_a:active_: Al momento de estar presionando sobre él.
-	**IMPORTANTE**: Se debe respetar cierto orden al definir los estados:
-	_a:hover_ debe de ir después de _a:link_ y _a:visited_.
-	_a:active_ debe de ir después de _a:hover_.
 
## Propiedades:

En esta sección se enlistan algunas de las propiedades de CSS más importantes.

### Generales:

-	`display` \- `{block, inline, inline-block, flex, none}`: Es para modificar la forma como se muestra un elemento. Modifica si se muestra como _inline_ o _block_, pero no modifica el tipo de elemento que es, por ejemplo, un elemento _inline_ con "_display: block_" no puede tener otros elementos _block_ adentro. Para más información visitar la [documentación](https://developer.mozilla.org/en-US/docs/Web/CSS/display).
-	`inline-block`: Permite establecer un alto y ancho del elemento y _top/bottom_ de _margin/padding_ son respetados (no pasa con _inline_). Además, no agrega un salto de línea después del elemento.
	-	`none`: No muestra el elemento y además elimina el espacio que ocuparía.
	-	`flex`: Consulta Flexbox.
-	`position` \- `{static, relative, fixed, bsolute, sticky}` (default: `static`): Especifica el método de posicionamiento de un elemento. Para más información visitar la [documentación](https://developer.mozilla.org/en-US/docs/Web/CSS/position).
	-	`static`: No es posicionada de alguna manera especial y no se ve afectado por las propiedades _top_, _bottom_, _left_ y _right_.
	-	`relative`: Se posiciona relativamente a su posición normal, es decir la posición por default. Especificando _top_, _bottom_, _left_ y _right_ provoca que se ajuste desde su posición normal.
	-	`fixed`: Se posiciona relativo al _viewport_ (pantalla disponible). Siempre se ve incluso si da scroll a la página en cualquier dirección se utiliza las propiedades top, bottom, left y right.
	-	`absolute`: Se posiciona relativo a su elemento padre. Si el elemento no está dentro de algún otro elemento, entonces se considera el elemento <body>.
	-	`sticky`: Se posiciona de manera estática, pero si se hace scroll cuando llegue a su posición determinada en top, bottom, left o right se comportará como elemento fijo.
-	`z-index`: Es un índice para indicar la posición de elementos apilados (que aparezcan en frente, detrás, etc.), solo funciona con elementos con position _absolute_, _relative_, _fixed_ o _sticky_. Puede ser cero, positivos o negativos. Para más información visitar la [documentación](https://developer.mozilla.org/en-US/docs/Web/CSS/z-index).
 
![{{Indice Z.](https://miro.medium.com/v2/resize:fit:720/format:webp/1*uGPV3qEF7yBq4PD0zua19A.png)

-	`overflow` \- `{visible, hidden, scroll, auto}`: Para indicar que ocurre con el contenido que es muy grande para caber en un área. Es necesario especificar la propiedad height. Existen variantes solo para un eje como `overflow-x` y `overflow-y`. Para más información visitar la [documentación](https://developer.mozilla.org/en-US/docs/Web/CSS/overflow).
	-	_visible_: Se desborda el contenido.
	-	_hidden_: No se muestra el contenido que no cabe.
	-	_scroll_: Se puede hacer _scroll _ en el contenido para visualizarlo dentro del contenedor.
	-	_auto_: Similar a _scroll_.
-	`float` \- `{left, right, none, inherit}`: Se utiliza para posicionar y dar formato a contenido, por ejemplo, colocar una imagen a lado de un texto. Para más información visitar la [documentación](https://developer.mozilla.org/en-US/docs/Web/CSS/float).
-	`clear` \- `{none, left, right, both, inherit}`: Se utiliza cuando se usa la propiedad `float`, para indicar que se quiere el elemento por debajo del elemento _float_.  Para más información visitar la [documentación](https://developer.mozilla.org/en-US/docs/Web/CSS/clear).

#### Flexbox:

Propiedades cuando se utiliza `display: flex`. Todas estas propiedades se definen en el mismo elemento contenedor, donde se definió `display: flex`. Para más información visitar la [documentación](https://developer.mozilla.org/en-US/docs/Learn/CSS/CSS_layout/Flexbox).
-	`flex-direction` \- `{row, row-reverse, column, column-reverse}`: Determina como se acomodan los elementos del contenedor _flexbox_. 
-	`flex-wrap` \- `{wrap, nowrap, wrap-reverse}`: Define si los elementos aparecen en una línea (_no-wrap_) o en múltiples líneas (_wrap_).
-	`flex-flow` \- `direction wrap`: Es una versión abreviada de las propiedades _flex-direction_ y _flex-wrap_. Los valores posibles son los mismos que los respectivos de ambas propiedades, primero indicando _direction_ y posteriormente _wrap_.
-	`justify-content` \- `{flex-start, flex-end, center, space-between, space-around, space-evenly}`: Define como los elementos son alineados con respecto al eje principal (_direction_) dentro de un contenedor _flexbox_. Los que empieza con _space_ distribuyen los elementos en el eje.
-	`align-items` \- `{flex-start, flex-end, center, baseline, stretch}` (defult: `stretch`): Define cómo los elementos se alinean de acuerdo al eje secundario.
-	`align-content` \- `{flex-start, flex-end, center, space-between, space-around, space-evenly}`: Define cómo cada línea se alinea dentro del contenedor, solo aplica si `flex-wrap: wrap` está definido y si se tiene múltiples líneas.

Las siguientes propiedades se aplican en los elementos interiores.
-	`order` \- _integer_: Orden de los elementos.
-	`flex-grow` \- _integer_: Define cuánto puede crecer un elemento si hay espacio disponible.
-	`flex-basis` \- _auto_, _lenght_: Define el tamaño inicial de un elemento en el flexbox. 
-	`align.self` \- `{flex-start, flex-end, center, baseline, stretch}`: Similar a `align-items`, pero para un item individual. Define cómo el elemento se alinea de acuerdo al eje secundario.

### Texto:
Propiedades para el formato de texto.

#### Color:
-	`color` \- _color_: Especifica el color del elemento, principalmente el color de texto.

#### Alineación del texto:
-	`text-align` \- `{left, right, center, justify`} (default: `left`): Alineación del texto horizontalmente.
-	`text-align-last` \- `{left, right, center, justify}` (default: `left`): Especifica la alineación de la última línea de un texto.
-	`direction` \- `{rtl, ltf}` (default: `ltf`): Dirección del texto:
	-	_rtl_: Derecha a izquierda.
	-	_ltf_: Izquierda a derecha.
-	`vertical-align` \- `{baseline, text-top, text-bottom, sub, sup}` (default: `baseline`): Alineación vertical del texto.
	-	_baseline_: Alineación normal.
	-	_text-top_: Alineación superior.
	-	_text-bottom_: Alineación inferior.
	-	_sub_: Alineación inferior, es menor que _text-bottom_.
	-	_sup_: Alineación superior, es mayor que _text-top_.

#### Otros:
-	`unicode-bidi`: Se usa junto con _direction_, para establecer si el texto puede soportar múltiples lenguajes en el mismo documento.

#### Decoraciones:
Particularmente útil para links.

-	`text-decoration-line` \- _{overline, line-through, underline}_: Añade una línea al texto, ya sea arriba, abajo o en medio, se puede poner más de un valor, separado por espacios, para combinar los valores.
-	`text-decoration-color` \- _color_: Color de la _decoration line_. 
-	`text-decoration-style` \- `{dotted, dashed, solid, double, groove, ridge, inset, outset, none, hidde}`: Estilo de la línea de la _decoration line_.
-	`text-decoration-thickness` \- _length_, _%_, _auto_: Ancho de la línea de la _decoration line_.
-	`text-decoration` \- `line color style thickness`: Versión abreviada donde se especifican todas las propiedades en una sola.

#### Mayúsculas/Minúsculas:

-	`text-transform` \- `{uppercase, lowercase, capitalize}`: Se usa para transformar el texto a mayúsculas, minúsculas o para poner en mayúsculas la primera letra de cada palabra. 

#### Sangría y espacios:

-	`text-indent` \- `length`: Sangría de la primera línea de un texto.
-	`letter-spacing` \- `length`: Espacio entre caracteres de un texto. Acepta valores negativos
-	`line-height` \- `length`: Espacio entre líneas de un texto.
-	`word-spacing` \- `length`, `normal` (default: `normal`): Espacio entre palabras de un texto.
-	`white-space` \- `{normal, nowrap, pre, pre-wrap, pre-line}`: Especifica como se manejan los espacios en blanco:
	-	_normal_: Más de un espacio se combinan en uno, se ignoran los saltos de línea y el texto se ajusta al tamaño de la ventana.
	-	_nowrap_: Similar a _normal_, pero el texto no se ajusta al tamaño de la ventana.
	-	_pre_: Se conservan el número de espacios en blanco y los saltos en línea solo en líneas nuevas.

#### Fuentes:
Existen cinco familias de fuentes genéricas:
-	_Serif_: Times New Roman, Georgia, Garamond, etc.
-	_Sans-serif_: Arial, Verdana, Helvetica, etc.
-	_Monospace_: Courier New, Lucida Console, Mocano.
-	_Cursive_: Brush Script MT, Lucida Handwriting, etc.
-	_Fantasy_: Copperplate, papyrus, etc.

Las propiedades son:
-	`font-family`: Nombre de la fuente, si el nombre tiene espacios poner entre comillas dobles. Es recomendado poner varias, separadas por coma.
-	`font-style` \- `{normal, italic, oblique}`: Específica si poner el texto en cursiva.
-	`font-weight` \- `{thin, extra light, light, normal, medium, semi bold, bold, extra bold, ultra bold}` o `number`: Ancho de la fuente, también puede ser un número, más o menos entre 100 y 900.
-	`font-variant` \- `{normal, small-caps}`: Especifica si la fuente debe de ser "small-caps", que son en mayúsculas, pero de un tamaño menor al de las mayúsculas normales.
-	`font-size` \- `length` (default: 16px): Establece el tamaño de la fuente, aparte de establecerla con unidades normales se puede establecer como:
	-	_em_: Permite que los usuarios modifiquen el tamaño en los menús de sus navegadores. `1em` equivale a 16px que es el tamaño por default se recomienda paralelamente establecer `font-size: 100%`, en `<body>` y en el resto usar _em_. Ejemplo: `1em`.
	-	_vw_: El tamaño de la fuente se autoajusta al tamaño de la venta. `1vw` equivale a 1% del _viweport width_, es decir si el _viewport_ es de 50cm entonces `1vw` es _0.5cm_.
-	`font` \- `style variant weight size family`: Versión abreviada donde se pueden especificar varias propiedades en una sola, `font-size` y `font-family` son obligatorias.

##### Web safe fonts: 
Son fuentes que son seguras y la mayoría de los navegadores y dispositivos pueden usar:
-	Arial (sans-serif)
-	Verdana (sans-serif)
-	Helvetica (sans-serif)
-	Tahoma (sans-serif)
-	Trebuchet MS (sans-serif)
-	Times New Roman (serif)
-	Georgia (serif)
-	Garamond (serif)
-	Courier New (monospace)
-	Brush Script MT (cursive)


#### Google fonts:
Para usar fuentes de Google se debe de crear un `<link>` en `<head>` y en CSS hacer referencia a la fuente con la propiedad `font-family`, usando el nombre de la fuente entre comillas dobles: `"font-name"`.

**Importante**: Se recomienda poner otra fuente en caso de que la fuente de Google falle.

## Contadores

Los contadores son como variables que son incrementadas por ciertas reglas de CSS, se utilizan 4 propiedades:
-	`counter-reset`: Crea o resetea un contador.
-	`counter-increment`: Incrementa el valor de un contador.
-	`content`: Inserta el contador generado
-	`counter()`/`counters()`: Agrega el valor del contador a un elemento.

**Ejemplo**:
```css
body {
/* crea el contador "section" */
  counter-reset: section;
}

h2::before {
/* indica que se incremente el contador "section" */
  counter-increment: section;
/* Agrega el valor del contador, counter() no va entre comillas*/
  content: "Section " counter(section) ": ";
}
```

## Backgrounds:

Propiedades relacionadas con el fondo de un elemento.

-	`background-color` \- `color` (default: `transparent`): Especifica el color de fondo de un elemento.
-	`opacity` \- `num: [0.0, 1.0]` (default: `1`): Especifica la transparencia de un elemento, donde 0 es transparente. **Importante**: Esta propiedad se hereda a los elementos hijos, para ello mejor determina la transparencia en el color.
-	`background-image` \- `function`, `none` (default: `none`): Establece el _background _con una imagen para un elemento, la imagen se repite para cubrir todo el elemento. Algunas opciones son:
-	`url()`: Especifica una dirección o ruta a una imagen. La url se pone entre comillas dobles, es preferible tener la imagen en la misma carpeta del proyecto en una subcarpeta llamada _img_.
-	`linear-gradient()`: Especifica un fondo gradiente lineal.
-	`radial-gradient()`: Especifica un fondo gradiente radial.
-	`background-repeat` \- `{repeat-x, repear-y, no-repeat}` (default: `repeat`): Controla como repetir la imagen en `background-image`. Por default se repite tanto horizontalmente como verticalmente.  Las opciones son:
	-	_repeat-x_: Para que se repita solo de manera horizontal.
	-	_repeat-y_: Repite la imagen solo de manera vertical.
	-	_no-repeat_: Para que no se repita la imagen.
-	`background-position` \- `% %` o 2 de las sig. Opciones `{top, bottom, left, right, center}` (default: `0% 0%`): Indica la posición de la imagen de `background-image`, particularmente útil si `background-repeat: no-repeat`. Se puede definir como:
	-	Un porcentaje con respecto al eje horizontal y vertical: `background-position: x% y%;`
	-	Una combinación de las _keywords_ para el eje vertical y horizontal: `background-position: y_keyword x_keyword;`
-	`background-attachment` \- `{fixed, scroll}` (default: `scroll`): Indica si la imagen debe de moverse al hacer _scroll_ o quedarse fija.
-	`background` \- `color image repeat position attachment`: Versión abreviada, donde se especifican todas las propiedades del _background_ en una sola propiedad, el orden no importa.	

**Otros**:
-	`background-size`: Tamaño de la imagen.
-	`background-origin`: _Origin _(ubicación de la imagen) de la imagen.
-	`background-clip`: Define la extensión (área) del _background _dentro del elemento.

## Listas:
Propiedades de lista:
-	`list-style-type`: Estilo del _marker_, el valor depende de si es `<ol>` o `<ul>`.
	-	`<ul>`: valores posibles `{circle, square, none}`.
	-	`<ol>`: 
-	`list-style-image` \- `function`: Utiliza una imagen como _marker_, usando la función `url()`.
-	`list-style-position` \- `{outside, inside}`: Para indicar si el texto debe tener sangría con respecto al _marker_ (cuando un elemento de la lista abarca dos o más líneas).
-	`list-style` \- `type position image`: Versión abreviada para establecer varias propiedades en una, el orden importa.
-	`padding` \- `number`: Se utiliza para definir qué tanta sangría tienen los elementos.

## Tablas:

### Selectores:

-	`tr:hover`: Para que se resalte una fila al pasar el mouse por encima.
-	`tr:nth-child()`: Para seleccionar las filas pares (_even_) o impares (_odd_) incluyendo el encabezado.

### General:

-	`text-align` \- `{left, right, center}`: Alineación del texto. Se especifica en `<td>` o `<th>`.
-	`vertical-align` \- `{top, bottom, middle}`: Alineación vertical del texto. Se especifica en `<td>` o `<th>`.
-	`padding` \- `length` Espacio ente los bordes y el contenido de la tabla. Se especifica en `<td>` o `<th>`.

### Bordes

Los bordes se definen para `<table>,` `<th>` y `<td>`.
-	`border` \- `width style color`: Establece varias propiedades del borde. Se pueden usar propiedades específicas para solo especificar un borde, ejemplo:
o	`border-bottom`.
-	`border-collapse` \- `{separate, collapse}` (default: `separate`): Como `<th>` y `<td>` tienen bordes independientes, entonces puede parecer como si tuvieran doble borde, para evitar eso usar `collapse`.

## Borders:

Especifican las propiedades de los bordes de los elementos. **Importante**: Las siguientes propiedades serán la general para todos los lados, pero existen las mismas propiedades para cada lado individual.

-	`border-style` \- `{dotted, dashed, solid, double, groove, ridge, inset, outset, none, hidde}` (defult: `none`). Estilo del borde. Para visualizar cada estilo consulta la imagen.
-	`border-width` \- 1 a 4 de `lenght` o `{thin, medium, thick}`: Ancho del borde. Puede ser un tamaño específico o un valor predefinido. Se puede especificar todos los lados o lados específicos. Para más información consulta Box-model.
-	`border-color` \- 1 a 4 de  `color`: Color del borde. Si no se especifica hereda el color del elemento padre. Se puede especificar todos los lados o lados específicos. Para más información consulta Box-model.
-	`border` \- `color style width`: Versión abreviada, donde se especifican algunas propiedades del _border_ en una sola propiedad.
-	`border-radius` ` \- 1 a 4 de `number` (default: `0`): Define el radio de las esquinas, es para hacer redondeadas las esquinas. Se puede usar pixeles (_px_) o porcentajes (_%_). Se puede especificar todos los lados o lados específicos. Para más información consulta Box-model.

**Ejemplo**:
Tabla con desplazador horizontal:
```css
<div style="overflow-x: auto;">
<table>
... table content ...
</table>
</div> 
```

**Estilos de bordes**:
 
 ![Estilos de bordes.](https://www.w3.org/community/webed/wiki/images/a/af/Cssed_borderstyles.png)


## Margin:

Especifican el ancho del espacio que hay entre un elemento y el resto de los elementos. 
**Importante**: Los elementos que están juntos pueden colapsar su _margin_, es decir si hay dos elementos, cada uno con su _margin_ especificado, puede que solo se muestre el de mayor ancho, porque se colapsaron los _margins_, no se mostraría la suma de ambos, sino solo el mayor, eso pasa verticalmente, se colapsan los _margins_ verticales de los elementos en el de mayor _margin_.

-	`margin-top` \- `length`, `inherit`, `Percentage%`: Ancho de la parte superior.
-	`margin-bottom` \- `length`, `inherit`, `Percentage%`: Ancho de la parte inferior.
-	`margin-left` \- `length`, `inherit`, `Percentage%`: Ancho de la parte izquierda.
-	`margin-right` \- `length`, `inherit`, `Percentage%`: Ancho de la parte derecha.
-	`margin` \- 4 de `length`, `auto`, `inherit`: Versión abreviada, se tiene que indicar cada propiedad o por pares, revisa Box-model para más información. 

## Padding:

Especifica el ancho entre el contenido y el borde de un elemento. 

**Importante** el _padding_ influye en la propiedad _width_ de los elementos, por lo que el _width_ final de un elementos será _width + padding_ (izquierdo y derecho), para evitar eso usar la propiedad `box-sizing`.

-	`padding-top` \- `length`, `inherit`, `Percentage%`: Ancho de la parte superior.
-	`padding-bottom` \- `length`, `inherit`, `Percentage%`: Ancho de la parte inferior.
-	`padding-left` \- `length`, `inherit`, `Percentage%`: Ancho de la parte izquierda.
-	`padding-right` \- `length`, `inherit`, `Percentage%`: Ancho de la parte derecha.
-	`padding` \- 4 de `length`, `auto`: Versión abreviada, se tiene que indicar cada propiedad o por pares, revisa Box-model para más información. 

## Outline:
 
Es una línea que se pone alrededor de los elementos, entre el _border_ y el _margin_, se usa para resaltar algunos elementos. No forma parte de la dimensión del elemento y puede que se encime con otros elementos:
-	`outline-style` \- `{dotted, dashed, solid, double, groove, ridge, inset, outset, none, hidde}` (defult: `none`). Estilo del _outline_. Para ver como se ve cada estilo consulta más abajo la imagen.
-	`outline-color` \- 4 de `color`: Color del outline. Puede ser un tamaño específico o un valor predefinido en cierta unidad.
-	`outlone-width` \- `length` o `{thin, medium, thick}`: Ancho del _outline_. Puede ser un tamaño específico o un valor predefinido en cierta unidad.
-	`outline-offset` \- `length`: Especifica un espacio transparente entre el _border_ y el _outline_.
-	`outline` \- `width style color`: Versión abreviada para definir el ancho, estilo y color al mismo tiempo. No importa el orden.

![Outline.](https://storage.googleapis.com/dycr-web/image/topic/css/outline-view.png)

## Imágenes.

Algunas propiedades del elemento `<img>`:
-	`opacity` \- `number: [0,1]`: Transparencia de la imagen, siendo 0 completamente transparente.

**Selectores**:
-	`img:hover {}`:

## Estilo del cursor:
Se refiere al tipo de cursor que aparece al poner el mouse sobre un elemento:
-	`cursor` \- `{auto, crosshair, default, e-resize, help, move, n-resize, ne-resize, nw-resize, pointer, progress, s-resize, se-resize, sw-resize, text, w-resize, wait}`: Para ver cómo se ve cada uno visita [esta pagína](https://cssreference.io/property/cursor/) (coloca el cursor sobre el texto).
.
## Alto y ancho:
Propiedades relacionadas con el alto y ancho del contenido de un elemento, sin incluir _padding_, _border_ ni _margin_:
-	`width` \-  `length`, `auto`, `Percentage%`, `initial`, `inherit` (default: `auto`): Ancho del elemento. Las opciones son:
	-	_auto_: Valor por default. El navegador calcula el ancho
	-	_lenght_. Define el ancho en unidades, como px, pt, cm, etc.
	-	_%_: Define el ancho como porcentaje del bloque contenedor.
	-	_initial_: Define el ancho a su valor por default.
	-	_inherit_: Hereda el ancho de su elemento padre.
-	`height` \ `length`, `auto`, `Percentage%`, `initial`, `inherit` (default: `auto`): Alto del elemento. Las opciones son:
	-	_auto_: Valor por default. El navegador calcula el ancho
	-	_lenght_. Define el ancho en unidades, como px, pt, cm, etc.
	-	_%_: Define el ancho como porcentaje del bloque contenedor.
	-	_initial_: Define el ancho a su valor por default.
	-	_inherit_: Hereda el ancho de su elemento padre.
-	`max-width` \- `none`, `length`, `Percentage%` (default: `none`): Establece el ancho máximo de un elemento. Si la pantalla es menor a ese ancho el elemento se ajusta
	-	`none`: Define que no hay un ancho máximo.
	-	`lenght`. Define el ancho máximo en unidades, como px, pt, cm, etc.
	-	`%`: Define el ancho máximo como porcentaje del bloque contenedor.
-	`max-height` \- `none`, `length`, `Percentage%` (default: `none`): Establece el alto máximo de un elemento. Si la pantalla es menor a ese alto el elemento se ajusta
	-	`none`: Define que no hay un ancho máximo.
	-	`lenght`. Define el ancho máximo en unidades, como px, pt, cm, etc.
	-	`%`: Define el ancho máximo como porcentaje del bloque contenedor.

**Otros**:
-	`max-height`: Alto máximo.
-	`min-height`: Alto mínimo.
-	`min-width`: Ancho mínimo.

## Posición:
Propiedades relacionadas con la propiedad _position_, se ponen después de haber especificado en tipo de posicionamiento.
-	`top` \- `auto`, `length`: Define la posición del elemento de acuerdo a su parte superior. 
-	`left` \- `auto`, `length`: Define la posición del elemento de acuerdo a su parte izquierda.
-	`right` \- `auto`, `length`: Define la posición del elemento de acuerdo a su parte derecha.
-	`bottom` \- `auto`, `length`: Define la posición del elemento de acuerdo a su parte inferior.

## Anexos

### Colores:

Hay diversas formas de determinar el color:

-	**Nombre**: aproximadamente hay 140 nombres con colores para revisar los nombres visitar [esta página](https://htmlcolorcodes.com).
-	**RGB**: Se puede poner un código rgb para determinar el color, indicando sus componentes rojo, verde y azul, en valores entre 0 y 255 cada uno, de la siguiente manera: <br> `color:rgb(r,g,b)`
-	**RGBA**: Es con código rgb con transparencia, la transparencia se define con un número entre 0 y 1 en el argumento _alpha_, siendo uno completamente opaco: <br> `color:rgba(r,g,b,alpha)`
-	**HSL**: Es un código donde se indican el _hue_, _saturation_ y _lightness_, _hue_ va de 0 a 360, donde 0 es rojo, 120 es verde y 240 es azul. _Saturation_ es un porcentaje de 0% a 100%, de gris a _full color_ y _lightness_ es un porcentaje de 0% a 100% de negro a blanco. Se ponen así tal cual, con el %: <br> `color:hsl(h,s,l)`
-	**HSLA**: Es con código _hsl_ con transparencia, la transparencia se define con un número entre 0 y 1 en el argumento _alpha_, siendo 1 completamente opaco.: <br> `color:hsl(h,s,l,alpha)`
-	**Hexadecimal**: Código hexadecimal, que son combinaciones de números de 0 al 9 y las letras de la A a la F, que representan los valores rojo, verde y azul, similar a rgb, por ejemplo: <br> `#rrggbb`
-	**Hexadecimal de 3 dígitos**: Existe una versión alterna a la forma hexadecimal con tres dígitos. Representa a los colores rojo, verde y azul, pero solo cuando ambos componentes de _rr_, _gg_ y _bb_ son los mismo, por ejemplo `#ff00cc` se podría representar como `#f0c`: <br> `color: #rgb`

### Lenght
Es un número seguido de una unidad. Formas de especificar longitudes y anchos:
-	**Longitudes absolutas**: Son longitudes fijas y aparecerán justo como se indiquen. Un número acompañado de una unidad, las unidades son:
	-	_pt_: Puntos
	-	_cm_: Centímetros
	-	_mm_: Milímetros.
	-	_in_: Pulgadas (1in = 96px = 2.54cm)
	-	_px_: Pixeles, es relativo al dispositivo. (1px = 1/96th of 1in)
	-	_pt_: Puntos (1pt = 1/72 of 1in)
	-	_pc_: Picas (1pc = 12 pt)
-	**Longitudes relativas**: Se especifica la longitud relativa a otra longitud:
	-	_em_: Relativo al tamaño de la fuente del elemento.
	-	_ex_: Relativo con la altura de la fuente actual (rara vez se usa).	
	-	_ch_: En relación con el ancho del "0" (cero).
	-	_rem_: En relación con el tamaño de fuente del elemento raíz. 	
	-	_vw_: En relación con el 1% del ancho de la ventana gráfica*. 	
	-	_vh_: En relación con el 1% de la altura de la ventana gráfica*.	
	-	_vmin_: En relación con el 1% de la dimensión más pequeña de la ventana gráfica*. 	
	-	_vmax_: En relación con el 1% de la dimensión más grande de la ventana gráfica*.	
	-	_%_: En relación con el elemento primario.
