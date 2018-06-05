Data generation
================

``` r
library("tibble")
library("tidyr")
library("readr")
```

``` r
get_data <- function(){
  tibble(
    month = month.abb,
    number = round(rnorm(12, 100, 50))
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

    ## # A tibble: 12 x 2
    ##    month number
    ##    <chr>  <dbl>
    ##  1 Jan     135.
    ##  2 Feb      93.
    ##  3 Mar     122.
    ##  4 Apr      17.
    ##  5 May      88.
    ##  6 Jun      93.
    ##  7 Jul     195.
    ##  8 Aug      82.
    ##  9 Sep      39.
    ## 10 Oct     207.
    ## 11 Nov      89.
    ## 12 Dec      50.

``` r
data_02
```

    ## # A tibble: 12 x 2
    ##    month number
    ##    <chr>  <dbl>
    ##  1 Jan      67.
    ##  2 Feb      72.
    ##  3 Mar     104.
    ##  4 Apr       9.
    ##  5 May     211.
    ##  6 Jun     128.
    ##  7 Jul      19.
    ##  8 Aug     228.
    ##  9 Sep      50.
    ## 10 Oct     106.
    ## 11 Nov      36.
    ## 12 Dec      89.
