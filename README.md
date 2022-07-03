# Credit_Risk_Analysis

## Overview
In this project we are using the credit card credit dataset from LendingClub, oversampling the data using the RandomOverSampler and SMOTE algorithms, and undersampling the data using the ClusterCentroids algorithm. We will then use a combinatorial approach of over- and undersampling using the SMOTEENN algorithm. Then compare two new machine learning models that reduce bias, BalancedRandomForestClassifier and EasyEnsembleClassifier, to predict credit risk.

## Results
### RandomOverSampler model
![ROSM 1](https://user-images.githubusercontent.com/100887673/177052600-76b0caa0-b9c6-4ad3-b580-aecfa694ee82.png)

![ROSM 2](https://user-images.githubusercontent.com/100887673/177052606-1743b91d-9161-4737-a9d8-34c47b50e1de.png)

The balanced accuracy is almost 68% & the high risk prediction is 1%. It has 60% sensitivity with F1 at 2%. Due to the lower number of High_risk prediction, the total / avergae preditction for this is at almost 100%.


### SMOTE model
![SMOTE 1](https://user-images.githubusercontent.com/100887673/177052627-07e626f9-2b22-48a8-b5cb-ecc531c05446.png)


![SMOTE 2](https://user-images.githubusercontent.com/100887673/177052635-cefc9259-5339-47f9-80cb-c32ffac0d125.png)

The balanced accuracy is at almost 66% & high_risk prediction, like above, is at 1%. Similarly, it also has a high number of the low_risk number bringing its prediction to almost 100%.

ClusterCentroids model
![CC 1](https://user-images.githubusercontent.com/100887673/177052650-02cb49af-68a9-48bd-8366-2cb73dc823cc.png)


![CC 2](https://user-images.githubusercontent.com/100887673/177052653-a64f7be2-4df0-41ee-bc5a-2af1f2f8dd13.png)
The balanced accuracy drops to 43% but the high_risk is still at 1% with sensitivity 59% and F1 of 1%. Still, low risk prediction is higher than high_risk.

SMOTEEN model
![SMOTEEN 1](https://user-images.githubusercontent.com/100887673/177052663-ea208698-a113-474a-8983-170d7f3bd741.png)


![SMOTEEN 2](https://user-images.githubusercontent.com/100887673/177052666-8af12323-53c9-4a43-8b0e-c71d3077bd71.png)

The balanced accuracy score is about 54% & the high_risk is still 1% with 71% sensitivity which makes a F1 of only 2%.
Due to the high number of false positives, the low_risk sensitivity is 54%.

BalancedRandomForestClassifier model
![BRFC 1](https://user-images.githubusercontent.com/100887673/177052683-7f9cff90-e5ec-4754-9e47-780b1bc2d47f.png)


![BRFC 2](https://user-images.githubusercontent.com/100887673/177052688-3363522c-c7fb-457a-ba90-327133123533.png)

The balanced accuracy score jumps to 90% but the high_risk jumps to, still low, 4% with 67% sensitivity which makes a F1 of only 7%.
The low_risk sensitivity is now 91% with 100% presicion.

EasyEnsembleClassifier model
![EEC 1](https://user-images.githubusercontent.com/100887673/177052725-10382610-6477-45b3-8e5d-95c5cef269fd.png)


![EEC 2](https://user-images.githubusercontent.com/100887673/177052730-578a0e24-1034-4e92-8349-1ed38c9e2b63.png)
The balanced accuracy jumps to 94% and high_risk precision is still low at 7%. Due to a smaller amount of false positives, the low_risk sensitivity is now 94% with 100% presicion.

### Summary
In conclusion, utilizing EasyRnsembleClassifier seems to be most effective model because it provides the highest score for risky loans, which means it has most efficient detection for risky credits. But, there are a number of lowrisk credits which are falsely deteced as high risk and can hamper the lenders's ability to provide credit to those accounts. In turn, this will affect the lender's revenue.

