# Stage at Bluewind: topics

![bluewind logo](assets/bwlogo.png)

This repository contains slides listing topics for stage at Bluewind.
Slides are prepared using Markdown files, that will be rendered as HTML files
using Remark based templates (see credits for details).

### Language

Slides language is English.

# Slides preparation and usage workflow

### Local copy

Please clone this repository including submodules:

```bash
$ git clone <this repo>
$ cd <this repo folder>
$ git submodule update --init
$ # or in one command
$ git clone --recursive <this repo>
```

### Working on existing slide sets

  - open the relevant markdown file with an editor
  - modify the content using normal markdown sintax with an eye to
    specific meanings for Remark based slides as found in the credits
  - enjoy the final result by opening the corresponding HTML file in a browser

```bash
user@host:~/code/stages-topic⟫ nano existing_slides.md
user@host:~/code/stages-topic⟫ firefox existing_slides.html
```

### Adding new slides sets

  - create a copy of existing markdown and HTML files, with a new name for both
  - modify the HTML file changing all references to its old name to the new name
  - modify and add content to the markdown file
  - enjoy the final result by opening the corresponding HTML file in a browser
  - add the new files under git control

```bash
user@host:~/code/stages-topic⟫ cp existing_slides.md new_slides.md
user@host:~/code/stages-topic⟫ cp existing_slides.html new_slides.html
user@host:~/code/stages-topic⟫ sed -i.bak 's/existing_slides/new_slides/' new_slides.html
user@host:~/code/stages-topic⟫ nano new_slides.html
user@host:~/code/stages-topic⟫ firefox new_slides.html
```

### Including images in slides

  - copy the useful image in ```assets``` subfolder
  - use normal markdown sintax to include the image in a slide

# Additional tools and operations

### Converting markdown files to PDF

When distributing slides it can be useful to prepare PDF files out of
markdown sources, because printing rendered HTML slides to PDF from the
browser gives strange results.

The best converter found is decktape:

https://github.com/astefanutti/decktape

and a docker image for easy usage of the tool is also available.

Please note that good results are obtained by processind HTML pages
published to a server, so in this example Github pages are used.

```bash
# Convert all slides to PDF files
# and write them inside pdf folder
for f in *.html; do \
docker run --rm -v `pwd`:/slides astefanutti/decktape \
https://stefanoco.github.io/stage-topics/$f pdf/${f%.*}.pdf; \
done
```

### Including images embedded in html / css files

Handy way of including images embedded in css (and html if applicable) files is
preparing base64 version and including the resulting ASCII string.

```bash
user@host:~/code/stages-topic⟫ cat assets/image.png |base64 -w0>b64.txt
```

This is useful while customising the slides template by modifying the
css file:

```bash
user@host:~/code/stages-topic⟫ nano remark/remark-template-bw.css
```

### Building (html) slides from (markdown) sources

```bash
user@host:~/code/stages-topic⟫ sudo apt-get install nodejs-legacy
user@host:~/code/stages-topic⟫ sudo apt-get install npm
user@host:~/code/stages-topic⟫ sudo npm install markdown-to-slides -g
user@host:~/code/stages-topic⟫ markdown-to-slides 1_requirements.md -o 1_requirements.html -s remark/remark-template-bw.css
```
This is deprecated now: please use instead the existing ```.html``` files
directly, they will include ```.md``` sources on the fly.

### Credits

- 2016 Stefano Costa, Bluewind
- https://github.com/gnab/remark/wiki
- http://tech.graze.com/2015/07/31/easily-create-slideshow-presentations-from-markdown-with-remark-js/
