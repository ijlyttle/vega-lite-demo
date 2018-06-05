Data generation
================

``` r
library("tibble")
library("tidyr")
library("readr")
library("here")
```

    ## here() starts at /Users/ijlyttle/Documents/git/github/public_work/vega-lite-demo

``` r
n_obs <- 10

get_data <- function(){
  tibble(
    category = LETTERS[seq(n_obs)],
    number = round(rnorm(n_obs, 100, 50))
  )  
}
```

``` r
data_01 <- get_data()
data_02 <- get_data()
```

``` r
data_01
```

    ## # A tibble: 10 x 2
    ##    category number
    ##    <chr>     <dbl>
    ##  1 A           90.
    ##  2 B          139.
    ##  3 C           62.
    ##  4 D          155.
    ##  5 E          128.
    ##  6 F           87.
    ##  7 G          102.
    ##  8 H          235.
    ##  9 I          108.
    ## 10 J           59.

``` r
data_02
```

    ## # A tibble: 10 x 2
    ##    category number
    ##    <chr>     <dbl>
    ##  1 A          142.
    ##  2 B          157.
    ##  3 C          206.
    ##  4 D          -11.
    ##  5 E          124.
    ##  6 F           86.
    ##  7 G           95.
    ##  8 H           59.
    ##  9 I           -1.
    ## 10 J           72.

``` r
write_csv(data_01, here("data-raw", "data_01.csv"))
write_csv(data_02, here("data-raw", "data_02.csv"))
```
