# ETL-for-Stocks
Preprocessing raw features before using the data for analysis.

# Imputation and Standardizarion
When dealing with the raw data, we should decide how to deal with the nan (missing) values, the outliers and think about the data standardization problem. The data you are given includes quarterly feature values for stocks. There are 5 quarters and 100 stocks in each quarter, and every stock has 5 features.

# Winsorizing the data
On a quarterly basis: fill the nan values in feature_1 to feature_5 (5 columns in total) with the median feature value; winsorize the data (after nan value handling) with 2.5th to 
the 97.5th percentile values (i.e. for each feature, set the data below the 2.5th percentile to the 2.5th percentile value; and the data above 97.5th percentile to the 97.5th percentile value); standardize each feature by subtracting the mean and then dividing this net result by the standard deviation (this computation will yield z-score values)

# 3-D final matrix(Output in a pkl file)
The position size for a portfolio manager in a certain stock is the percentage of the market value for this stock out of the total market value held by the portfolio manager. The dataset given is a holding file which includes the stocks the managers hold in each quarter and the market value of each stock.
