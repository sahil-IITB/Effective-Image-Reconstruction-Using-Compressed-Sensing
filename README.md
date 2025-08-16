# Effective Image Reconstruction using Various Compressed Sensing Techniques

## 📌 Overview
This project explores **image reconstruction** techniques using **Compressed Sensing (CS)** with emphasis on **Discrete Transforms** and **Deep Learning**.  
Compressed Sensing leverages the **sparsity of signals** in specific domains (e.g., Wavelet, Fourier, DCT) to reconstruct images from fewer measurements than traditional Nyquist-Shannon sampling, making it highly effective in **resource-constrained environments** such as:
- Medical Imaging 🩻
- Autonomous Vehicles 🚗
- Surveillance Systems 🎥

We implemented and compared three major approaches:
1. **Flexible Compressed Sensing (DFT/IDFT)**
2. **Compressed Sensing with Discrete Cosine Transform (DCT)**
3. **Deep Learning-based Autoencoder**

---

## ⚙️ Implementations

### 1. Flexible Compressed Sensing Transformation
- Applied **DFT** → manipulated frequency components → **IDFT** for reconstruction.
- PSNR used as a quality metric.
- Extended to **color images** (RGB channels processed independently).
- ✅ Simple, no training needed.  
- ⚠️ Limited flexibility, potential frequency-domain artifacts.

---

### 2. Compressed Sensing with Discrete Cosine Transform (DCT)
- Divided image into blocks and randomly sampled pixels.
- Constructed measurement matrix with **DCT basis**.
- Reconstructed via **Lasso Regression** for sparse recovery.
- ✅ High reconstruction quality with proper sparsity.  
- ⚠️ Computationally heavier, needs tuning of regularization.

---

### 3. Deep Learning Based Approach
- Built a **Convolutional Autoencoder** to reconstruct masked images.
- Steps:
  - Image preprocessing (grayscale, resizing).  
  - Random pixel masking (30%).  
  - Encoder–Decoder network reconstruction.  
  - Evaluation with **MSE** and **PSNR**.  
- ✅ State-of-the-art performance, low artifacts.  
- ⚠️ Requires **large datasets** and **high computational resources**.

---

## 📊 Comparison of Methods

| Method | Domain | Quality | Complexity | Training |
|--------|--------|---------|------------|----------|
| Flexible CS (DFT/IDFT) | Frequency domain | Moderate | Low–Moderate | ❌ |
| CS with DCT | Sparse domain | High | Moderate–High | ❌ |
| Deep Learning (Autoencoder) | Learned features | Very High | High | ✅ Large datasets |

---

## 📂 Project Structure
