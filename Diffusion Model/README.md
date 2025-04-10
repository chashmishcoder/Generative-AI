# Image Diffusion Model Implementation

![Diffusion Process](https://github.com/chashmishcoder/Generative-AI/blob/main/Diffusion%20Model/diff_img.png)

## Overview

This repository contains an implementation of a diffusion-based generative model inspired by Denoising Diffusion Probabilistic Models (DDPM) and Denoising Diffusion Implicit Models (DDIM). The model demonstrates how to train a neural network to gradually denoise an image, starting from pure noise.

## Features

- 🧠 Neural network-based diffusion model with U-Net architecture
- 🔄 Forward diffusion process (adding noise gradually)
- ↩️ Reverse diffusion process (denoising to generate images)
- 📊 Training and sampling pipelines
- 🚀 Advanced techniques for better quality:
  - Self-attention mechanisms
  - Cosine noise schedule
  - EMA (Exponential Moving Average) model tracking
  - DDIM sampling for faster and higher quality generation

## Getting Started


## How It Works

### 1. Forward Diffusion

The forward diffusion process gradually adds noise to an image following a predefined schedule:

```python
x_t = sqrt(α_t) * x_0 + sqrt(1 - α_t) * ε
```

Where:
- `x_0` is the original image
- `x_t` is the noisy image at timestep t
- `α_t` is the cumulative product of (1-β_t)
- `ε` is random noise sampled from a normal distribution

### 2. Neural Network Training

The U-Net model is trained to predict the noise added during the forward process.

### 3. Reverse Diffusion

During sampling, we start with pure noise and gradually denoise using our model.

## Implementation Details

- **Architecture**: U-Net with self-attention and residual blocks
- **Sampling**: DDIM for faster, higher-quality sampling
- **Optimization**: AdamW with weight decay and learning rate scheduling
- **Stability**: Gradient clipping and EMA parameter updates

## Results

The model demonstrates the ability to reconstruct an image after complete destruction through the diffusion process.

Forward Diffusion Process
![Forward Diffusion Process](https://github.com/chashmishcoder/Generative-AI/blob/c493474bd0e8d79b2ad784f973906ccfa874ba7a/Diffusion%20Model/download%20(2).png)


Reverse Diffusion Process
![Reverse Diffusion Process](https://github.com/chashmishcoder/Generative-AI/blob/main/Diffusion%20Model/download%20(1).png)

## References

- [Denoising Diffusion Probabilistic Models (DDPM)](https://arxiv.org/abs/2006.11239)
- [Denoising Diffusion Implicit Models (DDIM)](https://arxiv.org/abs/2010.02502)
- [Improved Denoising Diffusion Probabilistic Models](https://arxiv.org/abs/2102.09672)

## License

This project is licensed under the MIT License - see the LICENSE file for details.
