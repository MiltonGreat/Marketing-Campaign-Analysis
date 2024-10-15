# Marketing Campaign Analysis and Customer Segmentation

This project performs an in-depth analysis of a marketing campaign to evaluate its effectiveness, determine the Return on Investment (ROI), and segment customers based on their responsiveness and behavior.

## Table of Contents
- [Overview](#overview)
- [Dataset](#dataset)
- [Objectives](#objectives)
- [Key Features](#key-features)
- [Project Workflow](#project-workflow)
  - [Data Preprocessing](#data-preprocessing)
  - [Feature Engineering](#feature-engineering)
  - [Customer Segmentation](#customer-segmentation)
  - [Campaign ROI Analysis](#campaign-roi-analysis)
  - [A/B Testing](#ab-testing)
- [Model Training and Evaluation](#model-training-and-evaluation)
- [Insights](#insights)
- [Results](#results)
- [Usage](#usage)
- [License](#license)

## Overview

This project involves analyzing the effectiveness of a marketing campaign by calculating ROI, segmenting customers based on responsiveness, and evaluating campaign conversion rates across various demographic groups. In addition, clustering and RFM (Recency, Frequency, Monetary) analysis is used to categorize customers into different segments for more targeted marketing efforts.

## Dataset

The dataset used in this project contains customer information, their responses to marketing campaigns, and transactional data, including:
- **Customer demographics** (age, education, job, etc.)
- **Campaign interactions** (number of contacts, results, offers received)
- **Financial details** (total spending, promotional costs, etc.)
- **Campaign response** (converted or not)

## Objectives

- **Analyze the overall performance of the marketing campaign**
- **Calculate the ROI of the campaign**
- **Segment customers based on their responsiveness**
- **Apply customer segmentation using clustering techniques (KMeans, RFM)**
- **Perform A/B testing to assess the effectiveness of changes in the campaign**

## Key Features

1. **Campaign cost analysis**: Calculate total campaign cost and revenue generated.
2. **Customer segmentation**: Use KMeans clustering, RFM analysis, and demographic features to segment customers.
3. **Conversion analysis**: Analyze conversion rates based on different features like age, job type, education, and day of the week.
4. **A/B Testing**: Compare customer responses between control and treatment groups to assess the impact of campaign changes.

## Project Workflow

### Data Preprocessing
- **Data loading**: Load the marketing campaign data from a ZIP file and inspect the structure of the dataset.
- **Data cleaning**: Handle missing values, remove duplicates, and create derived metrics (total campaign spend, customer conversion indicators, engagement metrics).
- **Feature encoding**: Binary columns are converted to numerical format, and categorical variables are encoded.

### Feature Engineering
- **Campaign spend and revenue metrics**: Calculate total campaign cost, total revenue generated from converted customers, and derive the ROI.
- **Customer interaction frequency**: Calculate how frequently each customer interacted with the campaign.
- **Responsiveness categories**: Classify customers as "Highly Responsive," "Moderately Responsive," or "Non-Responsive" based on their conversion and spending behavior.

### Customer Segmentation
- **KMeans clustering**: Use KMeans to segment customers based on features like total spending, interaction frequency, and campaign duration.
- **RFM Analysis**: Calculate Recency, Frequency, and Monetary value (RFM) for each customer and segment them into groups such as "Top Customers," "High Value," "Medium Value," and "Low Value."
  
### Campaign ROI Analysis
- **Calculate the ROI**: Compare the total revenue generated from the campaign with the total campaign costs.
- **Conversion analysis**: Calculate conversion rates by demographic groups, campaign features, and responsiveness categories.

### A/B Testing
- **Control vs Treatment**: Split customers into control and treatment groups, apply changes (e.g., increased discount for the treatment group), and compare conversion rates and average spend.
- **Statistical tests**: Use t-tests and chi-square tests to assess the statistical significance of the differences in conversion rates and average revenue.

## Model Training and Evaluation

- **Machine learning models**: Logistic Regression, Random Forest Classifier, and Gradient Boosting Classifier are used to predict customer conversions.
- **Class imbalance**: SMOTE is applied to handle class imbalance, improving recall for predicting positive conversions.
- **Hyperparameter tuning**: GridSearchCV is used to tune hyperparameters for Random Forest.

### Evaluation Metrics
- **Accuracy**, **Precision**, **Recall**, **F1-Score**, **ROC-AUC Score**: These metrics are used to evaluate the performance of the classification models.

## Insights

### Campaign Performance
- **ROI**: The campaign incurred a loss with an ROI of **-80.93%**, indicating that the campaign cost exceeded the revenue generated.
- **Customer Segmentation**: The largest segment consists of "Non-Responsive" customers, followed by smaller groups of "Moderately Responsive" and "Highly Responsive" customers.
- **RFM Segmentation**: Customers classified as "Top Customers" had a higher conversion rate than other segments.

### A/B Testing Insights
- **Control vs Treatment**: No statistically significant difference was found in average revenue or conversion rates between the control and treatment groups.
- **Demographic Analysis**: Conversion rates were highest among **students**, **retired individuals**, and the **18-24 age group**.

## Results

- **Best Model**: After applying SMOTE, the Random Forest model achieved a recall of **0.81** for predicting conversions, but the precision remains low.
- **Customer Clusters**: Three distinct clusters were identified using KMeans, with Cluster 2 showing the highest conversion rate (6.46%).

### Part 2: Code Explanation and Insights

#### Code Overview:
The provided code is designed to:
1. **Load and preprocess data**: It cleans the dataset, handles missing values, and generates derived features like total campaign spend, customer conversion status, and engagement metrics.
2. **Customer segmentation**:
   - **KMeans Clustering**: Customers are segmented based on their spending and interaction frequency using KMeans clustering.
   - **RFM Analysis**: Recency, Frequency, and Monetary (RFM) values are calculated to segment customers into groups such as "Top Customers" and "Low Value."
3. **Campaign ROI analysis**: The total campaign cost and revenue are calculated to determine the ROI.
4. **A/B Testing**: Customers are randomly assigned to control and treatment groups to test changes in campaign strategies (e.g., higher discounts), with statistical tests (t-test, chi-square) performed to assess significance.
5. **Model training**: Machine learning models (Logistic Regression, Random Forest, Gradient Boosting) are used to predict customer conversions.
6. **Model evaluation**: Various metrics such as accuracy, recall, and ROC-AUC score are used to evaluate the models, with SMOTE applied to handle class imbalance.
7. **Visualization and feature importance**: Feature importance from the Random Forest model is visualized, and key metrics like conversion rates by demographic groups and RFM segments are plotted.

#### Key Insights from the Output:
1. **ROI Analysis**: The campaign resulted in an ROI of **-80.93%**, which indicates that the cost far exceeded the revenue generated.
2. **Customer Responsiveness**:
   - The majority of customers (13,257) were classified as **Non-Responsive**, meaning they did not convert during the campaign.
   - **Highly Responsive** customers represent a small portion (133), making them valuable for targeted marketing.
3. **RFM and KMeans Clustering**:
   - **RFM Segmentation**: The "Top Customers" group had a conversion rate of **5.56%**, making them the most valuable segment.
   - **KMeans Clustering**: Cluster 2 had the highest conversion rate of **6.46%**.
4. **A/B Testing Results**:
   - No statistically significant difference was found between the **control** and **treatment** groups in terms of revenue or conversion rate, suggesting that the changes in campaign strategy (e.g., increasing discounts) did not significantly impact performance.
5. **Conversion Rate by Demographics**:
   - **Students** and **retired individuals** had the highest conversion rates, and campaigns targeted toward these demographics may yield better results.
   - Conversion rates were also highest on **Tuesdays** and **Wednesdays**, suggesting that these days may be optimal for future campaigns.

## Source

https://www.kaggle.com/datasets/khanimar/marketing-campaign-analysis-data
