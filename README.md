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

![Data Distribution](images/data_distribution.png)

---

## 🔍 Exploratory Analysis — Feature Space

### Feature Distributions
![Feature Distribution](images/feature_distribution.png)

---

### Feature Correlations
![Feature Correlation](images/feature_correlation.png)

---

### Feature vs Memory Retention
![Feature vs Target](images/feature_vs_target.png)

---

## 🔍 Exploratory Analysis — Pattern Discovery

### Key Observations (from EDA)
- No single dominant feature explains memorability
- Multiple structural factors interact
- Non-linear patterns are evident

![EDA Summary](images/eda_summary.png)

---

## 🧩 Modeling Overview (Context Only)

Models are used to **quantify and validate analytical findings**, not as the project focus.

- Feature-based regression (analytical baseline)
- Image-based CNN regression
- Prediction-level model combination

---

## 📈 Model Comparison

![Model Comparison](images/model_comparison.png)

---

## 🖼 CNN Training Evidence

![CNN Training Curve](images/training_curve.png)

---

## 🔗 Model Combination Insight

![Fusion Illustration](images/fusion_diagram.png)

---

## 🧠 Key Takeaways

- Character memorability is multi-factorial
- Handcrafted features explain substantial variance
- Image-based representations capture complementary structure
- Combining both improves robustness

---

## 🛠 Tools

Python · pandas · matplotlib · scikit-learn · PyTorch

---

## 📌 Notes

Full implementation details are available in the accompanying notebook.
This repository emphasizes **analytical reasoning supported by modeling results**.

