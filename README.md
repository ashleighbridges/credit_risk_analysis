# credit_risk_analysis

## Overview
The purpose of this analysis to use multiple different algorithms to predit credit risk and assess the performance of the models. To perform this analysis, we used the following models:
- RandomOverSampler
- SMOTE
- ClusterCentroids
- SMOTEENN
- BalancedRandomForestClassifier
- EasyEnsembleClassifier

## Results

### *RandomOverSampler Model*
![ROS BOS](https://user-images.githubusercontent.com/100883212/181137523-be814f7f-a900-48cc-bdc4-fc7e1350cb6c.png)

![ROS CM](https://user-images.githubusercontent.com/100883212/181137530-309d722d-0155-49b0-bda6-f87d87d477a5.png)

![ROS CR](https://user-images.githubusercontent.com/100883212/181137539-39e5a6a3-a081-47d6-96bf-ad96d82ae8a5.png)

The balanced accuracy score is 64%. Due to the highly imbalanced numbers between the low_risk and high_risk populations, the precision score for the high_risk population is only 1% with a sensitivity of 60%. The precision of the low_risk population is 100% with a sensitivity of 65%.

### *SMOTE Model*
![SMOTE BOS](https://user-images.githubusercontent.com/100883212/181137549-ff10460e-5b63-4a2f-9dc9-218995a7e59b.png)

![SMOTE CM](https://user-images.githubusercontent.com/100883212/181137563-6cfe59de-de8a-41bf-ab59-62bd8c4f80b6.png)

![SMOTE CR](https://user-images.githubusercontent.com/100883212/181137572-08ab2c61-948a-4bbd-a928-0fd9c79cf08b.png)

The balanced accuracy score is 64%. Due to the highly imbalanced numbers between the low_risk and high_risk populations, the precision score for the high_risk population is only 1% with a sensitivity of 64%. The precision of the low_risk population is 100% with a sensitivity of 66%.

### *ClusterCentroids Model*
![CC BAS](https://user-images.githubusercontent.com/100883212/181137589-7db791d2-5004-4bdf-a132-d4e72a4a6ff2.png)

![CC CM](https://user-images.githubusercontent.com/100883212/181137598-ae3e6230-808a-4549-b459-63387756bd2b.png)

![CC CR](https://user-images.githubusercontent.com/100883212/181137602-7ae2bf2b-fe65-4807-8023-a622527c257c.png)

The balanced accuracy score is 64%. Due to the highly imbalanced numbers between the low_risk and high_risk populations, the precision score for the high_risk population is only 1% with a sensitivity of 59%. The precision of the low_risk population is 100% with a sensitivity of 43%.

### *SMOTEENN Model*
![SMOTEENN BAS](https://user-images.githubusercontent.com/100883212/181137627-d8e8dea9-9da6-4845-818d-d5d96f22793b.png)

![SMOTEENN CM](https://user-images.githubusercontent.com/100883212/181137646-1e47f430-fe6f-486e-80e9-887d4cd99863.png)

![SMOTEENN CR](https://user-images.githubusercontent.com/100883212/181137651-2b7ef19a-b1b3-4d32-a489-110b0f290a65.png)

The balanced accuracy score is 64%. Due to the highly imbalanced numbers between the low_risk and high_risk populations, the precision score for the high_risk population is only 1% with a sensitivity of 70%. The precision of the low_risk population is 100% with a sensitivity of 57%.

### *BalancedRandomForestClassifier Model*
![BRFC BAS](https://user-images.githubusercontent.com/100883212/181137666-ebdd3e2b-d918-489e-a649-13e524be5825.png)

![BRFC CM](https://user-images.githubusercontent.com/100883212/181137684-5a3da19d-08b5-4c85-b5ea-415f7d836610.png)

![BRFC CR](https://user-images.githubusercontent.com/100883212/181137688-8a95f8b6-8179-4f7d-9d85-462e5297584d.png)

The balanced accuracy score is 93%. The precision score for the high_risk population is 4% with a sensitivity of 67%. The precision of the low_risk population is 100% with a sensitivity of 91%.

### *EasyEnsembleClassifier Model*
![EEC BAS](https://user-images.githubusercontent.com/100883212/181137702-046ed51f-137e-40fa-9f92-eeebe24df7b6.png)

![EEC CM](https://user-images.githubusercontent.com/100883212/181137716-78251ae2-5a2f-4576-9213-ba59dd91a514.png)

![EEC CR](https://user-images.githubusercontent.com/100883212/181137881-4ef0bc11-6b88-4ff8-99c6-aa887699068a.png)

The balanced accuracy score is 93%. The precision score for the high_risk population is 7% with a sensitivity of 91%. The precision of the low_risk population is 100% with a sensitivity of 94%.

## Summary

None of the models used in this analysis had a precision score at or above 10% for the high_risk population, which shows that there is a low chance the algorithm will be able to precisely predict high credit risk.

The Ensemble models used showed far higher balanced accuracy and sensitivity scores than the Resampling models. The EasyEnsembleClassifer model had the highest scores with a balanced accuracy score of 93% and a sensitivity of 93% (predicted 79 out of 87 high-risk situations correctly). However, the low precision score shows that with larger samples, there is a high chance the model will incorrectly label low-risk clients as high-risk, leading to a poor client experience. 

Because even the best model we used could easily lead to poor client experience, loss of revenue, and poor reputation, I do not recommend the bank use any of these models to predict credit risk for their lending clients.
