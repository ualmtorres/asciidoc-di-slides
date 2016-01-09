# Introducción

Proyecto para la creación de presentaciones Asciidoc con plantilla básica para el Departamento de Informática de la UAL. Incluye el logo del Departamento de Informática en `reveal.js/css/theme/logo.png`.

Usa este proyecto modificando únicamente el archivo `slide.adoc`

## Requisitos

Debes tener instalado **Asciidoctor**, una herramienta desarrollada en Ruby que permite convertir contenido AsciiDoc a HTML5, DocBook 5 y otros formatos.

Puedes instalar Asciidoctor de estas dos formas:

* [Instalar la gema asciidoctor](http://asciidoctor.org/)

```
gem install asciidoctor
```

* [Instalar Asciidoc FX](http://www.asciidocfx.com/) **(Recomendado)**. Asciidoc FX es un editor de documentos asciidoc (`*.adoc`) multiplataforma que pemite ver en tiempo real el resultado. Asciidoc FX permite crear  fácilmente contenidos en PDF, HTML, Epub, Mobi, Odt, Docbook. Dispone además de una serie de extensiones muy interesantes, como por ejemplo las que permiten trabajar con UML, hacer presentaciones HTML con Reveal.js o Deck.js, destacado de sintaxis de código fuente, símbolos matemáticos, y demás.

## Generación de la presentación

Desde el directorio de la presentación ejecuta este comando 

```
asciidoctor -T asciidoctor-reveal.js/templates/slim/  slide.adoc 
```

## Consideraciones:

* Al principio del documento aparece comentado el coloreado de la sintaxis con objeto de que se pueda ver la presentación en AsciidocFX mientras se confecciona la presentación. Una vez, creada la presentación se pueden eliminar los comentarios de 

```
/// :source-highlighter: highlightjs
```

* Las notas del orador sí se verán si se exporta la presentación a PDF.
* Los PDFs generados a partir del archivo `*.adoc` de la presentación no pueden incluir videos. Por tanto, el video de Youtube incluido en la última diapositiva producirá un error si se genera un PDF a partir de la presentación. Basta con comentarlo si se quiere generar el PDF.
* 

```
/// video::2goMtz_vdtM[youtube, width=800, height=500]
```