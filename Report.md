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
The below table shows the root mean squared error of the three models for the years 2019 and 2020:-
| Model      | RMSE ()2019 | RMSE (2020)  |
| ----------- | ----------- | ----------- |   
| KNN     | 59324.26     |       64277.83       |
| Random Forest   | 58304.54      |   63211.05    |
| Gradient-Boosted Tree   | 59354.69       |      64151.26       |

  
 We can see from the above table that radom forest is performing the best. Furthermore, we can see that for each model, the RMSE of the year 2020 is more than the RMSE of 2019. This indicates that the models fitted on 2017 and 2018 data are not able to explain the incomes of the individuals in 2020, implying that incomes in 2020 has been impacted. To gather further evidence, we used t-test to test whether the mean of difference between actual and predicted values is statistically different for the years 2019 and 2020. We find that the mean of the difference between actual and predicted values for the years 2019 and 2020 is 1223.556 and 4801.022, respectively.  The p-value between them is less than< 2.2e-16 implying that the difference between the two values is statistically different.
 The below figure shows the histogram of log of income for the years 2019 and 2020:-    
 ![](actual_and_predicted_income.png "Figure 1")
  
