# 🫀 EAS 503: Cardiovascular Health & Stroke Prediction

## 📌 Overview
This project explores the global burden of cardiovascular diseases (CVDs), emphasizing the health disparities in low- and middle-income countries. Using a machine learning approach, we develop predictive models for stroke risk and deploy them via a user-friendly web application.

---

## 📊 Motivation
Cardiovascular diseases are a leading cause of death globally. Addressing CVDs is especially urgent in lower-resource settings where:
- There's a double burden of communicable and non-communicable diseases.
- Access to healthcare is limited.
- Delayed detection results in higher productivity loss and economic strain.

---

## 📈 Key Global Statistics
- **17.9 million** CVD deaths in 2019 (32% of all deaths).
- **85%** of these were due to heart attacks and strokes.
- High CVD risk from hypertension, smoking, and obesity.
- **$320 billion/year** spent on CVDs in the U.S. alone.

**Sources:**
- [CDC](https://www.cdc.gov/globalhealth/infographics/noncommunicable-diseases/every-heart-counts.html)
- [WHO](https://www.who.int/news-room/fact-sheets/detail/cardiovascular-diseases-(cvds))

---

## 🧠 Stroke Prediction Dataset
- **Source:** Kaggle
- **Size:** ~5000 patient records
- **Attributes:** Gender, Age, Hypertension, Heart Disease, Marital Status, Work Type, Residence Type, Avg Glucose, BMI, Smoking Status, Stroke
- **Goal:** Predict stroke risk using health/lifestyle indicators

---

## 🗃️ Database Design
- Normalized into 3 tables:
  - `PatientDemographics`
  - `HealthDetails`
  - `StrokeIncidence`
- Linked via `PatientID`
- Dropped less impactful fields: Marital Status and Work Type

---

## 🧹 Data Cleaning
- Missing BMI values filled with gender-specific averages
- “Unknown” smokers retained
- One entry with “Other” gender removed

---

## ⚙️ Machine Learning

### 🔁 Preprocessing
- Encoded categorical variables
- Feature selection using backward elimination
- 80-20 train-test split
- Standard scaling of numerical data

### 📦 Logistic Regression
- Selected features: Gender, HeartDisease, Hypertension, Smoker
- F1 Score: ~0.22
- ROC-AUC: ~0.57
- PR-AUC: ~0.11

### 🔍 k-Nearest Neighbors (k=3)
- Selected features: Gender, Hypertension, AvgGlucoseLevel, Smoker
- F1 Score: ~0.06
- ROC-AUC: ~0.57
- PR-AUC: ~0.08

---

## 🌐 Web App

**App:** [AI Doctor - Streamlit Web App](https://ai-doctor.streamlit.app/)

Two predictive tools:
1. **CAD Prediction System**
   - Inputs: Gender, Age, BMI, BP, PR, Smoking
2. **Stroke Prediction System**
   - Inputs: Symptoms, Age, Avg Glucose, BMI
   - Outputs: Stroke probability + model accuracy

---

## ✅ Conclusions
- Promising predictive power for early detection
- Need larger and more diverse dataset
- Plan to tackle class imbalance
- Future goals: integrate user feedback, enhance ML models, and expand input features

---

## 🙋‍♂️ Questions?
Feel free to reach out if you have any questions or feedback!
