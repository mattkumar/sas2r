# (PART) Data Wrangling {.unnumbered}

# dplyr Example 1 {#dw-eg1}

Here is an example on how to select all columns of a data frame that have a common *suffix* 

```r
library(dplyr)

# select columns that end with Width
my_query <- iris %>%
  select(ends_with("Width"))

# check
head(my_query)
```

```
##   Sepal.Width Petal.Width
## 1         3.5         0.2
## 2         3.0         0.2
## 3         3.2         0.2
## 4         3.1         0.2
## 5         3.6         0.2
## 6         3.9         0.4
```
