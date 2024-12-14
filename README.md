
<!-- README.md is generated from README.Rmd. Please edit that file -->

# tidyfft

<!-- badges: start -->
<!-- badges: end -->

The goal of tidyfft is to make working with fft’s in R easier and more
consistent. It follows the tidy philosophy by storing output in a
tibble.

## Installation

You can install the development version of tidyfft from
[GitHub](https://github.com/) with:

``` r
# install.packages("pak")
pak::pak("thk686/tidyfft")
```

## Example

This is a basic example which shows you how to solve a common problem:

``` r
library(ggplot2)
library(tidyfft)
tidy_fft(sunspot.month) |>
  plot() +
  scale_y_continuous(trans = "log") +
  scale_x_continuous(trans = "log") +
  geom_vline(aes(xintercept = 1), lty = 2, alpha = 0.5) +
  geom_vline(aes(xintercept = 0.1), lty = 2, alpha = 0.5) +
  geom_vline(aes(xintercept = 0.01), lty = 2, alpha = 0.5) +
  xlab("cycles per year") +
  geom_smooth()
#> `geom_smooth()` using method = 'gam' and formula = 'y ~ s(x, bs = "cs")'
```

<img src="man/figures/README-example-1.png" width="100%" />
