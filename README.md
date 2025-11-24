## Comparative Analysis for 3D Ear Mesh Dimensionality Reduction

This repository contains the scripts and final presentation for a proprietary deep learning project focused on compressing and analyzing a large dataset of 3D human ear mesh scans. The primary goal was to determine the optimal dimensionality reduction method for capturing population-level variation and accurately reconstructing complex ear geometry for audio device design.

### Project Overview & Problem Statement

Designing comfortable and high-performing audio devices is challenging due to the wide variation in human ear geometry. This project compared the effectiveness of PCA (linear), UMAP (non-linear), and Variational Autoencoder (VAE) (non-linear, generative) for reducing $3\text{D}$ ear mesh data across latent dimensions $n=1$ to $30$.

Accuracy was evaluated using the Mean Squared Error (MSE) and relative error of four key anatomical features: cavum width, height, depth, and tragus-antitragus distance.

---

### Methodology Highlights

The data pipeline involved generating and storing 10,000 unique ear meshes and then applying dimensionality reduction across the latent space.

**PCA (Principal Component Analysis):** Applied SVD to the flattened $2\text{D}$ data matrix, prepared with Z-score normalization.
**UMAP (Uniform Manifold Approximation and Projection):** Fitted UMAP using Stochastic Gradient Descent (SGD) for non-linear embedding. Reconstruction was performed using a supervised regressor model.
**VAE (Variational Autoencoder):** Implemented a VAE with a PointNet-inspired encoder and a mirrored MLP decoder. The model was trained with SGD ($\text{lr} = 10^{-2}$) and minimized the combined MSE and Kullback-Leibler (KL) divergence losses.

---

## IP Status

Materials are currently under Intellectual Property (IP) review by our institutional and corporate partners. Scripts that are under review contain placeholder variables in place of proprietary numerical constants and are not executable.
