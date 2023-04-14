# Project 2 - Ames Housing Data and Kaggle Challenge



## Problem Statement
Recently, the Ames Real Estate Company has made rapid advances in marketing and property acquisition. To help better support their agents, this project is aimed at creating a linear regression model that can better predict property values based on certain attributes. From this, there will be an increase in the profits for the stakeholders of the company, and increase in customer satisfaction and company credibility.

## Data Dictionary
|Feature|Type|Description|
|---|---|---|
|SalePrice|float|The value of a property, and our target variable.| 
|Total_sqft|float|The total square footage of a property.| 
|Electrical|object|The type of electrical utility on the property.| 
|Central Air|object|Does the property have central air conditioning.|
|Lot Area|float|Total area of the lot size, in square feet.|
|Mas Vnr Area|float|Total area of masonry veneer area, in square feet.|


## Preliminary Findings from EDA
Preliminarily, from the insights we've garnered during this EDA, we cannot say for certain which variables are likely to influence the relative price of any property. We can only say that there are a lot of variables at play, and the degree of which it may play a role in predictive value of a house is yet to be seen. Likely, through our modeling process we will develop a certainty for which qualities are the most important in the determination of its valuation



## Conclusion and Modeling Process

*Out of the 3 models, regular, ridge, and lasso, the Ridge method seemed to perform the best. The RMSE and R2 scores of the Lasso and initial model are about the same, but not as good as the Ridge model. In general, our model performed better than the baseline model, but is not anywhere near the perfect model that we are striving for. Our test_score is not very close to our train_score which suggests that our model is vastly overfit and does not generalize well to new data. Therefore, until we improve upon these aspects, we cannot expect a good prediction for any given input for this model.*

From our modeling process, we found that the best predictors for price are the total sq-ft and garage size / features. Surprisingly, features such as the age of the home and amenities like the fireplace and quality of finishes did not play a large role. This suggests that some of the most valuable things for a prospective buyer is the functionality of the house rather than the aesthetic factor or comfort level.