Programming Background
================
Supro Debnath

## Second Blog Post

My day to day workload primarily uses SAS and SQL. As a data analyst,
I’m responsible for partitioning and querying large datasets to extract
the relevant information I need for clients. The biggest problem I have
with SAS and SQL is the process of data visualization. R just seems a
lot more intuitive with ggplot, allowing me to create more complex
illustrations of models. The functionality of downloading packages and
having very easy access to syntax I am unfamiliar with. I’m able to
quickly debug errors and trace back lines of code that I can’t very
easily do in SAS or SQL. However, the one thing I do miss about SAS
specifically is the broad range of statistical capabilities offered by
the language. Being able to generate confidence intervals, various
estimates, and summary statistics with statements like `proc mean` or
`proc freq` made it a lot easier to see the breakdown of my data. I
think R is not a very difficult language to learn. I remember when I
first started learning R in my sophomore year of college, I thought that
it was a lot easier to maneuver compared to languages like Java or C++.
The more I practiced with R, the more I got comfortable using different
packages (contributing to Time Series and Machine Learning) and even
with ST558, learning how Git and various functions/loops can be used to
increase efficiency in my code.

## An Example of an R Markdown Output

``` r
plot(x = mtcars$wt, y = mtcars$mpg)
```

![](C:/Users/16787/OneDrive/Documents/suproman98.github.io/_posts/2022-06-08-blog-post-programming-background_files/figure-gfm/unnamed-chunk-1-1.png)<!-- -->

``` r
#rmarkdown::render("2022-06-08-blog-post-programming-background.Rmd", 
#                 output_format = "github_document",
#                output_dir = "C:/Users/16787/OneDrive/Documents/suproman98.github.io/_posts",
#                  output_options = list(
#                    df_print = "default",
#                    toc = FALSE,
#                    number_sections = FALSE,
#                    keep_html = FALSE)
#)
```

``` r
knitr::opts_chunk$set(fig.path = "../images/")
```
