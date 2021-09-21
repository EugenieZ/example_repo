Simple document
================
Yujin Zhang
2021-9-16

I’m an R Markdown document!

# Section 1

Here’s a **code chunk** that samples from a *normal distribution*:

``` r
samp = rnorm(100)
length(samp)
```

    ## [1] 100

# Section 2

I can take the mean of the sample, too! The mean is 0.0794851.

# Section 3

Let’s write a new code chunk.

This code chunk imports the ‘tidyverse’, creates a data frame, and makes
a histagram.

``` r
library(tidyverse)

set.seed(1)

plot_df = tibble(
  x = rnorm(1000, sd = .5),
  y = 1 + 2 * x + rnorm(1000)
)

ggplot(plot_df, aes(x = x)) + geom_histogram()
```

![](template_files/figure-gfm/unnamed-chunk-2-1.png)<!-- -->

``` r
ggplot(plot_df, aes(x = x, y = y)) + geom_point()
```

![](template_files/figure-gfm/unnamed-chunk-2-2.png)<!-- -->

# Section 4

This code chunk creates a dataframe.

``` r
library(tidyverse)

learning_df = tibble(
   x = rnorm(500, mean = 1),
   gr_than_0 = x > 0,
   abs_val = abs(x)
   )

ggplot(learning_df, aes(x = abs_val)) + geom_histogram()
```

    ## `stat_bin()` using `bins = 30`. Pick better value with `binwidth`.

![](template_files/figure-gfm/unnamed-chunk-3-1.png)<!-- -->
