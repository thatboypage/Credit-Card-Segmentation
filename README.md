# Credit-Card-Segmentation
This project performs a comprehensive unsupervised learning analysis to segment credit card customers based on their behavior. The goal is to identify distinct customer groups that can help financial institutions tailor marketing strategies and improve customer satisfaction.

---

## 🧠 Project Objective

To apply **clustering techniques** to segment customers using their credit card usage behavior, and provide **actionable insights** for business decision-making.

---

## 📊 Dataset

The dataset used in this project contains the following features:

* `Customer ID`
* `Balance`, `Balance Frequency`
* `Purchases`, `One-off Purchases`, `Installment Purchases`
* `Cash Advance`
* `Purchase Frequency`, `One-off Purchase Frequency`, `Installment Purchase Frequency`
* `Cash Advance Frequency`, `Cash Advance Trx`
* `Purchases Trx`, `Credit Limit`, `Payments`, `Minimum Payments`, `Tenure`

> The dataset has been preprocessed to handle null values and standardize features before clustering.

---

## 🔧 Tools & Technologies

* Python
* NumPy, Pandas
* Scikit-learn
* Seaborn, Matplotlib
* Jupyter Notebook

---

## 🔍 Methodology

### 1. Data Preprocessing

* Dropped the `CUST_ID` column as it is not needed for clustering.
* Handled missing values using median imputation.
* Scaled all numerical features using `StandardScaler`.

### 2. Dimensionality Reduction

* Applied **Principal Component Analysis (PCA)** to reduce features for visualization while preserving variance.

### 3. Clustering

* Performed **KMeans Clustering**.
* Used the **Elbow Method** and **Silhouette Score** to determine the optimal number of clusters, which was found to be **2**.
* DBSCAN was explored but not used in the final analysis.

### 4. Visualization

* 2D scatter plot using PCA components for cluster visualization.
* Boxplots used to understand feature differences between clusters.

---

## 💡 Insights

The customer base was segmented into **2 distinct groups**:

* **Cluster 0**: Customers with relatively **higher usage** patterns — including purchases, cash advances, and payments — indicating active and possibly high-value customers.
* **Cluster 1**: Customers with **lower usage** patterns — potentially dormant or low engagement customers.

> These insights enable targeted strategies, such as offering loyalty rewards to active customers or re-engagement campaigns for low-usage ones.

---

## 🚀 How to Run

1. Clone this repository:

   ```bash
   git clone https://github.com/yourusername/credit-card-segmentation.git
   cd credit-card-segmentation
   ```

2. Install the required libraries:

   ```bash
   pip install -r requirements.txt
   ```

3. Run the notebook:

   ```bash
   jupyter notebook Credit_Card_Segmentation.ipynb
   ```

---

## 📁 Repository Structure

```
├── Credit_Card_Segmentation.ipynb  # Main notebook with code and analysis
├── README.md                       # Project documentation
├── requirements.txt               # Python dependencies (to be added)
└── data/                          # (Optional) Folder for storing dataset
```

---

## 📌 Future Work

* Apply other clustering algorithms like **Gaussian Mixture Models**.
* Incorporate time-series features for longitudinal behavior analysis.
* Build an interactive dashboard using **Streamlit** or **Dash**.

---

## 📬 Contact

For questions or collaboration, reach out via GitHub or email.
