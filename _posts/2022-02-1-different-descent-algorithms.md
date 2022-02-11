---
title: What is the difference between batch gradient descent, stochastic gradient descent and mini-batch gradient descent?
author: Mustafa Khan
date: 2022-02-1
category: Jekyll
layout: post
---

In all 3 cases, gradient descent is the algorithm used to update a model's weights. However, there are differences in how batches are made and how the update step is computed. Summary:

* Batch Gradient Descent.
  * Batch Size = Size of Training Set
  * Average of all training examples's gradients used to update model parameters per epoch
* Stochastic Gradient Descent.
  * Batch Size = 1
  * One training example's gradient used to update model parameters per epoch
* Mini-Batch Gradient Descent.
  * 1 < Batch Size < Size of Training Set
  * Average of mini-batch's gradients used to update model parameters per epoch

A more detailed explanation can be found below.

Gradient Descent
Gradient descent in ML seeks to find the minimum of a loss function. To achieve this goal, it performs two steps iteratively:

Computing the slope (gradient) of the loss function at the current point.
Move-in the direction of steepest descent by the computed amount.
In ML, we use gradient descent to update the weights of our model. However, there are different ways in which the weights can go down.

## Batch Gradient Descent
In Batch Gradient Descent, all the training data is taken into consideration when taking a step. The average of the gradients of all training examples is calculated. This mean gradient is then used to update the model's parameters. This results in just 1 step of gradient descent in 1 epoch.

Batch Gradient Descent is great for convex or relatively smooth error manifolds. In this case, we move somewhat directly towards an optimum solution. In these cases, the graph of loss vs epochs graph is also quite smooth because we are averaging over all the gradients of training data for a single step. The loss keeps on decreasing over the epochs.

## Stochastic Gradient Descent (SGD)
In Batch Gradient Descent we were considering all the examples for every step of Gradient Descent. But what if our dataset is huge, the program would have to calculate the gradients of all examples each epoch. This does not seem efficient. So in SGD, we consider just 1 example at a time in order to take a single step in 1 epoch:

1. Take one training image
2. Feed it into the network
3. Calculate it’s gradient
4. Use the calculated gradient to update the weights.
5. Repeat for all the training data.
6. Since we are considering just one example at a time the loss will fluctuate over the training examples and it will not necessarily decrease. But in the long run, you will see the loss decreasing with fluctuations.

Also because the loss is fluctuating, it will never reach the minima but will keep dancing around it.

SGD can be used for larger datasets. It converges faster when the dataset is large as it causes updates to the parameters more frequently.

## Mini Batch Gradient Descent
In SGD we use only one example at a time, so we cannot implement a vectorized implementation on it. We use a batch of a fixed number of training examples which is less than the actual dataset and call it a mini-batch. Doing so helps us achieve the benefits of BGD and SGD. After creating a mini-batch of a fixed size, this is what is done in one epoch:

1. Pick a mini-batch
2. Feed it into the network
3. Calculate the mean gradient of the mini-batch
4. Use the calculated mean gradient to update the weights
5. Repeat for all the other mini-batches
6. Just like SGD, the average cost over the epochs in mini-batch gradient descent fluctuates because we are averaging a small number of examples at a time. However, since we're using min-batches we can use a vectorized implementation for faster computations.

## Sources

https://arxiv.org/pdf/1606.04838.pdf
https://stats.stackexchange.com/questions/49528/batch-gradient-descent-versus-stochastic-gradient-descent
https://towardsdatascience.com/batch-mini-batch-stochastic-gradient-descent-7a62ecba642a
https://www.geeksforgeeks.org/difference-between-batch-gradient-descent-and-stochastic-gradient-descent/
