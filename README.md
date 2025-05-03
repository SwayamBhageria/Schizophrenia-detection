

# 🧠 Schizophrenia Detection Using EEG Signals

A deep learning-based approach to classify schizophrenic and healthy individuals using EEG spectrogram data. This project leverages signal processing techniques, Gabor filtering, data augmentation, and a CNN-LSTM architecture to achieve high classification accuracy on EEG recordings.


## 📁 Project Overview

Schizophrenia is a complex neuropsychiatric disorder. This project presents a pipeline that processes EEG signals and uses deep learning to identify schizophrenia from brainwave patterns. The final model achieves over **97% classification accuracy** with low memory requirements and short training times.



## 🧪 Dataset

* **Source**: [brain.bio.msu.ru/eeg\_schizophrenia.htm](http://brain.bio.msu.ru/eeg_schizophrenia.htm)
* **Subjects**:

  * 45 Schizophrenic Patients
  * 39 Healthy Controls
* **Channels**: 16 EEG channels
* **Sampling Rate**: 128 Hz
* **Preprocessing**: Converted to 5-second segments, each transformed into a **224×224 spectrogram image**



## ⚙️ Methodology

### 1. **Preprocessing**

* Wavelet transform applied to EEG segments
* Spectrogram generation for time-frequency representation
* Normalization and resizing of images

### 2. **Feature Extraction**

* Applied **Gabor Filter Bank** to enhance frequency-specific features from spectrograms

### 3. **Data Augmentation**

* Used a **Variational Autoencoder (VAE)** to synthesize realistic spectrograms and mitigate class imbalance

### 4. **Model Architecture**

* **CNN-LSTM Hybrid Model**:

  * Convolutional layers for spatial feature extraction
  * LSTM layer to capture temporal dynamics across EEG channels
* Optimizer: Adam
* Loss Function: Categorical Crossentropy
* Accuracy Achieved: **97.1%**


## 📊 Results

| Metric    | Value |
| --------- | ----- |
| Accuracy  | 97.1% |
| Precision | 96.8% |
| Recall    | 97.4% |
| F1 Score  | 97.1% |

---

## 🛠️ Tech Stack

* Python
* TensorFlow / Keras
* NumPy, OpenCV, SciPy
* Matplotlib, Seaborn
* Wavelet transforms (PyWavelets)
* EEG Data Handling (MNE-Python)



## 🧩 Folder Structure

```
├── data/                # EEG spectrogram images
├── preprocessing/       # Wavelet & Gabor transforms
├── models/              # CNN-LSTM and VAE models
├── notebooks/           # Jupyter notebooks for exploration
├── results/             # Metrics, plots, and confusion matrices
├── README.md
└── requirements.txt
```

---


## 📈 Visualizations

* Spectrogram samples
* Filter outputs (Gabor layers)
* Training/validation accuracy
* Confusion matrix

---

## 📚 References

* EEG Dataset: [http://brain.bio.msu.ru/eeg\_schizophrenia.htm](http://brain.bio.msu.ru/eeg_schizophrenia.htm)
* Relevant Research Papers (add citations here)
* Deep Learning for EEG (Goodfellow et al., 2016)

---




