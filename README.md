# DSCA-BiGRU: Signer-Independent Kannada Sign Language Recognition

## Overview

This repository contains the implementation of the research paper:

**"A Dual Stream Cross Attention Bidirectional Gated Recurrent Network for Signer-Independent Sign Language Recognition Using Skeletal Landmarks"**

The proposed DSCA-BiGRU framework performs signer-independent Kannada Sign Language (KSL) recognition using MediaPipe Holistic skeletal landmarks and a lightweight dual-stream Bidirectional GRU architecture with adaptive cross-attention.

---

## Repository Contents

| File | Description |
|------|-------------|
| DSCA-BiGRU.ipynb | Complete implementation including preprocessing, training, evaluation, and inference |
| ksl_features.h5 | Trained DSCA-BiGRU model |
| label_map.json | Mapping between gesture labels and class names |
| manifest.csv | Dataset metadata used during experiments |
| dataset link.txt | Google Drive link to the processed landmark dataset |
| README.md | Repository documentation |

---

## Dataset

Due to participant privacy and institutional ethical requirements, the original sign language video recordings cannot be publicly distributed.

The processed skeletal landmark dataset used in this work is publicly available through the Google Drive link provided in:

```
dataset link.txt
```

The dataset contains MediaPipe Holistic landmark representations extracted from the original videos and is sufficient to reproduce the reported experiments.

---

## Experimental Dataset

- Number of gesture classes: **31**
- Number of signers: **9**
- Evaluation protocol: **Signer-Independent**
- Test signer: **Person 1**
- Sequence length: **40 frames**
- Feature dimension: **225 landmarks per frame**
- Canonical grouping used to prevent augmentation leakage.

---

## Model

The proposed DSCA-BiGRU model consists of:

- Dual-stream skeletal representation
- Bidirectional GRU encoders
- Adaptive Cross-Attention Fusion
- Residual Multi-Head Self-Attention
- Learnable Attention Pooling
- Softmax classifier

The trained model is provided as:

```
ksl_features.h5
```

---

## Software Requirements

- Python 3.10+
- TensorFlow / Keras
- NumPy
- OpenCV
- MediaPipe
- Pandas
- Scikit-learn
- Matplotlib

Install dependencies using:

```bash
pip install tensorflow numpy opencv-python mediapipe pandas scikit-learn matplotlib
```

---

## Running the Project

1. Download the processed dataset using the Google Drive link provided in:

```
dataset link.txt
```

2. Open

```
DSCA-BiGRU.ipynb
```

3. Execute the notebook sequentially.

The notebook performs:

- Dataset loading
- Feature preprocessing
- Model training
- Evaluation
- Signer-independent testing
- Performance visualization
- Prediction

---

## Reported Results

Best Validation Accuracy

```
87.03%
```

Signer-Independent Test Accuracy

```
68.71%
```

Weighted Precision

```
67.93%
```

Weighted Recall

```
68.71%
```

Weighted F1-score

```
65.21%
```

---

## Reproducibility

This repository contains:

- Complete implementation
- Trained model
- Dataset access link
- Label mapping
- Dataset metadata

These materials are provided to enable independent reproduction of the experimental results reported in the manuscript.

---

## Data Availability

The processed skeletal landmark dataset used in this study is publicly accessible through the Google Drive link provided in:

```
dataset link.txt
```

The original raw sign-language videos are not publicly released due to participant privacy and institutional ethical restrictions.

---

## Citation

If you use this repository, please cite:

```
Gurusiddappa Hugar and Ramesh M. Kagalkar.

A Dual Stream Cross Attention Bidirectional Gated Recurrent Network for Signer-Independent Sign Language Recognition Using Skeletal Landmarks.

Pattern Analysis and Applications.
```

---

## Contact

Gurusiddappa Hugar

Email:
gurusidda.h@gmail.com
