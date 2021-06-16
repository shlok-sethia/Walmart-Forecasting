# Walmart-Forecasting

# Predicting-Walmart-Sales---LGBM

This code is part of the kaggle competition "M5-Accuracy". Our team got the score that would put us within the top 200 teams among over 5500 teams getting us the silver medal (But didn't because a team member shared a kernel with his friend or secondary account and we got disqualified :(  )

Data: https://www.kaggle.com/c/m5-forecasting-accuracy/data (Too big for Github)

The notebooks are based on https://www.kaggle.com/kyakovlev/m5-three-shades-of-dark-darker-magic

# My contributions which drastically improved the accuracy:
# 1
I added new features which took certain events (like chirstmas and father's day) into account while predicting sales in previous days as well and not just the
day of the event. This was purely based on the logic that people shop for events not on the day of the event but before the event. This thinking gave us a very good prediction accuracy. (The new added features are present in the Features-1 file.)

# 2
Furthermore fine tuned the parameters to ensure that the model wasn't overfitting. (The tuned params are present in the Train-model kernel.)

# Execution:
1. Run the Features-1 kernel (Generates pkl files for the features created)
2. Run the Features-2 kernel (Uses the pkl files and uses it to create more lag based features and stores in pkl files)
3. Run the Features-3 kernel (Creates some custom features)
4. Run the Train-Model kernel (Uses the pkl files as data input to train LGBM model on the features in them. The hyperparameters are optimized. Generates the submission file which has the predictions of sales for next 28 days)

# Necessary software: 
1. Jupyter notebooks
