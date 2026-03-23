# Pokemon-Autoencoder

## Overview
This project implements a convolutional variational autoencoder (VAE) for representation learning on Pokémon fusion image data. The goal is to learn compact latent representations that preserve important visual and semantic information for reconstruction and downstream tasks.

## Model
The model is a convolutional encoder–decoder architecture with a variational bottleneck. The encoder extracts hierarchical features and maps inputs to a latent distribution (mean and variance). Latent variables are sampled during training using the reparameterization trick. The decoder reconstructs images from latent representations.

The architecture includes:
- Convolutional encoder with downsampling
- Latent space with Gaussian parameterization
- Transposed convolutional decoder
- Residual blocks for improved reconstruction quality

## Data
The dataset consists of Pokémon fusion images used for unsupervised representation learning. Labels are provided as type combinations (e.g., "fire,water") for evaluation tasks.

## Training Objective
The model is trained to:
- Minimize reconstruction error between input and output images
- Learn meaningful latent representations for downstream classification

## Evaluation
The learned representations are evaluated using:
- Reconstruction quality (image fidelity)
- Linear probing on latent features for classification

## Usage
1. Load dataset  
2. Train the model using the provided architecture  
3. Encode images into latent vectors  
4. Decode latent vectors to reconstruct images  

## Notes
This project focuses on balancing compression and reconstruction quality while maintaining useful representations under model and computational constraints.
