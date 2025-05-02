# Denoising of Polysomnographic Signals Using RNN (Bi-LSTM)

# **Overview**
This project presents a deep learning-based approach for denoising Polysomnographic (PSG) signals using a Bidirectional LSTM Autoencoder. PSG signals such as EEG and EOG are often contaminated with noise due to movement artifacts and other disruptions during sleep studies. Our solution leverages robust preprocessing and RNNs to restore clean biomedical signal patterns, enhancing reliability for downstream analysis like sleep staging.

## **Motivation**
Polysomnography is widely used for diagnosing sleep disorders. However, raw PSG signals often contain high levels of noise due to patient movement, electrode shifts, and other interferences. This noise can severely hamper signal interpretation and clinical decision-making. Our goal is to preprocess and denoise these signals using Bi-LSTM, which excels at modeling time-series data in both forward and backward directions.

## **Dataset Description**
**Source** : https://www.physionet.org/static/published-projects/sleep-edfx/sleep-edf-database-expanded-1.0.0.zip

**Data Types:**
EEG Fpz-Cz [µV]
EEG Pz-Oz [µV]
EOG Horizontal [µV]

**Folders Used:**
Sleep Cassette (Healthy individuals)
Sleep Telemetry (Unhealthy individuals)

**Format** : EDF files converted to CSV via Polyman software
Link to Polyman Software Download :- https://www.edfplus.info/downloads/index.html
Sampling Frequency: 100Hz

## Preprocessing Steps
Chunking: Splitting data into 30s windows for manageable input size

Robust Scaling: Normalization using IQR to handle outliers

Z-score Outlier Removal: Threshold set to 2.5

Interpolation & Padding: Linear fill for missing values

Bandpass Filtering: 0.5–40Hz using scipy.signal

## Model Architecture
Model: Bidirectional LSTM Autoencoder

Input Shape: (samples, 30, 3)

Output Shape: Same as input (for reconstruction)

Encoder: BiLSTM compresses sequence to latent vector

Decoder: BiLSTM + Linear layer reconstructs clean signal


## requiurements.txt 
numpy==1.24.4
pandas==1.5.3
matplotlib==3.7.1
scipy==1.10.1
scikit-learn==1.2.2
tensorflow==2.15.0
seaborn==0.12.2
jupyterlab==3.6.3
torch == 2.1.2
``pip install -r requirements.txt``

