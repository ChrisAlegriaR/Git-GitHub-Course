# 🧩 Introducción a Git y Github
## 📌 ¿Qué es Git?
**Git** es un **sistema de control de versiones distribuido** creado por **Linus Torvalds** en 2005. Con el tiempo, se ha convertido en una herramienta **fundamental para la gestión de código fuente** en proyectos de programación colaborativa. Esto significa que **un clon local del proyecto es un repositorio de control de versiones completo**, lo que permite trabajar **sin conexión o de manera remota** con facilidad.  

Los desarrolladores pueden **confirmar su trabajo localmente** y, a continuación, **sincronizar su copia del repositorio con la copia en el servidor**. Este enfoque es distinto del control de versiones centralizado, donde los clientes deben sincronizar el código con un servidor antes de crear nuevas versiones.  

Git es un **software que maneja versiones** y lo hace de manera **local**, directamente en el dispositivo donde estés trabajando. Esto permite **guardar capturas de distintas versiones** del código que desarrolles, facilitando el seguimiento de cambios y la colaboración con otros desarrolladores.  

>💡 *En resumen, Git te permite mantener un historial completo de tu proyecto, trabajar de manera organizada y segura, y colaborar eficientemente con otros desarrolladores.*  

## 📌 ¿Qué es GitHub?
**GitHub** es una **plataforma en línea** que utiliza el sistema de control de versiones **Git** para **alojar repositorios de código fuente** y facilitar la **colaboración en proyectos de desarrollo de software**. Fue fundada en **2008** por **Tom Preston-Werner, Chris Wanstrath, P. J. Hyett y Scott Chacon**, y desde entonces se ha convertido en una de las **herramientas más importantes y populares para desarrolladores en todo el mundo**.  

En GitHub, los desarrolladores pueden **subir sus repositorios locales a la nube**, compartirlos con otros, trabajar de manera conjunta en el mismo proyecto, **gestionar ramas, issues, pull requests**, y mantener un historial completo de cambios accesible desde cualquier lugar.  

>💡 *En resumen, GitHub es la plataforma que lleva la potencia de Git a la nube, permitiendo a equipos de cualquier tamaño colaborar en tiempo real, mantener un flujo de trabajo más ordenado y centralizar sus proyectos de software en un solo lugar.*

---

## ✅ Beneficios del uso de un sistema de gestión de versiones
Existen diferentes beneficios cuando usamos un **sistema de gestión de versiones** como lo es **Git**, ya que cumple una función fundamental en el desarrollo de software. Esta herramienta nos ayuda a **gestionar y controlar los cambios** que realizamos en nuestro código, evitando errores y pérdidas de información.  

Podemos imaginar dos posibles escenarios: uno donde utilizamos un sistema de gestión de versiones y otro donde no lo usamos.  

- **❌ Sin un sistema de gestión de versiones:**  
  Imaginemos que estamos trabajando en un proyecto en el cual inicialmente creamos un archivo `index.html`. En un primer momento, le añadimos una estructura base con un **header**, una **barra lateral** y un **footer**, y guardamos esos cambios. Esto equivaldría a crear, por ejemplo, la **versión 0.1**.  

  Más adelante, decidimos integrar **botones, inputs y más elementos de formulario** al HTML, y al guardar tendríamos la **versión 0.2**. El problema es que estos cambios sustituyen por completo la versión anterior.  

  Ahora bien, si después de un tiempo, ya sea por una petición del cliente, por motivos del equipo de trabajo o por decisión personal o por algún error, se nos solicita **volver al estado inicial** (con solo el header, la barra lateral y el footer), tendríamos que **borrar manualmente** todo lo que añadimos, lo cual es un proceso **tardado, propenso a errores y nada eficiente**.  

- **✔️ Con un sistema de gestión de versiones:**  
  Ahora bien, si aplicamos el mismo ejemplo pero utilizando un **sistema de gestión de versiones**, tendríamos que al crear un archivo `index.html`, en un primer momento le añadimos una estructura base con un **header**, una **barra lateral** y un **footer**. Al guardar estos cambios, podríamos crear una especie de **versión 0.1** mediante un **commit**, el cual consiste en **confirmar una versión en Git** que quedará registrada como un **punto de guardado en nuestro historial**.  

  Más adelante, si decidimos integrar **botones, inputs y más elementos de formulario** al HTML, al guardar podríamos tener la **versión 0.2**. A diferencia de cuando no contamos con un sistema de gestión de versiones, aquí **no se sustituye la versión 0.1**, sino que **todas las versiones anteriores permanecen almacenadas** en el historial del repositorio.  

  De esta manera, si después de un tiempo, ya sea por una petición del cliente, motivos del equipo, decisión personal o incluso por un error se nos solicita **volver al estado inicial** (con solo el header, la barra lateral y el footer), mediante Git tendríamos la posibilidad de regresar fácilmente a esa versión anterior. A este proceso se le conoce como **rollback**.  

  Además, el sistema de gestión de versiones nos permite **comparar el código de diferentes versiones** (pasadas o actuales), pudiendo identificar con precisión qué líneas de código fueron **agregadas, eliminadas o modificadas** en cada commit, lo cual facilita enormemente la depuración y el trabajo colaborativo.  

---

## 👥 Trabajo en equipo
Los sistemas de gestión de versiones nos permiten **trabajar de manera más eficiente en equipo**. Aunque se podría trabajar directamente, por ejemplo, en **Google Drive**, donde el código se actualiza en tiempo real, este enfoque tiene varias desventajas: siempre se necesita **conexión a Internet**, y si un archivo se elimina por error, **se pierde para siempre**, y ninguno de los integrantes tendría una copia.  

Con **Git**, en cambio, podemos trabajar y crear nuestros **commits** de manera **local** en nuestro dispositivo, y posteriormente **subir esos cambios al servidor** cuando queramos. Esto permite **controlar exactamente qué cambios se comparten**, evitando pérdidas accidentales de información.  

Además, Git cuenta con **repositorios remotos**, que son **lugares en la nube donde se almacena el código y todas sus versiones**, siendo **GitHub** la plataforma más utilizada. Todos los integrantes del equipo pueden trabajar localmente, subir sus cambios cuando estén listos y **consultar todas las versiones existentes**.  

>💡 *Trabajar de manera local con Git permite que nunca se elimine accidentalmente el trabajo en el repositorio y que solo se suban los cambios que realmente están correctos y aprobados.*

---

## 🚨 ¿Cuándo comenzó a fallar y por qué?
Uno de los grandes beneficios de un **sistema de gestión de versiones** como **Git** es que nos permite **detectar con precisión cuándo comenzó un error en nuestra aplicación**.  

Cuando varios integrantes de un equipo van subiendo cambios a un mismo proyecto, es posible que en algún momento una funcionalidad deje de funcionar correctamente. Gracias al **historial de commits**, Git nos permite **revisar paso a paso las versiones anteriores del código**, identificar en qué momento se introdujo el fallo y, si es necesario, **volver a una versión estable** mediante un **rollback**.  

Sin un sistema de control de versiones, esto no sería posible, ya que no contaríamos con un historial que indique **qué cambios se hicieron, cuándo y por quién**. En Git, cada commit funciona como una **copia de seguridad del estado del código en ese momento**, lo que nos brinda la capacidad de **avanzar o retroceder en el tiempo** según sea necesario.  

>💡 *Git nos da la capacidad de rastrear errores, corregirlos de manera eficiente y mantener la estabilidad de la aplicación sin perder el historial de nuestro trabajo.*

---

## 🖳 Terminal de Git
Si bien **Git** es un **sistema de gestión de versiones**, es importante mencionar que se trata de un **programa que debe instalarse** en nuestro equipo. Al hacerlo, no solo obtenemos la herramienta principal, sino también una **terminal propia** llamada **Git Bash**, en la cual podremos ejecutar **comandos específicos** para trabajar con nuestros proyectos.  

Para abrirla, simplemente podemos buscar **"Git Bash"** en la barra de búsqueda de Windows. Otra opción muy práctica es **hacer clic derecho en cualquier carpeta** y seleccionar **"Git Bash Here"**, lo cual abrirá la terminal directamente en esa ubicación. Esto es especialmente útil porque **cualquier acción que realicemos desde Git afectará al contenido de la carpeta actual**, como inicializar un repositorio, confirmar cambios, crear ramas o subir código a un repositorio remoto.  

Desde esta consola podemos realizar diversas acciones como **crear commits**, **subir cambios a GitHub**, **configurar nuestro usuario**, **crear ramas**, entre muchas otras operaciones que nos permiten tener un **control detallado del flujo de trabajo**.  

Por otro lado, algunos entornos de desarrollo como **Visual Studio Code** incluyen herramientas gráficas que facilitan la gestión de Git. Esto significa que podemos **confirmar cambios, crear ramas o sincronizar nuestro repositorio** sin necesidad de escribir comandos en la terminal, lo cual resulta muy práctico para quienes prefieren una interfaz más visual.  

>💡 *La terminal de Git es la herramienta más completa para interactuar con el sistema, y abrirla en la carpeta correcta nos permite ejecutar acciones directamente sobre su contenido, mientras que los entornos gráficos ofrecen una alternativa más sencilla y accesible.*

---

# ⚙️ Git Config
El comando **`git config`** se utiliza dentro de la **terminal de Git** y nos permite **realizar configuraciones importantes** para que la terminal sepa cómo manejar nuestro entorno. Gracias a este comando, podemos **personalizar Git según nuestras necesidades**, especificando información como **nombre de usuario, correo electrónico**, editor de texto predeterminado, colores en la terminal y otros parámetros que Git utilizará en nuestros commits y repositorios.  

Estas configuraciones son esenciales porque Git utiliza esta información para **identificar al autor de los commits** y mantener un historial organizado y claro, especialmente cuando trabajamos en **proyectos colaborativos**.  

## 🌐 --global
El parámetro **`--global`** se usa junto con el comando `git config`, quedando de la forma:  

```bash
git config --global
```

Al usar **`--global`**, le estamos indicando a Git que las configuraciones que definamos afectarán a todos los proyectos en nuestro equipo que utilicen Git, y no solo al repositorio en el que estemos trabajando actualmente. Esto es especialmente útil para establecer información general, como nuestro nombre o correo electrónico, que se aplicará automáticamente en todos los commits que realicemos.

## 🧑🏻‍💻 User
El parámetro **`user`** en Git nos permite declarar **dos opciones diferentes**: nuestro **nombre** y nuestro **correo electrónico**. Ambas son de **suma importancia** cuando se trabaja de manera colaborativa, ya que todos nuestros **commits** se registrarán con esta información. De esta forma, cualquier persona que consulte el historial de cambios en plataformas como **GitHub** podrá identificar **quién realizó cada acción** y con qué correo asociado.  

- **`user.name`:**  
  Para especificar nuestro **nombre** en Git utilizamos el comando `user.name`. Aquí, `user` hace referencia a la configuración de nuestro usuario, y `.name` indica que vamos a declarar nuestro nombre. El comando se ejecuta junto con comillas, dentro de las cuales colocaremos nuestro nombre, por ejemplo:  

  ```bash
  git config user.name "ChristianAR"
  ```

- **`user.email`:**
  Para especificar nuestro correo electrónico en Git utilizamos el comando `user.email`. Al igual que antes, `user` indica la configuración del usuario y `.email` señala que vamos a declarar nuestro correo. Es importante que este correo coincida con el que usaremos en nuestro repositorio remoto (GitHub, GitLab, Gitea, etc.), de lo contrario, podrían generarse errores al sincronizar los commits. El comando se ejecuta con comillas, dentro de las cuales colocaremos nuestro correo, por ejemplo:

  ```bash
    git config user.email "christian.alegriar@gmail.com"
  ```

## 🖥 Core
El parámetro **`core`** en Git hace referencia al **núcleo del sistema**, es decir, a aquellas configuraciones que afectan directamente el **funcionamiento fundamental de Git**. A través de este parámetro podemos establecer ajustes esenciales que determinan cómo se comporta Git en nuestro entorno de trabajo.  

Por lo que el parámetro `core` controla aspectos esenciales del funcionamiento de Git, como el editor por defecto, el manejo de archivos y el comportamiento interno del sistema, permitiéndonos personalizar la experiencia de trabajo según nuestras necesidades.

- **`core.editor`:**  
  El parámetro **`core.editor`** en Git nos permite **configurar el editor de texto o código predeterminado** que Git abrirá cuando sea necesario realizar acciones que requieran edición manual, como escribir un mensaje de commit más largo, resolver conflictos de merge o editar configuraciones avanzadas.  

  Por defecto, Git puede abrir editores básicos como **Vim** o **Nano** en la terminal, lo cual puede resultar incómodo si no estamos familiarizados con ellos. Para mayor comodidad, podemos indicar que queremos usar un editor más moderno, como **Visual Studio Code**, **Sublime Text** o cualquier otro editor instalado en nuestro sistema.  

  En el caso de **Visual Studio Code**, su comando de apertura es `code`. Para configurarlo como nuestro editor predeterminado en Git, ejecutaríamos el siguiente comando:

  ```bash
  git config core.editor "code"
  ```

  >⚠️ *OJO: Configurar un editor externo en Git no significa que vayamos a ejecutar los comandos desde ese editor (como git commit o git push). Lo que hace es que, cuando Git necesite que escribamos algo que la consola no maneja cómodamente (por ejemplo, un mensaje de commit largo, una descripción detallada en un merge o la edición de configuraciones internas), en lugar de usar la terminal, se abrirá automáticamente el editor que hayamos configurado.*


  - **`--wait`:**  
    El parámetro **`--wait`** se utiliza junto con `core.editor`, por ejemplo: `core.editor "code --wait"`. Su función es **indicarle a Git que debe esperar a que el editor externo termine de realizar la acción antes de continuar con el comando**.  
  
    Como mencionamos antes, Git abre editores externos para ciertos casos especiales, como escribir mensajes de commit largos o resolver conflictos. Sin embargo, en ocasiones Git puede **interpretar incorrectamente que ya hemos terminado**, ejecutando el comando **antes de que realmente hayamos ingresado la información necesaria** en el editor. Esto puede generar errores o commits vacíos.  
  
    El uso de `--wait` **soluciona este problema**, obligando a Git a **esperar hasta que guardemos y cerremos el editor externo** antes de ejecutar el comando correspondiente. De esta manera, se asegura que todo lo que necesitamos ingresar en el editor sea procesado correctamente por Git. Por lo que el comando completo para configurar Visual Studio Code como editor predeterminado y usar `--wait` sería:  
  
    ```bash
    git config core.editor "code --wait"
    ```

- **`core.autocrlf`:**  
  La mayoría de los servidores de repositorios remotos como **GitHub**, **GitLab** y otros funcionan en entornos **Linux/Unix**, lo que provoca que los **saltos de línea** se manejen de forma diferente en comparación con **Windows**.  

  Aquí es donde entra en juego el parámetro **`core.autocrlf`**, el cual nos permite **indicar a Git cómo manejar automáticamente los saltos de línea según el sistema operativo que estemos usando**.  

  Aunque Git suele detectar nuestro sistema operativo de forma automática, es recomendable **configurarlo manualmente** para evitar errores en los archivos al momento de compartir código con otros desarrolladores que trabajen en sistemas diferentes. Si no lo configuramos correctamente, pueden generarse **conflictos de formato** en los archivos, lo que complica el trabajo colaborativo. Por lo que la estructura básica es la siguiente:  

  ```bash
  git config core.autocrlf <valorSegunSistemaOperativo>
  ```

  Donde **`<valorSegunSistemaOperativo>`** puede variar según nuestro entorno:

  - **En Windows:** normalmente se utiliza `true`, quedando como:
    ```bash
  	git config core.autocrlf true
  	```
    
  - **En Linux/Unix o macOS:** generalmente se utiliza `input`,quedando como:
    ```bash
  	git config core.autocrlf input
  	``` 

  >💡 *core.autocrlf nos ayuda a que los saltos de línea se mantengan consistentes entre diferentes sistemas operativos, evitando errores y asegurando que el código sea legible y funcional sin importar desde dónde se edite.*

