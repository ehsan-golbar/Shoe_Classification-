# Shoe_Classification

This project implements a Convolutional Neural Network (CNN) to classify shoe images into three categories. The goal is to achieve over 86% accuracy using advanced deep learning techniques and model optimizations.  

---

## Dataset and Preprocessing  
- Images resized to 224×224 and normalized using ImageNet values.  
- Random augmentations (rotation and horizontal flipping) applied.  
- Split into training (80%) and validation (20%) sets, processed in batches of 32.  

---

## Model Architecture  
- **ResNet50** used with **Transfer Learning**, pretrained on ImageNet.  
- All layers except the final Fully Connected layer were frozen.  
- The final layer was adjusted to match the number of shoe categories.  

---

## Training and Evaluation  
- **Loss Function:** CrossEntropyLoss  
- **Optimizer:** Adam with a learning rate of 0.001  
- Trained for 20 epochs, achieving:  
  - **75.44% validation accuracy**  
  - **72.81% test accuracy**  
- Evaluation metrics included Precision, Recall, F1-score, and Confusion Matrix analysis.  

---

## Model Improvements  
- Added Conv2D, BatchNorm, and deeper Fully Connected layers.  
- Fine-tuned deeper layers of ResNet (Layer 4 and Fully Connected).  
- Implemented **Learning Rate Scheduler** and **Early Stopping**.  
- Achieved **87.47% test accuracy** after enhancements.  

---

## How to Run  
1. **Install Dependencies**  
   ```bash
   pip install tensorflow torch numpy matplotlib scikit-learn

