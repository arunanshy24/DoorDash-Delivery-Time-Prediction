# DoorDash Delivery Time Prediction

## Project Overview
This project focuses on predicting DoorDash delivery times using machine learning techniques. The model analyzes historical delivery data to estimate the total delivery duration in seconds, helping optimize delivery operations and improve customer experience.

## Dataset
The dataset (`historical_data.csv`) contains 197,428 historical delivery records with 16 original features including:
- Market and store information
- Order details (items, pricing, subtotal)
- Dasher availability metrics
- Time estimates (order placement, driving duration)
- Timestamps for order creation and actual delivery

## Key Features & Engineering

### Target Variable
- **actual_total_delivery_duration**: Calculated as the time difference between `created_at` and `actual_delivery_time` in seconds

### Engineered Features
- **estimated_non_prep_duration**: Sum of estimated driving and order placement durations
- **busy_dashers_ratio**: Ratio of busy dashers to onshift dashers
- **Categorical Encoding**: One-hot encoding for market_id, order_protocol, and store primary categories
- **Data Cleaning**: Handled missing values and infinite values

### Data Preprocessing
- Converted datetime columns to proper format
- Filled missing store categories using mode per store_id
- Removed redundant columns (timestamps, IDs)
- Handled infinite values and null entries
- Final training dataset: 177,070 samples × 100 features

## Model Approach
The project employs a regression-based machine learning approach to predict delivery times. While the specific model architecture isn't detailed in the provided code, the comprehensive feature engineering suggests a robust predictive modeling pipeline.

## Project Structure
- Data loading and exploration
- Feature engineering and preprocessing
- Data cleaning and transformation
- Model preparation with extensive feature set
- Categorical variable encoding (one-hot)
- Target variable derivation from timestamp data

## Technical Stack
- **Python** with pandas, numpy for data manipulation
- **matplotlib**, **seaborn** for visualization
- **scikit-learn** for machine learning components
- **datetime** for time-based feature engineering

## Potential Applications
- Delivery time estimation for customer communication
- Dasher allocation optimization
- Service quality monitoring
- Operational efficiency improvements

This project demonstrates a complete data science pipeline from raw data to model-ready features for predicting food delivery times in a real-world logistics scenario.
