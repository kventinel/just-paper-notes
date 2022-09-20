# LATENCY CONTROL FOR KEYWORD SPOTTING

Link https://arxiv.org/abs/2206.07261

## Problem

In this paper authors try to balance between accuracy and latency of keyword
spotting model, because when you try to train model with max pool loss, that
pretty best solution at our time, than model may have pretty bad latency.

## Solution in paper

Try to think about new loss, when for positive labels we have not
`l = pred[argmax_i pred[i]]` but `l = pred[(argmax_i pred[i]) - b]`, so in
this case we can tune latency by different values of `b`.

## Question for this paper

In my own study max pool only -- it's not the best choice. Better solution is
make combine loss with 2 parts:
- xent loss by frames
- max pool loss by utterance

Is this case we have predictable latency because of xent part of loss, and
also we have better accuracy.
