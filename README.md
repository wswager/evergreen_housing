# Evergreen Housing
![pine_tree.jpg](https://github.com/wswager/evergreen_housing/blob/main/images/pine_tree.jpg)
***
# Overview

Analyze data associated with houses sold in King County, Washington between September 9, 2014 and January, 10, 2015 and predict pricing using regression modeling.
***
![King County]()
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
** Examples: Date House Sold, If the House was Viewed Prior to Sale, Average Square Footage of the Surrounding Homes
* Features which cannot be improved through construction
** Examples: If the House is on the Waterfront, Basement Square Footage, Zipcode
* Redundant features

Define and Drop Outliers
* Homes with more than six bedrooms - 0.28% of total data
* Homes with more than four and one half bathrooms - 0.35% of total data
* Homes with square footages greater than 4,000 - 3.21% of total data
***
### Example
### Bathrooms Scatterplot
![bathrooms1](https://github.com/wswager/evergreen_housing/blob/main/images/bathrooms1.png)

### Bathrooms Joint Plot
![bathrooms2](https://github.com/wswager/evergreen_housing/blob/main/images/bathrooms2.png)

### Bathrooms QQplot
![bathrooms3](https://github.com/wswager/evergreen_housing/blob/main/images/bathrooms3.png)
***
## Define and Drop Outliers
* Bedrooms > 6 (0.28% of total data)
* Bathrooms > 4.5 (0.35% of total data)
* Square Footage of the Home > 4,000 (3.21% of total data)
***
# Model and Refine Data
## Remove Additional Fields
* Remove additional columns based on p-values: Condition, Grade, and Year Built
* Remove additional columns based on multicollinearity: Floors
## Define and Drop Additional Outliers
* Define and drop additional outliers based on QQplot, homoscedasticity, and five-point statistics
***
# Final Model
![model4.png](https://github.com/wswager/evergreen_housing/blob/main/images/model4.png)
***
# Conclusions

Evergreen Housing requested input regarding features which require construction (beyond basic repairs and/or cosmetic renovations) will increase the value of homes, as well as a model predicting pricing.

In analyzing the data from the houses sold in King County, Washington between September 9, 2014 and January, 10, 2015, the following features show a relationship with increased price (in order of significance):

* Square Footage of the Home
* Number of Bathrooms
* Number of Bedrooms

The recommendation would be, if a house being flipped is being considered for significant additions via construction, that increasing these features.

Surprisingly, it was found that while the grade from King County grading system showed some significance in its relationship with price, that was only the case of higher graded homes, and lower grades showed a less significant relationship.  Also, the condition of the home did not show a significant relationship with the price.
***
### Wes Swager
[Email](mail.westin.swager@lsventures.com)

[GitHub](https://github.com/wswager)

[LinkedIn](linkedin.com/in/wes-swager-36a84a2a)
