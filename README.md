# Customer Segmentation with Unsupervised Learning

This project aims to segment customers into meaningful groups using unsupervised machine learning techniques such as K-Means and Hierarchical Clustering. The goal is to help businesses better understand their customers and apply targeted marketing strategies based on behavioral and demographic data.

---

## Project Structure

- Exploratory Data Analysis (EDA): Statistical summaries, distribution plots, and correlation analysis.
- Feature Scaling: StandardScaler applied before clustering.
- Dimensionality Reduction: PCA used to project data into 2D space for visualization.
- K-Means Clustering: Optimal `k` chosen using Elbow and Silhouette methods.
- Hierarchical Clustering: Verified with dendrogram and AgglomerativeClustering model.
- Segment Analysis: Detailed business interpretations of each cluster.
- Visualization: PCA scatter plots with color-coded clusters.

---

## Dataset

- Source: [Kaggle – Mall Customers Dataset](https://www.kaggle.com/vjchoudhary7/customer-segmentation-tutorial)
- Rows: 200
- Columns:
  - CustomerID
  - Gender
  - Age
  - Annual Income (k$)
  - Spending Score (1-100)

---

## Clustering Models Used

### 1. K-Means Clustering

- PCA visualization shows well-separated clusters.
- `k=6` chosen using Elbow + Silhouette Score.
- Resulting segments analyzed with mean values.

### 2. Hierarchical Clustering

- Dendrogram used to estimate optimal clusters.
- AgglomerativeClustering model trained with `k=6`.
- Results visually aligned with K-Means segments.

---

## Business Insights (Sample)

| Segment | Description              | Strategy Suggestion                        |
| ------- | ------------------------ | ------------------------------------------ |
| 1       | Affluent & High-Spending | Luxury campaigns, exclusive offers         |
| 2       | Young but High-Spending  | Online/mobile-first promotions             |
| 4       | Wealthy but Low-Spending | Education-based value communication        |
| 5       | Low-Income, Low-Spending | Retention automation or minimal investment |

> Full segment analysis is included in the notebook.

---

## Technologies Used

- Python (Pandas, NumPy, Matplotlib, Seaborn, Scikit-learn)
- Jupyter Notebook, Jupyter Lab
- Git & GitHub

---

## Repository Structure

```bash
customer-segmentation-project/
├── data/
│   └── Mall_Customers.csv
├── notebooks/
│   └── 01-EDA-customer-segmentation.ipynb
├── visuals/
│   └── cluster_plots.png
├── scripts/
├── models/
├── README.md
├── requirements.txt
└── .gitignore
```

---

---

## 💾 Model Saving & Reusability

The final K-Means clustering model was saved using the `joblib` module in `.pkl` format to ensure reusability and compatibility with deployment environments.

```python
import joblib

# Save the trained model
joblib.dump(kmeans, "models/kmeans_model.pkl")

# To load the model later:
loaded_model = joblib.load("models/kmeans_model.pkl")


---

## Author

- Samed Demir
- Linkedin: (https://www.linkedin.com/in/samed-demir/)
```
