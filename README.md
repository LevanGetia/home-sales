# Home Sales Analysis Project

## Overview

This project focuses on analyzing home sales data using Apache Spark and PySpark,
showcasing the ability to handle and process large datasets efficiently. The
analysis aims to uncover insights from the home sales data, such as average prices
based on various criteria, view ratings for certain price ranges, and performance
differences between cached and uncached data.

## Objectives

The primary objectives of this project include:

1. **Data Loading and Processing**: Load home sales data from an AWS S3 bucket into a PySpark DataFrame.
2. **Data Analysis**: Perform various analytical queries using Spark SQL.
3. **Performance Optimization**: Leverage caching and partitioning to optimize query performance.
4. **Comparison of Data Storage Formats**: Evaluate the performance differences between standard and partitioned Parquet formats.

## Technical Requirements

- **PySpark**: Used for DataFrame creation and operations.
- **Spark SQL**: Employed for executing SQL queries on DataFrames.
- **AWS S3 Bucket**: Source of the home sales data.
- **Python**: The programming language used for scripting.

## Dataset Description

The dataset, sourced from an AWS S3 bucket, includes various details about home sales, such as sale price, number of bedrooms and bathrooms, square footage, and other relevant attributes.

## Key Challenges

1. **Data Ingestion**: Reading data from an S3 bucket into a PySpark DataFrame.
2. **Query Execution**: Writing and executing SparkSQL queries to extract meaningful insights.
3. **Performance Measurement**: Timing the execution of queries to assess the impact of caching and data partitioning.
4. **Data Management**: Caching data and managing temporary tables in Spark.

## Methodology

The project follows these steps:

1. **Data Reading**: Read the home sales data into a PySpark DataFrame.
2. **Temporary Table Creation**: Create a temporary table for Spark SQL operations.
3. **Analytical Queries**:
    - Determine the average price of four-bedroom houses sold each year.
    - Compute the average price of homes with three bedrooms and three bathrooms for each year they were built.
    - Find the average price of homes with specific features (three bedrooms, three bathrooms, two floors, ≥ 2,000 square feet) for each year built.
    - Ascertain the view rating for homes costing ≥ $350,000.
4. **Caching and Performance Analysis**: Cache the temporary table, run queries on cached data, and compare runtimes.
5. **Partitioning and Parquet Format**:
    - Partition the dataset by the `date_built` field.
    - Read the partitioned data in Parquet format and create a temporary table.
    - Compare query runtimes on Parquet format data to those on cached data.
6. **Uncaching**: Uncache the temporary table and verify its status.

## Results and Insights

The analysis provides valuable insights into the home sales data, such as trends in
average prices based on various property features. Additionally, it demonstrates
the effectiveness of caching and partitioning in improving query performance,
particularly for large datasets.

## Conclusion

This project exemplifies the power of PySpark and Spark SQL in big data analytics,
especially in handling and analyzing large datasets efficiently. The insights
derived from the home sales data are crucial for stakeholders in the real estate
market, providing a data-driven basis for decision-making.

