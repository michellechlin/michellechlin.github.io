---
title: A Journey Into Deep Learning - Day 2
header:
  teaser: "https://farm5.staticflickr.com/4076/4940499208_b79b77fb0a_z.jpg"
excerpt_separator: "<!--more-->"
categories:
  - Data Science
tags:
  - Udemy
  - Python
  - TensorFlow
---

## NLP for Text Generation with RNNs

### What is the NLP?

Natural Language Processing (NLP) extract useful information from the given text or sentence using machine learning and deep learning techniques. The techniques requires text being converted to a set of real number (a vector).

  >The process of converting text into numbers are called Vectorization.

Great summary in [Prabhu's blog](https://towardsdatascience.com/understanding-nlp-word-embeddings-text-vectorization-1a23744f7223).

----------------------

### How do we do to generate the useful text?

The course demonstrates how to use a [recurrent neural network (RNN)](https://en.wikipedia.org/wiki/Recurrent_neural_network) to generate text. Process could be done character by character.
Details in [Andrej Karpathy blog](http://karpathy.github.io/2015/05/21/rnn-effectiveness/)

### Step 0 - Importing main libraries
Libraries are always required:
```
import numpy as np
import pandas as pd
import matplotlib.pyplot as plt
import tensorflow as tf
```

### Step 1 - import text & understand the characters
Free text is available [here](https://www.gutenberg.org/)

Importing text:
```
path_to_file = 'FILENAME.txt'
text = open(path_to_file, 'r').read()
print(text[:1000])
```
Understanding the characters:
```
vocab = sorted(set(text))
print(vocab)
len(vocab)
```
`set()` where parameters could be list, tuple or dictionary

### Step 2 - text processing

As a neural network can't work with string data, the process of converting text into number is required. So, this section need to create dictionaries that can go from numeric index to character and character to numeric index.

```
char_to_ind = {char:ind for ind, char in enumerate(vocab)}
char_to_ind['H']
#33

ind_to_char = np.array(vocab)
ind_to_char[33]
#'H'
```
Note: `enumerate` is a built-in function of Python, which allows us to loop over something and have an automatic counter.

Create Mapping so we can go back and forth from char to num:
```
# encode text into text.array
encoded_text = np.array[char_to_ind[c] for c in text]
# Get the text
sample = text[:20]
# Parallel num for the text
encoded_text[:20]
```

### Step 3 - create batches
