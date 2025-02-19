**Internship Report: Data Exploration and Preprocessing Task**

**Prepared by:** Primesh Kumar Patel\
**Internship Organization:** Cognifyz\
**Task:** Data Exploration and Preprocessing\
**Date:** 19-02-2025

---

### **Introduction**

As part of my internship at Cognifyz, I was assigned the task of **data exploration and preprocessing** for a dataset related to restaurant information. The goal was to clean, analyze, and prepare the dataset for further analysis or modeling. Below is a detailed report of the steps I followed, the challenges encountered, and the solutions implemented.

---

### **Dataset Overview**

The dataset contains **9,551 rows and 21 columns**, with the following features:

- **Restaurant ID**: Unique identifier for each restaurant.
- **Restaurant Name**: Name of the restaurant.
- **Country Code**: Code representing the country.
- **City**: City where the restaurant is located.
- **Address**: Address of the restaurant.
- **Locality**: Locality within the city.
- **Locality Verbose**: Detailed locality information.
- **Longitude**: Geographic longitude.
- **Latitude**: Geographic latitude.
- **Cuisines**: Types of cuisines offered.
- **Average Cost for two**: Average cost for two people.
- **Currency**: Currency used for pricing.
- **Has Table booking**: Whether the restaurant offers table booking.
- **Has Online delivery**: Whether the restaurant offers online delivery.
- **Is delivering now**: Whether the restaurant is currently delivering.
- **Switch to order menu**: Whether the restaurant has a switch-to-order menu.
- **Price range**: Price range category.
- **Aggregate rating**: Overall rating of the restaurant.
- **Rating color**: Color associated with the rating.
- **Rating text**: Text description of the rating.
- **Votes**: Number of votes/ratings received.

---

### **Steps Performed**

#### **1. Importing Libraries**

I began by importing essential Python libraries for data analysis and visualization:

```python
import pandas as pd  
import numpy as np  
import matplotlib.pyplot as plt  
import seaborn as sns  
```

#### **2. Loading the Dataset**

The dataset was loaded into a Pandas DataFrame, and the first few rows were displayed using `head()` to get an initial understanding of the data.

#### **3. Data Exploration**

- **Shape of the Dataset**: The dataset contains **9,551 rows and 21 columns**.
- **Missing Values**: Only the **"Cuisines"** column had **9 missing values**. Instead of dropping these rows, I filled the missing values using the mode of the "Cuisines" column grouped by "City". The missing Restaurant IDs were:
  ```
  17284105, 17284211, 17284158, 17374552, 17501439, 17606621, 17059060, 17142698, 17616465  
  ```
  The code used for filling missing values:
  ```python
  df['Cuisines'] = df.groupby("City")["Cuisines"].apply(lambda x: x.fillna(x.mode()[0] if not x.mode().empty else "Unknown"))  
  ```

#### **4. Data Type Correction**

- **Boolean Conversion**: Columns like "Has Table booking", "Has Online delivery", "Is delivering now", and "Switch to order menu" were converted from categorical ("Yes"/"No") to Boolean (True/False):
  ```python
  bool_cols = ["Has Table booking", "Has Online delivery", "Is delivering now", "Switch to order menu"]  
  df[bool_cols] = df[bool_cols].applymap(lambda x: True if x == "Yes" else False)  
  ```
- **Categorical Conversion**: Columns like "Price range" and "Rating color" were converted to the 'category' data type:
  ```python
  df["Price range"] = df["Price range"].astype("category")  
  df["Rating color"] = df["Rating color"].astype("category")  
  ```
- **String Conversion**: The "Country Code" column was converted from integer to string:
  ```python
  df["Country Code"] = df["Country Code"].astype(str)  
  ```

#### **5. Target Variable Analysis**

The target variable for this dataset is **"Aggregate rating"**. I analyzed its distribution using a frequency plot (attached as `cognifyz_task_1_aggregate_rating.png`). The plot shows the following:

- The majority of ratings are concentrated around **3.0 to 4.0**, indicating that most restaurants receive moderate ratings.
- A significant number of restaurants have a **0.0 rating**, which could represent missing or unrated entries.
- Ratings above **4.5** are less frequent, indicating fewer high-rated restaurants.

#### **6. Class Imbalance Check**

I checked for class imbalance in the "Aggregate rating" column using:

```python
print(df['Aggregate rating'].value_counts())  
```

The output revealed a significant imbalance, with **2,148 entries having a 0.0 rating**. This imbalance could affect model performance if not addressed in future tasks.

---

### **Conclusion**

Through this task, I successfully explored and preprocessed the dataset. Key steps included handling missing values, correcting data types, and analyzing the target variable. The cleaned dataset was exported as **"processed\_data.csv"** for further use.

---

### **Next Steps**

- Address the class imbalance in the "Aggregate rating" column.
- Perform feature engineering to derive additional insights.
- Build predictive models to analyze restaurant ratings.

---

**Attachments:**

1. `cognifyz_task_1_aggregate_rating.png` - Frequency distribution of "Aggregate rating".
2. `processed_data.csv` - Cleaned and preprocessed dataset.

---

Thank you for the opportunity to work on this task. I look forward to further contributions during my internship at Cognifyz.
