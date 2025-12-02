# CDS521 Course Dissertation: Label Noise Analysis & CNN Implementation

This repository contains the source code and experimental data for the CDS521 Course Dissertation. The project focuses on addressing **Label Noise** in computer vision tasks using Deep Learning methods.

## Project Overview

The primary goal of this project is to evaluate the robustness of Convolutional Neural Networks (CNNs) against label noise and compare them with Multi-Layer Perceptrons (MLPs). We implemented **Importance Weighting** and **Transition Matrix Estimation (T-revision)** to mitigate the impact of noisy labels.

### Datasets Analyzed
The code performs analysis on three datasets with varying degrees of complexity and noise:

1.  **CIFAR-10** (Main focus of the report)
    * A standard benchmark for image classification.
    * Used to demonstrate the general efficacy of CNNs.
2.  **FashionMNIST0.3.npz** (Synthetic Noisy Data)
    * FashionMNIST dataset with **30% label noise**.
    * Used to test model robustness under moderate noise conditions.
3.  **FashionMNIST0.6.npz** (Synthetic Noisy Data)
    * FashionMNIST dataset with **60% label noise**.
    * Used to test model robustness under extreme noise conditions.

## Methodology

* **Models**: 
    * **CNN**: A custom Convolutional Neural Network with 2 convolutional layers and max-pooling.
    * **MLP**: A baseline Multi-Layer Perceptron.
* **Techniques**:
    * **Importance Weighting**: Reweighting samples to reduce the influence of likely mislabeled data.
    * **Transition Matrix Estimation**: Estimating the noise transition matrix to correct loss calculations.

## Getting Started

### Prerequisites
* Python 3.8+
* PyTorch
* NumPy
* Matplotlib
* Scikit-learn

### Running the Code
1.  Clone this repository:
    ```bash
    git clone [https://github.com/k8v8ia-wq/CDS521_Dissertation.git](https://github.com/k8v8ia-wq/CDS521_Dissertation.git)
    ```
2.  Open the Jupyter Notebook:
    ```bash
    jupyter notebook "5328ass2(2) (11).ipynb"
    ```
3.  Run the cells sequentially to reproduce the training loss curves and accuracy results.

## Results Highlights

* **CIFAR-10**: The CNN model achieved a mean accuracy of **65.52%**, outperforming the MLP baseline.
* **FashionMNIST (Noisy)**: The CNN with importance weighting showed significant resilience, maintaining high accuracy even on the 0.6 noise dataset compared to standard training methods.

## Authors
* ZHENG Guangyuan
