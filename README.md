# Machine Learning Homework - Exoplanet Exploration
Background
Over a period of nine years in deep space, the NASA Kepler space telescope has been out on a planet-hunting mission to discover hidden planets outside of our solar system.
To help process this data, create machine learning models capable of classifying candidate exoplanets from the raw dataset.
1. Preprocess the raw data
2. Tune the models
3. Compare two or more models

Conclusion
-------------
Random Forest Classifier Method fits the model best and scores the best Accuracy Results!

Process
----------
Data Cleaning and Pre-Processing: Data was read in from the exoplanet csv file. Null columns and null rows were dropped. Columns available to select as features to train the model on - "koi disposition." With X and y values set, split the data into training and testing sets using train_test_split with stratify=y to ensure that there was an even distribution of classification values in both data sets. Then, MinMaxScaler is used to scale both sets of X data.

This process was used for all four models, mentioned below.

Random Forest Classifier
--------------------------
Random Forest Classifier Score without Gridsearch

Training Data Score: 0.9937058935723823

Testing Data Score: 0.8781464530892449

Random Forest Classifier Score with Gridsearch

Training Data Score: 1.0
Testing Data Score: 0.8935926773455377

Random Forest Classification report

                   precision    recall  f1-score   support

     CANDIDATE       0.83      0.74      0.78       422
     CONFIRMED       0.80      0.84      0.82       450
     FALSE POSITIVE  0.97      1.00      0.98       876
      accuracy                           0.89      1748
     macro avg       0.87      0.86      0.86      1748
     weighted avg    0.89      0.89      0.89      1748

-------------------------------------------------------------------------------------------------------------------------------------------
Logistic Regression Score
----------------------------
Initialize the model using LogisticRegression() and fit the model using the training data. Then score the model using both the training and testing data. Both sets scored fairly well, with the training data at 84.11% and the testing data at 84.09%.

Training Data Score: 0.8411214953271028
Testing Data Score: 0.8409610983981693

GridSearchCV is then used to further tune the parameters to create a better scoring model. The parameters were set to explore different C values using both L1 and L2 penalties as regularization methods. Then fit a new model using this grid and found the best parameters, before predicting on the test data. This new model's score was 88.00%.

----------------------------------------------------------------------------------------------------------------------------------------------

KNN Score
-------------

KNN Score without Gridsearch

Training Data Score: 0.8725920274651917

Testing Data Score: 0.8249427917620137

KNN Score with Gridsearch

Training Data Score: 0.8725920274651917

Testing Data Score: 0.8249427917620137

------------------------------------------------------------------------------------------
Support Vector Machine
------------------------
Initialized the model with SVC() and set the kernel to linear before training and scoring the model, with the testing data scoring at 84.15%.

SVM without Gridsearch

Training Data Score: 0.8439824527942018

Testing Data Score: 0.8415331807780321

With Grid Search, explored various C values, gamma values. After training the new model, accuracy increased to 88.61%. 

SVM with Gridsearch

Training Data Score: 0.8901392332633988

Testing Data Score: 0.8861556064073226

SVM Classification Report

                   precision    recall  f1-score   support

     CANDIDATE       0.84      0.69      0.76       422
     CONFIRMED       0.75      0.85      0.80       450
     FALSE POSITIVE  0.98      1.00      0.99       876
      accuracy                           0.89      1748
     macro avg       0.86      0.85      0.85      1748
     weighted avg    0.89      0.89      0.88      1748