## ✏️ Edit
El parámetro **`--edit`**, abreviado como **`-e`**, nos permite **editar archivos de configuración** en Git. Dentro de `git config`, este parámetro nos facilita **verificar nuestras configuraciones actuales**, ya sea a nivel de proyecto o de manera global, y **modificarlas si así lo deseamos**.  

Cuando usamos **`git config -e`** o **`git config --edit`**, Git abre nuestro **editor de código externo** mostrando un archivo con toda nuestra configuración según corresponda (por proyecto o global). Este archivo incluye información como el **nombre de usuario**, **correo electrónico**, **origen del repositorio remoto**, **editor predeterminado**, entre otras configuraciones importantes. Ademas cabe mencionar que tanto la forma completa como la abreviada pueden ser ejecutadas y teniendo ambas la misma funcion, siendo las siguientes:

```bash
git config -e
git config --edit
```

Al ejecutar cualquiera de estos comandos nuestro editor de código abrirá un archivo similar al siguiente, donde podremos comprobar y modificar nuestras configuraciones:
```bash
[core]
	repositoryformatversion = 0
	filemode = false
	bare = false
	logallrefupdates = true
	symlinks = false
	ignorecase = true
	editor = code --wait
[remote "origin"]
	url = https://github.com/ChrisAlegria/Git-GitHub-Course.git
	fetch = +refs/heads/*:refs/remotes/origin/*
[branch "main"]
	remote = origin
	merge = refs/heads/main
```

## 📑 Archivo de configuración  
Cuando creamos un proyecto para trabajar con un sistema de gestión de versiones como **Git**, se genera un archivo llamado **`.gitconfig`**, el cual contiene toda la configuración que el proyecto está utilizando. Este archivo puede reflejar tanto configuraciones específicas del proyecto como configuraciones globales aplicadas a todo el sistema, y estará siempre presente en los repositorios que gestionemos con Git. En él se almacenan parámetros importantes como el **editor de texto predeterminado**, el **nombre de usuario**, el **correo electrónico** asociado y muchos otros ajustes que determinan el comportamiento de Git.  

>💡 *En resumen, el archivo `.gitconfig` es el lugar donde Git centraliza todas las configuraciones necesarias para que podamos trabajar de manera ordenada y personalizada en cada proyecto.*

# 📟 Comandos Básicos de la Terminal  
Existen diversos **comandos básicos** dentro de la **consola/terminal de Git**, los cuales están basados en los **comandos de Linux**. Estos comandos se pueden utilizar en diferentes momentos y resultan muy útiles para tareas como **ayuda, edición, modificación y gestión general** dentro del entorno de trabajo. La gran ventaja es que la mayoría de ellos son **universales**, es decir, pueden usarse en cualquier proyecto y en prácticamente cualquier situación, ya sea para **aplicar configuraciones globales, solicitar ayuda, realizar ediciones o limpiar la consola**. Son, en definitiva, **comandos clave** que todo desarrollador debe dominar para desenvolverse de manera más eficiente al trabajar con Git.  Por lo que algunos de los más comunes son: 

- **`--edit` / `-e`:**  
  El parámetro `--edit`, que también podemos usar en su forma corta como `-e`, nos permite **editar cualquier archivo de configuración**. Un ejemplo de esto es `core`, un archivo donde se guardan las configuraciones de nuestros proyectos. Si ejecutamos `git config core -e`, se abrirá dicho archivo para **realizar modificaciones manualmente** de manera directa. Por lo que un ejemplo de este seria:

  ```bash
  git config -e
  ```

- **`--help` / `-h`:**  
  El parámetro `--help`, que también puede usarse como `-h`, nos permite **solicitar ayuda a Git**. Al ingresar este comando, se mostrará una **lista de los posibles comandos disponibles** que podemos utilizar. Por ejemplo, `git config -h` nos mostrará todos los comandos disponibles para `git config`, y esto aplica de manera similar para cualquier otro comando o apartado. Por lo que un ejemplo de este seria:

  ```bash
  git config -h
  ```

- **`--list`:**  
  Comúnmente, para verificar información en algún archivo solemos usar `-e` para abrirlo y revisar manualmente su contenido. Con el comando o parámetro `--list`, podemos **extraer directamente la información del archivo** y mostrarla en la consola, sin necesidad de abrirlo manualmente. Esto facilita la **consulta rápida de configuraciones** y datos relevantes. Por lo que un ejemplo de este seria:

  ```bash
  git config --list
  ```

- **`clear`:**   
  El comando `clear` nos permite **limpiar la consola**, eliminando todos los comandos previos y cualquier salida que se haya mostrado en pantalla. Esto no **afecta en absoluto los archivos, configuraciones ni el estado de nuestro proyecto**, simplemente nos ofrece una **pantalla limpia** para continuar trabajando de manera ordenada.

- **`ls`:**  
El comando `ls` nos permite **visualizar el listado de archivos y carpetas** que se encuentran en el directorio donde hayamos abierto la terminal. Por ejemplo, si abrimos la terminal en una carpeta llamada `proyecto` y ejecutamos `ls`, se desplegarán todas las carpetas y archivos que estén dentro de ella. De esta manera, el comando muestra de forma clara el contenido del directorio actual, lo que nos ayuda a ubicar los recursos disponibles sin necesidad de salir de la terminal. Un ejemplo de su uso sería:  

  ```bash
  chris@LAPTOP-0DNMOIV6 MINGW64 /d/Trabajos/Cursos/Git-GitHub-Course (main)
  $ ls
  Course/  Practices/  README.md
  ```

  - **`-a`:**  
  La opción `-a` (**all**) se utiliza junto con el comando `ls` para **mostrar todos los archivos y directorios**, incluyendo aquellos que están **ocultos**. En los sistemas basados en Linux (como Git Bash), los archivos ocultos son aquellos cuyo nombre comienza con un punto (`.`), por ejemplo: `.git`, `.env`, `.config`. De manera predeterminada, el comando `ls` no los muestra, pero al usar `ls -a` sí aparecerán en la lista. Esto resulta muy útil cuando queremos **ver archivos de configuración internos** que normalmente no son visibles, ya que muchos proyectos contienen carpetas y archivos ocultos que son esenciales para su funcionamiento. Por lo que un ejemplo practico seria:                    

  	```bash
  	chris@LAPTOP-0DNMOIV6 MINGW64 /d/Trabajos/Cursos/Git-GitHub-Course (main)
  	$ ls -a
  	./  ../  .git/  index.html  README.md
  	$
  	```

- **`cd`:**  
El comando `cd` (change directory) se utiliza para **movernos entre carpetas** desde la terminal. Por defecto, todos los comandos que ejecutamos en la terminal afectan a la **carpeta en la que nos encontramos actualmente** y, según el caso, a todas las subcarpetas que esta contenga. Por ejemplo, si estamos ubicados en una carpeta llamada `proyecto`, que a su vez contiene dos subcarpetas llamadas `proyecto_1` y `proyecto_2`, cualquier acción que ejecutemos tendrá efecto en `proyecto`.  Ahora bien, si lo que queremos es **acceder a una subcarpeta específica** para trabajar directamente en ella, usamos el comando `cd`. Basta con escribir `cd` seguido del nombre de la carpeta a la que deseamos entrar. Una vez ejecutado, la terminal cambiará su ubicación a esa carpeta, quedando de la siguiente manera:  

  ```bash
  chris@LAPTOP-0DNMOIV6 MINGW64 /d/Trabajos/Cursos/Git-GitHub-Course (main)
  $ cd course

  chris@LAPTOP-0DNMOIV6 MINGW64 /d/Trabajos/Cursos/Git-GitHub-Course/course (main)
  $
  ```

- **`cd ..`:**  
El comando `cd ..` se utiliza para **retroceder un nivel en el árbol de directorios**, es decir, salir de la carpeta en la que nos encontramos actualmente y volver a la carpeta que la contiene. En otras palabras, funciona como la operación **inversa a `cd`**, ya que en lugar de entrar en una subcarpeta, nos permite **regresar a la carpeta padre**. Por ejemplo, si estamos dentro de la carpeta `proyecto_1`, que a su vez está dentro de `proyectos`, al ejecutar `cd ..` volveremos directamente a `proyectos`. La terminal quedaría de la siguiente manera:  

  ```bash
  chris@LAPTOP-0DNMOIV6 MINGW64 /d/Trabajos/Cursos/Git-GitHub-Course/course (main)
  $ cd ..

  chris@LAPTOP-0DNMOIV6 MINGW64 /d/Trabajos/Cursos/Git-GitHub-Course (main)
  $
  ```
  
- **`pwd`:**  
El comando `pwd` (**print working directory**) se utiliza para **mostrar la ruta completa del directorio en el que nos encontramos actualmente** dentro de la terminal. Al ejecutarlo, Git Bash (o cualquier terminal basada en Linux) nos devuelve la **dirección absoluta** de la carpeta en la que estamos trabajando. Es importante no confundirlo con `ls`. Mientras que `pwd` nos indica **en qué carpeta estamos ubicados**, el comando `ls` lista los **archivos y subcarpetas que contiene el directorio actual**. Por ejemplo, si queremos confirmar nuestra ubicación dentro de la estructura de carpetas, podríamos obtener algo como lo siguiente:  

  ```bash
  chris@LAPTOP-0DNMOIV6 MINGW64 /d/Trabajos/Cursos/Git-GitHub-Course (main)
  $ pwd
  /d/Trabajos/Cursos/Git-GitHub-Course
  $
  ```

- **`mkdir`:**  
El comando `mkdir` (**make directory**) se utiliza para **crear nuevas carpetas (directorios)** directamente desde la terminal de Git.  Aunque comúnmente hablamos de "carpetas", en los sistemas basados en Linux (como Git Bash) estas se conocen como **directorios**. Para crear uno, basta con escribir `mkdir` seguido del nombre que le queremos asignar. Por ejemplo, si queremos crear una carpeta llamada `proyecto_3`, podemos hacerlo de la siguiente manera:  

  ```bash
  chris@LAPTOP-0DNMOIV6 MINGW64 /d/Trabajos/Cursos/Git-GitHub-Course (main)
  $ mkdir proyecto_3
  $
  ```

- **`git init`:**  
El comando `git init` se utiliza para **indicarle a Git que la carpeta en la que estamos trabajando será gestionada con su sistema de control de versiones**. Al ejecutar este comando, la carpeta actual se **convierte en un repositorio local de Git**, es decir, un espacio de trabajo donde podremos comenzar a llevar un **historial de cambios (commits)**, gestionar versiones y trabajar con ramas, aunque aún no esté vinculado a un repositorio remoto. En otras palabras, `git init` **inicializa un nuevo repositorio vacío** dentro de la carpeta en la que estamos, creando un directorio oculto llamado **`.git/`**, donde se almacenará toda la información y la configuración necesaria para el seguimiento de versiones. Un ejemplo práctico sería el siguiente:  

  ```bash
  chris@LAPTOP-0DNMOIV6 MINGW64 /d/Trabajos/Cursos/proyectos
  $ git init
  Initialized empty Git repository in D:/Trabajos/Cursos/proyectos/.git/
  ```
  
- **`Abrir editor de código desde la consola`:**  
Desde la terminal podemos **abrir directamente nuestro editor de código** en el directorio en el que nos encontremos trabajando. Esto es muy útil, ya que nos evita tener que buscar manualmente la carpeta desde la interfaz gráfica del editor. El comando que utilizaremos depende del editor que tengamos instalado. Por ejemplo, en el caso de **Visual Studio Code**, basta con escribir:  

  ```bash
  chris@LAPTOP-0DNMOIV6 MINGW64 /d/Trabajos/Cursos/proyectos
  $ code .
  ```

# 〰️ Flujo de Git  
Git trabaja con un **flujo definido** en el cual nuestros archivos van **pasando por diferentes estados** hasta finalmente llegar al repositorio remoto (estado final). Por lo que en total, podemos identificar **4 estados principales** que conforman el flujo de trabajo de Git:  

1. **Local (sin marcar):**  
   El primer paso dentro del flujo de Git sucede cuando tenemos nuestros archivos **locales** en una carpeta de proyecto. Para iniciar este proceso, ejecutamos el comando **`git init`**, con lo cual damos de alta nuestro proyecto en Git. A partir de este momento, Git reconoce que ese directorio será gestionado bajo su sistema de control de versiones, aunque **aún no hace nada con los archivos**. En este estado, simplemente hemos **inicializado el repositorio**, pero los archivos siguen siendo locales sin ningún seguimiento activo.  

2. **Stage (marcados):**  
   El segundo paso es el estado **Stage** (o “staging area”). Aquí usamos el comando **`git add .`**, lo que le indica a Git que tome nuestros archivos y los **marque** para que comiencen a ser rastreados. En este punto, Git crea una **copia temporal de los archivos** y empieza a observarlos. Eso significa que si los modificamos o eliminamos, Git detectará esos cambios. Es importante destacar que en esta etapa Git **no guarda todavía un historial permanente**, simplemente mantiene una **versión sincronizada temporal** de los archivos listos para ser confirmados. Si hacemos modificaciones y volvemos a ejecutar **`git add .`**, estas copias se actualizarán con los últimos cambios.  

3. **Commit (fotografiados):**  
   Este paso es uno de los más importantes y muchas veces se confunde con Stage. La diferencia es que el **commit crea una versión oficial en el historial del repositorio**. Cuando ejecutamos **`git commit -m "mensaje"`**, Git toma los archivos que estaban en Stage (agregados con `git add .`) y los **almacena en el historial como un punto de guardado permanente**, con un mensaje que describe los cambios realizados. A diferencia de Stage, donde solo hay archivos preparados, en el commit ya tenemos una **fotografía exacta del proyecto en ese momento**, registrada de forma cronológica en el historial de versiones.  

4. **Remote (en el servidor):**  
   Finalmente, llegamos al estado **Remote**, que representa el último paso del flujo de Git. Aquí tomamos las confirmaciones locales (commits) junto con su historial de cambios y las **subimos a un repositorio remoto**, como **GitHub, GitLab o Bitbucket**. Para ello utilizamos el comando **`git push`**, el cual envía toda la información al servidor remoto. Cabe destacar que para que esto funcione correctamente debemos haber **configurado previamente las credenciales** y conectado nuestro repositorio local al remoto.  

# ☄️ Git: add, status, comit

## ➕ git add  
  El comando **`git add`** se utiliza para **mover archivos de estado local a Stage**, de modo que Git comience a darles seguimiento. También sirve para **actualizar versiones de archivos que ya están en Stage** si han sido modificados o eliminados. Este comando cumple una función crucial, ya que **si no pasamos archivos de Local a Stage, estos nunca podrán ser registrados en un commit** (es decir, en una versión o copia del historial). Además, si los archivos ya están en Stage y realizamos cambios, **estos cambios no se registrarán en el próximo commit** a menos que volvamos a ejecutar `git add` para actualizar el Stage.  

  Algunas formas de usarlo:  
  - `git add <nombreArchivo>`: agrega un archivo específico al Stage.  
  - `git add <nombreCarpeta>/`: agrega todos los archivos dentro de esa carpeta al Stage.  
  - `git add .`: agrega **todos los archivos y carpetas del proyecto** al Stage, incluyendo los nuevos y los modificados.

