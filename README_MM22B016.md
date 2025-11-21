
# 🛰️ Satellite Land-Cover Classification + DA5401 Kaggle Report (MM22B016)

This repository contains the full machine learning workflow for two major tasks:
1. **DA5401 Kaggle Competition — Score Prediction Model**
2. **Satellite Land‑Cover Classification — Multiclass ROC/PRC Benchmarking**

---

## 📁 Repository Structure
```
├── DA5401_Assignment7_MM22B016.ipynb
├── train_data.json           # Training set from competition
├── test_data.json            # Test set
├── metric_name_embeddings.npy
├── metric_names.json
├── sample_submission.csv
├── Updated_DA5401_Report_MM22B016.docx
├── README.md                 # This file — ready to paste!
```

---

## 🎯 Task 1 — DA5401 Kaggle Score Prediction

### ✔️ Key Steps
- Preprocessing conversational data  
- Merging user prompts, responses, and system instructions  
- Creating text embeddings using Sentence‑Transformers  
- Using metric embeddings for semantic alignment  
- Feature engineering (cosine similarity, Euclidean distance, diff, product)  
- Negative sampling for contrastive supervision  
- MLP model with BatchNorm + Dropout  
- 5‑Fold cross‑validation + ensemble predictions  

### 📈 Output  
- Final submission file saved as **submission.csv**  
- Detailed technical report included as **Updated_DA5401_Report_MM22B016.docx**

---

## 🛰️ Task 2 — Satellite Land‑Cover Classification (ROC/PRC)

Benchmarking on Landsat‑like data using:
- KNN  
- SVC  
- Logistic Regression  
- GaussianNB  
- Decision Tree  
- Random Forest  
- XGBoost  

### 🧮 Metrics Used
- Accuracy  
- Weighted F1  
- Macro ROC–AUC (OvR)  
- Macro PRC–AP  

### 🏆 Best Models
- **KNN:** Best F1 & PRC–AP  
- **SVC:** Best ROC–AUC  

---

## 🙌 Author
**Adarsh Mahaveer Tare**  
Roll No: **MM22B016**

---

## 📬 Contact
For questions or improvements, feel free to raise an issue.

