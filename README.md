🔄 Customer Churn Rate Prediction
An end-to-end Machine Learning project to predict customer churn using the Online Retail II dataset (1M+ transactions).

📖 Overview
Churn prediction helps businesses identify at-risk customers early and take proactive retention actions. 
This project builds a full ML pipeline — from raw data to a final optimized model achieving 91.6% Recall.

🔄 Workflow
🧹 Data Cleaning
      ↓
🧠 RFM Feature Engineering
      ↓
⚖️  SMOTE Class Balancing
      ↓
🤖 Model Training & Comparison
      ↓
🎯 Threshold Tuning
      ↓
🔧 GridSearchCV Hyperparameter Optimization
      ↓
✅ Final Tuned XGBoost Model

🤖 Model Comparison
Model                     Recall             F1-Score           ROC-AUC
Logistic Regression        0.841               0.751              0.791
Random Forest              0.689               0.687              0.737
⭐ Tuned XGBoost          0.916               0.747              0.793
🏆 Winner: Tuned XGBoost @ Threshold 0.40 — catches 9 out of 10 at-risk customers!

📊 Key Insights from the Final Model
After training, tuning, and evaluating the final Tuned XGBoost model, here are the most important takeaways:

🎯 High Recall is the priority — With a Recall of 91.6%, the model successfully identifies the vast majority of customers likely to churn, minimizing missed opportunities for intervention.
💡 Threshold tuning was a game changer — Simply lowering the decision threshold from 0.50 to 0.40 boosted Recall from 79.9% → 91.6%, proving that threshold optimization can be more impactful than hyperparameter tuning alone.
🔍 Frequency & Monetary are the strongest churn signals — Customers who purchase less frequently and spend lower amounts are significantly more likely to churn.
⚠️ Recency causes data leakage — Since churn was defined as "no purchase in 90 days", Recency was intentionally excluded from features to prevent the model from cheating.
⚖️ SMOTE prevented bias — With a near 50/50 churn split, SMOTE ensured the model didn't over-predict the majority class.
🔧 GridSearchCV gave marginal but consistent gains — Hyperparameter tuning improved ROC-AUC from 0.790 → 0.793 and Recall from 90.5% → 91.6%, confirming the model is well-optimized.

📥 Download the Online Retail II Dataset from the files attached and also checkout the Requirements before working.
