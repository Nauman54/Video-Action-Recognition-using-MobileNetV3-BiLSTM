# Installation Guide

This document explains how to set up the Video Action Recognition project using PyTorch.

---

# Prerequisites

Before installing the project, ensure the following software is installed:

- Python 3.10 or later
- Git
- pip
- Jupyter Notebook
- NVIDIA GPU (Recommended)
- CUDA Toolkit (Optional but recommended)

---

# Clone the Repository

```bash
git clone https://github.com/Nauman54/Video-Action-Recognition-using-MobileNetV3-BiLSTM.git

cd Video-Action-Recognition-using-MobileNetV3-BiLSTM
```

---

# Create a Virtual Environment (Recommended)

### Windows

```bash
python -m venv venv

venv\Scripts\activate
```

### Linux / macOS

```bash
python3 -m venv venv

source venv/bin/activate
```

---

# Upgrade pip

```bash
python -m pip install --upgrade pip
```

---

# Install Dependencies

```bash
pip install -r requirements.txt
```

---

# Verify PyTorch Installation

Run the following command:

```python
import torch

print(torch.__version__)
print(torch.cuda.is_available())
```

If CUDA is installed correctly, the second command should return:

```
True
```

---

# Launch Jupyter Notebook

```bash
jupyter notebook
```

Open

```
notebooks/Video_Action_Recognition.ipynb
```

---

# Project Workflow

The notebook performs the following tasks:

- Dataset Loading
- Video Frame Extraction
- Image Preprocessing
- Data Augmentation
- MobileNetV3 Feature Extraction
- Bi-LSTM Sequence Learning
- Model Training
- Model Evaluation
- Prediction
- Saving Best Model

---

# Output Files

After training, the following files are generated:

```
outputs/
│
├── confusion_matrix.png
└── roc_curve.png
```

---

# Troubleshooting

### CUDA not detected

Check:

```python
import torch
print(torch.cuda.is_available())
```

If False, reinstall the CUDA-enabled version of PyTorch.

---

### Missing Package

Install manually:

```bash
pip install package_name
```

---

### Notebook Kernel Missing

```bash
pip install ipykernel

python -m ipykernel install --user
```

---

# Recommended Hardware

Minimum

- Intel i5 / Ryzen 5
- 8 GB RAM
- CPU Training

Recommended

- NVIDIA RTX GPU
- CUDA 11.8+
- 16 GB RAM
