# 🧠 Chinese Character Memory Prediction

**Goal:**  
Understand and model how visual and structural properties of Chinese characters
relate to human memory retention.

---

## 📊 Data Overview

- Samples: Chinese characters
- Target: Memory retention score
- Inputs:
  - Handcrafted structural features
  - Character images

![Modeling Framework](images/Pipeline.png)



---

## 🔍 Exploratory Data Analysis (EDA)

This section provides a concise exploratory analysis to understand the
distributional properties of the target variable and the relationships
between structural features and memory retention.

---

### 🎯 Target Variable: Memory Retention (ACC)

<img src="images/acc_distribution.png" width="700">

The target variable (ACC) exhibits a pronounced **left-skewed distribution**
(skew ≈ −2.07), with a strong ceiling effect near 1.0.  
This indicates non-normality and motivates the use of transformations
and models robust to skewed targets.

<img src="images/acc_boxplot.png" width="700">

The boxplot further confirms heavy concentration at high ACC values
and the presence of low-end outliers.

---

### 📊 Feature Space Overview

<img src="images/feature_distributions.png" width="900">

Selected feature distributions highlight substantial heterogeneity:
continuous semantic features, discrete structural counts,
and binary orthographic indicators coexist within the feature space.
All features are scaled to the \([0,1]\) range for comparability.

---

### 🔗 Correlation Structure

<img src="images/correlation_clustermap.png" width="900">

Correlation analysis reveals that **lexical–semantic features**
(e.g., familiarity, contextual frequency) show stronger associations
with memory retention, while **structural features**
(e.g., stroke and radical counts) form coherent clusters with weaker
direct correlations to ACC.

These observations inform subsequent modeling choices and feature integration strategies.


## 🛠 Tools

Python · pandas · matplotlib · scikit-learn · PyTorch

---

## 📌 Notes

Full implementation details are available in the accompanying notebook.
This repository emphasizes **analytical reasoning supported by modeling results**.

