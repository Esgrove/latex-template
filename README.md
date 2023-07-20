# LaTeX template

Modern LaTeX template for LuaTeX.

## Compile

Using shell script:

```shell
./build.sh
```

Manually in terminal:

```shell
lualatex --shell-escape --halt-on-error --interaction=nonstopmode --file-line-error "template.tex"
```

## Check available font features

```shell
otfinfo --features <font>
otfinfo -f <font>

# for example
otfinfo -f ./Inter-Regular.ttf
otfinfo -f ~/Library/Fonts/Montserrat-Regular.ttf
```
