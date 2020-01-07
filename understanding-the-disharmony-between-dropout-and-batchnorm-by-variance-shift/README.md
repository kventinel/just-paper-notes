# Understanding the Disharmony between Dropout and Batch Nromalization by Variance Shift

Article: https://arxiv.org/abs/1801.05134

Code: https://github.com/bearpaw/pytorch-classification

## Problem

Bad results, when dropout and batchnorm used together.

## Work

Think about 2 cases in dropout:

1. Dropout -> BatchNorm
2. Dropout -> Weights -> BatchNorm

In first case variance not equal on training and test step, except case, when keep prob of dropout layer equal to 1.
In second case variance not equal on training and test step, except 2 cases:

1. Keep prob in dropout equal to 1.
2. Neurons count large (lim to infty)

Use as example of second case work Wide ResNet.

## Results

Dropout shoud be placed after all BatchNorm layers.
Or use some new formula for fix not equal variance on train and test step.
Or using adjustment for batchnorm layers: train data pass to network in eval mode in dropout layers for get right moving mean and variance variables.
