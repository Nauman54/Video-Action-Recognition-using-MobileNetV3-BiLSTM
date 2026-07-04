# UCF101 Dataset

This project is trained and evaluated using the **UCF101 Human Action Recognition Dataset**, one of the most widely used benchmark datasets for video action recognition.

---

# Dataset Overview

| Property | Value |
|-----------|------:|
| Dataset | UCF101 |
| Total Classes | 101 |
| Total Videos | 13,320 |
| Video Type | Real-world Human Actions |
| Resolution | Variable |
| Split | Train / Validation / Test |

---

# Action Categories

The dataset contains 101 action classes covering:

- Sports
- Human-object interaction
- Playing musical instruments
- Body motion
- Daily activities

Examples include:

- Basketball
- Basketball Dunk
- Soccer Juggling
- Cricket Bowling
- Tennis Swing
- Playing Guitar
- Playing Piano
- Diving
- Horse Riding
- Push Ups
- Pull Ups
- Skiing
- YoYo
- Walking With Dog

---

# Dataset Structure

```
UCF101/

├── ApplyEyeMakeup/
├── ApplyLipstick/
├── Archery/
├── BabyCrawling/
├── BalanceBeam/
├── ...
└── YoYo/
```

Each folder contains videos belonging to one action category.

---

# Download

Download the dataset from the official website:

https://www.crcv.ucf.edu/data/UCF101.php

---

# Dataset Preparation

After downloading:

1. Extract the dataset.
2. Place the dataset in your preferred directory.
3. Update the dataset path inside the notebook.

Example:

```python
DATASET_PATH = "D:/Datasets/UCF101"
```

---

# Data Processing Pipeline

The preprocessing pipeline includes:

```
Videos
      │
      ▼
Frame Extraction
      │
      ▼
Resize
      │
      ▼
Normalization
      │
      ▼
Data Augmentation
      │
      ▼
Frame Sequence Generation
      │
      ▼
PyTorch Dataset
```

---

# Model Input

Each video is converted into:

- Fixed-length frame sequences
- Resized images
- Normalized tensors

These tensors are passed to MobileNetV3 for feature extraction.

---

# Training Split

The dataset is divided into:

- Training Set
- Validation Set
- Test Set

for robust model evaluation.

---

# Evaluation

The model is evaluated using:

- Classification Accuracy
- Confusion Matrix
- ROC Curve

Final Test Accuracy

```
81.41%
```

---

# Citation

If you use the UCF101 dataset in your research, please cite:

```
Soomro, K., Zamir, A. R., & Shah, M. (2012).

UCF101: A Dataset of 101 Human Actions Classes From Videos in the Wild.

CRCV-TR-12-01.
```
