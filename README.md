
# Table of Contents

1.  [About](#org2a87731)
2.  [Contributors](#orgce798db)
3.  [Problem Statement](#org34f4af0)
4.  [Cleaning Data](#org1606021)
5.  [Machine Learning Models](#org587dfc8)
    1.  [Multi-Variate Linear Regression](#org3c3ada8)
    2.  [XGBoost Model](#org91ed319)
6.  [What did we learn](#org0433684)
7.  [Conclusion](#org0c40dee)
8.  [References](#orgd54d041)



<a id="org2a87731"></a>

# About

This repository is a Mini-Project which focuses on the Life Expectancy. The data set is obtained from [Kaggle](https://www.kaggle.com/datasets/kumarajarshi/life-expectancy-who). The data reflect every country's factors affecting life expectancy, from a period of 2000 to 2015. The original source of this data set is obtained from the data repository under World Health Organization (WHO). A video about this project is on [Youtube](https://www.youtube.com/watch?v=2V4sDu2Z7EA).  


<a id="orgce798db"></a>

# Contributors

-   [Jeremy](https://github.com/iiJoe) (Data Preparation, Data Cleaning, Model Building, Feature Selection, Cross Validation)
-   [Rhys](https://github.com/Restia-Ashdoll) (Data Preparation, Data Cleaning, Exploratory Data Analysis, Model Building, Visualization)
-   [Cheng](https://github.com/Worsl) (Data Preparation, Problem formulation, Conclusion, Insights, Model Building, Presentation)


<a id="org34f4af0"></a>

# Problem Statement

Life Expectancy is a key metric for assessing a country's population health. We would like to seek to improve the overall populations health of a given country. As such, we want to figure out what are the most significant factors that impact life expectancy and to build a model that would be able to predict life expectancy.  


<a id="org1606021"></a>

# Cleaning Data

We decided to fill null values with the median values of the corresponding column, and rows with outliers (< Q1 - 1.5 \* IQR or > Q3 + 1.5 \* IQR) are omitted.  


<a id="org587dfc8"></a>

# Machine Learning Models

**Note:** The plotly graphs may not show &#x2013; the whole notebook may need to be run first  


<a id="org3c3ada8"></a>

## Multi-Variate Linear Regression

We used a 75:25 split on the data into the training data set and test data set respectively. We built the model based on the training set and applied the model to predict on the test data set.  


<a id="org91ed319"></a>

## XGBoost Model

In an attempt to improve our model, we used feature selection to narrow down the predictors and cross validation. We passed the XGB model as an estimator to GridSearchCV which would compute the best combination of hyperparameters for our model.  


<a id="org0433684"></a>

# What did we learn

-   Plotly (Visualization tool)
-   Feature Selection
-   Cross Validation


<a id="org0c40dee"></a>

# Conclusion

We managed to find the more significant factors and built accurate models to predict life expectancy. One interesting thing was that schooling, or in other words, the amount of education received by individuals turned out to be a more significant factor compared to vaccinations and immunisations. Countries should focus more on the key factors identified to improve the life expectancy of citizens, increasing the overall population health of the country.  


<a id="orgd54d041"></a>

# References

-   <https://plotly.com/python/>
-   <https://www.kaggle.com/datasets/kumarajarshi/life-expectancy-who>
-   <https://machinelearningmastery.com/feature-selection-for-regression-data/>
-   <https://scikit-learn.org/stable/modules/feature_selection.html>
-   <https://xgboost.readthedocs.io/en/stable/tutorials/model.html>
-   <https://scikit-learn.org/stable/modules/generated/sklearn.model_selection.GridSearchCV.html>

