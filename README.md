# Project 2 - Ames Housing Data and Kaggle Challenge



## Problem Statement
Recently, the Ames Real Estate Company has made rapid advances in marketing and property acquisition. To help better support their agents, this project is aimed at creating a linear regression model that can better predict property values based on certain attributes. In preparation for building my model, I will be using correlation analysis to identify all features that are highly correlated with our target variable of Sale Price. Additionally, I will be using regularization techniques such as Ridge and Lasso to reduce the impact of irrelevant features. I will be using Mean Squared Error and R2 score to evaluate the model's performance compared to baseline. From this, there will be an increase in the profits for the stakeholders of the company, and increase in customer satisfaction and company credibility.

## Data Dictionary
|Feature|Type|Description|
|---|---|---|
|SalePrice|float|The value of a property, and our target variable.| 
|Total_sqft|float|The total square footage of a property.| 
|OverallQual|float|Overall material and finish quality on the property.| 
|Gr Liv Area|float|Above grade (ground) living area square feet.|
|YearBuilt|float|Original construction date of property.|
|Garage Area|float|Size of garage in square feet.|
|Total Bsmt SF|float|Total square feet of basement area.|
|1st Flr SF|float|Total square feet of first floor.|

## Visualizations from EDA

![Correlation of Features](./imgs/correlation_final.png)

![Pairplot of Features](./imgs/pairplot.png)

## Initial Conclusions from EDA

Preliminarily, from the insights we've garnered during this EDA, we have seen that variables such as Overall Qual, Gr Liv Area, Garage Area, Total Bsmt SF, 1st Flr SF, and Year Built are likely to influence the relative price of any property. 

The degree of which they may play a role in predictive value of a house is yet to be seen. Likely, through our modeling process, we will develop a certainty for which qualities are the most important in the determination of its valuation.

# Modelling Analysis
![predicted_v_actual](./imgs/predicted_v_actual_scatter.png)
![residuals_hist](./imgs/residuals_hist.png)
![residuals_scatter](./imgs/residuals_scatter.png)


## Conclusion and Recommendations
In this project, we used EDA to find the key features that are highly correlated with our target value, the price of homes. 

By building linear regression models based on those key features as well as engineered features, we were able to train a model that best predicted our target data.

Out of the 3 candidate models: regular, ridge, and lasso, the Lasso model seemed to perform the best. It improves slightly over our initial model, and correctly predicted 81.44% of housing sale prices with an error of \\$33746, which is considerably better than our baseline error of \\$78,375.

From our model, we found that Overall Quality, Total Square Footage, and Housing Age are some key factors that determine the value of a house.

Our model performed better than the baseline model, but is not anywhere near the perfect model that we are striving for. 

Our Test R2 is higher than the Train R2, suggesting that the the model is slightly overfit, and does not generalize as well to new data.

**Recommendations for Future Exploration**

We can use variance inflation factor to help feature select some of the dummified columns to include into our data. This will make selecting categorically encoded features less of a guess and check.

To help better analyze our data, we should include more data points that are more normalized to the dataset, because of our bias due to the outliers of many higher priced homes.