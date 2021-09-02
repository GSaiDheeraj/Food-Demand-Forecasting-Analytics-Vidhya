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

