# Overview
The Juniper Team of the Erdős Institute has utilized machine learning algorithms to predict the dominant forest cover types from ecological and geological information about a 30m x 30m patch in the Roosevelt National Forest of northern Colorado. In doing so, our project addresses two primary goals:
1. Generating an optimal algorithm to predict the cover type based on US Forest Service Information System data
2. Visualizing data to find hidden relationships between variables and communicate these relationships to wide users
We have evaluated the success of our models using the overall accuracies of each dominant forest cover type. After applying 6 algorithms, we found the Random Forest model with parameter tunings had the highest accuracy of 0.88. 

### Team Members:
- Chris Chia
- [Moeka Ono](https://www.linkedin.com/in/moeka-ono/)

## Dataset
The dataset of this project is available on [Kaggle](https://www.kaggle.com/competitions/forest-cover-type-kernels-only/data). The original training dataset includes 15,120 observations with 7 dominant forest cover types, including 1) Spruce/Fir, 2) Lodgepole pine, 3) ponderosa pine, 4) cottonwood/willow, 5) Aspen, 6) Douglass-fir, and 7) Krummholz. The dataset has 12 features containing both continuous and categorical data. The categorical features were already one hot coded, leading to a total of 53 independent variables. The 7 types of forest covers were balanced equally in the dataset. In our project, we split the original training set and used 90% as our training set and the remaining 10% as a validation data set. 

## Exploratory Data Analysis
### Visualization data with Topology
Topology has been used successfully with other projects (ex. COVID-19 data) to find hidden relationships between variables. Could we use topology to find some hidden relationships in this project?

### Model Selection
Soil_type7 and Soil_type15 don't have any correlations with Cover_Type, so we removed these variables from the training dataset.
![image](https://user-images.githubusercontent.com/90373346/204120644-ff4ba1d8-f6a3-4b04-bcfe-23425a923e38.png)

We deployed 6 algorithms: Random Forest, k-nearest neighbors (KNN), Support Vector Machines (SVM), Gradient Boosting, AdaBoost, and xgboost. 

## Results
Overall, our three ensemble learning algorithms (Random forest, XGBoost and Gradient Boosting) did better in predicting our dataset. The random forest classifier and XGBoost with parameter tuning had the highest overall accuracy of 0.88. On the other hand, KNN performed poorly because of overfitting since k=1 was the optimal estimator based on the result of the cross-validations. When focusing on the predicted forest cover class, type 1 and type 2 got mistaken for each other, likely resulting from xxx.  

## Future directions
1. 
