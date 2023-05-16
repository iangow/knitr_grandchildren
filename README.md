Knitr examples
===================

This example is intended to illustrate one way of including `knitr` code in
a parent document that is "pure" LaTeX.

The document `main_doc.Rnw` compiles without modification in RStudio.

To compile `main_doc_tex.tex`, it is first necessary to `knit` the two child
documents. 

```
library("knitr")
setwd("tables")
knit("world.Rnw")
knit("china.Rnw")
setwd("..")
```

Then one can simply compile the file `main_doc_tex.tex` using a LaTeX editor.