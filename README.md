# Fashion MNIST Classification using Neural Network

Classify apparel images from the Fashion-MNIST dataset using a custom-built fully connected neural network in PyTorch.

## Features
-  Multi-class image classification  
-  Custom fully connected neural network (no CNNs)  
-  Fashion-MNIST dataset with 10 apparel categories  
-  Implemented end-to-end in PyTorch  

## Table of Contents
- [Introduction](#introduction) 
- [Objective](#objective)
- [Dataset](#dataset)
- [Evaluation Criteria](#evaluation-criteria)
- [Solution Approach](#solution-approach)
- [License](#license)

## Introduction
The [Fashion-MNIST dataset](https://github.com/zalandoresearch/fashion-mnist) is a drop-in replacement for the original MNIST digits dataset. It contains apparel images and provides a more challenging benchmark for machine learning models.  

This project demonstrates classification using a simple fully connected neural network in PyTorch.

## Objective
Build and train a neural network using **only fully connected layers** to classify the ten classes of apparel images in Fashion-MNIST with competitive accuracy.

## Dataset
- **Training set**: 60,000 images  
- **Test set**: 10,000 images  
- **Classes**:  
  `T-shirt/top, Trouser, Pullover, Dress, Coat, Sandal, Shirt, Sneaker, Bag, Ankle boot`  
- **Image size**: 28×28 grayscale  

## Evaluation Criteria
- **Loss Function**: Negative Log-Likelihood Loss (`NLLLoss`)  
- **Performance Metric**: Accuracy  

## Solution Approach
1. Load dataset using `torchvision.datasets.FashionMNIST`  
2. Split into train (48k) / validation (12k) / test (10k)  
3. Wrap datasets in `DataLoader` with batch size 64  
4. Model architecture:  
   - Input: 784 (28×28 flattened)  
   - Hidden Layer 1: 128 units, ReLU + Dropout(0.25)  
   - Hidden Layer 2: 64 units, ReLU + Dropout(0.25)  
   - Output: 10 units, LogSoftmax activation  
5. Optimizer: Adam (lr=0.003)  
6. Trained for 25–35 epochs  
7. Achieved **~88–89% accuracy** on test set

## License
This project is licensed under the MIT License.
