#   Black Friday Sales Analysis

This repository contains code and analysis for analyzing and predicting Black Friday sales. The dataset used for this analysis is available in the `train.csv` file.

## Table of Contents

 1.   Data Understanding
 2.   Data Visualization
 3.   Outlier Detection
 4.   Data Preprocessing
 5.   Data Transformation
 6.   Machine Learning
 7.   Predictions

## Introduction

Black Friday is a popular shopping event that occurs after the Thanksgiving holiday in the United States. It is known for its heavy discounts and large sales volumes. In this project, we aim to analyze the Black Friday sales data and predict the purchase amounts using machine learning models.

## Installation

To run the code in this repository, you need to have the following libraries installed:

-   pandas
-   numpy
-   seaborn
-   matplotlib
-   scikit-learn

## Data Understanding

The dataset used for this analysis is stored in the `train.csv` file. It contains the following columns:

-   User_ID
-   Product_ID
-   Gender
-   Age
-   Occupation
-   City_Category
-   Stay_In_Current_City_Years
-   Marital_Status
-   Product_Category_1
-   Product_Category_2
-   Product_Category_3
-   Purchase

The dataset has 550,068 rows and 12 columns. It also contains some missing values, particularly in the `Product_Category_2` and `Product_Category_3` columns.

## Data Visualization

Data visualization is an essential step in understanding the patterns and relationships in the data. The following visualizations have been performed on the dataset:

-   Countplot of Gender: Shows the occurrences of gender in the dataset.
-   Barplot of Gender and Marital_Status: Compares the gender and marital status.
-   Barplot of Gender and Purchase: Compares the gender and purchase amounts.
-   Barplot of Occupation and Purchase: Shows the effect of occupation on purchases.
-   Barplot of Occupation, Gender, and Purchase: Shows the gender-specific purchases in different occupations.

## Outlier Detection

Outliers can significantly impact the performance of machine learning models. The presence of outliers has been checked using boxplots for the following variables:

-   Gender and Purchase
-   Occupation and Purchase
-   Age and Purchase
-   Product_Category_1 and Purchase

The boxplots help identify the presence of outliers in the data.

## Data Preprocessing

Data preprocessing is a crucial step in machine learning. In this project, the following preprocessing steps have been performed:

-   Replacing 'P00' in the Product_ID column and scaling the column using StandardScaler.
-   Dropping the Product_Category_3 column due to a high number of missing values.
-   Imputing missing values in the Product_Category_2 column using the mean value.
-   Encoding categorical variables using LabelEncoder.
-   Changing the values in the Stay_In_Current_City_Years column from '4+' to '4'.
-   Converting the data types of Gender, Age, and Stay_In_Current_City_Years to integer.
-   Changing the data type of City_Category to category.
-   Splitting the data into independent variables (X) and the target variable (Y).

## Data Transformation

To transform skewed data and improve the model's performance, a log transformation has been applied to the Purchase column. This helps approximate the data to a normal distribution.

## Machine Learning

Three machine learning models have been implemented.
