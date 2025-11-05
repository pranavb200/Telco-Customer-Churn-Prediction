# 📞 Telco Customer Churn Prediction

This is an **end-to-end Machine Learning project** that predicts whether a telecom customer is likely to churn (leave the service) based on their usage patterns, contract type, and demographics.  
It includes **data preprocessing, model comparison, evaluation, visualization, and real-world predictions.**

---

## 📊 Project Overview

Customer churn prediction helps telecom companies identify customers likely to switch to competitors.  
By predicting churn early, businesses can take preventive actions (discounts, better plans, etc.) to retain customers.

---

## 🧩 Dataset

- **Name:** [IBM Telco Customer Churn Dataset](https://raw.githubusercontent.com/IBM/telco-customer-churn-on-icp4d/master/data/Telco-Customer-Churn.csv)
- **Target Variable:** `Churn` — whether the customer left the service or not.
- **Size:** 7043 rows × 21 columns  
- **Reason for choosing:**  
  - Real-world business use case  
  - Imperfect data (missing values, categorical variables) — ideal for full ML pipeline  
  - Easy to visualize and interpret

---

## ⚙️ Steps Performed

### 1️⃣ Data Cleaning & Preprocessing
- Removed spaces and handled missing values in `TotalCharges`
- Converted categorical variables using **Label Encoding**
- Normalized numerical columns using **StandardScaler**
- Split dataset into training and testing (80:20)

### 2️⃣ Model Selection & Training
Trained and compared the following models:
| Model | Type | Purpose |
|--------|------|----------|
| Logistic Regression | Linear baseline | Interpretable and simple |
| Random Forest | Ensemble | Robust and reduces overfitting |
| SVM (RBF Kernel) | Non-linear | Handles complex relationships |
| Gradient Boosting | Sequential Ensemble | Learns iteratively and improves accuracy |

### 3️⃣ Model Evaluation Metrics
| Metric | Meaning | Reason for Use |
|---------|----------|----------------|
| Accuracy | % of correct predictions | General performance |
| Precision | % of predicted churns that are true | Avoid false churn alerts |
| Recall | % of actual churns detected | Important in churn detection |
| F1-Score | Balance between precision & recall | Good for imbalanced data |
| ROC-AUC | Separating ability of model | Measures ranking quality |

---

## 🧠 Best Model: Gradient Boosting

Gradient Boosting gave the best results because:
- It builds models **sequentially**, fixing errors step by step.  
- Handles **non-linear relationships** and mixed data types well.  
- Achieved the **highest Accuracy, F1, and ROC-AUC scores**.  
- Provides **feature importance**, making results interpretable.

---

## 📈 Visualizations

| Visualization | Purpose |
|----------------|----------|
| **Bar Chart** | Compare Accuracy, F1, ROC-AUC of all models |
| **ROC Curve** | Show model discrimination ability |
| **Confusion Matrix** | Display correct vs wrong predictions |
| **Feature Importance** | Identify key churn factors |
| **SHAP Summary Plot** | Explain why each feature affects churn |
| **Churn Probability Distribution** | Visualize customers at high risk |
| **Customer Scatter Plot** | Show churn probability for each customer |

---

## 🎯 Predictions

- **For all customers:** Predict churn probability and label (`Churn` or `No Churn`)
- **Top 10 at-risk customers:** Displayed with highest churn probabilities
- **Manual prediction:** Predict for new unseen customers

Example Output:
```
Customer CUST9999 is LIKELY to CHURN (Probability: 0.87)
```

---

## 🧮 Tech Stack

- **Language:** Python  
- **Libraries:** pandas, numpy, sklearn, seaborn, matplotlib, plotly, shap  
- **Environment:** Google Colab / Jupyter Notebook

---

## 🧠 Key Learnings

- Data cleaning & preprocessing are crucial before ML
- Evaluating with multiple metrics gives better insight
- Ensemble models like Gradient Boosting outperform simple models
- Visualizations & SHAP improve explainability

---

## 🧾 How to Run

1. Clone the repository:
   ```bash
   git clone https://github.com/pranavb200/Telco-Customer-Churn-Prediction.git
   ```
2. Open the notebook in [Google Colab](https://colab.research.google.com/)
3. Upload the dataset: `Telco-Customer-Churn.csv`
4. Run all cells sequentially
5. View model comparisons and churn predictions interactively

---

## 💡 Future Enhancements
- Deploy model using **Streamlit** web app  
- Add **customer retention strategy suggestions**  
- Connect to live database for real-time churn prediction  

---

## 👨‍💻 Author
**Pranav B**  
📧 [GitHub: pranavb200](https://github.com/pranavb200)  
💬 “Predicting churn is not just data science — it’s business intelligence.”
