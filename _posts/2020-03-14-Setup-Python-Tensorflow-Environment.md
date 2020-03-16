---
title: A Journey Into Deep Learning - Week 1
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

As I am thinking of self-learning Machine Learning (ML), I want to quickly pick up the skills and foundation of Python. *(I used more with R, Matlab during my PhD work)*. So, since last year when I was at 9-month pregnancy, I've completed [Python for Data Science and ML Bootcamp](https://www.udemy.com/course/python-for-data-science-and-machine-learning-bootcamp/), instructed by Jose Portilla. Today, I have some sorts of feeling that I know what I was doing as a mom (~ 6 months after giving birth). Then, I grab and read a book *The Algebra of Happiness*, make a coffee, and open my MacBook - thinking, I'd like to continue to learn more about ML as I have been always fascinated with data. In between my baby sleep-wake cycle, I read and code and write down what I did, even just a little bit.

On Saturday March 14, the world is fighting with coronavirus and my world is thrilling that I start the journey of learning new things, from this course [Tensorflow 2 and Keras Deep Learning Bootcamp](https://www.udemy.com/course/complete-tensorflow-2-and-keras-deep-learning-bootcamp/).

Hopefully, I can start making fun project soon through applying what I've learned every single time I have when my baby fall asleep and/or take a nap. Here I make notes of every steps and accomplishment, **even just a little bit**.

> Don't hate machine learning for being simple. Levers are simple too, but they can move the world.
> -Cassie Kozyrkov


## Day-1 (3/14): TensorFlow Setup and Install

**Here are the notes for myself:**

* Downland Python 3.7 Version from [Anaconda](https://www.anaconda.com/distribution/) for MacOS
* Create a folder, named "TensorFlow" under Desktop/Gitproject/
* Downland the class materials into the created folder

**What I should do next time for STARTING the course:**

* Locate the path in terminal with this code `% cd Desktop/Gitproject/TensorFlow`
* Open terminal and type `% conda activate mytfenv`for setup TensorFlow Environment
* Get into virtual env using `% jupyter notebook`

## Day-2 (3/15): NLP for Text Generation with RNNs

### What is the NLP?

Natural Language Processing (NLP) extract useful information from the given text or sentence using machine learning and deep learning techniques. The techniques requires text being converted to a set of real number (a vector).

  >The process of converting words into numbers are called Vectorization.

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
* Free text is available [here](https://www.gutenberg.org/)

* Importing text:
```
path_to_file = 'FILENAME.txt'
text = open(path_to_file, 'r').read()
print(text[:1000])
```
* Understanding the characters:
```
vocab = sorted(set(text))
print(vocab)
len(vocab)
```
`set()` where parameters could be list, tuple or dictionary

### Step 2 -
