# 🐾 Animal Classifier (CNN + Keras)

## 📌 Project Overview

This project builds an image classification model to identify different types of animals from images.

### Main question:  
Can a CNN accurately classify animals into their correct categories based on image data?

### Goal:  
Train a deep learning model to recognize animal classes and evaluate its performance.

---

## 📊 Dataset

Source: Kaggle Animals10 dataset

Link: https://www.kaggle.com/datasets/alessiocorrado99/animals10/data

---

## 🧾 Features Used

- Image pixel data  
- Labels derived from folder names  

---

## ⚙️ Data Preparation

- Loaded dataset using TensorFlow/Keras  
- Split into training and validation sets  
- Resized images to a fixed shape  
- Normalized pixel values  

---

## 🧠 Model

- Convolutional Neural Network (CNN)
  - Conv2D + ReLU  
  - MaxPooling  
  - Flatten  
  - Dense layers  
  - Softmax output  

---

## 🏋️ Training

- Optimizer: Adam  
- Loss: Categorical Crossentropy  
- Metrics: Accuracy  
- Trained over multiple epochs  

---

## 📈 Evaluation

- Accuracy on validation set  
- Precision, Recall, F1-score  
- Training vs validation loss/accuracy plots  

---

## ❌ Misclassifications

- Visualized incorrectly predicted images  
- Compared predicted vs actual labels  

---

## 📊 Key Observations

- Model performs well on distinct animals  
- Confusion occurs between visually similar classes  
- Performance depends on image quality and class balance  

---

## ⚠️ Limitations

- Some class imbalance may exist  
- Model is basic CNN (not optimized)  
- No data augmentation used  

---

## 🚀 How to Run

1. Open the notebook in Google Colab  

2. Mount Google Drive:
python from google.colab import drive drive.mount('/content/drive') 

3. Update dataset path  

4. Run all cells  

---

## 🔮 Future Improvements

- Data augmentation  
- Hyperparameter tuning  
- Transfer learning (e.g., MobileNet, ResNet)  
- Deploy as a web app  

---

## 👤 Author

- Your Name  

---

## 📄 License

For educational and personal use
