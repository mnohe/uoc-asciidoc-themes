# UOC Asciidoctor PDF theme

[Asciidoctor PDF](https://github.com/asciidoctor/asciidoctor-pdf) theme for UOC deliveries and assignments. 

## Usage

Generally, you can bring this project in as a sub-module:

``` sh
git submodule add https://github.com/mnohe/uoc-asciidoc-theme
```
and run the following command on your Asciidoc sources:

``` sh
docker run --rm \
  -v $(pwd):/documents/ \
  --user "$(id -u):$(id -g)" \
  asciidoctor/docker-asciidoctor \
  asciidoctor-pdf \
  -r asciidoctor-mathematical \
  -r asciidoctor-diagram \
  -a mathematical-format=svg \
  -a diagram-format=svg \
  -a pdf-theme=uoc \
  -a pdf-themesdir=uoc-asciidoc-theme \
  -a pdf-fontsdir=uoc-asciidoc-theme/fonts \
  path/to/index.adoc
```

## Render the sample

``` sh
docker run --rm \
  -v $(pwd):/documents/ \
  --user "$(id -u):$(id -g)" \
  asciidoctor/docker-asciidoctor \
  asciidoctor-pdf \
  -r asciidoctor-mathematical \
  -r asciidoctor-diagram \
  -a mathematical-format=svg \
  -a diagram-format=svg \
  -a pdf-themesdir=/documents \
  -a pdf-fontsdir=/documents/fonts \
  -a pdf-theme=uoc \
  sample.adoc
```
