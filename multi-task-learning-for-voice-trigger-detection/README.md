# MULTI-TASK LEARNING FOR VOICE TRIGGER DETECTION

Article: https://arxiv.org/pdf/2001.09519.pdf

# Problem

Train spotter with large phonemes dataset and small dataset for activation word.
From this we optimize wrong criterion, if train on large dataset with phonemes
without activation word. And we have overfitting, when train model on small
dataset.

# Ideas

1. Use multi-task loss
2. Train one head as ASR with CTC
3. Train other head as Spotter with 2 outputs (keyword and blank) with CTC loss.
