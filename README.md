# Predicting-Walmart-Sales

![Issues](https://img.shields.io/github/issues/shlok-sethia/Walmart-Forecasting)
[![License](https://img.shields.io/github/license/shlok-sethia/Walmart-Forecasting)](https://github.com/shlok-sethia/Walmart-Forecasting/blob/master/LICENSE)
![](https://img.shields.io/github/repo-size/shlok-sethia/Walmart-Forecasting.svg?label=Repo%20size&style=flat-square)&nbsp;

This code is part of the kaggle competition "M5-Accuracy". Our team got the score that would put us within the top 200 teams among over 5500 teams getting us the silver medal (But didn't because a team member shared a kernel with his friend or secondary account and we got disqualified :(  )

Data: https://www.kaggle.com/c/m5-forecasting-accuracy/data (Too big for Github)

# My contributions which drastically improved the accuracy:
# 1.Feature Engineering
I added new features which took certain events (like chirstmas and father's day) into account while predicting sales in previous days as well and not just the
day of the event. This was purely based on the logic that people shop for events not on the day of the event but before the event. This thinking gave us a very good prediction accuracy. (The new added features are present in the Features-1 file.)

# 2. Hyperparameter Tuning
Furthermore fine tuned the parameters to ensure that the model wasn't overfitting. (The tuned params are present in the LGBM_Poisson kernel.)

# Execution:
For the best score achieved:
1. Run the Features-1 kernel (Generates pkl files for the features created)
2. Run the Features-2 kernel (Uses the pkl files and uses it to create more lag based features and stores in pkl files)
3. Run the Features-3 kernel (Creates some custom features)
4. Run the LGBM_Poisson kernel (Uses the pkl files as data input to train LGBM model on the features in them. The hyperparameters are optimized. Generates the submission file which has the predictions of sales for next 28 days)

# Different models built:
1. Linear Regression with One Hot Encoding
2. Decision Tree Regressor
3. Bagging Regressor 
4. XGB Regressor
5. LGBM Poisson (Best performing model)
6. LGBM Tweedie
7. LGBM Regression
8. LGBM Gamma

# Necessary software: 
1. Jupyter notebooks
