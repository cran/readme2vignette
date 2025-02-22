
<!-- README.md is generated from README.Rmd. Please edit that file -->

# readme2vignette

<!-- badges: start -->
<!-- badges: end -->

The goal of `readme2vignette` is to attempt to install a package
directly GitHub or CRAN with convert `README.md` to Vignette during
Package installation.

Based on `remotes::install_github()` and `remotes::install_cran()` that
`remotes` version 2.4.2.

## Installation

You can install the released version of `readme2vignette` from CRAN
with:

``` r
install.packages("readme2vignette")
```

You can install the development version of `readme2vignette` like so:

``` r
install.packages("remotes")
remotes::install_github("indenkun/readme2vignette")
```

## Example

### `install_cran_with_readme()`

The basic usage is the same as `remotes::install_cran()`.

If you try to install a package with README.md but no vignette from CRAN
Repository using `readme2vignette::install_cran_with_readme()`, by
default the argument `readme_to_vignette` is TRUE and the contents of
`README.md` becomes a vignette called README.

Installation from binary packages is not supported. Installation must
always be done from the sourceco package.

``` r
readme2vignette::install_github_with_readme("MissMech")
```

Therefore, the contents of `README.md` can be referenced in the local
environment by `vignette("README", package = "packagename")`.

``` r
vignette("README", package = "MissMech")
```

### `install_github_with_reademe()`

The basic usage is the same as `remotes::install_github()`.

If you try to install a package with README.md but no vignette from
GitHub using `readme2vignette::install_github_with_readme()`, by default
the argument `readme_to_vignette` is TRUE and the contents of
`README.md` becomes a vignette called README.

``` r
readme2vignette::install_github_with_readme("indenkun/MissMech")
```

Therefore, the contents of `README.md` can be referenced in the local
environment by `vignette("README", package = "packagename")`.

``` r
vignette("README", package = "MissMech")
```

## Note

The `remotes` package on which this code is based was created by the
author of `remotes` and is now released at MIT.

The author of the remotes package is currently listed as Developed by
Gábor Csárdi, Jim Hester, Hadley Wickham, Winston Chang, Martin Morgan,
Dan Tenenbaum, Posit Software, PBC.

See [r-lib/remote](https://github.com/r-lib/remotes) for detailed
authorship.

Under the current specification, the images in the `README.md` are
copied for the figures in the directories under `man/figures/`, but not
for the images in other directories, which are missing.

## License

MIT

## Imports packages

- `desc`
- `fs`
- `knitr`
- `pkgbuild`
- `remotes`
- `rmarkdown`
- `usethis`
- `utils`
