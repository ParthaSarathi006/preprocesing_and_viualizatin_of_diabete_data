# ✅ Exploratory Data Analysis of Diabetes Patient Health Metrics

## 📌 Project Overview
This project performs exploratory data analysis (EDA) on the diabetes dataset to identify trends, relationships, and distributions within the health metrics. The analysis includes data preprocessing, visualization, and deriving meaningful insights.

---

## 🗃️ Dataset Information
- **Source:** Local file uploaded to Google Colab (`/content/drive/MyDrive/diabetes.csv`)
- **Format:** CSV
- **Number of Rows:** Varies (typically 768)
- **Number of Features:** 9

### Features:
- `Pregnancies`: Number of times pregnant
- `Glucose`: Plasma glucose concentration
- `BloodPressure`: Diastolic blood pressure (mm Hg)
- `SkinThickness`: Triceps skin fold thickness (mm)
- `Insulin`: 2-Hour serum insulin (mu U/ml)
- `BMI`: Body mass index (weight in kg/(height in m)^2)
- `DiabetesPedigreeFunction`: Diabetes pedigree function
- `Age`: Age in years
- `Outcome`: Class variable (0 or 1)

---

## 📊 Data Preprocessing
Performed the following steps:
- Loaded data using `pandas`
- Viewed initial data using `.head()`
- Inspected data types and nulls using `.info()` and `.isnull().sum()`
- Summarized using `.describe()` and `.nunique()`

---

## 📉 Exploratory Data Analysis (EDA)

### 🔸 Matplotlib Visualizations
- **Scatter Plot:** `BMI` vs `Age`
- **Line Plot:** Trend of BMI
- **Histogram:** Distribution of Age
- **Bar Plot:** Age by BMI
- **Pie Chart:** Outcome values (0 or 1)

### 🔹 Seaborn Visualizations
- `lineplot()` for BMI
- `scatterplot()` for BMI vs Age
- `barplot()` showing Outcome vs Age
- `displot()` and `distplot()` for Age
- `boxplot()` for BMI distribution
- `pairplot()` with `hue='Outcome'` for multi-feature comparison
- `heatmap()` for correlation matrix (with annotations)

---

## 🔍 Insights & Observations
- BMI and Age show a slight positive trend.
- Most patients have a BMI between 30-40.
- Patients with higher Age and BMI are more likely to have Outcome = 1 (diabetes positive).
- Strong correlations identified between some features such as Glucose and Outcome.

---

## 📌 Tools & Libraries Used
- `Pandas` for data manipulation
- `NumPy` for numerical operations
- `Matplotlib` for basic plotting
- `Seaborn` for advanced visualization

---

## 🧠 Future Scope
- Apply classification models (e.g., Logistic Regression, Random Forest)
- Feature importance analysis
- Create a Streamlit app for interactive visualization
- Model deployment using Flask or FastAPI

---

## 📷 Visualizations

```markdown
![Scatter Plot](images/scatter_bmi_age.png)
![Heatmap](images/correlation_matrix.png)
