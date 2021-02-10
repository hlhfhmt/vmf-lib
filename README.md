# Python/PyTorch Implementation of von Mises-Fisher and Its Mixture

The von Mises-Fisher (vMF) is a well-known density model for directional random variables. The recent surge of the deep embedding methodologies for high-dimensional structured data such as images or texts, aimed at extracting salient directional information, can make the vMF model even more popular. In this article, we will review the vMF model and its mixture, provide detailed recipes of how to train the models, focusing on the  maximum likelihood estimators, in Python/PyTorch. In particular, implementation of vMF typically suffers from the notorious numerical issue of the Bessel function evaluation in the density normalizer, especially when the dimensionality is high, and we address the issue using the MPMath library that supports arbitrary precision. For the mixture learning, we provide both  minibatch-based large-scale SGD learning, as well as the EM algorithm which is a full batch estimator. For each estimator/methodology, we test our implementation on some synthetic data, while we also demonstrate the use case in a more realistic scenario of image clustering. The technical report for the details can be found in https://arXiv...

---


## Features

* vMF density estimation via near-closed-form Maximum Likelihood Estimator (MLE) or Stochastic Gradient Descent (SGD)
* Estimation of mixture of vMFs via Expectation-Maximization (EM) or SGD
* Numerically stable estimation of the vMF normalizer through [mpmath](https://mpmath.org/)'s Bessel function estimation
* Examples of image clustering application


## Requirements

* Python 3.7
* PyTorch >= 1.4.0
* NumPy >= 1.18.1
* [mpmath](https://mpmath.org/) >= 1.1.0
* scikit-learn >= 0.23.2 (Required for metric computation in image clustering)


<p align="center">
  <img align="middle" src="./figs/thumbnail.png"/>
</p>
