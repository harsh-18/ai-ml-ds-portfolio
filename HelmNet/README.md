# SafeHelmetProjectCV – Helmet Detection for Worker Safety

## Overview
SafeHelmetProjectCV is a computer vision project designed to detect helmet usage among workers, ensuring safety compliance in industrial environments.  
The model leverages Convolutional Neural Networks (CNNs) and VGG‑16 architecture, combined with preprocessing and augmentation techniques, to achieve robust detection.

## Dataset Summary
- Total images: 631
- With Helmet (label = 1): 311
- Without Helmet (label = 0): 320
- Image shape: (200 x 200 x 3)

The dataset is balanced, with nearly equal representation of both classes.

## Pipeline
1. **Data Preprocessing**
   - Grayscale conversion and normalization [0,1]
   - Pixel distribution analysis
   - Augmentation (rotation, flipping, brightness adjustments)
2. **Model Development**
   - Baseline CNN
   - VGG‑16 (Base)
   - VGG‑16 + Feedforward Neural Network (FFNN)
   - VGG‑16 + FFNN + Augmentation
3. **Training & Validation**
   - Accuracy/loss monitoring
   - Confusion matrix analysis
4. **Deployment Considerations**
   - Latency vs. accuracy trade-offs
   - Real-time detection pipeline design

## Key Learnings & Insights
- **Technical Insight:** Augmentation improved generalization and reduced overfitting.  
- **Business Insight:** Automated helmet detection can reduce workplace accidents and compliance costs.  
- **Personal Learning:** Hands‑on experience in CNN tuning, hyperparameter optimization, and deployment trade-offs.

## Results
- **Baseline CNN:** Validation accuracy ~98% with stable loss curves  
- **VGG‑16 (Base):** Validation accuracy near 100% with strong generalization  
- **VGG‑16 + FFNN:** Validation accuracy consistently at 100%  
- **VGG‑16 + FFNN + Augmentation:** Validation accuracy consistently at 100%  
- **Final Test Evaluation (VGG‑16 Base):**
  - Test Accuracy: **100%**
  - Test Loss: **0.0498**
  - Classification Report: Perfect precision, recall, and F1-score for both classes
  - Confusion Matrix: Zero misclassifications

## Visualizations
- Class distribution
- Preprocessing example (grayscale + normalization)
- Sample outputs (helmet vs. no helmet)
- Training curves (CNN, VGG‑16, VGG‑16+FFNN, VGG‑16+Aug)
- Confusion matrices (validation and test sets)

## Visualizations

### Sample Images From Dataset
![Quick View](https://github.com/user-attachments/assets/ce1eaa2c-9b3c-41f7-868b-4deea8a65901)

### Class Distribution Histogram
![Histogram](https://github.com/user-attachments/assets/d6bae7bc-498d-443c-a67a-731a39ccb1a7)

### Preprocessing Example
![Image Processing](https://github.com/user-attachments/assets/f1c5c56e-9480-4dbf-af51-0ec3b6694f97)

### Training Curves – Baseline CNN
![Training Plot](https://github.com/user-attachments/assets/b2803da9-5bd4-4b8d-89d3-9ecc12b56552)

### Confusion Matrix – CNN
![CNN Confusion Matrix](https://github.com/user-attachments/assets/978bdc8d-115a-4e52-b2b2-bfa7ee26cfea)

### Training Curves – VGG‑16
![VGG Training Curves](https://github.com/user-attachments/assets/c349b416-8a0e-479f-bda0-cc9e2ecacfa0)

### Confusion Matrix – VGG‑16 Base
![VGG‑16 Base Confusion Matrix](https://github.com/user-attachments/assets/973dce19-81ee-4a27-9961-974b0ef3cb70)

### Training Curves – VGG‑16 + FFNN
![VGG‑16 + FFNN Training](https://github.com/user-attachments/assets/06a48799-388c-4235-bc86-2fb2dd3d16d6)

### Confusion Matrix – VGG‑16 + FFNN
![VGG‑16 + FFNN Confusion Matrix](https://github.com/user-attachments/assets/a054db33-e2b5-44ac-a775-03e67b4454d0)

### Training Curves – VGG‑16 + FFNN + Augmentation
![VGG‑16 + FFNN + Aug Training](https://github.com/user-attachments/assets/44776293-3f14-4db0-ade8-2c5d430b4f56)

### Confusion Matrix – VGG‑16 + Augmentation
![VGG + Aug Confusion Matrix](https://github.com/user-attachments/assets/7c8f0d4a-e9b5-458c-be91-1303a2381a26)

### Test Set Confusion Matrix – VGG‑16
![VGG Test Confusion Matrix](https://github.com/user-attachments/assets/36bc56a0-aef5-4c2f-9930-38d0bc1bb4f5)

## Actionable Insights & Recommendations
1. **Deploy VGG‑16 base model** in automated monitoring systems — reliable and ready for real-world use.  
2. **Enable real-time monitoring** at construction and industrial sites to flag non-compliance instantly.  
3. **Optimize operational efficiency:**  
   - With accuracy already ideal, focus on reducing latency and resource usage.  
   - For edge devices, consider lighter models (MobileNet, EfficientNet) if hardware limits arise.  
4. **Continuous retraining:**  
   - Real-world conditions (lighting, angles, PPE styles) evolve.  
   - Schedule periodic retraining with fresh site images to maintain robustness.  
5. **Error prevention:**  
   - Monitor for false positives/negatives post-deployment.  
   - Build a feedback loop: flagged images reviewed and added to future training sets.  
6. **Compliance & privacy:**  
   - Anonymize worker images (blur/mask faces) before storage.  
   - Prefer on-device inference to reduce data transfer risks.  
   - Store only minimal metadata for audits.  
7. **Scalability:**  
   - Integrate seamlessly into CCTV or IoT camera systems.  
   - Use batch inference for large-scale monitoring across multiple industrial zones.

## Environment & Dependencies
See `requirements.txt` for exact versions.  
To recreate the environment:

