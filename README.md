# StyleGAN from Scratch 🧠🎨

This project is an implementation of StyleGAN from scratch using PyTorch, as part of the Deep Learning Technologies course (DATA 255) at San Jose State University.

## 📚 Project Overview

We recreated StyleGAN, a state-of-the-art generative adversarial network for high-resolution face generation. The model design and training methodology are inspired by the original paper:  
**[A Style-Based Generator Architecture for GANs – Karras et al. (2019)](https://arxiv.org/pdf/1812.04948)**.

Key features implemented:
- Custom generator and discriminator using PyTorch
- Progressive growing from 4×4 to 256×256 resolution
- AdaIN layers for style injection
- Latent mapper with separate learning rate
- WGAN-GP for stable training
- Noise injection and minibatch stddev layers

## 🧪 Results

| Step | Description                         | Sample Output |
|------|-------------------------------------|---------------|
| 0    | Random noise                        | ![step_0](results/step_0.png) |
| 3    | Emerging facial features            | ![step_3](results/step_3.png) |
| 5    | Recognizable faces with artifacts   | ![step_5](results/step_5.png) |
| 6    | High-quality, realistic face output | ![step_6](results/step_6.png) |

**Metrics:**
- FID Score: ~123 (Step 5)
- PPL Score: ~1800 (Smooth latent interpolation)

## 🔧 Setup

Install dependencies:
```bash
pip install -r requirements.txt
