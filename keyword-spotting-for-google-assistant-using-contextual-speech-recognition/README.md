# Keyword Spotting for Google Assistant Using Contextual Speech Recognition

Article: https://storage.googleapis.com/pub-tools-public-publication-data/pdf/be2559f953dce47e69f4d06692df1184719c4d4b.pdf

## Problem:

Improve keyword detection task using online-validation on server

## Idea:

Use speech recognition on server for this (also it improve WER for speech recognition).
ASR in this article recognize all phrase (including key-word).

### How update ASR?

1. Retrain LM (because initial LM) doesn't train recognize activation phrase (because it not enter in queries for ASR)
2. Update EoU, because peoples may make pauses between keyword and query

### Why is it improve keyword spotting?

1. Larger model, that run on server and train on more complex task

### Why is it improve recignition?

1. No problem with clipping part of query after keyword
2. No problem with early cutoff between keyword and query
3. More context for ASR. That's may help with coctail party problem.
