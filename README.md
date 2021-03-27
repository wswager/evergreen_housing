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
- Examples: Date House Sold, If the House was Viewed Prior to Sale, Average Square Footage of the Surrounding Homes
* Features which cannot be improved through construction
- Examples: If the House is on the Waterfront, Basement Square Footage, Zipcode
* Redundant features
***
### Example Field Exploration
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
# Fit to Model and Refine Data
## Remove Additional Fields
* Remove additional columns based on lack of statistical significance (P-vlaue)
- Example: Grade, Condition
* Remove additional columns based on excessive correlation (multicollinearity)
- Floors
## Define and Drop Additional Outliers
* Define and drop additional outliers identified after modeling disrupting the model accuracy
- Homes priced higher than $1,000,000.00 - 3.24% of total data
***
# Final Model

***
# Conclusions

Evergreen Housing requested input regarding features which require construction (beyond basic repairs and/or cosmetic renovations) will increase the value of homes, as well as a model predicting pricing.

In analyzing the data from the houses sold in King County, Washington between September 9, 2014 and January, 10, 2015, the following features show a statistically significant relationship with increasing price of the home (in order of significance):
* Square Footage of the Home
* Number of Bathrooms
* Number of Bedrooms

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
# Thank You

### Wes Swager
[Email](mail.westin.swager@lsventures.com)

[GitHub](https://github.com/wswager)

[LinkedIn](linkedin.com/in/wes-swager-36a84a2a)
