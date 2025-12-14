# 🚨 AI-Based Network Intrusion Detection System

An end-to-end **Machine Learning–based Intrusion Detection System (IDS)** that detects malicious network traffic using the **NSL-KDD dataset**.
The system applies data preprocessing, model training, evaluation, and visualization to identify cyber attacks effectively.

---

## 📌 Project Overview

Intrusion Detection Systems are essential in cybersecurity to monitor network traffic and detect unauthorized or malicious activities.
This project uses **machine learning classifiers** to automatically distinguish between **normal traffic** and **network attacks**.

### 🔍 Key Highlights

* Binary classification (Normal vs Attack)
* Focus on **attack recall** to reduce missed intrusions
* Comparison of multiple ML models
* Clear evaluation using confusion matrices and performance metrics

---

## 🛠 Technologies Used

* **Programming Language:** Python 3
* **Libraries:**

  * NumPy
  * Pandas
  * Scikit-learn
  * Matplotlib
  * Seaborn
* **Tools:**

  * Jupyter Notebook
  * Joblib
* **Dataset:** NSL-KDD

---

## 📂 Project Structure

```
AI_Network_Intrusion_Detection/
│
├── 01_data_preprocessing.ipynb
├── 02_model_training.ipynb
├── 03_model_evaluation.ipynb
├── 04_results_visualization.ipynb
│
├── KDDTrain+.txt
├── KDDTest+.txt
│
├── X_train.npy
├── X_test.npy
├── y_train.npy
├── y_test.npy
│
├── random_forest_model_tuned.pkl
├── svm_model.pkl
│
└── README.md


## Dataset

This project uses the **NSL-KDD dataset**.

Due to repository size and best practices, the dataset files are not included.
You can download them from the official source:

https://www.unb.ca/cic/datasets/nsl.html

Required files:
- KDDTrain+.txt
- KDDTest+.txt
```

---

## 📊 Dataset Description

* **Dataset Name:** NSL-KDD
* **Source:** Improved version of KDD Cup 1999
* **Classes:**

  * `0` → Normal Traffic
  * `1` → Attack Traffic
* **Why NSL-KDD?**

  * Removes redundant records
  * Balanced and suitable for ML evaluation
  * Widely accepted in IDS research

---

## ⚙️ Implementation Workflow

### 1️⃣ Data Preprocessing

* Load raw NSL-KDD dataset
* Encode categorical features
* Normalize numerical features
* Split into training and testing sets
* Save preprocessed data as `.npy` files

### 2️⃣ Model Training

* Random Forest (baseline + tuned)
* Support Vector Machine (SVM)
* Trained models saved using `joblib`

### 3️⃣ Model Evaluation

* Accuracy
* Precision, Recall, F1-Score
* Confusion Matrix analysis
* Emphasis on reducing **false negatives**

### 4️⃣ Results Visualization

* Confusion matrix plots
* Accuracy comparison
* Attack-class performance comparison

---

## 📈 Results Summary

| Model                 | Accuracy | Attack Recall | Notes                  |
| --------------------- | -------- | ------------- | ---------------------- |
| Random Forest (Tuned) | ~76%     | Higher        | Best overall IDS model |
| SVM                   | ~78%     | Moderate      | Slower, less practical |

✔ Random Forest was selected as the **final model** due to better intrusion detection capability.

---

## 🎯 Key Observations

* Accuracy alone is **not sufficient** for IDS
* Reducing **missed attacks (False Negatives)** is critical
* Class-weight tuning improves attack detection
* Random Forest is more suitable for real-time IDS scenarios

---

## 🚀 How to Run the Project

1. Clone the repository
2. Install dependencies:

   ```bash
   pip install numpy pandas scikit-learn matplotlib seaborn
   ```
3. Open Jupyter Notebook:

   ```bash
   jupyter notebook
   ```
4. Run notebooks in order:

   * `01_data_preprocessing.ipynb`
   * `02_model_training.ipynb`
   * `03_model_evaluation.ipynb`
   * `04_results_visualization.ipynb`

---

## 🔮 Future Enhancements

* Multi-class attack classification
* Deep learning models (LSTM, CNN)
* Real-time packet capture integration
* Deployment using Flask or FastAPI
* Cloud-based IDS implementation

---

## 🎓 Academic Use

This project is suitable for:

* Final-year engineering projects
* Cybersecurity portfolios
* Machine learning coursework
* IDS research and demonstrations

---

## 👤 Author

**Suyash Chougule**
Computer Science Engineering
AI-Based Network Intrusion Detection System

---

## ⭐ Final Note

> This project demonstrates a complete and practical application of machine learning in cybersecurity, focusing on realistic evaluation rather than inflated accuracy.
