# 🧬 Skin Cancer Classification and Segmentation

This project tackles the dual challenge of **multiclass skin cancer classification** and **segmentation** using the **HAM10000** dataset. The primary goal is to automate the diagnostic process by distinguishing between seven types of skin lesions using deep learning.

---

## 📋 Project Tasks

1. **Multiclass Classification** using a CNN (ResNet-50 pretrained on ImageNet)
2. **Segmentation** of lesion regions (Future work)

---

## 🔍 Classes in the Dataset

The dataset contains the following skin lesion classes:

- **MEL**: Melanoma  
- **NV**: Melanocytic nevi  
- **BCC**: Basal cell carcinoma  
- **AKIEC**: Actinic keratoses and intraepithelial carcinoma  
- **BKL**: Benign keratosis-like lesions  
- **DF**: Dermatofibroma  
- **VASC**: Vascular lesions  

---

## 📁 Dataset Overview

- 📦 **Source**: [Kaggle - HAM10000](https://www.kaggle.com/datasets/kmader/skin-cancer-mnist-ham10000)
- 🧾 **Structure**:
  - Folder 1: Raw **images**
  - Folder 2: **Segmentation masks**
  - CSV file: **Labels** and metadata
- ✂️ **Custom Split**: The dataset is not pre-split. It was divided into train, validation, and test sets manually.

---

## 🧠 Classification Model

- 🔧 **Architecture**: ResNet-50 (ImageNet pretrained)
- 🧮 **Total Parameters**: Under 60 million
- 🛠️ **Framework**: PyTorch

> ✅ Model training was halted using early stopping at **epoch 16** to prevent overfitting.

---

## 📊 Test Results

| Metric       | Value   |
|--------------|---------|
| Accuracy     | 0.6870  |
| Precision    | 0.8032  |
| Recall       | 0.6281  |
| F1-score     | 0.6429  |
| Val Loss     | 11.8796 |
| Train Loss   | 33.1542 |

### 🔍 Per-Class Metrics

| Class   | Precision | Recall | F1-score | Support |
|---------|-----------|--------|----------|---------|
| MEL     | 0.82      | 0.04   | 0.07     | 239     |
| NV      | 0.86      | 0.88   | 0.87     | 1338    |
| BCC     | 0.75      | 0.25   | 0.38     | 106     |
| AKIEC   | 0.43      | 0.10   | 0.16     | 62      |
| BKL     | 0.58      | 0.11   | 0.18     | 206     |
| DF      | 1.00      | 0.14   | 0.24     | 22      |
| VASC    | 0.70      | 0.53   | 0.60     | 30      |

### Averages

- **Macro Avg**: Precision: 0.73 | Recall: 0.29 | F1-score: 0.36  
- **Weighted Avg**: Precision: 0.80 | Recall: 0.63 | F1-score: 0.64  

---

## 🔄 Segmentation Task (In Progress)

Segmentation masks are available, and work is underway to build a lesion segmentation model using U-Net or Mask R-CNN. Currently, the focus is on building a high-performance classifier.

---

## 📌 Project Structure
📁 project-root/
┣ 📄 README.md ← Project overview
┣ 📓 classification.ipynb ← Training + evaluation of classification model
