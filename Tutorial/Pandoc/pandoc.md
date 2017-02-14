# Pandoc

Pandoc es un **conversor** libre y de código abierto, escrito en **Haskell**,  que convierte archivos escritos en un determinado lenguaje de marcado, como MarkDown por ejemplo, a otro tipo de lenguaje. Fue creada por **John MacFarlane**, un profesor de Filosofía de la Universidad de Michigan, y representa una herramienta muy potente a la hora de convertir archivos.

### Funcionamiento

El funcionamiento de Pandoc es bastante sencillo. Se le pasa al programa un fichero escrito en MarkDown o en cualquiera de los formatos de entrada que soporta \(se especificarán más adelante\),  y lo pasa a un formato determinado, de entre los incluídos en formatos de salida.

### Formatos soportados por Pandoc

Pandoc puede convertir los siguientes formatos de entrada a los consiguientes de salida, cualquier combinación de éstos es posible gracias a ésta aplicación

**Entrada**:                                                                                           **Salida**:

* MarkDown                                                                 - HTML y todos sus formatos      
* reStructuredText                                                       - Microsoft Word y sus formatos
* textile                                                                         - OpenOffice/LibreOffice
* HTML                                                                         - Ebooks
* DocBook                                                                    - Formatos de documentación \(DocBook...\)
* LaTeX                                                                         - InDesign ICML
* MediaWiki markup                                                    - OPML
* TWiki markup                                                            - LaTeX y sus formatos
* OPML                                                                         - PDF
* Emacs Org-Mode                                                      - Lenguajes de marcado \(Markdown, MediaWiki markup...\)
* Txt2Tags
* Microsoft Word docx
* Libre Office ODT
* EPUB
* Haddock markup

### Instalación y uso

Para instalar Pandoc, debemos descargarnos un paquete para nuestro correspondiente sistema operativo en la página web oficial de Pandoc

[http://pandoc.org/installing.html](http://pandoc.org/installing.html "Enlace de descarga de Pandoc")

Una vez tengamos Pandoc instalado, usar el conversor es bastante sencillo a través de la línea de comandos

Para ello, debemos especificar:

* El formato de entrada, con la opción **-f**
* El formato de salida con la opción **-t**
* El nombre del fichero que queremos convertir \( Debe de estar en el mismo formato que el formato de salida\).
* La opción **-s**, permite que Pandoc añada plantillas y cabeceras al nuevo fichero creado.
* La opción **-o**, nos permite mandar la salida a un determinado fichero y no a la salida estándar.

#### **Ejemplos:**

```
pandoc nombreFicheroEntrada -f formatoEntrada -t formatoSalida -s -o nombreficheroSalida
```

Ejemplo de uso para un fichero ejemplo test.md y que se quiere pasar a html:

```
pandoc markdown.md -f markdown -t HTML -s -o fichero.html
```



