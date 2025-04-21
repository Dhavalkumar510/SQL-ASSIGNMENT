# 🚗 Synthetic Car Data Generator & SQLite Integration

## 📌 Project Overview
This project aims to generate synthetic car data using Python, organize it into a relational database schema, and integrate the data into an SQLite database. The dataset mimics realistic car sales information from the years 2010 to 2015, and includes various types of data such as Nominal, Ordinal, Interval, and Ratio (NOIR).

## 🔧 Tools & Libraries Used
Python

Google Colab

Faker - for generating fake data

Pandas - for DataFrame creation and manipulation

SQLite3 - for database integration

NumPy (optional) - for randomization and calculations

## 🗂️ Data Description
A total of 1200 rows and 10 columns were generated, including:

Number Plate (unique, Nominal)

Car Brand (Nominal)

Selling Date (Interval)

Selling Price (£) (Ratio)

Safety Rating (Ordinal)

Fuel Type (Nominal)

Top Speed (km/h) (Ratio)

Insurance Premium (£) (Ratio)

Maintenance Cost (£) (Ratio)

Owner Name (Nominal)

The data includes all four NOIR data types to simulate realistic automotive data.

## 📊 Data Handling Process

### 1. Data Generation
Used the Faker library to create random but realistic car-related information.

Ensured uniqueness in number plates.

Generated values within specified realistic ranges.

### 2. DataFrame Creation & Sorting
Created a Pandas DataFrame named car.

Sorted data in ascending order based on selling dates for better readability.

### 3. Database Schema & SQLite Integration
Created and connected to car_database.db.

Defined a relational schema with the following three tables:


Table Name	Description
car_data	Stores basic details (e.g., number plate, brand, price, date, safety, fuel, speed)
car_expense	Holds expense data (insurance, maintenance)
car_owner	Stores owner details (first and last names)
Tables were designed with foreign keys to maintain data relationships and integrity.

### 4. Data Insertion
Converted the cleaned Pandas DataFrame into SQLite tables using .to_sql().

Used composite keys and foreign keys to establish inter-table relationships.

### 5. Data Validation
Checked for missing values and duplicates.

Cleaned the data to ensure consistency and accuracy before database integration.


## ✅ Final Output
A well-structured SQLite database with 3 relational tables.

Accurate, diverse synthetic data useful for analysis, querying, and learning database design.

Example screenshots included (in original Colab/Notebook) to showcase successful outputs and queries.
