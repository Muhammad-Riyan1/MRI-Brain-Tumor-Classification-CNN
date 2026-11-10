# 🧠 MRI Brain Tumor Classification Using Convolutional Neural Network (CNN)

## 📌 Project Overview

This project implements a **Convolutional Neural Network (CNN)** using PyTorch to classify brain MRI images into different categories.

The model learns patterns and features from MRI images through multiple convolutional layers and predicts the corresponding image class.

The project includes model training, validation, testing, performance evaluation, and visualization of results.

## 🎯 Objectives

- Develop a CNN-based brain MRI image classification model.
- Preprocess MRI images for deep learning.
- Train and validate the CNN model.
- Evaluate model performance using multiple evaluation metrics.
- Visualize training performance and classification results.

## 🛠️ Technologies & Libraries

- Python
- PyTorch
- Torchvision
- NumPy
- Pandas
- Matplotlib
- Seaborn
- Scikit-learn
- Google Colab

## 🏗️ CNN Architecture

The proposed CNN architecture consists of:

1. **Convolutional Layer 1:** Extracts initial image features using 32 filters.
2. **Batch Normalization:** Normalizes intermediate feature maps.
3. **ReLU Activation:** Introduces non-linearity.
4. **Max Pooling:** Reduces spatial dimensions.
5. **Convolutional Layer 2:** Extracts more complex features using 64 filters.
6. **Convolutional Layer 3:** Extracts deeper features using 128 filters.
7. **Fully Connected Layer:** Maps extracted features to 256 neurons.
8. **Dropout:** Reduces overfitting.
9. **Output Layer:** Produces class predictions.

### Model Configuration

| Parameter | Value |
|---|---|
| Input Image Size | 64 × 64 |
| Input Channels | 1 (Grayscale) |
| Convolutional Layers | 3 |
| Filters | 32, 64, 128 |
| Fully Connected Neurons | 256 |
| Dropout | 0.5 |
| Optimizer | Adam |
| Learning Rate | 0.001 |
| Loss Function | CrossEntropyLoss |
| Batch Size | 16 |
| Training Epochs | 18 |

## 📂 Dataset Structure

The model uses the PyTorch `ImageFolder` dataset loader.

Expected directory structure:

```text
MRI/
│
├── Training/
│   ├── Class_1/
│   ├── Class_2/
│   └── ...
│
└── Testing/
    ├── Class_1/
    ├── Class_2/
    └── ...
```

The actual class names are automatically detected from the dataset folders.

## 🔄 Image Preprocessing

The following transformations are applied:

- Resize images to 64 × 64 pixels.
- Convert images to grayscale.
- Convert images into PyTorch tensors.
- Normalize pixel values using mean 0.5 and standard deviation 0.5.

## 🚀 Model Training

The dataset is divided into:

- 80% Training
- 20% Validation

The CNN is trained for 18 epochs using the Adam optimizer and Cross Entropy Loss.

## 📊 Model Evaluation

The trained model is evaluated using the testing dataset.

The following performance metrics are calculated:

- Accuracy
- Precision
- Recall
- F1-Score

The project also generates:

- Confusion Matrix
- Classification Report
- Training vs. Validation Loss Graph
- Training vs. Validation Accuracy Graph
- Performance Metrics Bar Chart
- Training Results Table

## 📈 Generated Outputs

The model generates two important output files:

- `mri_cnn_model.pth` — Trained model weights.
- `training_results.csv` — Training and validation performance history.

## ⚙️ Installation

Clone the repository:

```bash
git clone https://github.com/Muhammad-Riyan1/MRI-Brain-Tumor-Classification-CNN.git
```

Navigate to the project directory:

```bash
cd MRI-Brain-Tumor-Classification-CNN
```

Install the required libraries:

```bash
pip install -r requirements.txt
```

Run the Python script in Google Colab after configuring your MRI dataset in Google Drive.

## 📁 Repository Structure

```text
MRI-Brain-Tumor-Classification-CNN/
│
├── mri_brain_tumor_cnn.py
├── README.md
├── requirements.txt
└── .gitignore
```

## ⚠️ Disclaimer

This project is developed for educational and research purposes only.

It is not a clinically validated diagnostic system and should not be used to make medical decisions. Brain tumor diagnosis must be performed by qualified medical professionals.

## 🔬 Future Improvements

- Experiment with deeper CNN architectures.
- Apply transfer learning using ResNet or EfficientNet.
- Implement Grad-CAM for model interpretability.
- Develop a web-based MRI classification application.
- Improve generalization through data augmentation and external validation.

