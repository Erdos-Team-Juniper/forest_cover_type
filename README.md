# Forest Cover Type Prediction
The Juniper team of the Erdős Institute Data Science Bootcamp Fall 2022 has utilized multiple machine learning algorithms with the goal to predict forest cover type for a given 30 x 30 meter cells from various cartographic variables.

### Team Members:
- Chris Chia
- [Moeka Ono](https://www.linkedin.com/in/moeka-ono/)

## Dataset
The dataset used for this project can be found on [Kaggle](https://www.kaggle.com/competitions/forest-cover-type-kernels-only/data). The original training dataset includes 15,120 observations with 7 forest cover types including 1) Sprouce/Fir, 2) Lodgepole pine, 3) ponderosa pine, 4) cottonwood/willow, 5) Aspen, 6) Douglass-fir, and 7) Krummholz. The dataset has 12 features containing both continuous and categorical features. The categorical features were already one hot codede, leading to the total of 53 dependent variables. 7 types of forest cover types were equally included into the dataset. In our project, we splitted the original training set and used the 80% as our training set and the remaing 20% as validation set. 

## EDA and Model Selection
Soil_type7 and Soil_type15 don't have any correlations with Cover_Type, so we removed these variables from training dataset.
![image](https://user-images.githubusercontent.com/90373346/204120644-ff4ba1d8-f6a3-4b04-bcfe-23425a923e38.png)

We deployed 5 models: random forest, k-nearest neiboghers, suport vector machines, adaboost and xgboost. 

## Results
Overall, the ensemble learning (Random forest, Adaboost, and Xgboost) did better in predicting our dataset. The highest overall accuracy (0.88) was recorded in random forest classifier with parameter tuning. When focusing on the class closely, type 1 and type 2 tended to be predicted mistakenly that might be due to XXX. On the other hand, KNN performed poorly probably because there were not much clear differences in classes in any variables.   


## Future Directions
