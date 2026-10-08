# Feature Extraction for EEG Epileptic Seizure Detection & Classification

## Academic Context
This repository contains a collaborative project developed for the **Fundamentals of Machine Learning** course during the BS Physics program at the Pakistan Institute of Engineering and Applied Sciences (PIEAS). The research was conducted under the supervision of Prof. Dr. Shahzad Ahmad Qureshi, with contributions from team members Amina Akbar, Anza Arooj, Fatima Rehman, and Fatima Shahid.

## Project Overview
The objective of this framework is to develop an automated classification system capable of detecting epileptic seizures from long-duration Electroencephalography (EEG) recordings. By applying signal processing and sequential modeling to time-series data, this system aims to replace labor-intensive manual inspections with efficient, objective diagnostic insights.

## Dataset
The project utilizes the Epileptic Seizure Recognition dataset, derived from the Bonn University EEG database.
* **Dimensions:** 11,500 continuous EEG samples across 179 columns.
* **Features:** 178 variables representing raw electrical amplitude readings, sampled at 178 Hz over exactly 1 second.
* **Target Classes:** 5 perfectly balanced classes (2,300 samples each).
  * *Class 1:* Epileptic seizure activity (Target class).
  * *Classes 2-5:* Baseline/normal neurological states (e.g., eyes open, eyes closed, healthy brain area, tumor area).
    <img width="990" height="660" alt="image" src="https://github.com/user-attachments/assets/903504eb-78ae-45d8-b1f4-40d33c4a8f20" />


## Preprocessing Pipeline
* Data cleaning to remove extraneous index columns, missing values, and duplicates.
* Z-score normalization applied to scale amplitude features.
* Dataset partitioned into an 80:20 train-test split.

## Models & Performance Evaluation
Traditional machine learning algorithms were benchmarked against sequential deep learning architectures. Deep learning proved significantly more effective for this specific temporal data:
* **SVM (Polynomial Degree 3):** Achieved 78.96% overall accuracy.
* **KNN (k=1):** Achieved 75.00% overall accuracy.
* **Attention-Based LSTM:** Achieved 85.00% overall accuracy. The inclusion of a Long Short-Term Memory network equipped with an attention layer provided superior capability in mapping the sequential memory and time dependencies inherent in EEG signals.
  <img width="771" height="678" alt="image" src="https://github.com/user-attachments/assets/8d8e118a-4f55-466c-b0b5-2137711e3ba4" />
<img width="1035" height="728" alt="image" src="https://github.com/user-attachments/assets/d912e5ca-3014-46ca-83fb-000c1c090e3c" />
