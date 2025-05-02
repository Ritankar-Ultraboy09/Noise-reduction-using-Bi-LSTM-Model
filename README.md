# Denoising of Polysomnographic Signals Using RNN (Bi-LSTM)

# **Overview**
This project presents a deep learning-based approach for denoising Polysomnographic (PSG) signals using a Bidirectional LSTM Autoencoder. PSG signals such as EEG and EOG are often contaminated with noise due to movement artifacts and other disruptions during sleep studies. Our solution leverages robust preprocessing and RNNs to restore clean biomedical signal patterns, enhancing reliability for downstream analysis like sleep staging.

## **Motivation**
Polysomnography is widely used for diagnosing sleep disorders. However, raw PSG signals often contain high levels of noise due to patient movement, electrode shifts, and other interferences. This noise can severely hamper signal interpretation and clinical decision-making. Our goal is to preprocess and denoise these signals using Bi-LSTM, which excels at modeling time-series data in both forward and backward directions.

## **Dataset Description**
Source: PhysioNet.org
Data Types:
EEG Fpz-Cz [µV]
EEG Pz-Oz [µV]
EOG Horizontal [µV]
Folders Used:
Sleep Cassette (Healthy individuals)
Sleep Telemetry (Unhealthy individuals)

Format: EDF files converted to CSV via Polyman software

Sampling Frequency: 100Hz
