# **Cricket Player Performance Analysis**
---
## **About the Dataset**

### **1. Domain of the Data**
This dataset belongs to the **sports domain**, focusing specifically on cricket. It captures player performance statistics from cricket matches, including Test matches, with detailed information about individual innings.

### **2. Dataset Overview**
- **Rows:** 1999  
- **Columns:** 13  

### **3. Variable Types**
| **Variable**       | **Type**               | **Description**                                                                 |
|---------------------|------------------------|---------------------------------------------------------------------------------|
| `Player`           | Categorical - Nominal | Name of the cricket player.                                                    |
| `Runs`             | Numerical - Continuous| Number of runs scored by the player.                                           |
| `Mins`             | Numerical - Continuous| Minutes spent batting by the player.                                           |
| `BF`               | Numerical - Continuous| Balls faced by the player.                                                     |
| `4s`               | Numerical - Discrete  | Number of boundaries hit by the player.                                        |
| `6s`               | Numerical - Discrete  | Number of sixes hit by the player.                                             |
| `SR`               | Numerical - Continuous| Strike rate (calculated as `(Runs/BF)*100`).                                   |
| `Inns`             | Numerical - Discrete  | The innings number (1 or 2).                                                   |
| `Opposition`       | Categorical - Nominal | Opposing team in the match.                                                    |
| `Ground`           | Categorical - Nominal | Venue where the match was played.                                              |
| `Start Date`       | Categorical - Date/Time| The date when the match started.                                               |
| `NotOut`           | Categorical - Ordinal | Binary indicator (0 or 1) showing if the player was not out.                   |
| `Not_Out`          | Categorical - Nominal | A descriptive version of `NotOut` (e.g., "Yes" or "No").                       |

---

## **Exploratory Data Analysis (EDA)**

### **1. Statistical EDA**
- **Central Tendency and Dispersion Analysis:**  
  - **Mean, Median, Range, IQR, Standard Deviation** were calculated using the `.describe()` method.
- **Key Insights:**  
  - The data shows variability in player performance with outliers detected in runs scored.

### **2. Visual EDA**
#### **Univariate Analysis**
- **Histogram:** Distribution of runs scored.
- **Boxplot:** Detecting outliers and understanding data spread across opposition teams.

#### **Bivariate Analysis**
- **Scatter Plot:** Relationship between runs scored and match venues.

#### **Advanced Plots**
- **Violin Plot:** Distribution of runs scored across different opposition teams.
- **Pair Plot:** Pairwise relationships between all numerical variables for trend detection.

### **3. Outlier Detection**
- Outliers in the `Runs` variable were identified using boxplots and filtered for values greater than 300.

---

## **Project Workflow**

### **Step 1: Data Loading**
- Imported the dataset using `pandas` from an Excel file containing two sheets (`Sheet1` and `Sheet2`).

### **Step 2: Data Merging and Cleaning**
- Merged data from both sheets using `pd.merge()` based on the `Player` column.
- Removed duplicates using `.drop_duplicates()` and reset the index for a cleaner structure.

### **Step 3: Statistical Analysis**
- Analyzed key metrics using:
  - **Mean and Median:** Central tendency.
  - **Range and IQR:** Spread of data.
  - **Standard Deviation:** Data dispersion.

### **Step 4: Visualization**
- Visualized data using:
  - Histograms for `Runs` distribution.
  - Boxplots to detect outliers.
  - Scatter plots to analyze relationships between key variables.
  - Advanced visualizations like violin plots and pair plots using `Seaborn`.

---

## **Key Observations**

### **Performance Trends**
- Players tend to perform differently across various grounds and oppositions. Certain venues might provide a home advantage or be high-scoring pitches.

### **Time-Based Trends**
- Analyzing the `Start Date` variable shows whether player performance improves over time or follows seasonal patterns.

### **Outliers**
- Outliers represent either exceptional performances or recording errors. For example, scores over 300 runs are notable outliers.

---

## **Technologies Used**
- **Programming Language:** Python
- **Libraries:** `pandas`, `matplotlib`, `seaborn`
- **Tools:** Jupyter Notebook

---

## **Future Scope**
- Extend the analysis to include bowling and fielding statistics for a holistic view of player performance.
- Implement predictive models to forecast player performance based on historical data.
- Create dashboards using **Power BI** or **Tableau** for interactive visualizations.

---

## **Conclusion**
This project provides an in-depth analysis of cricket player performance, showcasing trends, patterns, and key insights. The analysis highlights the importance of data cleaning, statistical exploration, and visualization in extracting actionable insights.

