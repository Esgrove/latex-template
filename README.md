# LaTeX template

Modern LaTeX doc template for LuaTeX and [fontspec](https://github.com/latex3/fontspec/),
which enables using normal OpenType and TrueType fonts.

I have also included Master's Thesis templates for the University of Helsinki and Hanken School of Economics.
These try to follow the thesis guidelines for the respective schools quite closely.
I created them originally for people close to me when they were writing a thesis in these universities.
Both of them have the same example content here with some basic demonstration of how to work with LaTeX.

## Basic template

[template.tex](./template.tex)

### Compile

Using the shell script:

```shell
./build.sh
```

Manually in terminal:

```shell
lualatex --file-line-error --halt-on-error --interaction=nonstopmode "template.tex"
```

## University of Helsinki thesis template

[Helsinki-thesis.tex](./Helsinki-thesis.tex) and example bibliography in [references.bib](./references.bib).

```shell
./build.sh -b -f Helsinki-thesis.tex
```

## Hanken School of Economics thesis template

[Hanken-thesis.tex](./Hanken-thesis.tex) and example bibliography in [references.bib](./references.bib).

```shell
./build.sh -b -f Hanken-thesis.tex
```

## Format bibliography file

```shell
biber \
    --tool \
    --output_align \
    --output_indent=4 \
    --output_fieldcase=lower \
    --sortlocale en-GB \
    --output_file=references.bib \
    references.bib
```

## Check available OpenType font features

```shell
otfinfo --features <font>
otfinfo -f <font>

# for example
otfinfo -f ./Inter-Regular.ttf
otfinfo -f ~/Library/Fonts/Montserrat-Regular.ttf
```
