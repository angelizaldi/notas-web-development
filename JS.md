
# JS

Es un lenguaje para manipular los elementos de HTML y CSS. El código se pone dentro de las etiquetas `<script>` de HTML, la cual puede ir dentro de `<body>` o `<head>`. También se puede almacenar en archivos externos con la extensión _.js_ y usar dentro del documento HTML con la etiqueta  `<script>` y el atributo _src_. Se puede usar tantos `<script>` como sean necesarios. Es recomendado utilizar archivos externos.

Las sentencias en JavaScript se separan con ";". No es estrictamente necesario usarlo si cada sentencia se escribe en su propia línea, pero como quiera es buena práctica hacerlo.

<br>

## Impresión datos:

-   Escribir en un elemento HTML: `innerHTML`.
-   Escribir dentro del output de HTML: `document.write()`.
-   Escribir dentro de un alert box: `window.alert()`.  Muestra una ventana con un mensaje.
-   Escribir dentro de la consola del navegador: `console.log()`, se pueden poner varios objetos separados por coma, y se imprimirá como si estuvieran concatenados por un espacio.

<br>

## Solicitud de datos

Para solicitar al usuario ingresar datos, se puede usar la función `prompt()`.

<br>

## Incorporación en una página web:

Existen 3 formas de incorporar JS en una página web:

### Inline

Cualquier elemento de HTML puede recibir un script, sin embargo no es considerado una buena práctica escribir scripts de esta manera. Ejemplo de un script inline:

```html
<button  onclick="alert('Hello, world!')">Click  me!</button>
```
-   Los atributos donde se suelen escribir inline scripts son:
	-   `onclick`, `onload`, `onmouseover`, `Onmouseout`, `Onfocus`, `Onblur`.

<br>
    
### Script interno:

Son scripts que se suelen escribir dentro de los tags `<head>` o `<body>`, aunque lo más común es hacerlo en el body, y se escriben entre `<script> ... </script>`. Ejemplo:

```html
<script>  
	console.log('Welcome  to 30DaysOfJavaScript')  
</script>
```

<br>

### Script externo:

Son scripts que se suelen escribir dentro de los tags `<head>` o `<body>`, aunque lo más común es hacerlo en el body, y se escriben en el atributo  src del tag `<script> ... </script>`. Ejemplo:

```html
<script src="introduction.js"></script>
```
-   Se pueden insertar múltiples scripts de este tipo.

<br>

## Comentarios:

Para escribir comentarios se una línea usar `//`, para escribir comentarios de múltiples líneas usar `/* ... */`:

```js
// un comentario

/*
Comentario
de multiples
líneas
*/
```

---
## Operadores:

### Operadores aritméticos

| Operador | Descripción |
| --- | --- |
| `+` | Suma |
| `-` | Resta | 
| `*` | Multiplicación | 
| `**` | Exponenciación (ES2016) |
| `/` | División | 
| `%` | Módulo (Residuo) |
| `++` | Incremento |
| `--` | Decremento |

<br>

### Operadores de asignación: 

| Operador | Ejemplo | Igual que |
| --- | --- | --- |
| `=` | `x = y` | `x = y` |
| `+=` | `x += y` | `x = x + y` |
| `-=` | `x -= y` | `x = x - y` |
| `*=` | `x *= y` | `x = x * y` |
| `/=` | `x /= y` | `x = x / y` |
| `%=` | `x %= y` | `x = x % y` |
| `**=` | `x **= y` | `x = x ** y` |

<br>
 
### Operadores de comparación: 

| Operador | Descripción |
| --- | --- |
| `==` | igual a |
| `===` | Igual valor e igual tipo |
| `!=` | no es igual |
| `!==` | No es igual al valor o no es igual al tipo |
| `>` | mayor que |
| `<` | menor que |
| `>=` | mayor o igual que |
| `<=` | menor o igual que |
| `?` | operador ternario |

El operador ternario es como un _if-else_: 

```js
(condition) ? val_true: val_false 
```
- Dependiendo de si _condition_ es `true` o `false`, entonces se retorna `val_true` o `val_false`. 

<br>

### Operadores lógicos: 

| Operador | Descripción |
| --- | --- |
| `&&` | lógico Y |
| `||` | lógico O |
| `!` | lógico NO |

<br>

### Operadores bitwise 

| Operador | Descripción | Ejemplo | Igual que | Resultado | Decimal |
| --- | --- | --- | --- | --- | --- |
| `&` | AND | `5 & 1` | `0101 & 0001` | 0001 | 1 |
| `|` | OR | `5 | 1` | `0101 | 0001` | 0101 | 5 |
| `~` | NOT | `~ 5` | `~0101` | 1010 | 10 |
| `^` | XOR | `5 ^ 1` | `0101 ^ 0001` | 0100 | 4 |
| `<<` | _left shift_ | `5 << 1` | `0101 << 1` | 1010 | 10 |
| `>>` | _right shift_ | `5 >> 1` | `0101 >> 1` | 0010 | 2 |
| `>>>` | _unsigned right shift_ | `5 >>> 1` | `0101 >>> 1` | 0010 | 2 |

<br>
 
### Cadenas: 

Para concatenar cadenas de utiliza el símbolo `+` o `+=`: 

```js
string1 + string2 

string1 += string2 
```

<br>
 
### Jerarquia de operaciones: 

| Operador | Orden| Descripción | Ejemplo |
| --- | --- | --- | --- |
| `( )` | 21 | Agrupación de expresiones | `(3 + 4)` |
| `.` | 20 | Miembro | `object.name` |
| `[]` | 20 | Miembro | `object["name"]` |
| `()` | 20 | Llamada de función | `myFunction()` |
| `new` | 20 | Crear | `new Date()` |
| `++` | 18 | Incremento de postfijo | `i++` |
| `--` | 18 | Decremento de postfijo | `i--` |
| `++` | 17 | Incremento de prefijo | `++i` |
| `--` | 17 | Decremento del prefijo | `--i` |
| `!` | 17 | Lógico NO | `!(x==y)` |
| `typeof` | 17 | Tipo | `typeof x` |
| `**` | 16 | Exponenciación | `10 ** 2` |
| `*` | 15 | Multiplicación | `10 * 5` |
| `/` | 15 | División | `10 / 5` |
| `%` | 15 | Residuo de la división | `10 % 5` |
| `+` | 14 | Adición | `10 + 5` |
| `-` | 14 | Sustracción | `10 - 5` |
| `<<` | 13 | _Shift left_ | `x << 2` |
| `>>` | 13 | _Shift right_ | `x >> 2` |
| `>>>` | 13 | _Shift right (unsigned)_ | `x >>> 2` |
| `<` | 12 | Menor que | `x < y` |
| `<=` | 12 | Menor o igual que | `x <= y` |
| `>` | 12 | Mayor que | `x > y` |
| `>=` | 12 | Mayor o igual que | `x >= y` |
| `in` | 12 | Membresía | `"PI" in Math` |
| `instanceof` | 12 | Instancia de un objeto | `instanceof Array` |
| `==` | 11 | Igual que| `x == y` |
| `===` | 11 | Igual estricto | `x === y` |
| `!=` | 11 | Desigual| `x != y` |
| `!==` | 11 | Desigual estricto | `x !== y` |
| `&` | 10 | Bitwise AND | `x & y` |
| `^` | 9 | Bitwise XOR | `x ^ y` |
| `|` | 8 | Bitwise OR | `x | y` |
| `&&` | 7 | Logical AND | `x && y` |
| `||` | 6 | Logical OR | `x || y` |
| `??` | 5 | _Nullish Coalescing_ | `x ?? y` |
| `? :` | 4 | Operador ternario | `? "Yes" : "No"` |
| `+=` | 3 | Asignación| `x += y` |
| `/=` | 3 | Asignación| `x /= y` |
| `-=` | 3 | Asignación| `x -= y` |
| `*=` | 3 | Asignación| `x *= y` |
| `%=` | 3 | Asignación| `x %= y` |
| `<<=` | 3 | Asignación| `x <<= y` |
| `>>=` | 3 | Asignación| `x >>= y` |
| `>>>=` | 3 | Asignación| `x >>>= y` |
| `&=` | 3 | Asignación| `x &= y` |
| `^=` | 3 | Asignación| `x ^= y` |
| `|=` | 3 | Asignación| `x |= y` |
| `yield` | 2 | _Pause function_ | `yield x` |
| `,` | 1 | Coma| `5 , 6` |

<br>

---
## Keywords: 

| Keyword | Descripción |
| --- | --- |
| `var` | Declarar una variable. |
| `let` | Declarar una variable de bloque. |
| `const` | Declarar una constante de bloque. |
| `if` | Sentencia de control `if`. |
| `switch` | Sentencia de control `switch`. |
| `for` | Ciclo `for`. |
| `function` | Declara una función. |
| `return` | Retorna un valor de una función. |
| `try` | Implementa un manejador de error para un bloque de sentencias. |

<br>

### This: 

`this` se refiere a un objeto que depende de cómo fuera llamado o usado el _keyword_. 
- En un método de objeto, `this` hace referencia al objeto. 
- Por sí solo, `this` se refiere al objeto global. En un ventana de navegador se refiera a `<Window>`. 
- En una función, `this` se refiere al objeto global. En un ventana de navegador se refiera a `<Window>`.
- En una función, en modo estricto, `this` es `undefined`. 
- En un evento, `this` hace referencia al elemento (de HTML) que recibió el evento. 
- Métodos como `call()`, `apply()` y `bind()`, `this` puede referir a cualquier objeto. 

<br>
 
**Jerarquía para saber a qué objeto se refiere `this`**: 

| Precedencia | Objeto |
| --- | --- |
| 1 | `bind()` |
| 2 | `apply()` y`call()` |
| 3 | Método de objeto |
| 4 | Ambiente global |

<br>

### Objetos: 

| Operador | Descripción |
| --- | --- |
| `typeof` | Devuelve el tipo de dato de una variable. |
| `instanceof` | Devuelve `true` si un objeto es una instancia de un tipo de objeto. |

#### typeof 

Retorna el tipo de dato que es una variable o un valor. 
```js
// Verificar el tipo de dato de "x"
typeof x
```
- _x_ es una variable o valor.
- Los posibles valores que retorna son:
	- "string"
	- "number"
	- "boolean"
	- "undefined"
	- "object"
	- "function". 

Para ver si un objeto es del tipo `Array` usar el método `Array.isArray()`:

```js
// Verificar si "a" es un array
Array.isArray(a)
```
- _a_ es cualquier objeto.

Para otro tipo de datos como `Map`, `Set`, `Date`, etc. se puede usar la propiedad `.constructor` que retorna el constructor de todo tipo de variables: 

```js
// Verificar el tipo de dato de otra clase de objetos
x.constuctor 
```

<br>

#### instanceOf 

Verifica que un objeto sea una instancia de una clase específica: 
```js
// Verificar si obj es una instancia de type
obj instanceOf type 
```
- _type_ es el nombre de una clase, ya sea una estándar o una creada por el usuario.

