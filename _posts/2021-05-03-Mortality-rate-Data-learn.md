---
layout: post
title: Has Mortality rate gone down?
subtitle: What are some major factors that affect mortality rate, And will it decrease in the future?
tags: python, other
---

  The life expectancy is something that is very important to many of us. We work a lot and want more time. 
The main study was to see if life expectancy has been improving over time. 
The year have been split into training sets and then into test sets.

The main objective was to see as well if there was any correlation between the life expectancy and any other value from the data set,
that and if life expectancy or increased average lifepsans will increase more in later years.

Some of the first things done was to clear the data of any NaN values and other values that werent important / numeric. The data equivalated to something along these lines:

![sleep data dataframe](https://user-images.githubusercontent.com/48320567/123538576-aa7b1980-d703-11eb-9980-059a53b56521.PNG)
![newdata](https://user-images.githubusercontent.com/48320567/123538579-aea73700-d703-11eb-9a3a-daa9a84ad14d.PNG)

The next step was to break the different frame data between train and test.

---
mask = 2012

train_mask = (df_cut['Year'] < mask)
val_mask = (df_cut['Year'] >= mask)
test_mask = (df_cut['Year'] >= mask)
---

Next is to find a baseline accuracy

y_pred = [y_train.mean()] * len(y_train)
baseline_acc = mean_absolute_error(y_train, y_pred)

Baseline: 8.52

The pipeline for the dataset was tne next step to learn about the concentrated values of life averages.

model that was trained,  [59.69014243 59.17177372 58.34753025 58.36933264 57.88726633 56.89612443
 56.42846493 54.28960948 54.89476363 61.21170059 54.87421517 54.41469306
 75.22281586 75.3839934  74.47694608 74.82149671 74.33004798 74.48837062
 74.25878487 73.80378768 73.71849869 75.21137769 75.04031894 74.19658372]
 
 model test,  [61.21216113 60.4922542  60.77322852 60.01671952 75.70164977 75.48962933
 59.01139719 58.94855907 57.22816538 75.4176697  76.41961523 76.39393728
 74.85509968 85.28384944 84.90634606 84.7997012  74.63432722 69.10507547
 70.6107721  68.0308172  61.68894719 61.27328816 58.42254568 70.55302832
 71.10553038 73.74398474 74.28117105 71.460776   70.94576687 73.39545989]
 
 A few steps were taken to make charts of the correlation between values that were in the first data frame.
 
 ![scgool](https://user-images.githubusercontent.com/48320567/123539480-ffb92a00-d707-11eb-87a0-1b4f2383f41d.PNG)
![GDP](https://user-images.githubusercontent.com/48320567/123539481-0051c080-d708-11eb-93ca-b6d8553b7342.PNG)
![year](https://user-images.githubusercontent.com/48320567/123539482-0051c080-d708-11eb-8f2d-129af502f3a3.PNG)

The most relevant correlations seem to be School and Year, wher ethe life expectency seems to rise with the better schooling and life expectancy, oddly enough seems to be going down when the years are getting later.

The box plots now work to make sense of the increase in the average.

the first is the train plot to train the data set to recognize patterns before the year of 2012.
![boxplot](https://user-images.githubusercontent.com/48320567/123539912-1d878e80-d70a-11eb-993a-5a566933a37d.PNG)

the Test is the next one to test the data set for the life expectancy after the year of 2012.
![bocplot2](https://user-images.githubusercontent.com/48320567/123539914-22e4d900-d70a-11eb-822f-e05e72454009.PNG)

Testing now the new baseline accuracy
model = [y_test.mean()] * len(y_test)
baseline_acc2 = mean_absolute_error(y_test, model)
baseline_acc2 = 9.05

By the marginal increase, there is a clear increase in the base accuracy.
This means that there is an increase in the values over the years, with later years having an effect on the lives of others. 
The issue is tht the value isnt high enough to be significant, only increasing by 1 where it would need to be around 5 or so to have any significance.

---
In conclusion
---

There simply isnt enough of an increase in a simple descision tree pipeline to prove any increase in life expectency in later years.
