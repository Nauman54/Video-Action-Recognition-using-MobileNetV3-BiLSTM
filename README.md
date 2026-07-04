# 🎥 Video Action Recognition using MobileNetV3 + Bi-LSTM

[![Python](https://img.shields.io/badge/Python-3.10+-blue.svg)]()
[![PyTorch](https://img.shields.io/badge/PyTorch-Deep%20Learning-red.svg)]()
[![OpenCV](https://img.shields.io/badge/OpenCV-Computer%20Vision-green.svg)]()
[![License](https://img.shields.io/badge/License-MIT-yellow.svg)]()

A deep learning framework for **human action recognition in videos** using **MobileNetV3** for spatial feature extraction and **Bi-LSTM** for temporal sequence modeling. The model is trained and evaluated on the **UCF101** dataset using PyTorch, with support for mixed precision training, automated evaluation, and video inference.

---

# 📌 Features

- Human Action Recognition from videos
- MobileNetV3 feature extraction
- Bi-LSTM temporal sequence modeling
- Mixed Precision Training (AMP)
- Automatic dataset preprocessing
- Training & Validation pipeline
- Model checkpoint saving
- Confusion Matrix generation
- ROC Curve visualization
- Classification Report
- Video inference on custom videos
- GPU acceleration using CUDA

---

# 🧠 Model Architecture

The proposed framework consists of the following stages:

```
Input Video
      │
      ▼
Frame Extraction
      │
      ▼
Frame Preprocessing
      │
      ▼
MobileNetV3 Backbone
(Spatial Features)
      │
      ▼
Feature Sequence
      │
      ▼
Bi-LSTM
(Temporal Learning)
      │
      ▼
Fully Connected Layer
      │
      ▼
Softmax Classifier
      │
      ▼
Predicted Action
```

---

# 🏗️ Project Pipeline

<p align="center">
<img src="assets/pipeline.png" width="900">
</p>

---

# 📂 Repository Structure

```text
Video-Action-Recognition-MobileNetV3-BiLSTM/

│
├── assets/
│   ├── architecture.png
│   ├── pipeline.png
│   ├── confusion_matrix.png
│   ├── roc_curve.png
│   ├── training_loss.png
│   ├── validation_accuracy.png
│   ├── sample_prediction.png
│
├── docs/
│   ├── DATASET.md
│   ├── INSTALLATION.md
│
├── notebooks/
│   ├── Video_Action_Recognition.ipynb
│
├── outputs/
│   ├── best_model.pth
│   ├── classification_report.txt
│   ├── confusion_matrix.png
│   ├── roc_curve.png
│   ├── training_curves.png
│
├── LICENSE
│
├── README.md
│
└── requirements.txt
```

---

# 📊 Dataset

The project uses the **UCF101 Human Action Recognition Dataset**.

### Dataset Statistics

- 101 Action Classes
- 13,320 Videos
- Real-world Human Activities
- Sports, Daily Activities, Musical Instruments

For dataset preparation, refer to:

📄 **docs/DATASET.md**

---

# ⚙️ Installation

Clone the repository

```bash
git clone https://github.com/yourusername/Video-Action-Recognition-MobileNetV3-BiLSTM.git

cd Video-Action-Recognition-MobileNetV3-BiLSTM
```

Install dependencies

```bash
pip install -r requirements.txt
```

For detailed installation instructions, see

📄 **docs/INSTALLATION.md**

---

# 🚀 Training

Run the notebook

```
notebooks/Video_Action_Recognition.ipynb
```

The notebook performs:

- Dataset Loading
- Frame Extraction
- Data Augmentation
- Model Training
- Validation
- Evaluation
- Saving Best Model

---

# 🎯 Inference

Load the trained model and provide any input video.

Output:

```
Input Video

↓

Predicted Class

↓

Confidence Score
```

Example

```
Video

↓

Basketball Dunk

↓

Confidence: 98.4%
```

---

# 📈 Results

The repository includes:

- Training Loss
- Validation Accuracy
- Confusion Matrix
- ROC Curve
- Classification Report

Example outputs are available inside the **outputs/** directory.

---

# 📷 Sample Results

## Model Architecture

<p align="center">
<img src="assets/architecture.png" width="850">
</p>

---

## Confusion Matrix

<p align="center">
<img src="assets/confusion_matrix.png" width="650">
</p>

---

## ROC Curve

<p align="center">
<img src="assets/roc_curve.png" width="650">
</p>

---

## Sample Prediction

<p align="center">
<img src="assets/sample_prediction.png" width="700">
</p>

---

# 🛠️ Technologies Used

- Python
- PyTorch
- TorchVision
- OpenCV
- NumPy
- Matplotlib
- Scikit-learn
- Pillow
- tqdm

---

# 🔮 Future Improvements

- Vision Transformer (ViT)
- TimeSFormer
- SlowFast Networks
- 3D CNNs
- EfficientNet Backbone
- Real-time Webcam Inference
- Streamlit/Web Application
- ONNX/TensorRT Deployment

---

# 📜 License

This project is licensed under the MIT License.

---

# 👨‍💻 Author

**Nauman Ahmed**

AI Engineer | Computer Vision | Deep Learning | Generative AI

If you find this project useful, consider giving it a ⭐ on GitHub.
