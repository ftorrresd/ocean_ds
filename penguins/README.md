# Palmer Penguins

The goal of palmerpenguins is to provide a great dataset for data exploration & visualization, as an alternative to `iris`.

https://github.com/allisonhorst/palmerpenguins
https://doi.org/10.5281/zenodo.3960218

## About the data

Data were collected and made available by [Dr. Kristen
Gorman](https://www.uaf.edu/cfos/people/faculty/detail/kristen-gorman.php)
and the [Palmer Station, Antarctica LTER](https://pal.lternet.edu/), a
member of the [Long Term Ecological Research
Network](https://lternet.edu/).

The palmerpenguins package contains two datasets.

``` r
library(palmerpenguins)
data(package = 'palmerpenguins')
```

One is called `penguins`, and is a simplified version of the raw data;
see `?penguins` for more info:

``` r
head(penguins)
#> # A tibble: 6 x 8
#>   species island bill_length_mm bill_depth_mm flipper_length_… body_mass_g sex  
#>   <fct>   <fct>           <dbl>         <dbl>            <int>       <int> <fct>
#> 1 Adelie  Torge…           39.1          18.7              181        3750 male 
#> 2 Adelie  Torge…           39.5          17.4              186        3800 fema…
#> 3 Adelie  Torge…           40.3          18                195        3250 fema…
#> 4 Adelie  Torge…           NA            NA                 NA          NA <NA> 
#> 5 Adelie  Torge…           36.7          19.3              193        3450 fema…
#> 6 Adelie  Torge…           39.3          20.6              190        3650 male 
#> # … with 1 more variable: year <int>
```

The second dataset is `penguins_raw`, and contains all the variables and
original names as downloaded; see `?penguins_raw` for more info.

``` r
head(penguins_raw)
#> # A tibble: 6 x 17
#>   studyName `Sample Number` Species Region Island Stage `Individual ID`
#>   <chr>               <dbl> <chr>   <chr>  <chr>  <chr> <chr>          
#> 1 PAL0708                 1 Adelie… Anvers Torge… Adul… N1A1           
#> 2 PAL0708                 2 Adelie… Anvers Torge… Adul… N1A2           
#> 3 PAL0708                 3 Adelie… Anvers Torge… Adul… N2A1           
#> 4 PAL0708                 4 Adelie… Anvers Torge… Adul… N2A2           
#> 5 PAL0708                 5 Adelie… Anvers Torge… Adul… N3A1           
#> 6 PAL0708                 6 Adelie… Anvers Torge… Adul… N3A2           
#> # … with 10 more variables: `Clutch Completion` <chr>, `Date Egg` <date>,
#> #   `Culmen Length (mm)` <dbl>, `Culmen Depth (mm)` <dbl>, `Flipper Length
#> #   (mm)` <dbl>, `Body Mass (g)` <dbl>, Sex <chr>, `Delta 15 N (o/oo)` <dbl>,
#> #   `Delta 13 C (o/oo)` <dbl>, Comments <chr>
```

Both datasets contain data for 344 penguins. There are 3 different
species of penguins in this dataset, collected from 3 islands in the
Palmer Archipelago, Antarctica.

``` r
str(penguins)
#> tibble [344 × 8] (S3: tbl_df/tbl/data.frame)
#>  $ species          : Factor w/ 3 levels "Adelie","Chinstrap",..: 1 1 1 1 1 1 1 1 1 1 ...
#>  $ island           : Factor w/ 3 levels "Biscoe","Dream",..: 3 3 3 3 3 3 3 3 3 3 ...
#>  $ bill_length_mm   : num [1:344] 39.1 39.5 40.3 NA 36.7 39.3 38.9 39.2 34.1 42 ...
#>  $ bill_depth_mm    : num [1:344] 18.7 17.4 18 NA 19.3 20.6 17.8 19.6 18.1 20.2 ...
#>  $ flipper_length_mm: int [1:344] 181 186 195 NA 193 190 181 195 193 190 ...
#>  $ body_mass_g      : int [1:344] 3750 3800 3250 NA 3450 3650 3625 4675 3475 4250 ...
#>  $ sex              : Factor w/ 2 levels "female","male": 2 1 1 NA 1 2 1 2 NA NA ...
#>  $ year             : int [1:344] 2007 2007 2007 2007 2007 2007 2007 2007 2007 2007 ...
```

We gratefully acknowledge Palmer Station LTER and the US LTER Network.
Special thanks to Marty Downs (Director, LTER Network Office) for help
regarding the data license & use.