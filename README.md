# Credit Risk Analysis

## Overview of Analysis

The purpose of this analysis is to assist LendingClub in finding a good tecnique to predict their credit risk. With the data they've provided, we will go through 6 machine learning models to find which model performs the best. The models we will be testing include: Random Over Sampler, SMOTE, Cluster Centroids, SMOTEENN, Balanced Random Forest Classifier, and Easy Ensemble Classifier. Our findings and results can be found below. 


## Results

Using oversampling, undersampling, combination, and ensemble learners, we ran several tests to see which algorithm would give us the best overall balanced accuracy, precision, and recall scores. The results are below along with screenshots of our other measures such as the F1 Score to support the findings. 


### Oversampling Testing

#### Random Oversampler

* Balanced Accuracy Score: 0.65
* Precision Score: 0.99
* Recall Score: 0.68

![This is an image](https://github.com/belennlopezvega/Credit_Risk_Analysis/blob/main/Resources/RandomOverSampler.png)

Looking at the RandomOverSampler algorithm, the accuracy and recall score are lower than we would want them to be. Our precision score is high but as we'll show in the coming test, this is a recurrence in all the tests which if great, but doesn't tell us much when comparing all the models. 

#### SMOTE

* Balanced Accuracy Score: 0.64
* Precision Score: 0.99
* Recall Score: 0.66

![This is an image](https://github.com/belennlopezvega/Credit_Risk_Analysis/blob/main/Resources/SMOTE.png)

The SMOTE algorithm performed slightly worse than the Random Oversampler as it's accuracy and recall scores were a couple percentages below the Random Oversampler results. The F1 scores are only off by a percentage so it's safe to say oversampling in general wouldn't be the best to predict credit risk.


### Undersampling Testing

#### Cluster Centroids

* Balanced Accuracy Score: 0.52
* Precision Score: 0.99
* Recall Score: 0.44

![This is an image](https://github.com/belennlopezvega/Credit_Risk_Analysis/blob/main/Resources/Cluster_Centroids.png)

Looking at the Cluster Centroids model, the performance is overall worse than that of the oversampling models. The accuracy score and recall score are way too low, and although the precision score stays the same, it doesn't make up for the other measures. The F1 score is at 0.60 being the lowest F1 score thus far. 

#### SMOTEENN

* Balanced Accuracy Score: 0.62
* Precision Score: 0.99
* Recall Score: 0.57

![This is an image](https://github.com/belennlopezvega/Credit_Risk_Analysis/blob/main/Resources/SMOTEENN.png)

SMOTEENN performed better than Cluster Centroids, so out of both undersampling algorithms this would be the best, but still not as good as the first two oversampling algorithms. The accuracy score in this model performed better and as a result the F1 score is higher at 0.72.


### Ensemble Learners 

#### Balanced Random Forest Classifier

* Balanced Accuracy Score: 0.78
* Precision Score: 0.99 
* Recall Score: 0.91

![This is an image](https://github.com/belennlopezvega/Credit_Risk_Analysis/blob/main/Resources/BalancedRandomForestClassifier.png)

The results of the Balanced Random Forest Classifier proved to be the best thus far. The accuracy score is average at 0.78 and the precision and recall scores are close enough to each other so that F1 score is at 0.95 which is typically an indicator of a good model, but then we could start running into the issue of overfitting which could ruin the performance of the model on new data. 

#### Easy Ensemble Classifier

* Balanced Accuracy Score: 0.92
* Precision Score: 0.99
* Recall Score: 0.94

![This is an image](https://github.com/belennlopezvega/Credit_Risk_Analysis/blob/main/Resources/EasyEnsembleClassifier.png)

The results of the Easy Ensemble Classifier model prove to be the highest overall results. The accuracy score sits at 0.92 and the precision and recall score combined make an F1 score of 0.97 which is the highest F1 score we've had. This model predicts credit risk the best - but as stated above, we could run into overfitting in the future.  


## Summary

Overall the ensemble learning models proved to work the best, next would be oversampling, and last would be undersampling which we don't recommend. Moving forward, we recommend using the Easy Ensemble Classifier algorithm as it proved to have the best overall accuracy, precision, and recall scores in comparison to the other 5 models. 
