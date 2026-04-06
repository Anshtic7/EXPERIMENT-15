**NAME: ANSH PRATAP SINGH**

**PRN: 25070123143**

**AIM: To study and implement different data preprocessing techniques such as normalization (Min-Max normalization, Z-score normalization, and Decimal Scaling) and categorical data encoding methods (Label Encoding and One-Hot Encoding) using Python libraries like Pandas, NumPy, and Scikit-learn for preparing datasets for machine learning and data analysis.**

-------------------------------------------------------------------------------------------------------------------------------------------------------------------

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

--> Handles outliers better than Min-Max scaling

--> Useful in statistical analysis

--> Makes data centered around the mean

5. Decimal Scaling Normalization

Decimal scaling normalizes data by dividing values by a power of 10 so that the maximum value becomes less than 1.

Formula: X(norm) = X/10^j

Where:

X = original value

j = smallest integer such that max(|X(norm)|)<1

Advantages:

-->Simple technique

-->Useful when dealing with large numerical values

6. Categorical Data Encoding

Many datasets contain categorical variables such as gender, city, department, and payment method. Machine learning algorithms require numerical input, so categorical data must be converted into numerical form.

This process is called categorical encoding.

Two encoding techniques used in the experiment are:

i) Label Encoding

ii) One-Hot Encoding

7. Label Encoding: It converts categorical values into numerical labels.

Advantages: 

-->Simple and efficient

-->Works well for ordinal data (data with natural order)

Disadvantage: The model may assume an incorrect order between categories.

8. One-Hot Encoding: One-Hot Encoding converts categorical variables into multiple binary columns.

Advantages: 

-->Prevents the model from assuming ordinal relationships

-->Works well with most machine learning algorithms

Disadvantage: Increases dataset dimensionality when categories are many

9. Dummy Variable Encoding

Dummy encoding is a variation of One-Hot Encoding where one category column is dropped.

This avoids the dummy variable trap, which occurs when features become highly correlated.

-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------

**Conclusion**

The experiment demonstrated the importance of data preprocessing techniques in preparing datasets for data analysis and machine learning. Different normalization methods such as Min-Max normalization, Z-score normalization, and Decimal Scaling were applied to scale numerical data into comparable ranges. Additionally, categorical data encoding techniques like Label Encoding and One-Hot Encoding were implemented to convert non-numerical data into numerical form. Using Python libraries such as Pandas, NumPy, and Scikit-learn, the dataset was successfully transformed into a structured and machine-readable format, making it suitable for further analysis and model building.
