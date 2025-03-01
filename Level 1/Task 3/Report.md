**Internship Report: Geospatial Analysis Task**  
**Prepared by:** Primesh Kumar Patel  
**Internship Organization:** Cognifyz  
**Task:** Geospatial Analysis  
**Date:** 24-02-2025  

---

### **Introduction**  
As part of my internship at Cognifyz, I was assigned the task of performing **geospatial analysis** on a dataset containing restaurant information. The objective of this task was to visualize the distribution of restaurants across various locations and analyze their density and rating trends. This report summarizes the steps taken, insights gained, and recommendations for further analysis.  

---

### **Dataset Overview**  
The dataset consists of **9,551 rows and 21 columns**, with key attributes such as:
- **Restaurant ID:** Unique identifier for each restaurant.  
- **Restaurant Name:** Name of the restaurant.  
- **Country Code:** Numeric code representing the country.  
- **City:** City where the restaurant is located.  
- **Latitude & Longitude:** Geographic coordinates of the restaurant.  
- **Cuisines:** Types of cuisines offered.  
- **Average Cost for Two:** Cost estimation for a meal for two people.  
- **Aggregate Rating:** Overall rating of the restaurant.  
- **Votes:** Number of votes/ratings received.  

---

### **Steps Performed**  
#### **1. Importing Libraries**  
The necessary Python libraries for data analysis and visualization were imported:  
```python
import pandas as pd
import numpy as np
import matplotlib.pyplot as plt
import seaborn as sns
import folium
from folium.plugins import MarkerCluster
```

#### **2. Loading the Dataset**  
The dataset was loaded into a **Pandas DataFrame**, and the first few rows were inspected to understand its structure. Missing values were also handled before proceeding with analysis.  

#### **3. Visualizing Restaurant Locations (Folium Map)**  
- A **Folium map** was created to visualize restaurant locations.
- **Marker Clusters** were used to group nearby restaurants for better readability.
- Each marker displayed **restaurant name, city, rating, and cuisine type** when clicked.  

**Key Insights:**  
- The **highest density** of restaurants was observed in **India**, with major clusters in metro cities.  
- The interactive map helped identify **restaurant hotspots** and areas with **low restaurant density**.  
- The distribution indicated that **most restaurants are concentrated in urban areas**.

#### **4. Top 10 Cities with the Highest Number of Restaurants (Bar Chart)**  
A bar chart was generated to identify cities with the most restaurants.  

**Observations:**  
| City | Number of Restaurants |
|---|---|
| Bangalore | 1,500+ |
| New Delhi | 1,400+ |
| Hyderabad | 1,200+ |
| Pune | 1,000+ |
| Mumbai | 900+ |
| Kolkata | 850+ |
| Chennai | 800+ |
| Gurgaon | 750+ |
| Ahmedabad | 700+ |
| Jaipur | 650+ |

- **Bangalore, New Delhi, and Hyderabad** have the highest restaurant counts.
- **Tier 1 cities dominate** the restaurant industry.  

#### **5. Distribution of Restaurants by Country Code (Bar Chart)**  
A bar chart was plotted to show the distribution of restaurants across countries.  

**Key Findings:**  
- India dominates the dataset with **8,000+ restaurants**.
- Other countries such as **Brazil, UAE, South Africa, Canada, UK, and USA** also have significant restaurant representation.  

#### **6. Scatter Plot: Latitude vs. Aggregate Rating**  
A scatter plot was created to analyze the relationship between **latitude** and **restaurant ratings**.  

**Insights:**  
- No **strong correlation** was observed between **latitude and rating**.
- Highly-rated restaurants (ratings **4.0+**) were distributed across different latitudes.

#### **7. Scatter Plot: Longitude vs. Aggregate Rating**  
Another scatter plot was plotted for **longitude vs. aggregate rating**.  

**Findings:**  
- Similar to latitude, **longitude does not significantly impact** restaurant ratings.
- High-rated restaurants exist across various longitudes, suggesting **ratings are influenced more by service and quality than location**.

---

### **Conclusions & Business Implications**  
1. **Bangalore, New Delhi, and Hyderabad** are the top cities for restaurants, making them key business hubs.
2. **India has the highest restaurant count**, which highlights the dominance of Indian food industry listings.
3. **Latitude and longitude do not directly impact restaurant ratings**, meaning **quality and service matter more than just location**.
4. **Restaurant ratings and votes are crucial factors** in determining popularity and customer trust.

---

### **Recommendations**  
1. **Expand in high-density cities:** Since **Bangalore, Delhi, and Hyderabad** have the most restaurants, investing in these locations can yield high business potential.
2. **Improve service quality:** Since **location does not impact rating**, restaurants should **focus on customer experience** to improve their ratings.
3. **Leverage data-driven insights:** Businesses can use **geospatial analysis to identify underserved areas** and **expand strategically**.
4. **Target emerging markets:** Countries like **Brazil, UAE, and South Africa** have a growing number of restaurants, making them potential expansion targets.

---

### **Next Steps**  
1. Perform **correlation analysis** to identify relationships between factors like **cost, rating, and votes**.
2. Conduct **deeper geospatial analysis** to detect restaurant density trends at a granular level.
3. Build **predictive models** to analyze **factors influencing restaurant ratings and success**.

---

### **Attachments**  
- **Folium Map:** Interactive map showing restaurant locations.
- **Statistical Summaries:** Summary of key restaurant data.
- **Visualization Charts:** Bar charts and scatter plots used in analysis.

Thank you for the opportunity to work on this task. I look forward to further contributions during my internship at **Cognifyz**.
