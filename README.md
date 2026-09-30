# Zomato Restaurant Exploratory Data Analysis (EDA) 📊

A data analytics project focused on uncovering restaurant market dynamics, customer engagement patterns, and pricing structures using a sample of the Zomato dataset. The pipeline is built entirely using **Python**, **Pandas**, **Matplotlib**, and **Seaborn**.

---

## 📈 Executive Summary & Core Insights

* **The Engagement King:** **Empire Restaurant** emerged as the single most voted establishment in the dataset, marking it as the leader in customer engagement.
* **Flawless Data Integrity:** Post-cleaning, the dataset maintains **148 fully intact rows** with **0 missing values** across all dimensions, ensuring analytical accuracy.
* **Pricing Density:** The couple cost analysis (`approx_cost(for two people)`) shows distinct dining price clusters, allowing clear classification of budget vs. premium dining formats.
* **Service Channel Synergy:** The final cross-tabulation heatmap maps how online ordering behavior adapts dynamically across different functional restaurant formats (e.g., Buffet, Dining).

---

## 📂 Repository Layout

```text
zomato-analysis/
├── venv/                 # ❌ EXCLUDED via .gitignore (Environment Sandbox)
├── zomato-data.csv       # 📊 Source Dataset (148 clean rows)
├── requirements.txt      # 📦 Dependencies (Pandas, Numpy, Seaborn, Matplotlib)
├── .gitignore            # 🛡️ Tracks files to exclude from Git
└── analysis.ipynb        # 📓 Main Notebook (Contains complete code & charts)
```

---

## 🛠️ Data Processing & Technical Workflow

### 1. Vectorized String Ingestion & Formatting
The text-heavy `"rate"` column (originally formatted as string metrics like `"4.1/5"` or containing anomalies like `"-"`) was passed through a cleaning framework to systematically isolate numerical data types, strip trailing spaces, and output clean `float64` decimals.

### 2. Statistical Aggregations
* **Multi-variable Grouping:** Aggregated total engagement metrics (`votes`) across specific distribution models (`listed_in(type)`) to evaluate customer feedback volumes.
* **Cross-Tabulation Matrix:** Leveraged `pd.pivot_table(..., aggfunc='size')` to dynamically monitor operational frequencies between brick-and-mortar setups and online ordering availability.

### 3. Visual Analytics Portfolio
* **Categorical Distribution:** Utilized Seaborn's `countplot` coupled with modern color maps (`viridis`, `coolwarm`) to contrast structural distributions.
* **Trend & Density Evaluation:** Built line plots (`plt.plot`) highlighting customer voting behavior alongside Matplotlib histograms evaluating structural rating scales.
* **Variance & Outlier Detection:** Implemented `sns.boxplot` to track visual summary statistics comparing `online_order` impacts against user ratings (`rate`).

---

## 🚀 Quick Setup & Local Execution

To replicate this environment sandbox and run the calculations on your system, execute these terminal commands inside **iTerm**:

```bash
# 1. Clone the repository and navigate into your folder
cd "Zomato Data Analysis Using Python"

# 2. Create virtual environment and activation
conda create -p **your-venv-name** python=3.12
conda activate **your-venv-name**

# 3. Synchronize package dependencies
pip install -r requirements.txt

# 4. Open the workspace
jupyter notebook
```
