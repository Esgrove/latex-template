# LaTeX template

Modern LaTeX template for LuaTeX.

## Compile

Using shell script:

```shell
./build.sh
```

Manually in terminal:

```shell
lualatex --file-line-error --halt-on-error --interaction=nonstopmode "template.tex"
```

## Check available font features

```shell
otfinfo --features <font>
otfinfo -f <font>

# for example
otfinfo -f ./Inter-Regular.ttf
otfinfo -f ~/Library/Fonts/Montserrat-Regular.ttf
```

## Format reference file

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
