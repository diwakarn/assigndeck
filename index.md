---
title       : Predicton of weight of American women based on height
subtitle    : Developing data products course - December 2015
author      : ND
job         : Goofer
framework   : io2012        # {io2012, html5slides, shower, dzslides, ...}
highlighter : highlight.js  # {highlight.js, prettify, highlight}
hitheme     : tomorrow      # 
widgets     : []            # {mathjax, quiz, bootstrap}
mode        : selfcontained # {standalone, draft}
knit        : slidify::knit2slides
---

## Executive Summary

1. Shinayapp - predict weight range  of an american woman in lbs , given the height in inches

2. Uses the women data set in datasets package in R

3. Prediction based on linear regression 

4. Range of weight supplied based on the estimate @95% confidence


--- .class #id 

## Base Data for the Model 

Women Data set is used for this example 


```r
library(datasets)
head(women,2)
```

```
##   height weight
## 1     58    115
## 2     59    117
```
This contains height in inches and average weight in lbs 

--- .class #id 

## The Prediction  Model 

A linear regression model l1 is created at the start of the Application

```r
l1 <- lm(weight~ height,data = women)
 l1$coefficients
```

```
## (Intercept)      height 
##   -87.51667     3.45000
```
The prediction function 

p1 <- predict(l1, newdata, interval="predict") 

predicts  the range of weights with the lower and upper ranges 
available from the object p1


--- .class #id 


## Application Screen 

![width] (Picture1.bmp)



The link to the application is https://diwakarn.shinyapps.io/dataprod
 

--- .class #id 

