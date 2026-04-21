# Visual Analytics of Diabetes Risk Using General Line Coordinates

**MSBD 570 Final Project – James Walton**

---

## 📌 Project Overview

This project explores multivariate patterns in diabetes risk using advanced visualization techniques on a large healthcare dataset.

The analysis focuses on understanding how multiple health indicators interact by applying:

* **General Line Coordinates (Parallel Coordinates)** for interpretable multivariate analysis
* **Principal Component Analysis (PCA)** for dimensionality reduction and structural insight

---

## 🎯 Objectives

* Identify combinations of health indicators associated with diabetes risk
* Compare high-dimensional visualization (GLC) with PCA
* Demonstrate the value of interactive visual analytics

---

## 📊 Dataset

* Source: CDC Behavioral Risk Factor Surveillance System (BRFSS) 2015
* Accessed via Kaggle (*Diabetes Health Indicators Dataset*)
* Records: ~253,680
* Features: 21 health-related variables

---

## ⚙️ Installation & Setup

### Clone the repository

```bash
git clone https://github.com/thurgoodj3/msbd570-final-project-James-Walton.git
cd msbd570-final-project-James-Walton
```

### Install dependencies

**Using pip:**

```bash
pip install -r requirements.txt
```

**OR using conda:**

```bash
conda env create -f environment.yml
conda activate diabetes-vis
```

---

## 🚀 Usage

Run the notebook:

```bash
jupyter notebook
```

Open:

```
Final_Project.ipynb
```

---

## 🔍 Project Workflow

### Data Preprocessing

* Type conversion (float → integer)
* Duplicate removal (~23K records removed)
* Feature normalization
* Label transformation for readability

### Parallel Coordinates (GLC)

* Multivariate visualization across features
* Interactive filtering and pattern exploration
* Identification of combined risk factors

### PCA Visualization

* Dimensionality reduction to 2D
* Cluster and overlap analysis
* Interactive scatterplots

---

## 🧪 Example

```python
from sklearn.preprocessing import StandardScaler
from sklearn.decomposition import PCA

X = diabetes.drop(columns=['Diabetes_012'])
y = diabetes['Diabetes_012']

X_scaled = StandardScaler().fit_transform(X)
X_pca = PCA(n_components=2).fit_transform(X_scaled)
```

---

## 📦 Dependencies

* Python 3.10+
* pandas
* numpy
* scikit-learn
* matplotlib
* seaborn
* plotly
* ydata-profiling

---

## ⚠️ Limitations

* Parallel Coordinates requires sampling due to overplotting
* PCA captures limited variance in 2D
* PCA components are not directly interpretable
* Large datasets may affect interactive performance

---

## 🔮 Future Work

* Apply **t-SNE / UMAP**
* Add **machine learning classification models**
* Implement **SHAP feature importance analysis**
* Build an **interactive dashboard (Dash or Streamlit)**

---

## 📬 Contact

**James Walton**
MSBD 570 – Spring 2026

GitHub: https://github.com/thurgoodj3

---

## 📄 License

This project is for academic use only.
