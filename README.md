# Machine Learning Homework - Exoplanet Exploration
Background
Over a period of nine years in deep space, the NASA Kepler space telescope has been out on a planet-hunting mission to discover hidden planets outside of our solar system.
To help process this data, you will create machine learning models capable of classifying candidate exoplanets from the raw dataset.
In this homework assignment, you will need to:
1. Preprocess the raw data
2. Tune the models
3. Compare two or more models

Conclusion
-------------
Random Forest Classifier Method fits the model best and scores the best Accuracy Results!
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
FALSE POSITIVE       0.97      1.00      0.98       876

      accuracy                           0.89      1748
     macro avg       0.87      0.86      0.86      1748
  weighted avg       0.89      0.89      0.89      1748

-----------------------------------------------------------------------------------------


Logistic Regression Score
Training Data Score: 0.8411214953271028
Testing Data Score: 0.8409610983981693

-----------------------------------------------------------------------------------------

KNN Score without Gridsearch
Training Data Score: 0.8725920274651917
Testing Data Score: 0.8249427917620137

KNN Score with Gridsearch
Training Data Score: 0.8725920274651917
Testing Data Score: 0.8249427917620137

------------------------------------------------------------------------------------------
SVM without Gridsearch
Training Data Score: 0.8439824527942018
Testing Data Score: 0.8415331807780321

SVM with Gridsearch
Training Data Score: 0.8901392332633988
Testing Data Score: 0.8861556064073226

SVM Classification Report
                   precision    recall  f1-score   support

     CANDIDATE       0.84      0.69      0.76       422
     CONFIRMED       0.75      0.85      0.80       450
FALSE POSITIVE       0.98      1.00      0.99       876

      accuracy                           0.89      1748
     macro avg       0.86      0.85      0.85      1748
  weighted avg       0.89      0.89      0.88      1748

