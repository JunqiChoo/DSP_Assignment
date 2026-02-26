🎧 CEG3004 DSP Mini Project
Environmental Sound Classification
Student Information

CHOO JUN QI — 2302735
LIM XIN RU — 2302791

Project Overview

This project implements a complete Digital Signal Processing (DSP) and Machine Learning pipeline for environmental sound classification.

The full implementation is contained in:

CEG3004_Project_Colab_2302791_2302735.ipynb

The notebook performs:

Dataset loading and validation

Audio preprocessing

Feature extraction (MFCC, log-mel, spectral features)

Model training using Support Vector Machine (SVM)

Validation using Macro-F1 score

Submission prediction generation

System Requirements

Python 3.9 – 3.11 (Recommended: Python 3.10)

Jupyter Notebook installed

8GB RAM recommended

Check Python version:

python --version
Installation Instructions
1. Clone Repository
git clone https://github.com/JunqiChoo/DSP_Assignment.git
cd DSP_Assignment
2. Create Virtual Environment

Windows:

python -m venv venv
venv\Scripts\activate

Mac/Linux:

python3 -m venv venv
source venv/bin/activate
3. Install Required Dependencies
pip install numpy scipy pandas scikit-learn librosa soundfile tqdm joblib matplotlib ipywidgets
How to Run the Project

Activate virtual environment

Start Jupyter:

jupyter notebook

Open:

CEG3004_Project_Colab_2302791_2302735.ipynb

Run all cells from top to bottom

The notebook will:

Load dataset

Extract audio features

Train SVM model

Evaluate validation performance

Save trained model

Generate submission predictions

DSP & Feature Engineering Pipeline

The pipeline includes:

Silence trimming

Peak normalization

Fixed 5-second waveform padding/truncation

Pre-emphasis filtering

MFCC (20 coefficients)

Delta and Delta-Delta features

Log-mel spectrogram statistics

Spectral centroid

Spectral bandwidth

Spectral rolloff

Zero-crossing rate

Model Configuration

Classifier: Support Vector Machine (SVM)
Kernel: RBF
C = 10
Gamma = scale
Class weight = balanced

Pipeline:
StandardScaler → SVC

Evaluation Metric:
Macro-F1 Score

Output Files Generated

After running the notebook, the following files are generated:

<GROUP_ID>_model.joblib

<GROUP_ID>_predictions.csv

These are the required submission files.