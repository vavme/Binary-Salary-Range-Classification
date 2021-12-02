# Binary-Salary-Range-Classification
Final Project Sanbercode Data Science 0820 <br/>
Held on https://www.kaggle.com/c/sanbercode-data-science-batch0820/ <br/>
Competition Leaderboard : 7th/130 <br/>
<br/>
Task : Predicting whether the person's salary is below or above 7 million rupiah, based on 11 parameters : Age, Work Class, Demographic Weight, Education, Duration of Education, Marriage Status, Gender, Capital Gain, Capital Loss, and  Work Hour per Week. <br/>
<br/>

Overview
========
The data is imbalanced so SMOTE was applied. Since after SMOTE the dataset is too large, undersampling was done to make the data smaller in order to make
model training faster. In this modelling, 10 model classification was made using 10 classifiers which each of them has been finely tuned.<br/>
Then, all of the models were compared using F! Macro Average Parameter which is shown below. <br/>
<br/>
![Algs](https://user-images.githubusercontent.com/67742339/144507093-f668cbe8-2109-4337-b201-b76d0d195dd5.PNG) <br/>
Three models with the highest F1 Macro Average Score will be used for the next step. <br/>
<br/>
Those three models, which are LGBM Classifier, CatBoost Classifier and XGB Classifier, will proceed with the feature importance technique. Here is example of feature importance selection on LGBM Cassifier. <br/>
![fimportance](https://user-images.githubusercontent.com/67742339/144508660-cd1053ef-0920-4148-bfc1-3a339cc6117e.png) <br/>
<br/>
LGBM Classifer will proceed with 20 features, CatBoost Classifier will proceed with 15 features and XGB Classfier will procedd with 15 features.
After that, we used Soft Voting Classifier with those three classfier as the final model of this modelling. <br/>
The Performance of the final model, based on data test, is show below. <br/>
![Hard Vote sanbercode](https://user-images.githubusercontent.com/67742339/144508589-8f973f56-50a1-4d36-96ce-ed1a737eb8e6.png)
