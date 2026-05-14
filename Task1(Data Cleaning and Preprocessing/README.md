Data Cleaning and Preprocessing using Amazon Dataset
## Overview

This project focuses on Data Cleaning and Preprocessing using the Amazon dataset.
The main objective is to prepare raw data for analysis by handling missing values, removing duplicates, correcting inconsistent data, and converting data into a clean and structured format.

Data preprocessing is one of the most important steps in Data Science and Machine Learning because real-world datasets often contain incomplete, noisy, or inconsistent information.

## Dataset Used
Dataset Name: Amazon Dataset
Format: CSV
File Used: amazon.csv

The dataset contains product-related information such as:

Product Name
Category
Ratings
Reviews
Prices
Discount Information

## Objectives
The following preprocessing tasks were performed:

Handling Missing Values
Removing Duplicate Records
Cleaning Inconsistent Data
Converting Data Types
Formatting Columns Properly
Preparing Data for Analysis

## Technologies Used
Python
Google Colab
Pandas
NumPy

## Steps Performed
1. Importing Libraries

Required Python libraries were imported for data handling and preprocessing.

import pandas as pd
import numpy as np

2. Loading the Dataset
df = pd.read_csv('/content/amazon.csv')

3. Checking Dataset Information
df.head()
df.info()
df.describe()

This helped in understanding:

Number of rows and columns
Data types
Missing values
Statistical summary

4. Handling Missing Values
df.isnull().sum()

Missing values were handled using:

Filling values
Removing rows/columns where necessary

Example:

df.fillna(method='ffill', inplace=True)
5. Removing Duplicate Data
df.drop_duplicates(inplace=True)

Duplicate rows were removed to improve data quality.

6. Cleaning Inconsistent Data

Special characters like commas and currency symbols were removed from price columns.

Example:
df['discounted_price'] = df['discounted_price'].replace('[₹,]', '', regex=True)

7. Converting Data Types
df['discounted_price'] = df['discounted_price'].astype(float)
Columns were converted into proper numeric formats for analysis.

8. Final Cleaned Dataset
After preprocessing:

Missing values were handled
Duplicate records were removed
Data became consistent and analysis-ready

## Output
The cleaned dataset can now be used for:

Data Analysis
Visualization
Machine Learning
Business Insights

## Conclusion
This project demonstrates how raw data can be transformed into a clean and structured dataset through preprocessing techniques. Proper data cleaning improves the accuracy and reliability of future analysis and machine learning models.

## Author

Kadambini Behera
