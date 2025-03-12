# Algoritmos y Estructuras de Datos

Este es el repositorio del sitio web de Introducción al Desarrollo de Software, publicado en:

<https://intro-tb022.github.io/intro/>

## Instrucciones para actualizar la página web

Cualquier commit en el directorio raíz se auto-publica en la página al hacer push a la branch _main_. GitHub se encarga de ese proceso.

Para visualizar los cambios de manera local, se debe instalar [Jekyll](https://jekyllrb.com/docs/installation/). El archivo [Gemfile](Gemfile) lo hace bastante fácil:

```
# Setup inicial

$ apt-get install ruby ruby-dev bundler
$ gem install jekyll bundler
$ git clone git@github.com:intro-tb022/intro
$ cd intro
$ bundle install --path=../gems
$ // de tener problemas con nokogiri: apt-get install libxml2-dev

# Para visualizar al editar

$ cd intro
$ bundle exec jekyll serve --livereload
$ // de tener problemas con javascript runtime: apt-get install nodejs

```

(La opción `--livereload` es opcional, pero fuerza al navegador a mostrar
el nuevo contenido tras escribir un archivo.)

## Actualizar página de docentes

Una vez que está por comenzar el cuatrimestre, es necesario actualizar la página de docentes con los que van a ser parte del curso. Para esto, lo único necesario es actualizar en el directorio `_data` el archivo `docentes.yml` con el nombre de cada docente, y el archivo de la foto. Mientras no se tenga una foto de algún corrector, se puede usar el archivo `assets/img/docentes/unknown.png`.

## Subir nuevas encuestas

Para subir las encuestas de un cuatrimestre, subir el archivo dentro del directorio `assets/encuestas`, con nombre `YYYY-cuat.html`. Actualizar también la página de encuestas (`static/08_encuestas.md`).