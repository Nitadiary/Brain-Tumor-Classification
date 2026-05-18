# 🧠 Brain Tumor Classification from MRI Images using Deep Learning

## 📋 Project Overview
As a Medical Doctor (M.D.) with a strong interest in computational neuroscience and neuroimaging, I developed this deep learning project to evaluate how Convolutional Neural Networks (CNNs) can classify brain tumors from MRI scans. 

The objective is to classify brain MRI images into four distinct categories:
1. Glioma
2. Meningioma
3. Pituitary Tumor
4. No Tumor (Healthy Brain)

## 📊 Dataset
The project utilizes the **Brain Tumor Classification (MRI)** dataset available on Kaggle. It contains thousands of T1/T2-weighted MRI images split into training and testing sets.
*(Note: Due to GitHub's file size limits, the raw image dataset is not uploaded here. You can access it by name of "Brain Tumor Classification (MRI)" directly via Kaggle).*

## 🛠️ Technical Methodology & Transfer Learning
- **Framework:** TensorFlow / Keras (Python)
- **Architecture:** Pre-trained **MobileNetV2** via Transfer Learning (fine-tuned the top layers for 4-class classification).
- **Optimization:** Adam Optimizer with Categorical Cross-Entropy loss function.
- **Hardware Acceleration:** Trained using T4 GPU on Google Colab.

## 📈 Performance & Evaluation Analysis
The model was trained 15 epochs, and the training history is visualized below:

![Model Accuracy](accuracy_plot.png)

### 🔬 Analytical Insights (Overfitting Analysis)
- **Training Accuracy:** Reached over **97%**, showing that the network successfully extracted highly detailed feature maps from the training MRI slices.
- **Validation/Test Accuracy:** Stabilized between **74% and 76%**. 

**Discussion:** The gap between the training and validation lines indicates a classic case of **Overfitting**, which is common in medical image processing due to the structural complexity and subtle variations in MRI scans. 

**Future Adjustments:** To enhance generalization in future iterations, I plan to implement stricter regularization techniques such as:
1. Higher **Dropout** rates (e.g., 0.5) in the dense layers.
2. Advanced **Data Augmentation** (elastic deformations and random contrast adjustments) to better simulate real-world clinical variations.
3. Incorporating **L2 Regularization** to penalize extreme weight values.

## 🚀 How to Run
1. Clone this repository.
2. Download the dataset from Kaggle and place it in your directory.
3. Install dependencies:
   ```bash
   pip install tensorflow matplotlib numpy

