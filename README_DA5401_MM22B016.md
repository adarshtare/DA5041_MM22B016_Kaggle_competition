
# 📘 DA5401 Kaggle Competition — Score Prediction  
### **Author:** Adarsh Mahaveer Tare  
### **Roll No:** MM22B016  

---

## 📁 Repository Structure
```
├── DA_lab_MM22B016.ipynb
├── train_data.json
├── test_data.json
├── metric_name_embeddings.npy
├── metric_names.json
├── sample_submission.csv
├── README.md
```

---

## 🎯 Project Objective
The goal is to build a machine learning model that predicts evaluator-assigned scores (0–10) for model responses based on:
- User prompts  
- AI-generated responses  
- System prompts  
- Metric names and their embeddings  

This project focuses on **text–metric alignment**, using embeddings and feature engineering.

---

## ⚙️ Workflow Summary

### **1️⃣ Preprocessing**
- Clean missing text fields  
- Map metric names → embedding indices  
- Construct unified text input:  
  `"[Prompt] ... [Response] ... [System] ..."`  
- Encode text with **Sentence-Transformers**  
- Encode metric names and normalize embeddings  

---

### **2️⃣ Feature Engineering**
Each sample combines:
- Text embedding  
- Metric embedding  
- Cosine similarity  
- Euclidean distance  
- Element-wise difference  
- Element-wise product  

Negative sampling was added by pairing text with incorrect metrics to strengthen model contrast learning.

---

### **3️⃣ Model Architecture**
A **deep MLP regressor**:
- Linear → BatchNorm → ReLU → Dropout  
- Layers: 1024 → 512 → 128 → 1  
- Loss: MSE  
- Optimizer: AdamW  
- Scheduler: ReduceLROnPlateau  

---

### **4️⃣ Cross-Validation & Ensemble**
- 5-Fold CV  
- Best model per fold saved  
- Predictions averaged across folds  
- Final scores clipped + rounded  

---

### **5️⃣ Output**
- **submission.csv** – final competition file  
- **DA5401_Final_Report_MM22B016.docx** – detailed report  

---

## ✅ Conclusion
This project demonstrates an end-to-end ML pipeline involving:
- Text–metric embedding alignment  
- Feature engineering  
- Negative sampling  
- Deep neural regression  
- Cross-validated ensemble predictions  

It provides a strong predictive solution for the DA5401 Kaggle task.

---

## ✉️ Contact
Feel free to reach out for improvements or queries.
