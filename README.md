# Histopathologic-Cancer-Detection
CNN comparison for detecting cancer in histopathology images (96x96 RGB tissue patches).
Results
Enhanced CNN: 97.05% AUC (140K params) - WINNER
Simple CNN: 91.80% AUC (93K params)
ResNet50: 79.25% AUC (23.8M params) - Failed badly
Key Findings

Enhanced CNN won with batch normalization + dropout
ResNet50 failed due to domain mismatch (ImageNet ≠ medical images)
Architecture design > model complexity

Models

Simple CNN: Basic 3-layer baseline
Enhanced CNN: Added BatchNorm, Dropout, double convolutions
ResNet50: Transfer learning from ImageNet (frozen weights)

Hyperparameter Tuning
Learning Rates: 0.01 (95.71%) | 0.001 (97.05%) | 0.0001 (92.20%)
Optimizers: RMSprop (96.31%) | Adam (95.29%)
