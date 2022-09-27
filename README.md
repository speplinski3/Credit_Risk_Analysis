# Analysis of Credit Risk
## Overview
LendingClub, a peer-to-peer lending services company, has asked for our help in assessing customer credit risk.
Using Python, machine learning models to assess credit risk were created. The following methods were used:
* Oversample the data using the RandomOverSampler and SMOTE algorithms
* Undersample the data using the ClusterCentroids algorithm. 
* A combinatorial approach of over- and undersampling using the SMOTEENN algorithm. 
* Comparison of two new machine learning models that reduce bias, BalancedRandomForestClassifier and EasyEnsembleClassifier, to predict credit risk. 
* Evaluate the performance of these models and make a written recommendation on whether they should be used to predict credit risk.
## Results

* Oversample using RandomOverSampler and SMOTE algorithms 

![image](https://user-images.githubusercontent.com/103383489/192425591-bd570e34-7bf8-4898-8149-2c857c8127ea.png)

**The balanced accuracy score is 62.9%.
The high_risk precision is about 1% only with 57% sensitivity which makes a F1 of 2% only.
Due to the high number of the low_risk population, its precision is almost 100% with a sensitivity of 58%.**

![image](https://user-images.githubusercontent.com/103383489/192426425-c3f60152-8d8c-4565-8cc4-83315664291b.png)

**The balanced accuracy score is 62.7%.
The high_risk precision is about 1% only with 62% sensitivity which makes a F1 of 2% only.
Due to the high number of the low_risk population, its precision is almost 100% with a sensitivity of 62%.**

---

* Undersample using the ClusterCentroids algorithm

![image](https://user-images.githubusercontent.com/103383489/192426736-676635cc-771c-4059-955d-5ea645bc4cc8.png)

**The balanced accuracy score is 51%.
The high_risk precision is about 1% only with 59% sensitivity which makes a F1 of 1% only.
Due to the high number of the low_risk population, its precision is almost 100% with a sensitivity of 43%.**

---

* A combinatorial approach of over- and undersampling using the SMOTEENN algorithm

![image](https://user-images.githubusercontent.com/103383489/192427501-26af4860-de27-4122-9e49-a82685ed95f0.png)

**The balanced accuracy score is 62%.
The high_risk precision is about 1% only with 70% sensitivity which makes a F1 of 2% only.
Due to the high number of the low_risk population, its precision is almost 100% with a sensitivity of 54%.**

---

* Comparison of two new machine learning models that reduce bias, BalancedRandomForestClassifier and EasyEnsembleClassifier, to predict credit risk.

![image](https://user-images.githubusercontent.com/103383489/192428246-defb5a9f-a1b2-42f7-8555-feab991cee64.png)

**The balanced accuracy score improved to about 78%.
The high_risk precision is still low at 4% only with 67% sensitivity which makes a F1 of only 7%.
Due to a lower number of false positives, the low_risk sensitivity is now 91% with 100% presicion.**

![image](https://user-images.githubusercontent.com/103383489/192428427-e72be9bb-ae69-4186-91bd-3d9e763b57fe.png)

**The balanced accuracy score improved to about 92.5%.
The high_risk precision is 7% with 91% sensitivity which makes a F1 of 14%.
Due to a lower number of false positives, the low_risk sensitivity is now 91% with 100% presicion.**

## Summary
In the end, all algorithms would not be useful in advising a lender customer credit risk. EasyEnsembleClassifier had the highest accuracy score, but its high-risk F-Score at best was 14% for assessing high-risk lending. 
