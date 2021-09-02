# Food-Demand-Forecasting-Analytics-Vidhya

### Train.csv
id:	Unique ID                                                                                                                                   
week:	Week No                                                                                                                                   
center_id:	Unique ID for fulfillment center                                                                                                                                                                                                                                                                      
meal_id: Unique ID for Meal                                                                                                                                   
checkout_price:	Final price including discount, taxes & delivery charges                                                                                                                                   
base_price:	Base price of the meal                                                                                                                                                                                                                                                                      
emailer_for_promotion:	Emailer sent for promotion of meal                                                                                                                                   
homepage_featured:	Meal featured at homepage                                                                                                                                   
num_orders:	Orders Count

### Fullfillment_center_info.csv

center_id:	Unique ID for fulfillment center (Common in Train.csv)                                                                                             
city_code:	Unique code for city                                                                                                                                                                                  
region_code:  Unique code for region                                                                                                                                                                                                                                                                           
center_type:  Anonymized center type                                                                                                                                                                                  
op_area:  Area of operation (in km^2)

### Meal.csv
meal_id:	Unique ID for the meal (Common in Train.csv)                                                                                                                                                                                        
category:	Type of meal (beverages/snacks/soups….)                                                                                            
cuisine:	Meal cuisine (Indian/Italian/…)

## What is the target Column?

Since the problem statement is to find the demand of the Food supply , num_orders which gives the information orders count will be the target variable because if a particular food item x was order n number of times and food item y ordered 2x number of times we can tell item y has more demand and we nee to predict that demand                                                                  

In addition to the above point the num_order column was not given in test.csv file.😝                                                      
Question) There are some other columns as well that aren't given in test.csv file what about those?
Answer) Probably we can use them for feature engineering purpose(For creating more features)


## What is the Use Case?

The replenishment of raw materials is done only on weekly basis and since the raw material is perishable, the procurement planning is of utmost importance.  


Predicting the Demand helps in reducing the wastage of raw materials which would result in the reduced cost of operation. Increased customer satisfaction by timely fulfilling their expectations and requirements.

## Data Preprocessing

1) Importing the data
2) Merging the data
3) Checking for Null values
4) Checking Categorical data types and Numercal data Types

## EDA 

### Univariate Analysis
1) Count Plots of the categorical variables to know the ditribution of data. If the data was not normaly distributed we convert the data into log normal ditribution.

2) Boxplots of the numerical variables to know the outliers.

### Bivriate analysis
1) Barplot center_type vs num_order gives the information of sale at each type of center
2) week vs num_order gives the week wise sales of food items
3) barplot category vs num_order gives the information of highly sold category
4) week vs emailer_of_promotion gives information of week wise promotions so that we can compare the promostion vs sales 
5) check_out_price vs num_orders gives the information of whether the low cost item was selling more or not 
6) region vs num_orders gives the information of the region wise sales

-- I have used Auto EDA library "AutoViz" for vizulaizong the missed realtions and understanding the data more clearly.

## Feature Engineering 

-- Created the additional required features on which num_orders depend.

1) discount
2) discount percent
3) year
4) Quarter 

-- Encoded all the features using dummies

## Feature Selection 

-- Three Feature slection methods were used
### 1) Filter methods 
a) Correlation: Highly correlated independent features will be removed 
b) Anova Test: Gives top 40 features 
c) PCA : principal component analysis 
### 2) Wrapper Methods
a) Forward Feature Selection method
b) Sequential Feature Selection method
c) Recursive Feature Elimination method
d) Exhaustive feature Selection
### 3) Embedded Methods
a) Lasso Regression for feature seleciton
b) Ridge Regression for feature felection

## Models 
1) Linear Models 
2) Tree Algorithms 
3) Boosting algorithms 
4) Artificial Neural Networks
5) H2O Auto ML
6) Eval ML





















