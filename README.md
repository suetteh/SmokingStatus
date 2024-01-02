# Smoking Status Prediction Using Machine Learning

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
In this project, 1% of missing vaues was genetrated for practice purpose.missForest was applied for data imputation step, which handles missing data with random forest imputation algorithm, it can handle multivariate data consisting continuous and categorical variables simultaneously. Although missForest outperforms several imputation methods (KNNImpute, MICE), it is still rather expensive in terms of computation cost compared to KNNimpute. In order to speed up the process, the function was run in parallel by setting up a parallel backend and fixing parallelize=’forest’. This sets the total number of trees in each random forest to split in the same way.

## Concolusion:
This study showed that Decision Tree, Random Forest and XGBoost can be used to predict smoking status with 18 features which include the biochemistry and vital readings of patients. Among the three learning models, Random Forest shows the best performance, with Accuracy: 82.55%, AUC: 0.911, Sensitivity: 84.9% and Specificity: 78.51%. In general, each model has slightly better performance on training set than on test set. However, the difference is subtle which suggests there is no overfitting and underfitting issues. In this dataset, some features were recorded in categories such as height, weight, and age. It is not known if some important insights were missed in this dataset. In order to improve the prediction accuracy of the model, dataset should be kept in the unprocessed form. In future work, this study can further be extended to combine machine learning and statistical analysis to draw some valid conclusions from the study.
