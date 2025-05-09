# Johnson County Property Price Prediction

## Project Overivew

This project focuses on analyzing data from **[Redfin](https://www.redfin.com/?msockid=0ef39837a8b466032ea88d6aa93a6711)** for residental properties in Johnson County. I used Power Query to merge property data across different zip codes, then applied various machine learning models to predict selling prices.

## Completed Work
* **[Initial Notebook](https://github.com/Cstan1987stat/Cstan1987stat-JC-SFR-Selling-Price-Prediction/blob/main/notebooks/inital%20notebook.ipynb)** -> Code used for formatting column headers, removing unnecessary features, handling missing values, analyzing the distribution of the target variable (selling price), examining numerical and categorical predictors, one-hot encoding categorical variables, and splitting the data into training and testing sets.
* **[Finding Three Methods](https://github.com/Cstan1987stat/Cstan1987stat-JC-SFR-Selling-Price-Prediction/blob/main/notebooks/finding_three_methods.ipynb)** -> Code used to explore multiple models including Linear Regression, Support Vector Machines, Decision Trees, Random Forests, AdaBoost, and Gradient Boosting using scikit-learn. Models were tested under three scenarios: (1) only one-hot encoding, (2) log transformation and standard scaling of predictors, and (3) log transformation of both predictors and target variable. Based on R-squared and Mean Absolute Error (MAE) metrics, Support Vector Machine, Random Forest, and Gradient Boosting were selected for further tuning.
* **[SVR](https://github.com/Cstan1987stat/Cstan1987stat-JC-SFR-Selling-Price-Prediction/blob/main/notebooks/svr.ipynb)** Code that evaluates the impact of different kernels, C, and epsilon values on MAE. The best parameters were C = 2.1, epsilon = 0.06, and kernel = 'rbf', resulting in a test MAE of $71,541.30 and a training MAE of $54,345.34.
* **[Random Forest](https://github.com/Cstan1987stat/Cstan1987stat-JC-SFR-Selling-Price-Prediction/blob/main/notebooks/random%20forest.ipynb)** Code that tunes a Random Forest Regressor by testing combinations of n_estimators, max_depth, min_samples_split, min_samples_leaf, and max_features. The best configuration yielded a test MAE of $70,116.96. However, the training MAE was significantly lower at $35,804.95, indicating overfitting.
* **[Gradient Boost](https://github.com/Cstan1987stat/Cstan1987stat-JC-SFR-Selling-Price-Prediction/blob/main/notebooks/gradient%20boost.ipynb)** Code that uses RandomizedSearchCV to fine-tune a Gradient Boosting Regressor, testing various combinations of hyperparameters. Initially achieved a test MAE of $68,419.62. After applying PCA for dimensionality reduction and using a Random Forest Regressor as the base estimator, the final test MAE improved to $66,375.48. The corresponding training MAE was $24,922.38, again suggesting overfitting.

## Conclusion
This project gave me valuable hands-on experience with data preparation, feature engineering, and machine learning for real-world housing data. Although model performance improved through tuning and dimensionality reduction, the persistent gap between training and testing MAE underscored the real-world impact of overfitting. If I were to approach this project again, I would spend more time in the pre-modeling phase—especially on feature engineering and data exploration—and prioritize gathering a larger dataset, as this project was limited to approximately 1,600 rows.

## Tools Used
* Visual Studio Code
* Python
* Pandas, Numpy, Scikit-Learn
* Microsoft Excel
