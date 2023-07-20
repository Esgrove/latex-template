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
