# Poverty Logistic Regression Model
## Objective
In this project, a logistic regression model was made with the following steps:
1. Data Preparation
2. Logistic Regression Model Buidling
3. Model Evaluation

## Technology
Language: Python

## Dataset used
Provided by FTW Foundation which was derived from this [Kaggle](https://www.kaggle.com/code/johnnyyiu/poverty-prediction-from-visualization-to-stacking) source. 

## Step 1. Data Preparation

Overview of the dataset

![image](https://github.com/ysasamson/PovertyPredictorModel/assets/145044637/136ddb6a-5ef4-4c92-991e-458e191bdedc)

Checked which columns have null values

![image](https://github.com/ysasamson/PovertyPredictorModel/assets/145044637/563f9909-c550-4ca3-a558-f19cea69f327)

'bank_interest_rate' column dropped as 98% of rows are null

![image](https://github.com/ysasamson/PovertyPredictorModel/assets/145044637/4effaf49-2d66-4875-b4ea-45468dc9fc21)

Null education_level values were imputed with mode

![image](https://github.com/ysasamson/PovertyPredictorModel/assets/145044637/6005f281-b5fa-4975-8ed7-2ab3e5bc04cf)

New column 'poverty_status' was made based on 'poverty_probability' column

![image](https://github.com/ysasamson/PovertyPredictorModel/assets/145044637/accc7d84-8f7a-4e71-b7a0-3d5185603106)

Bool values were changed to 0/1 for usage in the model

![image](https://github.com/ysasamson/PovertyPredictorModel/assets/145044637/e7bb2b6d-ad00-4a98-a259-8a831a875e7d)


## Step 2. Model Building

Features were analyzed using correlation heatmap

![image](https://github.com/ysasamson/PovertyPredictorModel/assets/145044637/5b89d3de-5ea6-4087-be11-a3adc6a90e64)

![image](https://github.com/ysasamson/PovertyPredictorModel/assets/145044637/aea0a36e-26cb-4935-bbca-321eb31573d2)

## Step 3. Model Evaluation

