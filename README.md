# Developing Bioconductor-friendly packages using biocthis

This repository hosts the material for the [Ryten lab](https://rytenlab.com/) [biocthis](https://github.com/lcolladotor/biocthis) workshop.

# Prerequisites

-   A solid foundation in `R` and understanding of how to create your own functions.

-   An installation of the latest `biocthis` development version and it's dependencies via the code below, preferably on R v4.0 or above.

``` r
if (!requireNamespace("remotes", quietly = TRUE)) {
    install.packages("remotes")
}

remotes::install_github(c(
    "lcolladotor/biocthis", 
    "ropensci/bibtex",
    "ropensci/RefManageR",
    "cboettig/knitcitations"
))

remotes::install_cran(
    c(
        "available",
        "BiocManager",
        "devtools",
        "knitr",
        "pkgdown",
        "rmarkdown",
        "rstudioapi",
        "sessioninfo",
        "styler",
        "usethis"
    )
)

if (!requireNamespace("BiocStyle", quietly = TRUE)) {
    BiocManager::install("BiocStyle")
}
```

-   (Optionally) come with a function in mind that you would like to add to the example package we will create. Otherwise you will use an example function provided. If you do come with your own function, make sure it's already implemented.

# Acknowledgments

We are really grateful to [Leo](http://lcolladotor.github.io/), whose development of [biocthis](https://github.com/lcolladotor/biocthis) has made the creation of Bioconductor-friendly packages much easier.
