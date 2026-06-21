# Day 10 - Model Comparison and Hyperparameter Tuning

## Objective

The objective of this exercise was to compare multiple machine learning classification algorithms for customer churn prediction and identify the best-performing model based on business requirements.

## Models Evaluated

1. Logistic Regression
2. Random Forest
3. Gradient Boosting
4. XGBoost
5. K-Nearest Neighbors (KNN)

## Feature Engineering Used

* tenure_group
* Years_x_sites
* Log_Total_Purchase
* Years_Squared

## Pipeline Components

* ColumnTransformer
* StandardScaler
* OneHotEncoder
* Pipeline

## Hyperparameter Tuning

GridSearchCV was used to tune Random Forest and XGBoost models.

Cross Validation:

* 5-Fold Cross Validation (cv=5)

Evaluation Metric:

* Recall

Reason:
The business objective is to identify customers who are likely to churn. Therefore, recall was prioritized over accuracy.

## Model Results

| Model               | Recall |
| ------------------- | ------ |
| Logistic Regression | 0.59   |
| Gradient Boosting   | 0.53   |
| Tuned XGBoost       | 0.47   |
| Random Forest       | 0.44   |
| KNN                 | 0.38   |

## Best Model

Logistic Regression achieved the highest recall and F1-score and was selected as the final model.

## Key Learnings

* Complex models do not always outperform simple models.
* Recall is often more important than accuracy for churn prediction.
* GridSearchCV helps identify optimal hyperparameters.
* Cross Validation provides more reliable model evaluation.
* Pipelines make preprocessing and modeling reusable and production-ready.

## Conclusion

After evaluating multiple classification algorithms, Logistic Regression delivered the best overall performance for this dataset and was selected as the final model for churn prediction.
