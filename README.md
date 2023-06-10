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
   ![download](https://github.com/pras-ops/Black_Friday_Sales_Analysis/assets/56476064/7e98c952-7ab1-462a-b33f-6084d7af2d3f)
-   Barplot of Gender and Marital_Status: Compares the gender and marital status.
   ![download](https://github.com/pras-ops/Black_Friday_Sales_Analysis/assets/56476064/6e4e1919-659d-4c74-a138-db3a1816405a)
-   Barplot of Gender and Purchase: Compares the gender and purchase amounts.
    ![download](https://github.com/pras-ops/Black_Friday_Sales_Analysis/assets/56476064/e16224e8-470f-4b60-9a91-a0fffb699dcf)
-   Barplot of Occupation and Purchase: Shows the effect of occupation on purchases.
   ![download](https://github.com/pras-ops/Black_Friday_Sales_Analysis/assets/56476064/9a0aabce-5b04-4944-874b-29975e689c95)
-   Barplot of Occupation, Gender, and Purchase: Shows the gender-specific purchases in different occupations.
   ![download](https://github.com/pras-ops/Black_Friday_Sales_Analysis/assets/56476064/5cbec06d-97a9-486d-a7b1-ed24be52c7f4)

## Outlier Detection

Outliers can significantly impact the performance of machine learning models. The presence of outliers has been checked using boxplots for the following variables:

-   Gender and Purchase
![download](https://github.com/pras-ops/Black_Friday_Sales_Analysis/assets/56476064/9f386348-a14a-42c8-a519-ece0a9c9cdae)
-   Occupation and Purchase
![download](https://github.com/pras-ops/Black_Friday_Sales_Analysis/assets/56476064/b51212e4-d954-414f-bbb8-dd6f9a3a4679)
-   Age and Purchase
![download](https://github.com/pras-ops/Black_Friday_Sales_Analysis/assets/56476064/ab285814-59d2-45ab-b4f5-b9ee0a9e093a)
-   Product_Category_1 and Purchase
![download](https://github.com/pras-ops/Black_Friday_Sales_Analysis/assets/56476064/887a9b67-250e-4d4b-88b5-d594ae2bde16)

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