Un ejemplo deñ uso de **`git add`** en la terminal es el siguiente:

```bash
chris@LAPTOP-0DNMOIV6 MINGW64 /d/Trabajos/Cursos/Git-GitHub-Course (main)
$ git add decription.txt
```

## 🔀 git commit  
El comando **`git commit`** se utiliza para **realizar un registro o “fotografía” del código** dentro del historial de versiones de Git. Este comando **toma los archivos que están confirmados en el área de Stage** (agregados mediante `git add`) y crea una nueva versión del proyecto.  Si existen archivos en Stage que fueron modificados después del último `git add`, pero **no se volvieron a agregar**, Git los **ignorará** al momento de realizar el commit, tomando como referencia **la versión anterior** que fue registrada con el último `git add`.  En otras palabras, **un commit guarda el estado actual del proyecto**, tomando en cuenta únicamente los archivos **agregados, modificados o eliminados** desde el último commit, **siempre y cuando estén en Stage**.  

Estos commits son **locales**, es decir, se almacenan únicamente en el repositorio de tu máquina. Sin embargo, posteriormente pueden **subirse a un repositorio remoto**, como **GitHub**, lo que permite sincronizar los cambios y compartir el trabajo con otros desarrolladores.  

Una ventaja importante de los commits es que **actúan como puntos de control o versiones de respaldo** del proyecto. Gracias a ellos, podemos:  
- **Volver a versiones anteriores** del código en caso de errores.  
- **Comparar diferencias** entre versiones para analizar cambios.  
- **Visualizar modificaciones o eliminaciones específicas**.  

Comúnmente, el comando **`git commit`** se acompaña del parámetro **`-m`**, el cual significa **message (mensaje)**. Esto se debe a que **todo commit debe tener un mensaje descriptivo** que permita identificar fácilmente los cambios realizados en esa versión. Cabe destacar que **el formato y estilo del mensaje del commit pueden variar** dependiendo de **las normas de la empresa, el equipo de desarrollo o las preferencias personales** del programador. Algunas organizaciones establecen convenciones estrictas (como usar prefijos tipo `feat:`, `fix:`, `refactor:` o `docs:`), mientras que otras permiten mensajes más libres siempre que sean claros y coherentes. Pero por lo general, se escribe una descripción **breve y clara** del propósito del commit, como por ejemplo:  
- `"Se corrigió el bug en la función de login"`  
- `"Se agregó el archivo README.md"`  
- `"Se optimizó el código de validación de formularios"`  


Cuando se ejecuta un commit, Git mostrará en la consola un **resumen informativo**, donde se incluye:  
- La **rama actual** en la que se hizo el commit.  
- El **identificador único (hash)** del commit creado.  
- El **número de archivos afectados**.  
- La **cantidad de inserciones, eliminaciones o modificaciones de líneas**.  

Este mensaje de confirmación indica que **el commit se ha realizado correctamente**, y nos brinda una visión rápida de los cambios registrados. Por lo que un ejemplo de un commit exitoso junto con su mensaje de confirmacion es el siguiente:

```bash
chris@LAPTOP-0DNMOIV6 MINGW64 /d/Trabajos/Cursos/Git-GitHub-Course/Course (main)
$ git commit -m "Update: Git Commit Description"
[main 797cfda] Update: Git Commit Description
 1 file changed, 2 insertions(+)
```

## 📊 git status  
   El comando **`git status`** es una herramienta fundamental en Git que nos permite **consultar el estado actual de los archivos dentro del repositorio**. Con este comando podemos saber exactamente **qué archivos han sido modificados, cuáles están sin seguimiento (untracked), cuáles están en Stage y cuáles están listos para ser confirmados (commiteados)**. Por ejemplo, cuando ejecutamos `git status`, Git analiza el directorio de trabajo y nos muestra información sobre los cambios realizados desde la última confirmación (`commit`). Por lo que un ejemplo de cómo se visualiza el uso del comando `git status` seria el siguiente:

   ```bash
   chris@LAPTOP-0DNMOIV6 MINGW64 /d/Trabajos/Cursos/Git-GitHub-Course (main)
   $ git status
   On branch main
   Your branch is up to date with 'origin/main'.
   
   Changes not staged for commit:
    (use "git add <file>..." to update what will be committed)
    (use "git restore <file>..." to discard changes in working directory)
          modified:   Course/README.md

   Untracked files:
    (use "git add <file>..." to include in what will be committed)
          Practices/

   no changes added to commit (use "git add" and/or "git commit -a")
   ```

Ahora bien, pueden existir diferentes situaciones y funciones dentro del flujo de Git que pueden resultar confusas al principio, especialmente al manejar nuestros archivos. Aquí es donde **`git status`** se convierte en una herramienta clave, ya que nos permite **ubicar fácilmente el estado de nuestros archivos y entender qué acciones podemos tomar**. Recordemos que los **4 estados del flujo de Git** son: **local (sin seguimiento)**, **stage (marcados)**, **commit (fotografiados)** y **remote (en el servidor)**.  

### Archivos en estado Local (sin seguimiento)  
Cuando nuestros archivos están en el estado **local**, Git aún no les está dando seguimiento. En este caso, **`git status` nos mostrará una recomendación para usar `git add .`**, indicando que debemos agregarlos al Stage para comenzar a rastrearlos.  Es importante destacar que si hacemos un commit antes de agregar los archivos, **Git no los incluirá**, ya que aún no están marcados.  Ejemplo de cómo se mostraría un archivo local sin seguimiento:  

```bash
Untracked files:
  (use "git add <file>..." to include in what will be committed)
        Practices/
   ```

### Archivos en estado Stage (marcados)  
Una vez que marcamos nuestros archivos con `git add`, pasan al estado **Stage**, donde Git los observa para incluirlos en el próximo commit. Al ejecutar **`git status`** en este caso, la consola nos indicará que **hay cambios listos para ser confirmados**. Además, Git nos muestra sugerencias útiles, como **usar `git restore --staged` para desmarcar archivos y quitarles el estado Steg, regresandolos a estado local, esto sin alterar su contenido**. Ejemplo de cómo se muestra en la consola:  

 ```bash
   Changes to be committed:
  (use "git restore --staged <file>..." to unstage)
        new file:   "practices/\342\230\204\357\270\217 Git add, status, comit/file.txt"
   ```

### Acciones posibles en Stage antes de Commit  
Con los archivos ya en **Stage**, existen dos posibilidades:  

1. **Realizar un commit**:  
   Esto crea una “fotografía” de los archivos actuales, registrando los cambios en el historial de Git.  

2. **Modificar o eliminar archivos antes del commit**:  
   Si realizamos cambios en los archivos ya marcados, **`git status`** nos mostrará cuáles archivos han sido modificados o eliminados, y nos dará sugerencias de las posibles acciones que podemos realizar:  

   - **Agregar nuevamente los archivos modificados** con `git add .`:  
     Git nos dará esta sugerencia para incluir los cambios en el próximo commit. Esto es importante porque, si hacemos un commit sin agregar los archivos modificados, Git registrará y creará el commit en base a la versión **anterior** de los archivos, dejando fuera los cambios recientes.  

   - **Eliminar archivos** del proyecto usando `git rm`:  
     Git nos sugerirá esta acción para eliminar archivos tanto del Stage como del disco, reflejando correctamente la intención de borrarlos del proyecto. En caso de que un archivo eliminado ya estuviera en alguna versión previa del historial, al realizar un commit con el archivo eliminado, este dejará de aparecer en la versión más reciente del proyecto.  

   - **Quitar archivos del Stage** sin eliminarlos del proyecto usando `git restore --staged <file>`:  
     Esta acción mantiene los archivos dentro del proyecto, conservándolos en el directorio, pero **sin seguimiento temporal en Stage**. Mientras permanezcan fuera del Stage, los cambios no se incluirán en el próximo commit hasta que volvamos a agregarlos.  

   - **Restaurar archivos a la versión previamente agregada o del último commit** usando `git restore <file>`:  
     Esta acción nos permite restaurar nuestros archivos a una versión anterior antes de las modificaciones. Puede tomar como referencia la última versión guardada mediante un **commit** o la versión actual en **Stage** (después de un `git add .`). Si el archivo fue eliminado, se restaurará; si fue modificado, volverá al contenido de la versión previa.

     Ejemplo de cómo se muestran los cambios de archivos marcados con modificaciones o eliminados sin commit:  

     ```bash
     Changes not staged for commit:
          (use "git add/rm <file>..." to update what will be committed)
          (use "git restore <file>..." to discard changes in working directory)
                deleted:    "practices/\342\230\204\357\270\217 Git add, status, comit/file1.txt"
                modified:   "practices/\342\230\204\357\270\217 Git add, status, comit/file2.txt"
     ```

     Ahora bien, cuando realizamos un **commit** y se suben todos nuestros archivos a dicho commit —es decir, cuando absolutamente **todo lo que está en Stage ha sido actualizado y registrado correctamente**—, al ejecutar nuevamente el comando **`git status`**, Git nos mostrará un mensaje indicando que **no hay nada nuevo para confirmar (commit)**. Esto significa que **no existen cambios pendientes**, ya que todos los archivos fueron incluidos en el último commit y el estado del repositorio está completamente sincronizado. Por lo tanto, la consola mostrará un mensaje similar al siguiente:

     ```bash
     chris@LAPTOP-0DNMOIV6 MINGW64 /d/Trabajos/Cursos/Git-GitHub-Course/Course (main)
     $ git status
     On branch main
     Your branch is ahead of 'origin/main' by 1 commit.
       (use "git push" to publish your local commits)

     nothing to commit, working tree clean
     ```

## ✂️ Forma corta de Git Status
Adicionalmente, cabe mencionar que existe una forma **simplificada y resumida** de visualizar el estado del repositorio usando el comando:

```bash
git status -s
```

Esta variante del comando **muestra un resumen compacto** de los archivos modificados, agregados, eliminados o en diferentes estados dentro del repositorio.  
En lugar de mostrar un desglose largo y detallado como el `git status` normal, esta versión utiliza **símbolos específicos** para indicar rápidamente el tipo de modificación o el estado del archivo. Por ejemplo, si vemos algo como:

```bash
 M Course/README.md
```

La letra **`M`** indica que ese archivo fue **modificado**, por lo que está pendiente de ser agregado al Stage o de ser confirmado en un commit. Este formato es ideal cuando se quiere tener una vista rápida del estado del repositorio sin saturarse con información detallada. Ejemplo real dentro de Git Bash:

```bash
chris@LAPTOP-0DNMOIV6 MINGW64 /d/Trabajos/Cursos/git-github-course (main)
$ git status -s
 M Course/README.md
```

## 📌 Símbolos comunes en `git status -s`
Git utiliza diferentes símbolos para indicar de forma rápida lo que ocurrió con cada archivo.  
Los más comunes son:

- **M** → *Modified (modificado)*  
  Indica que el archivo ha sido modificado en el área de trabajo (working directory).

- **M** a la izquierda y espacio a la derecha → *Modificado en Stage*  
  Significa que el archivo fue agregado al Stage con `git add`, pero volvió a modificarse después.

- **A** → *Added (agregado)*  
  Indica que es un archivo nuevo que ya ha sido agregado al Stage.

- **??** → *Untracked (sin seguimiento)*  
  Significa que el archivo no está siendo rastreado por Git; está en estado local.

- **D** → *Deleted (eliminado)*  
  Indica que el archivo fue eliminado del proyecto.

- **R** → *Renamed (renombrado)*  
  Indica que un archivo fue cambiado de nombre.

- **UU** → *Unmerged (conflicto)*  
  Aparece cuando existe un conflicto durante un merge.

# 😑 Git Ignore
Git maneja una herramienta muy útil que consiste en un archivo llamado **`.gitignore`**, el cual es un archivo de configuración donde podremos introducir **todos los nombres de archivos y carpetas que queremos que Git ignore completamente**.  
Esto significa que Git **jamás les tomará foto**, **no les dará seguimiento**, **no aparecerán en `git status` como archivos para agregar**, y además **nunca serán subidos a un repositorio remoto**. Es importante aclarar que, aunque Git ignore estos archivos, **el archivo `.gitignore` sí debe agregarse al Stage y subirse al repositorio remoto**, ya que es precisamente este archivo el que instruye a Git (y a otros colaboradores) qué elementos deben omitirse dentro del proyecto.

## 🤔 ¿Por qué se usa este archivo?
El archivo `.gitignore` se usa principalmente para **evitar subir archivos que no deben formar parte del repositorio**, ya sea por motivos de seguridad, porque se generan automáticamente o porque simplemente no tienen relevancia en el control de versiones. Entre sus usos más comunes encontramos:

- **Evitar subir credenciales sensibles o privadas**, como archivos `.env`, tokens, API keys, configuraciones locales, etc.  
- **Evitar subir carpetas generadas automáticamente**, como `node_modules/` o dependencias de otros entornos.  
- **Ignorar archivos o carpetas que se regeneran al ejecutar el proyecto**, como logs, cachés, configuraciones temporales o archivos de compilación.  
- **Mantener limpio el historial del proyecto**, evitando que versiones innecesarias saturen el repositorio o compliquen la colaboración con otras personas.

El archivo `.gitignore` evita pérdidas de seguridad, reduce el tamaño del repositorio y mejora considerablemente la organización del proyecto.


## 📄 Cómo crear el archivo `.gitignore`
Para crear o generar un archivo `.gitignore`, simplemente debemos **crear un archivo nuevo con ese mismo nombre** dentro del proyecto. Este archivo debe colocarse **en la carpeta raíz del repositorio**, para que su configuración afecte a todos los archivos y carpetas del proyecto. En caso de tener múltiples módulos o proyectos dentro de un mismo repositorio, se pueden crear varios `.gitignore`, pero el general siempre debe estar en la raíz.

## 📁 Declaración de archivos y carpetas a ignorar
El funcionamiento del archivo `.gitignore` es muy sencillo:  
**solamente escribimos la ruta del archivo o la carpeta que deseamos ignorar**, y Git dejará de rastrear esa información automáticamente. Esto es muy útil cuando deseamos no subir cierto contenido por temas de seguridad, privacidad, organización o simplemente porque no es necesario para el repositorio.

### Ejemplo para ignorar un archivo dentro de una carpeta
Al especificar un archivo en `gitignore` Git ignorará ese archivo específico.
```bash
styles/style.css
```

### Ejemplo para ignorar una carpeta completa
Al especificar una carpeta dentro de `gitignote`, **toda la carpeta y todo su contenido** será ignorado por Git sin necesidad de escribir cada archivo manualmente.

```bash
styles
```

## 🎴 Uso de comodines
Dentro del archivo `.gitignore` podemos utilizar **comodines especiales**, que nos ayudan a ignorar tipos de archivos completos o patrones de nombres sin necesidad de escribirlos uno por uno. Esto es especialmente útil cuando manejamos muchos archivos multimedia o grandes cantidades de archivos generados automáticamente.

### Ejemplo de comodín por extensión
Podemos ignorar todos los archivos de un mismo formato usando la extension y con esto Git ignorará absolutamente **todos los archivos** que terminen con esa extensión, sin importar en qué carpeta estén ubicados.

