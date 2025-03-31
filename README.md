# Rice-Grain-Classification-using-MobileNetV2

Rice Grain Classification using MobileNetV2
This project implements a CNN-based rice grain classification model using MobileNetV2 to differentiate between five rice varieties: Arborio, Basmati, Ipsala, Jasmine, and Karacadag. The dataset consists of 75,000 images (15,000 per class).
Dataset Preparation
The image dataset is divided into training (80%) and validation (20%) sets using ImageDataGenerator.

Training Set: 80% of the images, with data augmentation applied (rotation, zoom, shear, and horizontal flip) to improve model generalization.

Validation Set: 20% of the images, only rescaled for evaluation.

🚀 Project Overview
Model Used: MobileNetV2 (Pretrained on ImageNet)

Dataset: 75,000 rice grain images

Input Size: 224x224x3

Classes: 5

Evaluation Metrics: Accuracy, Precision, Recall, F1-Score

Hardware Used: CPU (Training on GPU recommended for faster processing)

📊 Performance Metrics
Class	Precision	Recall	F1-Score	Support
Arborio	1.00	0.96	0.98	3000
Basmati	0.99	0.99	0.99	3000
Ipsala	0.99	1.00	1.00	3000
Jasmine	0.99	0.99	0.99	3000
Karacadag	0.97	1.00	0.98	3000
Overall Accuracy	99%	99%	99%	15000
⏳ Training Details
Epochs: 2

Training Time:

Epoch 1: ~55 min (Accuracy: 89.58%, Val Acc: 98.62%)

Epoch 2: ~41 min (Accuracy: 96.95%, Val Acc: 98.71%)

Loss: Gradually decreased, indicating model convergence

⚡ Optimization Suggestions
🔹 Use a GPU (e.g., NVIDIA CUDA) to significantly reduce training time
🔹 Reduce image resolution (e.g., 128x128) for efficiency
🔹 Data Augmentation can further improve model robustness

Observations:

The model performs very well, with most predictions on the diagonal (correct classifications).

Misclassifications:

Arborio: 99 samples were misclassified.

Jasmine: Has some confusion with Basmati (22 samples misclassified).

Basmati & Ipsala: Almost perfect classification.
Future Improvements 📌 Data Augmentation: Further augmentation techniques (rotation, scaling, flipping) can help improve robustness. 📌 Hyperparameter Tuning: Fine-tuning MobileNetV2 architecture (learning rate, dropout) may enhance performance. 📌 Model Pruning & Quantization: Optimize for mobile and edge deployments without significant accuracy loss.
