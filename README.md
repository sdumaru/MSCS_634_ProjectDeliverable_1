# Course: MSCS 634 - Advanced Data Mining for Data-Driven Insights and Predictive Modeling  

## Deliverable 1: Data Collection, Cleaning, and Exploration
**Dataset:** Adult Income Dataset (UCI Machine Learning Repository)  
**Author:** Sujan Dumaru  

---

## Dataset Summary and Key Insights

The Adult Income dataset includes over 32,000 records and 14 attributes capturing demographic, educational, occupational, and financial details of individuals. The goal is to predict whether a person's income exceeds $50K per year.

Key insights from analysis:

- Most individuals are aged between 25–45 and work around 40 hours per week.
- Higher education levels (bachelor's, master's, etc.) are positively associated with higher income.
- Capital gain and loss features are highly skewed, with most values being zero.
- Outliers were present in `capital-gain`, `hours-per-week`, and `age`, which were managed using the IQR method.

---

## Major Steps in Data Cleaning and Exploration

1. **Missing Value Handling**:  
   - Imputed missing values in `workclass`, `occupation`, and `native-country` using the mode.

2. **Duplicate Removal**:  
   - Identified and removed duplicate rows to maintain data quality and prevent bias in modeling.

3. **Standardizing Categorical Variables**:  
   - Converted all string columns to lowercase and stripped whitespace to ensure consistent labeling.

4. **Outlier Detection and Removal**:  
   - Applied the Inter Quartile Range (IQR) method to filter out extreme values in numeric fields like `capital-gain`, `hours-per-week`, and `age`.

5. **Exploratory Data Analysis (EDA)**:  
   - Used histograms, boxplots, and count plots to understand variable distributions and relationships.
   - Reordered education levels in visualizations for logical interpretation.

---

## Challenges Encountered and Solutions

- **Inconsistent Categorical Formatting**:  
  Some category labels had extra spaces or mixed casing. This was resolved using `str.strip().str.lower()`.

- **Duplicate Records**:  
  While the dataset is often considered clean, duplicates were found and removed using `df.duplicated()` and `drop_duplicates()`.

- **Skewed Financial Features**:  
  `capital-gain` and `capital-loss` had extreme values. These were cleaned using IQR to improve model reliability.

---

## Final Note

The dataset is now cleaned, consistent, and ready for modeling in subsequent project phases (e.g., regression, classification, clustering). The EDA also provided valuable direction for feature selection and transformation.
