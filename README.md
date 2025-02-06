# U-Net Architecture for Image Segmentation

This project implements the U-Net architecture for **image segmentation**. The U-Net model is designed to work with segmentation tasks but can be applied to any image segmentation problem. This implementation is built using **PyTorch** with data from [Kaggle](https://www.kaggle.com/competitions/carvana-image-masking-challenge/overview).

## Table of Contents
- [Introduction](#introduction)
- [Features](#features)
- [Requirements](#requirements)
- [Installation](#installation)
- [Usage](#usage)
- [Evaluation](#evaluation)
- [Results](#results)

## Introduction
The U-Net architecture is a type of convolutional neural network (CNN) used for semantic segmentation. It has an encoder-decoder structure with skip connections to help preserve spatial information. This repository provides a PyTorch implementation of U-Net for image segmentation tasks.

## Features
- **Encoder-Decoder Architecture**: U-Net consists of a contracting path (encoder) and an expansive path (decoder).
- **Skip Connections**: Skip connections between the encoder and decoder help the model retain spatial information.
- **Data Augmentation**: Built-in data augmentation for better generalization.

## Requirements
- kaggle==1.6.17
- matplotlib==3.10.0
- torchaudio==2.6.0+cu118
- torchvision==0.21.0+cu118
- Other dependencies (see `requirements.txt`)

## Installation
Clone this repository and install requirements
```bash
git clone https://github.com/yourusername/unet-image-segmentation.git
cd unet-image-segmentation

pip install -r requirements.txt
```
In addition to requirements.txt, you must install PyTorch from their [website](https://pytorch.org/get-started/locally/).

## Usage
After installing the repository and setting up your environment, you can use the model to perform image segmentation.

## Evaluation
To evaluate the model I took the dice score, intersection over union score, and accuracy of the model. The metric tests are shown under [Results](#results) and were taken after 3 epochs.

## Results

Side by side of a test image vs. its predicted mask:

![alt text](image_vs_pred.png "Image vs Predicted Mask")

Mask applied over a test image:

![alt text](AppliedMask.png "Applied Mask")

| Metric     | Value  |
|------------|--------|
| IoU        | ~0.975 |
| Dice Score | ~0.987 |
| Accuracy   | ~99.5% |