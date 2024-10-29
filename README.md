# Abstract
The curse of dimensionality refers to the challenges introduced when analyzing, processing, visualizing, and storing
high dimensional data. Dimension reduction was introduced to transform such data, lying on a high-dimensional
surface or manifold, to a low-dimensional representation of the data - which retains the important properties of the
original data, ideally close to its intrinsic dimension. There are many dimension reduction methods, including (linear
and non-linear) principal component analysis, autoencoders and self-organizing maps, all of which are applied in this
assignment. These methods often perform well on some data types, but poorly on others. The goal of this assignment
is to apply these dimension reduction methods to different kinds of data to determine which methods and parameters
work best on different datasets. The KNN algorithm is used to evaluate performance on each dimension reduction
method, tested before and after dimension reduction is applied. As a result, I find that a KNN trained on SOM
reduced WDBC data had the smallest difference in accuracy (0.005) relative to the original model. In addition, I find
that a KNN trained on autoencoder reduced CG data had the smallest absolute difference in accuracy (0.001) relative
to the original model.

# Introduction
Richard E. Bellman, an American mathematician, described the “curse of dimensionality” as the increase in volume
associated with adding extra dimensions to a Euclidean space, Karanam (2021) . Although an increasing number of
dimensions can theoretically introduce more information to the data, practically, this may also introduce more noise
and redundancy during analysis, in addition to an increase in processing requirements.
We also see that as the number of dimensions increase, the machine learning algorithm requires exponentially more 
observations to achieve good performance. However, once the optimal number of dimensions have been reached, the
model performance begins to deteriorate, Built In (2022) .
Principal Component Analysis (PCA), Self-Organizing Maps (SOM) and Autoencoders are dimension reduction techniques
which will be implemented in this assignment.
PCA is a linear dimension reduction method that aims to reduce the dimensionality of a dataset by preserving as
much of the original variance in the dataset as possible, Wikipedia (2023b) . Non-linear (or Kernel) PCA on the other
hand, is an extension of linear PCA, which allows separation of non-linear data by using Kernel functions Tanner
(2022) .
A SOM is a type of artificial neural network used for clustering and visualizing high-dimensional data, GeeksforGeeks
(2020) . The SOM learns a low-dimensional, discretized representation of the input data while preserving the topological
properties of it, Wikipedia (2023c) .
Autoencoders are neural networks that learn two functions, and have two important components: (1) an encoder
which reconstructs the original data to a compressed representation and (2) a decoder that recreates the original data
from its encoded representation, Wikipedia (2023a) .
The goal of this assignment is to determine the best dimension reduction method for different kinds of data. In this
analysis, we assess two datasets, namely: (1) a sample of not MNIST images containing the letters C and G, and (2)
the Wisconsin Diagnostic Breast Cancer dataset.
I will apply the K-nearest neighbors (KNN) algorithm to the data, once before and after applying the dimension
reduction method. The performance of each reduction method is then assessed by calculating the change in KNN
accuracy pre- and post-dimension reduction.
