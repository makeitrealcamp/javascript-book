# Tipos y Operadores

En este capítulo vamos a hablar sobre cadenas de texto, números y booleanos (verdadero o falso), que son tipos de datos básicos en JavaScript, y cómo realizar algunas operaciones básicas con ellos. Empecemos con las cadenas de texto.

## Cadenas de texto

Una cadena de texto es un conjunto de caracteres encerrados entre comillas simples (`'`) o dobles (`"`). Por ejemplo:

```js
"Texto entre comillas dobles"
'Texto entre comillas simples'
```

Eso es todo. Sin embargo, queremos mostrarte los tres errores más comunes que cometen los principiantes al definir una cadena de texto para que los tengas en cuenta y no los cometas:

1. Olvidarse de la comilla de cierre. Por ejemplo:

   ```
   "Hola mundo
   ```
2. Cerrar la cadena con la comilla incorrecta (p.e. abrir la cadena con comilla doble y cerrarla con comilla sencilla). Por ejemplo:

   ```
   "Hola mundo'
   ```
3. Insertar el mismo tipo de comillas dentro de la cadena de texto. Por ejemplo:

   ```
   "Y él dijo: "Hola Mundo""
   'Hol'a mundo'
   ```

Para solucionar el último error (punto 3) podemos encerrar la primera cadena entre comillas simples y la segunda entre comillas dobles para que funcione:

```js
"Hol'a mundo"
'Y él dijo: "Hola mundo"'
```

**Recuerda:** Lo importante es que el texto no contenga la comilla que se utilizó para definir la cadena.

Pero ¿qué pasa si tenemos un texto con comillas simples y dobles? En ese caso tendríamos que utilizar el caracter de escape `\` como en el siguiente ejemplo:

```js
'Y \'él dijo\': "Hola mundo"'
```

O

```js
"Y 'él dijo': \"Hola mundo\""
```

En el primer ejemplo escapamos con `\` las comillas simples porque con esas fue que encerramos el texto, mientras que en el segundo ejemplo escapamos las comillas dobles porque con esas fue que encerramos el texto.

### Imprimiendo una cadena de texto

Para imprimir una cadena de texto en la línea de comandos (o en la consola del navegador) utilizamos `console.log` como hicimos en el capítulo anterior:

```js
console.log('Y \'él dijo\': "Hola mundo"');
```

Si guardas esa línea en un archivo llamado `strings.js` y lo ejecutas, el resultado debería ser el siguiente:

```
$ node strings.js
Y 'él dijo': "Hola mundo"
```

### Concatenando cadenas

Es posible unir cadenas de texto con el operador `+`. Por ejemplo, abre la consola de NodeJS y ejecuta lo siguiente:

```js
console.log("Hola" + "Mundo" + "Cómo" + "Estás");
```

Deberías ver algo como esto:

```
$ node
> console.log("Hola" + "Mundo" + "Cómo" + "Estás");
HolaMundoCómoEstás
```

Fíjate que las palabras no se separan con espacio automáticamente, tenemos que agregar los espacios explícitamente:

```
$ node
> console.log("Hola " + "Mundo " + "Cómo " + "Estás");
HolaMundoCómoEstás
```

En este momento la concatenación de cadenas no es muy útil porque hubiesemos podido escribir todo el texto `"Hola Mundo Cómo Estás"` dentro de una sola cadena, pero a medida que veamos otros conceptos se va a volver cada vez más importante.

## Números

Crea un nuevo archivo llamado `numbers.js` con el siguiente código:

```js
console.log(1 + 2)
console.log(3 * 4 + 5)
console.log(8 / 2)
```

Si lo ejecutas deberías ver algo así:

```
$ node numbers.rb
3
17
4
```

Fíjate en la segunda línea del ejemplo. JavaScript sigue el mismo estandar que en matemáticas, y por lo tanto la multiplicación se ejecuta primero que la suma. Puedes cambiar el comportamiento con paréntesis. Por ejemplo, cambia la operación de la segunda línea por `3 * (4 + 5)`. El resultado ahora debería ser `27`.

A diferencia de las cadenas de texto, los números **no** se encierran entre comillas de ninún tipo (de lo contrario JavaScript los trata como texto y no como números). Por ejemplo, abre la consola de NodeJS y escribe `"1" + "2"`. El resultado ya no es `3`, es la cadena de texto `"12"`:

```
$ node
> "1" + "2"
'12'
```

**Debes tener cuidado al concatenar cadenas y hacer sumas**, porque los dos utilizan el mismo operador `+`. Por ejemplo, intenta lo siguiente en la consola de NodeJS:

```
$ node
> "1 + 2 es " + 1 + 2
'1 + 2 es 12'
> "1 + 2 es " + (1 + 2)
'1 + 2 es 3'
```

En el primer ejemplo JavaScript toma la cadena `"1 + 2 es "` y la concatena con `"1"`, luego concatena el `"2"`, y el resultado es `"1 + 2 es 12"`.

En el segundo ejemplo JavaScript realiza primero la operación `(1 + 2)`, que da `3`, y luego concatena la cadena `"1 + 2 es "` con ese `3`, por eso es que el resultado es ahora `"1 + 2 es 3"`.

### Comparaciones

Crea un nuevo archivo llamado `comparisons.js` y escribe lo siguiente:

```js
console.log(5 > 3) // mayor que
console.log(5 >= 3) // mayor o igual que
console.log(4 < 4) // menor que
console.log(4 <= 4) // menor o igual que
console.log(2 == 2) // igual a
console.log(2 != 2) // diferente de
```

Ejecuta el archivo, deberías ver algo así:

```js
$ node comparisons.js
true
true
false
true
true
false
```

A los operadorres `<`, `>`, `<=`, `>=`, `==`, `!=` se les llama **operadores lógicos** y se caracterizan porque retornan un valor booleano: verdadero (`true`) o falso (`false`).

Cómo ejercicio, agrégale a cada línea del ejemplo anterior un texto con su respectiva operación para que se vea de la siguiente forma cuando lo ejecutas:

```
$ node comparisons.js
5 > 3 es true
5 >= 3 es true
4 < 4 es false
4 <= 4 es true
2 == 2 es true
2 != 2 es false
```
