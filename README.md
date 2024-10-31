# Marketing Campaign Analysis and Customer Segmentation

This project performs an in-depth analysis of a marketing campaign to evaluate its effectiveness, determine the Return on Investment (ROI), and segment customers based on their responsiveness and behavior.

## Overview

This project involves analyzing the effectiveness of a marketing campaign by calculating ROI, segmenting customers based on responsiveness, and evaluating campaign conversion rates across various demographic groups. In addition, clustering and RFM (Recency, Frequency, Monetary) analysis is used to categorize customers into different segments for more targeted marketing efforts.

## Dataset

The dataset used for this analysis is contained within a ZIP file named Marketing Campaign.zip. The primary dataset is a CSV file named train.csv, which includes various customer features such as:

- id: Unique identifier for each customer
- target: Indicates whether a customer responded to the campaign
- day: Day of the month when the interaction occurred
- month: Month of the interaction
- duration: Duration of the interaction
- contactId: Identifier for the type of contact
- age, gender, job, maritalStatus, education: Demographic features of customers
- accountBalance: Customer's account balance

## Methodology

1. Load the Data: The data is loaded from the ZIP file, and the contents are inspected.

2. Basic Data Exploration: Perform initial data inspection, including checking the first few rows, data types, and descriptive statistics.

3. Data Cleaning:
- Handle missing values.
- Remove negative values from accountBalance.
- Drop duplicate rows.
- Convert data types as necessary.

4. Extract Date Features and Perform RFM Analysis: Calculate RFM metrics and categorize customers based on their behaviors.

5. Summary Statistics: Calculate and display total revenue, average revenue, and unique customer counts.

6. Data Normalization: Normalize RFM data for clustering.

7. KMeans Clustering: Apply KMeans clustering to segment customers and visualize the results.

## Results

RFM Analysis Sample: Provides insight into customer segments based on recency, frequency, and monetary value.

Summary Statistics:
- Total Revenue: 43,293,800
- Average Revenue: 1,502.89
- Number of Unique Customers: 28,807

Normalized RFM Data Sample: Displays normalized values for RFM metrics to prepare for clustering.
