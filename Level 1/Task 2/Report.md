# **Internship Report: Descriptive Analysis**

**Prepared by**: Primesh Kumar Patel  
**Internship Organization**: Cognifyz  
**Task**: Descriptive Analysis  
**Date**: 20-02-2025

---

## **Introduction**
As part of my internship at Cognifyz, I was assigned the task of performing a **descriptive analysis** on a dataset containing restaurant information. The goal was to explore the dataset, calculate key statistical measures, and identify trends in cuisines and cities. This report summarizes the steps taken, insights gained, and recommendations for further analysis.

---

## **Dataset Overview**
The dataset contains **9,551 rows** and **21 columns**, with the following key features:
- **Restaurant ID**: Unique identifier for each restaurant.
- **Restaurant Name**: Name of the restaurant.
- **Country Code**: Code representing the country.
- **City**: City where the restaurant is located.
- **Cuisines**: Types of cuisines offered.
- **Average Cost for two**: Average cost for two people.
- **Price range**: Price range category.
- **Aggregate rating**: Overall rating of the restaurant.
- **Votes**: Number of votes/ratings received.

---

## **Steps Performed**

### **1. Importing Libraries**
I began by importing essential Python libraries for data analysis and visualization:
```python
import pandas as pd
import numpy as np
import matplotlib.pyplot as plt
import seaborn as sns
```

---

### **2. Loading the Dataset**
The dataset was loaded into a Pandas DataFrame, and the first few rows were displayed to understand its structure.

---

### **3. Descriptive Analysis**

#### **3.1 Basic Statistical Measures**
The following table summarizes the key statistics for numerical columns:

| Column Name            | Mean      | Median | Std Dev    | Min  | Max     | Q1 (25%) | Q3 (75%) |
|-------------------------|-----------|--------|------------|------|---------|----------|----------|
| Average Cost for two    | 1199.21   | 400    | 16121.18   | 0    | 800000  | 250      | 700      |
| Price range             | 1.80      | 2      | 0.91       | 1    | 4       | 1        | 2        |
| Aggregate rating        | 2.67      | 3.2    | 1.52       | 0    | 4.9     | 2.5      | 3.7      |
| Votes                   | 156.91    | 31     | 430.17     | 0    | 10934   | 5        | 131      |

**Key Insights**:
- The **Average Cost for two** has a wide range, from **₹0** to **₹800,000**, with a median of **₹400**.
- Most restaurants fall in the **Price range** of **1 to 2** (affordable to mid-range).
- The **Aggregate rating** has a median of **3.2**, indicating moderate customer satisfaction.
- The **Votes** column shows significant variability, with some restaurants receiving over **10,000 votes**.

---

#### **3.2 Distribution of Categorical Variables**

##### **Country Code**
The dataset includes restaurants from the following countries:
- **Country Code 1**: 8,652 restaurants (most frequent).
- **Country Code 216**: 434 restaurants.
- **Country Code 215**: 80 restaurants.

**Key Insight**: The majority of restaurants are located in **Country Code 1**.

---

##### **City**
The top 5 cities with the highest number of restaurants are:

| City       | Number of Restaurants |
|------------|-----------------------|
| New Delhi  | 5,473                 |
| Gurgaon    | 1,118                 |
| Noida      | 1,080                 |
| Faridabad  | 251                   |
| Ghaziabad  | 25                    |

**Key Insight**: **New Delhi** has the highest concentration of restaurants, making it a key market.

---

##### **Cuisines**
The top 5 most popular cuisines are:

| Cuisine                     | Number of Restaurants |
|-----------------------------|-----------------------|
| North Indian                | 936                   |
| North Indian, Chinese       | 511                   |
| Chinese                     | 354                   |
| Fast Food                   | 354                   |
| North Indian, Mughlai       | 334                   |

**Key Insight**: **North Indian** cuisine is the most popular, followed by fusion cuisines like **North Indian, Chinese**.

---

### **4. Top Cuisines and Cities**

#### **Top 10 Cuisines**
The following cuisines are the most popular among restaurants:
1. **North Indian**: 936
2. **North Indian, Chinese**: 511
3. **Chinese**: 354
4. **Fast Food**: 354
5. **North Indian, Mughlai**: 334
6. **Cafe**: 299
7. **Bakery**: 218
8. **North Indian, Mughlai, Chinese**: 197
9. **Bakery, Desserts**: 170
10. **Street Food**: 149

---

#### **Top 10 Cities**
The following cities have the highest number of restaurants:
1. **New Delhi**: 5,473
2. **Gurgaon**: 1,118
3. **Noida**: 1,080
4. **Faridabad**: 251
5. **Ghaziabad**: 25
6. **Bhubaneshwar**: 21
7. **Amritsar**: 21
8. **Ahmedabad**: 21
9. **Lucknow**: 21
10. **Guwahati**: 21

---

## **Conclusion**
Through this task, I successfully performed a **descriptive analysis** of the restaurant dataset. Key insights include:
- **New Delhi** is the most prominent city for restaurants.
- **North Indian** cuisine is the most popular, followed by fusion cuisines.
- Most restaurants fall in the **affordable to mid-range** price category.

---

## **Recommendations**
1. **Focus on Popular Cuisines**: Invest in restaurants offering **North Indian** and fusion cuisines, as they have the highest demand.
2. **Expand in Key Cities**: Consider expanding operations in **New Delhi**, **Gurgaon**, and **Noida**, as they have a high concentration of restaurants.
3. **Improve Ratings**: Restaurants with lower aggregate ratings should focus on improving customer satisfaction to increase their ratings and attract more customers.
4. **Target Mid-Range Pricing**: Since most restaurants fall in the price range of **1 to 2**, targeting this range can attract more customers.

---

## **Next Steps**
1. Perform **correlation analysis** to identify relationships between variables (e.g., `Average Cost for two` and `Aggregate rating`).
2. Conduct **geospatial analysis** to visualize restaurant density across cities.
3. Build **predictive models** to analyze factors influencing restaurant ratings.

---

## **Attachments**
1. **Basic Statistical Measures Table**: Summary of numerical column statistics.
2. **Top Cuisines and Cities**: Lists of top cuisines and cities.

---

Thank you for the opportunity to work on this task. I look forward to further contributions during my internship at Cognifyz.
