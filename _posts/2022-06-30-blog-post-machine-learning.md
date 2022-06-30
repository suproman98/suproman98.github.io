Machine Learning Update
================
Supro Debnath

## Post-Project Thoughts

I think the coolest thing I’ve learned so far in this class has been
creating functions and working on completing a working Pokedex for my
first project. I anticipate that this answer will change once I dive
deeper into machine learning, but for now I think pulling data from an
API was incredibly interesting. Parsing through URLs, experimenting with
different setting in ggplot, and generating summaries from different
endpoints was certainly the most interesting aspect so far in this
class. I hadn’t done any work like it in my previous R courses, so while
it was difficult (and certainly frustrating) to grasp at times, I think
it was incredibly useful. Here is an example of pulling data from an
endpoint from the API that I researched.

## API Function

``` r
library(tidyverse)
library(dplyr)
library(jsonlite)
library(httr)
version <- function(game) {
  # Checks if a valid input has been entered into the function.
  if ((game > 34) || (game < 1)) {
    stop("This is an invalid game. Please refine search.")
  }
  
  #Set URL for the version endpoint in the API.
  respGAME <- GET(paste0("http://pokeapi.co/api/v2/version/", game))
  conGAME <- content(respGAME)
  ver <- conGAME$version_group$url %>% GET() %>% content()
  
  #Create a tibble that prints basic version information based on the function input.
  output <- tibble(
    name = ver$name,
    region = ifelse(is_empty(ver$region), NA, ver$regions[[1]]$name),
    generation = ver$generation$name
  )
  return(output)
}
```

Now we can call the function to print out the generation details.

``` r
version(5)
```

    ## # A tibble: 1 × 3
    ##   name        region generation   
    ##   <chr>       <chr>  <chr>        
    ## 1 gold-silver kanto  generation-ii

Overall, I think communicating with APIs are both unique but difficult,
as parsing through multiple embedded URLs can be tricky, as well as
dealing with data that isn’t present in the API (in my case, I wanted to
look at trainer and champion teams to see which type was used the most).
However, while APIs are certainly interesting, I’m a lot more excited to
dive into random forests and boosting, since there are so many different
factors that can influence a model’s performance.

### Knit Code

``` r
#rmarkdown::render("2022-06-30-blog-post-machine-learning.Rmd", 
#                 output_format = "github_document",
#                 output_dir = "_posts",
#                 output_options = list(
#                    df_print = "default",
#                    toc = FALSE,
#                    number_sections = FALSE,
#                    keep_html = FALSE)
#)
```

\`\`\`
