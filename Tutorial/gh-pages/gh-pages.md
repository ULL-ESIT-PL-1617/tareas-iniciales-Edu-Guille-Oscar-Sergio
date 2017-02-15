# LAS GITHUB PAGES

Las GitHub Pages, conocidas también como las gh-pages, son una herramienta que la plataforma GitHub ofrece a los desarrolladores. Se trata de un servicio estático de hosting para páginas webs, diseñado para alojar páginas personales, de organizaciones o de proyectos directamente en un repositorio de GitHub. Es ideal para sitios informativos con un funcionamiento básico, pero no para sitios web más complejos puesto que no soporta la ejecución de código en el lado del servidor; lenguajes como PHP, Ruby o Python son inservibles.

Los sitios alojados en GitHub Pages se asocian con el dominio _.github.io_ y utilizan el protocolo HTTPS.

---

### PARA USUARIOS Y ORGANIZACIONES

Las páginas orientadas a la representación de usuarios y organizaciones se alojan en un repositorio específico dedicado a sus archivos. Estos repositorios deberán llamarse con el nombre de usuario \(o de la organización\) de la siguiente manera:

```
username.github.io --- organizationame.github.io
```

Los pasos para la creación de la página, utilizando la terminal, serían los siguientes:

1. Crear el repositorio. Su nombre deberá corresponderse con el ya mencionado.
2. Clonamos el repositorio en la máquina donde vayamos a trabajar.
3. Situamos el código HTML5 de nuestra página en el repositorio local.
4. Confirmamos los cambios y hacemos _push_ al repositorio remoto, en la rama master. 

Seguidos estos cuatro pasos, el sitio web debería estar disponible después de algunos segundos. Simplemente abrimos un navegador e introducimos la dirección de la página, que se corresponde con el nombre que le dimos al repositorio. Es importante saber que el contenido debe estar en la rama master: en las páginas para usuarios y organizaciones el código fuente HTML5 no puede situarse en ninguna otra localización.

---

### PARA PROYECTOS

A diferencia de los sitios web para usuarios y organizaciones, los sitios orientados a los proyectos alojan su código fuente en el mismo repositorio que el del proyecto. Se puede configurar GitHub Pages para que publique el sitio web en base a los ficheros fuente HTML5 situados en la rama _master_, _gh-pages_, o de un directorio _/docs_ en la rama master. Para hacer esto, seguimos los siguientes pasos:

1. Vamos a los ajustes de nuestro repositorio.
2. En la pestaña de opciones, hacemos _scroll_ hacia abajo hasta la sección _GitHub Pages_. 
3. En el menú desplegable _Source_, seleccionamos una de las tres opciones: tomar la rama _master_, la rama _gh-pages_, o el directorio _/doc_. 

Es importante tener en cuenta que, para que cada una de esas opciones esté disponible, habrá que tener una rama _master_ o _gh-pages_ creada, o un directorio _/doc_ bajo la rama master. Una vez hecho esto, el sitio web pasará a estar disponible bajo la dirección:

```
https://username.github.io/projectname --- https://organizationame.github.io/projectname
```

---

### GITHUB PAGES Y JEKYLL

Además de soportar código tradicional HTML5, GitHub Pages está profundamente integrado con Jekyll, un generador de sitios web muy popular diseñado para la creación de blogs y documentación de software, aunque se puede utilizar con muchos más fines.

La integración entre estos dos servicios nos permite seleccionar una plantilla de Jekyll para darle estilo a el sitio web de nuestro usuario, organización o proyecto. Simplemente vamos a los ajustes del repositorio, y en la pestaña Options, bajamos hasta la sección GitHub Pages. Seleccionamos _Change Theme_ y elegimos el que más nos guste.

---

### EL MÓDULO GH-PAGES

El módulo gh-pages es un módulo de npm \(Node Package Manager\) que permite automatizar la publicación de archivos en una rama gh-pages de un repositorio de GitHub \(o cualquier otra rama u otro servicio\). Para entender su forma de instalarlo y su funcionamiento, debemos saber previamente lo que soy los paquetes npm. Consultar el capítulo 2 para más información sobre esto.

Para la instalación del módulo, introducimos el siguiente comando:

```
$ npm install gh-pages --save-dev
```

A continuación, tendremos que crear un fichero que ponga en funcionamiento el módulo. La sintaxis de este fichero es bastante sencilla y se basa principalmente en el uso de la función _publish_ del módulo gh-pages. Veamos un ejemplo en un fichero _deploy.js_:

```
var gh-pages = require('gh-pages');
var path = require('path');

gh-pages.publish(path.join(__dirname, 'docs'), {
    branch: master,
    //add: true,
    repo: 'https://github.com/ULL-ESIT-PL-1617/tareas-iniciales-Edu-Guille-Oscar-Sergio.git',
    //branch: master,
    remote: 'github',
    user: {
        //user options
    }
}, callback);
```

La llamada a la función publish creará una copia temporal del respositorio actual, creará una rama gh-pages local en caso de que no exista y copiará los archivos del directorio especificado \(en este caso 'docs'\). Hace un commit y por último un push al repositorio remoto. Si la rama gh-pages ya existe, llevará a cabo el mismo proceso pero actualizando la rama.

Nótese que hemos especificado una serie de opciones a la función \(algunas están comentadas\). La opción _branch_ nos permite especificar la rama remota a la que vamos a subir los archivos, siendo por defecto la rama gh-pages. La opción _add_ evita que se eliminen archivos, permitiendo solo que se añadan nuevos o se modifiquen anteriores.

La opción _repo_ es bastante interesante: permite especificar el repositorio remoto al que queremos hacer push de los archivos. Por defecto, se hará subirián al repositorio remoto especificado en los ficheros de configuración de git locales, pero en casos como el nuestro, que tenemos dos repositorios remotos para nuestro proyecto \(uno para GitHub y otro para GitBook\), conviene especificar a cuál queremos subir los archivos.

La opción _remote_ permite especificar el nombre del remoto al que queremos publicar. Por defecto es origin, pero podríamos tener nuestros enlaces a repositorios remotos con otro nombre. Del mismo modo que utilizábamos la opción _repo_ para evitar problemas con adónde exactamente se subirían los archivos, podemos utilizar esta opción.

Por último, la opción user permite especificar algunos parámetros de usuario como el nombre o el correo electrónico.

---

Como ejemplo de uso de GitHub Pages, en la introducción de este libro se han incluido enlaces cuatro sitios web que han sido creados aprovechando esta herramienta. Son los sitios web de los usuarios que conforman este grupo de trabajo.

