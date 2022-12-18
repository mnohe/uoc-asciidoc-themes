# UOC Asciidoctor PDF theme

[Asciidoctor PDF](https://github.com/asciidoctor/asciidoctor-pdf) theme for UOC deliveries and assignments. 

## Usage

``` sh
docker run --rm -v $(pwd):/documents/ \
  asciidoctor/docker-asciidoctor \
  asciidoctor-pdf \
  -r asciidoctor-mathematical \
  -r asciidoctor-diagram \
  -a mathematical-format=svg \
  -a diagram-format=svg \
  -a pdf-theme=uoc \
  -a pdf-themesdir=<uoc-asciidoc-theme_location> \
  -a pdf-fontsdir=<uoc-asciidoc-theme_location>/fonts \
  index.adoc
```

## Render the sample

``` sh
docker run --rm -v $(pwd):/documents/ \
  asciidoctor/docker-asciidoctor \
  asciidoctor-pdf \
  -r asciidoctor-mathematical \
  -r asciidoctor-diagram \
  -a mathematical-format=svg \
  -a diagram-format=svg \
  -a pdf-themesdir=/documents \
  -a pdf-fontsdir=/documents/fonts \
  sample.adoc
```
