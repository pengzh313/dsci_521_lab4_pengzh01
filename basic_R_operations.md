Lab4_Question 7
================
Peng Zhang
2022-10-01

# Introduction

This report is to demonstrate how to create a dataframe in R and do a
few simple operations.

## Create a new dataframe

We can create a toy dataframe from the below code:

``` r
df <- data.frame(name = c('John', 'Ty', 'Jim'),
                 age = c(21, 30, 45),
                 title = c('Estimator', 'Engineer', 'Manager'))
df
```

    ##   name age     title
    ## 1 John  21 Estimator
    ## 2   Ty  30  Engineer
    ## 3  Jim  45   Manager

## Operations on dataframe

We can select a particular column and output the specified column only.

``` r
# load necessary library
library(tidyverse)
```

    ## ── Attaching packages ─────────────────────────────────────── tidyverse 1.3.2 ──
    ## ✔ ggplot2 3.3.6     ✔ purrr   0.3.4
    ## ✔ tibble  3.1.8     ✔ dplyr   1.0.9
    ## ✔ tidyr   1.2.0     ✔ stringr 1.4.1
    ## ✔ readr   2.1.2     ✔ forcats 0.5.2
    ## ── Conflicts ────────────────────────────────────────── tidyverse_conflicts() ──
    ## ✖ dplyr::filter() masks stats::filter()
    ## ✖ dplyr::lag()    masks stats::lag()

``` r
df_1 <- df |> select(title)
df_1
```

    ##       title
    ## 1 Estimator
    ## 2  Engineer
    ## 3   Manager

We can filter the dataframe based on a certain condition. In the
following example, it will only output people with their age over 30.

``` r
df_2 <- df |> filter(age >30)
df_2
```

    ##   name age   title
    ## 1  Jim  45 Manager
