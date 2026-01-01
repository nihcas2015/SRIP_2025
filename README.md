# Summer Research Internship Programme 2025  
## Intrusion Detection in IoT Environment using Stacked Ensemble Learning

## 📌 Overview
This project was developed as part of the **Summer Research Internship Programme (SRIP) 2025**.  
The research focuses on building a **high-accuracy intrusion detection system (IDS)** for **IoT environments** using a **stacked ensemble learning approach combined with a chained prediction mechanism**.

The proposed system is evaluated on multiple benchmark IoT intrusion datasets and demonstrates strong performance in both **binary intrusion detection** and **attack-type classification**.

---

## 🎯 Objectives
- Detect intrusions in IoT network traffic
- Classify the type of attack after intrusion detection
- Improve detection performance using ensemble learning
- Reduce false positives and improve generalization
- Evaluate the system on multiple real-world IoT datasets

---

## 🧠 Model Architecture

### 🔹 Stacked Ensemble Design
The intrusion detection system is built using a **stacked ensemble model** with the following configuration:

#### Base Models
- Random Forest Classifier  
- XGBoost Classifier  

These base learners capture both non-linear relationships and complex feature interactions present in IoT network traffic.

#### Meta-Learner
- Logistic Regression  

The meta-learner combines predictions from the base models to produce the final decision, improving robustness and accuracy.

---

## 🔗 Chain-Based Prediction Mechanism
A **two-stage chained classification approach** is used:

### Stage 1: Binary Classification
- Predicts whether network traffic is:
  - Normal  
  - Intrusion  

### Stage 2: Attack Type Classification
- Activated only if traffic is classified as an intrusion
- Predicts the specific type of attack (e.g., DoS, Botnet, etc.)

This chain mechanism improves efficiency and reduces misclassification by separating detection and classification tasks.

---

## 🗂️ Datasets Used
The model is trained and evaluated on multiple well-known IoT intrusion datasets:

- GOTHAM 2025 Dataset  
- Botnet Dataset  
- TON-IoT Dataset  

These datasets provide diverse attack scenarios and realistic IoT traffic patterns.

---

## 🔄 Data Preprocessing & Feature Engineering
- Removal of redundant and irrelevant features
- Handling missing and inconsistent values
- Label Encoding for categorical attributes
- One-Hot Encoding where applicable
- Feature scaling using Standard Scaler
- Train-test split with strict prevention of data leakage

---

## ⚙️ Tech Stack
- Programming Language: Python  
- Machine Learning: Scikit-learn, XGBoost  
- Data Processing: Pandas, NumPy  
- Visualization: Matplotlib, Seaborn  
- Environment: Colab Notebook / Local Python Environment  

---

## 🧪 Experimental Workflow
1. Load and merge IoT intrusion datasets
2. Perform preprocessing and feature engineering
3. Train base models (Random Forest and XGBoost)
4. Generate base model predictions
5. Train Logistic Regression as meta-learner
6. Apply chained classification mechanism
7. Evaluate performance on unseen test data

---

## 📊 Evaluation Metrics & Results

The stacked ensemble with chained prediction achieved the following results:

✅ Accuracy: 0.9980  
✅ Weighted F1 Score: 0.9980  
✅ Macro F1 Score: 0.9539  
✅ Macro Precision: 0.9629  
✅ Macro Recall: 0.9457  
❌ Hamming Loss: 0.001976  

These results demonstrate the model’s strong ability to detect intrusions and accurately classify attack types while maintaining a very low error rate.

---

## 📈 Key Observations
- Stacked ensemble outperformed individual base models
- Chain-based approach reduced false positives
- Strong generalization across multiple IoT datasets
- Effective detection of both intrusion presence and attack category

