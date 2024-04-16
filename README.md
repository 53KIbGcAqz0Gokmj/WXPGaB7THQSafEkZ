53KIbGcAqz0Gokmj

# Happy Customers

## Context:
Logistics and delivery sector.

## Focus:
Providing on-demand delivery services to customers.

## Objective:
Predict whether customers are content or dissatisfied based on their responses to specific questions.

## Data Description:

Attributes X1 to X6 represent answers to various questions.

Response scale: Values range from 1 to 5, where higher values reflect stronger agreement.
Target Variable Y: Represents customer happiness level (0 for unhappy, 1 for happy).

Attributes:
    
    X1: Timely delivery of my order.
    X2: Satisfaction with product quality.
    X3: Fulfillment of all desired items in the order.
    X4: Perceived value for the price paid.
    X5: Satisfaction with the courier service.
    X6: User-friendliness of the ordering app.
    
# Methodology:

## Summary of the dataset

![image](https://github.com/53KIbGcAqz0Gokmj/WXPGaB7THQSafEkZ/assets/143815258/9b4ed329-1e99-4fc8-ab5d-027bb659becf)

* All the numerical variables seem to be right-skewed.
* The mean of the X6 - (the app makes ordering easy for me) and X1 - (my order was delivered on time) was very high and X2 - (contents of my order was as I expected) was the lowest.

## Observation on Target attribute

![image](https://github.com/53KIbGcAqz0Gokmj/WXPGaB7THQSafEkZ/assets/143815258/c5b75d47-678d-49f2-8952-4c3a18eb4160)

## Let's explore how hte different variables correlated with each other.

![image](https://github.com/53KIbGcAqz0Gokmj/WXPGaB7THQSafEkZ/assets/143815258/694a5a97-e38a-4d12-9855-4163cb3e89be)

* X1 - My order delivered on time.
* X5 - I am satisfied with my courier.
* X6 - the app makes ordering easy for me.
* These 3 customer feedback had the highest distributtion of ratings above 3 out of 5.

## Model evaluation criterion

* Addition of New variables

![image](https://github.com/53KIbGcAqz0Gokmj/WXPGaB7THQSafEkZ/assets/143815258/8154bbf2-2912-48e2-9b41-c363aa3f99de)

## Compairing all models

![image](https://github.com/53KIbGcAqz0Gokmj/WXPGaB7THQSafEkZ/assets/143815258/f4028830-f74a-4f67-a6a7-a30bc29edf29)

![image](https://github.com/53KIbGcAqz0Gokmj/WXPGaB7THQSafEkZ/assets/143815258/532f94d3-5bc7-4772-a196-4a5b5bc8c129)

* The Decision Tree and Tuned Decision Tree and Tuned Adaboost Classifier models are giving the best results with an accuracy score of 73%.
  
* The Tuned Adaboost Classifier model has given a good and generalized performance on the training and testing set, we will use it as our final model.
  
## Let's check the important features of the final model.

![image](https://github.com/53KIbGcAqz0Gokmj/WXPGaB7THQSafEkZ/assets/143815258/3c7927d2-5924-40bd-9768-21530334b6c0)

* Looking at the feature importance of the Tuned Adaboost Classifier model, it's evident that top features are 
* X1: my order was delivered on time,
* X3: I ordered everything I wanted to order and
* X5: I am satisfied with my courier  
* These features plays a pivotal role in predictive target variable. These features consistently emerged as a top contributors to the model's accuracy and performance.