```bash
*.jpg
*.mp4
*.mp3
*.gif
```

# 🆚 Git Diff
Dentro de Git existe un comando muy útil llamado **`git diff`**, el cual nos permite **comparar el contenido de un archivo entre dos estados distintos**.  
Este comando se usa principalmente para visualizar los **cambios que existen en el Working Directory (local)** respecto a la versión de ese mismo archivo que ya fue agregada al **Stage** mediante `git add`. Esto significa que si un archivo ya está en Stage (es decir, Git ya tiene una “copia” lista para el siguiente commit) y luego realizamos nuevas modificaciones sin agregarlo nuevamente, `git diff` mostrará **exactamente qué cambió** entre la versión del Stage y la versión actual del archivo.

Con `git diff` podemos ver:
- Líneas **eliminadas**
- Líneas **modificadas**
- Líneas **agregadas**
- Diferencias específicas entre versiones antes de realizar un commit

Esto es extremadamente útil para revisar cambios antes de confirmarlos en un commit. Por lo que este es Ejemplo de uso real:

```bash
chris@LAPTOP-0DNMOIV6 MINGW64 /d/Trabajos/Cursos/git-github-course/course (main)
$ git diff
diff --git a/Course/texto.txt b/Course/texto.txt
index 37d8675..9f529c2 100644
--- a/Course/texto.txt
+++ b/Course/texto.txt
@@ -1 +1,3 @@
-Hola mundo
\ No newline at end of file
+Hola mundo
+
+¿como estan?
\ No newline at end of file
```

## 📝 Explicación detallada línea por línea del resultado
Como se puede ver el comando `git diff` muestra diferentes lineas de codigo, por lo cual se explicara a continuacion cada una de ellas.

### `diff --git a/Course/texto.txt b/Course/texto.txt`
Esta línea indica **los dos archivos que se están comparando**, los cuales Git los compara como si fueran dos archivos distintos llamados *a* y *b*.
- `a/Course/texto.txt` → versión registrada en Stage (antes del cambio reciente)  
- `b/Course/texto.txt` → versión actual del archivo en el directorio de trabajo  

### `index 37d8675..9f529c2 100644`
Esta línea de codigo muestra:

- Los **hashes internos** de Git que representan cada versión del archivo.
- El número final (`100644`) indica permisos del archivo (normal en archivos de texto en Git).

Por lo que no hay que preocuparse o tomar mucha atencion a esto, ya que es metadata de Git.

### `--- a/Course/texto.txt`
El archivo con el prefijo `---` representa la **versión anterior** (la que está en Stage).  
Git lo marca con un signo “–” (menos) porque es la versión “vieja”.

### `+++ b/Course/texto.txt`
El archivo con el prefijo `+++` representa la **versión nueva** (la que está en local).  
Git lo marca con “+” porque contiene los nuevos cambios.

### `@@ -1 +1,3 @@`
Esta línea forma parte del encabezado del bloque de cambios que Git muestra cuando usamos `git diff`.
Su propósito es indicar **desde qué línea comienzan las modificaciones** y **cuántas líneas están involucradas**, tanto en la versión anterior como en la versión actual.

- **`-1`** → Indica que en la **versión anterior** el cambio inicia en la **línea 1**.
- **`+1,3`** → Indica que en la **nueva versión** el cambio también comienza en la **línea 1**, pero además especifica que ahora **hay 3 líneas en total** dentro del bloque modificado.

En pocas palabras, Git usa estos números para saber **dónde empezaron los cambios** y **cuántas líneas se agregaron o forman parte del nuevo contenido**.

### `-Hola mundo`
El signo **`-`** al inicio indica que esta línea **fue eliminada** o reemplazada respecto a la versión previa. Sin embargo, en este caso verás que en la versión nueva también aparece, por lo que en realidad Git lo muestra así porque detectó cambios en el bloque del archivo.

### `+Hola mundo`
El signo **`+`** indica que esta línea **forma parte de la versión nueva**. Aunque el texto es el mismo, aparece como nueva porque forma parte de un bloque de líneas que sufrió cambios.

### `+`
Línea vacía agregada. Git la marca como nueva porque **esa línea antes no existía**.

### `+¿como estan?`
Otra línea agregada. El signo **`+`** indica que esta línea **no existía en la versión previa (Stage)** y fue añadida en el Working Directory.

### `\ No newline at end of file`
Esto indica que **el archivo no terminaba con una línea vacía**. No es un error, solo una advertencia visual común de Git.

> ⚠️ *OJO: Git solo muestra las líneas que fueron modificadas*, agregadas o eliminadas; **no muestra todo el contenido del archivo**, únicamente el fragmento involucrado en el cambio junto con con unas pocas líneas de contexto alrededor de los cambios.*

# </> Git Log  
Git, además de manejar comandos para visualizar el estado de los archivos que están siendo rastreados, modificados o en Stage, también cuenta con un comando muy útil que nos permite ver **un listado completo del historial de commits** realizados en nuestro proyecto. Ese comando es **`git log`**, el cual muestra información detallada sobre cada commit registrado en el repositorio. Sin embargo, para muchos usuarios al principio puede resultar **verboso, largo o incluso confuso**, ya que muestra bastante información y además, una vez ejecutado, es necesario usar un comando especial para **salir de la vista del historial y regresar a la consola Bash** con normalidad.

## 👁️‍🗨️ Información que muestra `git log`

Cuando se utiliza el comando **`git log`**, Git despliega una estructura muy clara y consistente. Cada commit se muestra con **cuatro elementos fundamentales**, los cuales nos permiten identificar completamente la información del registro. Los cuales se presentan a continuación.

1. **Clave del commit (Commit Hash):**  
   Git muestra una clave o código largo compuesto por caracteres alfanuméricos. Este código es el identificador único del commit, conocido como **hash del commit**, y permite acceder exactamente a ese punto del historial. Además, Git también puede mostrar la **rama** en la que se realizó ese commit.

2. **Autor del commit:**  
   En esta sección aparecen los datos del usuario que realizó el commit, incluyendo:  
   - **Nombre del autor** configurado en Git.  
   - **Correo electrónico** asociado a la cuenta.  

   Esto es fundamental en proyectos colaborativos para saber quién realizó cada cambio.

3. **Fecha y hora del commit:**  
   Git muestra la fecha exacta en la que se creó ese commit, incluyendo la hora con su zona horaria. Esto permite rastrear cuándo fue realizado cada cambio en el proyecto.

4. **Mensaje del commit:**  
   Finalmente, aparece la descripción o mensaje que el usuario ingresó con el parámetro `-m` al realizar el commit. Este mensaje debe describir de forma breve y clara el propósito del cambio registrado.

## 🪖 Orden de los commits en `git log`
El historial que muestra `git log` **siempre aparece ordenado del commit más reciente al más antiguo**.  
Es decir:

- El primer commit que aparece arriba del todo es **el último que se realizó**.
- El segundo es el **penúltimo**.
- Y así sucesivamente, descendiendo en orden cronológico hacia los commits más antiguos.

Gracias a este orden, es muy sencillo identificar de inmediato cuál fue la última versión registrada del proyecto.

## 🎯 ¿Qué significa HEAD en `git log`?
Cuando Git muestra un commit acompañado de la palabra **HEAD**, esto indica que:

- Ese commit es **el último commit realizado en la rama actual**.
- Es el commit **en el que te encuentras parado actualmente**, es decir, el que tu repositorio está usando como referencia en ese momento.

HEAD siempre apunta al commit activo, lo que permite saber con exactitud en qué versión del código estamos trabajando en ese instante.

## 🖥️ Ejemplo del uso de `git log`
Una vez que se ejecuta el comando `git log` dentro de la consola, se podrá visualizar el historial de commits realizados junto con su información correspondiente por cada commit.

```bash
chris@LAPTOP-0DNMOIV6 MINGW64 /d/Trabajos/Cursos/git-github-course (main)
$ git log
commit 8069095a752b0e6f59f10a44d3ba35fdfa6368dc (HEAD -> main, origin/main)
Author: Chris Alegria <christian.alegriar@gmail.com>
Date:   Mon Nov 17 17:02:34 2025 -0600

    Add: Short Status Command Section

commit 6fba1d3e05fd494973913478156efaa1e6582971
Author: Chris Alegria <christian.alegriar@gmail.com>
Date:   Mon Nov 17 16:39:15 2025 -0600

    Add: Git Diff Section

commit 7297de953740b4c6fe1fcea37fd623fd07e3113f
Author: Chris Alegria <christian.alegriar@gmail.com>
Date:   Mon Nov 17 16:25:44 2025 -0600
```

## ✂️ Forma corta de Git Log
Existe una **forma corta de `git log`** que nos permite visualizar nuestro historial de commits **mostrando únicamente un commit por línea**, lo cual resulta muy útil cuando queremos una vista rápida, compacta y limpia del historial. Sin embargo, este método tiene una **limitante importante**, ya que solo nos mostrará **el código (hash) del commit** —que es el identificador único con el que Git registra dicho commit— y **el mensaje o descripción** que se colocó al momento de crearlo. Es decir, no muestra autor, fecha, ni detalles adicionales. Para utilizar esta forma corta, simplemente debemos agregar el parámetro `--oneline`, quedando el comando completo como:

```bash
git log --oneline
```

Una vez ejecutado, Git nos devolverá un listado de commits en una sola línea por cada uno, mostrando únicamente:
- El **código** del commit (hash abreviado).  
- El **nombre o descripción** del commit.  

Una vez ejecutado, el resultado será un **historial compacto** que facilita mucho la navegación entre versiones, mostrando unicamente los 2 puntos/aspectos mencionados anteriormente. Mostrandose en cosola algo parecido a lo que se muestra a continuacion.

```bash
chris@LAPTOP-0DNMOIV6 MINGW64 /d/Trabajos/Cursos/git-github-course (main)
$ git log --oneline
0a10183 (HEAD -> main, origin/main) Update: Git Log Section With Some Note Fixes
2446537 Update: README to clarify Git line modification
46b6bc2 Update: Note At Git Diff Section
3ad93e7 Add: Gti Diff Section
8069095 Add: Short Status Command Section
6fba1d3 Add: Git Diff Section
7297de9 Add: Git Ignore Section
904301e Delete: Spaces In General README
f6e672f Update: Spaces
91d38c0 Delete: Spaces
46aa6a8 Delete: Spaces At Principal README
101e193 Delete: Space
afb5f36 Update: Space
dc85cee Add: Git Ignore Section
8cf93a9 Update: Git Commit Information
:
```

# 🌿 ¿Qué es una Branch (Rama)?
Una **branch** o **rama** dentro de un proyecto en Git puede parecer un concepto complicado al inicio, pero existe una forma muy sencilla y visual de entenderlo.

Imaginemos que somo el **director de una película**, y que esta película tiene su propio **expediente** donde se va guardando todo el material. Ahora piensa que **cada commit es como un “frame” o una toma grabada**. La toma más reciente —el último commit— sería el frame donde actualmente está la película (*HEAD*).

Ahora bien, una **rama** en Git sería como **una versión diferente de esa misma película**. En el expediente principal puedes tener **más de una versión de la película**, tal como sucede en la vida real, donde existen escenas alternativas, finales extendidos, cortes del director, etc.

Por ejemplo:  
Podemos tener una película con 20 frames (commits) ya grabados, y a partir de ese frame 20 podemos crear **tres versiones diferentes**. Todas comparten los mismos 20 frames iniciales, pero a partir de ahí cada versión toma un rumbo distinto: nuevas escenas, cambios, adiciones, pruebas, etc.

Sin embargo, siempre existe **una película principal**, la que finalmente se estrenará en el cine. Las otras versiones (ramas) se crean **para experimentar, probar ideas, desarrollar partes por separado o permitir que distintos integrantes del equipo trabajen sin afectar la película principal**.

Lo mismo ocurre en Git:  
Dentro de nuestro proyecto podemos crear **múltiples ramas**, que representan **caminos alternos al camino principal**. Cada rama tiene sus propios commits y se crea a partir de **cualquier commit** de la rama principal.

Estas ramas pueden utilizarse para múltiples propósitos, como:  
- Trabajar una sección específica del proyecto.  
- Permitir que un integrante del equipo desarrolle una función sin afectar el código estable.  
- Crear versiones alternativas del proyecto para ver cuál funciona mejor.  
- Realizar pruebas sin riesgo.

Al final, el líder del equipo (o tú mismo) decide si **integrar esas versiones alternativas a la película principal**, y esto se hace mediante un **merge**, que combina los cambios de una rama externa con la rama principal.

La rama principal suele llamarse **master** o **main**, y su finalidad típica es ser la versión del código **estable, final o lista para producción**. En cambio, las ramas adicionales se usan para **desarrollo, pruebas, ideas, correcciones, nuevas funciones**, etc.

En resumen:  
**Una branch es una línea alterna de trabajo que parte de un punto específico del proyecto y permite desarrollar cambios sin afectar directamente a la versión principal.**

# 📝 Git Branch, Checkout & Merge
Como se mencionó anteriormente, Git cuenta con un **sistema de ramas**, las cuales representan **versiones alternas del código** que pueden desarrollarse de forma independiente y, en algún momento, **integrarse con la versión principal** del proyecto. Gracias a las ramas, es posible trabajar en nuevas características, funciones o pruebas sin afectar el código principal. Por lo general, esa rama principal se llama **master** o **main**, y a partir de ella podemos crear otras ramas donde trabajaremos de manera aislada. Para gestionar este sistema de ramas, Git utiliza tres comandos fundamentales: **`git branch`**, **`git checkout`** y **`git merge`**.  A continuación se explica cada uno con detalle:

## 🌳 Git Branch
El comando **`git branch`** es muy sencillo de entender, pero extremadamente importante. Su función es **mostrar el listado de ramas del proyecto** y señalar cuál es la rama en la que estamos trabajando actualmente. Cuando ejecutamos este comando, Git nos devolverá todas las ramas existentes en el repositorio, y marcará con un **asterisco** la rama activa en ese momento.  

Es importante mencionar que el resultado dependerá del proyecto que estemos trabajando:  
- En un **proyecto 1**, podrías estar trabajando sobre la rama `master`.  
- En un **proyecto 2**, podrías estar trabajando en una rama llamada `desarrolloPruebas`, `test-1`, `v2`, etc.

Cada proyecto puede tener sus propias ramas creadas según las necesidades del equipo o del usuario. A continuación, se presenta un ejemplo de cómo se visualiza este comando una vez ejecutado.

```bash
chris@LAPTOP-0DNMOIV6 MINGW64 /d/Trabajos/Cursos/git-github-course (main)
$ git branch
* main
ramaDePruebas
```

## ☑️ Git Checkout
El comando **`git checkout`** tiene **dos funciones principales**: **crear una nueva rama y cambiar a esta** dentro de nuestro proyecto y **cambiar** a una rama ya existente. A continuación se explica cada caso.

- **Crear y cambiar a una nueva rama (`git checkout -b nombreRama`):** Para crear una nueva rama y cambiarse a ella en un solo paso se usa la opción `-b`(branch). Es decir, `git checkout -b nombreRama` le indica a Git que **cree la rama** `nombreRama` y **cambie la rama activa** a esa nueva rama. Al ejecutar este comando, Git mostrará un mensaje confirmando que **se creó la rama** y que **se ha cambiado a ella**, indicándote que ahora se esta trabajando sobre la rama recién creada.

   ```bash
   chris@LAPTOP-0DNMOIV6 MINGW64 /d/Trabajos/Cursos/git-github-course (main)
   $ git checkout -b ramaDePruebas
   Switched to a new branch 'ramaDePruebas'
   ```

