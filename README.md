# SmokingStatus
Smoking Status Prediction Using Machine Learning

Smoking has been known as a key factor in causing diseases with high mortality rate such as lung diseases, cancer, and cardiovascular disease. The use of machine learning can help to develop effective treatment regimens for smoking cessation and detect any onset of diseases caused by smoking. This can enable early treatment to be given to reverse the condition. This study explored on the performance of three tree-based machine learning models Decision Tree, Random Forest and Extreme Gradient Boosting in predicting smoking status using 19 features. 

- R programming language was used in this study.
- Data pre-processing techniques were applied: outliers removal, one-hot encoding
- Hyperparameter tuning was performed to each base model
- Model fitness was evaluated based on the comparison of model performance on training and test data.

Concolusion:
Random Forest with ntree=2000, mtry=3 achieved best results 82.55% accuracy, 0.911 AUC, 84.9% sensitivity and 78.51% specificity.
