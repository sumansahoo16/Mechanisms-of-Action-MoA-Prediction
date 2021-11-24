# Mechanisms of Action (MoA) Prediction

### Problem Statement 

In pharmacology, the term Mechanism of Action (MoA) refers to the specific biochemical interaction through which a drug substance produces its pharmacological effect.
The task is predicting multiple targets of the Mechanism of Action (MoA) responses of different samples. Samples are drugs profiled at different time points and doses.

### Features

Features with g- prefix are gene expression features and there are 772 of them (from g-0 to g-771)
Features with c- prefix are cell viability features and there are 100 of them (from c-0 to c-99)
cp_type, cp_time, cp_dose :  categorical features 
PCA feature are used for all models with different n_components (50 genes + 15 cells for 1D-CNN, 600 genes + 50 cells for TabNet and DNN).
Statistical features (such as mean, min, max, skew, kurt, (X_train>9).sum(axis=1) ) and combination features are used in Tabnet.
Variance fillter is used in Tabnet and DNN.
Sample Normalization

### Modelling
- ResNet-like shallow NN
- 2 Head NN
- RNN
- TabNet