> **Nota**: Las instancias de clases que son "clases hijas", también serán instancias de las clases padre.

<br>

---
## Tipos de datos. 

Existen 8 tipos básico en JavaScript, los primeros 7 se conocen como "primitivos", algunas características de los tipos primitivos y no primitivos: 
- `boolean`: Los valores `true` y `false`. 
- `null`: Una palabra clave especial que indica un valor nulo (no tiene valor). Como JavaScript distingue entre mayúsculas y minúsculas, null no es lo mismo que _Null_, _NULL_ o cualquier otra variante.
- `undefined`: Una propiedad cuyo valor no está definido. Las variables no inicializadas y las funciones que no retornan nada son `undefined`. 
- `number`: Un número entero o de coma flotante.  
- `bigint`: Un entero con precisión arbitraria.  
- `string`: Una secuencia de caracteres que representan un valor de texto.  
- `symbol`: Un tipo de datos cuyas instancias son únicas e inmutables. 
- `Object`: \-. 

### Clasificación de tipos de datos:

- **Primitivos**: No se pueden modificar* una vez creados (inmutables) y se pueden comparar entre sí usando operadores de comparación. 
- **No primitivos**: Se pueden modificar una vez creados y no se pueden comparar entre sí con operadores de comparación, sin embargo se puede verificar si hacen referencia al mismo objeto. 
- **Iterables**: Son objetos que se pueden iterar usando `for...of loop`:
	-   Arrays.
	-   Strings.
	-   Maps.
	-   Sets.
	-   _Generators_.
	-   _Async generators_.
	-   Objetos _Arguments_.
	-   NodeLists.
	-   Colecciones DOM.

*No confundir con que se puedan modificar las variables con tipos primitivos, es diferente. Por ejemplo: 
```js
let myString = "Hola" 

myString[0] = "B" // No se puede 

myString = "Adios" // Sí se puede 
```

<br> 

 ---
### number

Solo existe un tipo de dato numérico. Se escriben con o sin decimales. Se pueden escribir números con notación científica: 

```js
\\ Número sin decimales 
1000 

\\ Número con decimales 
1000.0 

\\ Números en notación científica 
10e3 
10e-3 
10E3 
10E-3 
```
- Todos los números en JS son _float64_. 

<br>
 
#### Números especiales: 

Algunos valores especiales son: 

- `NaN`: Representa que un objeto no es un número. 
- `infinity`: Para representar un número muy grande, también es el valor devuelto en operaciones indefinidas. 

