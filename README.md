# SmokingStatus
Smoking Status Prediction Using Machine Learning

Smoking has been known as a key factor in causing diseases with high mortality rate such as lung diseases, cancer, and cardiovascular disease. The use of machine learning can help to develop effective treatment regimens for smoking cessation and detect any onset of diseases caused by smoking. This can enable early treatment to be given to reverse the condition. This study explored on the performance of three tree-based machine learning models Decision Tree, Random Forest and Extreme Gradient Boosting in predicting smoking status using 19 features. 

## Tools applied: 
This project was completed using R programming language. Multiple libraries were used include DataExplorer, doParallel, missForest, missMethods, VIM, caret, rpart, ggplot2, dplyr, tree, randomForest and caTools. 

## Data source: 
The dataset used is a collection of health checkup information of smoking and non-smoking individuals and it is extracted from Kaggle (https://www.kaggle.com/datasets/kukuroo3/body-signal-of-smoking). The dataset was compiled by Kukuroo3 (2022) from a Korean database (https://www.data.go.kr/data/15007122/fileData.do) and translated into English language.

## Dataset preparation:
- Missing values: This dataset does not have any missing values. For practice purpose, 1% of missing values was generated include metric and non-metric variables.
- Data pre-processing techniques were applied: outliers removal, one-hot encoding (only for XGBoost model), data imputation using missForest, exclude variables which have weak or no correlation with other variables.
- Hyperparameter tuning was performed to each base model
- Model fitness was evaluated based on the comparison of model performance on training and test data.

## Challenges: 
missForest was applied for data imputation step, which handles missing data with random forest imputation algorithm, it can handle multivariate data consisting continuous and categorical variables simultaneously. Although missForest outperforms several imputation methods (KNNImpute, MICE), it is still rather expensive in terms of computation cost compared to KNNimpute. In order to speed up the process, the function was run in parallel by setting up a parallel backend and fixing parallelize=’forest’. This sets the total number of trees in each random forest to split in the same way.

## Concolusion:
Random Forest with ntree=2000, mtry=3 achieved best results 82.55% accuracy, 0.911 AUC, 84.9% sensitivity and 78.51% specificity.
