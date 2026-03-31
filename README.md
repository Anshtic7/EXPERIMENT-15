**NAME: ANSH PRATAP SINGH**

**PRN: 25070123143**

**AIM: To study and implement different data preprocessing techniques such as normalization (Min-Max normalization, Z-score normalization, and Decimal Scaling) and categorical data encoding methods (Label Encoding and One-Hot Encoding) using Python libraries like Pandas, NumPy, and Scikit-learn for preparing datasets for machine learning and data analysis.**

-----------------------------------------------------------------------------------------------------------------------------------------------------------------------

**THEORY**

1. Data Preprocessing

Data preprocessing is an important step in data analysis and machine learning. Raw data collected from different sources is often incomplete, inconsistent, or not in a suitable format for analysis. Data preprocessing involves transforming raw data into a clean, structured, and usable format so that machine learning algorithms can work efficiently.

The main objectives of data preprocessing are:

-->To improve data quality

-->To remove inconsistencies and noise

-->To transform data into a machine-readable format

-->To improve the performance and accuracy of machine learning models

Common preprocessing techniques include:

-->Data cleaning

-->Data transformation

-->Data normalization

-->Encoding categorical variables

-->Feature scaling


2. Data Normalization

Normalization is a technique used to scale numerical data into a specific range, usually between 0 and 1. It is important because features in a dataset may have different ranges of values, which can affect machine learning algorithms.

Normalization helps in:

-->Faster convergence of algorithms

-->Improved model performance

-->Reduced bias caused by large value features


3. Min-Max Normalization

Min-Max normalization rescales data values to a fixed range, usually 0 to 1.

Formula

X(norm) = X - X(min)/X(max) - X(min)

where: 

X = original value

X(min) = minimum value of the feature

X(max) = maximum value of the feature

Advantages:-

-->Preserves the relationships between original data values

-->Simple and easy to implement

-->Works well when the dataset does not contain extreme outliers

4. Z-Score Normalization (Standardization)

Z-Score normalization converts data into a standard normal distribution with a mean of 0 and standard deviation of 1.

Formula:-

Z = X-U/D

where:

X = original value

U = mean of the feature
Advantages
Handles outliers better than Min-Max scaling
Useful in statistical analysis
Makes data centered around the mean

In the notebook, Units_Sold is standardized using Z-Score normalization.

5. Decimal Scaling Normalization

Decimal scaling normalizes data by dividing values by a power of 10 so that the maximum value becomes less than 1.

Formula
𝑋
𝑛
𝑜
𝑟
𝑚
=
𝑋
10
𝑗
X
norm
	​

=
10
j
X
	​


Where:

𝑋
X = original value
𝑗
j = smallest integer such that 
𝑚
𝑎
𝑥
(
∣
𝑋
𝑛
𝑜
𝑟
𝑚
∣
)
<
1
max(∣X
norm
	​

∣)<1

Example:

If the maximum value of price is 55000, dividing by 100000 scales it to 0.55.

Advantages
Simple technique
Useful when dealing with large numerical values

In the experiment, Price values are normalized using decimal scaling.

6. Categorical Data Encoding

Many datasets contain categorical variables such as gender, city, department, and payment method. Machine learning algorithms require numerical input, so categorical data must be converted into numerical form.

This process is called categorical encoding.

Two encoding techniques used in the experiment are:

Label Encoding
One-Hot Encoding
7. Label Encoding

Label Encoding converts categorical values into numerical labels.

Example:

Gender	Encoded
Male	1
Female	0

Each category is assigned a unique integer value.

Advantages
Simple and efficient
Works well for ordinal data (data with natural order)
Disadvantages
The model may assume an incorrect order between categories

In the experiment, label encoding is applied to:

Customer_Gender
City
Payment_Method
Product_Category
Placement_Status

using LabelEncoder from sklearn.preprocessing.

8. One-Hot Encoding

One-Hot Encoding converts categorical variables into multiple binary columns.

Example:

Payment Method	UPI	Credit Card	Debit Card
UPI	1	0	0
Credit Card	0	1	0

Each category becomes a separate column with values 0 or 1.

Advantages
Prevents the model from assuming ordinal relationships
Works well with most machine learning algorithms
Disadvantage
Increases dataset dimensionality when categories are many

In the notebook, pd.get_dummies() is used to perform One-Hot Encoding.

9. Dummy Variable Encoding

Dummy encoding is a variation of One-Hot Encoding where one category column is dropped.

This avoids the dummy variable trap, which occurs when features become highly correlated.

Example:

If a feature has 4 categories, dummy encoding will create 3 columns instead of 4.

In the notebook, this is done using:

pd.get_dummies(drop_first=True)
10. Real Dataset Implementation

The experiment also applies preprocessing techniques to real datasets such as:

Amazon Products Dataset
Student Dataset

The following preprocessing tasks are performed:

Min-Max normalization for price
Z-Score normalization for units sold
Decimal scaling
Label encoding of placement status
One-hot encoding of department

These steps demonstrate how preprocessing prepares datasets for machine learning models and statistical analysis.