- **Cambiar a una rama existente (`git checkout nombreRama`):** Si la rama ya existe, simplemente se usa `git checkout nombreRama` para cambiar la rama activa. Git devolvera un mensaje confirmando que **se cambió a la rama indicada** y a partir de ese momento todos los cambios que se hagan estarán en esa rama.

   ```bash
   chris@LAPTOP-0DNMOIV6 MINGW64 /d/Trabajos/Cursos/git-github-course (ramaDePruebas)
   $ git checkout main
   Switched to branch 'main'
   Your branch is up to date with 'origin/main'.
   ```

Además de crear y cambiar ramas, `git checkout` **permite situarse en un commit específico** escribiendo el **identificador (hash)** del commit. Por ejemplo, al ejecutar `git checkout <hash>` se colocará el repositorio en el estado exacto de ese commit.

- **Efecto:**  
  Al ejecutar `git checkout <hash>` se pasa a un estado llamado **detached HEAD**, lo que significa que **no se está en ninguna rama** sino directamente apuntando a un commit histórico. En este estado se puede inspeccionar el código, ejecutar pruebas o compilar exactamente como estaba en ese punto del tiempo.

- **Precauciones importantes:**  
  - En **detached HEAD** los cambios no se asocian automáticamente a una rama. Si se realizan modificaciones y se desea conservarlas, **se debe crear una rama** a partir de ese estado (`git switch -c nombreNuevaRama` o `git checkout -b nombreNuevaRama`) antes de perder la referencia; de lo contrario, esas modificaciones pueden perderse al cambiar de rama.  
  - El uso de `git checkout <hash>` es principalmente **para inspección o recuperación rápida**. Para trabajar y mantener cambios suele ser mejor crear una rama desde ese commit y continuar el trabajo en la nueva rama.

- **Alternativa moderna:**  
  También existe la forma más explícita `git switch --detach <hash>`, que deja claro que se está entrando en un estado detached HEAD sin intención de mover una rama.

## 🔀 Git Merge
El comando **`git merge`** es uno de los más importantes dentro del flujo de trabajo en Git, ya que permite **unir los cambios de una rama secundaria con la rama principal**. En términos simples, este comando combina dos líneas de desarrollo diferentes para integrarlas en una sola versión final del proyecto. Para llevar a cabo un *merge*, se siguen los siguientes pasos:

1. **Colocarse en la rama principal:**  
   Para poder fusionar los cambios, primero **se debe asegurar** que se está ubicado en la rama que **recibirá** las modificaciones. Generalmente esa rama es **`main`** (o `master`, dependiendo del proyecto). Para posicionarse en esa rama, se utiliza el comando: `git checkout main`. Este comando coloca el proyecto en la rama principal, dejándola lista para recibir los cambios provenientes de otra rama.

2. **Ejecutar el merge:**  
   Una vez que se está en la rama principal, se procede a realizar la integración de cambios mediante: `git merge nombreRama`. Este comando toma todos los cambios registrados en **nombreRama** y los fusiona con los de la rama principal. Después de ejecutarlo, Git mostrará en consola una serie de líneas que indican cuáles archivos cambiaron, cuántas inserciones o eliminaciones se realizaron y cómo se integró el contenido entre ambas ramas. Estas líneas funcionan como un reporte detallado del proceso de fusión.

## 📝 Explicación detallada línea por línea del resultado
Ahora bien al ejecutar dicho comando nos arrojara un par de lineas de codigo las cuales se explicancion es:

### `Updating 6c2f8f7..442442f`
Esta línea indica que Git está **actualizando la rama actual** usando los cambios provenientes de otra rama.  
Los valores `6c2f8f7` y `442442f` representan los **hashes internos** de Git:

- El primer hash corresponde al **estado anterior** de la rama principal.  
- El segundo hash representa el **nuevo estado** después de aplicar los cambios.

En otras palabras, Git está diciendo: *“Tu rama pasó de esta versión… a esta otra nueva versión después del merge”*.

### `Fast-forward`
Esta línea indica que Git realizó un **merge de tipo *fast-forward***.  
Esto significa que:

- No hubo conflictos.  
- La rama principal **avanzó directamente** hasta alcanzar el mismo punto que la rama secundaria.  
- No fue necesario crear un commit adicional de merge.  

Es el tipo de combinación más simple y limpia.

### `Course/texto.txt    | 0`
Esta línea muestra la **ubicación del archivo** que fue parte de la combinación.  
El número `0` indica que **no hubo cambios** dentro del archivo (ni líneas agregadas ni eliminadas).  
Git lo lista porque formó parte del proceso, pero **su contenido permaneció igual** al fusionarse con la rama principal.

### `Practices/texto.txt | 3 +--`
Esta línea indica otro archivo involucrado en la fusión.

- El número `3` indica que Git detectó **3 líneas modificadas** en este archivo.  
- El símbolo `+` indica que **se agregó una línea**.  
- Los símbolos `--` indican que **se eliminaron dos líneas**.

En resumen: en este archivo **entró 1 línea nueva y salieron 2 líneas anteriores**.

### `2 files changed, 1 insertion(+)`
Esta línea expresa un pequeño resumen de lo que se modificó durante la fusión:

- Se modificaron **2 archivos**.  
- Hubo **1 inserción** total (una sola línea agregada entre todos los archivos).  

Git también incluye aquí las eliminaciones, pero solo indica explícitamente el número de inserciones.

### `delete mode 100644 Course/texto.txt`
Esta línea indica que Git **eliminó el archivo** `Course/texto.txt` durante la fusión.  
La palabra *mode* acompañada de `100644` representa los **permisos del archivo** antes de ser borrado (una configuración típica de archivos de texto).

En resumen: Git detectó que, según la otra rama, este archivo **ya no debía existir**, así que lo eliminó en la rama principal como parte del merge.

### `create mode 100644 Practices/texto.txt`
Esta línea indica que Git **creó un archivo nuevo** como resultado de la fusión: `Practices/texto.txt`.  
El modo `100644` vuelve a ser la metadata de permisos estándar.

Esto significa que la rama secundaria contenía un archivo que **no existía** en la rama principal y que, al fusionarse, Git lo añadió. Por lo que el código que arroja la terminal completo es el siguiente

```bash
chris@LAPTOP-0DNMOIV6 MINGW64 /d/Trabajos/Cursos/git-github-course (main)
$ git merge ramaDePracticas
Updating 6c2f8f7..442442f
Fast-forward
 Course/texto.txt    | 0
 Practices/texto.txt | 1 +
 2 files changed, 1 insertion(+)
 delete mode 100644 Course/texto.txt
 create mode 100644 Practices/texto.txt
```

> 👁️ *Dato:* Al ejecutar **`git log`** después de realizar un **`git merge`**, puede aparecer una línea similar a: `commit 442442f988a0e37d1f6d65913a7ad74f1232bb4e (HEAD -> main, origin/ramaDePracticas, ramaDePracticas)`. Esto indica que, tras la fusión, **tanto la rama principal (`main`) como la rama secundaria (`ramaDePracticas`) apuntan exactamente al mismo commit**. En otras palabras, ambas ramas quedaron **sin diferencias** y comparten el mismo punto en la historia, por lo que Git marca el commit como **HEAD** para ambas. Esto ocurre porque al fusionarse, sus contenidos quedaron completamente alineados.

> ⚠️ *OJO:* Algunos editores como **Visual Studio Code**, en la parte inferior de la ventana, muestran **el nombre de la rama en la que se está trabajando actualmente** &nbsp; <img src="assets/images/visual_studio_code/img_1.png" width="40"></img> &nbsp;. Esto es útil para verificar rápidamente si se está en `main`, en una rama de desarrollo o en cualquier otra rama del proyecto.

# ⌨️ Git en Visual Studio Code
Git no solo se puede manejar desde la consola: editores como **Visual Studio Code** (VS Code) incluyen herramientas integradas que permiten realizar tareas como crear commits, manejar ramas, visualizar cambios e incluso subir commits al repositorio remoto. Estas funciones brindan **alternativas más visuales y accesibles**, facilitando el flujo de trabajo del desarrollador. A continuación se explica cómo funciona el soporte de Git dentro de Visual Studio Code y cómo interpretar cada una de sus ayudas visuales.

## 🎨 Indicadores visuales en el explorador de archivos
Cuando un proyecto ya fue inicializado con Git (`git init`), VS Code comienza a mostrar **colores e íconos especiales** en el explorador lateral de archivos. Por ejemplo, si se crea un archivo nuevo que **todavía no está en stage**, VS Code lo marcará con un color **verde**, indicando que es un archivo **nuevo**, sin seguimiento y sin haber sido agregado aún.
<br>
<br>
<p align=center>
	<img src="assets/images/visual_studio_code/img_2.png" width="200"></img>
</p>

## 🧭 Panel de *Source Control* (Control de versiones)
En la barra lateral izquierda, junto al icono del explorador de archivos, se encuentra el botón del **Source Control**, que abre el panel donde VS Code gestiona las funciones relacionadas con Git. Este panel permite:

- Visualizar archivos modificados  
- Identificar archivos en *stage* o fuera de él  
- Escribir mensajes de commit  
- Hacer *stage* o *unstage* de archivos  
- Ver diferencias entre versiones  

<br>
<p align=center>
	<img src="assets/images/visual_studio_code/img_3.png" width="200"></img>
</p>

## 📂 Secciones: *Staged Changes* y *Changes*
Dentro del panel de control de versiones, los archivos modificados se organizan en dos áreas:

### **🔵 Staged Changes**
Aquí aparecen los archivos que **ya fueron agregados a stage** mediante un `git add`. Estos archivos están **listos para ser incluidos** en un commit.

### **🟡 Changes**
Aquí se muestran:
- Archivos modificados **pero aún sin agregar a stage**.  
- Archivos que *ya están en stage*, pero recibieron **modificaciones adicionales** sin stagear.

A la derecha del nombre de cada archivo, VS Code muestra una **letra** indicando el tipo de cambio:

- **A** → Archivo agregado al proyecto (nuevo).  
- **M** → Archivo modificado.  
- **U** → Archivo sin seguimiento (*untracked*).  

Estos indicadores ayudan a entender qué tipo de modificación ocurrió en cada archivo.

<br>
<p align=center>
	<img src="assets/images/visual_studio_code/img_4.png" width="200"></img>
</p>

## 👁️ Visualización dentro del explorador de archivos
Los mismos indicadores también aparecen en el explorador de archivos general, junto a los nombres de los archivos del proyecto:

- Archivos **nuevos, sin estar en stage** se muestran marcados en **verde**.  
- Archivos **modificados** se muestran marcados en **amarillo**.  
- Archivos que ya están **stageados** se muestran en **azul**.  

Esto permite reconocer el estado de cada archivo sin necesidad de entrar al panel del control de versiones.

<br>
<p align=center>
	<img src="assets/images/visual_studio_code/img_5.png" width="200"></img>
</p>

## 🧩 Git add, restore & rm en Visual Studio Code
Dentro del panel de **Source Control**, donde aparece el listado de archivos **modificados** o **en Stage**, Visual Studio Code incluye una serie de botones a la derecha del nombre de cada archivo. Estos botones permiten realizar acciones rápidas sin necesidad de usar la terminal. A continuación se explica cada uno:

1. Botón con ícono de **hoja (🗎):** Este botón **abre el archivo** directamente en el editor. Es útil cuando se desea revisar su contenido antes de decidir si agregarlo a Stage o descartar los cambios.

2. Botón con ícono de **flecha curva (↩):** Este botón permite **descartar los cambios realizados** en el archivo. Al presionarlo, el contenido del archivo regresará a su **última versión en Stage**, es decir, volverá al estado previo a la modificación. Es equivalente a usar el comando:

   - `git restore <archivo>`  

3. Botón con ícono de **más (+):** Este botón sirve para **agregar el archivo a Stage**, marcándolo para que sea incluido en el próximo commit. Al presionarlo, el archivo pasa del apartado **Changes** al apartado **Staged Changes**.


### 🔽Caso especial para archivos en Stage
Cuando un archivo **ya está en Stage**, el botón de “+” ya no aparece. En su lugar aparece un botón con icono de **menos (–)**.

1. **Botón con menos (–):** Este botón sirve para **quitar el archivo del Stage**, regresándolo al apartado de **Changes**, sin borrar su contenido. Es equivalente a ejecutar:

   - `git restore --staged <archivo>`

<br>
<p align="center">
	<img src="assets/images/visual_studio_code/img_6.png" width="200"></img>&nbsp;
	<img src="assets/images/visual_studio_code/img_7.png" width="200"></img>
</p>

## 📝 Vista de diferencias (*Diff*)
Si se selecciona un archivo marcado con **M** (modificado) dentro del Source Control, VS Code abrirá automáticamente una vista dividida:

- **Panel izquierdo:** muestra el contenido del archivo **antes de la modificación**.  
- **Panel derecho:** muestra **la versión actual**, es decir, los cambios realizados.  

Esta herramienta es muy útil para revisar qué líneas fueron agregadas, cambiadas o eliminadas antes de confirmar un commit.

<br>
<p align=center>
	<img src="assets/images/visual_studio_code/img_8.png" width="350"></img>
</p>

## 🔄 Restaurar cambios desde el Diff
En la vista del *diff*, específicamente **en el panel derecho**, donde aparecen los cambios actuales, Visual Studio Code añade un pequeño botón en forma de **flecha curva** o de **tres puntos** junto a cada línea o bloque modificado. Esta opcion sirve para:

- **Restaurar la línea** a su versión anterior  
- **Revertir solo ese cambio específico**, sin afectar el resto del archivo  
- Facilitar correcciones rápidas sin usar comandos en la terminal  

En pocas palabras: si una modificación no convence, basta con **dar clic en la flecha o los tres puntos** para regresar esa línea exactamente a como estaba antes del cambio.

<br>
<p align="center">
	<img src="assets/images/visual_studio_code/img_9.png" width="350" center></img>
</p>

## 🪛 Realización de commits
Dentro del mismo apartado de **Source Control** se encuentra un campo para escribir el **mensaje del commit**. El placeholder suele mostrar algo como `Message (Ctrl+Enter to commit on ...)`. Junto a ese campo aparece un **botón largo azul claro con una palomita (✓)**: ese botón **confirma el commit** y guarda los cambios stageados con el mensaje escrito. A la derecha del botón principal hay una **flecha ▼** que despliega varias opciones de commit. Estas opciones permiten realizar tipos de commit específicos, por ejemplo:

- **Commit**: confirma los cambios localmente.  
- **Commit & Push**: confirma los cambios y los envía al remoto en un solo paso.  
- **Commit & Sync**: hace el commit y sincroniza las diferencias entre el remoto y el local (pull + push según corresponda).

Además, se puede usar el atajo **Ctrl+Enter** (o la combinación que muestre el editor) para confirmar rápidamente el commit desde el campo del mensaje.

<br>
<p align="center">
  <img src="assets/images/visual_studio_code/img_10.png" width="200" center></img>
</p>

### ¿Qué pasa después de hacer un commit?
Al confirmar el commit, la lista de cambios en el panel de Source Control **se vacía** (los archivos pasan de Staged/Changes a estar registrados en el historial). En el lugar del listado quedará un **botón azul** que ofrece acciones según el estado del repositorio remoto:

