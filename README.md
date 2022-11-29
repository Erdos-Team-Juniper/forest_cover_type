# Forest Cover Type Prediction
The Juniper team of the Erdős Institute Data Science Bootcamp Fall 2022 has utilized multiple machine learning algorithms to predict forest cover types for a given 30 x 30-meter patch in 4 wilderness areas in the Roosevelt National Forest.

### Team Members:
- Chris Chia
- [Moeka Ono](https://www.linkedin.com/in/moeka-ono/)

## Dataset
The dataset of this project is available on [Kaggle](https://www.kaggle.com/competitions/forest-cover-type-kernels-only/data). The original training dataset includes 15,120 observations with 7 forest cover types, including 1) Spruce/Fir, 2) Lodgepole pine, 3) ponderosa pine, 4) cottonwood/willow, 5) Aspen, 6) Douglass-fir, and 7) Krummholz. The dataset has 12 features containing both continuous and categorical data. The categorical features were already one hot coded, leading to a total of 53 independent variables. The 7 types of forest covers were balanced equally in the dataset. In our project, we split the original training set and used 80% as our training set and the remaining 20% as a validation data set. 

## EDA and Model Selection
Soil_type7 and Soil_type15 don't have any correlations with Cover_Type, so we removed these variables from the training dataset.
![image](https://user-images.githubusercontent.com/90373346/204120644-ff4ba1d8-f6a3-4b04-bcfe-23425a923e38.png)

We deployed 5 algorithms: Random Forest, k-nearest neighbors (KNN), Support Vector Machines (SVM), AdaBoost, and xgboost. 

## Results
Overall, the ensemble learning (Random forest, Adaboost, and Xgboost) did better in predicting our dataset. The random forest classifier with parameter tuning had the highest overall accuracy of 0.88. On the other hand, KNN performed poorly because of overfitting since k=1 was the optimal estimator based on the result of the cross-validations. When focusing on the predicted forest cover class, type 1 and type 2 got mistaken for each other, likely resulting from xxx.  

## Future directions
