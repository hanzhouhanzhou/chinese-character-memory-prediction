# 🧠 Chinese Character Memory Prediction

## 🎯 Project Goal

This project investigates how **visual and structural properties of Chinese characters**
relate to **human visual–verbal memory retention (ACC)**.

The primary focus is on **exploratory data analysis and feature understanding**.
Machine learning models are used as supporting tools rather than the main narrative.

---

## 🗺️ Overall Pipeline

🧩 End-to-end analytical workflow:

![Pipeline](images/Pipeline/Pipeline.png)

---

## 📦 Data Overview

- **Samples**: Chinese characters  
- **Target variable**: Memory retention score (**ACC**, range 0–1)
- **Feature groups**:
  - 🧱 Structural features (stroke count, radicals, composition)
  - 🧠 Psycholinguistic features (AoA, familiarity)
  - 🖼️ Visual image-based features (used later)

---

## 🎯 Target Variable Analysis (ACC)

### 📊 Distribution of ACC

![ACC Histogram](images/Pipeline/Histogram%20of%20the%20Target%20Variable%20(ACC).PNG)

- Strong left-skewness
- Clear ceiling effect near 1.0
- Indicates non-normality and motivates transformation / robust modeling

---

### 📦 Boxplot of ACC

![ACC Boxplot](images/Pipeline/Boxplot%20of%20the%20target%20variable%20.png)

- Most values concentrated at high ACC
- Long tail of lower-retention characters
- Presence of outliers confirmed

---

## 🧹 Data Quality Check

### 🚨 Missing Values Summary

![Missing Values Summary](images/Pipeline/Missing%20Values%20Summary.png)

---

### 📋 Missing Values Across Features

![Missing Values Across Features](images/Pipeline/Summary%20of%20Missing%20Values%20Across%20Features)

- Missingness is feature-dependent
- Some psycholinguistic variables contain substantial gaps
- Decisions on exclusion or handling were made accordingly

---

## 🔍 Exploratory Feature Analysis

### 🔗 Correlation Matrix (Numeric Features + ACC)

![Correlation Matrix](images/Pipeline/Correlation%20Matrix%20of%20Predictive%20Numeric%20Features.png)

Key observations:

- Familiarity and frequency-related features show moderate correlation with ACC
- Structural features exhibit internal correlations
- No extreme multicollinearity directly with ACC

---

### 🌳 Hierarchically Clustered Correlation Heatmap

![Clustered Correlation Heatmap](images/Pipeline/Hierarchically%20Clustered%20Correlation%20Heatmap.png)

- Reveals feature clusters beyond pairwise correlations
- Highlights redundancy groups among structural variables
- Supports later feature grouping and modeling decisions

---

## 🤖 Modeling (Brief Overview)

- Regression-based models (linear, regularized, tree-based)
- CNN-based image features used as complementary signals
- Ensemble strategies explored at a conceptual level

📌 Modeling serves as validation rather than the main contribution.

---

## 🧠 Key Takeaways

- Memory retention (ACC) is highly skewed and non-Gaussian
- Structural and psycholinguistic features provide partial explanatory power
- Strong internal feature structure justifies careful feature handling
- Data understanding precedes and constrains model performance

---




## 🛠 Tools

Python · pandas · matplotlib · scikit-learn · PyTorch

---

## 📌 Notes

Full implementation details are available in the accompanying notebook.
This repository emphasizes **analytical reasoning supported by modeling results**.

