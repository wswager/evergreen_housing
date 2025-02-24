# Evergreen Housing
![pine_tree.jpg](https://github.com/wswager/evergreen_housing/blob/main/images/pine_tree.jpg)
***
# Overview

Analyze data associated with houses sold in King County, Washington between September 9, 2014 and January, 10, 2015 and predict pricing using regression modeling.
***
![King County](https://github.com/wswager/evergreen_housing/blob/main/images/king_county.jpg)
***
# Business Problem

Evergreen Housing is a new house flipping startup looking to establish themselves in the east suburbs of Seattle, Washington.

House flipping is purchasing properties with the intent of selling them with the goal of making a profit.

In order to make a profit, most house flips involve improvements to the home which increase the value.  However, the cost of these improvements must be accounted for, so earning a profit requires selling for more than the amount paid initially plus plus the cost of the improvements.  

The most common improvements will be basic repairs and/or cosmetic renovations, however, for some properties Evergreen Housing may look to make more significant additions to the house via construction.

In order to better assess whether additions which require construction are worthwhile, Evergreen Housing have requested input regarding which features will increase the value of homes and a model predicting pricing. 
***
# Data
## King County House Sales Data

Data associated with houses sold in King County, Washington between September 9, 2014 and January, 10, 2015.
***
# Data Cleaning

## Remove Fields
* Features not associated with the physical features of the home

Examples: Date House Sold, If the House was Viewed Prior to Sale, Average Square Footage of the Surrounding Homes

* Features which cannot be improved through construction

Examples: If the House is on the Waterfront, Basement Square Footage, Zipcode

* Redundant features
***
### Example Field Exploration

### Bathrooms Statistics
**Mean**: 3.37

**Standard Deviation**: 0.92

**Minimum Value**: 1.00

**Lower Quartile**: 3.00

**Median**: 3.00

**Upper Quartile**: 4.00

**Maximum Value**: 33.00

### Bathrooms Scatterplot
![bathrooms1](https://github.com/wswager/evergreen_housing/blob/main/images/ex_bathrooms1.png)

### Bathrooms Joint Plot
![bathrooms2](https://github.com/wswager/evergreen_housing/blob/main/images/ex_bathrooms2.png)
***
## Define and Drop Outliers
* Homes with more than six bedrooms - 0.28% of total data
* Homes with more than four and one half bathrooms - 0.35% of total data
* Homes with square footages greater than 4,000 - 3.21% of total data
***
# Modeling

## Individual Features
Fit Each feature individually v price to a linear regression model to assess fit.
  Conclusion: Drop Year the House was Built due to an R-Squared value of 0.00 and a P-value of 0.10, indicating a poor fit.

## Fit to Multiple Linear Regression Model, Analyze Fit Metrics, Refine Data, and Remodel to Assess Change
### Explore Removal of Additional Fields
Columns based on lack of statistical significance (P-vlaue): Grade, Condition
  Conclusion: Changes discarded due to R-squared and Root Mean Squared Error decreasing, indicating a worsening of fit.

Columns based on excessive correlation (multicollinearity): Floors
  Conclusion: Changes discarded due to R-squared and Root Mean Squared Error decreasing, indicating a worsening of fit.

### Define and Drop Additional Outliers
Define and drop additional outlier: Homes priced higher than $1,000,000.00 - 3.24% of total data
  Conclusion: R-squared decreased 

***
# Final Model
The model indicated an average difference between predictions and actual pricing of $144,369.00.

A Root Mean Squared Error of 144369.39 and R-Squared of 0.47 indicates that while the model does have some predictive ability, there is room for improvement.

![pine_tree.jpg](https://github.com/wswager/evergreen_housing/blob/main/images/model.png)
***
# Conclusions

Evergreen Housing requested input regarding features which require construction (beyond basic repairs and/or cosmetic renovations) will increase the value of homes, as well as a model predicting pricing.

In analyzing the data from the houses sold in King County, Washington between September 9, 2014 and January, 10, 2015, the following features show a statistically significant relationship with increasing price of the home (in order of significance):

* Square Footage of the Home
* Number of Bathrooms
* Number of Bedrooms
***
![King County](https://github.com/wswager/evergreen_housing/blob/main/images/king_county.jpg)
***
## Additional Comments

### Grade
While the grade from King County grading system showed some significance, it was only with higher graded homes; lower grades showed less significance.  
This could indicate that construction improvements are more worthwhile with higher graded homes.
This could also indicate that seeking to improve a home’s ability to perform well with King County’s grading system is worthwhile.
However, more investigation is required before conclusions can be made.

### Condition
The condition feature did not show significance.
While this feature would seem to be similar to the King County grading system, the differing metrics must cause it to have less of a relationship toward price.
This would indicate that in making renovations for a home, the metrics associated with the King County grading system should be prioritized over the metrics for Condition.
***
![pine_tree.jpg](https://github.com/wswager/evergreen_housing/blob/main/images/pine_tree.jpg)
***
# Thank You

### Wes Swager
[Email](mail.westin.swager@lsventures.com)

[GitHub](https://github.com/wswager)

[LinkedIn](linkedin.com/in/wes-swager-36a84a2a)
