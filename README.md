# 🧠 Chinese Character Memory Prediction

## 🎯 Project Goal

This project investigates how **visual and structural properties of Chinese characters**
relate to **human visual–verbal memory retention (ACC)**.

The primary focus is on **exploratory data analysis and feature understanding**.
Machine learning models are used as supporting tools rather than the main narrative.

---

## 🗺️ Overall Pipeline

**Figure 1. End-to-end analytical workflow**

*Overview of data processing, feature analysis, and modeling strategy.*

![Pipeline Overview](images/Pipeline/Pipeline.png)

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

**Figure 2. Distribution of memory retention score (ACC)**

*Histogram showing the skewed distribution and ceiling effect of ACC.*

![ACC Histogram](./images/Histogram%20ACC.png)

- Strong left-skewness  
- Clear ceiling effect near 1.0  
- Indicates non-normality and motivates transformation / robust modeling  

---

### 📦 Boxplot of ACC

**Figure 3. Boxplot of ACC values**

*Visual summary of central tendency, spread, and outliers.*

![ACC Boxplot](./images/Boxplot%20ACC.png)

- Most values concentrated at high ACC  
- Long tail of lower-retention characters  
- Presence of outliers confirmed  

---

## 🧹 Data Quality Check

### 🚨 Missing Values Summary

**Figure 4. Summary of missing values across variables**

*Counts of missing observations per feature.*

![Missing Values Summary](./images/Missing%20Values%20Summary.png)

---

### 📋 Missing Values Across Features

**Figure 5. Missing value distribution by feature**

*Feature-level inspection of data completeness.*

![Missing Values](./images/Missing%20Values.png)

- Missingness is feature-dependent  
- Some psycholinguistic variables contain substantial gaps  
- Decisions on exclusion or handling were made accordingly  

---

## 🔍 Exploratory Feature Analysis

### 🔗 Correlation Matrix (Numeric Features + ACC)

**Figure 6. Pearson correlation matrix**

*Pairwise correlations among numeric features and ACC.*

![Correlation Matrix](./images/Correlation%20Matrix.png)

Key observations:

- Familiarity and frequency-related features show moderate correlation with ACC  
- Structural features exhibit internal correlations  
- No extreme multicollinearity directly with ACC  

---

### 🌳 Hierarchically Clustered Correlation Heatmap

**Figure 7. Hierarchical clustering of feature correlations**

*Correlation structure revealed through hierarchical clustering.*

![Hierarchical Correlation](./images/Hierarchically.png)

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


## 🛠 Tools

Python · pandas · matplotlib · scikit-learn · PyTorch

---

## 📌 Notes

Full implementation details are available in the accompanying notebook.
This repository emphasizes **analytical reasoning supported by modeling results**.

