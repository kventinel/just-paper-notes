# How Does Batch Normalization Help Optimization?

Article: https://arxiv.org/pdf/1805.11604.pdf

# Problem

Why Batch Norm so good


# Ideas

1. It's good not because ICS (internal covariate shift). It's means, there is
not significant difference between distribution of input with and witout BN
2. Loss and gradient landscapes more smooth
3. Lipschitz constant for loss better with BN

# Questions

1. There is no mention about augmentation part of BN
(each sample on each epoch enter in batch with different other samples)
