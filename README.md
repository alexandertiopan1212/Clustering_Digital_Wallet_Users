# 💳 Clustering Digital Wallet Users using K-Prototypes

**Segmentation of Digital Wallet Users Based on Survey Responses (Categorical + Numerical Data)**

## 📌 Project Overview

This project applies **K-Prototypes clustering algorithm** to segment digital wallet users based on their behavior and demographic survey data. K-Prototypes is ideal for datasets with mixed **numerical** and **categorical** attributes.

The primary goal is to:
- Understand usage behavior and user characteristics
- Identify homogeneous groups for targeted marketing strategies
- Generate insights from survey data involving students’ digital wallet habits

---

## 🧾 Dataset Description

- **Source**: Survey of 68 respondents
- **Columns**:
  - `Usia` (Age)
  - `Jenis Kelamin` (Gender)
  - `Income` (Monthly Income)
  - `Expense` (Monthly Spending)
  - `Alasan Utama Penggunaan` (Main Reason for Use)
  - `Frekuensi Penggunaan` (Usage Frequency)

All values are complete (no missing data).

---

## 🔍 Exploratory Data Analysis (EDA)

### 📊 Gender Distribution
- Female: 72%
- Male: 28%
- Both genders have similar averages in age, income, and frequency of use.

### 📊 Main Reason for Wallet Use
- Transfer: 63%
- Belanja (Shopping): 16%
- Promo/Cashback: 10%
- Tagihan (Bills): 9%
- Entertainment Voucher: 1%

### 💡 Behavioral Insights
- Transfer users have **moderate income and high frequency**
- Promo/cashback users have **lower income and lower frequency**
- Shoppers have **highest frequency** (avg 8.36x/month)

---

## 🧠 Clustering with K-Prototypes

### ✨ Why K-Prototypes?
K-Prototypes handles both **numerical (e.g. age, income)** and **categorical (e.g. gender, usage reason)** data types, making it suitable for survey-based behavioral segmentation.

### 🔍 Determining Optimal Clusters (Elbow Method)
- Tried K from 1 to 8
- Cost drops significantly until **K = 3**

### ✅ Final Model
- **K = 3**
- `kprototype.fit_predict(...)`
- Fitted in just 2 iterations
- Cost: ~9.9 trillion

---

## 📊 Cluster Insights

### 🟢 Cluster 0
- **High-income, high-expense users**
- Avg income: Rp 3,166,667
- Usage: Moderate (5.5x/month)
- Mostly females using wallets for **Tagihan (Bills)**

### 🔵 Cluster 1
- **Lower-income but consistent users**
- Avg income: Rp 813,750
- Usage: 4.1x/month
- Predominantly female users for **Transfer**

### 🔴 Cluster 2
- **Mid-high income and highest usage**
- Avg income: Rp 1.63 million
- Usage: 9.4x/month
- Mix of reasons: Belanja & Transfer
- Gender mix more balanced

---

## 📈 Visualization

All EDA visualized using:
- `plotnine` (ggplot-like in Python)
- Grouped bar charts for:
  - Gender breakdown
  - Usage frequency
  - Income & Expense distribution
  - Purpose of usage

---

## 🧰 Tools & Libraries

- Python
- pandas, plotnine, seaborn
- scikit-learn (for encoding)
- kmodes (K-Prototypes implementation)
- warnings, numpy

---

## 💡 Key Takeaways

- **Transfer** is the dominant use case across all segments
- **High-usage users** spend significantly more, indicating potential for loyalty programs
- **Promo/cashback-driven users** may require incentivization to improve frequency
- Clustering offers a **data-driven segmentation** strategy for wallet providers

---

## ✍️ Author

**Alexander Tiopan**  
📫 alexandertiopan1212@gmail.com  
🔗 GitHub: [alexandertiopan1212](https://github.com/alexandertiopan1212)

