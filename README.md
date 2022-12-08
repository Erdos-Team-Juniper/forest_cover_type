# Overview
The Juniper Team of the Erdős Institute has utilized machine learning algorithms to predict the dominant forest cover types from ecological and geological information about a 30m x 30m patch in the Roosevelt National Forest of northern Colorado. In doing so, our project addresses two primary goals:
1. Generating an optimal algorithm to predict the cover type based on US Forest Service Information System data.
2. Visualizing the “shape” of the dataset and finding the most essential variables in clustering. We wished to communicate relationships between features to a wide audience of users.

We have evaluated the success of our models using the overall accuracies in predicting each dominant forest cover type. After testing six different algorithms, we found our Random Forest and XGBoost algorithms with parameter tunings had the highest accuracy, correctly predicting 88% of our data points.

### Team Members:
- Chris Chia
- [Moeka Ono](https://www.linkedin.com/in/moeka-ono/)

## Dataset
The dataset of this project is available on [Kaggle](https://www.kaggle.com/competitions/forest-cover-type-kernels-only/data). The original training dataset includes 15,120 observations with 7 dominant forest cover types, including 1) Spruce/Fir, 2) Lodgepole pine, 3) ponderosa pine, 4) cottonwood/willow, 5) Aspen, 6) Douglass-fir, and 7) Krummholz. The dataset has 12 features containing both continuous and categorical data. The categorical features were already one hot coded, leading to a total of 53 independent variables. The 7 types of forest covers were balanced equally in the dataset. In our project, we split the original training set and used 90% as our training set and the remaining 10% as a validation data set. 

## Exploratory Data Analysis
### Visualization data with Topology
Topology has been used successfully with other projects (ex. COVID-19 data) to find hidden relationships between variables. We’ve also created images that clearly show that elevation is the feature that distinguishes clusters in our data set the most. These images highlight the most important type of data to collect in regards to cover type identification.  



### Model Selection
Soil_type7 and Soil_type15 don't have any correlations with Cover_Type, so we removed these variables from the training dataset.
![image](https://user-images.githubusercontent.com/90373346/204120644-ff4ba1d8-f6a3-4b04-bcfe-23425a923e38.png)

We have deployed a base model as multi logistic regression and 6 different ML models as belows.

- Ensemble Learning
  - Random forest
  - XGboost
  - Gradient boosting
  - Adaboost
- KNN (K-nearest neighbors)
- SVM (support vector machines)

## Results
Overall, our three ensemble learning algorithms (Random forest, XGBoost, and Gradient Boosting) did better in predicting our dataset. The random forest classifier and XGBoost with parameter tuning had the highest overall accuracy of 0.88. Compared with these models, Adaboost performed poorly in predicting the forest cover type. KNN and SVM were worse than the three ensemble models. In particular, KNN might be overfitted since k=1 was the optimal estimator based on the result of the cross-validations.

When focusing on the predicted forest cover class, type 1 and type 2 got mistaken for each other, likely resulting from their similar features. They generally prefer low to moderate soil moisture levels and are shade intolerant. Although the spruce/fir is typically fire-intolerant and lodgepole pine is not, their growths after fires are relatively fast, therefore, the distance to the past fire points, which was the only available variable, regarding fires in this dataset, might not be sufficient to distinguish these two forest cover accurately. In contrast, the precision and recall scores of type 7 (Krummholz) were almost always the highest in any model. This is because Krummholz is not a specific tree species but a unique formation of trees under exposure to fierce, freezing winds.  


In conclusion, our machine learning algorithm gives accurate predictions for those that require an assessment of the location of cover types just from knowing certain basic features such as elevation, slope, soil types, and other features that can be found from satellite imagery rather than requiring data gatherers.

## Future directions
1. Implementing time
2. Even better accuracy in distinguishing Spruce/Fir and Lodgepole Pine cover types
  - Our model struggled the most with these two cover types likely because the features except for elevation seem to be very similar. It would be ideal with having better distinguishing the two spcies since the former is fire-intolerant, the later is fire-tolerant.
3. More parameter tuning on TDA model to separate into 7 clusters for each cover type.

