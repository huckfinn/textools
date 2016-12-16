# textools [![Build Status](https://travis-ci.org/simonharrer/textools.png?branch=master)](https://travis-ci.org/simonharrer/textools) [![Dependency Status](https://www.versioneye.com/user/projects/54c65d551a0071a7e4000058/badge.svg?style=flat)](https://www.versioneye.com/user/projects/54c65d551a0071a7e4000058) 

Textools provides CLI commands for the most commonly used tasks when working with [LaTeX](http://www.latex-project.org/),
e.g., generating a `.gitignore` file, creating the final pdf and validating the `.tex` and `.bib` files.

**Only** works for UTF-8 encoded `.tex` and `.bib` files.

## Installation

Requires JDK 8 with JAVA_HOME set to the JDK path!

    $ git clone git@github.com:simonharrer/textools
    $ cd textools
    $ gradlew installDist
    # add textools/build/install/textools/bin to PATH

## Usage

    # in your latex directory
    $ textools pdf # create the pdf with pdflatex and bibtex using main.tex as the starting file
    $ textools validate # validates all .tex and .bib files using Simon's validation rules
    $ textools clean # remove all generated files like .div, .pdf, .log, ...

## Commands

    textools [command]

     create-gitignore             creates a latex project specific .gitignore file
     clean                        Removes all generated files during a tex build
     texlipse                     generates texlipse project files
     texniccenter                 generates the texniccenter project files
     validate                     executes validate-latex and validate-bibtex commands in sequence
     validate-bibtex              validates all .bib files for the existence of certain fields
     validate-latex               validates .tex files
     validate-acronym             detects unmarked acronyms in text
     minify-bibtex-optionals      removes optional keys in bibtex entries
     minify-bibtex-authors        replace additional authors with et al. in bibtex entries
     pdf                          creates pdf with pdflatex, including bibtex; logs to textools-pdf.log
     pdfclean                     executes pdf and clean commands in sequence
     version                      prints the current version
     help                         prints usage information

## Works best when

- the citation style is numeric/alphanumeric.
- each sentence is in its own line.
- labels in tables/figures should be put right after the caption
- all files are in UTF-8

## Authors

[Simon Harrer](mailto:simon.harrer@gmail.com)

## Contribute

    10 Fork
    20 Create feature branch
    30 Create commits
    40 Create pull request
    GOTO 10
