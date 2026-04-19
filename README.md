# CodTech_imageclassification_Task3
# Image Classification using Deep Learning (CNN)

## 📌 Project Overview
This project focuses on building a high-performance **Convolutional Neural Network (CNN)** to classify images from the **Oxford-IIIT Pet Dataset**. The challenge involves distinguishing between 37 different breeds of cats and dogs, which requires the model to learn subtle morphological features.

To achieve high accuracy and avoid the "pixelation" issues common in smaller datasets, this project utilizes **Transfer Learning** with **MobileNetV2**. By leveraging a model pre-trained on millions of images, we can achieve expert-level classification even with a limited training window.

## 🚀 Key Features
* **Architecture:** Convolutional Neural Network (CNN) using the MobileNetV2 backbone.
* **Transfer Learning:** Utilizes pre-trained ImageNet weights to boost accuracy and reduce training time.
* **Advanced Preprocessing:** Real-time image resizing to $160 \times 160$ and feature scaling for optimal neural network input.
* **Explainable Visualization:** Generates a prediction grid that highlights **Correct (Green)** and **Incorrect (Red)** classifications with automated reasoning.
* **Performance Optimization:** Uses the `tf.data` pipeline with caching and prefetching for efficient memory management.

## 🛠️ Tech Stack
* **Language:** Python
* **Deep Learning Framework:** TensorFlow 2.x / Keras
* **Data Source:** TensorFlow Datasets (Oxford-IIIT Pet)
* **Visualization:** Matplotlib, NumPy

## 📋 Model Summary
The model architecture is built as follows:
1.  **Input Layer:** $160 \times 160 \times 3$ RGB images.
2.  **Base Layer:** MobileNetV2 (Frozen weights) for feature extraction.
3.  **Global Average Pooling:** Converts 2D feature maps to a 1D feature vector.
4.  **Dropout Layer:** Implemented at 20% to prevent overfitting.
5.  **Output Layer:** Dense layer with 37 neurons (Softmax) for breed classification.

## 📊 Results
The model demonstrates strong convergence. By using Transfer Learning, the network bypasses the "random guessing" phase typical of standard CNNs and immediately begins identifying breed-specific textures like fur patterns, ear shapes, and snout lengths.

## ⚙️ Setup & Usage
1.  Clone the repository or download the `.ipynb` file.
2.  Install dependencies:
    ```bash
    pip install tensorflow tensorflow-datasets matplotlib numpy
    ```
3.  Run the notebook in **Google Colab** (recommended to use a GPU runtime for faster training).

---
**Author:** Dhruti  
**Task:** 03 - Image Classification  
**Organization:** CODTECH IT SOLUTIONS
