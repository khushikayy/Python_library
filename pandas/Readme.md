# 📊 Pandas Library Guide

![Python](https://img.shields.io/badge/Python-3.9%2B-blue)
![Pandas](https://img.shields.io/badge/Pandas-Latest-brightgreen)
![License](https://img.shields.io/badge/License-MIT-yellow)

## 📖 Overview

**Pandas** is an open-source Python library designed for fast, flexible, and powerful data manipulation and analysis. It provides easy-to-use data structures and data analysis tools that make working with structured data simple and efficient.

Pandas is widely used in:

- Data Science
- Machine Learning
- Data Analytics
- Business Intelligence
- Financial Analysis
- Research
- Data Engineering

Whether you are cleaning messy datasets, analyzing customer information, or preparing data for machine learning models, Pandas provides a rich set of tools to perform these tasks efficiently.

---

# ✨ Features

- Read data from multiple file formats
  - CSV
  - Excel
  - JSON
  - SQL Databases
  - HTML Tables
  - XML
  - Parquet

- Powerful DataFrame and Series objects

- Missing value detection and handling

- Data cleaning and preprocessing

- Data filtering and selection

- Sorting and ranking

- Grouping and aggregation

- Merge, Join, and Concatenate datasets

- Time Series Analysis

- Pivot Tables

- Statistical Analysis

- Data Visualization Support

- Export data into multiple formats

---

# 📦 Installation

## Install using pip

```bash
pip install pandas
```

## Install using conda

```bash
conda install pandas
```

## Verify Installation

```python
import pandas as pd

print(pd.__version__)
```

---

# 📚 Requirements

- Python 3.9 or higher
- pip or conda package manager

Recommended:

```
numpy
matplotlib
seaborn
openpyxl
xlrd
sqlalchemy
```

Install recommended packages:

```bash
pip install numpy matplotlib seaborn openpyxl sqlalchemy
```

---

# 🚀 Quick Start

Import Pandas

```python
import pandas as pd
```

Read CSV

```python
df = pd.read_csv("customers.csv")
```

Display first rows

```python
print(df.head())
```

Display last rows

```python
print(df.tail())
```

Shape of data

```python
print(df.shape)
```

Column names

```python
print(df.columns)
```

Information about dataset

```python
print(df.info())
```

Summary statistics

```python
print(df.describe())
```

---

# 📄 Reading Different File Formats

### CSV

```python
df = pd.read_csv("data.csv")
```

### Excel

```python
df = pd.read_excel("sales.xlsx")
```

### JSON

```python
df = pd.read_json("employees.json")
```

### SQL

```python
from sqlalchemy import create_engine

engine = create_engine("sqlite:///database.db")

df = pd.read_sql("SELECT * FROM customers", engine)
```

### HTML

```python
tables = pd.read_html("https://example.com")
```

---

# 🛠 Data Inspection

```python
df.head()
df.tail()
df.sample(5)
df.info()
df.describe()
df.shape
df.columns
df.index
df.dtypes
```

---

# 🔍 Selecting Data

Single Column

```python
df["Name"]
```

Multiple Columns

```python
df[["Name","Age"]]
```

Using loc

```python
df.loc[0]
```

Using iloc

```python
df.iloc[0]
```

Rows and Columns

```python
df.loc[0:10, ["Name","Salary"]]
```

---

# 🎯 Filtering Data

```python
df[df["Age"] > 30]
```

Multiple Conditions

```python
df[ (df["Age"] > 30) & (df["Salary"] > 50000) ]
```

Using isin()

```python
df[df["Department"].isin(["IT","HR"])]
```

Using between()

```python
df[df["Age"].between(20,40)]
```

---

# 🧹 Data Cleaning

Find Missing Values

```python
df.isnull().sum()
```

Drop Missing Values

```python
df.dropna()
```

Fill Missing Values

```python
df.fillna(0)
```

Rename Columns

```python
df.rename(columns={ "fname":"First Name" })
```

Remove Duplicates

```python
df.drop_duplicates()
```

Change Data Types

```python
df["Age"] = df["Age"].astype(int)
```

---

# 📈 Sorting

Ascending

```python
df.sort_values("Age")
```

Descending

```python
df.sort_values(
    "Salary",
    ascending=False
)
```

---

# 📊 GroupBy Operations

```python
df.groupby("Department").mean()
```

Count

```python
df.groupby("Department").size()
```

Multiple Aggregations

```python
df.groupby("Department").agg({ "Salary":["mean","max","min"], "Age":"mean" })
```

---

# 🔄 Merge DataFrames

Inner Join

```python
pd.merge(df1, df2, on="ID")
```

Left Join

```python
pd.merge( df1, df2, how="left" )
```

Right Join

```python
pd.merge( df1, df2, how="right")
```

Outer Join

```python
pd.merge( df1, df2, how="outer" )
```

---

# 📌 Concatenate DataFrames

```python
pd.concat([df1,df2])
```

Horizontal

```python
pd.concat( [df1,df2], axis=1 )
```

---

# 📅 Working with Dates

```python
df["Date"] = pd.to_datetime(df["Date"])
```

Extract Year

```python
df["Date"].dt.year
```

Extract Month

```python
df["Date"].dt.month
```

Extract Day

```python
df["Date"].dt.day
```

---

# 📊 Pivot Table

```python
pd.pivot_table(
    df,
    values="Sales",
    index="Region",
    columns="Category",
    aggfunc="sum"
)
```

---

# 📉 Export Data

CSV

```python
df.to_csv(
    "output.csv",
    index=False
)
```

Excel

```python
df.to_excel(
    "output.xlsx",
    index=False
)
```

JSON

```python
df.to_json("output.json")
```

---

# 📈 Visualization

```python
import matplotlib.pyplot as plt

df["Sales"].plot()

plt.show()
```

Bar Chart

```python
df.plot.bar(x="Name", y="Sales")
```

Histogram

```python
df["Age"].hist()
```

---

# 📚 Common Pandas Functions

| Function          | Description             |
| ----------------- | ----------------------- |
| head()            | First rows              |
| tail()            | Last rows               |
| info()            | Dataset information     |
| describe()        | Statistical summary     |
| shape             | Dataset dimensions      |
| columns           | Column names            |
| dtypes            | Data types              |
| value_counts()    | Frequency count         |
| unique()          | Unique values           |
| nunique()         | Number of unique values |
| sort_values()     | Sorting                 |
| groupby()         | Grouping                |
| merge()           | Join DataFrames         |
| concat()          | Concatenate             |
| pivot_table()     | Pivot Tables            |
| fillna()          | Fill missing values     |
| dropna()          | Remove missing values   |
| drop_duplicates() | Remove duplicates       |

---

# ⚡ Performance Tips

- Use vectorized operations instead of loops.
- Specify column data types when loading large files.
- Use `usecols` in `read_csv()` to load only required columns.
- Convert repeated text columns to the `category` data type.
- Use `query()` for complex filtering.
- Avoid using `iterrows()` when possible.

---

# 🧪 Example Project

```python
import pandas as pd

df = pd.read_csv("employees.csv")

df = df.drop_duplicates()

df["Salary"] = df["Salary"].fillna(
    df["Salary"].mean()
)

high_salary = df[df["Salary"] > 50000]

department_summary = (
    high_salary
    .groupby("Department")
    .agg({
        "Salary":"mean",
        "Age":"mean"
    })
)

department_summary.to_csv(
    "summary.csv"
)

print(department_summary)
```

---

# 📖 Official Documentation

- https://pandas.pydata.org/docs/
- https://pandas.pydata.org/getting_started.html

---

# 📄 License

This project is licensed under the MIT License.

---

# 👨‍💻 Acknowledgements

- Pandas Development Team
- NumPy Community
- Python Software Foundation

---

## ⭐ Support

If you found this project helpful:

- ⭐ Star the repository
- 🍴 Fork the project
- 🐞 Report issues
- 💡 Suggest improvements

Happy Coding! 
