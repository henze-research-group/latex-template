# CU Boulder's LaTeX Template

This repository contains an updated version of CU's LaTeX class with support for a couple other features including:

* table of acronyms
* table of code snippets

The resulting PDF contains examples on how to best use LaTeX for a PhD Prospectus or PhD Thesis.

To use, open `main-cu-prospectus.tex` in your favorite Tex editor such as TexStudio or VSCode. You can also upload this entire package to Overleaf to edit collaboratively online.

One catch is that to see the acronyms the `makeglossaries` command needs to be in the build step. This repo committed the .vscode/settings.json file with the changes. In TexStudio, this will need to be 
manually configured as well. Also, it is common to have to call the `pdflatex` command twice to have the glossaries show up correctly.

```
    "latex-workshop.latex.recipes":[
        {
            "name": "Build with glossaries",
            "tools": [
                "pdflatex",
                "makeglossaries",
                "pdflatex",
                "pdflatex"
            ]
        },
    ],
    "latex-workshop.latex.tools":[
        {
            "name": "pdflatex",
            "command": "pdflatex",
            "args": [
                "-synctex=1",
                "-interaction=nonstopmode",
                "-file-line-error",
                "%DOC%"
            ]
        },
        {
            "name": "makeglossaries",
            "command": "makeglossaries",
            "args": [
              "%DOCFILE%"
            ]
          }
    ]
```

An example PDF is in this project [here](./main-cu-prospectus.pdf) and [here](./main-cu-phd-thesis.pdf) but a version is created each commit on GitHub. The GitHub veresion is [here](https://github.com/henze-research-group/latex-template/actions). Go to the latest passing workflow run, then click on the PDF text in the Artifacts section. Note that the GitHub build version does not have the Acronyms listing since the build step does not know how to `makeglossaries`.

The difference between the prospectus and thesis is minimal. The prospectus version contains language that it is just that, a prospectus, and the thesis.cls has the approval page.

