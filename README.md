This repository compares classical machine learning methods on the PathMNIST dataset that consists of 28×28 RGB histology image patches sampled from colon tissue slides, covering 9 distinct tissue classes. It is part of the [MedMNIST benchmark](https://medmnist.com/), designed for lightweight biomedical image classification tasks.  

## Files
- `rf_boost.ipynb`  
  Implements a classical ML pipeline:  
  `StandardScaler → PCA(95%) → SMOTE → RandomizedSearchCV`  
  for Random Forest and AdaBoost classifiers.  
  - Strengths: lightweight, interpretable, decent baseline accuracy.  
  - Limitations: performance bottleneck due to PCA feature compression and lack of spatial awareness.  

- `vgg16.ipynb`  
  A custom VGG16-like CNN tailored for the patches.  
  Includes Batch Normalization, Dropout, Adam optimizer, learning-rate scheduling, and early stopping.  
  - Significantly outperforms classical baselines, capturing local texture and spatial patterns, achieving overall accuracy of 91%.

Architecture:  
<p align="center">
<img width="8172" height="3291" alt="out-1" src="https://github.com/user-attachments/assets/fa8059a6-39f5-41d2-bfc4-ef5ae0cc7c75" />
</p>
