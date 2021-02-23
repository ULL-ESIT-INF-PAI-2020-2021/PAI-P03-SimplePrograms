# Práctica 2. Programas simples
### Factor de ponderación: 5

### Objetivos
Los objetivos de esta práctica son:
* 
* Ser capaz de realizar programas simples en JavaScript
* Conocer y saber utilizar la plataforma Exercism
* Conocer y poner en prácticas las recomendaciones de la Guía de Estilo de Google para JavaScript

### Rúbrica de evaluacion del ejercicio
Se señalan a continuación los aspectos más relevantes (la lista no es exhaustiva)
que se tendrán en cuenta a la hora de evaluar esta práctica:
* El alumnado ha de acreditar que es capaz de desarrollar y ejecutar programas simples
* El alumnado debe ser capaz de subir la solución a un problema de Exercism a esa plataforma
* Se comprobará que el código que el alumnado escribe se adhiere a las reglas de la Guía de Estilo que se
  usará en la asignatura

### Indicaciones de caracter general
A la hora de resolver los problemas que se le proponen, trate de usar exclusivamente las características de
JavaScript que ha estudiado en clase o bien en el material que se le ha pedido que estudie.

Descarte soluciones avanzadas y nunca utilice código que no sea Ud. capaz de comprender y explicar a otra
persona.

Los programas que escriba han de seguir **fielmente** todas las indicaciones de la 
[Guía de estilo de Google para JavaScript](https://google.github.io/styleguide/jsguide.html).
Estudie esa guía omitiendo todo lo que se refiera a características avanzadas del lenguaje que no haya Ud.
estudiado aún.
Preste particular atención a los siguientes aspectos:
* Reglas para nombres (identificadores) de diferente tipología (constantes, variables, parámetros, funciones, ...)
* [Formateo](https://google.github.io/styleguide/jsguide.html#formatting) del código
* Utilización de los
  [espacios en blanco](https://google.github.io/styleguide/jsguide.html#formatting-horizontal-whitespace)
* Comentarios de ["cabecera"](https://google.github.io/styleguide/jsguide.html#jsdoc-top-file-level-comments) para sus programas. 
  Para este aspecto se recomienda utilizar una "plantilla" base de comentarios que incluya información tal
  como: Universidad, Titulación, Asignatura, Proyecto, Autor, Fecha, ... que irá siempre seguido de una
  descripción más o menos exhaustiva del programa en cuestión
Esa guía de estilo es la que se utilizará en la asignatura y la conformidad de todos los programas presentados como prácticas es un requisito en la evaluación de los mismos.

Estudie 
[esta referencia](https://nodejs.org/en/knowledge/command-line/how-to-parse-command-line-arguments/) 
para aprender a trabajar con parámetros pasados en línea de comandos a un programa ejecutado con Node.js.

Este [código de ejemplo](https://repl.it/@fsande/commandLineArguments) (ejecútelo en la consola de Node, no en el REPL.it) puede servirle de ayuda inicialmente.

No lo necesitará para Exercism, pero pruebe a ejecutar todos los programas que escriba pasándole parámetros
por línea de comandos.


### Armstrong Numbers
Localice en el track de JavaScript de Exercism el problema 
[Armstrong Numbers](https://exercism.io/my/solutions/5e1f0bde06fb41e78acbfb2312181821) 
y descárguelo en su máquina virtual. 
Resuelva ese problema.

Si analiza el programa que realiza los tests (`armstrong-numbers.spec.js`) observará que necesita Ud. programar una función `isArmstrongNumber()`
que tome como parámetro un número entero y devuelva un valor booleano indicando si el parámetro es o no un
número de Armstrong.

La función que ha de escribir es una *arrow function* que tendría la siguiente *signature*:

```js
export const isArmstrongNumber = (number) => {
};
```

Ejecute los tests que acompañan al problema para comprobar que todos pasan correctamente y cuando lo consiga, suba su solución a Exercism.

Una vez que suba su solución a la plataforma, revise la solución que hayan subido otros usuarios y compárelas
con la suya.

Una vez que su programa funcione en consola, consiga que funcione en una página web similar a la que se ha usado para el cálculo de Pi. 

### Darts
Localice en el track de JavaScript de Exercism el problema 
[Darts](https://exercism.io/my/solutions/de65d30c065c435b82911b0c7ca10b0c)
y descárguelo en su máquina virtual. 
Resuelva ese problema.

Ejecute los tests que acompañan al problema para comprobar que todos pasan correctamente y cuando lo consiga, suba su solución a Exercism.

Una vez que suba su solución a la plataforma, revise la solución que hayan subido otros usuarios y compárelas
con la suya.

### Nth Prime
Localice en el track de JavaScript de Exercism el problema 
[Nth Prime](https://exercism.io/my/solutions/07630f17544c4c4ca7cc30fa69c51e7e)
y descárguelo en su máquina virtual. Resuelva ese problema.

Para lanzar una excepción (que es lo que se espera en el caso de un parámetro negativo o nulo en este problema) en JavaScript utilice una sentencia como:
```js
throw new Error('Only positive numbers are allowed');
```

Para saber más sobre las excepciones en JavaScript estudie el apartado
[Exceptions](https://eloquentjavascript.net/08_error.html) 
en el capítulo 8 de *Eloquent JavaScript*, y el apartado
[“Throw” operator](https://javascript.info/try-catch#throw-operator)
en el *Modern JavaScript Tutorial*.

Ejecute los tests que acompañan al problema para comprobar que todos pasan correctamente y cuando lo consiga, suba su solución a Exercism.

Una vez que suba su solución a la plataforma, revise la solución que hayan subido otros usuarios y compárelas
con la suya.
