# NLP-ETHZ
This repository contains the practical part of the 4 assignments I completed for the Natural Language Processing course at ETHZ in the Fall Semester 2023.

## Assignment 1 - Backpropagation

For this task, I implemented _backpropagation_ from scratch for simple mathematical operations and their compositions.

## Assignment 2 - Conditional Random Fields for Part-Of-Speech tagging

This assignment implements a _Neural Conditional Random Field_ for the modeling of tag-tag dependencies and word-tag influence on the English language version of the Universal Dependencies dataset. This task is an exploration of the _backward algorithm_ and its variants. Therefore, I succesfully implemented the backward algorithm, the forward algorithm, the Viterbi algorithm, Dijkstra's algorithm and utilized the backward algorithm to compute the entropy as a regularization term by lifting the CRF into the expectation semiring.

## Assignment 3 - WFST

For this task, I explored the implementation of a _Finite-State Transducer_ using the library ``rayuela''. Firstly, I looked at the encoding of an input string using an FST, then I implemented a method to construct an _edit-distance transducer_, which has _insertion, deletion and substitution_ transitions for string processing. Then, I implemented the _transducer composition_ method. Lastly, I implemented and utilized _Lehmann's algorithm_ to compute the normalizer of a transducer, the log-likelihood of target strings, and the weight of the most probable target string.

## Assignment 5 - Graph-Based Neural Dependency Parser

Using _BERT_ as a contextual word embedder, this task implements a neural network which finds the _maximum (scoring) spanning tree_ to model the dependencies between words in a sentence. I first tackled the problem of extracting the word embeddings using BERT tokens, followed by the implementation of a _Biaffine Parser_ using _feedforward networks_ to compute the scores of the head and dependent representations using their embeddings. Then, I implemented two theorems for computing the partition function for directed graphs, and finally computed the MST, its score and its probability, to then bring it all together in a training function. The resulting model is trained on individual sentences and is able to capture the dependencies with the root node and to output the MSE with an 84% accuracy.
