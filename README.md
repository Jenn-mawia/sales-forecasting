# Walmart Sales forecasting

## Contributors
Jenipher Mawia

## Description
This is a brief analysis that was done on Walmart's sales data with the task of predicting the department-wide sales for each store. 

In addition, Walmart runs several promotional markdown events throughout the year. These markdowns precede prominent holidays, the four largest of which are the Super Bowl, Labor Day, Thanksgiving, and Christmas. The weeks including these holidays are weighted five times higher in the evaluation than non-holiday weeks. Part of the challenge presented is modeling the effects of markdowns on these holiday weeks in the absence of complete/ideal historical data. A point to note is that **not all holidays are captured** in the data. 

## Findings/Results

There are 45 stores and 3 types of stores A, B, C in which Type 'A' are relatively huge stores, type 'B' are medium-sized stores while type 'C' are smaller stores.

#### Weekly Sales Analysis throughout the period

<img width="1038" alt="Screenshot 2023-03-06 at 16 46 10" src="https://user-images.githubusercontent.com/64205510/223128280-acaeb5f0-20e9-4caa-9d74-c8a6080f8cfb.png">
From the image above, there are significant peaks and dips throughout the period.

- The peaks are seen towards the end of each year suggesting increased purchases during Thanksgiving and Christmas holiday. We do not have data for the whole of 2012 and hence there are no significant peaks during this time.

#### Sales per holiday per year

Feature Engineering was done to extract the date features such as Month, Year, Week Number so that it is easier to analyse the data. A few more holidays such as **President's day, Easter Holiday, Independence day, Columbus day, New Years etc** not included were added. 

<img width="785" alt="Screenshot 2023-03-06 at 16 56 40" src="https://user-images.githubusercontent.com/64205510/223130255-aa10f273-4277-4ad7-8731-56052de19be5.png">
From the image above, the highest sales were recorded during Thanksgiving. 2012 data is not complete and hence there is no data for holidays such as Thanksgiving and Christmas during this period. 

#### Modelling 

Label Encoding was done to the categorical features and features with higher correlation with each other were removed. This is important for **Linear Regression** as it does not work well with correlated features. The Linear Model performed very **poorly** with a **high RMSE(21818)** value and a very **low R^2(0.06997)** value. 

The **Random Forest Regressor** performed really well with a **lower RMSE(3867)** but exhibited signs of overfitting as the **R^2(0.97)** was really high. 

**The RMSE(7563)** for the **LightGBM Regressor model** is slightly higher than the random forest model but lower than the linear regression model. It basically performs better than the linear regression model with **R^2 OF 0.89** but the random forest model exhibits signs of overfitting.

## TO DO
- Perform regression modelling with XGBOOST and compare the performance results with the other models.
- Perform hyper parameter tuning to improve model performance.
- Compare the feature importances for each model and select the best model based on the most important features. 

## Complete Setup / Installation Requirements
To open and view the notebook, you will need Jupyter Notebooks or Google Colaboratory. Do have a look at it.😊

## Technologies used
Used Python 3 in this project

## Contributing / Bug / Feature Request
Pull requests are welcome for contribution. For major changes, please open an issue first to discuss what you would like to change.
