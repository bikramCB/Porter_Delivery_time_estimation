# Porter_Delivery_time_estimation
Prediction of order delivery time using Neural Network

## Problem Statement:
Porter is India's Largest Marketplace for Intra-City Logistics. Leader in the country's $40 billion intra-city logistics market, Porter strives to improve the lives of 1,50,000+ driver-partners by providing them with consistent earning & independence. Currently, the company has serviced 5+ million customers

Porter works with various restaurants to deliver their items directly to the people.

Porter has several delivery partners available for delivering the food, from various restaurants and wants to get an estimated delivery time that it can provide the customers based on what they are ordering, from where, and also the delivery partners.

This dataset has the required data to train a regression model that will do the delivery time estimation, based on all those features

## Data Dict:
Each row in this file corresponds to one unique delivery. Each column corresponds to a feature as explained below.

market_id: integer id for the market where the restaurant lies
created_at: the timestamp at which the order was placed
actual_delivery_time: the timestamp when the order was delivered
store_primary_category: category for the restaurant
order_protocol : integer code value for order protocol(how the order was placed ie: through porter, call to restaurant, pre-booked, third party etc)
total_items subtotal: the final price of the order
num_distinct_items: the number of distinct items in the order
min_item_price: the price of the cheapest item in the order
max_item_price: the price of the costliest item in order
total_onshift_partners: number of delivery partners on duty at the time the order was placed
total_busy_partners: number of delivery partners attending to other tasks
total_outstanding_orders: total number of orders to be fulfilled at the moment

## Tech Used:
1. Neural Networks
2. Random Forest

## Tools Used
1. Scikit Learn, Tensorflow, Keras, Matplotlib, Seaborn, Pandas, Numpy

## Solutions:

1. Alomost 2lakh Data was collected with the help of data engineer from Porter's backend and the frontend.
2. Create target feature time taken mins into datasets.
3. Extract Hour, the day of the week when the order was placed.
4. remove outlier 831 data points using LOF because don't know maybe one outlier is important for other features or not. so confirm it by using the LOF technique.
5. Business related insight:
  weekends(Sat, Sun) a little bit large no of orders and night between 1 and 3 bigger orders. And so it takes longer time between 1 & 3 am to fulfill orders. So we 
  might engage more delivery partners in between these times.
6. Applied Random forest with MAPE score of 2.77 and also got the importance of essential features related to the food delivery business.
7. Applied Neural Network with 3 hidden layers and neurons(hyperparameter tuning) and received MAPE score of 0.009.

8. Let's say out of 2000 responses who are asked to rate this service out of 0-10 scale rate :

1800 respondents gave a score of 9-10 (Promoters)
80 respondents gave a score of 7-8 (Passives)
120 respondents gave a score of 0-6 (Detractors)
Percentage of Promoters = (1800 / 2000) * 100 = 90%
Percentage of Passives = (80 / 2000) * 100 = 4%
Percentage of Detractors = (120 / 2000) * 100 = 6%

NPS = Percentage of Promoters - Percentage of Detractors
NPS = 90% - 6% = 84%

## Business Impact :

So we can increase the net promoter score by almost 84% by collecting feedback from customers. SO this model is amazing.





