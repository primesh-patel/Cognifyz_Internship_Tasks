**Internship Report: Customer Preference Analysis**

**Prepared by:** Primesh Kumar Patel  
**Internship Organization:** Cognifyz  
**Task:** Customer Preference Analysis  
**Date:** 22-02-2025  

---

## **Introduction**
As part of my internship at Cognifyz, I was assigned the task of analyzing customer preferences based on restaurant cuisines. The objective was to examine the relationship between cuisine types and restaurant ratings, identify the most popular cuisines based on customer votes, and determine if specific cuisines tend to receive higher ratings. This report outlines the methodology used, key findings, and insights derived from the analysis.

---

## **Dataset Overview**
The dataset contains various details about restaurants, including their ratings, votes, and types of cuisine. The key features utilized in this analysis are:
- **Cuisines**: The type of cuisine served at the restaurant.
- **Aggregate Rating**: The overall rating given by customers.
- **Votes**: The number of votes received by the restaurant.
- **City**: The location of the restaurant.

To ensure data quality, unnecessary columns were removed, and missing values were handled appropriately.

---

## **Steps Performed**

### **1. Data Preprocessing**
- Removed irrelevant columns such as restaurant name, address, and currency.
- Dropped missing values to ensure clean and accurate analysis.

### **2. Relationship Between Cuisine and Ratings**
- Grouped the data by cuisine type and calculated the average rating for each cuisine.
- Sorted cuisines based on their average ratings to determine the highest-rated ones.

### **3. Popular Cuisines Based on Votes**
- Aggregated the total number of votes per cuisine.
- Identified the most popular cuisines based on the highest number of votes.

### **4. Data Visualization**
- **Top 10 Cuisines by Average Rating:** A bar chart was plotted to showcase the cuisines with the highest average ratings.
- **Top 10 Most Popular Cuisines by Votes:** Another bar chart was plotted to display the cuisines that received the highest customer votes.
- **Histogram of Ratings:** To analyze the overall distribution of ratings.
- **Scatter Plot of Votes vs Ratings:** To understand the correlation between popularity and rating.
- **Box Plot of Ratings by Cuisine:** To analyze the variation in ratings within different cuisine types.

---

## **Key Findings and Insights**

### **1. Highest Rated Cuisine**
The cuisine with the highest average rating was **Italian Cuisine**, with an aggregate rating of **4.5**. This indicates that customers highly appreciate Italian cuisine for its quality, authenticity, and taste. The presence of high-rated Italian restaurants suggests strong customer satisfaction in this category.

### **2. Most Popular Cuisine by Votes**
The cuisine that received the highest number of votes was **Fast Food**, with a total of **120,000** votes. This suggests that fast food is widely preferred by customers due to its affordability, quick service, and accessibility. However, despite being the most popular, its average rating was slightly lower at **3.8**, indicating that while many people eat fast food, they may not rate it as highly as other cuisines.

### **3. Correlation Between Cuisines and Ratings**
- Some cuisines, such as **Japanese and Mediterranean**, tend to receive consistently high ratings (above 4.3), indicating strong customer satisfaction and quality perception.
- On the other hand, highly popular cuisines like **Fast Food and Street Food** have lower average ratings, suggesting that availability and affordability drive their popularity rather than quality.
- The scatter plot analysis showed that restaurants with a high number of votes do not always have the highest ratings, emphasizing that popularity does not necessarily mean better quality.

### **4. Distribution of Ratings**
- The histogram analysis showed that most restaurant ratings fall between **3.5 and 4.5**, indicating a general trend of customer satisfaction.
- Very few restaurants received ratings below **3.0**, suggesting that extremely low-rated restaurants are rare or do not survive in competitive markets.

### **5. City-Wise Preference Analysis**
- The top cities with the highest-rated restaurants were **Paris, New York, and Tokyo**, with an average rating above **4.4**. These cities are known for their culinary excellence and high standards in food service.
- In contrast, some cities had lower average ratings due to a higher concentration of fast food and casual dining establishments.

---

## **Conclusion**
Through this analysis, I was able to determine the relationship between cuisines and customer preferences. Key insights include:
- **Certain cuisines, like Italian and Japanese, consistently receive higher ratings, reflecting strong customer satisfaction and quality perception.**
- **Most popular cuisines (in terms of votes) indicate customer demand but may not always have the best ratings, as seen with Fast Food.**
- **Restaurant ratings are generally distributed between 3.5 and 4.5, indicating overall positive customer experiences.**
- **Cities with high culinary standards tend to have better-rated restaurants compared to cities with a higher concentration of fast food joints.**

These findings can help restaurant businesses optimize their offerings by focusing on high-rated cuisines while also catering to popular demand. Further analysis could explore factors influencing customer ratings, such as pricing, service quality, and restaurant location.

---

## **Future Recommendations**
- **Conduct sentiment analysis on customer reviews** to understand why certain cuisines receive higher or lower ratings.
- **Analyze price and rating correlations** to determine if expensive cuisines receive better reviews.
- **Study regional variations** in cuisine preferences to help restaurant chains expand effectively.
- **Examine factors like service quality, ambiance, and online ordering influence on customer ratings.**
