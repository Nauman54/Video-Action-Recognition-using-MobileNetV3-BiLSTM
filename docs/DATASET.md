# 📂 Dataset

This project uses the **UCF101 - Action Recognition** dataset provided on Kaggle by **Matthew Jansen**. The dataset is a preprocessed version of the original UCF101 benchmark and is already organized into **training**, **validation**, and **testing** subsets, making it ready for deep learning workflows.

---

# 📌 Dataset Overview

| Property | Value |
|----------|-------|
| Dataset | UCF101 - Action Recognition |
| Source | Kaggle |
| Original Dataset | UCF101 (CRCV, University of Central Florida) |
| Total Classes | 101 |
| Total Videos | 13,320 |
| Dataset Type | Video Classification |
| Framework | PyTorch |
| Evaluation | Classification Accuracy, Confusion Matrix, ROC Curve |

---

# 📥 Download

Download the dataset from Kaggle:

https://www.kaggle.com/datasets/matthewjansen/ucf101-action-recognition

The dataset is approximately **6–7 GB** after extraction.

---

# 📁 Dataset Structure

After downloading and extracting, the dataset should have the following structure:

```text
ucf101-action-recognition/

│
├── train/
│   ├── ApplyEyeMakeup/
│   ├── ApplyLipstick/
│   ├── Archery/
│   ├── ...
│   └── YoYo/
│
├── val/
│   ├── ApplyEyeMakeup/
│   ├── ApplyLipstick/
│   ├── ...
│   └── YoYo/
│
├── test/
│   ├── ApplyEyeMakeup/
│   ├── ApplyLipstick/
│   ├── ...
│   └── YoYo/
│
├── train.csv
├── val.csv
└── test.csv
```

Each action class contains multiple video clips stored in AVI format.

The accompanying CSV files provide:

- Video filename
- Relative path
- Action label

---

# 📊 Dataset Statistics

| Attribute | Value |
|-----------|-------|
| Action Classes | 101 |
| Total Videos | 13,320 |
| Training Set | 75% |
| Validation Set | 12.5% |
| Testing Set | 12.5% |
| Video Source | YouTube |
| Video Format | AVI |

The Kaggle version follows a **75% / 12.5% / 12.5%** train/validation/test split, allowing models to be trained and evaluated without creating custom splits.

---

# 🏷️ Action Categories

The dataset contains a diverse range of human activities, including:

- Sports
- Human–Object Interaction
- Human–Human Interaction
- Body Motion
- Musical Instrument Performance

Example classes include:

- Basketball
- Basketball Dunk
- Cricket Bowling
- Diving
- Golf Swing
- Horse Riding
- Playing Guitar
- Playing Piano
- Soccer Juggling
- Tennis Swing
- Volleyball Spiking
- YoYo

---

# 🔄 Data Processing Pipeline

The project processes every video through the following pipeline:

```text
Video
   │
   ▼
Frame Extraction
   │
   ▼
Resize Frames
(224 × 224)
   │
   ▼
Normalization
   │
   ▼
Sequence Generation
(Fixed Number of Frames)
   │
   ▼
PyTorch Dataset
   │
   ▼
Model Training
```

---

# 🧠 Model Input

Each input video is transformed into a sequence of frames before being passed to the network.

Processing steps include:

- Read video using OpenCV
- Extract frames
- Resize frames to **224 × 224**
- Normalize pixel values
- Convert frames to tensors
- Create a fixed-length sequence
- Feed the sequence into MobileNetV3

The extracted feature sequence is then processed by the Bi-LSTM network for temporal modeling.

---

# 📈 Model Evaluation

The trained model is evaluated on the **test split** using:

- Classification Accuracy
- Confusion Matrix
- ROC Curve

## Final Test Accuracy

**81.41%**

---

# 📚 Original Dataset

The Kaggle dataset is derived from the original **UCF101** benchmark introduced by the Center for Research in Computer Vision (CRCV), University of Central Florida. It contains realistic human action videos collected from YouTube and is one of the most widely used benchmarks for action recognition research. :contentReference[oaicite:2]{index=2}

---

# 📖 Citation

If you use the UCF101 dataset in your research, please cite:

```bibtex
@article{soomro2012ucf101,
  title={UCF101: A Dataset of 101 Human Actions Classes From Videos in The Wild},
  author={Soomro, Khurram and Zamir, Amir Roshan and Shah, Mubarak},
  journal={CRCV-TR-12-01},
  year={2012}
}
```