- **Si no hay repositorio remoto conectado:** el botón mostrará **“Publish Branch”** (Publicar rama), permitiendo crear el repositorio remoto y subir la rama por primera vez.  
- **Si ya está conectado a un remoto:** el mismo botón ofrecerá opciones para **sincronizar** (push/pull) y subir los commits al repositorio remoto.

<br>
<p align="center">
  <img src="assets/images/visual_studio_code/img_11.png" width="200"></img>&nbsp;
  <img src="assets/images/visual_studio_code/img_12.png" width="200"></img>
</p>

## 🌳 Crear ramas
En Visual Studio Code, en la **esquina inferior izquierda**, aparece un **icono de ramas** acompañado del **nombre de la rama actual** en la que estamos trabajando. &nbsp;<img src="assets/images/visual_studio_code/img_1.png" width="40"></img>&nbsp;. Si hacemos clic sobre este elemento, se abrirá en la parte superior una **barra de búsqueda** con varias opciones relacionadas con la gestión de ramas. Las tres primeras opciones que aparecen son:

- **(＋) Create new branch** → permite **crear una nueva rama desde la rama actual**.  
- **Create new branch from…** → permite **crear una nueva rama a partir de otra rama diferente** (por ejemplo, crear una rama desde *main* aunque actualmente estés en *dev*).  
- **Checkout detached** → permite posicionarte en un commit específico sin estar en una rama (modo “detached HEAD”), útil para inspecciones, aunque no se recomienda trabajar así a largo plazo.

<br>
<p align="center">
	  <img src="assets/images/visual_studio_code/img_13.png" width="250"></img>
</p>

### Listado de ramas locales
Debajo de estas tres opciones aparece una **línea divisoria**, y enseguida se muestra el **listado de todas las ramas locales** del proyecto.  
Cada rama se muestra con información útil como:

- Nombre de la rama.
- Fecha de creación o última actualización.
- Usuario que la creó.
- Identificador del commit más reciente  .
- Descripción del último commit realizado dentro de la rama.

Este apartado permite seleccionar cualquiera de estas ramas para **cambiar a ella** y continuar trabajando dentro de ese contexto.

<br>
<p align="center">
	  <img src="assets/images/visual_studio_code/img_14.png" width="200"></img>
</p>

### Listado de ramas remotas
Más abajo, separado también por una línea, se encuentra el listado de las **ramas remotas**, es decir, las que existen en el repositorio en la nube (GitHub, GitLab, etc.). Estas ramas muestran la misma información que las locales:

- Nombre de la rama  
- Fecha de creación o actualización  
- Usuario que la creó  
- Código o hash del commit más reciente  
- Mensaje del último commit

Desde aquí también se puede seleccionar cualquier rama remota para **cambiarse a ella** y trabajar sobre esa versión del código. Ademas de que al lado derecho de dicho boton se encuentra un boton con simbolo de sincronización, el cual si se preciona esta rama sera publicada en el reposotorio remoto si es que existe una conexion al mismo.

<br>
<p align="center">
	  <img src="assets/images/visual_studio_code/img_15.png" width="200"></img>
</p>

## 🖇️ Merge y muchas otras opciones
Dentro del panel de **Source Control**, en la parte superior del campo donde se escribe el mensaje del commit, se encuentra un botón con **tres puntos (…)**. Al presionarlo, Visual Studio Code despliega un **menú completo de opciones**, el cual incluye categorías como:

- **View & Sort**  
- **Pull**  
- **Push**  
- **Clone**  
- **Checkout to…**  
- **Fetch**  
- **Commit**  
- **Changes**  
- **Pull & Push**  
- **Branch**  
- **Remote**  
- **Stash**  
- **Tags**  
- **Show Git Output**

Este menú concentra prácticamente todas las acciones importantes que pueden realizarse con Git desde la interfaz gráfica de VS Code, permitiendo gestionar el repositorio sin necesidad de usar comandos directamente.

<br>
<p align="center">
	  <img src="assets/images/visual_studio_code/img_16.png" width="200"></img>
</p>

### Realizar un merge desde Visual Studio Code
Para realizar un merge desde este menú, el procedimiento es similar al del uso de Git por consola: primero se debe **estar ubicado en la rama que recibirá los cambios**, normalmente `main` o `master`. Ya estando en esa rama:

1. Se presionan los **tres puntos (…)**.  
2. Se selecciona la opción **Branch**.  
3. Dentro de esa categoría aparece la opción **Merge**.

<br>
<p align="center">
	  <img src="assets/images/visual_studio_code/img_17.png" width="200"></img>
</p>

Al seleccionar “Merge”, Visual Studio Code abrirá la **barra de búsqueda superior**, mostrando un listado de **todas las ramas disponibles**, tanto **locales** como **remotas**, desde las cuales puede realizarse el merge hacia la rama actual.

<br>
<p align="center">
	  <img src="assets/images/visual_studio_code/img_18.png" width="200"></img>
</p>

### Más opciones disponibles
Además del merge, este menú permite realizar prácticamente cualquier acción común de Git: cambiar de rama, hacer un fetch, trabajar con stashes, manejar tags, revisar historial, entre muchas otras opciones esenciales del flujo de trabajo. Los **tres puntitos** funcionan como una **puerta de acceso a casi todas las herramientas avanzadas de Git** dentro de VS Code, lo que facilita administrar el proyecto sin necesidad de comandos manuales.

# 📊 VSC Plugin: Git Graph
Dentro de Visual Studio Code existen numerosas **extensiones externas** que no vienen incluidas por defecto, pero que han sido desarrolladas por terceros para mejorar el flujo de trabajo. Una de las más útiles y populares en proyectos que usan Git es **Git Graph**, una herramienta que permite visualizar de manera gráfica y clara la historia completa del repositorio: commits, ramas, merges, pushes y mucho más.

<br>
<p align="center">
	  <img src="assets/images/git_graph/img_1.png" width="200"></img>
</p>


## ⭐ ¿Dónde aparece Git Graph una vez instalado?
Después de instalar la extensión, podemos acceder a ella desde el apartado de **Source Control**.  
En la parte superior —donde normalmente aparecen las opciones para ver más comandos de Git y refrescar el repositorio—, ahora aparecerá un nuevo botón con un ícono que parece un conjunto de **cables o conexiones**, el cual abre directamente Git Graph.

<br>
<p align="center">
	  <img src="assets/images/git_graph/img_2.png" width="200"></img>
</p>

## 🧩 ¿Qué muestra Git Graph?
Al abrir Git Graph, se despliega una vista completa y visual del historial del repositorio. Esta vista está dividida principalmente en dos secciones:

### 🟣 **Lado izquierdo: Línea de tiempo visual**

Aquí se muestra una **representación gráfica del árbol de Git**:

- La **línea azul** representa la rama `main` (o `master`).  
- Si creamos nuevas ramas, aparecerán **líneas de diferentes colores** naciendo desde el commit donde se bifurcaron.  
- Si hiciste un merge, podrás ver claramente cómo estas ramas **se unen nuevamente** hacia la principal.
- Cada **punto** en las líneas representa un **commit**, posicionado exactamente en la rama donde ocurrió.

En conjunto, esta visualización ayuda a entender cómo ha evolucionado el proyecto con el tiempo.

### 🟡 **Lado derecho: Lista de commits**
A la derecha aparece una lista completa de todos los commits, ordenados cronológicamente.  
Cada uno muestra:

- Su **mensaje de commit**  
- El **autor**  
- La **fecha y hora**  
- La **rama** en la que se realizó  
- Y se conecta visualmente con el punto en la línea gráfica correspondiente.

Además:
- Cuando se crea una rama nueva, Git Graph coloca un **recuadro de color** junto al commit donde nació dicha rama, mostrando claramente su **nombre**.
- Cada acción queda registrada: creación de ramas, merges, push, pull, etc.

<br>
<p align="center">
	  <img src="assets/images/git_graph/img_3.png" width="500"></img>
</p>

# 🛰️ Git Remote / Origin
El tema de **Git Remote**, y en particular el concepto de **origin**, es uno de los más fundamentales al trabajar con Git.  
Este apartado se refiere a la **conexión entre nuestro repositorio local** (el que vive en nuestra computadora) y un **repositorio remoto**, el cual normalmente se encuentra alojado en plataformas como **GitHub**, **GitLab** o **Bitbucket**. Gracias a esta conexión, Git permite **subir, descargar, sincronizar y compartir** el proyecto con otros desarrolladores o simplemente almacenarlo en la nube como respaldo. Para comenzar a trabajar con repositorios remotos, lo primero que se necesita es **tener una cuenta** en la plataforma elegida, en este caso **GitHub**, que es la más popular actualmente.

## 📄 Página principal de GitHub
Una vez iniciada la sesión en GitHub, la pantalla inicial se divide en varias secciones importantes:

- **Parte derecha:** muestra un historial de nuestras actividades recientes relacionadas con Git—commits, creación de ramas, repositorios creados, forks, pull requests, etc.—siempre y cuando ya hayamos trabajado previamente con repositorios remotos.

- **Parte central:** se encuentra un *feed* donde aparecen las actividades recientes de las personas, organizaciones o proyectos que seguimos, además de noticias o recomendaciones de GitHub.

- **Parte izquierda:** aparece un listado con los repositorios en los que más hemos trabajado recientemente.  
  En este mismo bloque también se encuentra el botón **verde "New"**, que permite crear un nuevo repositorio remoto.

<br>
<p align="center">
	  <img src="assets/images/git_remote_origin/img_1.png" width="200"></img>
</p>

## ✨ Creación de un nuevo repositorio
Tras presionar el botón **New**, GitHub nos lleva a la página donde configuraremos nuestro repositorio remoto.  
La parte superior de esta página incluye un pequeño texto informativo que explica:

> *(Crear un nuevo repositorio.  
> Los repositorios contienen los archivos de un proyecto y su historial de versiones.  
> ¿Tienes un proyecto en otro lugar? Importa un repositorio.  
> Los campos requeridos están marcados con un asterisco.)*

A la izquierda podemos ver una columna vertical con dos pasos numerados.

### 🔵 **Paso 1: Información principal del repositorio**
Aquí se ingresan los datos más importantes:
- El **propietario** (tú o alguna organización).
- El **nombre del repositorio**, el cual GitHub recomienda que sea corto, descriptivo y cumpla con ciertas reglas.
- Una **descripción opcional**, donde puede añadirse información general del proyecto.

<br>
<p align="center">
	  <img src="assets/images/git_remote_origin/img_2.png" width="200"></img>
</p>

## 🔧 Paso 2: Configuraciones avanzadas
En la segunda sección se encuentran opciones adicionales que pueden mejorar o complementar la configuración del repositorio:

### 🔐 **Visibilidad**
Se puede elegir que el repositorio sea:
- **Público:** totalmente accesible para cualquier persona en Internet.
- **Privado:** únicamente accesible por el propietario y los colaboradores autorizados.

### 📄 **Agregar un README**
GitHub permite que el repositorio se cree con un archivo **README.md** inicial.  
Este archivo explica de qué trata el proyecto y aparece automáticamente en la página principal del repositorio.

### 🚫 **Agregar un .gitignore**
Aquí se puede elegir una plantilla específica de `.gitignore` según el tipo de proyecto (Node.js, Python, Android, Web, etc.).  
El `.gitignore` permite excluir archivos o carpetas que **no deben subirse al repositorio**, como módulos, cachés o archivos personales.

### 📜 **Elegir una licencia**
Opcionalmente se puede agregar una licencia al proyecto para definir los permisos de uso, distribución y modificación del código.

<br>
<p align="center">
	  <img src="assets/images/git_remote_origin/img_3.png" width="200"></img>
</p>

## 📂 Repositorio creado
Una vez finalizado el formulario y creado el repositorio, GitHub nos redirige a la página principal del nuevo repositorio remoto. Aquí encontraremos:

- Opciones para **agregar colaboradores** al proyecto.  
- Posibilidad de añadir un **README**, un **.gitignore** o archivos iniciales si no se añadieron durante la creación.
- Y lo más importante:  
  **instrucciones claras y específicas para conectar nuestro repositorio local con este repositorio remoto.**

Estas instrucciones incluyen:
- El comando para agregar el origen remoto:  
  `git remote add origin <url>`
- El comando para el primer push:  
  `git push -u origin main`
- Alternativas si ya existe un repositorio local con historial previo.

<br>
<p align="center">
	  <img src="assets/images/git_remote_origin/img_4.png" width="200"></img>
</p>

## 🌐 Git Remote
El comando `git remote` permite **vincular** (o gestionar) repositorios remotos asociados al repositorio local. Para conectar un repositorio local con su remoto (por ejemplo en GitHub) se usa la forma: `git remote add origin <url-del-repositorio>`. Donde a continuación se explica qué significa de cada parte de dicho comando:

- **`git remote`**: Indica que se va a trabajar con **remotos** (orígenes externos). Es el subcomando que agrupa acciones relacionadas con repositorios remotos (listar, añadir, renombrar, eliminar, etc.).

- **`add`**:  Es la acción que **añade** un nuevo remoto a la configuración del repositorio local. Con `add` se está registrando una nueva referencia hacia un repositorio en la nube.

- **`origin`**: Es el **nombre (alias)** que se le asigna al remoto. Por convención, `origin` es el nombre por defecto que se usa para referirse al repositorio remotos principal, pero se puede usar cualquier nombre (por ejemplo `upstream`, `github`, `prod`, etc.). `origin` solo es un identificador corto —internamente apunta a una URL—.

- **`<url-del-repositorio>`**:  
  Es la **URL** que proporciona la plataforma remota (HTTPS o SSH) que apunta al repositorio en GitHub/GitLab/Bitbucket. Ejemplos:  
  - HTTPS: `https://github.com/usuario/nombre-repo.git`  
  - SSH: `git@github.com:usuario/nombre-repo.git`


### ¿Para qué sirve `git remote`? (explicado punto por punto)
- **Vincular tu repo local con uno remoto:** Al añadir un remoto (`git remote add origin <url>`) se guarda en la configuración del proyecto la **dirección** a la que se le podrá enviar (`push`) o desde la que se podrá traer (`fetch`/`pull`) código. Es como guardar la dirección de un servidor: **sin esa dirección, Git no sabe a dónde enviar ni de dónde traer cambios**.

- **Consultar qué remotos tienes conectados:** Con `git remote -v` se muestran los remotos registrados y sus URLs. Esto sirve para **verificar** a qué repositorios apunta el proyecto (por ejemplo `origin` → GitHub, `upstream` → repo original de donde se hizo fork). Es útil para saber exactamente dónde se harán `push` o `fetch`.

- **Cambiar la URL del remoto:** Si la URL del remoto cambia (por ejemplo migras de HTTPS a SSH, o el repositorio se mueve), se puede **actualizar** sin perder el resto de la configuración. Se puede usar `git remote set-url origin <nueva-url>` o renombrarlo/volver a añadirlo. Esto mantiene las referencias intactas sin tener que reconfigurar todo.

- **Eliminar un remoto:** Si ya no se necesita un remoto (por ejemplo un repo obsoleto o mal configurado), se puede quitar con `git remote remove <nombre>`. Esto borra esa entrada de la configuración local; **no borra el repositorio remoto** en la plataforma, solo elimina la referencia local.

- **Gestionar múltiples remotos si tu proyecto lo necesita:** Un proyecto puede tener varios remotos (por ejemplo `origin` para tu fork y `upstream` para el repo original). `git remote` facilita:  
  - **añadir** varios remotos,  
  - **nombrarlos** para diferenciarlos (`origin`, `upstream`, `staging`, `prod`),  
  - y realizar operaciones dirigidas a uno u otro (`git push origin main`, `git fetch upstream`).  
  Esto es clave en flujos como forks, despliegues o integración entre varios servidores.

