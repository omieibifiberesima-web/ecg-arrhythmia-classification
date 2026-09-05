# ecg-arrhythmia-classification
An ML project classifying ECG heartbeats (Normal, Supraventricular, Ventricular) from 48 MIT-BIH patients. To avoid data leakage, data was split by patient (38 train/10 test). Using SMOTE to handle class imbalance tripled Supraventricular recall (8%→22%) and raised Ventricular recall (68%→77%), prioritizing recall over raw accuracy.
