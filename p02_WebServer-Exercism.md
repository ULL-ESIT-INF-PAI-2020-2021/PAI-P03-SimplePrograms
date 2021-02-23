# Práctica 2. Node Express Static Web Server. Exercism
### Factor de ponderación: 5

### Objetivos
Los objetivos de esta práctica son:
* Instalar un servidor web estático en la máquina virtual de la asignatura
* Conocer y configurar el entorno de trabajo de Exercism
* Configurar y practicar el uso del Visual Studio Code para editar ficheros en la máquina IaaS de la asignatura

### Rúbrica de evaluacion del ejercicio
Se señalan a continuación los aspectos más relevantes (la lista no es exhaustiva)
que se tendrán en cuenta a la hora de evaluar esta práctica:
* El alumnado ha de acreditar que es capaz de editar ficheros de forma remota en su VM usando VSC
* El alumnado ha de ser capaz de instalar y mantener ejecutando un servidor web estático
* El alumnado debe ser capaz de subir la solución a un problema de Exercism a esa plataforma

### Servidor web basado en Node y Express
Establezca una conexión `ssh` con su máquina virtual IaaS.

utilice [esta referencia](https://lenguajejs.com/npm/introduccion/que-es/) para conocer `npm` e instalarlo en
su máquina virtual.

Clone este repositorio en su VM del IaaS-ULL y siga estas instrucciones para instalar en la máquina IaaS un servidor web basado en Node y Express. 
No es necesario que conozca los detalles de estas herramientas, sino simplemente seguir las instrucciones suministradas.

Si todo funciona correctamente, al abrir un navegador en la URL `http://<your VM IP address>:8080` debería ejecutar en esa web un programa que calcula el 
valor de PI de forma aproximada.

Modificando convenientemente el fichero index.html (o colocando los ficheros necesarios en su lugar) en el directorio `www` del proyecto 
creado puede visualizar diferentes webs que pudiera crear en el futuro. Experimente con este servidor web.


[![Node Logo](http://sub1.kevinchisholm.com/blog/images/node-js-logo.png)](http://blog.kevinchisholm.com/?s=node)

## Dependencias

Lo que se precisa para ejecutar instalar el servidor: 

* [Node.Js](https://nodejs.org)

### Configuración

* 1 - Clone este repo en el directorio de esta práctica: 

```
git clone git@github.com:fsande/PAI-P02-WebServer-Exercism.git <yourDirectory>
```

* 2 - Sitúese en ese directorio para trabajar en él:

```
cd <yourDirectory>
```

* 3 - Ejecute este comando:

```
npm install
```

* 4 - Ejecute a continuación:

```
npm start
```

* 5 - Abra una página en su navegador con la siguiente dirección:

```
http://<your VM IP address>:8080
```

Para que el servidor web se mantenga activo incluso en el caso de que se cierre la sesión en la máquina
virtual utilice el comando
```
$ nohup sudo -b npm start
```
en el paso 5 anterior.

### Exercism
[Exercism](https://exercism.io/) es una plataforma orientada a aprender a programar o también a mejorar las
capacidades de cualquier programadora.
El objetivo de Exercism es servir como medio para aprender a programar en un determinado lenguaje, y para ello se propone
hacerlo mediante la resolución de ejercicios que otros usuarios han planteado. 
Lo que se persigue es que tanto quien resuelve el problema como quien lo planteó aprendan al mismo tiempo. 
Además, la interacción con el resto de la comunidad podrá llevar a debates para determinar cuál sería la mejor solución para un determinado problema.

La plataforma se basa en una una aplicación de línea de comandos disponible para diferentes sistemas
operativos (Linux, Mac, Windows).
Usando esa aplicación, un usuario puede descargar una serie de ejercicios de programación disponibles en la
plataforma y realizar los correspondientes programas hasta que consiga pasar los diferentes tests que se
suministran con cada ejercicio.

La plataforma puede ser usada en "modo práctica", en cuyo caso no existe la opción de mentorización (solicitar
que una experta le ayude con sus ejercicios), pero aún
así merece la pena practicar los múltiples ejercicios que hallará en la plataforma.

## Primeros pasos en Exercism
Comience por [registrarse en Exercism](https://exercism.io/users/sign_up). 
usando su cuenta de GitHub.
Una vez disponga de una cuenta, configure lo básico de la misma y elija un "track" (un lenguaje) en el que
desee practicar.
Obviamente se propone que elija el track correspondiente a JavaScript++.

Propóngase a continuación resolver el problema "Hello World".
En la página de ese problema (o de cualquier otro) hallará Ud. un enlace que indica *Get started* y 
[Begin walk-through](https://exercism.io/cli-walkthrough).
Si sigue ese enlace le llevará a la página *Welcome to the Exercism installation guide!* con instrucciones
sobre cómo instalar `exercism`.
En este documento se propone instalarla en la máquina virtual Linux de la asignatura.
Eligiendo la opción *Linux* y a continuación la opción *Using snap* se le pedirá que ejecute
```
$ sudo snap install exercism
```
Ese comando instalará en primer lugar `snap` y a continuación `exercism`, que es lo que se persigue.
También en esa página se indica que se compruebe que la instalación es correcta con el comando
```
$ exercism version
```
[`snap`](https://blogubuntu.com/que-es-ubuntu-snap) es un mecanismo alternativo al ya conocido
`apt-get install` para instalar aplicaciones en Ubuntu Linux.
Si quiere Ud. saber más sobre `snap` puede consultar
[esta referencia](https://snapcraft.io/docs/getting-started),
aunque ello no es necesario para el trabajo que se propone realizar con Exercism.

Una vez instalada la aplicación `exercism` el siguiente paso es configurar la interfaz de comandos (CLI) de la
aplicación.
Para ello se pide que se ejecute el comando
```
$ exercism configure --token=xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx
```
donde el *token* que figura en el comando anterior se encuentra (es específico de cada usuario) en la [página
de configuración](https://exercism.io/my/settings) de la cuenta de usuario que se ha creado.
Basta copiar de esa página el token y colocarlo en el comando anterior.

El comando anterior, una vez ejecutado indica:
```
You have configured the Exercism command-line client:

Config dir:                       /home/usuario/snap/exercism/5/.config/exercism
Token:         (-t, --token)      xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx
Workspace:     (-w, --workspace)  /home/usuario/snap/exercism/5/exercism
API Base URL:  (-a, --api)        https://api.exercism.io/v1
```
A continuación se puede elegir un problema para pasar a resolverlo.
Se propone, como ya se ha dicho, elegir el problema "Hello World".
En la página de ese problema figura una descripción precisa del problema planteado y en la parte derecha de
esa página figuran las instrucciones para:
* Download. Descargar el problema mediante el comando `exercism download --exercise=hello-world --track=javascript`
* Solve. Para resolver el problema se propone usar el editor favorito del usuario. Se recomienda usar Visual
  Studio Code
* Submit. El comando para subir a la plataforma la solución que el usuario proponga.

Si se ejecuta el comando para descargar el problema el sistema responde:
```
exercism download --exercise=hello-world --track=javascript

Downloaded to
/home/usuario/snap/exercism/5/exercism/javascript/hello-world
```
indicando el directorio donde ha colocado el código necesario para trabajar en ese problema.

Revise los ficheros que exercism ha descargado.

## Ejecución de los tests para un determinado problema
El siguiente paso consiste en editar el programa (en el caso del problema "Hello World" el fichero a editar es
`hello-world.js`).
Edite ese fichero hasta que considere que tiene una versión operativa.
Una vez finalizado su programa, el siguiente paso consiste en pasar (superar) los tests del código.
Cada ejercicio de Exercism va acompañado de una serie de tests que el programa debe superar para ser
considerado válido.

Tal como se explica en la página [Running the Tests](https://exercism.io/tracks/javascript/tests), cada problema va
acompañado de sus tests unitarios.

Para comprobar su solución ejecute:

```
$ npm run test
```

Cuando su solución al problema pase todos los tests y esté Ud. satisfecha con la misma, puede remitirla a la
plataforma.
Utilice para ello el comando `exercism submit` que hallará Ud. en la página correspondiente al problema.
Una vez que haya enviado su solución a Exercism recibirá un mensaje similar a este:
```
Your solution has been submitted successfully.
You can complete the exercise and unlock the next core exercise at:

https://exercism.io/my/solutions/xxxx
```
A partir de este punto puede ya ver las soluciones que otras usuarias hayan dado al mismo problema o bien
avanzar con otros problemas de ese mismo "track".
