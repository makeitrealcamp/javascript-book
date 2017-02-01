# Variables

Las variables son uno de los conceptos básicos de la programación y nos permiten almacenar información temporal que podemos usar más adelante en nuestros programas.

Crea un archivo llamado `variables.rb` y agrega lo siguiente:

```js
var name = "Germán"; // cámbialo por tu nombre
console.log("Hola " + name);
```

En este ejemplo estamos definiendo una variable con nombre `name` y le asignamos el valor "Germán" (o el valor que le hayas asignado). En la siguiente línea estamos utilizando concatenación de cadenas para mostrar la cadena de texto "Hola " seguido del valor que tenga en ese momento la variable `name`.

Las variables se crean con la palabra clave `var` seguido del nombre de la variable. Opcionalmente, le puedes asignar un valor a la variable utilizando el caracter igual y el valor que le quieras dar. El punto y coma (`;`) al final es opcional pero se considera una buena práctica tenerlo.

El nombre de una variable debe comenzar con `$`, `_` o una letra, y después puede contener letras, dígitos, `_` y `$`. Ejemplos de nombres válidos son:

```
name
$element
_trains
```

Ejemplos de nombres inválidos son:

```
443german    // no puede comenzar con un número
element&123  // el caracter & no es válido en el nombre
```

Las palabras reservadas de JavaScript no se pueden usar como nombres de variables.

Como buena práctica se recomienda empezar las variables con una letra en minúscula y, si el nombre se compone de varias palabras, capitalizar cada palabra después de la primera. Por ejemplo `videoTrascoder` o `firstName`.

Los nombres de las variables diferencian entre mayúsculas y minúsculas (p.e. `firstname` es diferente a `firstName`).

## La utilidad de las variables

Crea un archivo llamado `square.js` y escribe el siguiente código:

```js
console.log("El perímetro de un cuadrado de lado 5 es " + (5 * 4));
console.log("El área de un cuadrado de lado 5 es " + (5 * 5));
```

Al ejecutarlo debería aparecer lo siguiente:

```js
$ node square.js
El perímetro de un cuadrado de lado 5 es 20
El área de un cuadrado de lado 5 es 25
```

El problema con este código es que si quisiéramos calcular el perímetro y el área de un cuadrado de lado 10, o 20, tendríamos que modificar ese valor en varias partes del código. Podemos mejorarlo utilizando una variable:

```js
var side = 5;

console.log("El perímetro de un cuadrado de lado " + side + " es " + (side * 4));
console.log("El área de un cuadrado de lado " + side + " es " + (side * side));
```

Si ejecutas el código te debería dar el mismo resultado. La ventaja es que si quieres calcular el perímetro y el área de un cuadrado con otro tamaño solo debes cambiar el valor de la variable. Intenta con 18 (te debería dar 72 de perímetro y 324 de área) y después con 39.

## Cambiando el valor de las variables



## Variables sin valor

En programación es muy común declarar una variable sin un valor, quizá porque más adelante vamos a pedirle el valor al usuario, o simplemente porque el valor se lo vamos a asignar después.

Una variable declarada sin un valor va a tener el valor de `undefined`.

Abre la consola de NodeJS y escribe `var name;`, te debería aparecer la palabra `undefined debajo`:

```
$ node
> var name;
undefined
```

Si vuelves a escribir el nombre de la variable (ya no necesitas el `var`) vas a volver a ver `undefined`. Inténtalo!
