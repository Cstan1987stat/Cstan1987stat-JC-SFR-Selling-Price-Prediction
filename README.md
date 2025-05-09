# Johnson County Property Price Prediction

## Project Overivew

This project involves analyzing data from **[Redfin](https://www.redfin.com/?msockid=0ef39837a8b466032ea88d6aa93a6711)** for Johnson County houses, using Power Query to merge the data for different zip codes, and utilzing different machine learning models to predict the selling prices. 

**Completed Work**
* **[Initial Notebook](https://github.com/Cstan1987stat/Cstan1987stat-JC-SFR-Selling-Price-Prediction/blob/main/notebooks/inital%20notebook.ipynb)** -> Code used for property format column headers, removing unnesesary features, handling missing values, analyzing target variable (Selling Price) distribution, analyzing numerical predictor features, analyzing categorical predictor variables, one-hot encoding categorical features, and splitting up our data into a training and testing set.
* **[Finding Three Methods](https://github.com/Cstan1987stat/Cstan1987stat-JC-SFR-Selling-Price-Prediction/blob/main/notebooks/finding_three_methods.ipynb)** -> Code used to fit Linear Regression, Support Vector Machine, Decision Tree, Random Forest, AdaBoost, and Gradient Boosting machine learning models using Scikit-Learn. First run through was with no transformations besides the previous one-hot encoding, second run through was with the predictor variable being logarithmically transformed and standard scaled, and third run through was same as the second run through but with the target variable being logartihmically transformed aswell. After analyzing the r-squared and mean absolute error for every model on the training data, it was determined that Support Vector Machine, Random Forest, and Gradient Boost would be the three models to be further explored.
* **[SVR](https://github.com/Cstan1987stat/Cstan1987stat-JC-SFR-Selling-Price-Prediction/blob/main/notebooks/svr.ipynb)** Code used to build and explore Support Vector Machine Regressors. Explored the impact the regularization paramter C, differning kernel parameters, and epsilon parameters had on the mean absolute error.
   * Lower values of C decreased error up to a certain point, then increased the error.
   * RBF kernel has the lowest error.
   * Epsilon lead to higher errors as it was increased.
A crude function was defined to find the best combination of C, kernel, and epsilon (which resulted in a best testing error of 71541 (prediction were off by using C=2.1, epsilon = 0.06, and kernel = rbf). 

* ****
