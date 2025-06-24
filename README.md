# Employee-Analysis

This project performs exploratory data analysis (EDA) and data cleaning on an "Employee Sample Data" dataset. The goal is to understand the structure, characteristics, and potential issues within the employee data, and to prepare it for further analysis or modeling.

Project Structure
The core of this project is a Colab notebook (employee.ipynb) which contains the Python code for data loading, exploration, and cleaning.

Dataset
The analysis is performed on the Employee Sample Data file.csv dataset. This file is expected to be present in the same directory as the Colab notebook.

Key Tasks Performed
1. Data Loading
Loads the Employee Sample Data file.csv into a pandas DataFrame.

Includes robust error handling for FileNotFoundError, pd.errors.ParserError, and general exceptions, including specific handling for decoding errors (using latin-1 encoding if utf-8 fails).

Displays the first 5 rows of the loaded DataFrame.

2. Data Exploration
This section provides a comprehensive overview of the dataset, including:

Data Shape and Info: Displays the dimensions of the DataFrame and a summary of its columns, including non-null counts and data types.

Summary Statistics: Provides descriptive statistics for both numerical and categorical columns.

Missing Values: Identifies and quantifies missing values for each column.

Unique Values: Counts the number of unique entries in each column.

Data Distribution (Numerical): Describes the distribution of numerical features like 'Age' and 'Annual Salary'.

Data Distribution (Categorical): Shows the value counts for categorical features such as 'Job Title', 'Department', 'Country', 'Gender', and 'Ethnicity'.

Correlation Analysis: Attempts to calculate correlations between numerical features (if enough are present).

3. Data Cleaning
This section focuses on preparing the data for analysis by addressing common data quality issues:

Handling Missing Values in 'Exit Date':

Creates a new binary column Has Left Company (1 if an 'Exit Date' exists, 0 otherwise).

Drops the original 'Exit Date' column.

Data Type Conversion:

Converts 'Annual Salary' and 'Bonus %' columns to numeric types.

Removes non-numeric characters (e.g., '$', '%') before conversion.

Coerces errors during conversion, replacing unconvertible values with NaN.

Imputes any remaining missing values in these columns with their respective medians.

Outlier Detection and Handling:

(Details not fully provided in the snippet, but typically involves using IQR method for 'Annual Salary' and 'Bonus %' to identify and manage outliers.)

Duplicate Removal:

(Details not fully provided in the snippet, but typically involves checking for and removing duplicate rows.)

How to Run the Project
Download the Dataset: Ensure you have the Employee Sample Data file.csv file.

Open in Google Colab: Upload the employee.ipynb notebook to Google Colab.

Upload Data: Upload the Employee Sample Data file.csv file to your Colab environment.

Run Cells: Execute the cells sequentially in the Colab notebook.

Requirements
Python 3.x

pandas library (pip install pandas)

numpy library (pip install numpy)

Author
Raji Ibrahim Aduragbemi

