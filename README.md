# Multimodal Speech Emotion Recognition and Ambiguity Resolution

This project explores the identification of emotions from speech using lightweight and interpretable machine learning models compared to deep learning counterparts. The work employs hand-crafted features from audio signals, achieving state-of-the-art performance on the **IEMOCAP dataset** for speech emotion recognition and ambiguity resolution.

---

## Overview

Emotion recognition from speech is inherently complex due to the ambiguous nature of emotions. This project addresses these challenges by:
- Developing lightweight multimodal machine learning models.
- Comparing their performance against heavier deep learning models.
- Utilizing hand-crafted feature vectors extracted from audio signals.

The experiments demonstrate that lightweight models perform comparably to, and sometimes outperform, deep learning baselines, offering state-of-the-art results.

---

## Models Used

### Machine Learning Models
- Logistic Regression (LR)
- Support Vector Machines (SVM)
- Random Forest (RF)
- eXtreme Gradient Boosting (XGB)
- Multinomial Naive-Bayes (MNB)

### Deep Learning Models
- Multi-Layer Perceptron (MLP)
- LSTM Classifier

---

## Dataset

The experiments are conducted on the **IEMOCAP dataset**, a widely used dataset for emotion recognition tasks. Hand-crafted feature vectors are extracted from audio signals and used for training and evaluation.

---

## Results

The results of various experiments are summarized below:

### **Audio Models Performance**

| Model         | Accuracy (%) | F1 (%) | Precision (%) | Recall (%) |
|---------------|--------------|--------|---------------|------------|
| RF            | 56.0         | 56.0   | 57.2          | 57.3       |
| XGB           | 55.6         | 56.0   | 56.9          | 56.8       |
| SVM           | 33.7         | 15.2   | 17.4          | 21.5       |
| MNB           | 31.3         | 9.1    | 19.6          | 17.2       |
| LR            | 33.4         | 14.9   | 17.8          | 20.9       |
| MLP           | 41.0         | 36.5   | 42.2          | 35.9       |
| LSTM          | 43.6         | 43.4   | 53.2          | 40.6       |
| ARE (4-class) | 56.3         | -      | 54.6          | -          |
| E1 (4-class)  | 56.2         | 45.9   | 67.6          | 48.9       |
| E1            | 56.6         | 55.7   | 57.3          | 57.3       |

> **E1**: Ensemble (RF + XGB + MLP)

---

### **Text Models Performance**

| Model         | Accuracy (%) | F1 (%) | Precision (%) | Recall (%) |
|---------------|--------------|--------|---------------|------------|
| RF            | 62.2         | 60.8   | 65.0          | 62.0       |
| XGB           | 56.9         | 55.0   | 70.3          | 51.8       |
| SVM           | 62.1         | 61.7   | 62.5          | 63.5       |
| MNB           | 61.9         | 62.1   | 71.8          | 58.6       |
| LR            | 64.2         | 64.3   | 69.5          | 62.3       |
| MLP           | 60.6         | 61.5   | 62.4          | 63.0       |
| LSTM          | 63.1         | 62.5   | 65.3          | 62.8       |
| TRE (4-class) | 65.5         | -      | 63.5          | -          |
| E1 (4-class)  | 63.1         | 61.4   | 67.7          | 59.0       |
| E2            | 64.9         | 66.0   | 71.4          | 63.2       |

> **E2**: Ensemble (RF + XGB + MLP + MNB + LR)  
> **E1**: Ensemble (RF + XGB + MLP)

---

### **Audio + Text Models Performance**

| Model         | Accuracy (%) | F1 (%) | Precision (%) | Recall (%) |
|---------------|--------------|--------|---------------|------------|
| RF            | 65.3         | 65.8   | 69.3          | 65.5       |
| XGB           | 62.2         | 63.1   | 67.9          | 61.7       |
| SVM           | 63.4         | 63.8   | 63.1          | 65.6       |
| MNB           | 60.5         | 60.3   | 70.3          | 57.1       |
| MLP           | 66.1         | 68.1   | 68.0          | 69.6       |
| LR            | 63.2         | 63.7   | 66.9          | 62.3       |
| LSTM          | 64.2         | 64.7   | 66.1          | 65.0       |
| MDRE (4-class)| 75.3         | -      | 71.8          | -          |
| E1 (4-class)  | 70.3         | 67.5   | 73.2          | 65.5       |
| E2            | 70.1         | 71.8   | 72.9          | 71.5       |

> **MDRE**: Multi-Modal Deep Representation Ensemble  
> **E2**: Ensemble (RF + XGB + MLP + MNB + LR)  
> **E1**: Ensemble (RF + XGB + MLP)

---