> **Importante**: Para usar esos valores espaciales revisar las [propiedades](#propiedades-estáticas-de-number) de `number`. 

<br>

#### Propiedades estáticas de `number`: 

Para utilizar números especiales y otros valores usar las siguientes propiedades, directamente sobre el objeto `number`, no sobre las instancias: 

| Propiedad | Descripción |
| --- | --- |
| `number.MAX_VALUE` | Devuelve el mayor número posible en JavaScript |
| `number.MIN_VALUE` | Devuelve el número más pequeño posible en JavaScript |
| `number.POSITIVE_INFINITY` | Representa infinito (devuelto al desbordamiento) |
| `number.NEGATIVE_INFINITY` | Representa el infinito negativo (devuelto en el desbordamiento) |
| `number.NaN` | Representa un valor "_Not-a-Number_" |

> Para una lista completa visitar la  [documentación](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Number#static_properties).

<br>

**Ejemplo**: En este ejemplo se imprime el valor máximo posible:

```js
console.log(number.MAX_VALUE)
```

<br>

#### Métodos estáticos de `number`: 

Se aplican directamente sobre el objeto `number`. 

| Método | Descripción |
| --- | --- |
| `number.parseFloat()` | Analiza un argumento de cadena y devuelve un número de coma flotante. |
| `number.parseInt()` | Analiza un argumento de cadena y devuelve un entero de la base o radix especificada. |
| `number.isFinite()` | Determina si el valor pasado es un número finito. |
| `number.isInteger()` | Determina si el valor pasado es un número entero. |
| `number.isNaN()` | Determina si el valor pasado es NaN. |
| `number.isSafeInteger()` | Determina si el valor proporcionado es un número entero seguro. |

> Para una lista completa visitar la  [documentación](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Number#static_methods).

<br>

**Ejemplo**: En este ejemplo se verifica si un número es un entero:
```js
const x = 25.5
console.log(number.isInteger(x))
```

<br>

#### Métodos de instancia de `number`: 

Se aplican sobre instancias de `number`.

> Para una lista completa visitar la  [documentación](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Number#instance_methods).

<br>

- `number.toString(radix=10)` \- `string`: Retorna un número como una cadena.
	- **`radix`** \- `number`: Número del 2 al 36 para indicar la base numérica.

<br>

- `number.toFixed(digits)` \- `string`: Retorna un número como una cadena con un número específico de decimales.
	- **`digits`** \- `number`: Número de decimales a incluir en la cadena.

<br>

- `number.toPrecision(digits)` \- `string`: Retorna un número como una cadena con una longitud específica, agregando ceros si es necesario.
	- **`digits`** \- `number`: Número de decimales a incluir en la cadena.

<br>

- `number.toExponential(fractionDigits)` \- `number`: Retorna el número en notación exponencial.
	- **`fractionDigits`** \- `number`: Número de dígitos después del punto decimal.

<br>

---
### string

Es un objeto que representa cadenas de caracteres. Las cadenas de caracteres pueden escribirse dentro de comillas simples, dobles o _backsticks_. 

```js
// Todas las siguientes opciones son válidas para escribir una cadena
const foo = "my string 1" 
const bar = 'my string 2'
const baz = `my string 3`
```

Es posible crear una cadena con el _wrapper_ `String()`, pero no es necesario hacerlo de esta forma: 
```js
// Ejemplo usando String()
const foo = new String("foo"); 
```
 
Se puede dividir una cadena en múltiples líneas usando el operador de concatenación: 
```js
const foo = "una línea" + 
	"otra línea" 
```
 
Otra forma de hacer una cadena de múltiples líneas es con: 
```js
const foo = "una línea \ 
	otra línea" 
```

Las cadenas se pueden indexar usando corchetes y el índice del caracter: 
```js
// foo es string
foo[ind]
```
- _ind_ es el índice del carácter, comienza en cero. 
- Indexar cadenas no siempre funciona correctamente.

#### Cadenas unicode: 

Para crear cadenas con caracteres unicode usar `"\u"` seguido de al menos 4 dígitos hexadecimales, por ejemplo: 
```js
const foo = "\u00A9" 
```
- Para revisar los códigos unicode visitar [esta página](https://symbl.cc/en/unicode/table/).

#### Secuencias de escape: 

Para insertar una secuencia de escape usar: 

| Code | Result | Description |
| --- | --- | --- |
| `\'` | ' | Comilla simple |
| `\"` | " | Comilla doble |
| `\\` | \ | Barra invertida |
| `\b` |  | Retroceso |
| `\n` |  | Nueva línea |
| `\r` |  | Retorno de carro |
| `\t` |  | Tabulador horizontal |
| `\v` |  | Tabulador vertical |

*Notar que se puede usar " " y ' ' simultáneamente para poder escribir cadenas con comillas dobles o simples en una cadena. 

**Ejemplo**: En el siguiente ejemplo se utiliza la secuencia `"\n"`, así como se ejemplifica el uso de comillas simples y dobles de manera simultánea.

```js
// Uso de secuencias de escape
myString = 'La fórmula es: \n "E=mc**2"'
```

#### String Templates: 

Otra forma de definir una cadena es con _backsticks_, de esta forma es posible incluir variables en la cadena, así como definir cadenas en múltiples líneas: 

```js
// Multiples líneas con backsticks
const foo = `una línea \ 
	otra línea` 
``` 

Para incluir valores de variables en una cadena se utiliza `${...}`: 
```js
// Uso de template strings
const x = 2
const foo = `Dos al cuadrado: ${x**2}` 
``` 
- Dentro de los corchetes se pueden poner variables, cálculos, etc. 

 
#### Propiedades de instancia de `string`: 

- `string.length` \- `number`: Retorna la longitud de la cadena.

> Para más información visitar la  [documentación](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/String#instance_properties).

#### Métodos de instancia de `string`:

> Para una lista completa visitar la  [documentación](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/String#instance_methods).

##### Información:

- `string.includes(searchString, position=0)` \- `string`: Retorna `true` si la cadena contiene un patrón, en caso contrario retorna `false`.
	- `searchString` \- `string`: Cadena a buscar.
	- `position` \- `number`: Posición inicial desde donde buscar.

<br>

- `string.startsWith(searchString, position=0)` \- `string`: Retorna `true` si la cadena empieza por patrón, en caso contrario retorna `false`.
	- `searchString` \- `string`: Cadena a buscar.
	- `position` \- `number`: Posición inicial desde donde buscar.

<br>

- `string.endsWith(searchString, position=0)` \- `string`: Retorna `true` si la cadena empieza por patrón, en caso contrario retorna `false`.
	- `searchString` \- `string`: Cadena a buscar.
	- `position` \- `number`: Posición inicial desde donde buscar.

##### Subcadenas:

- `string.slice(start, end = -1)` \- `string`: Extraer parte de una cadena indicando su posición inicial y final.
	- `start`, `end` \- `number`: Posición inicial y final respectivamente, los índices comienzan en cero y end es exclusivo. Se pueden usar índices negativos para indicar desde el final de la cadena.

<br>

- `string.substring(start, end = -1)` \- `string`: Extraer parte de una cadena indicando su posición inicial y final.
	- `start`, `end` \- `number`: Posición inicial y final respectivamente, los índices comienzan en cero y end es exclusivo. No se pueden usar índices negativos.

<br>

- `string.charAt(indice)` \- `string`: Retorna el carácter en la posición indicada.
	- `indice` \- `number`: Índice del carácter, comienza en cero.

<br>

- `string.charCodeAt(indice)` \- `string`: Retorna el código UTF-16 del carácter en la posición indicada.
	- `indice` \- `number`: Índice del carácter, comienza en cero.

<br>

##### Buscar y reemplazar:


- `string.replace(regexp|substr, newSubStr|function, flags)` \- `string`: Devuelve una cadena reemplazando todas o algunas coincidencias de un patrón. No modifica la cadena sobre la cual se llamó al método, sino que retorna una nueva cadena.
	- `regexp|substr` \- `RegExp` o `string`: Patrón a reemplazar.
	- `newSubStr|function` \- `string` o `Function`: Cadena que reemplazará al patrón o una función para crear la nueva cadena.
	- `flags` \- `string`: Combinación de flags para modificar el comportamiento del método, algunas opciones son:
		- `g`: Para que reemplace todos los patrones encontrados.
		- `i`: Para ignorar mayúsculas.

<br>

- `string.search(regexp)` \- `number`: Retorna la posición de la primera coincidencia de un patrón, si no se encuentra retorna -1.
	- `regexp` \- `RegExp`: Regular expression a buscar.

<br>

- `string.match(regexp)` \- `object`: Retorna todas las coincidencias con un patrón en una cadena.
	- `regexp` \- `RegExp`: Regular expression a buscar.
	- El objeto retornado tiene como propiedades:
		- `Input`: Cadena donde se está buscando.
		- `Index`: índice donde se encontró la coincidencia.
		- `0`: Coincidencia encontrada.
		- `1, 2, ...`: Grupos capturados.

<br>

- `position=0]) [string.indexOf(searchString, [position=0])` \- `number`: Retorna la posición de la primera coincidencia de un patrón, si no se encuentra retorna -1.
	- `searchString` \- `string`: Cadena a buscar.
	- `position` \- `number`: Posición inicial desde donde buscar.

<br>

- `string.lastIndexOf(searchString, position=0)` \- `number`: Retorna la posición de la última coincidencia de un patrón, si no se encuentra retorna -1.
	- `searchString` \- `string`: Cadena a buscar.
	- `position` \- `number`: Posición máxima desde donde buscar.

<br>

##### Manipulación:

- `string.toUpperCase()` \- `string`: Convierte la cadena a mayúsculas.
	- No tiene argumentos.

<br>

- `string.toLowerCase()` \- `string`: Convierte la cadena a minúsculas.
	- No tiene argumentos.

<br>

##### Concatenación y splits:

- `string.concat(str1, str2, /* ..., */ strN)` \- `string`: Concatena dos o más cadenas y retorna una nueva. Se puede usar como alternativa del operador +.
	- `(str1, ..., strN` \- `string`: Cadenas a concatenar.

<br>

- `string.split(separator, limit)` \- `Array`: Retorna una cadena separada por un carácter en un array.
	- `separator` \- `string` o `RegExp`: Separador de la cadena.
	- `limit` \- `number`: Especifica el número máximo de _splits_ a realizar.

<br>

##### Trims y Pads:

- `string.trim()` \- `string`: Elimina los espacios en blanco a ambos extremos de la cadena.
	- No tiene argumentos.

<br>

- `string.trimStart()` \- `string`: Elimina los espacios en blanco al inicio de la cadena.
	- No tiene argumentos.

<br>

- `string.trimEnd()` \- `string`: Elimina los espacios en blanco al final de la cadena.
	- No tiene argumentos.

<br>

- `string.padStart(targetLength, padString)` \- `string`: Agrega un patrón al inicio de una cadena para que tenga una longitud deseada. El patrón se repetirá si es necesario.
	- `tagerLenght` \- `number`: Longitud deseada.
	- `padString` \- `string`: Cadena a agregar al inicio de la cadena. Si es muy grande se truncará.

<br>

- `string.padEnd(targetLength, padString)` \- `string`: Agrega un patrón al final de una cadena para que tenga una longitud deseada. El patrón se repetirá si es necesario.
	- `tagerLenght` \- `number`: Longitud deseada.
	- `padString` \- `string`: Cadena a agregar al final de la cadena. Si es muy grande se truncará.

### boolean: 

Un valor booleano puede representar dos valores, `true` o `false`. Todos los valores al ser evaluados como _bool_ se consideran `true` (truthy), excepto algunos cuantos, los valores que son evaluados como `false` (falsy) son: 
- Valor `false`. 
- Número cero (`0`). 
- Cadenas vacías (`''`). 
- Valor `undefined`. 
- Valor `null`. 
- Valor `NaN`. 

> **Importante**: arrays y objetos vacíos no se evaluan como `false`. 

### object: 

Es una lista de cero o más pares propiedad-valor. Se escriben entre llaves, cada elemento se declara en una par _property:"value"_. Los objetos se suelen declarar como constantes:
 
```js
// Plantilla básica de un objeto
const myObject = {property1: "value1", property2: "value2, ...}; 
```
- _myObject_ es el nombre del objeto. 
- _propertyi_ es el nombre de cada propiedad. Los nombres no son necesarios ponerlos como cadenas, pero también es posible hacerlo así, incluso puede ser una cadena vacía. 
- _valuei_: Es el valor de cada elemento, pueden ser de diferentes tipos incluso arrays, funciones u otros objetos. Si es numérico no es necesario ponerlo entre comillas.  
	- Si el valor es una función la propiedad será un tipo método. 

Otra forma de crear un objeto es con:
 
```js
let myObject = new Object() 
```

Es posible agregar nuevas propiedades y métodos de manera dinámica de la siguiente manera:
 
```js
myObject.new_property = value // Solo válido con nombres no complejos ni raros 

myObject.new_method = function(args) { expressions } 
```

#### Acceder a propiedades y métodos:

Para acceder a las propiedades de cada objeto usar:
 
```js
// Solo válido con nombres no complejos ni raros
myObject.property;  

 // Válido para nombres más complejos
myObject["property"]; 
```

Para acceder a los métodos de cada objeto usar: 
```js
objectName.method(args); 
```

#### Eliminar propiedades o métodos:

Para eliminar una propiedad o método se usa la palabra reservada `delete`:
 
```js
// Eliminar una propiedad
delete myObject.property; 

// Eliminar una propiedad
delete myObject["property"]; 

// Eliminar con base al índice
delete myObject[index]; 

// Eliminar un método
delete myObject.method; 
```

#### Verificar membresía:

Se puede usar el operador `in` para verificar que exista una propiedad en un objeto:
 
```js
// Verificar membresia
property in myObject
```
- _property_ tiene que ser `string`, `number` o `symbol`. 

Otra forma de verificar si un objeto tiene una propiedad específica es con el método `.hasOwnProperty()`. 
```js
// Verificar membresia
myObject.hasOwnProperty('name'): 
```
- _myObject_ es el nombre del objeto. 
- _name_ es el nombre de la propiedad que se quiere verificar si existe en _myObject_.

#### Desempacar:

Para desempacar objetos el nombre de las variables debe de ser el mismo que el nombre de las propiedades. 
```js
let {propName1, propName2, ...} = myObject 
```

Se pueden asignar valores por default a propiedades que se sabe que no existen en el objeto. 
```js
let {propName1, propName2, propName3 = "value", ...} = myObject 
```

Se puede renombrar las variables al momento de desempacar usando: 
```js
let {prop1: newName1, prop2: newName2, ...} = myObject 
```
 
Es posible desempacar un objeto incluso al llamar a una función: 
```js
// Definir objeto
const triangulo = { 
  base: 10, 
  altura: 20 
} 

// Definir función
const area = ({base, altura}) => { 
  return (base * altura) / 2
}

// Utilizar la función
console.log(area(triangulo)) 
```
- En este ejemplo, se puede pasar a la función un objeto que tenga las propiedades `base` y `altura`, automáticamente se desempacará.	 

#### Copiar objetos: 

Se puede usar operador _spread_ (`...`) para crear una copia de un objeto. 

```js
const persona = { 
  nombre: 'Juan',
  edad: 25, 
  nacionalidad: 'Mexicano'
} 

const copiaPersona = {...persona} 
```
- El valor de una propiedad se puede modificar usando: <br> `const copiaPersona = {...persona, property: newVal}`


#### Métodos: 

Los objetos también tienen métodos, se almacenan como propiedades cuyos valores son funciones.

```js
// Plantilla de como definir métodos en un objeto
const myObject = {..., methodName: function (args) {expresions}}; 
```
- Dentro de la definición de la función se puede usar `this.property` para acceder a las propiedades del objeto `myObject`. 

Para utilizar los métodos de un objeto usar: 

```js
objectName.methodName(args) 
```
- Si no se ponen los paréntesis retornará la definición del método (el código fuente del método). 

Se puede utilizar métodos de otros objetos en un objeto aparte siempre y cuando tengan la misma estructura (las mismas propiedades) usando `.call()` y `.apply()`: 
```js
// Utilizar un método en otro objeto
obj1.methodName.call(obj2)

// Utilizar un método con argumentos en otro objeto
obj1.method_name.call(obj2, arg1, arg2, …)  
```
- `methodName` es un método de _obj1_, pero se utilizará en _obj2_. 


El método `apply()` que es muy similar a `call()`, la única diferencia es que para pasar los argumentos del método en `apply()` se debe de hacer dentro de un `array`. 
```js
// Utilizar un método en otro objeto
obj1.methodName.apply(obj2) 

// Utilizar un método con argumentos en otro objeto
obj1.methodName.call(obj2, myArray)
```
- `methodName` es un método de _obj1_, pero se utilizará en _obj2_. 
- _myArray_ es un arreglo con los argumentos de `methodName`.

#### Métodos de object

> Falta agregar

### Arrays: 

Es un objeto especial que permite almacenar múltiples valores en una sola variable. Se escriben entre corchetes, separando los elementos con comas.
```js
// Plantilla básica de como declarar un array
const myArray = [val1, val2, ...]; 
```
- Es común que los arrays se declaren como constantes. 
- Los elementos del array pueden ser de diferentes tipos. 
- Se pueden dejar elementos vacíos, pero es recomendable indicar que se está dejando un elemento vacío con un comentario: <br> `const myArray = [val1, val2, /* empty */, ...];` 


Otra forma de crear un array en con  
```js
cont myArray = new Array(val1, val2, ...) 
```
- Lo anterior es igual a usar los corchetes `[]`. 

Se puede crear un array con elementos vacíos, pero de determinada longitud, con: 
```js
const myArray = new Array(num); 
```
- _num_ es un valor numérico entero.
 
#### Seleccionar elementos: 

Para seleccionar elementos de un array usar: 
```js
// Seleccionar elementos de un array
myArray[ind] 
```
- _ind_ es el índice del elemento. La indexación comienza en cero. 
- Para acceder al último elemento se puede usar: <br> `myArray[myArray.lenght - 1]`

 
#### Agregar y modificar elementos: 

Para agregar o modificar elementos simplemente seleccionar su índice y asignar un nuevo valor: 
```js
myArray[ind] = new_val 
```

#### Concatenar arrays:

Se puede usar el operador _spread_ (`...`), para crear un array que sea la concatenación de varios arrays: 
```js
// Definir arrays
const pares = [0, 2, 4, 6, 8] 
 
const impares = [1, 3, 5, 7, 9] 

// Concatenar arrays 
const enteros = [...pares, ...impares] 
``` 

#### Modificar longitud:

Se puede modificar la longitud de un array existente con:
```js
myArray.length = num 
```
- _num_ es un valor numérico entero.
- Si _num_ es menor al número de elementos actual, entonces se truncará el array. 
- Si _num_ es `0`, entonces se vaciará el array.	 

#### Desempacar: 

Para desempacar un `array` en varias variables usar: 
```js
Let [var1, var2, ...] = MyArray 
```
- El número de variables debe ser igual al número de elementos en el array. 
- Los elementos pueden ser otros arrays. 
- Si el número de variables es menor que el número de elementos en el array, entonces el resto de los elementos en el array se ignorarán. 
- Se puede omitir algún elemento con una coma: <br> `let [var1, ,var3, ...] = MyArray`
- Se puede asignar algún valor por default en caso de que el array tenga `undefined` o en caso de que algún índice no esté definido: <br> `let [var1, var2, var3, var4 = 'anything'] = MyArray` 
- Si se quiere asignar solo unas cuantas variables y el resto asignarlo a otro array usar: <br> `let [var1, var2, ...rest] = MyArray`

#### Iteración: 

Se puede iterar sobre los elementos del array usando un cíclo _for ... of_: 
```js
// Ejemplo de iteración de un array
const numeros = [1, 2, 3, 4, 5];  

for (const numero of numeros) {  

	console.log(numero);  

} 
```

> Revisar también los métodos de iteración. 

Alternativamente se puede iterar con los índices:

```js
const numeros = [1, 2, 3, 4, 5];  

for (let i=0; i<numeros.lenght; i++) {  

	console.log(numeros[i]);  

} 
``` 
- Para iterar el array de manera inversa usar: <br> `for (let i=numeros.lenght-1; i>=0; i--) {...}`

Se puede iterar sobre arrays anidados, donde cada elemento son del mismo tamaño de la siguiente manera: 

```js
for (const [ele1, ele2] of myArray) { 
		... 
	} 
```
- En este ejemplo, cada array interno es de dos elementos. 
- Si el número de variables es menor al número de elementos en los array internos, entonces solo se tomarán el número de variables, ignorando el resto. 

#### Crear copia de array: 

Se puede usar el operador _spread_ (`...`), para crear una copia de un array: 
```js
// definir el array
const vocales = ['a', 'e', 'i', 'o', 'u']

// crear copia
const letras = [...vocales] 
``` 

#### Arrays multidimensionales 

Se pueden crear array cuyos elementos sean otros arrays, para ello, cada elemento se debe indicar que es un array y posteriormente usar la notación [i][j] para ir llenando el array. Ejemplo para un array de dos dimensiones: 
```js
const a = new Array(4); 
for (let i = 0; i < 4; i++) { 

  // Indicar que cada elemento será un array de 4 elementos 
  a[i] = new Array(4); 
  for (let j = 0; j < 4; j++) { 

    // Ir llenando el array por "fila" y "columna". 
    a[i][j] = `[${i}, ${j}]`; 
  } 
} 
```

#### Propiedades de instancia de `Array`

- `Array.length` \- `number`: Retorna la longitud del array.

#### Métodos estáticos de `Array`

> Para una lista completa visitar la  [documentación](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Array#static_methods).

- `Array.from(arrayLike, mapFn, thisArg)` \- `Array`: Retorna un array desde cualquier objeto que tenga la propiedad `lenght` o un objeto iterable.
	- `arrayLike` \- `iterable` o `array-like`: Objeto el cual convertir a un array.
	- `mapFn` \- `Function`: Función a aplicar a cada elemento de `arrayLike`. La función debe de tomar los argumentos `element` e `index` y debe de retornar el elemento: <br> `function myFunction(element, index) { ... }`
	- `thisArg` \- `any`: valor a usar como `this` dentro de `mapFn`.

<br>

- `Array.isArray(value)` \- `boolean`: Indica si un objeto x es un array o no.
	- `value` \- `any`: Valor a verificar.

<br>

#### Métodos de instancia de `Array`

> Para una lista completa visitar la  [documentación](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Array#instance_methods).

##### Conversión:

- `Array.toString()` \- `string`: Convierte un array a una cadena, con los elementos separados por coma.
	- No tiene argumentos.

##### Agregar y eliminar elementos:

- `Array.push(element1, element2, /* …, */ elementN)` \- `number`: Agrega un elemento o varios al final del array in-place. Retorna la nueva longitud del array.
	- `element1, ..., elementN` \- `any`: Elemento o elementos a agregar al final del array.

<br>

- `Array.unshift(element1, element2, /* …, */ elementN)` \- `number`: Agrega un elemento o varios al inicio del array, recorriendo el resto de los elementos del array in-place. Retorna la nueva longitud del array.
	- `element1, ..., elementN` \- `any`: Elemento o elementos a agregar al inicio del array.

<br>

- `Array.pop()` \- `any`: Elimina y retorna el último elemento del array.
	- No tiene argumentos.

<br>

- `Array.shift()` \- `any`: Elimina y retorna el primer elemento del array, recorre el resto de los elementos una posición.
	- No tiene argumentos.

<br>

- `Array.splice(start, deleteCount, item1, item2, /* …, */ itemN)` \- `None`: Reemplaza, remueve o agrega elementos nuevos al array in-place.
	- `start` \- `number`: Índice desde el cual empezar a modificar el array.
	- `deleteCount` \- `number`: Entero que indicar cuántos elementos eliminar desde start. Por default son todos, desde start.
	- `item1, ..., itemN` \- `any`: Valores a agregar desde start. Si no se especifican solo se eliminarán.

<br>

##### Buscar elementos:

- `Array.indexOf(item, position=0)` \- `number`: Retorna la posición de la primera coincidencia de un valor, si no se encuentra retorna -1.
	- `item` \- `any`: Valor a buscar.
	- `position` \- `number`: Posición inicial desde donde buscar.

<br>

- `Array.lastIndexOf(item, position=0)` \- `number`: Retorna la posición de la última coincidencia de un valor, si no se encuentra retorna -1.
	- `item` \- `any`: Valor a buscar.
	- `position` \- `number`: Posición inicial desde donde buscar.

<br>

- `Array.includes(value)` \- `boolean`: Indica si un elemento está en el array.
	- `value` \- `any`: Valor a buscar.

<br>

- `Array.find(callbackFn, thisArg)` \- `any`: Retorna el primer elemento que cumple una condición. La función debe de retornar una condición que evalue a `true` o `false`.
	- `callbackFn` \- `Function`: Función a ser ejecutada una vez por cada elemento. Esa función tiene tres argumentos value, index y array, los cuales se pueden usar dentro de la función: <br> `function myFunction(value, index, array) {...}`.
	- `thisArg` \- `any`: valor a usar como `this` dentro de callbackFn.
	- No es necesario declarar la función con los tres.

<br>

- `Array.findIndex(callbackFn)` \- `number`: Retorna el índice del primer elemento que cumple una condición.
	- `callbackFn` \- `Function`: Función a ser ejecutada una vez por cada elemento. Esa función tiene tres argumentos value, index y array, los cuales se pueden usar dentro de la función: <br> `function myFunction(value, index, array) {...}`.
	- No es necesario declarar la función con los tres.

<br>

##### Concatenar y splits:

- `Array.concat(value1, value2, /* …, */ valueN)` \- `Array`: Concatena arrays o valores.
	- `value1, ..., valueN` \- `any`: Arrays o valores a concatenar.

<br>

- `Array.join(separator)` \- `string`: Convierte un array a una cadena, con los elementos separados por un separador.
	- `separators` \- `string`: Separador a usar.

<br>

##### Slice:

- `Array.slice(start = 0, end)` \- `Array`: Retorna una porción de un array indicando el principio y el final (exclusivo).
	- `start` \- `number`: índice desde el cual empezar a hacer el slice. Empieza en cero. Se pueden usar índices negativos para empezar desde un desplazamiento desde el final.
	- `end` \- `number`: índice en el cual terminar el slice, sin incluir este índice. Empieza en cero. Se pueden usar índices negativos para indicar un desplazamiento desde el final.

<br>

##### Ordenar

- `Array.sort()` \- `undefined`: Ordena un array de texto de manera ascendente in-place.
	- No tiene argumentos.
	- Para ordenar arrays numéricos de manera ascendente usar: <br> `X.sort(function(a, b){return a - b})`
	- Y de manera descendente: <br> `X.sort(function(a, b){return b - a})`
	- Para ordenar un array numérico de manera aleatoria (shuffle) usar: <br> `X.sort(function(a, b){return 0.5 - Math.random()})`

<br>

- `Array.reverse()` \- `undefined`: Modifica el orden del array de manera contraria in-place.
	- No tiene argumentos.

<br>

Para ordenar los objetos en un array:
```js
objArr.sort(function (a, b) {  
	if (a['key'] < b['key']) return -1  
	if (a['key'] > b['key']) return 1  
	return 0  
})
```

<br>

##### Rellenar:

- `Array.fill(value, start, end)` \- `Array`: Rellena con un valor desde una posición inicial hasta una posición final.
	- `value` \- `any`: Valor con el que se rellenará el array.
	- `start`, `end` \- `number`: Posición inicial y final respectivamente.

<br>

##### Máximos y mínimos:

No hay métodos built-in para encontrar valores extremos, pero se puede crear las siguientes funciones para encontrar tales valores:

**Máximo**:
```js
function myArrayMax(arr) {
	return Math.max.apply(null, arr);
}
```

**Mínimo**:
```js
function myArrayMin(arr) {
	return Math.min.apply(null, arr);
}
```

<br>

##### Iteración:

- `Array.forEach(callbackFn)` \- `undefined`: Llama a una función una vez por cada elemento en el array.
	- `callbackFn` \- `Function`: Función a ser ejecutada una vez por cada elemento. Esa función tiene tres argumentos `value` (elementos del array), `index` (índice del los elementos) y `array` (el array mismo), los cuales se pueden usar dentro de la función: <br> `function myFunction(value, index, array) {...}`
	- No es necesario declarar la función con los tres, pero `value` sí es obligatorio.

<br>

- `Array.keys()` \- `Iterator`: Retorna los elementos como un objeto iterable.
	- No tiene argumentos.

<br>

- `Array.entries()` \- `Iterator`: Retorna los elementos como un objeto iterable en un formato `index, value`.
	- No tiene argumentos.

<br>

##### Funciones

- `Array.map(callbackFn)` \- `Array`: Aplica a una función a cada elemento y retorna un array nuevo.
	- `callbackFn` \- `Function`: Función a ser ejecutada una vez por cada elemento. Esa función tiene tres argumentos value (elementos del array), index (índice del aray) y array (el array mismo), los cuales se pueden usar dentro de la función: <br> `function callbackFn (value, index, array) {...}`.
		- No es necesario declarar la función con los tres.

<br>

- `Array.filter(callbackFn)` \- `Array`: Crea un nuevo array solo con los elementos que cumplen cierta condición (evalua a true). La función debe de retornar el resultado de la condición.
	- `callbackFn` \- `Function`: Función a ser ejecutada una vez por cada elemento. Esa función tiene tres argumentos value (elementos del array), index (índice del value) y self (el array mismo), los cuales se pueden usar dentro de la función: <br> `function callbackFn (value, index, self) {...}`
		- No es necesario declarar la función con los tres.

<br>

- `Array.reduce(callbackFn, initialValue)` \- `number`: Itera sobre cada elemento, opera sobre ellos para reducirlos a un solo número.
	- `callbackFn` \- `Function`: Función a ser ejecutada una vez por cada elemento. Esa función tiene tres argumentos accumulator, currentValue e index, los cuales se pueden usar dentro de la función: <br> `function callbackFn (accumulator, currentValue, index) {...}`
		- No es necesario declarar la función con los tres.
	- `initialValue` \- `any`: Es el valor inicial que tendrá el accumulator en la primera iteración. Si no se específica será array`0`. No tiene que ser un número, pueden ser otros tipos como cadenas o arrays.

<br>

- `Array.reduceRight(callbackFn)` \- `number`: Itera sobre cada elemento, opera sobre ellos para reducirlos a un solo número, de derecha a izquierda.
	- `callbackFn` \- `Function`: Función a ser ejecutada una vez por cada elemento. Esa función tiene tres argumentos value, index y array, los cuales se pueden usar dentro de la función: <br> `function callbackFn (value, index, array) {...}`
		- No es necesario declarar la función con los tres.

<br>

- `Array.every(callbackFn)` \- `string`: Verifica que todos los elementos cumplan una condición, iterando elemento por elemento. La función debe de retornar una condición que evalue a `true` o `false`.
	- `callbackFn` \- `Function`: Función a ser ejecutada una vez por cada elemento. Esa función tiene tres argumentos value, index y array, los cuales se pueden usar dentro de la función: <br> `function callbackFn (value, index, array) {...}`
		- No es necesario declarar la función con los tres.

<br>

- `Array.some(callbackFn)` \- `string`: Verifica que algunos de los elementos cumplan una condición, iterando elemento por elemento. La función debe de retornar una condición que evalúe a `true` o `false`.
	- `callbackFn` \- `Function`: Función a ser ejecutada una vez por cada elemento. Esa función tiene tres argumentos value, index y array, los cuales se pueden usar dentro de la función: <br> `function callbackFn (value, index, array) {...}`
		- No es necesario declarar la función con los tres.

<br>

### Sets. 

Los _sets_ son una colección de valores únicos. Para crear un `Set` usar:
```js
const mySet = new Set([val1, val2, ...]) 
```
- Se puede pasar un `Array` al constructor `Set()`. Si el array tiene valores repetidos se eliminarán. 
- Se puede crear un `Set` vacío simplemente indicando el constructor. 

 
#### Iteración: 

Se puede iterar directamente sobre los elementos del set usando un cíclo `for ... of`: 
```js
for (const val of mySet) {  

	console.log(val);  

}
```
- La iteración respeta el orden de inserción.	 


#### Operaciones de sets: 

Existen de manera nativa métodos para realizar operaciones entre _sets_, pero a continuación se presentan unas alternativas.

> Para una lista completa visitar la  [documentación](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Set#instance_methods).

##### Unión: 

Para hacer la unión de _sets_, se tiene que hacer previo a tener los _sets_, es decir, se necesitan los objetos como _arrays_ y utilizar: 
```js
// Concatenar los arrays
let foo = [...a, ...b] 

// Convertir a Set el array foo
let MySet = new Set(foo) 
```
- _a_ y _b_ son `Array` previamente declarados e inicializados.

##### Intersección: 

Para hacer la intersección de _sets_, se tiene que hacer previo a tener los _sets_, es decir, se necesitan los objetos como _arrays_ y utilizar: 
```js
// Convertir a Set el array 'b'
let bar = new Set(b) 

// Filtrar el array 'a' con base al Set 'bar'
let foo = a.filter((val) => bar.has(val)) 

// Convertir a Set el array foo
let MySet = new Set(foo) 
```
- _a_ y _b_ son `Array` previamente declarados e inicializados. 

##### Diferencia: 

Para hacer la diferencia de _sets_, se tiene que hacer previo a tener los _sets_, es decir, se necesitan los objetos como _arrays_ y utilizar: 
```js
// Convertir a Set el array 'b'
let bar = new Set(b) 

// Filtrar el array 'a' con base al Set 'bar'
let foo = a.filter((num) => !bar.has(num)) 

// Convertir a Set el array foo
let MySet = new Set(foo) 
```
- _a_ y _b_ son `Array` previamente declarados e inicializados. 

#### Propiedades de instancia de `Set`

- `Set.size` \- `number`: Retorna la longitud del set. 

<br>

#### Métodos de instancia de `Set`

> Para una lista completa visitar la  [documentación](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Set#instance_methods).

- `Set.add(value)` \- `Array`: Agrega un elemento al set.
	- `value` \- `any`: Elemento a agregar al set.

<br>

- `Set.delete(value)` \- `string`: Elimina un elemento específico del set, retorna un valor booleano dependiendo si el valor estaba en el set o no.
	- `value` \- `any`: Elemento a eliminar del set.

<br>

- `Set.clear()` \- `string`: Elimina todos los elementos de un `Set`.
	- No tiene argumentos.

<br>

- `Set.has(value)` \- `string`: Retorna un valor booleano dependiendo si el valor está en el set o no.
	- `value` \- `any`: Elemento a buscar en el set.

<br>

- `Set.values` \- `Iterator`: Retorna un iterator con los valores del set.
	- No tiene argumntos.

<br>

- `Set.forEach(callbackFn, thisArg)` \- `undefined`: Llama a una función una vez por cada elemento en el set.
	- `callbackFn` \- `Function`: Función a ser ejecutada una vez por cada elemento. Esa función tiene tres argumentos value, index y array, los cuales se pueden usar dentro de la función: <br> `function callbackFn (value, key, set) {...}`.
		- No es necesario declarar la función con los tres.
	- `thisArg` \- `any`: valor a usar como `this` dentro de callbackFn.

<br>

### Maps.

Un _map_ contiene pares _key-value_, donde _key_ puede ser de cualquier tipo de dato (a diferencia de `object`, que debe de ser _string_ o _symbol_). Un `map` mantiene el orden como fueron insertados los elementos.
```js
const x = new Map() 
```
- Puedes pasar un `Array` al constructor `Map()`. El _array_ debe estar anidado, donde cada elemento sea otro _array_ con dos elementos, el primero será la llave y el segundo será el valor.
-Se puede crear un map vacío simplemente indicando el constructor. 

Se recomienda usar Maps sobre Objetos en los siguientes escenarios: 
- Utilizar `map` sobre `object` cuando las llaves son desconocidas durante el tiempo de ejecución, y cuando todas las llaves son del mismo tipo y todos los valores son del mismo tipo. 
- Utilizar `map` si es necesario almacenar valores primitivos como claves, ya que el objeto trata cada clave como una cadena, ya sea un valor numérico, un valor booleano o cualquier otro valor primitivo.
- Utilizar `object` cuando haya una lógica que opere en los elementos individuales. 

 
#### Iteración 

Para iterar por un `Map`, se puede usar el cíclo `for ... of`: 
```js
for (const [key, value] of map_name){ 
	// code block
}	 
```
- Se itera de acuerdo al orden de inserción.	 

También es posible iterar solo por las llaves: 
```js
for (const key of map_name){ 
	// code block
}	 
```

#### Propiedades de instancia de `Map`

- `Map.size` \- `number`: Retorna la longitud del _map_. 

<br>

#### Métodos de estáticos de `Map`

> Para una lista completa visitar la  [documentación](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Map#instance_methods)

#### Métodos de instancia de `Map`

> Para una lista completa visitar la  [documentación](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Map#static_methods)

- `Map.set(key, value)` \- `Map`: Agrega o actualiza valores en el map.
	- `key` \- `any`: Llave a agregar o actualizar.
	- `value` \- `any`: Valor de key.

<br>

- `Map.get(key)` \- `any`: Retorna el valor de una llave.
	- `key` \- `any`: Nombre de la llave.

<br>

- `Map.delete(key)` \- `Map`: Elimina un elemento específico del map, retorna un valor booleano dependiendo si el valor estaba en sel set o no.
	- `key` \- `any`: Elemento a eliminar del map.

<br>

- `Set.has(key)` \- `string`: Retorna un valor booleano dependiendo si la llave está en el map o no.
	- `key` \- `any`: Elemento a buscar en el set.

<br>

- `Map.entries()` \- `Iterator`: Retorna un iterator con los `key, value` del map.
	- No tiene argumentos.

<br>

- `Map.forEach(callbackFn, thisArg)` \- `None`: Llama a una función una vez por cada elemento en el map.
	- `callbackFn` \- `Function`: Función a ser ejecutada una vez por cada elemento. Esa función tiene tres argumentos value, index y array, los cuales se pueden usar dentro de la función: <br> `function callbackFn (value, key, set) {...}`.
		- No es necesario declarar la función con los tres.
	- `thisArg` \- `any`: valor a usar como `this` dentro de callbackFn.

<br>

### Date 

Permite trabajar con fechas y tiempo. Para crear una fecha se suele declarar como una constante de la siguiente manera: 
```js
const x = new Date() 
```
- `Date()` se puede especificar de las siguientes maneras: 
	- `new Date()`: Retorna la fecha y hora del navegador. 
	- `new Date(year, month, day)`: Se específica las partes individualmente, solo las partes de fecha. 
	- `new Date(year, month, day, hours, minutes, seconds, milliseconds)`: Se específica las partes individualmente.  
	- `new Date(milliseconds)`: Milisegundos desde 1/1/1970 (Unix epoch). 
	- `new Date(date-string)`: Cadena con una fecha. Algunos formatos de cadenas válidos son: 
		- `YYYY-MM-DDTHH:mm:ss.sssZ`: ISO, Los tiempos y zona horaria son opcionales. 
		- `MM/DD/YYYY` o `DD/MM/YYYY`: Dependiendo del formato local. 
		- `MMM DD YYYY` o `DD MMM YYYY`: En este caso los meses son nombres completos o abreviados, no sensibles a mayúsculas, no números. 

#### Métodos estáticos de `Date`

> Para una lista completa visitar la  [documentación](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Date#static_methods)

- `Date.now()` \- `number`: Devuelve el valor numérico correspondiente al actual número de milisegundos transcurridos desde el 1 de Enero de 1970.
	- No tiene argumentos.
	- La manera como se usa es: <br> `let date = new Date(Date.now())`;.

<br>

- `Date.parse(dateString)` \- `number`: Convierte una cadena que representa una fecha a milisegundos desde 01/01/1970.
	- `dateString` \- `string`: Cadena en ISO.

<br>

#### Métodos de instancia de `Date`

> Para una lista completa visitar la  [documentación](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Date#instance_methods)

##### Conversión:

- `Date.toString()` \- `string`: Retorna la fecha como cadena.
	- No tiene argumentos.

<br>

- `Date.toUTCString()` \- `string`: Retorna la fecha como cadena UTC.
	- No tiene argumentos.

<br>

- `Date.toDateString()` \- `string`: Retorna la fecha como cadena con mejor formato para lectura.
	- No tiene argumentos.

<br>

- `Date.toISOString()` \- `string`: Retorna la fecha como cadena en formato ISO.
	- No tiene argumentos.

<br>

##### Partes de fechas:

Los siguientes métodos retornan partes de una fecha, no tienen argumentos y todos retornan `number`. Se utilizan sobre instancias de `Date`.

| Método | Descripción |
| --- | --- |
| `.getFullYear()` | Recupera el año como un número de cuatro dígitos (_yyyy_) |
| `.getMonth()` | Recupera el mes como un número (0-11) |
| `.getDate()` | Recupera el día como un número (1-31) |
| `.getHours()` | Recupera la hora (0-23) |
| `.getMinutes()` | Recupera el minuto (0-59) |
| `.getSeconds()` | Recupera el segundo (0-59) |
| `.getMilliseconds()` | Recupera el milisegundo (0-999) |
| `.getTime()` | Recupera el _unix epoch_ (milisegundos desde el 1 de enero de 1970) |
| `.getDay()` | Recupera el día de la semana como un número (0-6) |

Los siguientes métodos se usan para trabajar con fechar UTC:

| Método | Descripción |
| --- | --- |
| `getUTCDate()` | Igual que `getDate()`, pero devuelve la fecha UTC. |
| `getUTCDay()` | Igual que `getDay()`, pero devuelve el día UTC. |
| `getUTCFullYear()` | Igual que `getFullYear()`, pero devuelve el año UTC. |
| `getUTCHours()` | Igual que `getHours()`, pero devuelve la hora UTC. |
| `getUTCMilliseconds()` | Igual que `getMilliseconds()`, pero devuelve los milisegundos UTC. |
| `getUTCMinutes()` | Igual que `getMinutes()`, pero devuelve los minutos UTC. |
| `getUTCMonth()` | Igual que `getMonth()`, pero devuelve el mes UTC. |
| `getUTCSeconds()` | Igual que `getSeconds()`, pero devuelve los segundos UTC. |

##### Establecer partes de fechas: 

Los siguientes métodos sirven para establecer una parte de una fecha ya existente, todos reciben como argumento `number` y son _in-place_, por lo que retornan `undefined`:

| Método | Descripción |
| --- | --- |
| `setDate()` | Establece el día como un número (1-31) |
| `setFullYear()` | Establece el año (opcionalmente mes y día) |
| `setHours()` | Establece la hora (0-23) |
| `setMilliseconds()` | Establece los milisegundos (0-999) |
| `setMinutes()` | Establece los minutos (0-59) |
| `setMonth()` | Establece el mes (0-11) |
| `setSeconds()` | Establece de los segundos (0-59) |
| `setTime()` | Establece la hora (milisegundos desde el 1 de enero de 1970) | 

### Math

Este objeto permite realizar operaciones matemáticas en números (`number`). 

#### Propiedades estáticas de `Math`:

> Para una lista completa visitar la  [documentación](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Math#static_properties)

| Propiedad | Descripción |
| --- | --- |
| `Math.E` | Devuelve el número de Euler |
| `Math.PI` | Devuelve el número Pi |
| `Math.SQRT2` | Devuelve la raíz cuadrada de 2 |
| `Math.SQRT1_2` | Devuelve la raíz cuadrada de 1 |
| `Math.LN2` | Devuelve el logaritmo natural de 2 |
| `Math.LN10` | Devuelve el logaritmo natural de 10 |
| `Math.LOG2E` | Devuelve el logaritmo base 2 de E |
| `Math.LOG10E` | Devuelve el logaritmo base 10 de E |

#### Métodos estáticos de `Math`

> Para una lista completa visitar la  [documentación](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Math#static_methods)

##### Redondeo:

Todos los métodos reciben `number` como argumento y retornan `number`.

| Método | Descripción |
| --- | --- |
| `Math.round(x)` | Devuelve un número redondeado a su entero más cercano. |
| `Math.ceil(x)` | Devuelve un número redondeado hacia arriba a su entero más cercano. |
| `Math.floor(x)` | Devuelveun número redondeado hacia abajo a su entero más cercano. |
| `Math.trunc(x)` | Devuelve la parte entera de `x` (nuevo en ES6). |

<br>

##### Misceláneos:

Todos los métodos reciben `number` como argumento y retornan `number`.

| Método | Descripción |
| --- | --- |
| `Math.power(x,y)` | Retorna `x` elevado a la `y`. |
| `Math.sqrt(x)` | Retorna la raíz cuadrada de `x`. |
| `Math.cbrt(x)` | Retorna la raíz cúbica de `x`. |
| `Math.abs(x)` | Retorna el valor absoluto de `x`. |
| `Math.sign(x)` | Retorna el signo de `x`, como -1, 0 o 1. |

<br>

##### Logaritmo y exponenciales:

Todos los métodos reciben `number` como argumento y retornan `number`.

| Método | Descripción |
| --- | --- |
| `Math.log(x)` | Retorna el logaritmo natural de `x`. |
| `Math.log(x)` | Retorna el logaritmo base 2 de `x`. |
| `Math.log(x)` | Retorna el logaritmo base 10 de `x`. |
| `Math.exp(x)` | Retorna e elevado a `x`, donde `x` es el argumento, y e es el número de Euler. |
| `Math.expm1(x)` | Retorna `exp(x)-1`. |

<br>

##### Mínimos y máximos:

Todos los métodos reciben `number` como argumento y retornan `number`.

| Método | Descripción |
| --- | --- |
| `Math.min(value1, value2, /* …, */ valueN)` | Retorna el valor mínimo de una serie de valores. |
| `Math.max(value1, value2, /* …, */ valueN)` | Retorna el valor máximo de una serie de valores. |

<br>

##### Números aleatorios:

Todos los métodos reciben `number` como argumento y retornan `number`.

| Método | Descripción |
| --- | --- |
| `Math.random()` | Retorna un número entre 0 y 1 (sin incluir el 1). |

Para retornar enteros aleatorios usar:
```js
// Retorna aleatorios entre 0 y N-1-
Math.floor(Math.random() * N); 
```

Para enteros entre dos números usar (incluye ambos extremos):
```js
function getRndInteger(min, max) {
	return Math.floor(Math.random() * (max - min) ) + min;
}
```
<br>

##### Trigonométricas:

Todos los métodos reciben `number` como argumento y retornan `number`.

| Método | Descripción |
| --- | --- |
| `Math.sin(x)` | Retorna el seno de `x`. |
| `Math.cos(x)` | Retorna el coseno de `x`. |
| `Math.tan(x)` | Retorna la tangente de `x`. |
| `Math.asin(x)` | Retorna el seno inverso de `x`. |
| `Math.acos(x)` | Retorna el coseno inverso de `x`. |
| `Math.atan(x)` | Retorna la tangente inversa de `x`. |

<br>

##### Trigonométricas:

Todos los métodos reciben `number` como argumento y retornan `number`.

| Método | Descripción |
| --- | --- |
| `Math.sinh(x)` | Retorna el seno hiperbólico de `x`. |
| `Math.cosh(x)` | Retorna el coseno hiperbólico de `x`. |
| `Math.tanh(x)` | Retorna la tangente hiperbólica de `x`. |
| `Math.asinh(x)` | Retorna el seno hiperbólico inverso de `x`. |
| `Math.acosh(x)` | Retorna el coseno hiperbólico inverso de `x`. |
| `Math.atanh(x)` | Retorna la tangente hiperbólica inversa de `x`. |

### JSON

JSON es un formato de texto basado en la sintaxis de los objetos de JavaScript, utilizado para almacenar y transportar datos. Se considera un tipo de dato semiestructurado. Las llaves de los objetos JSON deben de ir entre comillas

Debido a la similitud entre JSON y los objetos de JS, se pueden convertir uno al otro.

#### JSON a object

- `JSON.parse(json, reviver)` \- `object`: Convierte una cadena que represente un JSON a un objeto . 
	- `json` \- `string`: Cadena a convertir a objeto. 
	- `reviver` \- `function`: Una función para transformar los valores antes de construir el objeto. La función recibe dos argumentos _key_ y _value_. La función funciona iterativamente por cada valor _key-value_, y lo que debe de retornar es el nuevo valor que tendrá el _key_. 

<br>

#### object a JSON

- `JSON.stringify(obj, replacer, space)` \- `string`: Convierte un objeto a una cadena JSON.
	- `obj` \- `object`: Objeto a convertir a cadena.
	- `replacer` \- `Function` o `Array`: Modifica el output:.
		- `Array`: Si es un array debe de incluir los nombres de las propiedades que el output debe de tener. Los elementos en el array deben de ser cadenas o números.
		- `Función`: Una función para transformar los valores antes de construir el objeto. La función recibe dos argumentos _key_ y _value_. La función funciona iterativamente por cada valor _key-value_, y lo que debe de retornar es el nuevo valor que tendrá el _key_.
	- `space` \- `number` o `string`: Espacios a añadir para hacer leíble el JSON.
		- `number`: Número de espacios a usar como identación.
		- `string`: Cualquier carácter a usar para añadir espacios en blancos como '/t', '/n', ' ', etc. O cualquier carácter.

<br>

## Variables. 

Existen dos tipos de valores en JavaScript: 
- Variables: Valores que pueden cambiar a lo largo del programa. 
- Literales: Valores fijos, que no cambian de valor. 

Dependiendo del tipo de valor se utilizar diferentes _keywords_ para su declaración: 
- `var`: Una variable que sea compatible con navegadores antiguos, en genral no se recomienda usar. No tiene _block scope_ y pueden ser redeclaradas. No tienen que ser declaradas antes de usarlas, se recomienda como quiera declararlas al inicio del script. 
- `let`: Una variable. Tienen _block scope_ y no pueden ser redeclaradas (en el mismo bloque). Tienen que ser declaradas antes de usarlas. 
- `const`: Una literal. Tienen _block scope_ y no pueden ser redefinidas ni redeclaradas (en el mismo block). Se les debe de asignar un valor al ser declaradas, no posteriormente. Tienen que se declaradas antes de usarlas. Si es un array los elementos del array sí se pueden modificar, pero el array mismo no se puede redeclarar. 

### Declaración de variables: 

Las variables son contenedores de datos, hay diferentes formas de declarar una variable, se puede inicializar la variable desde que se declara o posteriormente (solo con `var` y `let`). 

```js
// Declarar e inicializar 
var x = val 
let x = val 
const x = val 

// Primero declarar, luego inicializar 
var x 
x = val 

// Primero declarar, luego inicializar 
let x 
x = val 
```
- Los nombres de las variables son sensibles a mayúsculas y minúsculas.  
- Los nombres de las variables deben empezar con una letra, el símbolo "\$" o guión bajo ("\_"), seguido por letras, números, "\$" o "\_". 
- Se recomienda usar "_camelCase_" para nombrar variables. 
- No se pueden usar _keywords_ como nombres. 
- Las variables no inicializadas tienen por default el valor `undefined`. 

Es posible declarar más de una variable en una sola línea separando por coma: 
```js
let varName1 = val1, varName2 = val2, ...
```

Para borrar el contenido de una variable usar: 
```js
var = undefined 
```

### Modo estricto: 

Es un modo para indicar que todas las variables debieron haber sido declaradas antes de usarlas, para ello usar lo siguiente al inicio del script. 
```js
"use strict" 
```
- Debe de ir entre comillas. 
- También se puede poner dentro de una función. 

### Conversión

Para convertir un tipo de dato a otro se puede utilizar funciones o JavaScript lo puede hacer automáticamente.

- `parseFloat(string)` \- `number`: Convierte una cadena a un valor numérico flotante.
	- `string` \- `string`: Cadena que contenga valores numéricos.

<br>

- `parseInt(string, radix)` \- `number`: Convierte una cadena a un valor numérico entero. Si se pasa un número flotante lo truncará al primer entero que encuentre.
	- `string` \- `string`: Cadena que contenga valores numéricos.
	- `Radix` \- `Numero`: Número entre 2 y 36 que representa la base del sistema numérico a convertir.

<br>

Otra técnica es utilizar el operador `+` antes de la cadena para poder hacer operaciones entre cadenas numéricas, por ejemplo:
```js
// Operaciones entre cadenas numéricas
+"1.1" + +"1.1"; // 2.2
```
<br>

- `String(x)` \- `string`: Convierte algo a una cadena. Es el constructor de `string`, la primer letra va en mayúscula.
	- `x` \- `number`, `Date`, `string`: Valor o expresión a convertir a cadena.

<br>

## Scopes.

Un _scope_ se refiere el ambiente en donde están disponibles las variables.

### Block scope:

Es un ambiente local que se define entre `{ }`, cualquier variable dentro del _block scope_ no es accesible fuera de él: 
```js
// Ejemplo de un block scope
{ 
	// block scope 
	let foo = "val" 
} 
```
- La variable _foo_ solo está disponible dentro del ambiente del bloque.

> **Importante**: Los _block scopes_ incluye a bloques como `if-else`, `for loops`, etc. 

> **Importante**: Solo `let` y `const` tienen _block scope_, si se declara una variable con `var` dentro de un _block scope_ si se puede acceder a su valor fuera de él. 

Es posible ponerle un nombre ([label](#labels)) a ese bloque de código usando: 
```js
// Nombrando un block scope
name: { 
	// block scope 
	expression 
} 
```

### Local scope: 

Es el ambiente dentro del cuerpo de las funciones. Las variables en este ambiente solo se pueden acceder dentro del mismo ambiente. 

```js
// Ejemplo de un block scope
function myFuction(){
	let foo = "val"
}
``` 
- La variable _foo_ solo está disponible dentro del cuerpo de la función.

### Global scope: 

Es el ambiente definido de manera general, afuera de cualquier función. Las variables globales son accesibles desde cualquier parte del script.

## Estructuras de control

### If-else 

Las sentencias condicionales se utilizan para realizar diferentes acciones dependiendo  de que se satisfagan determinadas condiciones. 

```js
// Plantilla básica de un bloque if-else if-else
if (condition){ 

	// code block 

} else if (condition){ 

	// code block 

} else { 

	// code block 
} 
```
- _condition_ son expresiones que resulten en un valor `boolean`. En JavaScript cualquier expresión automáticamente se evalua como `false` o `true`.  Revisar [Boolean](#boolean).

Recordar que se puede usar el operador ternario `?` para hacer un _if-else_ sencillo: 
```js
condition ? value_true:value_false 
```
- No es necesario escribir todo en una sola línea. 


### Switch:

Permite anidar varias sentencias _if-else_: 
```js
// Plantilla básica de switch
switch(expression) { 

	case a: 
	// code block 
	break; 

	case b: 
	// code block 
	break; 
	
	...

	default: 
	// code block 

} 
```
- Se evalua _expression_. Dependiendo del valor que haya tomado _expression_ se ejecuta el caso asociado. 
- Si no hay ninguna coincidencia se ejecuta el caso `default`. Este bloque es opcional. 

> **Importante**: Si no se pone la sentencia break, seguirá ejecutandose los siguientes casos. 


Si se requiere que dos o más casos compartan un bloque de código utilizar: 
```js
switch(expression) { 

	case a:
	case b: 
	// code block 
	break; 

	case c: 
	// code block 
	break; 
	
	...

	default: 
	// code block 

}
```
- En este ejemplo _a_ y _b_ comparten el mismo bloque de código. 

 
Si se quiere usar comparaciones en los casos, entonces dentro de swith se debe usar `true` y poner las comparaciones en cada caso: 
```js
switch(true) { 

	case comparisson1: 
	// code block 
	break; 

	case comparisson2: 
	// code block 
	break; 

	default: 
	// code block 
} 
```
- _comparissoni_ son expresiones que evaluadas resultan en valores booleanos. 

### For loop. 

Permite ejecutar un bloque de código cierta cantidad de veces
 
```js
// Plantilla básica de un ciclo for
for (begin;condition;step) { 
	// code block 
}
```
- _begin_ establece el valor inicial del iterador, por ejemplo: `let i=0`. Es posible declarar más de un valor, separándolos por coma. Se pueden declarar e inicializar afuera del _for loop_.
- _condition_ establece una condición de hasta cuando iterar, por ejemplo: `i<10`. 
- _step_ establece cómo incrementar el iterador, para ello se utilizan valores como `i++`, `i--`, `i+=2`, etc. Es posible llevar control del iterador dentro del código. 

#### Iterar un objeto
 
Otra forma de definir un _for loop_ es para que itere sobre las propiedades de un objeto. 
```js
for (let value in object){ 
	// code block 
} 
```
- _value_ se tiene que declarar con `let` o `const`. 
- Si _object_ es `object` iterará sobre los _keys_. 
- Si _object_ es `array` iterará sobre cada valor. <br> **Importante**: La iteración sobre arrays no sigue el mismo orden que el orden del array, por lo que si el orden importa podría haber resultados indeseados. Es preferible usar el método de iteración del array o usar un for of loop. 

#### Iterar un iterable
 
Otra forma de definir un for loop es para iterar sobre los valores de un iterable: 
```js
for (let variable of iterable){ 
	// code block 
} 
```
- _value_ se tiene que declarar con `let` o `const`. 
- _iterable_ es un objeto iterable, revisar [clasificación de tipos de datos](#clasificación-de-tipos-de-datos).
- Si _iterable_ es un array anidado, entonces se puede desempacar con una estructura similar a: <br> `for (const [val1, val2, ...] of iterable)`. 

#### Sentencias: 

Para cualquier tipo de _for loop_ existen dos sentencias para modificar el comportamiento del ciclo:
- `break`: Detiene la ejecución del ciclo. 
- `continue`: Detiene la ejecución de una iteración y pasa a la siguiente. 


### While loop. 

Permite ejecutar un bloque de código de manera iterativa mientras una condición sea verdadera:

```js
// Plantilla básica de un ciclo while
while (condition) { 

	// code block 

} 
```
- _condition_ es cualquier expresión que resulte en un valor `boolean`. 
- Si _condition_ depende de una variable ese valor se debe de actualizar dentro del bloque de código. 
- El bloque de código se ejecutará cero o más veces, dependiendo de si se cumple la condición. 

 
Si se requiere que el código se ejecute al menos una vez usar: 
```js
do { 

	// code block 

} 
while (condition) 
```
- _condition_ es cualquier expresión que resulte en un valor `boolean`. 
- Si _condition_ depende de una variable ese valor se debe de actualizar dentro del bloque de código. 
- El bloque de código se ejecutará cero o más veces, dependiendo de si se cumple la condición. 

#### Sentencias:

Para cualquier tipo de ciclo _while_ existen dos sentencias para modificar el comportamiento del ciclo:
- `break`: Detiene la ejecución del ciclo. 
- `continue`: Detiene la ejecución de una iteración y pasa a la siguiente. 

### Labels: 

Los _labels_ permiten etiquetar sentencias completas, y cada vez que se haga referencia al _label_, se estará haciendo referencia a toda la sentencia. Son particularmente útiles con las sentencias `break` y `continue` y _loops_ aninados, de tal forma que se pueda salir o pasar a la siguiente iteración del _loop_ externo desde el _loop_ interno: 

```js
// Ejemplo de uso de labels para salir de un for-loop anidado
outerLoop: for (let i = 0; i < 10; i++) {  
	innerLoop: for (let j = 0; j < 10; j++) {  
		if (i === 5 && j === 5) {  

			break outerLoop;  
		}  
	} 
}
``` 
- En este ejemplo se está usando el _label_ `outerLoop` para salir del _for loop_ externo desde el _for loop_ interno.

## Funciones:

Son un bloque de código que realiza cierta acción, que se ejecuta cuando es llamada, la sintaxis es:
```js
function functionName(args, ...) {
	expressions
	return  obj
}
```
-   `functionName` es el nombre de la función. Los nombres son sensibles a mayúsculas y minúsculas. El nombre debe empezar con una letra, el símbolo $ o guión bajo (\_), seguido por letras, números, $ o \_.
-   _args_ son los argumentos de la función separados por coma.    
-   La función se deja de ejecutar cuando llega a `return`.   Si no se indica qué objeto retornar se retorna `undefined` por default. 
-   Modificaciones en objetos y _arrays_ dentro de la función modifica los valores fuera de ella.    
-   Las funciones no necesariamente tienen que ser declaradas antes de usarlas.    
-   Para llamar a la función usar: <br> `functionName(args, ...)`

### Argumentos

Los argumentos de una función se almacenan automáticamente en un array llamado `arguments` el cual se puede utilizar para acceder a los argumentos por su posición en lugar de por su nombre

Se puede pasar una cantidad indeterminada de argumentos a una función con la sintaxis `...TheArgs`:
```js
// Ejemplo de uso de ...theArgs
function  multiply(multiplier, ...theArgs) {  
	return  theArgs.map((x) => multiplier * x);  
}
```
-   `TheArgs` será un array dentro de la función. No estrictamente se tiene que llamar de esa manera.
-   Este argumento se debe de poner al final de los parámetros y todos los argumentos que por posición no tengan un correspondiente parámetro formarán parte de  `TheArgs`.
-   Otra alternativa para pasar una cantidad indeterminada de argumentos es declarando la función sin ningún parámetro, y dentro de la función usar el objeto  `arguments`, para acceder a ellos.
 
### Funciones anónimas:

Son funciones con una sintaxis más simple, se suelen asignar a una variable.
```js
let var_name  = function (args){
	expression
};

// Posteriormente se puede usar esa  variable para llamar la funciones
var_name(args)
```

### Arrow functions

Son funciones anónimas  con una sintaxis abreviada:
```js
(args) => expression;
```
-   Automáticamente se retornará  _expression_.
-   Es válido si la función solo tiene una sentencia.
-   Si la función solo tiene un argumento no es necesario poner los paréntesis.
-   Si la función no tiene argumentos poner los paréntesis vacíos.
-   Se pueden pasar una cantidad indeterminada de argumentos con el operador spread (`...theArgs`), el cual se usará como un _array_ dentro de la función.
-   No tiene `this`, `arguments`, `super` o `new.target`.
-   Si se requiere que la función tenga más de una expresión usar llaves:
```js
(args) => {
	expressions
	...
}
```

Si es necesario que la función tenga nombre se puede asignar a una variable de la siguiente manera:
```js
const  my_arrow_function = (args) => expression;
```
-   En lugar de `const`, se puede usar `let`.
-   Posteriormente se puede usar el nombre para llamar la función: `my_arrow_function(args)`.
    

### JSDoc  Comments:

Estos bloques de comentarios se utilizan con fines de documentación y, a menudo, se denominan "comentarios JSDoc". Estos bloques de comentarios se colocan inmediatamente antes de la función o método que describen.

Los elementos que lo conforman:
- `/** ... */`: Esta sintaxis se usa para iniciar un bloque de comentarios multilínea en estilo JSDoc. 
- `* ...`: Cada línea dentro del bloque de comentarios comienza con un asterisco (*) seguido de la descripción o anotación.
- `@param`: Esta anotación se utiliza para describir los parámetros de la función. Incluye el nombre del parámetro, su tipo y una descripción de lo que representa.
- `@returns`: Esta anotación (no utilizada en el ejemplo proporcionado) se puede utilizar para describir el tipo de retorno de la función y lo que devuelve la función.
- `@description`: Esta anotación (que tampoco se utiliza en el ejemplo proporcionado) se puede utilizar para proporcionar una descripción de alto nivel de lo que hace la función.
    
Ejemplo:
```js
/**
* Descripción de la función.
* @param {datatype} argName1 - Descripción del argumento.
* @param {datatype} argName2 - Descripción del argumento.
...
* @returns {datatype} - Descripción del valor retornado.
*/
function  myFuncition(args) {
	// fuction  body
}
```

### Closures.

Los closures son funciones anidadas cuya función interna conserva acceso a las variables de su función contenedora incluso después de que esta última ha terminado de ejecutarse. Para que un _closure_ sea útil la función interna debe ser retornada (preferentemente, para conservar el _closure_) o llamada  por la función externa en algún momento, aunque por definición no es necesario que esto sea así, basta con que se utilicen variables de la función externa en la función interna para que sea un _closure_.

Las variables y funciones definidas en la función externa vivirán más tiempo que la duración de la ejecución de la función externa, si la función interna logra sobrevivir más allá de la vida de la función externa. Un _closure_ se crea cuando la función interna se pone de alguna manera a disposición de cualquier alcance fuera de la función externa.
```js
function  outerFunction() {
	var  outerVariable = 'Soy una variable de la función externa';
		function  innerFunction() {
			console.log(outerVariable);
			}
	return  innerFunction;
}

var  closureExample = outerFunction();

// Retorna: "Soy una variable de la función externa"
closureExample(); 
```
- Para que un _closure_ efectivamente sea preservado el resultado de la función externa se debe de asignar a una variable y posteriormente usar esta variable como una función como se nota en el ejemplo. 
- Notar que lo anterior captura la esencia de los _closure_, a pesar de que la función externa ya se ejecutó, la función interna (conservada en la variable `closureExample `) sigue teniendo acceso a las variables de la función externa independiente de en qué momento se llama a la función interna. Lo anterior solo aplica si la función externa retorna a la función interna.
-   Si la función interna es retornada por la función externa: Se genera un _closure_ diferente cada vez que se asigna el resultado de la función externa a una variable y esos _closures_ se almacenan en memoria.
-   Si la función interna no es retornada por la función externa: Se libera la memoria de los _closure_ al terminar la ejecución de las funciones internas.
    
En caso de que ambas funciones tengan argumentos, para pasarlos se puede hacer de las siguientes maneras:
```js
function  outside(x) {  
	function  inside(y) {  
		return x + y;  
	}  
return  inside;  
}  

// Se define primero la externa y luego la interna  
const fnInside = outside(3); 
console.log(fnInside(5)); // 8

// Se define ambas al mismo tiempo  
console.log(outside(3)(5)); // 8
```

#### Closures anidados.

En funciones anidadas de más niveles, las funciones internas tienen acceso a todas las variables de las funciones superiores a ella. En caso de que haya variables con mismos nombres, entonces las variables más internas tienen preferencia sobre las variables más externas.

### Funciones callback.

Son funciones que se utilizan como argumento de otra función y desde esa otra función se llama a la función.

#### setTimeout

`setTimeout(functionRef, delay)`: Es una función especial que ejecuta una función después de cierto tiempos.
- `functionRef`  es el nombre de la función que se ejecutará. 
- `delay` es el número de milisegundos que pasará antes de ejecutar la función.
- En caso de que la función tenga parámetros se deben de pasar después del argumento `delay`.

#### setInterval

`setInterval(func, time)`: Es una función especial que ejecuta una función cada cierto tiempo.
-   `func` \- `Function` o `string`:  es el nombre de la función que se ejecutará. Opcionalmente, en lugar de pasar una función, se puede pasar una cadena con código, el cual será ejecutado en cada intervalo.
-  `delay` \- `number` es el intervalo en milisegundos que se pasará entre cada ejecución de la función.
- En caso de que la función tenga parámetros se deben de pasar después del argumento `delay`.


## Clases.

Posee atributos y métodos, un objeto es una instancia de una clase. Para crear clases se usa
```js
class ClassName{
	attri = val
	...

	constructor(args){
		this._attr1 = val;
		...
	}

	get getName(args){}

	set setName(args){attr = val}

	methodName(args){expressions}
		...
	}
```
-   Los atributos se suelen nombrar con un guion bajo al principio.

### Crear instancias:

Para crear una instancia de una clase usar:
```js
let myObject = new ClassName(attrs);
```
-   Automáticamente se manda a llamar el constructor de la clase.
    

### Métodos

Son acciones que pueden realizar las instancias de una clase. Se definen como funciones dentro de la clase, sin la palabra clave function:
```js
class ClassName{

	...

	methodName(args){
		// method body
	}
	...
}
```

#### Constructor:

El _constructor_ es un método especial, que es llamado automáticamente al crear una instancia de una clase. Un constructor tiene una sintaxis similar a la de una función, el cual puede recibir parámetros y definir valores a las propiedades del objeto.  El constructor generalmente se utiliza para:
-   Inicializar las propiedades de las instancias con valores
-   Validar los valores de las propiedades
-   Crear referencias a otros objetos (como conectarse con una base de datos)
    

Sintaxis
```js
constructor(arg1, arg2) {  
	this.property1 = arg1  
	this.property2 = arg2
	...  
}
```
- `this` es un objeto especial que hace referencia a la instancia que se está creando.
- Los parámetros pueden tener valores por default.
- Las propiedades no tienen porque estrictamente tomar los valores de los argumentos, pueden ser operaciones entre los argumentos y otras manipulaciones.

#### Métodos _set_ y _get_:

Son métodos especiales para recuperar o establecer los valores de las propiedades de un objeto:

- `get get_name(args){return this.property}`
- `set set_name(args){this.property  = val}`
	-   No estrictamente  se tiene que asignar  un valor, por  ejemplo, si  la propiedad es un array, se puede  agregar  elementos, en  lugar de asignar  valores.
	- Para utilizar estos métodos no es necesario usar paréntesis al llamarlos. <br> `obj.get_name` <br> `obj.set_name = val`


#### Método estáticos:

Son métodos que se utilizan directamente sobre las clases, y no sobre las instancias/objetos. Para crear un método estático utilizar la _keyword_ `static` antes del método.
```js
static methodName(args) {
	// method body
}
```
-   No necesariamente tienen que recibir argumentos.
-   Como argumento se puede recibir una instancia/objeto.
-   Para llamar al método usar: <br> `className.method_name(args)`
    

### Atributos estáticos:

Son atributos exclusivos de la clase, pero no de las instancias/objetos. Para crear una propiedad estática utilizar la _keyword_ `static` antes del nombre de la propiedad.
```js
static attrbName = val
```
- Para acceder al valor del atributo usar: <br> `className.attrName`

### Herencia:

**Importante**: Todas las clases automáticamente heredan las clases y atributos de la clase _object_.

La herencia es útil para acceder a todas las propiedades y métodos de una clase padre. Para heredar los atributos y los métodos de una clase a otra usar:
```js
class ChildClass extends ParentClass {

	constructor(parentArgs, newArgs, ...){
		super(parentArgs)
		this._arg1 = val
		// constructor body
	}

}
```

### Sobreescritura:

En una clase hija se puede modificar el comportamiento de un método de la clase padre, se tiene que usar el mismo nombre y los mismos argumentos:
```js
metod_parent(args){
	super.parentMethod
	// method body
}
```
-   `parentMethod` es el nombre del método en la clase padre, con `super.method_parent` se llama a ese método y después se pueden agregar más cosas.
    

## RegExp.

Una expresión regular es una secuencia de caracteres para formar un patrón de búsqueda. La sintaxis es:
```js
const re =  /pattern/flags
```
- El patrón se pone entre `/`, _pattern_ se refiere a el patrón a usar, si además se quieren agregar _flags_, entonces se deben de poner después del último `/`, no importa que sea más de una _flag_.
- **Importante**: No se pone entre comillas, no es una cadena.
    

Otra forma de construir una expresión regular es con:
```js
const re = new RegExp("pattern");

const re = new RegExp("pattern", "flags");
```
-   Utilizar esta forma cuando el patrón se estará modificando durante el programa  o cuando no se conoce con antelación el patrón.
-   En flags van todas las flags a usar en la misma cadena.
- En este paso tanto el patrón como las banderas sí son cadenas.
    

Para utilizar metacaracteres de manera literal como parte del patrón usar `\`, antes del metacaracter, por ejemplo:
```js
const re =  /a\*b/
```
- En este ejemplo se está escapando el carácter `*`, para que el patrón incluya un asterisco literalmente.

### Flags

| Flag | Descripción | Propiedad correspondiente |
| --- | --- | --- |
| `d.` | Generar índices para coincidencias de subcadenas. | `hasIndices`. |
| `g.` | Búsqueda global. | `global`. |
| `i.` | Búsqueda sin distinción entre mayúsculas y minúsculas. | `ignoreCase`. |
| `m.` | Permite que ^ y $ coincidan con caracteres de nueva línea. | `multiline`. |
| `s.` | Permite que "." coincida con una nueva línea. | `dotAll`. |
| `u.` | "Unicode"; tratar un patrón como una secuencia de dígitos de código Unicode. | `unicode`. |
| `v.` | Una actualización al modo u con más características Unicode. | `unicodeSets`. |
| `y.` | Realice una búsqueda "sticky" que coincida a partir de la posición actual en la cadena de destino. | `sticky`. |

### Métodos de instancias de `RegExp`

Para usar cualquiera de los métodos siguientes primero se tuvo que haber definido el patrón . O aplicarlo directamente sobre el patrón:
```js
const myRe = /d(b+)d/g;  
// Sobre el objeto
const myArray = myRe.exec("cdbbdbsbz");

// Sobre el patron
const myArray = /d(b+)d/g.exec("cdbbdbsbz");
```
-   Tanto `MyArray` como `MyRe` tendrán unas propiedades especiales que se resumen más adelante.


- `RegExp.test(str)` \- `string`: Indica si un patrón está en una cadena.
	- `str` \- `string`: Cadena donde buscar el patrón.

<br>

- `RegExp.exec(str)` \- `Array`, `null`: Retorna las coincidencias de un patrón en una cadena.
	- `str` \- `string`: Cadena donde buscar el patrón.
	- El array que se retorna tiene propiedades extras como index, input e índices (si se estableció la flag d).

<br>
