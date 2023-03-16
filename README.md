

# Flight Research and Analytics Group

**Authors: Annie Chan, Azucena Faus, Mohammad Mahmoudighaznavi**

**Company Industry: Air Transportation**

**Company Size: 3 (startup)**

**[GitHub Repository](https://github.com/fausa/Flight_Analytics)**


## Abstract:
The airline industry plays an important and critical role in the world’s transportation sector. Various factors such as weather conditions, air traffic control, airport operations, etc., have the capability to directly and indirectly affect airline services, leading to delayed and canceled flights. Understanding the effects of such issues in advance can prepare customers and airline operators for potential reasons for flight cancellations.

## Problem Statement:
Although travelers know the propensity for canceled flights during the winter months due to weather, it is difficult to know when that likelihood is highest and what flight to schedule if travel is nonetheless required. Customer dissatisfaction is not only painful for the customer, but the airlines, airport flow, and other customers. Having some indication that a flight might be canceled and then knowing what airline to go with if there is a high likelihood of cancellation would be useful to set realistic expectations and hopefully increase customer satisfaction.

## Goals:
The success of this project will contribute to the achievement of the following goals:

1. Combining weather and flight data to find connections and correlations between extreme weather conditions and canceled flights.

2. Training a model to predict cancellations on the flight dataset with weather condition data and predict whether a flight has a high probability of being canceled based on the weather for that date/time. We would like to attain an accuracy/F1 score/Sensitivity of: 0.8, 0.8, and 0.7, respectively.

3. Providing recommendations to airlines on customer service plans that should be offered to customers in the event of a flight cancellation.

Ultimately, the goal of this project is to provide customers with information regarding the likelihood of canceled flights due to weather, along with suggestions for which airlines would be best to go with, in case the likelihood is high. The airline recommendations would stem from customer satisfaction when they experienced canceled flights with those airlines, and the services they not only offer, but actually follow through with. This will not only help customers planning out their future trips in case of uncontrollable circumstances, but also improve the reputation of multiple airline companies.

## Non-Goals:
We are not looking to forecast weather - yet. Only if we can adequately predict canceled flights based on weather conditions. Once this concept is proven, a weather forecasting model can be used in conjunction with the canceled flights predictive model. We are also not trying to predict airline performance - just adding what is already known about customer satisfaction with specific airlines to provide an added benefit to the customer when the likelihood of a canceled flight is high. Finally, another non-goal is we are not interested in delving into predicting delayed flights, or flights that come from airports that do not have any weather data in our source datasets yet either. 

## Data Sources:
* Airline relational database
* Weather dataset (CSV)
* Airline Customer Satisfaction for Canceled Flights (CSV)

One of the data sources comes from a relational database called Airline that contains US domestic flight information for January of 2016, along with information regarding canceled flights and whether those cancellations were due to weather. The second dataset was collected from Kaggle, which contains weather data for US airports for the years 2016-2021. This way, departure airport weather conditions can be added features for those flights that experienced cancellations due to weather. The final dataset contains customer review data for US airlines when flights were canceled. 

Some risks with the data are that it is only for one month, so any predictions would have to be for the following year, in the same month as weather conditions are seasonal. More data would have to be collected to further prove this concept. 

The source data will be stored in an S3 bucket and will get there by way of SQL extraction of the necessary tables, and loading the comma-delimited files for weather and customer service.



