# Federated Learning Model Comparison & Generalizability

This repository provides two Jupyter notebooks to explore federated learning for disease classification using spectral data:

- **FL Comparisons.ipynb**: Compares federated learning strategies across neural network, SVM, and logistic regression models for 4 different aggregation strategies.
- **Generalization Test.ipynb**: Assesses the generalizability of federated models in comparison to other learning strategies.

This work supports ongoing research in federated learning and spectral-based disease classification.

## Contents

### FL Comparisons.ipynb

- Implements federated learning for three models: neural network (PyTorch), SVM (scikit-learn), logistic regression (scikit-learn).
- Supports multiple FL strategies (such as FedAvg, FedProx, FedAdam, FedOpt) with options for grid-search tuning.
- Trains and evaluates models using cross-validation, reporting metrics: accuracy, F1-score, precision, and recall.
- Includes baseline models: centralized, and local models as points of comparison.
- Aggregates and visualizes results for comparison.

### Generalization Test.ipynb

- Evaluates how well FL-trained models generalize to unseen client data.
- Processes spectral features with techniques such as B-spline basis functions and standard scaling.
- Splits data for cross-validation and federated simulation.
- Reports global federated, personalized federated (fine-tuned), local, averaged local, and centralized model performance.
- Designed for tomato disease classification based on spectral data.

## Requirements

- Python 3.8 or newer
- PyTorch
- scikit-learn, scipy
- numpy, pandas, matplotlib, seaborn
- flwr[simulation]  

Conda can handle all package dependencies other than Flower which requires pip install

## Usage

1. Ensure your spectral dataset is prepared and formatted as required by the notebooks (refer to example csv for naming and file format).
2. Open and run **FL Comparisons.ipynb** for model and FL strategy comparison.
3. Open and run **Generalization Test.ipynb** to evaluate federated generalizability.
4. Review the metric outputs and visualizations for analysis.

## Notes

- The notebooks are designed to be modular and easy to adapt to related spectral classification problems.
- Performance metrics and plots are saved for further analysis.
- If using Windows 11, ensure that Ray is using 2.48 or higher to prevent `ray.init()` and `ray start` issues.

## Acknowledgments

This couldn't have been possible without the help of Mohammad Amini and Dr. Mostafa Reisi Gahrooei at UF ISE. They helped tremendously throughout the course of this project. If there are any questions about the code feel free to contact me at lucaszhou2007@gmail.com
