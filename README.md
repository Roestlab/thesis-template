
# Thesis template

This repository contains a template that may be used to write an academic
thesis, such as a PhD or Master thesis. It was designed to be used at ETH
Zurich and conforms to the requirements of this university. However, it should
easily be adoptable to other university's requirements.

## Features

The following template contains sample code to create

- a title page as required by ETH Zurich
- an abstract in two languages
- an auto-generated abbreviation section 
- a multi-part thesis with integration into the table of content
- an inspirational quote at the beginning of a chapter
- a bibliography at the end of each chapter
- figures with captions on a new page
- a basic thesis structure that can be used to get started quickly

It is adopted to A4 paper as is custom in Europe.

## Compile

This template uses [biber](http://biblatex-biber.sourceforge.net/ Biber) to
create the bibliography instead of BibTeX. Biber is a modern replacement for
BibTeX when used with BibLaTeX and it has full support for UTF-8
bibliographies, see for example [this article](http://tex.stackexchange.com/questions/25701/bibtex-vs-biber-and-biblatex-vs-natbib)
for a discussion of the various packages available for creating a bibliography
in LaTeX.

Compile with biber/biblatex:

    pdflatex phdthesis_template
    makeindex phdthesis_template.nlo -s nomencl.ist -o phdthesis_template.nls
    biber phdthesis_template
    pdflatex phdthesis_template
    pdflatex phdthesis_template

The .tex document requires a dummy.png and a sample bibliography. These are part of the repository but can also be obtained from 

    convert -size 600x600 xc:gray dummy.png
    wget http://ctan.mackichan.com/macros/latex/exptl/\
    biblatex/doc/examples/biblatex-examples.bib

## Extra info

This template does not use different margins for even and odd pages. However it
does contain code that allows treating the headers differently on odd and even
pages. Note that odd pages are always on the right.

