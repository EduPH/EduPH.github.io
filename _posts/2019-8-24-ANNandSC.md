---
layout: post
title: Artificial Neural Networks and Simplicial Complexes
---

This post is under construction, so you are reading a preliminary
version...

![alt
text](https://github.com/EduPH/eduph.github.io/blob/master/images/404.jpg?raw=true)



In this post, I would like to describe a little bit our first approach
to give a constructive solution to the Universal Approximation
theorem. This approach is developed in a formal tase in the following
preprint: ["Two-hidden-layer Feedforward Neural Networks are Universal Approximators: A Constructive Approach"](https://arxiv.org/pdf/1907.11457.pdf). Those who have studied a little about Machine Learning, and
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
in a mathematical formula by $$F(x)=\sum_{i=1}^{N} v_{i}
\varphi\left(w_{i}^{T} x+b_{i}\right)$$ where $$\varphi$$ is an
activation function, $$b_i$$ is the bias term, and $$w_i$$ are the
weights. The Universal Approximation theorem claims that any
continuous function from a compact to $$\mathbb{R}$$ can be
approximated by one of these ANNs with just one hidden layer. However,
as mentioned above, there is no clue about how many neurons must
compose the hidden layer. 

In our case, we will get a more difficult ANN architecture. We will
use two hidden layers that will have a very specific commitment. The
idea is very simple: having a triangulation of a given space, we will
obtain its barycentric coordinates with the first hidden layer. Then,
in the second hidden layer, we will approximate the continuous
function by a simplicial approximation (whatever it is, we will
explain below). Then, we recover the cartesian coordinates. In
our case, we can approximate any continuous function from a space
$$X$$ to a space $$Y$$. However, it is important for us that both
spaces are triangulable. Besides, sometimes is not easy to get such a
triangulation.

### Simplicial Complexes

Simplicial complexes will be our main structure. If we want to approximate a continuous
function from a given space $$X\subset \mathbb{R}^n$$ to $$Y\subset \mathbb{R}^m$$, we
need a more simple representation of $$X$$ and $$Y$$. So, if $$X$$ and $$Y$$ are triangulable,
and we know that triangulation, we can build a continuous function that **approximates**
the original continuous function.

> A simplicial complex $$K$$ is (roughly speaking) a data structure that is built by gluing
small pieces called simplices: $$0$$-simplices are points, $$1$$-simplices are edges, $$2$$-simplices
are triangles, $$3$$-simplices are tetrahedrons, and so on. This data structure is widely used to
represent topological spaces. However, not all spaces are triangulable.

<side>"Computational Topology: An introduction" is a great book to consult about simplicial complexes and simplicial approximations, among other topics in computational topology.</side>

Let us assume that we have two triangulable spaces $$X$$ and $$Y$$, and a continuous function $$g:X\rightarrow Y$$. 
Then, we could obtain two simplicial complexes $$K$$ and $$L$$ from $$X$$ and $$Y$$, respectively. The question now is, 
how can we define a function between these two simplicial complexes?








