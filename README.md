# crime-data-clustering-svd
Exploratory data analysis and K-Means clustering on crime statistics to identify regional safety clusters and patterns.

# Crime Data Segmentation & Clustering Analysis

## 1. Business Problem
### 1.1. What is the business objective?
The primary objective is to analyze regional crime statistics (such as rates of murder, assault, and urban population metrics) using unsupervised machine learning. By grouping states or regions into distinct clusters based on crime profiles, law enforcement agencies and policy-makers can identify high-risk areas, allocate resources efficiently, and formulate targeted intervention or crime-prevention strategies.

### 1.2. Are there any constraints?
* **Differing Scales:** Crime metrics (e.g., murder rates vs. percent urban population) are measured on different scales, requiring strict feature scaling or normalization to prevent distance metrics from being biased toward larger numerical values.
* **Outliers:** Certain regions may exhibit unusually high or low crime rates, which can heavily skew clustering boundaries if not appropriately handled during preprocessing.
* **Interpretability:** Clusters must clearly delineate safety tiers or crime characteristics so that non-technical stakeholders can easily draw actionable insights.

---

## 2. Data Dictionary
*(Adjust or verify based on your specific columns in `crime_data.csv`)*

| Feature Name | Data Type | Description |
| :--- | :--- | :--- |
| **State / City** | Categorical / String | Name of the state or region being analyzed. |
| **Murder** | Numeric | Murder arrests (per 100,000 residents). |
| **Assault** | Numeric | Assault arrests (per 100,000 residents). |
| **UrbanPop** | Numeric | Percent of the population living in urban areas. |
| **Rape** | Numeric | Rape arrests (per 100,000 residents). |

---

## 3. Exploratory Data Analysis (EDA)
* **3.1. Summary:** Descriptive statistical overview (mean, median, standard deviation, min, max) of all crime indicators and population metrics.
* **3.2. Univariate Analysis:** Visualizing the distribution and skewness of individual crime categories across regions using histograms and box plots.
* **3.3. Bivariate Analysis:** Examining correlations between urban population density and various crime rates (e.g., how population concentration correlates with assault or murder rates).

---

## 4. Data Pre-processing
* **4.1. Data Cleaning & Feature Engineering:** Checked for missing values, handled outliers, and separated non-numeric location labels before model training.
* **Normalization:** Applied standard scaling (StandardScaler / MinMaxScaler) to normalize features so they contribute equally to distance-based algorithms.

---

## 5. Model Building
* **5.1. Scaled Data Modeling:** Implemented clustering algorithms on the normalized feature set.
* **5.2. K-Means Clustering & Scree Plot:** Utilized the Elbow Method (plotting Within-Cluster Sum of Squares against the number of clusters) to determine the optimum number of clusters ($k$).
* **5.3. Cluster Validation & Insights:** Validated performance across different cluster sizes, assigned descriptive safety/crime tier labels, and compared results.

---

## 6. Business Benefits & Impact
Providing this data-driven clustering solution offers key benefits:
* **Resource Allocation:** Enables law enforcement and state authorities to deploy budget and personnel efficiently to high-risk cluster zones.
* **Targeted Policies:** Helps policy-makers design region-specific safety and social intervention programs tailored to specific crime profiles.
* **Risk Assessment:** Facilitates objective categorization of geographic safety levels for administrative planning.
