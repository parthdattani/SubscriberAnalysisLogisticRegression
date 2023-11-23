# Mobile Service Cancellation Predictor

## Overview
This repository contains R code to predict the chances of a user canceling their mobile service based on several factors using logistic regression.


## Installation
Before running the code, you will need to install the following R packages if you haven't already. You can install them using the following commands:

```R
install.packages("tidyverse")
install.packages("corrplot")
install.packages("olsrr")
install.packages("smotefamily")
```

## Usage
- Clone this repository to your local machine.
```
git clone https://github.com/parthdattani/MobilePhoneSubscriberAnalysis-logistic-regression-with-r.git
```

- Set the working directory to the folder where you cloned this repository. You can change this line in the code to match your directory:

```
setwd("C:/working-directory")
```

- Run the script to execute the logistic regression analysis and predictions.

## Code Description
1 The code reads mobile phone subscriber data from a CSV file.
2 It performs exploratory data analysis, including creating histograms and a correlation matrix plot.
3 Class imbalance is addressed using the SMOTE technique.
4 A logistic regression model is generated to predict mobile service cancellations.
5 Model accuracy and confusion matrix metrics are calculated.

## Results
- The script provides predictions for mobile service cancellations and evaluates model performance.

## Questions and Answers
1. Which, if any, of your predictions were incorrect. Explain why this might 
be the case. 
- AvgCallsPerMonth was one of the predictions that were incorrect. We 
originally thought that this would have no significant relation in the 
model but according to the correlation matrix it has a direct impact with 
0.03. Which means, higher number of calls indicate that the customer is 
happy with the network and would not cancel their service. AccountWeeks and 
AvgCallMinsPerMonth is also directly correlated to CancelledServiceTRUE, 
We’re not sure why that must be. 
 
2. Why is DataPlan highly correlated with DataUsage?  
- Users with higher the DataPlan would mean higher the DataUsage. 
 
3. Why is MonthlyBill highly correlated with DataPlan and DataUsage?  
- Usually, higher data plans are priced more than lower data plans which 
means that monthly bill would be higher. Thus, higher DataPlan means their 
DataUsage is more which also means MonthlyBill would be higher.
