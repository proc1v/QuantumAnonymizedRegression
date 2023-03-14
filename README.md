# Predictive Modeling for Internship Task

This project aims to build a predictive model to predict a target variable based on 53 anonymized features. The model is evaluated using RMSE as the performance metric.

First I conducted descriptive analysis, found that features of the test data are the same as features of the training data, all features are either float64 or int64 type and there are no missing values.
There are groups of features that are having approximately the same distribution, some аeatures have a big variance, negative kurtosis indicates that the data is less outlier-prone than the normal distribution

Then build histplot and scatterplot of features and target. The majority of the features is approximately uniformly distributed, Feature 6 exhibits a larger variance and more extreme values compared to the mean,
feature 8 is categorical and there are no outliers.

From scatter plot it is evident that there is a quadratic relationship between feature 6 and the target feature.

Conducting correlation analysis found that there is very strong linear dependance between feature 6 squared and target and there are no linear correlations between other numerical features

Counducted anova and t-test found high correlation between feature 6 and 8. Should consider to not end up with multicollinearity

Then I preprocessed data using standart scaler and trained linear regression. Achived good metric (RMSE: 2.2e-15), then looked for feature importance and found that as expected feature 6 squared has a very big importance. Also eature 7 has a very little impact on prediction. I will use these 2 features for Regression. I trained LinearRegression, Lasso, Ridge and DecisionTreeRegressor using cross validation. LinearRegression showed best results