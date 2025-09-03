# Machine_Learning_Neural_Engineering
This repository builds a neural decoding pipeline: preprocess spike data, reduce dimensionality (PCA/KPCA), classify with SVM.

The steps are:
Data Loading & Preprocessing where trainSpike is training spike data (features), trainState is corresponding labels (states), and testSpike is test data for prediction.
Data is cleaned by removing NaN labels and aligning spike features with valid states.

Exploratory Visualization
Raw spike data is plotted to show amplitude over time.
Training/test signals are displayed for first 50 samples.

Dimensionality Reduction (Feature Extraction)
Principal Component Analysis (PCA) and Kernel PCA applied to spike data.
This reduces high-dimensional neural activity into a few components that capture most variance and enables visualization (2D/3D plots).

Classification
Uses Support Vector Machines (SVMs) for supervised classification.
This finds a decision boundary (hyperplane) that maximizes the margin between classes.

Performance Evaluation
Checks classification accuracy, confusion matrices, and plots decision boundaries in PCA-transformed space.

Also PCA vs Kernel PCA are compared for nonlinear structure in spike data.

PCA finds orthogonal directions (principal components) that maximize variance computed via eigen-decomposition of covariance matrix.

Kernel PCA extends PCA by mapping data into a higher-dimensional feature space using a kernel.
This captures nonlinear patterns in spike data that linear PCA might miss.

The interpretation in Neuroscience Context is the spike trains are high-dimensional and noisy so PCA/KPCA reduces redundancy and noise.

SVM classifies neural states (possibly movement intentions, sensory responses, or stimulus categories).

Together, PCA + SVM form a common pipeline in brain-machine interfaces and neural decoding.
