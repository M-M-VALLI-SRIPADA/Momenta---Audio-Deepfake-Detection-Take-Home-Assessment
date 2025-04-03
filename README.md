# Momenta Audio Deepfake Detection Take-Home Assessment

## Description
This project is part of the **Momenta take-home assessment** and demonstrates an **audio deepfake detection pipeline**. The system streams `.flac` audio files directly from the **ASVspoof 5 dataset archive** and employs **MFCC (Mel-Frequency Cepstral Coefficients)** features combined with the **AASIST model**, a lightweight binary classification architecture, to classify audio as either **real** or **spoof**.

---

## Key Features
- 📥 **Streams audio data directly** without requiring local dataset downloads.  
- 🎶 **Extracts MFCC features** (13-dimensional) from streamed `.flac` files.  
- 🧠 Implements the **AASIST model** for efficient binary classification (**real vs. spoof**).  
- 📊 **Evaluates model performance** using **AUC-ROC** as the primary metric.

---

## Notebook Overview
The implementation pipeline is structured into **eight key steps** within the Jupyter Notebook (`AASIST_Evaluation.ipynb`):

1. **Streaming Data**: Access `.flac` audio files from the dataset.  
2. **Audio Validation**: Ensure streamed audio files are complete and usable for processing.  
3. **Feature Extraction**: Extract MFCC features for classification.  
4. **Dataset Preparation**: Prepare train-test splits for model training and evaluation.  
5. **Model Design**: Construct the AASIST binary classification model.  
6. **Model Training**: Train the model using extracted MFCC features.  
7. **Model Evaluation**: Evaluate model performance using **AUC-ROC** and other metrics.  
8. **Performance Analysis**: Analyze strengths, weaknesses, and areas for improvement.

---

## How to Use This Repository

### Clone the Repository
Clone this repository to your local machine using:


git clone https://github.com/M-M-VALLI-SRIPADA/Momenta---Audio-Deepfake-Detection-Take-Home-Assessment.git

cd Momenta---Audio-Deepfake-Detection-Take-Home-Assessment

## Install Dependencies
Install the Python libraries listed in requirements.txt:
pip install -r requirements.txt

## Run the Notebook
Open AASIST_Evaluation.ipynb in Jupyter Notebook or JupyterLab and execute the cells step by step:

1. 📥 Stream and validate .flac audio files

2. 🎶 Extract MFCC features from audio

3. 🧠 Train the binary classification model

4. 📊 Evaluate model performance using AUC-ROC

## Results
**Model Evaluation**: AUC-ROC Score: 0.5893

## Performance Observations

**Strengths**:
1. Lightweight architecture
2. Effective classification using MFCC features

**Weaknesses**:
1. Limitations in handling noisy or unseen datasets

## Reflection

**Challenges Encountered**:

1. **Streaming Audio Data**: Resolved issues with corrupted .flac files by implementing validation methods

2. **Model Input Compatibility**: Addressed mismatches between extracted MFCC features and the AASIST model's input dimensions

3. **Feature Consistency**: Ensured uniform MFCC extraction across all audio samples to prevent inconsistencies

## Real-World Applicability

While effective in controlled environments, the system requires further optimization for noisy or diverse datasets.

## Future Improvements

1. Experiment with **alternative features** like spectrograms to enhance robustness

2. Utilize datasets with greater diversity and introduce **adversarial samples** for improved generalization

## Deployment Strategy

1. Automate **real-time preprocessing** for streaming and feature extraction

2. Optimize the **AASIST model** for low-latency predictions in production environments, such as **voice authentication systems**
