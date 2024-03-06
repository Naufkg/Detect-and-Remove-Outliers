# Detect-and-Remove-Outliers
[Dataset Used](https://drive.google.com/file/d/1UlWRYU0UglE2ex3iFse0J6eCLEU8g98P/view?usp=sharing)

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


# Hypothesis Testing

Hypothesis testing is a statistical method used to make inferences about a population parameter based on sample data. It involves the formulation of two competing hypotheses: the null hypothesis (H0) and the alternative hypothesis (H1 or Ha). The null hypothesis typically represents the status quo or a statement of no effect, while the alternative hypothesis represents the opposite.

1. Formulating Hypotheses: Define the null hypothesis (H0) and the alternative hypothesis (H1). These hypotheses should be mutually exclusive and exhaustive.

2. Choosing a Significance Level: Select the level of significance (alpha, usually denoted as α), which represents the probability of rejecting the null hypothesis when it is true. Common choices for α include 
   0.05 and 0.01.

3. Collecting Data: Obtain a sample from the population of interest.

4. Calculating Test Statistic: Calculate a test statistic based on the sample data and the assumptions of the null hypothesis.

5. Determining the Critical Region: Determine the critical region of the test statistic, which represents extreme values that would lead to rejection of the null hypothesis.

6. Making a Decision: Compare the calculated test statistic to the critical values. If the test statistic falls within the critical region, reject the null hypothesis in favor of the alternative hypothesis. If it does not fall within the critical region, fail to reject the null hypothesis.

7. Drawing Conclusion: Based on the decision in step 6, draw a conclusion about the population parameter of interest.

   
 ## Hypothesis tests used here:
   1. Z-test:Used for testing hypotheses about population mean when the population standard deviation is known.
   2. t-test: Similar to the Z-test but used when the population standard deviation is unknown and estimated from the sample.


# Data Preprocessing

[Dataset Used](https://drive.google.com/file/d/1F3lRf32JM8ejnXq-Cbf9y7fa57zSHGz_/view?usp=sharing)

Objective:
 The main objective of this project is to design and implement a robust data preprocessing system that addresses common challenges such as missing values, outliers, inconsistent formatting, and noise. By performing effective data preprocessing, the project aims to enhance the quality, reliability, and usefulness of the data for machine learning.
 
In the real world, we usually come across lots of raw data, which are especially sensitive to noisy, missing, and inconsistent  since it originates from various sources with different characteristics

1. Raw data - real-world data, such as text, pictures, and videos etc.

2. Low-quality data will yield low-quality data mining outcomes

3. Data mining is a process for extracting knowledge and useful patterns from vast volumes of data

### What steps should be taken in order to improve the data's quality?

Data preprocessing is the most important step in the data mining process and has a significant impact on the precision and effectiveness of the output

Data preprocessing is an approach of converting the raw data into a clean data set

Data pre-processing

Data preprocessing is the process of converting raw data into a format that is understandable and readable for a machine learning model.

### Importand steps of Data Preprocessing
1.Acquire the dataset
2.Importing libraries
3.Importing datasets
4.Finding Missing Data
5.Encoding Categorical Data
6.Splitting the dataset
7.Feature scaling


### The main Python libraries used for data preprocessing in machine learning are:

 NumPy
 Matplotlib
 Pandas



# Linear Regression
Linear regression is a statistical modeling technique used to model the relationship between a dependent variable (also called the target or response variable) and one or more independent variables (also called predictors or features). It assumes that the relationship between the variables is linear, meaning that the change in the dependent variable is directly proportional to the change in the independent variables.

### Problem Statement
A Chinese automobile company Geely Auto aspires to enter the US market by setting up their manufacturing unit there and producing cars locally to give competition to their US and European counterparts. They have contracted an automobile consulting company to understand the factors on which the pricing of cars depends. Specifically, they want to understand the factors affecting the pricing of cars in the American market, since those may be very different from the Chinese market. The company wants to know:

Which variables are significant in predicting the price of a car 
How well those variables describe the price of a car 
Based on various market surveys, the consulting firm has gathered a large dataset of different types of cars across the American market. So, put on your seatbelt and get ready for a fun journey. We're about to explore the world of cars, solve mysteries, and have a good laugh along the way! 

### Steps 
Understanding the Problem Statement
Data Checks to Perform
Exploratory Data Analysis
Data Pre-Processing
Model Training
Choose Best Model

We have DataSet > Car Price 
The Shape DataSet = (Rows = 205, columns = 26) 

No null value 

No Duplicated value 
Some Analyst 

Price cars 
Avg price = $13,276 

Min price = $5,118 

Max price = $45,400 

### Analysis
When increasing the number of cylinders, the price tends to increase, though the majority of users stick with 4 cylinders.
As the engine size increases, so does the price.
The wheelbase, car length, and car width have an effect on the price, but the car height doesn't seem to have any significant impact.

the best model Linear Regression  with 87% accuracy.
