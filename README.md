# ECG Arrhythmia Classification from Heartbeat Features

This project explores whether individual heartbeat measurements — timing 
between beats, waveform amplitude, and shape statistics — can be used to 
classify ECG rhythms as Normal, Supraventricular, or Ventricular arrhythmia. 
Working with the MIT-BIH Arrhythmia Database (100,604 heartbeats from 48 
patients), I split the data by patient rather than by row to ensure a 
clinically honest evaluation, avoiding the risk of the model learning 
individual patients' rhythm quirks rather than general arrhythmia patterns.

The dataset is heavily imbalanced, with Normal beats making up roughly 90% 
of the data — a realistic reflection of clinical practice, where 
arrhythmias are the rare exception. A baseline Random Forest classifier 
achieved 91% overall accuracy, but this figure masked a critical weakness: 
only 8% of true Supraventricular arrhythmias were correctly identified. 
Applying SMOTE (Synthetic Minority Oversampling Technique) to the training 
data nearly tripled Supraventricular recall to 22%, at the cost of overall 
accuracy and precision — a genuine clinical trade-off rather than a clean 
improvement.

This project is not intended as a diagnostic tool, but as an honest 
exploration of the challenges involved in detecting rare, clinically 
significant conditions in imbalanced real-world clinical data — directly 
relevant to decision-support and predictive modeling work in healthcare AI.
