# Baseline Needs Even More Love: A Simple Word-Embedding-Based Model for Genetic Engineering Attribution

## Introduction

This repository contains my submission for the [Genetic Engineering Attribution Challenge](https://altlabs.tech/geac/).
The goal of the challenge was to create an algorithm that identified the most likely lab-of-origin for genetically 
engineered DNA. The challenge is described in more detail [here](https://www.drivendata.org/competitions/63/genetic-engineering-attribution/page/165/),
and the competition dataset is analysed [here](https://www.drivendata.co/blog/genetic-attribution-benchmark/).
on the private test set.

Approached the challenge using natural language processing. Byte-pair encoded genetic sequences. Implemented a variant 
of SWEM-max in TensorFlow to classify the encoded sequences. SWEM-max was particularly well suited to the task given 
its strong performance on small datasets and long texts. The approach proposed in my paper was judged as "particularly 
promising" and "quite distinctive from the other submissions", and ranked [5th in the Innovation Track](https://www.drivendata.org/competitions/63/genetic-engineering-attribution/page/221/) 
(judged on the real-world merits of the model). Also ranked [21st in the Prediction Track](https://www.drivendata.org/competitions/63/genetic-engineering-attribution/leaderboard/) 
(judged on model top-10 accuracy).

## Abstract

([Shen et al., 2018](https://arxiv.org/abs/1805.09843)) first demonstrated that Simple Word-Embedding-Based Models (SWEMs)
outperform convolution neural networks (CNNs)
and recurrent neural networks (RNNs) in many
natural language processing (NLP) tasks. We apply SWEMs to the task of genetic engineering
attribution. We encode genetic sequences using
BPE as proposed by ([Alley et al., 2020](https://www.biorxiv.org/content/10.1101/2020.08.22.262576v1)), which
separates the sequence into motifs (distinct sequences of DNA). Our model uses a max-pooling
SWEM to extract a feature vector from the organism’s motifs, and a simple neural network to
extract a feature vector from the organism’s phenotypes (observed characteristics). These two
feature vectors are concatenated and then used
to predict the lab of origin. Our model achieves
90.24% top-10 accuracy on the private test set,
outperforming RNNs ([Alley et al., 2020](https://www.biorxiv.org/content/10.1101/2020.08.22.262576v1)) and
CNNs ([Nielsen & Voigt, 2018](https://www.nature.com/articles/s41467-018-05378-z)). The simplicity of
our model makes it interpretable, and we discuss
how domain experts may approach interpreting
the model.

[Read the full report here.](https://github.com/KieranLitschel/GeneticSWEM/blob/master/Report.pdf)

![alt text](https://raw.githubusercontent.com/KieranLitschel/GeneticSWEM/master/model_pipeline.PNG "Model pipeline for an example sample")

#### BibTeX

If you would like to cite this report, please cite it as:

```
@article{GeneticSWEM,
  author = {Kieran Litschel},
  title = {Baseline Needs Even More Love: A Simple Word-Embedding-Based Model for Genetic Engineering Attribution},
  URL = {https://github.com/KieranLitschel/GeneticSWEM},
  year = {2020},
}
```

## Code

### Development directory

During the competition I made a submission every time I made a significant improvement to my model. I saved the 
notebooks corresponding to each submission and have included them in this repository in the [development directory](https://github.com/KieranLitschel/GeneticSWEM/tree/master/development).
If you are curious about how the development of my model progressed through the competition take a look.

### Submission

The [Train](https://github.com/KieranLitschel/GeneticSWEM/blob/master/Train.ipynb), [Infer](https://github.com/KieranLitschel/GeneticSWEM/blob/master/Infer.ipynb), 
and [Build vectors and metadata for TensorFlow]((https://github.com/KieranLitschel/GeneticSWEM/blob/master/Build%20vectors%20and%20metadata%20for%20TensorFlow.ipynb)) 
notebooks were my final submission for the Innovation Track. The Train notebook loads and pre-processes the training data, 
and uses it to train the model. The Infer notebook loads and pre-processes the test data, and makes predictions for each
sample using the model trained in the Train notebook. The Build vectors and metadata for TensorFlow notebook is used to 
extract the word embeddings from the trained model in the format [projector.tensorflow.org](http://projector.tensorflow.org/) 
accepts as input.

Note that the execution output is not saved for any of the submitted notebooks. If you want to see the execution output, 
take a look at development notebook [GE_8_36]((https://github.com/KieranLitschel/GeneticSWEM/tree/master/development/GE_8_36.ipynb)),
as this notebook trains and evaluates the same model.

### Requirements for Running Notebooks

These notebooks were run on Ubuntu 18.04 using Python 3.6.9. A requirements.txt of the versions of packages we used is
included. You will likely have success running these notebooks with a different operating system and different version 
of Python and the required packages, but we have not tested this.

### XSWEM Package

I am currently working on an open source implementation of SWEM-max (max-pooling SWEM) in TensorFlow, with an emphasis on the 
interpretability techniques discussed in the paper. I have had some ideas of how to make the model even more explainable, 
which I plan to include in the implementation. Development is at an early stage and currently the implementation is not 
flexible enough to completely replicate the model proposed here, but I plan to improve flexibility in the future to 
support this. You can check it out [here](https://github.com/KieranLitschel/XSWEM).

## Future Plans

I have had a few ideas on how to improve my approach since the competition. I plan to explore these ideas, and then 
develop the report into a full pre-print paper.
