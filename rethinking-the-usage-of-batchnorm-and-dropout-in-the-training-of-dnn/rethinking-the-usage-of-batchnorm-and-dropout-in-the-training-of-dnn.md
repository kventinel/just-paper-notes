# Rethinking the Usage of Batch Normalization and Dropout in the Training of Deep Neural Networks

Article: https://arxiv.org/abs/1905.05928

## Problem:

Decorrelation features in neural networks

## IC (Independent Components) Layer

Simple layer from batchnorm + dropout used for decorelate features.
In paper proved theorem, that claims, that Shannon entropy decreased linearly by dropout coef and mutual information decreased quadratically by p.
Also showed, that correlation coef decreased linearly by p, such as expected activation.
Also proved, that BatchNorm should be placed after activation function.

## Residual connection options:

1. RELU-IC-CONV
2. IC-CONV-RELU
3. CONV-RELU-IC

## Datasets:

1. CIFAR 10/100
2. ImageNet (2012)

## Expetimens:

1. ResNet baseline architecture with BatchNorm layers
2. 3-types of residual connection options

Baseline for ImageNet used from "Understanding the Disharmony between Dropout and Batch Normalization by Variance Shift", where showed, that Dropout and BatchNorm work bad together.

## Results:

1. more stable training process
2. faster convergence speed
3. better convergence limit
