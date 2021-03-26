# Evergreen Housing
![pine_tree.jpg](https://github.com/wswager/evergreen_housing/blob/main/images/pine_tree.jpg)

# Overview

Analyze data associated with houses sold in King County, Washington between September 9, 2014 and January, 10, 2015 and predict pricing using regression modeling.
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

### Fields
* **id** - Unique identification number for each house
* **dateDate** - Date sold
* **pricePrice** -  Price sold for
* **bedroomsNumber** -  Number of bedrooms
* **bathroomsNumber** -  Number of bathrooms
* **sqft_livingsquare** -  Square footage of house
* **sqft_lotsquare** -  Square footage of lot
* **floorsTotal** -  Number of floors
* **waterfront** - If house has a view to a waterfront
* **view** - If house was viewed
* **condition** - Rating of overall house condition, one-through-five
* **grade** - Grade from King County grading system, one-through-thirteen
* **sqft_above** - Square of house above groun-level, not including basement
* **sqft_basement** - Square footage of basement
* **yr_built** - Year built
* **yr_renovated** - Most recent year renovated
* **zipcode** - Zipcode
* **lat** - Latitude coordinate
* **long** - Longitude coordinate
* **sqft_living15** - Average square footage of house for nearest fifteen neighbors
* **sqft_lot15** - Average square footage of lot for nearest fifteen neighbors
***
# Data Cleaning
## Remove Fields
* Remove features not associated with the physical features of the home: 'id', 'date', 'view', 'sqft_living15', and 'sqft_lot15'
* Remove features which cannot be improved through construction: 'waterfront', 'sqft_basement', 'zipcode', 'lat', and 'long'
* Remove redundent features: 'sqft_above', in context, is the same as 'sqft_living'

## Define and Drop Outliers
* Bedrooms > 6 (0.28% of total data)
* Bathrooms > 4.5 (0.35% of total data)
* Square Footage of the Home > 4,000 (3.21% of total data)
***
# Model and Refine Data
## Remove Additional Fields
* Remove additional columns based on p-values: Condition, Grade, and Year Built
* Remove additional columns based on multicollinearity: Floors
* Define and drop additional outliers based on QQplot, homoscedasticity, and five-point statistics
***
# Conclusions

Evergreen Housing requested input regarding features which require construction (beyond basic repairs and/or cosmetic renovations) will increase the value of homes, as well as a model predicting pricing.

In analyzing the data from the houses sold in King County, Washington between September 9, 2014 and January, 10, 2015, the following features show a relationship with increased price (in order of significance):

* Square Footage of the Home
* Number of Bathrooms
* Number of Bedrooms

The recommendation would be, if a house being flipped is being considered for signification additions via construction, that increasing these features.

Surprisingly, it was found that while the grade from King County grading system showed some significance in its relationship with price, that was only the case of higher graded homes, and lower grades showed a less significant relationship.  Also, the condition of the home did not show a significant relationship with the price.
