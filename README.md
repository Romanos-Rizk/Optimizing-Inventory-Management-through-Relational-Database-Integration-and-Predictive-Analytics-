# Optimizing Inventory Management through Relational Database Integration and Predictive Analytics

## Tools
- **Python**: Used for data analysis and predictive modeling.
- **MySQL**: Employed for database management and data storage.
- **Tableau**: Utilized for data visualization and insights.

## Outline
1. [Project Overview](#project-overview)
2. [Problem Statement](#problem-statement)
3. [Proposed Solution](#proposed-solution)
4. [Methodology](#methodology)
   - [Data Preprocessing](#data-preprocessing)
   - [Database Design](#database-design)
   - [Prediction Model](#prediction-model)
5. [Results](#results)
6. [Limitations & Recommendations](#limitations--recommendations)
   - [Limitations](#limitations)
   - [Recommendations](#recommendations)
7. [Conclusion](#conclusion)

## Project Overview

This project addresses the challenges faced by Linkers, a wholesale appliance company, in managing and forecasting inventory. The goal was to design a relational database to store and analyze inventory and sales data, followed by the development of a predictive model to forecast sales and optimize inventory management.

## Problem Statement

Wholesale appliance companies, like Linkers, often struggle with inventory forecasting due to limited access to direct customer data. Linkers, operating since 1993, used Excel for inventory management but required a more efficient solution. The absence of a structured database led to challenges in predicting inventory needs accurately.

## Proposed Solution

To address these issues, we implemented a MySQL relational database to store and manage inventory data. We then used Python to build a predictive model for forecasting sales. This approach aimed to improve inventory management, reduce stock imbalances, and optimize restocking processes.

## Methodology

### Data Preprocessing
- **Transforming Column Names**: Standardized column names for consistency and integration into MySQL.
- **Handling Missing Values**: Replaced or removed missing values in key columns.
- **Converting Date Columns**: Changed date columns to date/time format for meaningful analysis.
- **Normalizing Categorical Columns**: Standardized categorical data for consistency.
- **Addressing Illogical Values**: Removed rows with invalid values in key columns.
- **Normalizing Description Columns**: Cleaned and standardized description text for better analysis.

### Database Design
- **Creating Tables**:
  - **Customer Table**: Stores customer details.
  - **Order Table**: Tracks order information.
  - **Product Table**: Maintains product details.
  - **Product Categories**: Specific tables for different product categories.
- **Defining Relationships**: Established relationships between tables using foreign keys to ensure data integrity.

### Prediction Model
- **Data Splitting**: Divided the dataset into training (80%) and validation (20%) sets.
- **Feature Engineering**: Refined features to improve model performance.
- **Model Building**: Implemented a Random Forest model. Trained the model and evaluated its performance, addressing overfitting issues.

## Results
- **Training RMSE**: Approximately 4.24
- **Validation RMSE**: Approximately 13.09

The model demonstrated a strong fit to the training data but showed potential overfitting issues on unseen data. Further refinement is needed to enhance model generalizability.

## Limitations & Recommendations

### Limitations
- **1 Item Limit per Order**: Customers ordering multiple items in a single transaction require multiple records, reflecting current operational constraints.
- **Employee Training**: Transitioning from Excel to a database system requires employee training and a period of parallel system operation.
- **Primary Key Management**: Manual creation of item codes and customer IDs due to non-numeric primary keys in MySQL.

### Recommendations
- **User Authentication**: Implement a user authentication system to control access to the database.
- **User Interface**: Develop a user-friendly interface to facilitate data retrieval without requiring complex SQL queries.

## Conclusion

The project successfully designed a robust database structure for Linkers, enabling efficient data management and predictive analytics. This implementation provides Linkers with valuable insights to optimize inventory management and gain a competitive edge in the market.
