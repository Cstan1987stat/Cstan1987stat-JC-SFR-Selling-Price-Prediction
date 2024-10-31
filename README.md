# Cstan1987stat-JC-SFR-Selling-Price-Prediction

## Update on October 31, 2024.

I’ve uploaded all three notebooks where I explored building Support Vector Regressors, Random Forest Regressors, and Gradient Boosting Regressors. The Support Vector Regressor notebook (svr.ipynb) is the one I’m most proud of, as I invested substantial time in commenting each line of code and creating clear markdown sections to explain the process. By the time I reached the Random Forest Regressor notebook (random forest.ipynb), the commenting and markdown process felt monotonous, so I focused primarily on tuning the model for optimal performance. Using Scikit-learn’s Randomized Search, I aimed to narrow down the best parameter combinations to minimize the MAE on the test data. Unfortunately, the MAE remained around 70,000, with evident overfitting.

Expecting the Gradient Boosting Regressor (gradient boost.ipynb) to yield better results, I moved on to that model. However, overfitting issues persisted, and my attempts to mitigate them were unsuccessful. I was able to reduce the MAE to 65,000 by lowering dimensionality, but it became clear that the project might not yield the results I had hoped for. I plan to create a final notebook to test different transformations, interaction terms, and squared terms to aim for a lower MAE.

Currently, the target variable is logarithmically transformed. The predictor variables pass through a pipeline that applies a logarithmic transformation followed by standard scaling.
