###Challenge - LendingClub

##Overview

Build and evaluate several machine learning models to assess credit risk, using data from LendingClub; a peer-to-peer lending services company.
Employ different techniques to train and evaluate models with unbalanced classes. Use imbalanced-learn and scikit-learn libraries to build and evaluate models using resampling. Evaluate the performance of these models and make a recommendation on whether they should be used to predict credit risk.

##Models Evaulated: 
    #Random - Oversample 
	    Precision = 0.010
	    Recall = 0.723
	    Balanced Accuracy Score = 0.658
    #SMOTE – Oversample 
	    Precision = 0.012
	    Recall = 0.644
	    Balanced Accuracy Score = 0.66
    #Cluster Centroids – Undersample
	    Precision = 0.006
	    Recall = 0.663
	    Balanced Accuracy Score = 0.53
    #Combination SMOTEENN
	    Precision = 0.010
	    Recall = 0.733
	    Balanced Accuracy Score = 0.65
    #Balanced Random Forest Classifier
	    Precision = 0.027
	    Recall = 0.594
	    Balanced Accuracy Score = 0.73
    #Easy Ensemble AdaBoost Classifier
	    Precision = 0.920
	    Recall = 1.000
	    Balanced Accuracy Score = 0.996

##Final recommendation on the model to use:

Random Over Sampling, SMOTE, Cluster Centeroids, SMOTEENN, and Balanced Random Forest Classifier algorithms all did a poor job at accurately predicting credit risks.  Of these five methods; SMOTEEN has the best sensitivity, an the Balanced Random Forest Classifier did a fair job of minimizing false positives. However, none of these algorithms were very accurate at positively identifying credit risks and the absence of risk.   

The Easy Ensemble AdaBoost Classifier produced the best results for determining credit risk from the dataset.  It produced 0 false negatives, and only 2 false positives, and has an exceedingly high Balanced Accuracy Score of 0.996 indicating that the algorithm correctly predicts the both credit risks and the absence of credit risks.  However, these promising test results may not repeat as the algorithm is used on further data, this may be a case of overfitting.  Still it is recommended to use Easy Ensemble AdaBoost Classifier algorithm to predict credit risks.  
