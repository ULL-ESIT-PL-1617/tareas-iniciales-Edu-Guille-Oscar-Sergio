# LAS GH-PAGES

Las GitHub Pages, conocidas también como las gh-pages, son una herramienta que la plataforma GitHub ofrece a los desarrolladores. Se trata de un servicio estático de hosting para páginas webs, diseñado para alojar páginas personales, de organizaciones o de proyectos directamente en un repositorio de GitHub. Es ideal para sitios informativos con un funcionamiento básico, pero no para sitios web más complejos puesto que no soporta la ejecución de código en el lado del servidor; lenguajes como PHP, Ruby o Python son inservibles.

Los sitios alojados en GitHub Pages se asocian con el dominio _.github.io_ y utilizan el protocolo HTTPS.



### PARA USUARIOS Y ORGANIZACIONES

Las páginas orientadas a la representación de usuarios y organizaciones se alojan en un repositorio específico dedicado a sus archivos. Estos repositorios deberán llamarse con el nombre de usuario \(o de la organización\) de la siguiente manera:

```
username.github.io --- organizationName.github.io
```

Los pasos para la creación de la página, utilizando la terminal, serían los siguientes:

1. Crear el repositorio. Su nombre deberá corresponderse con el ya mencionado.
2. Clonamos el repositorio en la máquina donde vayamos a trabajar.
3. Situamos el código HTML5 de nuestra página en el repositorio local.
4. Confirmamos los cambios y hacemos _push_ al repositorio remoto, en la rama master. 

Seguidos estos cuatro pasos, el sitio web debería estar disponible después de algunos segundos. Simplemente abrimos un navegador e introducimos la dirección de la página, que se corresponde con el nombre que le dimos al repositorio. Es importante saber que el contenido debe estar en la rama master: en las páginas para usuarios y organizaciones el código fuente HTML5 no puede situarse en ninguna otra localización.



### PARA PROYECTOS

En el caso de las páginas para proyectos, se puede configurar GitHub Pages para que publique el sitio web en base a los ficheros fuente HTML5 situados en la rama

