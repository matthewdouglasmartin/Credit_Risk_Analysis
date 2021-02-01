# Credit_Risk_Analysis
Supervised Machine Learning and Credit Risk
## Overview of the Analysis:

Financial entities, such as banks and credit card companies, can incur major losses over time if credit risk is not accurately assessed and determined for applicants.  Six different methods of sampling consumer credit data were used and then ran through machine learning models in order to determine which method would be most reliable when performing analysis on credit risk.  

## Results:

### Naive Random Oversampling
*  Balanced Accuracy Score: 63.8%
*  Confusion Matrix:
   *  ![Random Oversampling CM](https://github.com/matthewdouglasmartin/Credit_Risk_Analysis/blob/main/Resources/NRO_CM.png)
* Classification Report:
  *  ![Random Oversampling CR](https://github.com/matthewdouglasmartin/Credit_Risk_Analysis/blob/main/Resources/NRO_CR.png)
* Notes: A little more than 50% of the time this method and model will be accurate. Likely to correctly predict low-risk applicants (high precision) but not for high-risk applicants (low precision).  Around 61% and 66% likelihood that the test will measure predictions and the predictions are true (high-risk has higher precision).  

### SMOTE Oversampling
*  Balanced Accuracy Score: 65.9%
*  Confusion Matrix:
   *  ![SMOTE CM](https://github.com/matthewdouglasmartin/Credit_Risk_Analysis/blob/main/Resources/SMOTE_CM.png)
* Classification Report:
  * ![SMOTE CR](https://github.com/matthewdouglasmartin/Credit_Risk_Analysis/blob/main/Resources/SMOTE_CR.png)
* Notes: The accuracy score is slightly higher with this test, just over 65%. Likely to correctly predict low-risk applicants (high precision) but not for high-risk applicants (low precision). Around 62% and 69% likelihood that the test will measure predictions and the predictions are true (low risk has higher precision). 

### ClusterCentroids Undersampling
*  Balanced Accuracy Score: 54.7%
*  Confusion Matrix:
   *  ![ClusterCentroids CM](https://github.com/matthewdouglasmartin/Credit_Risk_Analysis/blob/main/Resources/CLUST_CM.png)
* Classification Report:
  * ![CLusterCentroids CR](https://github.com/matthewdouglasmartin/Credit_Risk_Analysis/blob/main/Resources/CLUST_CR.png)
* Notes: Lowest quality accuracy rate of all tests. Likely to correctly predict low-risk applicants (high precision) but not for high-risk applicants (low precision). More precise with determining high risk applicants (68%) compared to low risk applicants (41%).  This is the one positive aspect of this test, but not enough to outperform all other tests.

### SMOTEEN Over and Under Sampling
*  Balanced Accuracy Score: 62.4%
*  Confusion Matrix:
   *  ![SMOTEEN CM](https://github.com/matthewdouglasmartin/Credit_Risk_Analysis/blob/main/Resources/SMOTEEN_CM.png)
* Classification Report:
  * ![SMOTEEN CR](https://github.com/matthewdouglasmartin/Credit_Risk_Analysis/blob/main/Resources/SMOTEEN_CR.png)
* Notes: Again, not an ideal accuracy score for this test. Likely to correctly predict low-risk applicants (high precision) but not for high-risk applicants (low precision). More precise with determining high risk applicants (65%) compared to low risk applicants (59%). 
  
### Balanced Random Forest Classifier
*  Balanced Accuracy Score: 78.7%
*  Confusion Matrix:
   *  ![BRFC CM](https://github.com/matthewdouglasmartin/Credit_Risk_Analysis/blob/main/Resources/BRFC_CM.png)
* Classification Report:
  *  ![BRFC CM](https://github.com/matthewdouglasmartin/Credit_Risk_Analysis/blob/main/Resources/BRFC_CR.png)
* Notes: The accuracy score for this test is not perfect but it is good, any better and there might be concerns of overfitting model to the data.  Likely to correctly predict low-risk applicants (high precision) but not for high-risk applicants (low precision). This model is more precise with identifying low risk applicants (91%) compared to high risk applicants (67%).  The precision for high risk applicants is not horrible, nor is it ideal. 
  
### Easy Ensemble AdaBoost Classifier
*  Balanced Accuracy Score: 92.5%
*  Confusion Matrix:
   *  ![EEC CM](https://github.com/matthewdouglasmartin/Credit_Risk_Analysis/blob/main/Resources/EEC_CM.png)
* Classification Report:
  *  ![EEC CR](https://github.com/matthewdouglasmartin/Credit_Risk_Analysis/blob/main/Resources/EEC_CR.png)
* Notes: This model and test has the highest accuracy of all six models for machine learning.  In addition its sensitivity for both types of applicants is over 90%.  Almost seems too good too be true and needs to be adjusted over concerns of overfitting.

## Summary:

An ideal model to use with a dataset such as this would be one that has a strong accuracy score (not too strong) and the sensitivity metrics are equally as strong. The ClusterCentroids model provided the lowest accuracy score of all tests, 54.7%.  the model that produced the highest accuracy score was the Easy Ensemble AdaBoost Classifier model, 92.5%, and over 90% sensitivity for both categories.  Though the latter seems like an ideal candidate for future predictions, these stats would need to be further tested with other datasets in order to disprove any concerns of overfitting the model.  Therefore the model that would be recommended out of the six is the Balanced Random Forest Classifier, with an accuracy score of 78.7%.  In addition to this metric, this model tested with good results for sensitivity.  Though these scores are not as high as the Easy Ensemble model, they are more likely to produce dependable results with future datasets.     