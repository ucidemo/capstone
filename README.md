# What drives the price of a car.

I will analyse the car data set and provide a recommendations to the dealer on what are attributes
are important and consumer value in a used car.

## Business Understanding
The busiess task is to identify which are the factors consumer is interested in buying( attributes 
makes the price expensive or cheaper)
This will help seller to focus on key attributes that consumer is interested in buying a car

## Data Understanding

Dataset (vehicle.csv) consists of 18 features and 426880 rows. 

below features has  numerical values
    price - Target Value
    year  - vehicle year ( Ranging from 1931 to 2018)
    odometer - odometer reading
    region - cities or region where car is sold
    manufacturer - vehicle manufacurer ( make )
    model - model of car 
    condition - ( new /like new/fair/good/excellent etc)
    cylinders - cylinders of car ( ranging from 4 to 12)
    fuel  - gas/hybrid/diesel/electric and also noticed other is also present
    title_status - whether parts are missing/lien or clean or salvgage etc. we will find out whether this is important
                   feature or not that customer is interested
    VIN  - vin number - this should not be key attribute determining price. this can be dropped
    drive - whether 4 wheel drive etc.
    size - full size or compact or mid-size
    paint_color - color of car. this could be interesting and important feature that consumer is interested in
    state -  vehicle state - price might vary based on vehicle state


## Data Preparation

All the attibutes except price/region/state contains Nan Values.
data cleaning has to be done prior to modelling


## Modeling

I have used three regression models and validation method

   Ridge Regression to find coefficients
   SequentualFeature Selection
   Lasso

## Evaluation
I have listed out the ranking of regression modes by comparing metrics and also plot a graph
with mean sequarred error

Based on MSE and R^2 score of different regression model and Cross validation technique indicated
lowest MSE and Highest R^2 score are Ridge Regression mdel. It looked more reasonable. So 
Ridge Regression model were choosen as recommended model.

## Recommendations to the car dealership

1. Total rows in data set were 426880 and target column was price
2. Data Clean up is done as there were lots of Nan values
3. Outliers were removed
4. Categorical features were applied since there are categorical features in dataset
5. Visualization of key features were included above
6. Ran with three regression model
    Ridge Regression
    Sequential/Regression
    Lasso
    It is observed Ridge regression model performed as top model in this datset with MSE 0.212 and R^2 0.82

7. Three most important feature customer value in cars are gas,diesel and automatic