## 🌍 Proyecto en remoto
Una vez que se vinculó el proyecto local con el repositorio remoto (`git remote add origin <url>`) y se realizó el **primer push**, GitHub mostrará el repositorio con todos los archivos del proyecto. La vista principal del repositorio se verá algo así:

<br>
<p align="center">
  <img src="assets/images/git_remote_origin/img_5.png" width="300"></img>
</p>

En esta interfaz se encuentran varias herramientas e información clave para **visualizar, administrar y compartir** el proyecto.


### 🏷️ Nombre del repositorio & visibilidad
En la **parte superior izquierda** aparece el **nombre del repositorio** y un indicador de **visibilidad**:

- **🔓 Público** → cualquiera puede ver el repositorio.  
- **🔒 Privado** → solo el propietario y los colaboradores autorizados pueden acceder.

<br>
<p align="center">
  <img src="assets/images/git_remote_origin/img_6.png" width="300"></img>
</p>

### ⭐ Controles principales: Pin, Views, Fork y Star
En la **parte superior derecha** están los controles rápidos:

- **📌 Pin** → fijar el repositorio en el perfil para destacarlo.  
- **👀 Views** → número de vistas del repositorio.  
- **🍴 Fork** → crear una copia del repositorio (útil para organización/forks).  
- **⭐ Star** → marcar como favorito.

Estos botones ayudan a gestionar la visibilidad y la interacción con la comunidad.

<br>
<p align="center">
  <img src="assets/images/git_remote_origin/img_7.png" width="300"></img>
</p>


### 🌿 Ramas y Tags (esquina izquierda)
A la izquierda se muestra la **rama activa** y controles relativos a ramas y tags:

- **Rama actual** → indica qué rama se está visualizando.  
- **Contador de ramas** → al pulsarlo despliega la lista completa de ramas.  
- **Tags** → acceso a versiones marcadas del proyecto.

Esto facilita navegar entre versiones o revisar ramas específicas.

<br>
<p align="center">
  <img src="assets/images/git_remote_origin/img_8.png" width="300"></img>
</p>


### 🔎 Herramientas del encabezado: Buscar, Crear archivo y Clonar
En la parte superior derecha del contenido aparecen controles rápidos para trabajar con los archivos:

- **🔎 Buscador** → buscar archivos dentro del repositorio.  
- **➕ Add file** → crear o subir archivos directamente desde GitHub.  
- **💻 Code (botón verde)** → copiar la **URL del repositorio** (HTTPS o SSH) para clonar o declarar como remoto; también ofrece descarga ZIP.

Esto es útil para obtener la URL que se usa en `git clone` o `git remote add`.

<br>
<p align="center">
  <img src="assets/images/git_remote_origin/img_9.png" width="300"></img>
</p>

### 📊 Panel lateral derecho: stats y descripción
En la columna derecha GitHub muestra información resumida del proyecto:

- **Descripción** del repositorio.  
- **Actividad reciente** (commits, PRs, issues).  
- **⭐ Estrellas**, **🍴 Forks**, **👀 Views**.  
- **Releases** y **Packages** vinculados.

Estos datos permiten evaluar rápidamente la salud y popularidad del proyecto.

<br>
<p align="center">
  <img src="assets/images/git_remote_origin/img_10.png" width="300"></img>
</p>

### 📁 Explorador de archivos y cabecera del contenido
En el panel central se visualiza la **estructura del proyecto** (carpetas y archivos). En la cabecera del recuadro se muestra información clave sobre el último commit:

- **Autor del último commit (HEAD)**  
- **Mensaje del último commit**  
- **SHA corto del commit**  
- **Última fecha de actualización**  
- **Número total de commits**

Al hacer clic en estos elementos se puede navegar al historial completo y ver los detalles/versiones anteriores de cada archivo.

<br>
<p align="center">
  <img src="assets/images/git_remote_origin/img_11.png" width="300"></img>
</p>

### 📘 README renderizado
En la parte inferior de la página GitHub renderiza el **`README.md`** del repositorio, mostrando su contenido con formato (Markdown).  
Este archivo suele contener:

- Descripción del proyecto ✅  
- Instrucciones de instalación y uso 🛠️  
- Capturas, ejemplos y documentación 📷📚  
- Licencia y notas legales 📜

El README es la **tarjeta de presentación** del proyecto en GitHub.

<br>
<p align="center">
  <img src="assets/images/git_remote_origin/img_12.png" width="300"></img>
</p>

> 💡 **Tip:** mantener el `README.md` actualizado y bien estructurado ayuda mucho a que otros entiendan y colaboren en el proyecto rápidamente.

# ⬇️ Git Push & Pull
## 🚀 Git Push
Imaginemos que se trabaja en un proyecto con otras personas y cada quien tiene una **copia local** del código. Cada vez que se hacen cambios en la máquina local, esos cambios **no se comparten automáticamente** con el equipo. Para que todos vean y usen los cambios hechos localmente, es necesario **subirlos al repositorio remoto**: eso es justo lo que hace **`git push`**.

**`git push`** toma los commits que están en la rama local y los **envía** al repositorio remoto (por ejemplo GitHub). Es como presionar un botón para **compartir** lo que ya fue guardado (commiteado) localmente con el resto del equipo.

> 💡 **Tip:** `git push` **no** crea commits ni modifica el historial local: solo **envía** lo que ya existe en la máquina local al remoto.

### ✅ Requisitos antes de hacer push
- El proyecto ya debe estar **inicializado** con `git init`.  
- Debe existir **al menos un commit** local (sin commits no hay nada que subir).  
- El repositorio local debe estar **vinculado** a un remoto (`git remote add origin <url>`).  
- Estar en la **rama** que se desea subir (por ejemplo `main` o `master`).

### ¿Cómo funciona en la práctica?
Normalmente, para el primer push hacia el remoto se usa: `git origin main`

- **`origin`** es el **alias** del remoto (nombre corto que apunta a la URL del repositorio remoto).  
- **`main`** (o `master`) es el nombre de la rama local que se está subiendo.

Un uso común para establecer la rama local para que *rastreé* la remota es: `git push -u origin main`

El parámetro `-u` (upstream) configura que la rama `main` local **rastreará** `origin/main`, de modo que en adelante solo será necesario `git push` o `git pull` sin especificar `origin main`. Pero por defecto el uso de solamente `git push origin main` ya rastrea al repositorio remoto.

> ⚠️ **OJO:** Puede haber ocasiones en las que se genere un **pequeño error** al intentar subir nuestra rama `main` por primera vez.  
> Esto sucede mucho cuando el repositorio fue creado recientemente y **la rama local tiene otro nombre** (por ejemplo `master` o `main` en distinto casing). El error que suele aparecer es el siguiente:

> ```bash
>chris@LAPTOP-0DNMOIV6 MINGW64 /d/Trabajos/Cursos/proyecto-ejemplo (master)
>$ git push -u origin main
>error: src refspec main does not match any
>error: failed to push some refs to 'https://github.com/ChrisAlegriaR/testGitPushPull.git'
> ```
> 
> Este error significa que **Git no encontró ninguna rama llamada `main` en tu repositorio local**, por lo que **no puede subir algo que no existe**. Esto ocurre porque, dependiendo de la versión de Git, la configuración del sistema o la plantilla del proyecto, Git puede crear la rama inicial con nombres como:

>- `master`  
>- `Main` (diferente por mayúscula)  
>- `main`  
>- o incluso otra rama si se creó manualmente

>Como queremos trabajar con la convención moderna (usar **`main`** como rama principal), lo que debemos hacer es **renombrar la rama actual** a `main` usando: `git branch -M main`.

>### 🧠 ¿Qué significa `-M`?
>La bandera **`-M`** significa **"move/rename forcé"** (mover/renombrar de forma forzada).  
Esto quiere decir que:

>- Si la rama ya existiera con ese nombre, **forzará el cambio**.  
>- Si la rama anterior tenía otro nombre (`master`, `dev`, etc.), se convertirá en **`main` inmediatamente**.  
>- No importa cuál era el nombre original: lo reemplaza sin pedir confirmación.

# 🔄 Git Pull
Imaginemos que estamos trabajando en un proyecto con otras personas, y todos usan una **carpeta compartida en línea** para guardar el código del proyecto (el repositorio remoto).  Cada vez que alguien más hace cambios y los sube a esa carpeta, **tu copia local NO se actualiza automáticamente**. Para obtener esos cambios más recientes y sincronizarlos con tu computadora, usamos: `git pull`.  Este comando le dice a Git: *“Ve al repositorio remoto, busca los últimos cambios que otros subieron y tráelos a mi copia local.”*

> 💡 **`git pull` = traer a tu computadora los cambios más recientes del repositorio remoto. Te mantiene actualizado con el equipo y con la última versión del proyecto.**

## 🧩 Requisitos para usar `git pull`
Para que Git pueda descargar los cambios, deben cumplirse estas condiciones:

1. 🔗 El proyecto local **debe estar vinculado** con el remoto (con `git remote add origin <url>`).  
2. 📌 Debe existir **contenido en el repositorio remoto**.  
3. 🔄 Debe haber **cambios en remoto que no se tengan en local**.  

Cuando esto ocurre, `git pull` descargará lo que falta desde la nube y lo integrará en el proyecto local.

> 🎯 **Git Pull es lo contrario de Git Push:**  
> - `git push` → envía cambios **de local → remoto**  
> - `git pull` → trae cambios **de remoto → local**

La cual una vez realizado y ejecutado dicho comando la consola nos arrojara el siguiente mensaje:

```bash
chris@LAPTOP-0DNMOIV6 MINGW64 /d/Trabajos/Cursos/proyecto-ejemplo (main)
$ git pull origin main
From https://github.com/ChrisAlegriaR/testGitPushPull
 * branch            main       -> FETCH_HEAD
Updating dc14e18..ad3a29d
Fast-forward
 texto2.txt | 1 +
 1 file changed, 1 insertion(+)
 create mode 100644 texto2.txt
```

## 📝 Explicación detallada línea por línea del resultado
Ahora bien al ejecutar dicho comando nos arrojara un par de lineas de codigo las cuales se explicancion es:

### `From https://github.com/ChrisAlegriaR/testGitPushPull`
Indica la **URL del remoto** del cual Git descargó (fetched) la información.  
Es la fuente de donde vinieron los objetos/commits que se trajeron al repositorio local.

### `* branch            main       -> FETCH_HEAD`
Significa que se **obtuvo la rama remota `main`** y se guardó temporalmente en una referencia llamada **`FETCH_HEAD`**.  
- `* branch main` → rama remota consultada.  
- `-> FETCH_HEAD` → Git coloca la punta de esa rama en `FETCH_HEAD` para uso inmediato (por ejemplo para un `merge` o `fast-forward`).  
`FETCH_HEAD` es una referencia temporal que contiene el commit más reciente traído por el `fetch` dentro del flujo de `pull`.

### `Updating dc14e18..ad3a29d`
Muestra que la rama local **se actualizará** desde el commit con hash **`dc14e18`** hasta el commit **`ad3a29d`**.  
En otras palabras: *antes del pull* el HEAD estaba en `dc14e18`; *después del pull* estará en `ad3a29d`.  
Esto permite ver qué rango de commits se aplicaron a la rama local.

### `Fast-forward`
Indica que Git realizó un **merge tipo fast-forward**: la rama local avanzó directamente hasta el nuevo commit remoto sin necesidad de crear un commit de fusión ni resolver conflictos.  
Condiciones del fast-forward:
- La rama local no tenía commits divergentes respecto al remoto; solo quedó “al día” moviendo el puntero.
- Es la fusión más sencilla: no combina cambios conflictivos, simplemente avanza la referencia.

### `texto2.txt | 1 +`
Explica qué cambios afectaron a archivos individuales durante la actualización:
- **`texto2.txt`** → archivo afectado.  
- **`| 1`** → número total de líneas involucradas en el diff para ese archivo (en este caso 1 línea diferente).  
- **`+`** → indica que la línea fue **agregada** (inserción). Si hubiera `-` o combinaciones como `+--` mostraría inserciones y eliminaciones.

### `1 file changed, 1 insertion(+)`
Resumen global de los cambios aplicados en la fusión / fast-forward:
- **`1 file changed`** → se modificó (o añadió) 1 archivo en total.  
- **`1 insertion(+)`** → hubo 1 línea **insertada** entre todos los archivos afectados.  
(Nota: las eliminaciones se mostrarían como `X deletion(-)` si las hubo).

### `create mode 100644 texto2.txt`
Indica que **se creó un nuevo archivo** en el repositorio como parte de la actualización: `texto2.txt`.  
- **`create mode`** → acción: creación de archivo.  
- **`100644`** → permisos del archivo (metadata POSIX típica para archivos de texto: lectura/escritura para propietario y solo lectura para grupo/otros).  
En resumen: la rama remota traía un archivo nuevo y, al hacer pull, Git lo añadió con esos permisos.

## ✅ Resumen rápido
- La salida empieza mostrando **de dónde** vino la información (URL).  
- Luego indica **qué rama remota** se descargó y se puso en `FETCH_HEAD`.  
- `Updating old..new` muestra el **rango de commits** aplicado.  
- `Fast-forward` significa que la rama local avanzó sin conflictos.  
- Las siguientes líneas detallan **qué archivos** cambiaron, cuántas líneas se insertaron/eliminaron y si se crearon o eliminaron archivos, incluyendo permisos.

> ⚠️ **OJO:** Puede haber ocasiones en las que se genere un **pequeño error** al intentar descargar nuestra rama `main` por primera vez.  
> Esto sucede mucho cuando el repositorio fue creado recientemente y **la rama local no sabe de que rama remota descargar el contenido** (por ejemplo `master` o `main` en distinto casing). El error que suele aparecer es el siguiente:
>
>```bash
>chris@LAPTOP-0DNMOIV6 MINGW64 /d/Trabajos/Cursos/proyecto-ejemplo (main)
>$ git pull
>remote: Enumerating objects: 4, done.
>remote: Counting objects: 100% (4/4), done.
>remote: Compressing objects: 100% (2/2), done.
>remote: Total 3 (delta 0), reused 0 (delta 0), pack-reused 0 (from 0)
>Unpacking objects: 100% (3/3), 943 bytes | 6.00 KiB/s, done.
>From https://github.com/ChrisAlegriaR/testGitPushPull
>   dc14e18..ad3a29d  main       -> origin/main
>There is no tracking information for the current branch.
>Please specify which branch you want to merge with.
>See git-pull(1) for details.
>
>    git pull <remote> <branch>
>
>If you wish to set tracking information for this branch you can do so with:
>
>    git branch --set-upstream-to=origin/<branch> main
>```
>
>## ❓ ¿Qué significa este error?
>Este error aparece porque **la rama local (por ejemplo `main`) no sabe a qué rama remota debe conectarse** para descargar los cambios. En Git, esto se llama **upstream tracking** (rama de seguimiento). Es decir que la rama local no tiene configurado un “camino” hacia la rama remota correspondiente. Entonces no sabe de dónde bajar los cambios.
>
>Por ejemplo:  
>- La rama local: `main`  
>- La rama remota: `origin/main`  
>
>Si no se configuró el vínculo entre ambas, Git no puede hacer `pull` automáticamente. Por lo que para solucionar este error, simplemente hay que establecer el **tracking**(vínculo) entre la rama local y la rama remota usando `git branch --set-upstream-to=origin/main main`. Esto le dice a Git que a partir de ahora, la rama local `main` debe seguir a la rama remota `origin/main`. Otra forma de solucionarlo es ejecutar: `git push -u origin main`. 
>
>### ¿Qué significa?
>
>- **`origin`** → nombre del remoto (nombre que se le da a la url del proyecto)  
>- **`main`** → nombre de la rama remota  
>- **`-u` (o `--set-upstream`)** → establece el tracking automáticamente  
>
>Es decir, este comando descarga los cambios desde `origin/main` y además configura tu rama local para que a partir de ahora siga esa rama remota.

