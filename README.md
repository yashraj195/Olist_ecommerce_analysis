# Predictive Delivery Risk System for Brazilian E-commerce

## Project Overview

### This project leverages machine learning to build a Predictive Delivery Risk System using the Olist Brazilian E-commerce dataset. The primary goal is to predict the probability of a delivery being delayed. By identifying high-risk shipments, this system enables logistics teams to implement proactive intervention strategies, thereby improving customer satisfaction and optimizing operational costs.

### The analysis follows a complete data science pipeline, from data preparation and feature engineering to model training, evaluation.

## Dataset
### Olist Brazilian E-commerce Public Dataset
It contains information on 100,000 orders placed on Olist, a major Brazilian marketplace, from 2016 to 2018.

The dataset is composed of multiple files, which were merged and used for the analysis:

olist_orders_dataset.csv (Order status, purchase/delivery dates)

olist_order_items_dataset.csv (Product details, shipping limits)

olist_products_dataset.csv (Product category, dimensions, weight)

olist_customers_dataset.csv (Customer location)

olist_sellers_dataset.csv (Seller location)

olist_geolocation_dataset.csv (Coordinates for zip codes)

## Methodology
Data Merging & Preprocessing: The various CSV files were loaded and merged into a single, comprehensive dataframe using shared keys like order_id and customer_id. Missing values and incorrect data types were handled to ensure data quality.

## Feature Engineering:

### Target Variable: A binary variable, is_delayed, was created by comparing the order_estimated_delivery_date with the order_delivered_customer_date.

### Time-Based Features: New features were engineered from timestamps, including day_of_week, month, and shipping_lead_time.

### Order & Product Features: Features like product_weight_g, product_volume, freight_value, and order_value were created and used as predictors.

## Model Training:

### An XGBoost Classifier due to its robust performance and ability to handle complex, non-linear relationships.

### The data was split into training and testing sets to validate the model's performance on unseen data.

## Model Evaluation & Interpretation:

### The model's performance was evaluated using standard classification metrics, including ROC AUC, Precision, Recall, and the F1-Score.

### Feature Importance analysis was performed to identify the key drivers of delivery delays.
