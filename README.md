# Detect-and-Remove-Outliers

## Introduction
In statistics, an outlier is an observation point that is distant from other observations
In this repository, will be showed how to detect and remove outliers from your data, using pandas and numpy in python. I would like to provide 3 methods in this post, solution based on "z score" ,solution based on "IQR",Solution based on Percentile, Also have included a solution based on mean function.
Also have plotted the corresponding distribution of dataframe at each methods .
Created a Correlation Heatmap and scatter plot for all the numerical columns exist in the data.
Something important when dealing with outliers is that one should try to use estimators as robust as possible. The mean of a distribution will be biased by outliers but e.g. the median will be much less.

## The Z-score 
Is the signed number of standard deviations by which the value of an observation or data point is above the mean value of what is being observed or measured.
upper limit = mean+3*standard deviation
lower limit = mean-3*standard deviation
Are used to detect the outliers

## IQR score 
The interquartile range (IQR), also called the midspread or middle 50%, or technically H-spread, is a measure of statistical dispersion, being equal to the difference between 75th and 25th percentiles, or between upper and lower quartiles, IQR = Q3 − Q1.In other words, the IQR is the first quartile subtracted from the third quartile; these quartiles can be clearly seen on a box plot on the data.It is a measure of the dispersion similar to standard deviation or variance, but is much more robust against outliers.
Here we use the upper limit=Q3+1.5*IQR and 
                lower limit=Q1-1.5*IQR

## Percentile
upper limit=dataframe.quantile(0.95)

lower limit=dataframe.quantile(0.05)

Also can use 99% and 1% as the upper and lower quantile.
## Methods to remove Outliers
1. Trimming: It is a method of deleting the rows that are considered to be the outliers
2. Capping: Not deleting any data from dataset , instead keeping away from the distribution.
            In this technique called “outlier detection,” we cap our data to set limits.


### To find the Numerical columns from the dataset
#finding the numerical columns
#checking the dataset and selecting the numerical columns
numerical_columns=df.select_dtypes(include=['int', 'float']).columns
numerical_columns