# 🔛 Git Tag & Switch
## 🏷️ Git Tag
El uso de `git tag` permite etiquetar commits como **commits importantes**, y esta funcionalidad es ampliamente utilizada para marcar versiones **estables**, **listas para producción** o **hitos relevantes** dentro del proyecto. Un **tag** actúa como un marcador que identifica un commit como una versión significativa dentro del desarrollo. Un tag puede utilizarse para indicar versiones como:
- `v1.0.0`
- `v2.3.1`
- `release-2025`
- `hotfix-01`

De esta forma se facilita que otros desarrolladores sepan cuál es la versión estable o cuál commit corresponde a una entrega específica.

### 🧩 ¿Qué representa realmente un tag?
Cuando se asigna un tag, Git no altera el proyecto ni genera nuevos commits. Únicamente se registra un **nombre o etiqueta** que apunta a un commit ya existente. Esto resulta útil para:

- Identificar versiones estables del proyecto.
- Regresar fácilmente a un punto del historial.
- Descargar versiones específicas desde plataformas como GitHub.
- Marcar hitos del desarrollo.

### 💻 Uso básico en código
Para aplicar un tag sobre el **último commit de la rama actual**, se utiliza: ´git tag nombreEtiqueta´. El cual al ejecutar este comando, Git no muestra un mensaje explícito de confirmación, pero la etiqueta queda registrada en el historial. Para visualizarla se usa: ´git log´. Este comando mostrará algo similar a:

```bash
chris@LAPTOP-0DNMOIV6 MINGW64 /d/Trabajos/Cursos/git-github-course (main)
$ git log --oneline
daedf6a (HEAD -> main, tag: status, tag: etiquetaPrueba, origin/main) Finished: Git Push & Git Pull Section
4e9c442 Add: Git Push And Git Pull Section
06aa25e Enhance README with synchronization button details
66ac03b Fix: Spelling And Improve Git Remote Documentation
94a3524 Merge branch 'main' of https://github.com/ChrisAlegria/Git-GitHub-Course
28ce1ed Update: Assets Filesa For Git Explication
cbddd34 Add: Section for Gi Remote in README
e1d8e51 Update README.md
fe2cf97 Fix: Names In Assets
40db8ba Merge branch 'main' of https://github.com/ChrisAlegria/Git-GitHub-Course
```

### 🕒 Visualización de tags en commits anteriores
Si después de crear un tag se continúan realizando otros commits, el comando `git log` mostrará en qué commit se aplicó la etiqueta, indicando visualmente que ese punto del historial fue marcado.

```bash
chris@LAPTOP-0DNMOIV6 MINGW64 /d/Trabajos/Cursos/git-github-course (main)
$ git log --oneline
e1321e6 (HEAD -> main) Add: Git Descriptions
1a4fd7f Update: Spaces In Line
daedf6a (tag: status, tag: etiquetaPrueba, origin/main) Finished: Git Push & Git Pull Section
4e9c442 Add: Git Push And Git Pull Section
06aa25e Enhance README with synchronization button details
66ac03b Fix: Spelling And Improve Git Remote Documentation
94a3524 Merge branch 'main' of https://github.com/ChrisAlegria/Git-GitHub-Course
28ce1ed Update: Assets Filesa For Git Explication
cbddd34 Add: Section for Gi Remote in README
e1d8e51 Update README.md
```

> ⚠️ **OJO:** Cuando se quiere regresar a un commit específico normalmente se utiliza `git checkout` seguido del **hash** del commit. Sin embargo, cuando ese commit tiene un **tag asignado**, no es necesario escribir el hash completo. Git permite usar el **nombre del tag** directamente en lugar del hash, lo cual facilita mucho el proceso y evita errores al copiar o identificar hashes largos. Esto significa que, si un commit tiene un tag llamado `v1.0.0`, se puede volver a ese punto del historial simplemente usando: `git checkout v1.0.0`. Esta práctica es especialmente útil cuando se manejan versiones del proyecto, ya que los tags funcionan como puntos de referencia más claros y fáciles de recordar que un hash alfanumérico extenso.

## 🔀 Git Switch
El comando **`git switch`** se utiliza para **cambiar entre ramas locales** dentro de un repositorio Git. Su propósito es ofrecer una alternativa más clara, sencilla y segura a `git checkout`, ya que este último combina demasiadas funciones en un solo comando (cambiar de rama, crear ramas y hasta cambiar archivos), lo que puede generar confusión, especialmente para quienes están iniciando en Git. A diferencia de `git checkout`, cuando se usa `git switch` **Git no busca ramas en el repositorio remoto**, ni intenta crearlas automáticamente. Esto significa que **solo permite cambiar a ramas que existen en el entorno local**, lo que evita cambios inesperados o descargas no intencionadas desde el servidor remoto. Cuando se usa `git checkout`, si la rama no existe localmente, Git intenta encontrarla en el remoto y descargarla. Esto puede ser útil en algunos casos, pero también puede provocar comportamientos no deseados si no se sabe exactamente qué ramas existen localmente y cuáles no.  

Con `git switch`, ese riesgo desaparece, ya que el comando **únicamente valida las ramas locales** y no toma decisiones adicionales por su cuenta. Para usar el comando, simplemente se escribe: `git switch nombreDeLaRama`. Si la rama existe en el entorno local, Git realizará el cambio inmediatamente. La consola mostrará un mensaje indicando que la operación se ejecutó correctamente, confirmando que ahora se está trabajando en la nueva rama seleccionada. Este enfoque hace que **`git switch` sea ideal cuando ya se tiene la rama en local y únicamente se desea mover entre ellas**, manteniendo un flujo de trabajo claro, sin interferencias con ramas remotas ni riesgo de crear ramas nuevas por accidente.

> 💡 *`git switch` se introdujo para brindar mayor claridad y buenas prácticas al trabajar con ramas. Permite cambiar de manera segura entre las ramas locales del proyecto y evita acciones implícitas que `git checkout` podría ejecutar sin que el usuario lo note.*

```bash
chris@LAPTOP-0DNMOIV6 MINGW64 /d/Trabajos/Cursos/git-github-course (main)
$ git switch ramaDePruebas
Switched to branch 'ramaDePruebas'
```
# 📱 Git Stash & Stash Apply
En ocasiones podemos estar trabajando en una funcionalidad o modificación dentro de nuestro proyecto, pero necesitamos **guardar esos cambios temporalmente sin hacer un commit**. Tal vez queremos cambiar de rama, actualizar nuestro repositorio, hacer un pull, o simplemente pausar nuestro trabajo sin registrarlo aún.  
Para este tipo de situaciones existe **`git stash`**, una herramienta que nos permite **guardar todos los cambios actuales en un “almacenamiento temporal”** sin incluirlos en el historial del repositorio. Cuando ejecutamos `git stash`, Git toma **todos los archivos modificados, agregados o eliminados**, y los guarda en un **stash**, que funciona como un commit temporal **solo local**, es decir, **nadie del equipo podrá ver esos cambios**, incluso si hacemos un `git push` o un `git pull`. Cada stash se guarda con un identificador automático similar a: `stash@{0}`, `stash@{1}`, `stash@{2}` y así sucesivamente.

Una vez que Git guarda el stash, **nuestro directorio de trabajo vuelve exactamente al estado del último commit**, dejando el proyecto limpio y listo para otras tareas. Podemos verificar todos los stashes almacenados mediante: `git stash list`. Este comando mostrará una lista completa de los “commits temporales” que Git mantiene en memoria local, ordenados desde el más reciente al más antiguo.

```bash
chris@LAPTOP-0DNMOIV6 MINGW64 /d/Trabajos/Cursos/git-github-course (ramaDePruebas)
$ git stash list
stash@{0}: WIP on ramaDePruebas: d58dc3a Add: Git Practices In Branch RamaDePruebas
stash@{1}: WIP on ramaDePruebas: d58dc3a Add: Git Practices In Branch RamaDePruebas
```

## 🔄 Restaurar un Stash
Cada stash es independiente y se puede restaurar en cualquier momento usando: `git stash apply nombreDelStash`. Esto tomará el stash especificado (por ejemplo `stash@{0}`) y **volverá a aplicar sus cambios sobre el código actual**, mostrando incluso las diferencias con el último commit, como si usáramos también un `git status`. Es importante tener en cuenta que si realizamos nuevos cambios después de haber creado o regresado a un stash, **esos cambios NO se guardarán en el stash anterior**. Cada "snapshot" debe crearse manualmente con un nuevo `git stash` si queremos guardar las modificaciones adicionales.

```bash
chris@LAPTOP-0DNMOIV6 MINGW64 /d/Trabajos/Cursos/git-github-course (ramaDePruebas)
$ git stash apply stash@{0}
On branch ramaDePruebas
Changes not staged for commit:
  (use "git add <file>..." to update what will be committed)
  (use "git restore <file>..." to discard changes in working directory)
        modified:   Course/texto.txt

Untracked files:
  (use "git add <file>..." to include in what will be committed)
        test.txt

no changes added to commit (use "git add" and/or "git commit -a")
```

## 🔄 Volver al último commit sin aplicar un Stash
Si queremos **descartar los cambios actuales y regresar al estado del último commit**, sin restaurar un stash, podemos usar: `git restore .` Este comando elimina los cambios del área de trabajo y restaura los archivos como estaban en el commit más reciente.

```bash
chris@LAPTOP-0DNMOIV6 MINGW64 /d/Trabajos/Cursos/git-github-course (ramaDePruebas)
$ git restore .
```

## 🗑️ Eliminar Stashes
Si deseamos borrar los stashes almacenados, existen dos opciones:

- **Eliminar un stash específico:**  
  `git stash drop nombreDelStash`. Esto borra únicamente el stash seleccionado.

- **Eliminar todos los stashes:**  
  `git stash clear`. Esta opción elimina **todos** los guardados temporales.

En ambos casos, Git mostrará mensajes en la consola indicando que los cambios fueron eliminados correctamente y la lista de stashes actualizada.

```bash
chris@LAPTOP-0DNMOIV6 MINGW64 /d/Trabajos/Cursos/git-github-course (ramaDePruebas)
$ git stash drop stash@{0}
Dropped stash@{0} (de3cdf774229e461c015ec3083a7c3451031dc1c)

chris@LAPTOP-0DNMOIV6 MINGW64 /d/Trabajos/Cursos/git-github-course (ramaDePruebas)
$ git stash drop stash@{0}
Dropped stash@{0} (de3cdf774229e461c015ec3083a7c3451031dc1c)
```

> 💡 *`git stash` es una herramienta ideal para pausar tu trabajo sin comprometer cambios en el historial, mantener tu entorno limpio y volver a tus avances en cualquier momento, de manera segura y totalmente local.*

# ⛔ Eliminación de Ramas
La eliminación de ramas es una acción comúnmente realizada por el responsable del repositorio remoto o el líder de equipo, aunque **si trabajas solo también puedes eliminar ramas** en tu repositorio de GitHub. Antes de eliminar una rama es importante recordar que **siempre debe existir otra rama activa distinta a la que vas a borrar** (por ejemplo `main` o `develop`), porque Git no permite eliminar la rama en la que estás posicionado. Podemos eliminar ramas **localmente** o **en el remoto**. A continuación se explica cada caso con su comportamiento y recomendaciones.


## 🧭 Eliminar una rama local
Para eliminar una rama en tu repositorio local se usa: `git branch -d nombreRama`

- `-d` significa **delete** y Git intentará borrar la rama _solo si_ sus cambios ya fueron fusionados (merged) en la rama actual o en otra rama de destino.  
- Si la rama contiene cambios no fusionados, Git te impedirá borrarla con `-d` para evitar pérdida accidental de trabajo.  
- Si estás seguro y quieres forzar la eliminación (eliminando los cambios no fusionados), puedes usar `git branch -D nombreRama` (mayúscula `-D`). **Ten cuidado**: esto puede hacer que pierdas commits que no estén en ninguna otra rama.

**Requisito:** debes estar en otra rama distinta a la que borrar (por ejemplo, `git switch main` o `git switch develop`) antes de ejecutar el comando.

Al ejecutarlo correctamente, la consola mostrará un mensaje confirmando que la rama fue eliminada localmente.

```bash
chris@LAPTOP-0DNMOIV6 MINGW64 /d/Trabajos/Cursos/git-github-course (main)
$ git branch -d ramaDesarrollo
Deleted branch ramaDesarrollo (was d58dc3a).
```

## 🌐 Eliminar una rama remota
Para eliminar una rama en el repositorio remoto (por ejemplo en GitHub) se usa: `git push origin --delete nombreRama`. Este comando envía una instrucción al remoto similar a cuando haces `git push origin nombreRama` (que sube una rama). La diferencia es que aquí se está pidiendo expresamente **eliminar** la rama en el servidor mediante la opción `--delete`. Al ejecutarlo, el remoto devolverá un mensaje confirmando que la rama fue borrada de forma remota.

**Notas importantes:**
- Necesitas permisos de escritura en el repositorio remoto para poder eliminar ramas allí.  
- Borrar una rama remota afectará a todo el equipo: otros colaboradores ya no podrán recuperar esa rama desde el servidor (salvo si alguien la tiene todavía en local y la vuelve a subir).  
- Si borraste una rama por error, se puede recuperar si alguien tiene esa rama localmente y la vuelve a `git push origin nombreRama`.

```bash
chris@LAPTOP-0DNMOIV6 MINGW64 /d/Trabajos/Cursos/git-github-course (ramaDesarrollo)
$ git push origin --delete ramaDesarrollo
remote: This repository moved. Please use the new location:
remote:   https://github.com/ChrisAlegriaR/Git-GitHub-Course.git
To https://github.com/ChrisAlegria/Git-GitHub-Course.git
 - [deleted]         ramaDesarrollo
```

## ✅ Buenas prácticas y recomendaciones
- Antes de borrar, verifica el estado con `git branch` (locales) y `git branch -r` (remotas) o `git fetch && git branch -r` para listar ramas remotas actualizadas.  
- Asegúrate de que los cambios importantes estén fusionados o respaldados.  
- Prefiere `-d` sobre `-D` para evitar pérdida accidental de trabajo.  
- Comunica al equipo antes de eliminar ramas compartidas (especialmente ramas de trabajo o feature branches).


> ⚠️ **OJO:** No intentes eliminar la rama en la que estás trabajando; primero cámbiate a otra rama. Además, eliminar una rama remota requiere permisos en el servidor y puede afectar a tus compañeros: confirma que la rama ya no es necesaria o que su trabajo está fusionado antes de borrarla. Si por error borras una rama remota, aún puedes recuperarla si alguien del equipo la tiene en local y la vuelve a `git push origin nombreRama`.

> 💡 *Eliminar ramas remotas es una buena práctica para mantener el repositorio organizado, evitar confusiones y garantizar que únicamente existan las ramas activas o relevantes para el proyecto.*  
