# 🏠 House Prices Data Analysis Project 2

---
## 📚 Course Information
Course: (طرق البرمجة المتقدمة)  
Instructor: (رزان فيصل الفقير)

---
## 👩‍🎓 Team Members
- Noura Saad  
- Fatimah Abdullah  
- Amjad Al-Hilem  
- Nasaem Salem  
- Jowana Al-Qahtani  
- Raghad Abdulrahman  

---

# 🎯 Project Objective
Analyze house prices using:
- Pandas
- NumPy
- Matplotlib

The goal is to find patterns between price and features like size, bedrooms, city, and year.

---

# 👩‍💻 1. Noura Saad — Data Loading & Exploration

## 📥 Code
```python
import pandas as pd
import numpy as np
import matplotlib.pyplot as plt

df = pd.read_excel('house_prices_realistic.xlsx')

print(df.head(10))
print(df.tail(10))
print(df.shape)
print(df.dtypes)
📌 Explanation
Noura is responsible for loading the dataset and exploring its structure by checking rows, columns, and data types.

👩‍💻 2. Fatimah Abdullah — Data Cleaning

🧹 Code
print(df.isnull().sum())
df = df.fillna(df.mean(numeric_only=True))
📌 Explanation
Fatimah handled missing values and cleaned the dataset by replacing null values with the mean.

👩‍💻 3. Amjad Al-Hilem — Statistical Analysis

📊 Code
print(df.describe())
print(df.select_dtypes(include=np.number).agg(['min', 'max']))
📌 Explanation
Amjad performed statistical analysis including mean, standard deviation, minimum, and maximum values.

👩‍💻 4. Nasaem Salem — Data Visualization (Part 1)
📈 Code
df.groupby('Year')['Price'].mean().plot(kind='bar')
plt.title("Average House Prices Per Year")
plt.show()

df.groupby('Year')['Price'].mean().plot(kind='line', marker='o')
plt.title("Price Trend Over Years")
plt.grid(True)
plt.show()
📌 Explanation
Nasaem created bar and line charts to analyze price trends over years.
👩‍💻 5. Jowana Al-Qahtani — Data Visualization (Part 2)

📊 Code
df['Price'].hist(bins=20)
plt.title("Price Distribution")
plt.show()

plt.scatter(df['Size_m2'], df['Price'])
plt.title("Size vs Price")
plt.show()
📌 Explanation
Jowana created histogram and scatter plot to analyze price distribution and relationship with size.

👩‍💻 6. Raghad Abdulrahman — Advanced Analysis

📊 Code
df.groupby('City')['Price'].mean().plot(kind='bar')
plt.title("Average Price by City")
plt.xticks(rotation=45)
plt.show()

df.groupby('Bedrooms')['Price'].mean().plot(kind='bar')
plt.title("Bedrooms vs Price")
plt.show()
📌 Explanation

Raghad analyzed differences in prices between cities and the effect of number of bedrooms

# 🎯 Project Idea

This project is a real estate data analysis project that focuses on studying house prices.

The main idea is to understand how different factors such as:
- house size  
- number of bedrooms  
- city  
- year of sale  

affect the final price of a house.

We use Python to explore the dataset and discover patterns in the housing market.

---

# 💡 Final Insights

- House prices increase with size  
- More bedrooms increase price  
- Cities have different price levels  
- Prices change over time  
- Strong relationship exists between features and price  

---

# 🧾 Conclusion

This project successfully analyzes real estate data using Python.

It includes:
- Data loading and exploration  
- Data cleaning  
- Statistical analysis  
- Data visualization  

The results help us understand how house features affect pricing and reveal patterns in the real estate market.
