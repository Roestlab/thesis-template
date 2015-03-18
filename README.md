
# Thesis template

This repository contains a template that may be used to write an academic
thesis, such as a PhD or Master thesis. It was designed to be used at ETH
Zurich and conforms to the requirements of this university. However, it should
easily be adoptable to other university's requirements.

## Compile

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

