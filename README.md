# Exploratory Data Analysis (EDA) – Titanic Dataset



---

## 1. Objective

The objective of this task is to perform **Exploratory Data Analysis (EDA)** on the Titanic dataset to understand its structure, distribution, correlations, and data quality. The insights gained through EDA are foundational for making the dataset suitable for building predictive models in later stages.

---

## 2. Tools and Libraries Used

The following tools and Python libraries were used for this task:

* **Pandas**: For data loading, cleaning, and summary statistics.
* **NumPy**: For numerical operations.
* **Matplotlib & Seaborn**: For creating static visualizations such as histograms, boxplots, and heatmaps.
* **Plotly Express**: For building interactive plots that aid in detailed data exploration.

---

## 3. Dataset Information

* **Dataset**: Titanic - Machine Learning from Disaster
* **Source**: [Kaggle - Titanic Dataset](https://www.kaggle.com/datasets/yasserh/titanic-dataset)
* **Format**: CSV
* **Features** include:

  * PassengerId, Name, Sex, Age, Fare, Ticket, Cabin, Embarked
  * Pclass (Passenger class), SibSp (Siblings/Spouses), Parch (Parents/Children)
  * Survived (Target variable)

---

## 4. Steps Followed in EDA

### 4.1. Data Loading

* Loaded the dataset using `pandas.read_csv()`.
* Created a duplicate dataset named `df_cleaned` to preserve the original data throughout the process.

### 4.2. Initial Data Inspection

* Inspected the shape, data types, and the presence of null values.
* Generated summary statistics using `.describe(include='all')`.

### 4.3. Handling Missing Values

* **Age**: Filled missing values with the **median** of the column.
* **Cabin**: Replaced missing values with the string `"Unknown"`, considering it a categorical feature.
* **Embarked**: Filled missing values with the **most frequent value (mode)**.
* Ensured that no missing values remained in the cleaned dataset.

### 4.4. Univariate Analysis

* **Histograms**: Plotted histograms to understand distributions of `Age`, `Fare`, etc.
* **Boxplots**: Used to detect outliers and visualize spread for numerical features like `Fare`.

### 4.5. Categorical Variable Analysis

* Count plots for features like `Sex` and `Embarked` to observe class distribution.

### 4.6. Bivariate and Multivariate Analysis

* **Correlation Heatmap**: Analyzed correlation between numerical features using `sns.heatmap()`.
* **Pairplot**: Visualized pairwise relationships between selected features using `sns.pairplot()`.

### 4.7. Interactive Visualization

* Created an interactive scatter plot using `Plotly` to observe how `Age` and `Fare` relate to survival.

### 4.8. Feature Engineering

* Applied `log1p` transformation on `Fare` to normalize its skewed distribution.
* Created a new feature `FamilySize` by combining `SibSp` and `Parch`.

### 4.9. Exporting Cleaned Dataset

* The cleaned dataset was saved as `titanic_cleaned.csv` for further use in modeling or additional analysis.

---

## 5. Key Findings

* **Missing Values**: Cabin had the highest percentage of missing data.
* **Age Distribution**: Slight right-skew; majority of passengers were between 20-40 years.
* **Survival Trends**:

  * Higher survival rates observed in females and passengers in Pclass 1.
  * Fare and Pclass are positively correlated with survival.
* **Correlations**: Strong positive correlation between `SibSp` and `Parch`, suggesting overlapping family features.

---

## 6. How to Run

### 6.1. Using Google Colab

* Open the notebook file in GitHub.
* Replace the GitHub URL with `githubtocolab.com` to launch it in Google Colab.

Example:

```text
https://github.com 
|
V 
https://githubtocolab.com
```

### 6.2. Locally (Using Jupyter Notebook)

1. Clone the repository:

   ```bash
   git clone https://github.com
   ```

2. Open the notebook using:

   ```bash
   jupyter notebook EDA-Titanic.ipynb
   ```

3. Ensure the following packages are installed:

   ```bash
   pip install pandas numpy matplotlib seaborn plotly
   ```

---

## 7. Files Included

| File Name             | Description                                   |
| --------------------- | --------------------------------------------- |
| `EDA-Titanic.ipynb`   | Jupyter Notebook containing full EDA process. |
| `Titanic-Dataset.csv`         | Original dataset from Kaggle.                 |
| `titanic_cleaned.csv` | Cleaned version of the dataset.               |
| `README.md`           | Task documentation and execution guide.       |

---

