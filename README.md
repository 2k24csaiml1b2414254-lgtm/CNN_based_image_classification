# CNN-Based Image Classification using PyTorch

A Convolutional Neural Network (CNN) built with PyTorch to classify images from the CIFAR-10 dataset into 10 different categories.

## Overview

This project demonstrates the fundamentals of deep learning and computer vision by building and training a CNN on the CIFAR-10 image dataset.

The model learns visual features through convolutional layers and pooling operations, then uses fully connected layers to predict the image category.

## Features

- CIFAR-10 dataset loading using Torchvision
- Image preprocessing and normalization
- Custom CNN architecture using PyTorch
- Model training with Adam optimizer
- Cross-entropy loss for multiclass classification
- Test-set accuracy evaluation
- Downloadable dataset through Torchvision

## Tech Stack

- Python
- PyTorch
- Torchvision
- CNN (Convolutional Neural Network)
- CIFAR-10

## Model Architecture

The CNN consists of three convolutional blocks:

1. **Convolutional Layer 1:** 3 input channels → 32 feature maps
2. **Convolutional Layer 2:** 32 → 64 feature maps
3. **Convolutional Layer 3:** 64 → 128 feature maps

Each block uses ReLU activation and max pooling.

The extracted features are flattened and passed through:
- Fully connected layer: 2048 → 256
- Output layer: 256 → 10 classes

The model returns logits for the 10 CIFAR-10 categories.

## Dataset

CIFAR-10 contains 60,000 colour images of size 32 × 32 pixels, divided into 10 classes:

- Airplane
- Automobile
- Bird
- Cat
- Deer
- Dog
- Frog
- Horse
- Ship
- Truck

The dataset includes 50,000 training images and 10,000 test images.

## Project Structure

```text
CNN_based_image_classification/
├── CNN_for_CIFAR10.py
├── README.md
└── cnn working image.jpg
```

The dataset is downloaded into the `data/` directory when the script runs.

## Installation

### 1. Clone the repository

```bash
git clone https://github.com/2k24csaiml1b2414254-lgtm/CNN_based_image_classification.git
cd CNN_based_image_classification
```

### 2. Install dependencies

```bash
python -m pip install torch torchvision
```

### 3. Run the model

```bash
python CNN_for_CIFAR10.py
```

The CIFAR-10 dataset will be downloaded automatically if it is not already available locally.

## Training Configuration

| Parameter | Value |
|---|---|
| Dataset | CIFAR-10 |
| Batch size | 64 |
| Epochs | 10 |
| Optimizer | Adam |
| Loss function | CrossEntropyLoss |
| Output classes | 10 |
| Image normalization | Mean 0.5, standard deviation 0.5 per channel |

## Results

The script prints the average training loss for each epoch and calculates classification accuracy on the test dataset.

**Test accuracy:** Add the actual measured accuracy after running the script.

## Future Improvements

- Add GPU support using CUDA
- Track training and validation metrics across epochs
- Save and load trained model weights
- Visualize sample predictions and misclassified images
- Experiment with data augmentation and learning-rate scheduling
- Compare the CNN with a deeper architecture

## Learning Outcomes

- Understanding CNN architecture and feature extraction
- Working with PyTorch datasets and DataLoaders
- Implementing forward propagation and backpropagation
- Training a multiclass image classifier
- Evaluating model performance on unseen data

