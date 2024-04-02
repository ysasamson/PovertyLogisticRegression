# Poverty Predictor Logistic Regression Model
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

Logistic Regression model built using features whose absolute value of the correlation efficient was higher than 0.2. The dataset was split into a train and test datasets.

![image](https://github.com/ysasamson/PovertyPredictorModel/assets/145044637/58fc70ee-60ed-490d-a216-d1a7bc8e963c)


## Step 3. Model Evaluation

Confusion matrix.

![image](https://github.com/ysasamson/PovertyPredictorModel/assets/145044637/08badcad-645c-4bf1-8d93-814471d3301a)

![image](https://github.com/ysasamson/PovertyPredictorModel/assets/145044637/872505bd-d919-4fdc-906e-e449f01a8910)

| Metric        | Score           |
| :-----------: |:-------------:|
| Accuracy      | 0.70 |
| Precision     | 0.71      | 
| Recall        | 0.88      |
| F1-Score        | 0.79      |
| Area under ROC curve        | 0.73      |

ROC AUC

![image](https://github.com/ysasamson/PovertyPredictorModel/assets/145044637/f158c011-4a1f-4916-a254-7b2e0fa10e3c)

![image](https://github.com/ysasamson/PovertyPredictorModel/assets/145044637/48636b5f-2f23-4eaa-92f3-ebe0c989f4dc)

## Conclusion
Based on the metric evaluation, the model achieves an accuracy of 0.70, which means it correctly predicts the outcome for approximately 70% of the instances in the dataset. A precision score of 0.71 indicates that when the model predicts a positive outcome, it is correct about 71% of the time. A recall of 0.88 indicates that the model correctly identifies 88% of all actual positive instances in the dataset. The F1-score, which is the harmonic mean of precision and recall is 0.79, this means there is a reasonable balance between precision and recall. An AUC (area under the ROC curve) of 0.73 indicates that the model is moderately effective at distinguishing between the two classes. Overall, the logistic regression model seems to predict poverty incidence reasonably well, with relatively high recall (88%) suggesting it is good at capturing positive instances, and a balanced F1-score (0.79) indicating a trade-off between precision and recall. 
