# Car Brand Classification

## Project Overview

This project focuses on **image classification** to identify car brands using **deep learning** techniques.  
It explores both **Fully Trained Neural Networks**(CNN) and **Transfer learning** (ResNet) for classification.  
Additionally, **Hyperparameter tuning** was conducted to optimize performance.

## Dataset

- **Total Samples:** 1463  
- **Size:** 105.2 MB  
- **Number of Classes:** 4    

### **Data Splits**
- **Training:** 1001 images  
- **Validation:** 250 images  
- **Testing:** 200 images  

### **Preprocessing**
- **Data Normalization:** Mean & Standard Deviation  
- **Data Augmentation:**  
  - Random Horizontal Flip  
  - Random Rotation  
  - Color Jitter  

## Model Architecture

### **Base Neural Network**
- Standard CNN architecture for image classification  
- **Loss Function:** `CrossEntropyLoss()`  
- **Optimizer:** Stochastic Gradient Descent (SGD)  

### **Transfer Learning**
- Pretrained **ResNet** model fine-tuned for car brand classification  

## Hyperparameter Tuning

**Optimization Algorithm:** Stochastic Gradient Descent (SGD)  

### **Tuned Hyperparameters**
| **Parameter**          | **Tuning Range** |
|------------------------|-----------------|
| Learning Rate         | 0.01 to 0.1     |
| Momentum             | 0.5 to 0.9      |
| Number of Layers     | 1 to 2          |
| Number of Filters    | 4 to 8          |
| Batch Size          | 4               |
| Epochs              | Tuned via Grid Search |

### **Optimization Strategies**
- **With Learning Rate Decay**  
- **Without Learning Rate Decay**  

ClearML Parallel coordinate plots were used to analyze parameter effectiveness.

## Results

### **Transfer Learning vs Fully Trained Neural Network**
- **Transfer Learning (ResNet)**: Higher accuracy with fewer training epochs  
- **Fully Trained NN**: Required more training but achieved competitive performance  

## Summary

This project successfully classifies car brands using **deep learning** and **transfer learning**.  
Key findings include:  
- **Transfer learning outperforms fully trained models in accuracy and efficiency**  
- **Grid search tuning significantly improved model performance**  
