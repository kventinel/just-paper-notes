# The State of Sparsity in Deep Neural Networks

Article: https://arxiv.org/abs/1902.09574

Code: https://github.com/google-research/google-research/tree/master/state_of_sparsity

## Problem:

Compare different techniques for inducing sparsity in deep neural networks

## Methods:

### Random Pruning:

Zeroing some random weights of network on each N steps.

### Magnitude Pruning:

Allow gradient updates to masked weights, make use of a gradual sparcification shedule with sorting-based weight thresholding. https://arxiv.org/abs/1710.01878

### Variational Dropaut

Simply use variational dropout from https://arxiv.org/abs/1701.05369 paper.

### ![equation](http://www.sciweavers.org/tex2img.php?eq=l%5F0&bc=White&fc=Black&im=jpg&fs=12&ff=arev&edit=) regularization

Simply use ![equation](http://www.sciweavers.org/tex2img.php?eq=l%5F0&bc=White&fc=Black&im=jpg&fs=12&ff=arev&edit=) regularization from https://arxiv.org/abs/1712.01312 paper.

### Lottery tickets

Try train network, than prune it, and than retrain network with same weigths at initialization.

### Scratch

Try train netwrok, than prunt it, and than retrain netwrok with new random weights at initialization.

## Experiments:

1. Transformer for translation from english to german.
2. ResNet-50 on ImageNet.

## Results:

1. Demonstrated that complex techniques shown to yield state-of-the-art compression on small datasets perform inconsistently, and that simple heuristics can achieve comparable or better results.
2. Provide strong counterexamples to two recently proposed theories that models learned through pruning techniques can be trained from scratch to the same test set performance of a model learned with sparsification as part of the optimization process.
3. Surprisingly, authors were unable to produce sparse ResNet-50 models with ![equation](http://www.sciweavers.org/tex2img.php?eq=l%5F0&bc=White&fc=Black&im=jpg&fs=12&ff=arev&edit=) regularization that did not significantly damage model quality.
