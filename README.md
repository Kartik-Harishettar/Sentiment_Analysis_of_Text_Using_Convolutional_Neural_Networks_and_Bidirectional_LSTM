# 📌 Sentiment Analysis of Text Using CNN-BiLSTM

This project implements a **hybrid Convolutional Neural Network (CNN) and Bidirectional Long Short-Term Memory (Bi-LSTM)** model for **sentiment analysis** of textual data (Twitter dataset).  
The hybrid approach leverages:
- **CNN** → for extracting local word patterns  
- **Bi-LSTM** → for capturing long-term dependencies and contextual meaning  

The model achieves **91.5% accuracy** and a **89.86% weighted F1-score**, making it highly effective for classifying tweets as **Positive, Neutral, or Negative**.

---

## ✨ Features
- Data preprocessing pipeline (cleaning, tokenization, stop-word removal, padding)  
- Word embedding using TensorFlow/Keras  
- Hybrid **CNN + Bi-LSTM** architecture  
- Evaluated with **ROC-AUC, Precision-Recall, Confusion Matrix, Accuracy/Loss plots**  
- Achieved:
  - ✅ Accuracy: **91.5%**
  - ✅ Weighted F1-score: **89.86%**
  - ✅ AUC ≈ **0.91** for Positive & Neutral sentiments

---

---

## ⚙️ Methodology

### 🔹 Data Collection
- 50,000 tweets obtained from Kaggle  
- Sentiment labels: **Positive, Negative, Neutral**

<p align="center">
  <img src="Model/meth.jpeg" alt="Research Methodology" width="300"/>
</p>

---

### 🔹 Preprocessing
- Remove noise (URLs, hashtags, special chars)  
- Case folding (convert to lowercase)  
- Stop-word removal (using NLTK)  
- Tokenization & sequence padding (Keras)

<p align="center">
  <img src="Model/preprocessing.jpeg" alt="Preprocessing Flow" width="300"/>
</p>
<p align="center">
  <img src="Model/preprocessing_example.jpeg" alt="Stopword Removal Visualization" width="600"/>
</p>

---

### 🔹 Word Embedding
- Convert tokens into dense numerical vectors using **Keras Embedding Layer**

---

### 🔹 Modeling
- **CNN layers** → Extract local text patterns  
- **Bi-LSTM layers** → Capture sequence dependencies (forward & backward)  
- **Dense + Softmax layer** → Classify into sentiment categories  

<p align="center">
  <img src="Model/model.jpeg" alt="Model Architecture" width="300"/>
</p>

---

### 🔹 Evaluation Metrics
- Confusion Matrix  
- ROC-AUC Curve  
- Precision-Recall Curve  
- Accuracy & Loss plots  

---

## 📊 Results

### 🔹 ROC Curve
<p align="center">
  <img src="Results/ROC_Curve.png" alt="ROC Curve" width="300"/>
</p>

---

### 🔹 Precision-Recall Curve
<p align="center">
  <img src="Results/Precision_and_Recall_Curve.png" alt="PR Curve" width="300"/>
</p>

---

### 🔹 Training & Validation Accuracy
<p align="center">
  <img src="Results/accuracy.jpeg" alt="Accuracy Curve" width="300"/>
</p>

---

### 🔹 Training & Validation Loss
<p align="center">
  <img src="Results/loss.jpeg" alt="Loss Curve" width="300"/>
</p>

---

### 🔹 Confusion Matrix
<p align="center">
  <img src="Results/cf.png" alt="Confusion Matrix" width="300"/>
</p>

---

### ✅ Performance Summary
- **Overall Accuracy**: **91.5%**  
- **Weighted F1-score**: **89.86%**
- 
| Class    | Precision | Recall | F1-Score |
| -------- | --------- | ------ | -------- |
| Negative | 0.89      | 0.88   | 0.90     |
| Neutral  | 0.91      | 0.90   | 0.89     |
| Positive | 0.91      | 0.89   | 0.90     |


- ROC-AUC ≈ **0.91**  
- Validation accuracy stabilized at **91.5%**  
- Overall F1-score **~89.86%**  

---

