---
layout: post
title: Artificial Neural Networks and Simplicial Complexes
---

## Post in construction!!!

![alt
text](https://github.com/EduPH/eduph.github.io/blob/master/images/404.jpg?raw=true)



In this post, I would like to describe a little bit our first approach
to give a constructive solution to the Universal Approximation
theorem. Those who have studied a little about Machine Learning, and
Artificial Neural Networks (ANNs)  should know about the Universal Approximation
theorem. It states, roughly speaking, that an ANN with only one hidden
layer can approximate any continuous function (with some
constraints) as closely as we desired. The traditional proofs were
based in existence arguments, i.e. these proofs state that there is
one but with no clue about how many neurons (or units) the ANN should
have in this hidden layer. 

So, let us begin with an informal introduction to this Universal
Approximation theorem and our version of it. We did not pretend to
solve it, but we restrict ourselves to a smaller version of it, and,
using simplicial complexes, we gave this constructive version of the
proof.

### Artificial Neural Networks

Artificial Neural Networks can be described as computational graphs
which are directed and have weights. These weights are usually
updated in a training process, trying to solve an optimization
problem. This optimization problem is based on a function that
measures how far is the model (i.e. the ANN) from the right
classification of a dataset. In our case, we will not use any kind of
training, but we will give, as we will explain below, the specific
values for the weights. 

As we were explaining, an ANN is a computational graph. However, the
Universal Approximation theorem traditionally restricts to the case of
one hidden layer ANNs. To visually explain it, I will borrow the
following picture from the post of [this link](https://blog.goodaudience.com/artificial-neural-networks-explained-436fcf36e75).

![alt
text](https://miro.medium.com/proxy/1*-a-flCLHLCGM0-7TOcNJnQ.png)

As we can see in the picture, there are three layers of neurons, the
first layer is an input layer, the second one is the so-called hidden
layer, and the last one is the output layer. This ANNs can be written
in a mathematical formula by ![eqn1](https://github.com/EduPH/eduph.github.io/blob/master/images/post1/eqn1.png?raw=true)

$F(x)=\sum_{i=1}^{N} v_{i} \varphi\left(w_{i}^{T} x+b_{i}\right)$




