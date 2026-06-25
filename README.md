# Motion Blur Image Restoration

A deep learning project for restoring sharp images from motion-blurred inputs using Convolutional Neural Networks (CNNs).

This project investigates image restoration techniques by training a neural network to reconstruct clean images from synthetically generated motion blur. The goal is to learn the mapping between blurred and sharp images and evaluate the model using common image quality metrics.

---

## Project Overview

Motion blur is a common problem in computer vision caused by camera movement or moving objects during image capture. This project applies deep learning to recover the original sharp image from a blurred version.

The workflow includes:

- Creating synthetic motion blur
- Preparing paired training data
- Building a CNN-based restoration model
- Training the network
- Evaluating reconstruction quality
- Visualizing prediction results

---

## Features

- Synthetic motion blur generation
- Image preprocessing pipeline
- CNN model for image restoration
- Training and validation workflow
- Performance evaluation
- Visualization of original, blurred, and restored images

---

## Project Structure

```
Motion-Blur/
│
├── data/
│   ├── original/
│   ├── blurred/
│
├── models/
│
├── notebooks/
│
├── src/
│   ├── dataset.py
│   ├── blur_generator.py
│   ├── model.py
│   ├── train.py
│   ├── predict.py
│   └── utils.py
│
├── outputs/
│
├── requirements.txt
└── README.md
```

---

## Technologies

- Python
- PyTorch
- OpenCV
- NumPy
- Matplotlib
- Jupyter Notebook

---

## Dataset

The project uses a dataset of clean images.

Motion blur is synthetically generated using OpenCV by applying linear motion kernels with different lengths and angles, allowing the model to learn under various blur conditions.

Example:

Original Image → Motion Blur → Restored Image

---

## Model

The restoration network is a Convolutional Neural Network (CNN) consisting of multiple convolutional layers with ReLU activation functions.

The network learns an end-to-end mapping:

```
Blurred Image → CNN → Restored Image
```

Loss Function:

- Mean Squared Error (MSE)

Optimizer:

- Adam

---

## Training

Install the required packages:

```bash
pip install -r requirements.txt
```

Train the model:

```bash
python train.py
```

Run inference:

```bash
python predict.py
```

---

## Evaluation

Model performance can be evaluated using:

- Mean Squared Error (MSE)
- Peak Signal-to-Noise Ratio (PSNR)
- Structural Similarity Index (SSIM)

Example metrics:

| Metric | Value |
|---------|--------|
| Training Loss | 0.0078 |
| PSNR | 29.6 dB |
| SSIM | 0.91 |

*(Replace these values with your actual results.)*

---

## Results

The model successfully reconstructs much of the lost image detail caused by motion blur.

Example visualization:

| Original | Blurred | Restored |
|----------|----------|-----------|
| Image | Image | Image |

(Add sample images from your project.)

---

## Future Improvements

- Implement a U-Net architecture
- Train on larger datasets
- Use real-world motion blur datasets
- Experiment with GAN-based deblurring models
- Improve image quality using perceptual loss

---

## Learning Outcomes

Through this project, I gained practical experience with:

- Deep Learning
- Convolutional Neural Networks
- Image Restoration
- Computer Vision
- PyTorch
- Image preprocessing
- Model evaluation

---

## References

- OpenCV Documentation
- PyTorch Documentation
- Motion Deblurring Research Papers
- Image Restoration Literature

---

## Author

**Amineh Yazdizadeh**

Automation Engineer | AI & Computer Vision

GitHub:
https://github.com/Amy396
