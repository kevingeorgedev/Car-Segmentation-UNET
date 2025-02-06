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

pip install requirements.txt
```

## Usage
After installing the repository and setting up your environment, you can use the model to perform image segmentation.

## Evaluation
To evaluate the model I used the dice score metric. After 10 epochs, the model had a dice score of $0.87$ and an accuracy of $94.61$%. If trained for longer, the model should perform better considering these tests were performed after only training for 10 epochs.

## Results

| Metric     | Value  |
|------------|--------|
| IoU        | ~0.627 |
| Dice Score | ~0.876 |
| Accuracy   | ~94.7% |