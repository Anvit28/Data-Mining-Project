## Abstract
# Introduction
# Methods
We use information from the Current Population survey (CPS) from 2017-2020. Our outcome variable is individual's total pre-tax personal income or losses. The set of features that we used to fit our models is:   
* Age   
* Sex – whether a person is male/female 
* Marital status 
* Relationship to household head – we encoded initially categorical variable as dummy variable whether a person is head of a household or not 
* Race 
* State 
* Number of children in the family 
* Citizenship status 
* Employment status - we encoded initially categorical variable as dummy variable whether a person is working or not 
* Occupation 
* Hours usually worked per week 
* Educational attainment recode 
* Self-reported health 
  
We restrict our dataset to individuals older 20 years old. Additionally, we exclude individuals whose hours usually worked per week vary. 
  
We use three different regression models to predict individual income: K-nearest-neighbors (KNN), random forest and gradient-boosted tree. In order to fit the model, we use data for the years 2017-2018. We have used cross-validation in conjunction with hyperparameter tuning to fit the models. The test set comprises of the data points from the year 2019. We have used root mean squared error as the evaluation metric. 
Additionally, we have also tested the performance of our models for the year 2020. For the model that best fits the data, we have used t-test to test whether the mean of difference between actual and predicted values is statistically different for the years 2019 and 2020. This is done to check whether the impact of covid on an individual's income was statistically significant.   
## Results

| Syntax      | Description |
| ----------- | ----------- |
| Header      | Title       |
| Paragraph   | Text        |
Table: Table 1
