# ♻️ Waste Classification with Transfer Learning

## 🚀 Overview

This is a computer vision project developed as a **final project for the IBM Deep Learning with Keras and TensorFlow course**. It classifies waste into **Recyclable** and **Organic** categories using **Transfer Learning with VGG16**.

This project demonstrates an end-to-end deep learning workflow and simulates a real-world smart waste sorting system.

🔗 Repository: [https://github.com/Shiverion/IBM-Classify-Waste-Products-Using-Transfer-Learning](https://github.com/Shiverion/IBM-Classify-Waste-Products-Using-Transfer-Learning)

---

## 🎓 Course Context

This project was completed as part of:
**IBM Deep Learning with Keras and TensorFlow**

It focuses on applying practical deep learning techniques including transfer learning, fine-tuning, and model evaluation in a real-world scenario.

---

## 🎯 Objectives

* Apply transfer learning using VGG16
* Preprocess image data with ImageDataGenerator
* Train a feature extraction model
* Fine-tune the model for better performance
* Evaluate model performance
* Visualize predictions on test data

---

## 🧱 Project Structure

```
├── Final_Proj_Classify_Waste_Products_Using_TL_FT_v1.ipynb
├── README.md
```



## ⚙️ Setup

### Install Dependencies
```

pip install tensorflow matplotlib numpy

````

### Import Libraries
```python
import tensorflow as tf
from tensorflow.keras.preprocessing.image import ImageDataGenerator
import matplotlib.pyplot as plt
````

---

## 📊 Workflow

### 🔹 Data Preparation

* Load dataset using ImageDataGenerator
* Apply rescaling and augmentation

### 🔹 Model Development

* Use VGG16 (pre-trained on ImageNet)
* Freeze convolutional base for feature extraction
* Add custom classification layers

### 🔹 Training Strategy

1. Feature Extraction Model
2. Fine-Tuned Model

---

## 🧪 Tasks Completed

| Task    | Description                               |
| ------- | ----------------------------------------- |
| Task 1  | Print TensorFlow version                  |
| Task 2  | Create test generator                     |
| Task 3  | Check train generator length              |
| Task 4  | Display model summary                     |
| Task 5  | Compile model                             |
| Task 6  | Plot accuracy (feature extraction)        |
| Task 7  | Plot loss (fine-tuning)                   |
| Task 8  | Plot accuracy (fine-tuning)               |
| Task 9  | Visualize prediction (feature extraction) |
| Task 10 | Visualize prediction (fine-tuned model)   |

---

## 📈 Results & Insights

* Transfer learning significantly reduces training time
* Fine-tuning improves accuracy and generalization
* Visualization helps interpret model predictions

---

## 🖼️ Outputs

Screenshots for each task are available in the `/screenshots` folder.

---

## 🧠 Key Learnings

* Transfer learning is highly effective for small datasets
* Fine-tuning boosts model performance
* Data preprocessing is critical in computer vision tasks

---

## 🌍 Real-World Impact

This model can be applied to:

* Smart waste bins
* Recycling facilities
* Automated waste sorting systems

---

## ✍️ Author

**Muhammad Iqbal Hilmy Izzulhaq**

* GitHub: [https://github.com/Shiverion](https://github.com/Shiverion)
* LinkedIn: [https://www.linkedin.com/in/izzulhaq-iqbal/](https://www.linkedin.com/in/izzulhaq-iqbal/)

---

## 💡 Future Improvements

* Add more waste categories (plastic, metal, glass)
* Deploy as a web app (Gradio/Streamlit)
* Experiment with EfficientNet or ResNet

---

## ⭐ Final Note

This project highlights practical implementation of transfer learning as taught in the IBM Deep Learning course, bridging theory with real-world application in sustainability and automation.

## System Design

### Requirements

- Classify waste images into organic and recyclable classes.
- Compare a frozen VGG16 feature extractor with a fine-tuned VGG16 model and inspect test predictions.

### Pipeline

```text
External two-class image folders → ImageDataGenerator resize/rescale/augment
                                → ImageNet VGG16 feature extraction
                                → fine-tuning → test predictions and plots
```

The 150×150 image workflow is contained in `Final_Proj_Classify_Waste_Products_Using_TL_FT_v1.ipynb`. The dataset itself is not included in the repository.

### Trade-offs

| Decision | Benefit | Cost |
| --- | --- | --- |
| Start from ImageNet VGG16 weights | Reuses visual features for a small coursework dataset | Requires compatible weights and external image folders |
| Keep training in one notebook | Makes the learning sequence easy to follow | Runtime state is not packaged as an inference service |

### What to Revisit

- Document the expected dataset directory layout and source.
- Save a final model and add a small inference example.
- Record the TensorFlow version and training configuration.
