# HousePredictionModels
Multi-Modal House Price Prediction: A comparative study of 21 Deep Learning architectures (including ResNet, Inception, VGG, and DenseNet) that fuse visual data (images) with tabular property features to predict real estate prices.
# 🏠 Multi-Modal House Price Prediction: A Comparative Study of 21 CNNs

![Python](https://img.shields.io/badge/Python-3.8%2B-blue)
![TensorFlow](https://img.shields.io/badge/TensorFlow-2.x-orange)
![Deep Learning](https://img.shields.io/badge/Domain-Real%20Estate-green)

## 📖 Overview
This repository hosts a comprehensive deep learning framework designed to predict house prices using a **Multi-Modal** approach. Unlike traditional models that rely solely on tabular data (e.g., number of bedrooms, location), this project fuses **visual data** (images of the houses) with **structured data** to improve prediction accuracy.

The core objective is to benchmark **21 different Convolutional Neural Network (CNN) architectures** to determine which backbone performs best for real estate valuation.

## 🧠 Architecture
The model uses a dual-branch neural network structure:

1.  **Visual Branch (CNN):** Processes images to extract aesthetic and condition-based features.
2.  **Tabular Branch (MLP):** Processes numerical and categorical data (Price, Location, Area, etc.).
3.  **Fusion Layer:** Concatenates outputs from both branches and passes them through a dense regression head.

```mermaid
graph LR
    A[Image Input] --> B[CNN Backbone (e.g., ResNet)]
    C[Tabular Input] --> D[Dense Network]
    B --> E[Concatenation]
    D --> E
    E --> F[Fully Connected Layers]
    F --> G[Final Price Prediction]

🔬 Models ImplementedWe compare the following 21 architectures as feature extractors:AlexNetNiN (Network in Network)ZfNetVGGGoogleNet (Inception V1)Inception-V3Highway NetworksInception-V4ResNet (Residual Networks)Inception-ResNet-v2FractalNetWideResNetXceptionResidual Attention NetworkSqueeze-and-Excitation (SE-Net)DenseNetCompetitive Squeeze and ExcitationMobileNet-V2CapsuleNetHRNetV2ResNeXt📂 DatasetThe model is trained on a dataset containing:Images: Exterior shots of properties.Tabular Data: Features including Location, Bedrooms, Bathrooms, Land Area ($m^2$), and Building Area.Target: Listing Price (USD).Note: The dataset used for this project focuses on the real estate market in Zimbabwe.🚀 Installation & UsageClone the repository
