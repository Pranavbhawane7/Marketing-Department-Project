
# Credit Card Customer Segmentation for Targeted Marketing

---

## 📌 Project Overview

This project focuses on segmenting credit card customers based on their spending habits, payment behavior, credit utilization, and transaction patterns.

The goal is to help banks understand customer behavior and develop targeted marketing strategies using unsupervised machine learning.

The project explores **K-Means Clustering, Principal Component Analysis (PCA), and a Deep Autoencoder** to identify meaningful customer segments.

---

## 🎯 Business Problem

Banks serve customers with different spending habits, payment patterns, and financial behaviors. Sending the same marketing offers to every customer can result in ineffective campaigns and missed business opportunities.

**Objective:** Segment credit card customers into meaningful groups to support personalized marketing strategies and improve customer engagement.

---

## 🎯 Project Objectives

- Perform Exploratory Data Analysis (EDA).
- Identify and handle missing values.
- Standardize numerical features.
- Apply K-Means clustering to group similar customers.
- Use PCA for dimensionality reduction and visualization.
- Build a Deep Autoencoder to learn compressed representations.
- Apply K-Means clustering to the encoded features.
- Explore business applications of customer segmentation.

---

## 📊 Dataset Description

The dataset contains **8,950 customer records and 18 columns**, including a customer identifier and 17 behavioral features.

The dataset includes information about account balances, purchases, cash advances, transaction frequency, credit limits, and payment behavior.

### Key Features

| Feature | Description |
|---|---|
| `CUST_ID` | Unique customer identifier |
| `BALANCE` | Outstanding account balance |
| `BALANCE_FREQUENCY` | Frequency of balance updates |
| `PURCHASES` | Total purchase amount |
| `ONEOFF_PURCHASES` | Amount spent on one-time purchases |
| `INSTALLMENTS_PURCHASES` | Amount spent on installment purchases |
| `CASH_ADVANCE` | Total cash advance amount |
| `PURCHASES_FREQUENCY` | Frequency of purchases |
| `ONEOFF_PURCHASES_FREQUENCY` | Frequency of one-time purchases |
| `PURCHASES_INSTALLMENTS_FREQUENCY` | Frequency of installment purchases |
| `CASH_ADVANCE_FREQUENCY` | Frequency of cash advances |
| `CASH_ADVANCE_TRX` | Number of cash advance transactions |
| `PURCHASES_TRX` | Number of purchase transactions |
| `CREDIT_LIMIT` | Credit limit assigned to the customer |
| `PAYMENTS` | Total payment amount |
| `MINIMUM_PAYMENTS` | Minimum payment amount |
| `PRC_FULL_PAYMENT` | Proportion of full payments |
| `TENURE` | Duration of credit card service |

---

## 🛠️ Technologies Used

- **Python** — Programming language
- **Pandas** — Data manipulation and analysis
- **NumPy** — Numerical computing
- **Matplotlib** — Data visualization
- **Seaborn** — Statistical visualization
- **Scikit-learn** — Preprocessing, PCA, and K-Means
- **TensorFlow / Keras** — Deep Autoencoder
- **Jupyter Notebook** — Interactive development

---

## 🔄 Project Workflow

1. Data loading and inspection
2. Exploratory Data Analysis (EDA)
3. Missing-value treatment
4. Feature selection and preprocessing
5. Feature standardization
6. K-Means clustering
7. Cluster-count exploration using the Elbow Method
8. Dimensionality reduction using PCA
9. Deep Autoencoder development and training
10. K-Means clustering on encoded features
11. Visualization and interpretation of customer segments

---

## ⚙️ Methodology

### 1. Data Preprocessing

- Inspect the dataset for missing values and inconsistencies.
- Remove `CUST_ID` from the modeling features.
- Impute missing values in `MINIMUM_PAYMENTS` and `CREDIT_LIMIT` using their column means.
- Standardize numerical features using `StandardScaler`.

### 2. Exploratory Data Analysis (EDA)

- Examine feature distributions.
- Explore customer purchase and balance patterns.
- Investigate payment and cash advance behavior.
- Analyze correlations between numerical features.
- Visualize relationships between customer characteristics.

### 3. K-Means Clustering

K-Means is an unsupervised learning algorithm that groups similar observations into clusters.

The Elbow Method is used to examine within-cluster sum of squares (WCSS) across different cluster counts.

The notebook applies K-Means to the standardized customer features using **8 clusters**.

### 4. Principal Component Analysis (PCA)

PCA reduces the standardized feature set to two principal components, allowing customer patterns and cluster assignments to be visualized in a lower-dimensional space.

PCA provides a linear dimensionality-reduction approach for comparison with the autoencoder.

### 5. Deep Autoencoder

A Deep Autoencoder learns a compressed representation of input data and attempts to reconstruct the original input.

- **Encoder:** Compresses the customer features.
- **Latent representation:** Stores the learned compressed features.
- **Decoder:** Reconstructs the original features.

The notebook uses a **10-dimensional encoded representation** and trains the network using reconstruction loss.

### 6. Clustering on Encoded Features

K-Means is applied to the autoencoder's encoded representation using **4 clusters**.

The project explores two approaches:

- **PCA + K-Means:** Uses a linear, two-dimensional representation.
- **Autoencoder + K-Means:** Uses a learned, nonlinear, 10-dimensional representation.

The number of clusters alone does not establish which method performs better. Further evaluation is required to compare cluster quality and business usefulness.

---

## 💼 Business Applications

Customer segmentation can support potential marketing activities such as:

- Personalized rewards and cashback offers.
- Installment-based purchase promotions.
- Engagement campaigns for customers with low purchase activity.
- Product recommendations based on spending patterns.
- Tailored communication strategies for different customer groups.

These are potential applications, not measured business outcomes from a deployed campaign.

---

## 🚀 How to Run the Project

### Prerequisites

Install Python and Jupyter Notebook.

### Step 1: Clone the Repository

```bash
git clone https://github.com/Pranavbhawane7/Marketing-Department-Project.git
cd Marketing-Department-Project
```

### Step 2: Install Dependencies

```bash
pip install pandas numpy matplotlib seaborn scikit-learn tensorflow jupyter
```

### Step 3: Launch Jupyter Notebook

```bash
jupyter notebook
```

Open `marketing_data.ipynb` and run the cells in sequence.

**Note:** Ensure the dataset file is available in the working directory and its filename matches the filename referenced in the notebook.

---

## 📁 Repository Structure

```text
Marketing-Department-Project/
├── README.md
├── Marketing_Data.csv
└── marketing_data.ipynb
```

---

## 🔮 Future Improvements

- Evaluate clustering performance using silhouette scores.
- Profile clusters using the original customer features.
- Compare PCA-based and autoencoder-based clustering with consistent metrics.
- Investigate outliers and alternative imputation methods.
- Document dependency versions for reproducibility.
- Build an interactive customer segmentation dashboard using Power BI.
- Validate segment usefulness using actual marketing campaign results.

---

## 📝 Conclusion

This project explores how unsupervised machine learning can be used to identify patterns in credit card customer behavior.

By combining EDA, feature standardization, PCA, K-Means clustering, and a Deep Autoencoder, it investigates different approaches to customer segmentation.

The resulting segments can provide a foundation for personalized marketing strategies and data-driven decision-making.

---

## 👨‍💻 Author

**Pranav Bhawane**

- GitHub: [Pranavbhawane7](https://github.com/Pranavbhawane7)
- Repository: [Marketing-Department-Project](https://github.com/Pranavbhawane7/Marketing-Department-Project)
