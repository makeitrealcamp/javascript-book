# Primeros Pasos

En este libro vas a aprender las bases de JavaScript, que te serán útiles sin importar qué camino desees tomar más adelante, ya sea convertirte en Desarrollador Front End, Backend y/o Móvil.

En este capítulo vamos a ver cómo ejecutar código JavaScript tanto en el navegador como en [NodeJS](https://nodejs.org/en/), pero para la mayoría de ejemplos más adelante nos vamos a concentrar en [NodeJS](https://nodejs.org/en/) únicamente. La razón es que, incluso si tu objetivo es convertirte en Desarrollador Front End, vas a necesitar [NodeJS](https://nodejs.org/en/) para automatizar tareas de desarrollo y definir dependencias a librerías que utilices desde tus proyectos, así que vale la pena familiarizarse con esta plataforma desde ahora.

Por último, nuestra recomendación es que transcribas y ejecutes cada uno de los ejemplos de este libro en tu computador e intentes solucionar cada uno de los ejercicios de forma que aceleres tu aprendizaje. Recuerda que la mejor forma de aprender sobre programación es escribiendo código.

## Requisitos

Para sacar el mayor provecho de este libro necesitas saber qué es la línea de comandos (también conocida como consola, terminal o símbolo del sistema), cómo abrirla y cómo navegar por las carpetas de tu computador. Si aún no estás familiarizado con la línea de comandos te recomendamos [este post en el blog de Make it Real](http://blog.makeitreal.camp/la-linea-de-comandos/) que te brinda una introducción y te indica algunos recursos que puedes consultar si quieres más información.

Para seguir los ejemplos de este libro vas a necesitar tener instalado [NodeJS](https://nodejs.org/en/) y un editor de texto como [Atom](https://atom.io/), [Sublime Text](https://www.sublimetext.com/) o el de tu preferencia. Si no tienes un editor de preferencia nuestra recomendación es que instales [Atom](https://atom.io/).

Aunque lo más probable es que aún no tengas instalado [NodeJS](https://nodejs.org/en/) en tu máquina, verifica igual abriendo una línea de comandos y ejecutando `node -v`. Si ya lo tienes te va a aparecer una línea similar a la siguiente:

```
$ node -v
v7.0.2
```

La versión puede ser diferente, y cualquier versión mayor a 5.0.0 está bien.

Si ves un mensaje diciendo que el comando no fue encontrado, significa que aún no lo tienes instalado. Puedes encontrar las instrucciones para instalarlo en el siguiente enlace: https://github.com/makeitrealcamp/node-installation.

Una vez que tengas instalado [NodeJS](https://nodejs.org/en/) y lo hayas verificado, continúa. En las siguientes secciones vamos a ver cómo ejecutar código JavaScript tanto en el navegador como en [NodeJS](https://nodejs.org/en/).

## Ejecutando JavaScript en el navegador

Existen dos formas de ejecutar código JavaScript en los navegadores: a través de las herramientas de desarrollador que trae el navegador y creando un archivo HTML que incluya código JavaScript.

### A través de las herramientas de desarrollador

Las herramientas de desarrollador (en inglés developer tools) son un conjunto de herramientas integradas al navegador que utilizan los Desarrolladores Front End para analizar, depurar y mejorar su código.

La forma más fácil de abrir las herramientas de desarrollador en cualquier navegador es hacer click en cualquier parte de la página y seleccionar la opción "Inspeccionar Elemento" en el menú desplegable que aparece.

También existe un atajo del teclado para abrir y cerrar las herramientas de desarrollador. El atajo para la mayoría de navegadores en Mac es `Alt` + `Command` + `I`. Para PC es `Ctrl` + `Shift` + `I`.

Una de las herramientas que incluyen las herramientas de desarrollador es la **Consola**, que la puedes abrir haciendo click en la pestaña "Consola" (o en Inglés "Console") como se muestra en la siguiente imagen.

![Herramientas de Desarrollador](images/developer-tools.jpg)

En la **Consola** podemos escribir una expresión de JavaScript, oprimir Enter, y ver el resultado de esa expresión en la siguiente línea. Por ejemplo, escribe `1+2` y oprime Enter. Deberás ver el número `3` en la siguiente línea como se muestra en la siguiente imagen.

![La Consola](images/developer-tools-console.jpg)

### A través de un documento HTML

La otra forma de ejecutar código JavaScript en el navegador es dentro de un documento HTML. Crea un archivo llamado `index.html` y pega el siguiente contenido:

```html
<!DOCTYPE html>
<html>
  <head>
    <title>Ejemplo JavaScript</title>
  </head>
  <body>
    <script>
      alert("Hola Mundo");
    </script>
  </body>
</html>
```

Ábrelo con tu navegador preferido. Deberías ver un mensaje de alerta con el texto "Hola Mundo".

Aunque insertar el código directamente dentro del HTML funciona, se considera una mala práctica. Crea un nuevo archivo llamado `app.js` en la misma carpeta donde se encuentre `index.html` y pega el siguiente contenido:

```js
alert("Hola Amigo");
```

Ahora modifica `index.html` con el siguiente contenido:

```html
<!DOCTYPE html>
<html>
  <head>
    <title>Ejemplo JavaScript</title>
  </head>
  <body>
    <script src="app.js"></script>
  </body>
</html>
```

Ábrelo nuevamente con un navegador o refresca la página si ya lo tenías abierto. Deberías ver una alerta pero ahora con el texto "Hola Amigo".

## Ejecutando código en NodeJS

Existen dos formas de ejecutar código JavaScript en [NodeJS](https://nodejs.org/en/): desde la consola de NodeJS o desde un archivo.

### La consola de NodeJS

Para abrir la consola de NodeJS ejecuta el siguiente comando desde la línea de comandos:

```
$ node
>
```

La consola de NodeJS nos permite escribir una **expresión** de JavaScript, oprimir Enter, y ver el resultado de esa expresión en la siguiente línea, muy parecido a cómo lo hicimos sobre la consola del navegador en la sección pasada.

Por ejemplo, si escribimos `1+2` y oprimimos `Enter` debería mostrar `3` en la siguiente línea:

```
$ node
> 1 + 2
3
>
```

Para salir de la consola oprime `Ctrl` + `D`.

**Nota:** En JavaScript el punto y coma (`;`) al final de cada expresión es opcional. Cuando estemos trabajando en la consola de NodeJS los vamos a omitir. Sin embargo, cuando mostremos código que va a ir en un archivo los incluímos porque es una buena práctica.

### Desde un archivo

La otra forma de ejecutar código JavaScript en [NodeJS](https://nodejs.org/en/) es crear un archivo con extensión `js` en el que escribimos nuestro código y lo ejecutamos con el comando `node`.

Crea un archivo llamado `app.js`, ábrelo con tu editor favorito y pega el siguiente contenido:

```js
console.log("Hola Mundo!");
```

Guárdalo y ejecuta `node app.js` sobre la línea de comandos (asegúrate de estar ubicado sobre la carpeta donde se encuentra el archivo). Deberías ver el texto "Hola Mundo" en la siguiente línea:

```
$ node app.js
Hola Mundo
```

Cambia el texto por cualquier otro y vuelve a ejecutar el archivo.

¡Felicitaciones, has creado tu primer programa en JavaScript con NodeJS!

## Errores

Veamos ahora qué pasa si cometemos algún error en nuestro código. Por ejemplo, borra el caracter `l` de la palabra `console` y vuelve a ejecutar el archivo. Te debería aparecer un mensaje de error similar al siguiente:

```
/Users/germanescobar/Projects/node/app.js:1
(function (exports, require, module, __filename, __dirname) { consoe.log("Hola Mundo");
                                                              ^

ReferenceError: consoe is not defined
    at Object.<anonymous> (/Users/germanescobar/Projects/node/app.js:1:63)
    at Module._compile (module.js:571:32)
    at Object.Module._extensions..js (module.js:580:10)
    at Module.load (module.js:488:32)
    at tryModuleLoad (module.js:447:12)
    at Function.Module._load (module.js:439:3)
    at Module.runMain (module.js:605:10)
    at run (bootstrap_node.js:420:7)
    at startup (bootstrap_node.js:139:9)
    at bootstrap_node.js:535:3
```

Toma un tiempo acostumbrarse a leer los mensajes de error de NodeJS pero ahí está todo lo que necesitas saber para solucionarlo. El caracter `^` nos muestra dónde ocurrió el error (aunque está mezclado con otro código que genera NodeJS) y debajo de esa línea una frase que dice `ReferenceError: consoe is not defined`.

Hay veces en los que es fácil encontrar los errores, otras veces no es tan fácil. Lo que si es cierto es que a medida que vayas trabajando con el lenguaje vas a ir desarrollando una intuición que te va a permitir solucionar los errores más fácilmente, pero al principio es un proceso lento que es parte de ese aprendizaje.

Cometamos otro error intencionalmente para ver un mensaje diferente. Vuelve a escribir `console` correctamente, pero ahora borra la comilla al final de la cadena de texto así:

```js
console.log("Hola Mundo);
```

Y vuelve a ejecutar el archivo. Debería salir un mensaje como el siguiente:

```
/Users/germanescobar/Projects/node/app.js:1
(function (exports, require, module, __filename, __dirname) { console.log("Hola Mundo);
                                                                          ^^^^^^^^^^^^^
SyntaxError: Invalid or unexpected token
    at Object.exports.runInThisContext (vm.js:78:16)
    at Module._compile (module.js:543:28)
    at Object.Module._extensions..js (module.js:580:10)
    at Module.load (module.js:488:32)
    at tryModuleLoad (module.js:447:12)
    at Function.Module._load (module.js:439:3)
    at Module.runMain (module.js:605:10)
    at run (bootstrap_node.js:420:7)
    at startup (bootstrap_node.js:139:9)
    at bootstrap_node.js:535:3
```

Esta vez el mensaje `SyntaxError: Invalid or unexpected token` no es tan claro, pero fíjate que nos indica dónde está el problema con varios caracteres `^`.

## Escribiendo más líneas

Vuelve a agregar la comilla y verifica que se ejecute normalmente.

NodeJS ejecuta el archivo línea por línea, una después de la otra. Así que podemos agregar una segunda línea a nuestro archivo:

```js
console.log("Hola Mundo");
console.log("Esto está muy bacano");
```

El ejecutar el archivo deberías ver el siguiente resultado:

```
$ node app.js
Hola Mundo
Esto está muy bacano
```

## Comentarios

Los comentarios se utilizan para documentar o aclarar nuestro código y son ignorados al ejecutar el archivo. En JavaScript se utilizan los caracteres `//` para crear un comentario de una línea. Por ejemplo:

```js
// este es un comentario de una línea
console.log("Hola Mundo");
console.log("Esto está muy bacano"); // este es otro comentario
```

También puedes crear comentarios de múltiples líneas encerrando el texto entre `/*` y `*/`. Por ejemplo:

```js
/*
 este es un comentario
 de varias líneas
 console.log("esto no aparece al ejecutar el archivo")
*/
console.log("Hola Mundo");
console.log("Esto está muy bacano");  
```

Fíjate que la última línea del comentario es código JavaScript válido. Sin embargo, **ese código no se ejecuta porque está como comentario**.

## Evalúate

Al final de cada capítulo encontrarás algunas preguntas sobre los conceptos más importantes. No te preocupes si tienes que repasar el capítulo para encontrar las respuestas. Lo que sí te recomendamos es que escribas las respuestas en alguna parte (no importa si es en papel o digitalmente) para que afiances los conceptos.

1. ¿Qué es NodeJS?

2. Nombre al menos 2 formas en las que podemos ejecutar código JavaScript.

3. ¿Cómo imprimimos "Me gusta JavaScript!" desde un archivo de texto?

4. ¿Cómo se ejecuta un archivo de JavaScript en NodeJS?

5. ¿Cómo se pueden definir comentarios en JavaScript?
