## Experiment 14: Data Binning and Data Formatting using Python

**Aim:** To perform data preprocessing techniques including data binning, formatting, normalization, and categorical variable conversion using Python's Pandas and NumPy libraries.

---

### Theory of Operations

#### 1. Data Binning
Data binning (or bucketing) is a process of grouping a specific number of continuous values into a smaller number of "bins." In your code, `pd.cut()` is used to transform numerical columns like `Price` and `Order_Value` into categorical groups (e.g., LOW, MEDIUM, HIGH). This helps in reducing the effects of minor observation errors and makes the data easier to analyze for patterns.

#### 2. Data Formatting
Formatting ensures that data is consistent and in the correct type for computation. Your experiment demonstrates several key formatting tasks:
* **Type Conversion:** Using `.astype(float)` to ensure numerical columns are treated as floating-point numbers.
* **String Manipulation:** Using `.str.upper()` to standardize text data, ensuring "Laptop" and "laptop" would be treated identically.
* **Rounding:** Using `.round()` to limit decimal precision for cleaner reporting.

#### 3. Data Sorting and Inspection
Sorting data using `.sort_values()` (both ascending and descending) allows for quick identification of outliers or top-performing entries. Using `.unique()` and `.value_counts()` helps in understanding the distribution of categorical data after binning.

#### 4. Data Normalization
The experiment includes loading a dataset specifically for normalization. Normalization is the process of scaling numerical features to a standard range (usually 0 to 1 or -1 to 1). This is crucial when features have different units (e.g., comparing `Price` in thousands vs. `Rating` out of 5) to prevent one feature from dominating the model during analysis.

#### 5. Turning Categorical Variables into Quantitative Variables
Machine learning models generally require numerical input. The final section of your code prepares a student dataset to convert text-based categories (like `Gender` or `Placement_Status`) into quantitative formats, such as "One-Hot Encoding" or "Label Encoding," so they can be processed mathematically.

---

### Conclusion
By completing this experiment, we successfully demonstrated how to clean and restructure raw data into a format suitable for analysis. We concluded that **data binning** simplifies complex numerical distributions, while proper **formatting and normalization** ensure consistency and prevent bias in data processing. These steps are fundamental to any data science pipeline to ensure the accuracy and reliability of subsequent results.
