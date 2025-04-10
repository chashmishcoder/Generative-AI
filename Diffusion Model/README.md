# Image Diffusion Model Implementation

![Forward Diffusion Process](https://github.com/chashmishcoder/Generative-AI/blob/c493474bd0e8d79b2ad784f973906ccfa874ba7a/Diffusion%20Model/download%20(2).png)

![Reverse Diffusion Process](https://github.com/chashmishcoder/Generative-AI/blob/main/Diffusion%20Model/download%20(1).png)
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

### Prerequisites

Make sure you have Python 3.8+ installed. Then install the required packages:

```bash
pip install -r requirements.txt
