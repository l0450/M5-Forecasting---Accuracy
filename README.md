# M5 Forecasting - Accuracy
---------------------------------------------------------------------------------------------
Estimating the unit sales of Walmart retail goods. Here's the link to check out the entire overview of this project: [text](https://www.kaggle.com/competitions/m5-forecasting-accuracy/overview)
---------------------------------------------------------------------------------------------
## Objectives ##

The objective of the M5 forecasting competition is to advance the theory and practice of forecasting by identifying the method(s) that provide the most accurate point forecasts for each of the 42,840 time series of the competition. I addition, to elicit information to estimate the uncertainty distribution of the realized values of these series as precisely as possible. To that end, the participants of M5 are asked to provide 28 days ahead point forecasts (PFs) for all the series of the competition, as well as the corresponding median and 50%, 67%, 95%, and 99% prediction intervals (PIs). The M5 differs from the previous four ones in five important ways, some of them suggested by thediscussants of the M41 competition, as follows:

- First, it uses grouped unit sales data, starting at the product-store level and being aggregated to that of product departments, product categories, stores, and three geographical areas: the States of California (CA), Texas (TX), and Wisconsin (WI).
- Second, besides the time series data, it includes explanatory variables such as sell prices, promotions, days of the week, and special events (e.g. Super Bowl, Valentine’s Day, and Orthodox Easter) that typically affect unit sales and could improve forecasting accuracy.
- Third, in addition to point forecasts, it assesses the distribution of uncertainty, as the participants are asked to provide information on nine indicative quantiles.
- Fourth, instead of having a single competition to estimate both the point forecasts and the
uncertainty distribution, there will be two parallel tracks using the same dataset, the first
requiring 28 days ahead point forecasts and the second 28 days ahead probabilistic forecasts for the median and four prediction intervals (50%, 67%, 95%, and 99%).
- Fifth, for the first time it focuses on series that display intermittency, i.e., sporadic demand including zeros.

## Approach ##

I have started on EDA (Exploratory Data Analysis) based on the data provided by Kaggle. For this reason I created this notebook below.

### exploration.ipynb ###

In this notebook I described all the exploratory data analysis done on data and prepration/combining of data provided in Kaggle for further processing. In this file we have several information on how sales are varying according to state, category, department etc.

### featureengineering.ipynb ###

This Notebook describes all feature engineering I have done on the data. We have various time series and date related done feature engineering in this notebook.

### modelling.ipynb ###

On this exact notebook you can find 2 machine learning models used for sales forecasting. Here I have shown the result by both custom implementation of WRMSSE on test and cross validation data.
The ML models I have used are: LSTM and CNN-LSTM NN (both with no date features).
