# DATA-ANALYTICS-ABOUT-THE-DATASET
# AIM
To perform data analytics on a given dataset using Python and Pandas, understand the characteristics of the dataset, identify different types of data, examine missing values, and prepare the dataset for further analysis and machine learning.

# THEORY
Data analytics is the process of collecting, inspecting, cleaning, and analyzing data to obtain useful information. Python provides several libraries for data analysis, among which Pandas is widely used.

Pandas is a Python library used to handle and analyze structured data. It provides two important data structures: Series and DataFrame.

The dataset can be analyzed using the following operations:
1. Loading the Dataset: Importing the dataset using the Pandas library.
2. Viewing the Data: Displaying the first and last few rows.
3. Dataset Information: Identifying the number of rows, columns, and data types.
4. Statistical Analysis: Finding mean, median, minimum, maximum, and other statistical values.
5. Missing Values: Identifying empty or null values in the dataset.
6. Duplicate Values: Checking whether repeated records are present.
7. Data Cleaning: Removing duplicates and handling missing values to prepare the dataset for further analysis.
# PYTHON CODE
```````

import pandas as pd

# Load the dataset
df = pd.read_csv("dataset.csv")

# Display first five rows
print("First Five Rows:")
print(df.head())

# Display last five rows
print("\nLast Five Rows:")
print(df.tail())

# Display dataset shape
print("\nDataset Shape:")
print(df.shape)

# Display dataset information
print("\nDataset Information:")
df.info()

# Display column names
print("\nColumn Names:")
print(df.columns)

# Display data types
print("\nData Types:")
print(df.dtypes)

# Statistical description
print("\nStatistical Description:")
print(df.describe(include="all"))

# Check missing values
print("\nMissing Values:")
print(df.isnull().sum())

# Check duplicate values
print("\nDuplicate Rows:")
print(df.duplicated().sum())

# Display unique values in each column
print("\nUnique Values:")
for col in df.columns:
    print(col, ":", df[col].nunique())

# Remove duplicate rows
df = df.drop_duplicates()

# Handle missing values
df = df.dropna()

# Display cleaned dataset
print("\nCleaned Dataset:")
print(df.head())

# Save cleaned dataset
df.to_csv("cleaned_dataset.csv", index=False)

print("\nData Analytics Completed Successfully!")

````````````


# RESULT
Thus, data analytics was successfully performed on the given dataset using Python and the Pandas library. The dataset characteristics, number of rows and columns, data types, statistical information, missing values, and duplicate records were identified. The dataset was cleaned and saved for further analysis and machine learning applications.
