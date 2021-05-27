MARYURY GARCIA GELVES 1950186
================

## Mediciones diarias de la calidad del aire en Nueva York.

En este trabajo visualizaremos una base de datos la cual nos muestra las
mediciones diarias de la calidad del aire en Nueva York, en un marco de
datos de 153 observaciones sobre 6 variables., de mayo a septiembre de
1973, teniendo en cuenta los criterios de clasificación de
**Airquality.**

Crearemos un Dataframe de la calidad de aire en Nueva York.

``` r
data(airquality)
library(dplyr)
```

    ## 
    ## Attaching package: 'dplyr'

    ## The following objects are masked from 'package:stats':
    ## 
    ##     filter, lag

    ## The following objects are masked from 'package:base':
    ## 
    ##     intersect, setdiff, setequal, union

``` r
airquality <- mutate(airquality, Reflectancia=(Solar.R-Temp)^2/Ozone)

Reporte <-airquality$Reflectancia 
Mayo <- mean(Reporte[1:31])
Junio <- mean(Reporte[32:61])
Julio <- mean(Reporte[62:92])
Agosto <- mean(Reporte[93:123])
Septiembre <-mean(Reporte[123:153])
```

## Including Code

You can include R code in the document as follows:

``` r
summary(cars)
```

    ##      speed           dist       
    ##  Min.   : 4.0   Min.   :  2.00  
    ##  1st Qu.:12.0   1st Qu.: 26.00  
    ##  Median :15.0   Median : 36.00  
    ##  Mean   :15.4   Mean   : 42.98  
    ##  3rd Qu.:19.0   3rd Qu.: 56.00  
    ##  Max.   :25.0   Max.   :120.00

## Including Plots

You can also embed plots, for example:

![](Maryury-2-parcial-Diseño_files/figure-gfm/pressure-1.png)<!-- -->

Note that the `echo = FALSE` parameter was added to the code chunk to
prevent printing of the R code that generated the plot.
