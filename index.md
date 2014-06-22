---
title       : BMI Calculator - Shiny Web App 
subtitle    : 
author      : P.L.
job         : 
framework   : io2012        # {io2012, html5slides, shower, dzslides, ...}
highlighter : highlight.js  # {highlight.js, prettify, highlight}
hitheme     : tomorrow      # 
widgets     : []            # {mathjax, quiz, bootstrap}
mode        : selfcontained # {standalone, draft}
knit        : slidify::knit2slides
---

## BMI Calculator - Usage

This Web App is calculating the BMI and the category of weight for a user.

The user enters the values for:

    1. name
    2. weight in kg
    3. height in cm

and the application is calculating the bmi and the category of weight.

To enter the name the user just types the name in the name textbox.

To enter the weight and height the user uses the sliders for weight and height.

---

## BMI Calculator - Formula

To calculate the bmi the app is using the following formula:

    bmi = (weight)/((height/100)^2)

To get the weight category the app is using the following table:

| BMI       | Weight category |
|-----------|-----------------|
|< 18.5     | underweight     |
|< 25	    | normal weight   |
|< 30   	| overweight      |
|>= 30	    | obesity         |

---

## BMI Calculator - R functions

To calculate bmi and category the app is using the following R functions:


```r
bmiCalculator <- function(weight, height) {
    weight/((height/100)^2)
}
category<-function(bmi){
    if(bmi<18.5) "underweight"
    if(bmi<25)   "normal weight"
    if(bmi<30)   "overweight"
    if(bmi>=18.5)"obese"
}
```

--- 

## BMI Calculator - Examples



1. A patient with a weight of 50 and height of 170, has a BMI of 17.3 and is underweight.

2. A patient with a weight of 60 and height of 170, has a BMI of 20.76 and is normal weight.

3. A patient with a weight of 80 and height of 170, has a BMI of 27.68 and is overweight.

4. A patient with a weight of 100 and height of 170, has a BMI of 34.6 and is obese.

---
