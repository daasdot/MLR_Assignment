# Bike Sharing System
> A bike-sharing system is a service in which bikes are made available for shared use to individuals on a short term basis for a price or free. Many bike share systems allow people to borrow a bike from a "dock" which is usually computer-controlled wherein the user enters the payment information, and the system unlocks it. This bike can then be returned to another dock belonging to the same system. The problem state here is to identify the variables which would have a impact whether positive or negative on the Demand.
> The company wants to know:

- Which variables are significant in predicting the demand for shared bikes.

- How well those variables describe the bike demands


## Table of Contents
* [General Info](#general-information)
* [Technologies Used](#technologies-used)
* [Conclusions](#conclusions)
* [Acknowledgements](#acknowledgements)

<!-- You can include any other section that is pertinent to your problem -->

## General Information
> The aim here is to model the demand for shared bikes with the available independent variables. It will be used by the management to understand how exactly the demands vary with different features. They can accordingly manipulate the business strategy to meet the demand levels and meet the customer's expectations. Further, the model will be a good way for management to understand the demand dynamics of a new market. 
> This is a classic case of Linear Regression , Linear regression is a statistical method used to model the relationship between a dependent variable (often denoted as y) and one or more independent variables (often denoted as X). It assumes a linear relationship between the independent variables and the dependent variable. The goal of linear regression is to find the best-fitting straight line that describes the relationship between the variables
> As we are dealing with two or more independent variable , it falls under the multiple linear regression.
<!-- You don't have to answer all the questions - just the ones relevant to your project. -->

> Multiple Linear Regression
 > It follows the following steps to draw conclusion
    - Reading , understanding and visualizing data
    - Preparing the data for modeling(train-test split , rescaling)
    - Training the model
    - Residual analysis
    - Predication and evaluation on the test set
## Observation
 - Reading , understanding and visualizing data   
    - Categorical Variable
     - Season , mnth(month), weathersit , holiday , weekday and working day are categorical variables in the data set.
     - Fall season the number of bike booking is more by looking at the distribution. Summer and Winter also has significant amount of booking. This can 
     be a good predictor. Booking are happening with a median of more than 5000 for summer and fall.
     - Month can be a good predictor as each month has a significant amount of booking.May , Jun , July ,Aug , Sept bookings are happening with a median 
     of more than 4000 .
     - Clear weather sit has more visitor due to which the bike hiring is happening with a median of more than 4000.
     - Thunderstorm does not attract the bikers so it has very less booking compared to others
    - Numerical Variables
     - CNT , atemp and temp has some sort of positive correlation
 - Preparing the data for modeling(train-test split , rescaling)
    - During this step dummy variables are created from categorical variable.
    - Recaling performed using MinMaxScaler
  - Training Model
    - Calculate P score and VIF
    - Look at the significance of variables by looking at the p value
    - Variables got dropped based on the following rule
      - HIGH vif LOW P - Drop
      - HIGH vif LOW P - Remove these after all others
      - LOW vif HIGH P - Drop , remodel the setup and check the VIF
      - LOW vif LOW P - Accept
  - Residual Analysis of the train data
    - Error terms are normally distributed as per the LR assumption
    - Error terms are independent of each other 
    - Error terms have constant variance (homoscedasticity)
  - Prediction and Evaluation on Test sets
    -  evaluate rsquare for test data
    -  compare with rsquare for train data
   
## Conclusions
> Major Predictor
- yr(Year)
    - Coefficient : 2029.34
    - Increase in year increase bike hiring by 2029.34
- temp(Temperature):
    - Coefficient : 4265.03
    - Increase in temp increase bike hiring by 4265.03
- windspeed
    - Coefficient : -1285.15
    - Increase in temp decreases bike hiring by  -1285.15
    

> The equation for Best Fitted Line
- CNT = 1812.85 + 2029.34 * yr +4265.03 * temp - 914.41 * holiday - 1285.15 * windspeed - 569.51 * Spring + 413.18 * Summer - 737.14 * Winter - 427.95 * July + 660.70 * September - 420.22 *Sunday -714.46 * Cloudy_mist - 2516.27 * Light_Rain_Thunder


<!-- You don't have to answer all the questions - just the ones relevant to your project. -->


## Technologies Used
- Python: version 3.x
- Pandas: version 1.3.4
- Seaborn: version 0.12.2
- Matplotlib: version 3.5.3
- Plotly: version 5.9.0
- sklearn version 1.5.0
- statsmodels 0.14.1

<!-- As the libraries versions keep on changing, it is recommended to mention the version of library used in this project -->

## Acknowledgements
Give credit here.
- This project was inspired by the need to predict the variables affecting the bike sharing stats.


## Contact
Created by Dibya Ranjan Sethi - feel free to contact me!
