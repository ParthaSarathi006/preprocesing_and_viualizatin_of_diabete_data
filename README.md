# preprocesing_and_viualizatin_of_diabete_data

Here's a well-structured **`README.md`** file tailored for your **Diabetes Data Preprocessing and Visualization** notebook, formatted for GitHub and organized by topic with code snippets. This version presents code *centered in context* (GitHub doesn’t support center-aligned code blocks, so layout clarity is prioritized instead).

---

````markdown
# 🧠 Diabetes Data Preprocessing & Visualization

This repository contains a notebook demonstrating **data exploration** and **visualization techniques** using a diabetes dataset. It covers summary statistics, visual insights, and correlation analysis that can be used for EDA (Exploratory Data Analysis) in a machine learning workflow.

---

## 📁 Dataset

The dataset used is [`diabetes.csv`] located in your Google Drive:

```python
data = pd.read_csv('/content/drive/MyDrive/diabetes.csv')
````

---

## 📊 1. Data Exploration

Explore the structure, summary, and missing values:

```python
data.head()
data.info()
data.describe()
data.nunique()
data.isnull().sum()
```

---

## 📈 2. Basic Visualizations (Using Matplotlib)

### 🔹 BMI vs Age (Scatter Plot)

```python
x = data['BMI']
y = data['Age']
plt.scatter(x, y)
plt.xlabel('BMI')
plt.ylabel('Age')
plt.show()
```

### 🔹 BMI Line Plot

```python
plt.plot(x)
plt.show()
```

### 🔹 Age Histogram

```python
plt.hist(y)
plt.show()
```

### 🔹 Bar Plot of BMI vs Age

```python
plt.bar(x, y)
plt.xlabel('BMI')
plt.ylabel('Age')
plt.show()
```

### 🔹 Outcome Pie Chart

```python
A = data['Outcome']
plt.pie(A)
plt.show()
```

---

## 🌊 3. Visualizations Using Seaborn

### 🔹 Line Plot

```python
sns.lineplot(x)
```

### 🔹 Scatter Plot

```python
sns.scatterplot(x=x, y=y, data=data)
```

### 🔹 Outcome vs Age Bar Plot

```python
sns.barplot(x=data['Outcome'], y=y, data=data)
```

### 🔹 Age Distribution Plot

```python
sns.displot(x=y)     # Modern
sns.distplot(x=y)    # Deprecated in latest versions
```

### 🔹 Box Plot for BMI

```python
sns.boxplot(y=x, data=data)
```

### 🔹 Pair Plot with Hue (Outcome)

```python
sns.pairplot(data, hue='Outcome')
```

### 🔹 Heatmap for Correlation Matrix

```python
sns.heatmap(data.corr(), annot=True)
```

---

## 📚 Libraries Used

```python
import pandas as pd
import numpy as np
import matplotlib.pyplot as plt
import seaborn as sns
```

---

## ✅ Output

A set of plots and statistical summaries that:

* Help visualize the relationship between BMI, Age, and Outcome
* Understand distribution and variance in data
* Provide a correlation map for machine learning input features

---

## 📄 License

This project is licensed under the MIT License.

---

## 🙌 Acknowledgements

* [Seaborn Documentation](https://seaborn.pydata.org/)
* [Matplotlib Documentation](https://matplotlib.org/)
* Publicly available **Pima Indians Diabetes Dataset**

---

> Fork, visualize, and build your ML models on top of this clean EDA pipeline!




