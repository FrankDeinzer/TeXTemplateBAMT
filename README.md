# Configuration

## Language
Select the language in the file ```doc.tex``` at the very top:

    %\def\MyLanguage{english}
    \def\MyLanguage{ngerman}

## Thesis type
Select the thesis type in the file ```doc.tex``` at the very top:

    %% bt: Bachelor Thesis
    %% mt: Master Thesis
    \documentclass[\MyLanguage,bt]{dbvdoc}

# Building a pdf document

## Creating a pdf document on the tex->pdf path
    pdflatex doc
    biber doc
    pdflatex doc
    pdflatex doc

## Create a pdf document on the path tex->dvi->ps->pdf
    latex doc
    biber doc
    latex doc
    latex doc
    dvips doc
    ps2pdf14 -dUseFlateCompression#true -dPDFSETTINGS#/prepress -dEmbedAllFonts#true -sPAPERSIZE#a4 doc.ps doc.pdf

This mode will allow for tricks like psfrag
