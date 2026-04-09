
## **Aim**
To perform data preprocessing tasks including **data binning**, **data formatting**, and **basic data manipulation** using the Pandas and NumPy libraries in Python.

---

## **Theory**

### **1. Data Binning**
Data binning (or bucketing) is a data pre-processing technique used to reduce the effects of minor observation errors or to convert continuous numerical variables into discrete categorical "bins." 
* **Method:** You used `pd.cut()`.
* **Mechanism:** It segments and sorts data values into bins. In your code, you defined specific boundaries (e.g., `[0, 10000, 30000, 60000]`) and assigned labels like 'LOW', 'MEDIUM', and 'HIGH' to represent those ranges. This helps in identifying patterns, such as categorizing products by price range or sales volume.


### **2. Data Formatting (Type Conversion)**
Data formatting ensures that data is in the correct format for analysis. 
* **Method:** You used `.astype(float)`.
* **Mechanism:** Converting columns (like `Units_Sold`) from integers to floats is often necessary when you anticipate performing divisions or when the dataset requires a uniform decimal format for mathematical consistency.

### **3. String Manipulation**
In real-world datasets, text data is often inconsistent. 
* **Method:** You used `.str.upper()`.
* **Mechanism:** This converts all text in a specific column (like `Product`) to uppercase. This "canonicalization" prevents the computer from treating "Laptop" and "laptop" as two different products.

### **4. Data Sorting**
Sorting is essential for identifying trends, such as the most expensive items or the highest delivery times.
* **Method:** You used `.sort_values(by='Price', ascending=False)`.
* **Mechanism:** This rearranges the rows of the DataFrame based on the values of a selected column. Setting `ascending=False` places the highest values at the top.

### **5. Statistical Summarization**
* **Method:** You used `.unique()` and `.value_counts()`.
* **Mechanism:** `.unique()` identifies the distinct categories present in a column, while `.value_counts()` returns the frequency of each category. This is crucial for understanding the distribution of your "binned" data (e.g., how many 'LOW order' vs 'HIGH order' entries exist).

---

## **Conclusion**
Through this experiment, I successfully implemented data binning to transform continuous numerical data into meaningful categories. I also practiced essential data cleaning techniques, such as type casting, string normalization, and sorting. These processes are fundamental in preparing a raw dataset for advanced exploratory data analysis (EDA) and machine learning modeling.
