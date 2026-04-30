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

- Total classes available: 10  
- Used classes: Dog, Cat, Horse  
- Images resized to: 96×96  
- Train/Validation split: 80/20  

Dataset size (approx):

- Dog: 4863 images  
- Cat: 1668 images  
- Horse: 2623 images  

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

## 🧠 Model Architecture

CNN structure:

- Input: (96, 96, 3)
- Conv2D (32 filters) + MaxPooling
- Conv2D (64 filters) + MaxPooling
- Conv2D (128 filters) + MaxPooling
- Flatten
- Dense (128)
- Dropout
- Output: Softmax (3 classes)
Total parameters: ~1.7M

---

## 🏋️ Training

- Optimizer: Adam  
- Loss: Sparse Categorical Crossentropy  
- Metric: Accuracy  
- Epochs: ~20  
---

## 📈 Results

### Overall Performance

- Training Accuracy: ~68%  
- Validation Accuracy: ~72–74%  

---

## ❌ Misclassifications

- Visualized incorrectly predicted images  
- Compared predicted vs actual labels  

---

## 📊 Key Observations

- Strong bias toward predicting "Dog"
- Cat class is poorly learned
- Model struggles with visually complex or indoor images

---

## ⚠️ Limitations

- Model is basic CNN (not optimized)  
- Low image resolution (96×96)
- Only 3 out of 10 classes used

---
## 🚀 Improvements

To significantly improve performance:

1. Balance dataset

   - Oversample Cats or undersample Dogs

2. Increase image resolution

   - Use 128×128 or 224×224

3. Use transfer learning

   - MobileNetV2 / ResNet50

4. Apply class weights during training

5. Add early stopping + learning rate scheduling

---

## ▶️ How to Run

1. Open notebook in Google Colab

2. Install kagglehub:
```text
pip install kagglehub
```

3. Download dataset directly from Kaggle:
```text
import kagglehub
import os

path = kagglehub.dataset_download("alessiocorrado99/animals10")
dataset_path = os.path.join(path, "raw-img")
```

4. Verify dataset:
```text
print(os.listdir(dataset_path))
```

5. Run all cells
