# Momenta Audio Deepfake Detection Take-Home Assessment

## Description
This project is part of the Momenta take-home assessment and demonstrates an audio deepfake detection pipeline. The system streams `.flac` audio files directly from the ASVspoof 5 dataset archive and employs MFCC (Mel-Frequency Cepstral Coefficients) features combined with the AASIST model, a lightweight binary classification architecture, to classify audio as either real or spoof.

## Key Features
- Streams audio data directly without requiring local dataset downloads.
- Extracts MFCC features (13-dimensional) from streamed `.flac` files.
- Implements the AASIST model for efficient binary classification (real vs. spoof).
- Evaluates model performance using AUC-ROC as the primary metric.

## Notebook Overview
The implementation pipeline is structured into eight key steps within the Jupyter Notebook (`AASIST_Evaluation.ipynb`):
1. **Streaming Data**: Accesses `.flac` audio files from the dataset.
2. **Audio Validation**: Ensures streamed audio files are complete and usable for processing.
3. **Feature Extraction**: Extracts MFCC features for classification.
4. **Dataset Preparation**: Prepares train-test splits for model training and evaluation.
5. **Model Design**: Constructs the AASIST binary classification model.
6. **Model Training**: Trains the model using extracted MFCC features.
7. **Model Evaluation**: Evaluates model performance using AUC-ROC and other metrics.
8. **Performance Analysis**: Analyzes strengths, weaknesses, and areas for improvement.

## How to Use This Repository
### Clone the Repository

1. Clone this repository to your local machine using:
   ```bash
   git clone https://github.com/M-M-VALLI-SRIPADA/Momenta---Audio-Deepfake-Detection-Take-Home-Assessment.git
   cd Momenta---Audio-Deepfake-Detection-Take-Home-Assessment

2. Install Dependencies
Install the Python libraries listed in requirements.txt:
pip install -r requirements.txt

3. Run the Notebook
Open AASIST_Evaluation.ipynb in Jupyter Notebook or JupyterLab and execute the cells step by step:

Stream and validate .flac audio files.
Extract MFCC features from audio.
Train the binary classification model.
Evaluate model performance using the AUC-ROC metric.

**Results**
**Model Evaluation**
AUC-ROC Score: 0.5893

**Performance Observations:**

**Strengths:** Lightweight architecture and effective classification based on MFCC features.

**Weaknesses:** Potential limitations in handling noisy or unseen datasets.

**Reflection**

**Challenges Encountered
**
1. Streaming Audio Data: Addressed issues with corrupted .flac files by implementing validation methods.

2. Model Input Compatibility: Resolved mismatches between extracted MFCC features and the AASIST model's input dimensions.

3. Feature Consistency: Ensured uniform MFCC extraction across all audio samples to prevent inconsistencies.

**Real-World Applicability
**
1. While effective in controlled environments, the system requires further optimization for real-world scenarios, such as noisy or diverse datasets.

**Future Improvements
**
1. Experiment with alternative features, such as spectrograms, to enhance robustness.

2. Utilize datasets with greater diversity and introduce adversarial samples to improve generalization.

**Deployment Strategy
**
1. Automate real-time preprocessing for streaming and feature extraction.

2. Optimize the AASIST model for low-latency predictions in production environments, such as voice authentication systems.
