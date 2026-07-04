# 📂 Dataset

This project uses the **UCF101 Action Recognition Dataset** available on Kaggle, a pre-organized version of the original UCF101 dataset designed for deep learning and video classification tasks.

The dataset contains **13,320 labeled video clips** spanning **101 human action classes**, including sports, musical instrument playing, body movements, and human-object interactions. It is widely used as a benchmark dataset for evaluating video action recognition models. :contentReference[oaicite:0]{index=0}

---

# 📊 Dataset Overview

| Property | Value |
|-----------|------:|
| Dataset Name | UCF101 Action Recognition |
| Source | Kaggle |
| Total Classes | 101 |
| Total Videos | 13,320 |
| Video Format | AVI |
| Data Type | RGB Videos |
| Framework | PyTorch |
| Task | Human Action Recognition |

---

# 📥 Dataset Download

Download the dataset from Kaggle:

**https://www.kaggle.com/datasets/matthewjansen/ucf101-action-recognition** :contentReference[oaicite:1]{index=1}

You can also download the original dataset from the University of Central Florida:

**https://www.crcv.ucf.edu/research/data-sets/ucf101/** :contentReference[oaicite:2]{index=2}

---

# 📁 Dataset Structure

The Kaggle dataset is already organized into training, validation, and testing directories, making it convenient for deep learning workflows. It also includes CSV annotation files containing video names, paths, and class labels. :contentReference[oaicite:3]{index=3}

```text
UCF101_Action_Recognition/

│
├── train/
│   ├── ApplyEyeMakeup/
│   ├── Archery/
│   ├── Basketball/
│   ├── ...
│
├── validation/
│   ├── ApplyEyeMakeup/
│   ├── Archery/
│   ├── Basketball/
│   ├── ...
│
├── test/
│   ├── ApplyEyeMakeup/
│   ├── Archery/
│   ├── Basketball/
│   ├── ...
│
├── train.csv
├── validation.csv
└── test.csv
```

---

# 📈 Dataset Split

The Kaggle version provides a predefined split:

| Split | Percentage |
|--------|-----------:|
| Training | 75% |
| Validation | 12.5% |
| Testing | 12.5% |

This predefined split helps ensure consistent evaluation across experiments. :contentReference[oaicite:4]{index=4}

---

# 🎯 Action Categories

The dataset contains **101 human action classes** grouped into five major categories:

- 🏀 Sports
- 🎸 Playing Musical Instruments
- 🤝 Human-Human Interaction
- 🏃 Body Motion
- 🛠 Human-Object Interaction

Example classes include:

- Basketball
- Basketball Dunk
- Cricket Bowling
- Diving
- Golf Swing
- Horse Riding
- Playing Guitar
- Playing Piano
- Playing Violin
- Soccer Juggling
- Tennis Swing
- Volleyball Spiking
- Walking With Dog
- YoYo

---

# ⚙️ Data Preprocessing

The preprocessing pipeline used in this project consists of:

```text
Input Video
      │
      ▼
Frame Extraction
      │
      ▼
Resize (224 × 224)
      │
      ▼
Pixel Normalization
      │
      ▼
Data Augmentation
      │
      ▼
Fixed-Length Frame Sequence
      │
      ▼
PyTorch Dataset
```

The processed frame sequences are then passed to the MobileNetV3 backbone for spatial feature extraction, followed by a Bi-LSTM network for temporal sequence modeling.

---

# 🧠 Model Input

Each input sample consists of:

- RGB video frames
- Fixed-length frame sequence
- Image size: **224 × 224**
- Tensor format compatible with PyTorch

---

# 📊 Model Evaluation

The trained model was evaluated using:

- Classification Accuracy
- Confusion Matrix
- ROC Curve

### Final Performance

| Metric | Value |
|---------|------:|
| Test Accuracy | **81.41%** |

---

# 📚 Why UCF101?

UCF101 is one of the most widely adopted benchmark datasets for video action recognition because it:

- Contains diverse real-world videos collected from YouTube.
- Covers 101 challenging action categories.
- Includes significant variations in camera motion, viewpoint, illumination, background clutter, and object appearance.
- Provides a standardized benchmark for comparing action recognition models. :contentReference[oaicite:5]{index=5}

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

---

# 🔗 References

- **Kaggle Dataset:** https://www.kaggle.com/datasets/matthewjansen/ucf101-action-recognition :contentReference[oaicite:6]{index=6}
- **Original UCF101 Dataset:** https://www.crcv.ucf.edu/research/data-sets/ucf101/ :contentReference[oaicite:7]{index=7}
- **Original Research Paper:** https://arxiv.org/abs/1212.0402 :contentReference[oaicite:8]{index=8}
