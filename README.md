
<!-- README.md is generated from README.Rmd. Please edit that file -->

# How to Bayes

<!-- badges: start -->
<!-- badges: end -->

Welcome to the *How to Bayes* workshop repository.

Please, follow these instructions to get ready before the workshop.

## Pre-requisites

Prior to joining the workshop, make sure you have installed or updated
the following.

-   The **latest version of R** (<https://cloud.r-project.org>).

-   The **latest version of RStudio**
    (<https://www.rstudio.com/products/rstudio/download/#download>).

-   Your **operating system is up-to-date**.

## Download

You can now **download this repository** on your own laptop.

If you fancy the command line, you can simply clone the repository in a
convenient location:

``` bash
git clone https://github.com/stefanocoretta/how-bayes.git
```

Or click on the green `Code` button and `Download ZIP`. Unzip the
archive and place the folder in a convenient location.

## Installation

Now you will need to install a few packages and extra software.

### Install the C++ toolchain

Some of the software requires a working C++ toolchain for compilation.

You can find information on how to set up the C++ toolchain at this address: <https://mc-stan.org/docs/2_29/cmdstan-guide/cmdstan-installation.html#installing-the-c-toolchain>.

Follow the instructions for your operating system.

### Install the R packages

Double click on the `how-bayes.Rproj` file, which
will open RStudio.

Then, run the following command in the console:

``` r
install.packages("renv")
renv::restore(prompt = FALSE)
```

It will take several minutes, depending on your system and
configuration.

### Install cmdstanr and CmdStan

When the installation is done, run the following command in the console:

``` r
renv::install("stan-dev/cmdstanr")
cmdstanr::install_cmdstan(cores = parallel::detectCores(), overwrite = TRUE)
```

This will install the `cmdstanr` back-end, which allows R and Stan (the
software behind Bayesian computation) to communicate with each other.

If at any point you get asked about installing extra software, depending on your
system, please do so.

## Troubleshoot

If you have issues with any of these steps, please get in touch with
Stefano.
