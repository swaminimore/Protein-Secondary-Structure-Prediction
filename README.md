# Protein-Secondary-Structure-Prediction
This repository contains code and resources for residue-level protein secondary structure prediction using deep learning. The project trains and evaluates a convolutional neural network (CNN) on large-scale benchmarks (CullPDB for training; CB513 for testing) and achieves high Q3 accuracy for helix, sheet, and coil classification.

# Features
- Modern Python (TF/Keras) deep learning pipeline
- Preprocessed datasets: Direct use of CullPDB (train) and CB513 (test) from PiPred
- Best practices to prevent data leakage (checks for sequence overlap)
- Class imbalance handling via sample weights
- Evaluation with Q3 accuracy and per-class precision/recall/F1
- Visualization: Training curves and confusion matrix

# Results
- Q3 Accuracy on CB513 test set: ~96.6% (see discussion below)
- No overlap between train and test datasets (checked programmatically)
- Detailed per-class metrics and confusion matrix available

#Dataset Preparation
Datasets Source: PiPred: https://lbs.cent.uw.edu.pl/pipred

**Files used:**
- cullpdb+profile_6133_filtered_updated.npy (training set)
- cb513+profile_split1_updated.npy (test set)
