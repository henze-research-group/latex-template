# CU Boulder's LaTeX Template

This repository contains an updated version of CU's LaTeX class with support for a couple other features including:

* table of acronyms
* table of code snippets

The resulting PDF contains examples on how to best use LaTeX for a PhD Prospectus.

To use, open `main-cu-prospectus.tex` in your favorite Tex editor. I use TexStudio. You can also upload this entire package to Overleaf to edit collaboratively online.

An example PDF is in this project [here](./main-cu-prospectus.pdf) but a version is created each commit on GitHub. The GitHub veresion is [here](https://github.com/henze-research-group/latex-template/actions). Go to the latest passing workflow run, then click on the PDF text in the Artifacts section. Note that this version does not have the Acronyms listing since the build step does not know how to `makeglossaries`.