# Funciones

Eventualmente vas tener algunas líneas de código que necesitan ser ejecutadas varias veces y desde diferentes partes de tu programa. En vez de repetir el mismo código una y otra vez puedes crear una función (también se les conoce como procedimientos o métodos) e **invocarla** cada vez que necesites ejecutar ese trozo de código.

Crea un archivo llamado `methods.js` y escribe lo siguiente:

```js
function hello() {
  console.log("Hola Mundo");
}
```

Para definir un método usamos la palabra reservada `function`, le damos un nombre (en este caso `hello`), abrimos y cerramos paréntesis (`()`), abrimos corchetes (`{`), escribimos el cuerpo de la función (el código que queremos ejecutar cuando sea invocada), y por último cerramos los corchetes `}`.

Si ejecutamos este código no aparece nada en la pantalla:

```
$ node methods.js
```

Una característica de las funciones es que no son ejecutadas hasta que no las **invoquemos**. Modifiquemos nuestro programa para invocarla:

```js
function hello() {
  console.log("Hola Mundo");
}

hello(); // acá la estamos invocamos
```

En la última línea la estamos invocando. Si lo ejecutas ahora si debería aparecer "Hola mundo":

```
$ node methods.js
Hola mundo
```

## Parámetros

Las funciones pueden recibir cero o más parámetros (o argumentos). Piensa en los parámetros como **variables** que puedes utilizar dentro de la función. Utilizando parámetros podemos hacer una función reutilizable que salude a cualquier persona:

```js
function hello(name) {
  console.log("Hola " + name);
}

hello("Germán");
hello("David");
```

Si lo ejecutamos deberías ver lo siguiente:

```
$ node methods.js
Hola Germán
Hola David
```

Los parámetros se definen dentro de los paréntesis al declarar la función y se separan con coma.

## Retornando un valor

Opcionalmente puedes retornar un valor desde la función utilizando la palabra clave `return`. Podemos modificar la función `hello` para que en vez de imprimir con `console.log` retorne una cadena de texto:

```js
function hello(name) {
  return "Hola " + name;
}

var g1 = hello("Germán"); // podemos asignar el valor de retorno a una variable
console.log(g1);

// podemos llamar la función directamente en el parámetro de otra función.
console.log(hello("David"));
```

¿Notas la diferencia? En vez de hacer el `console.log` dentro de la función lo hacemos cuando la invocamos (de lo contrario no aparecería nada en pantalla).

En lo posible se recomienda retornar valores en vez de utilizar `console.log` dentro de las funciones. La razón es que hace la función más reutilizable. Ahora podemos utilizar esta función en otros contextos en donde no se utilice `console.log` para imprimir en la línea de comandos, como en una aplicación Web.

El `return` es la última línea que se ejecuta de una función, cualquier código que se encuentre después de esa línea será ignorado. Por ejemplo:

```js
function hello(name) {
  return "Hola " + name;
  console.log("Esto nunca se va a imprimir");
}
```

## Las partes de una función

Recapitulemos lo que hemos visto hasta ahora. La sintaxis de una función es la siguiente:

```js
function <name>([param1], [param2], ...) {
  // cuerpo de la función
  return <valor de retorno>;
}
```

Lo que debes tener en cuenta:

* La función se crea con la palabra clave `function`.

* El nombre de la función tiene las mismas reglas de nombramiento que las variables: debe comenzar con `$`, `_` o una letra, y después puede contener letras, dígitos, `_` y `$`.

* La función puede tener cero o más parámetros dentro de los paréntesis que van después del nombre.

* Piensa en los parámetros como variables que puedes utilizar en la función.

* Los valores de esos parámetros se definen cuando invocan la función.

* Cada parámetro debe tener un nombre de una variable válido. Recuerda que el nombre de una variable debe comenzar con `$`, `_` o una letra, y después puede contener letras, dígitos, `_` y `$`.

* Puedes retornar un valor desde la función utilizando la palabra clave `return`.

* El valor de retorno debe ser un tipo válido de JavaScript: un número, una cadena de texto, un booleano, un arreglo, etc.

* Puedes almacenar el valor de retorno de una función en una variable o puedes invocar la función como parámetro de otra función.

## Cajas negras

En muchas ocasiones es bueno pensar en funciones como cajas negras que reciben unos parámetros de entrada y genera un valor de salida (el valor de retorno).

## Ejemplo

Vamos a hacer una función que calcule el indice de masa corporal.
