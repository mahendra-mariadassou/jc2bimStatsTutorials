
<!-- README.md is generated from README.Rmd. Please edit that file -->

# Inferential statistics tutorials

<!-- badges: start -->
<!-- [![binder](https://github.com/mahendra-mariadassou/learningr/workflows/binder/badge.svg)](https://mybinder.org/v2/gh/mahendra-mariadassou/learningr/master) -->
<!-- badges: end -->

The goal of this package is to provide interactive tutorials for the
\*Atelier sur les statistiques inférentielles". Tutorials are packaged
so you can install them on you computer and do the exercices without
access to an internet connection but a binder image is also provided as
a failsafe.

## Installation

### Local installation

You need to perform the following steps:

-   installing **R**
-   installing **Rstudio**
-   installing **R** package `remotes`

However each of them may take some time.

#### Installing R

Go to the CRAN [webpage](https://cran.r-project.org/), select your OS
and follow the instructions.

-   On Windows, you should just download and execute an .exe file.
-   On MacOS, you should just download and execute a .pkg file.
-   On Linux, you can get install R from the command line using
    something like

``` bash
## If you're on Ubuntu
sudo apt-get install r-base
```

#### Installing RStudio Desktop

Go to the
[download](https://rstudio.com/products/rstudio/download/#download)
page. Select, download and install the file corresponding to your OS.

#### Installing R packages

Launch Rstudio (by clicking on the corresponding icon) and execute the
following commands in the console

``` r
install.packages("remotes") 
```

#### Installation (II)

You need to install the tutorials **every time** there is an update
(hopefully not too often)

### Installing the tutorials

You can install the tutorials from [GitHub](https://github.com/) by
launching Rstudio and typing the following command in the console:

``` r
remotes::install_github("mahendra-mariadassou/jc2bimStatsTutorials")
```

<!-- Alternatively, you can use a remote R session to complete the tutorial by launching binder:  [![Binder](https://mybinder.org/badge_logo.svg)](https://mybinder.org/v2/gh/mahendra-mariadassou/learningr/master?urlpath=rstudio) -->

You only need a web browser, no account or anything and the tutorials
will always be up to date. The main drawbacks of this solution (compared
to the previous one) are that (i) you lose your progress each time you
launch a new session and (ii) the binder image may take some time to
launch (usually a few minutes).

## Starting a tutorial

This package is intended for use with `learnr`:

``` r
library(learnr)
```

You should only launch **one** tutorial at the time. Before launching a
new tutorial, **restart R**.

### Basic notions of R and ggplot

Those two tutorials are shamelessly taken from
[rstudio-education](https://rstudio.cloud/learn/primers). You can skip
those if you have prior knowledge of R and ggplot.

``` r
## Launch only one tutorial at the time!!
learnr::run_tutorial("01.1_programming_basics", package = "jc2bimStatsTutorials")
learnr::run_tutorial("01.2_visualisation_basics", package = "jc2bimStatsTutorials")
```

### Refresher on probability distributions

``` r
learnr::run_tutorial("02.1_random_variables", package = "jc2bimStatsTutorials")
learnr::run_tutorial("02.2_classical_distributions", package = "jc2bimStatsTutorials")
learnr::run_tutorial("02.3_bivariate_statistics", package = "jc2bimStatsTutorials")
```

### Estimation, confidence intervals and tests

``` r
learnr::run_tutorial("03.1_estimation", package = "jc2bimStatsTutorials")
learnr::run_tutorial("03.2_statistical_tests", package = "jc2bimStatsTutorials")
```

## Troubleshooting

If you have an error when launching a vignette (it may happen on Windows
with R &gt;= 4.0.0), try this syntax (illustrated on the first
vignette):

``` r
rmarkdown::run(file = NULL, 
               dir = learnr:::get_tutorial_path("01.1_programming_basics",  
                                                package = "jc2bimStatsTutorials"), 
               shiny_args = list(launch.browser = 1))
```
