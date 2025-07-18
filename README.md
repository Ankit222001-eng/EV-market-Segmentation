
#  EV Market Segmentation Based on Age (India)

This project focuses on **segmenting the Indian EV market based on the age of the customers**, using demographic and income data from an automobile buying behavior dataset. The goal is to identify which age groups are most likely to adopt Electric Vehicles (EVs) and how their preferences vary in terms of price, salary, and other features.

---

##  Dataset Overview

**Primary Dataset:** `Indian automoble buying behavour study 1.0.csv`

| Column             | Description                            |
|--------------------|----------------------------------------|
| Age                | Age of the individual buyer            |
| Profession         | Salaried / Business                    |
| Marrital Status    | Married / Single                       |
| Education          | Graduate / Post Graduate               |
| No of Dependents   | Number of dependent family members     |
| Personal loan      | Whether buyer has a personal loan      |
| House Loan         | Whether buyer has a housing loan       |
| Wife Working       | Wife is employed or not                |
| Salary             | Individual's annual salary             |
| Wife Salary        | Annual salary of spouse (if working)   |
| Total Salary       | Sum of individual and spouse salary    |
| Make               | Car model                              |
| Price              | Price of the car owned (in INR)        |

---

##  Exploratory Data Analysis (EDA)

- **Age distribution**: Majority of buyers fall in the 26–38 age range.
- **Loan effect**: Personal and home loans do not strongly influence EV buying.
- **Salary vs Price**: Even high salary groups prefer affordable EVs.
- **Make vs Price**: Some models (like Verna) show wider price range preferences.
- **Dependents vs Price**: No strong correlation observed.
- **Education vs Salary/Price**: Minor difference, not dominant.

**Correlation Heatmap** shows strong correlation between:
- Salary & Total Salary
- Total Salary & Price

---

## 🧪 Data Preprocessing

- **Label Encoding**: Applied to categorical features (`Profession`, `Marrital Status`, etc.)
- **Feature Scaling**: Standardized all numerical features using `StandardScaler`.

---

## 📈 Clustering (KMeans)

Used **KMeans** to segment customers based on scaled features.

- **Elbow Method**: Optimal clusters = 3
- **Interpretation of Clusters**:

| Cluster | Age Group   | Income Range     | Preference                     |
|---------|-------------|------------------|--------------------------------|
| 0       | 45–51       | Very High         | Premium EVs                    |
| 1       | 20–30       | Moderate          | Low-to-mid range EVs          |
| 2       | 30–45       | Average to High   | Wide range, from mid to high  |

- **Visualizations**:
  - `sns.pairplot()` for age, salary, wife salary, total salary, and price.
  - Boxplots and heatmaps for pattern identification.

---

## 💡 Insights & Recommendations

1. **Target Age Group**: 26–38 years
2. **Preferred Price Range**: ₹8–15 Lakhs
3. **Product Strategy**:
   - Compact SUVs and hatchbacks
   - Feature-rich and efficient models
   - Urban use-case design
4. **Marketing Strategy**:
   - Focus on salaried professionals
   - Highlight fuel economy, EMI benefits, and modern features

---

## 📦 Additional Brand-Level Analysis

Used secondary dataset (`evdataset3.csv`) to analyze global EV brands:

- Mapped Euro prices to INR
- Found high-efficiency EVs available at relatively lower prices
- Plotted:
  - Brand vs Efficiency
  - Brand vs Price
  - Efficiency vs Price

---

## 🛠️ Technologies Used

- Python
- Pandas
- NumPy
- Matplotlib
- Seaborn
- Scikit-learn

---

## 📁 How to Run

```bash
pip install pandas matplotlib seaborn scikit-learn
python analysis.py  # Or run the Jupyter notebook
