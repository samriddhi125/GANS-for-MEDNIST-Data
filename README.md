# MedNist GAN Training

## Overview
This project explores the generation of medical images using three different Generative Adversarial Networks (GANs) trained on the MedNist dataset. The goal is to compare their performance in generating high-quality medical images across multiple categories. GANs are widely used for synthetic data generation, data augmentation, and anomaly detection in medical imaging.

### Models Used:
1. **Wasserstein GAN (WGAN)** - An improved version of GAN that replaces the traditional loss function with the Wasserstein distance to mitigate mode collapse and training instability.
2. **Wasserstein GAN with Gradient Penalty (WGAN-GP)** - An enhancement over WGAN that introduces a gradient penalty term to enforce the Lipschitz constraint more effectively, leading to better convergence and training stability.
3. **Least Squares GAN (LSGAN)** - A GAN variant that minimizes the Pearson χ² divergence by using a least squares loss function instead of binary cross-entropy, resulting in more stable training and high-quality image generation.

Each model is trained for **50 epochs**, and their performances are compared using the following evaluation metrics:
- **Inception Score (IS)**
- **Fréchet Inception Distance (FID)**
- **Visual inspection of generated images**

## Dataset
The **MedNist dataset** is a publicly available medical imaging dataset designed for deep learning applications. It includes six different types of medical images:
- **Abdomen CT**
- **Breast MRI**
- **Chest X-ray**
- **Hand X-ray**
- **Head CT**
- **Brain MRI**

The dataset is sourced from various medical imaging databases and has been preprocessed for deep learning tasks. The images are grayscale and of relatively small size, making them suitable for rapid training and experimentation with GANs.

## Evaluation Metrics
The trained models are evaluated using the following metrics:

- **Inception Score (IS):**
  - Measures the quality and diversity of generated images by using a pre-trained Inception model.
  - High IS indicates more realistic and diverse images.
  - Computed as:
    \[ IS = \exp (E_x [KL (p(y|x) || p(y))]) \]
  - Where \( p(y|x) \) is the conditional label distribution predicted by the Inception network, and \( p(y) \) is the marginal label distribution.

- **Fréchet Inception Distance (FID):**
  - Measures the similarity between real and generated images by comparing their feature distributions in a high-dimensional space.
  - Lower FID values indicate that the generated images are closer to real images.
  - Computed as:
    \[ FID = || \mu_r - \mu_g ||^2 + Tr(\Sigma_r + \Sigma_g - 2 (\Sigma_r \Sigma_g)^{1/2}) \]
  - Where \( \mu_r, \Sigma_r \) are the mean and covariance of real images and \( \mu_g, \Sigma_g \) are the mean and covariance of generated images.

- **Visual Inspection:**
  - Manually assessing image quality by observing sharpness, details, and overall realism.
  - Checking for mode collapse, artifacts, and unnatural structures in generated images.

## Results
| Model    | Inception Score (IS) | FID Score |
|----------|----------------------|-----------|
| WGAN     | TBD                  | TBD       |
| WGAN-GP  | TBD                  | TBD       |
| LSGAN    | TBD                  | TBD       |
