# 🖼️ Image Denoising using Custom CNN Architecture

A deep learning project that removes Gaussian noise from images using a custom Convolutional Neural Network (CNN) built with TensorFlow/Keras. The model is trained and evaluated on the CIFAR-10 dataset with synthetically added noise.

---

## 📌 Overview

Image noise is a common problem in digital photography, medical imaging, and computer vision. This project demonstrates how a custom CNN architecture can effectively learn to reconstruct clean images from noisy inputs.

---

## 🚀 Key Features

- Custom CNN architecture designed for image reconstruction
- Gaussian noise simulation on CIFAR-10 dataset
- Training and validation loss curve visualization
- Quantitative evaluation using PSNR and SSIM metrics
- Visual comparison of noisy vs denoised vs original images

---

## 📊 Dataset

**CIFAR-10** — 60,000 RGB images (32×32) across 10 classes

| Split | Images |
|---|---|
| Training | 50,000 |
| Testing | 10,000 |

Gaussian noise with factor **0.25** was synthetically added to simulate real-world image degradation.

---

## 🧠 Model Architecture

Custom Sequential CNN with 5 convolutional layers:

| Layer | Filters | Activation |
|---|---|---|
| Conv2D | 64 | ReLU |
| Conv2D | 64 | ReLU |
| Conv2D | 32 | ReLU |
| Conv2D | 64 | ReLU |
| Conv2D (Output) | 3 | Sigmoid |

- **Total Parameters:** 77,411
- **Optimizer:** Adam
- **Loss Function:** Mean Squared Error (MSE)
- **Epochs:** 10

---

## 📈 Results

| Metric | Value |
|---|---|
| PSNR | 22.04 dB |
| SSIM | 0.7565 |

Higher PSNR indicates better noise reduction. SSIM of 0.75+ indicates good structural similarity with the original image.

---

## 💻 Tech Stack

| Category | Tools |
|---|---|
| Language | Python |
| Deep Learning | TensorFlow, Keras |
| Data Processing | NumPy |
| Visualization | Matplotlib |
| Evaluation | scikit-image (PSNR, SSIM) |

---

## ▶️ Run the Notebook

Open directly in Google Colab:

1. Upload `Image_Denoising_CNN.ipynb` to Colab
2. Set runtime to **GPU (T4)** for faster training
3. Run all cells sequentially

---

## 📸 Visual Results

The notebook includes visual comparison of:
- Noisy input images
- Original clean images
- CNN denoised output images

---

## 📈 Future Improvements

- Implement U-Net architecture for better denoising
- Test on higher resolution datasets
- Experiment with different noise levels and types
- Add batch normalization for improved training stability
