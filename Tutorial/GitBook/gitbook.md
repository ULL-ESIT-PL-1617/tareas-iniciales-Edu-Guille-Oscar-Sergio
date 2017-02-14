# GitBook

#### ¿Qué es?

[GitBook](/www.gitbook.com "Gitbook") es una plataforma online para la publicación de libros, documentos, manuales y trabajos de investigación en Internet. Lanzado en el 2014, GitBook permite tanto a usuarios individuales como a organizaciones empresariales crear sus publicaciones digitales en Internet empleando el sistema de control de versiones Git, desarrollando los contenidos mediante el uso de la sintaxis en Markdown.

La plataforma ha sido creada bajo código abierto que podemos consultar en los servidores de GitHub. Podremos crear  cuentas de usuarios de  manera tradicional o incluso usando nuestra cuenta de GitHub y dando permisos a la aplicación. Además de GitHub podremos usar cuentas de Twitter, Facebook o Google. GitBook nos permite elegir si queremos que nuestra publicación sea pública o privada, para lo cual tendremos que tener una cuenta de pago.

#### Instalar GitBokk

Gitbook esta implementado usando [NodeJS](https://nodejs.org/es/) \(Capítulo 2\) y podremos instalarlo usando [NPM](https://www.npmjs.com/):

```
$npm install gitbook-cli --save-dev
```

#### Como se utiliza GitBook

Una vez tengamos instalado GitBook podremos empezar a crear nuestros libros que estarán alojadas en un repositorio de la plataforma.

Para **crear nuestro libro** tendremos que hacer:

```
$gitbook init nombre_del_libro
```

Esto nos creará una carpeta con el nombre de nuestro libro en la que se encuentran todos los ficheros MarkDown del mismo. Tras esto tendremos que entrar en dicha carpeta y especificar las dependencias de nuestro proyecto, para ello usaremos:

```
$npm init -y
```

Una vez ejecutamos el comando, el fichero [package.json](https://docs.npmjs.com/files/package.json) en el que se especifican las dependencias de nuestro proyecto.

