# 🧠 Motor Imagery EEG Analysis – Mini Project Summary

## 1. Objective

To analyze EEG signals during motor imagery and identify characteristic changes in the mu (8–13 Hz) and beta (13–30 Hz) frequency bands, as well as compare neural patterns between left and right hand imagery.


## Workflow Overview

### 1. Data Loading

- PhysioNet EEG Motor Movement/Imagery Dataset (EEGMMIDB, 1.0.0)

- 1–2 healthy participants performing left and right-hand motor imagery

### 2. Preprocessing
- Bandpass filter: 7–30 Hz- ICA and artifact removal- Epoching (-0.2 s to 4 s)
Clean signal and isolate trials per condition


### 3. Event Segmentation
- Extracted epochs labeled left_hand and right_hand

- Separate experimental conditions

### 4. Time–Frequency Analysis
- Morlet wavelet transform to compute ERD/ERS

- Visualize desynchronization in mu/beta bands

### 5. Feature Extraction & Classification
- Extracted power spectral features; used Logistic Regression

- Assess model’s ability to distinguish motor imagery
 
### 6. Visualization
- ERD/ERS maps- Topographic maps- Comparison plots for left vs right hand
  
- Summarize neural activation and lateralization

## 3. Key Results
- ERD/ERS Analysis: Clear desynchronization around 10–20 Hz during motor imagery, stronger in contralateral (C3/C4) electrodes.
  
- Left vs Right Hand Evoked Response: Distinct time-locked differences visible in event-related potentials.
  
- Classification Accuracy: ~50–65% using logistic regression (baseline chance = 50%), suggesting reproducible but moderate discrimination with single-subject data.
  
- Observation: Accuracy improves when filter bandwidth widened to 5–40 Hz and with more trials included.

## 4. Discussion
- The observed mu and beta suppression supports known motor imagery physiology (ERD during imagined movement).

- Limited accuracy attributed to small sample size, limited trial count, and natural EEG noise.
  
- Future improvement: multi-subject training, spatial filtering (CSP), and feature optimization.
## 5. Tools and Envirnoment

### Tools: Python (MNE 1.5+), NumPy, Matplotlib, Scikit-learn

### Environment: Google Colab, Code adaptation: https://mne.tools/stable/auto_tutorials/intro/10_overview.html 

## Author 
## Dr Yonatan Yotora, MD

## Adare General Hospital, Hawassa
