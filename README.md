# 🔄 Customer Churn Rate Prediction  

An end-to-end **Machine Learning project** to predict customer churn using the **Online Retail II dataset** (1M+ transactions).

---

## 📖 Overview  

Customer churn prediction helps businesses identify at-risk customers early and take proactive retention actions.  

This project builds a **complete ML pipeline** — from raw transactional data to a fully optimized model achieving **91.6% Recall**.

---

## 🔄 Project Workflow  

🧹 **Data Cleaning**  
↓  
🧠 **RFM Feature Engineering**  
↓  
⚖️ **SMOTE Class Balancing**  
↓  
🤖 **Model Training & Comparison**  
↓  
🎯 **Threshold Tuning**  
↓  
🔧 **GridSearchCV Hyperparameter Optimization**  
↓  
✅ **Final Tuned XGBoost Model**

---

## 🤖 Model Comparison  

| Model                  | Recall | F1-Score | ROC-AUC |
|------------------------|--------|----------|----------|
| Logistic Regression    | 0.841  | 0.751    | 0.791    |
| Random Forest          | 0.689  | 0.687    | 0.737    |
| ⭐ **Tuned XGBoost**   | **0.916** | 0.747 | 0.793 |

🏆 **Winner: Tuned XGBoost @ Threshold 0.40**  
Catches **9 out of 10** at-risk customers!

---

## 📊 Key Insights from the Final Model  

After training, tuning, and evaluating the final **Tuned XGBoost model**, here are the major takeaways:

### 🎯 High Recall is the Priority  
With a **Recall of 91.6%**, the model successfully identifies the vast majority of customers likely to churn — minimizing missed intervention opportunities.

### 💡 Threshold Tuning Was a Game Changer  
Lowering the decision threshold from **0.50 → 0.40** boosted Recall from **79.9% → 91.6%**.  
This proves that **threshold optimization can sometimes be more impactful than hyperparameter tuning alone**.

### 🔍 Frequency & Monetary Are the Strongest Signals  
Customers who purchase less frequently and spend lower amounts are significantly more likely to churn.

### ⚠️ Recency Causes Data Leakage  
Since churn was defined as *“no purchase in 90 days”*, the **Recency** feature was intentionally excluded to prevent data leakage.

### ⚖️ SMOTE Prevented Class Bias  
By balancing the dataset close to a **50/50 churn split**, SMOTE ensured the model did not over-predict the majority class.

### 🔧 GridSearchCV Provided Marginal but Consistent Gains  
Hyperparameter tuning improved:
- **ROC-AUC:** 0.790 → 0.793  
- **Recall:** 90.5% → 91.6%  

These improvements confirm the model is **well-optimized and stable**.

---

## 📥 Dataset & Requirements  

- Download the **Online Retail II Dataset** from the attached files.  
- Make sure to review the **requirements.txt** before running the project.
