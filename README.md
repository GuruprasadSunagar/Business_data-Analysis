# 🍔 Food Delivery Data Analysis

## 📌 Project Overview

This project performs **Exploratory Data Analysis (EDA)** on a food delivery dataset using Python.

The main goal of this project is to understand food delivery orders, order types, delivery person ratings, order trends over time, and city-wise order distribution.

The project uses **Pandas, NumPy, and Matplotlib** to clean, analyze, and visualize the data.

---

## 🎯 Objectives

* Load and explore the food delivery dataset
* Understand the structure of the dataset
* Check the number of rows and columns
* Check for missing values
* Find and remove duplicate records
* Analyze different types of orders
* Analyze delivery person ratings
* Analyze daily order trends
* Analyze monthly order trends
* Analyze orders by city type
* Create charts and visualizations

---

## 🛠️ Technologies Used

* 🐍 Python
* 🐼 Pandas
* 🔢 NumPy
* 📊 Matplotlib
* 📓 Jupyter Notebook / Google Colab

---

## 📂 Project Files

```text
Food-Delivery-Data-Analysis/
│
├── Welcome_To_Colab.ipynb
├── cleaned_test.csv
├── type_counts.png
├── orders_by_city.png
├── monthly_orders.png
└── README.md
```

---

## 🔍 Data Analysis Performed

### 1. Dataset Loading

The dataset is loaded using Pandas:

```python
import pandas as pd

a = pd.read_csv('cleaned_test.csv')
```

---

### 2. Dataset Exploration

The project checks:

* First 5 records
* Last 5 records
* Dataset shape
* Dataset size
* Column names
* Dataset information

Example:

```python
print(a.shape)
print(a.size)
print(a.columns)
```

---

### 3. Missing Value Analysis

Missing values are checked using:

```python
print(a.isnull().sum())
```

This helps identify columns that contain missing data.

---

### 4. Duplicate Data

Duplicate records are identified:

```python
print(a.duplicated().sum())
```

Duplicates are then removed:

```python
a.drop_duplicates(inplace=True)
```

---

### 5. Order Type Analysis

The project analyzes different types of orders using:

```python
a['Type_of_order'].value_counts()
```

A bar chart and pie chart are created to understand the distribution of order types.

---

### 6. Delivery Person Rating Analysis

The project analyzes delivery person ratings:

```python
a['Delivery_person_Ratings'].value_counts()
```

A bar chart is created to visualize the rating distribution.

---

### 7. Daily Order Trends

The `Order_Date` column is converted into datetime format:

```python
a['Order_Date'] = pd.to_datetime(
    a['Order_Date'],
    format='%d-%m-%Y',
    errors='coerce'
)
```

This is used to analyze the number of orders over time.

A line chart is created to visualize daily order trends.

---

### 8. Monthly Order Analysis

The project extracts the year and month from the order date:

```python
a['Year_Month'] = a['Order_Date'].dt.to_period('M')
```

Then monthly order counts are calculated.

This helps understand how order volume changes from month to month.

---

### 9. City-wise Order Analysis

Orders are grouped according to the `City` column:

```python
city_counts = a['City'].value_counts()
```

A bar chart is created to visualize the distribution of orders by city type.

---

## 📊 Visualizations

The project generates different visualizations, including:

* Order Type Distribution
* Percentage of Order Types
* Delivery Person Rating Distribution
* Daily Order Trends
* Orders by City Type
* Monthly Order Trends

---

## 💡 Key Skills Demonstrated

This project demonstrates practical knowledge of:

* Python programming
* Pandas DataFrame operations
* NumPy
* Data cleaning
* Missing value checking
* Duplicate data handling
* Data aggregation
* Date and time handling
* Exploratory Data Analysis (EDA)
* Data visualization
* Matplotlib

---

## 🚀 How to Run the Project

### Step 1: Clone the Repository

```bash
git clone YOUR_GITHUB_REPOSITORY_URL
```

### Step 2: Open the Notebook

Open:

```text
Welcome_To_Colab.ipynb
```

You can run it using:

* Google Colab
* Jupyter Notebook
* JupyterLab

### Step 3: Add the Dataset

Make sure the following file is available in the same working environment:

```text
cleaned_test.csv
```

### Step 4: Run the Notebook

Run the cells from top to bottom to perform the complete analysis.

---

## 📈 Project Outcome

This project provides an understanding of food delivery data through data cleaning, statistical analysis, and visualization.

It helps identify patterns in:

* Order types
* Delivery ratings
* Daily orders
* Monthly orders
* City-wise orders

---

## 👨‍💻 Author

**Prasad**

BCA Student | Aspiring Data Scientist

### Skills

`Python` `Pandas` `NumPy` `Matplotlib` `Data Analysis` `EDA`

---

## ⭐ Future Improvements

Some possible improvements for this project are:

* Add more detailed statistical analysis
* Analyze delivery time
* Analyze order cost
* Analyze traffic conditions
* Analyze weather conditions
* Build an interactive dashboard using Power BI
* Apply Machine Learning for prediction
* Add more advanced visualizations

---

## 📜 License

This project is created for **learning and educational purposes**.
