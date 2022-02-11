---
title: Data can be thought of as a manifold.
author: Mustafa Khan
date: 2022-02-11
category: Jekyll
layout: post
---

A manifold is a concept from Topology.

## Topology

- The study of properties unchanged under homeomorphisms (i.e. deformations such as zooming in to a geometry). In short, topology tells you what changes and what remains unchanged.

## Uses Of Topology

- Understanding the $$ \epsilon-\delta $$ proof from Calculus requires Topology to define what we considered open (such as an interval of the form $$ (a,b) $$) or closed (such as an interval of the form $$ [a,b] $$).
    - What happens if you redefine derivatives in other systems other than $$\mathbb{R}^n$$?
- Allows you to extend and understand odd geometries.
    - Interesting problem in topology: What is the difference between $$\mathbb{R}^2$$ and  $$\mathbb{R}^3$$?
- An application in robotics with the Hartman Grobman theorem (a theorem about ODEs).
    - Consider a point in equilibria in a non-linear direction field. How do we tell if this point is a saddle point?
    - We zoom in to the non-linear direction field so that the field appears like we are in Cartesian or Euclidian space. Here we can compute the Wronskian. Stability happens to be the topological property that is unchanged.

## Practical Definition Of A Manifold

- A manifold is a curved surface or plane. It defines continuity because if you zoom in, it looks flat.
    - It is helful to consider a small ant walking on a surface (it could be curvy, have twists, or even have holes), if from the perspective of the ant, everywhere it walks looks like a flat plane, this surface is a manifold. E.g.: We live on a manifold, a sphere is the simplest example of a manifold in 3D. 
    - On the other hand, a surface with "sharp" points such as a cube is not a manifold.
- If the surface is smooth, we call this a differentiable manifold.

## Mathematical Definition Of A Manifold

- A manifold is a topological space that has these properties:
    - Hausdroff
        - This is a very abstract concept that you can draw two circles around two circles around two points that don’t intersect.
    - 2nd Countable
        - Allows the idea of distance to make sense.
    - Locally homeomorphic to $$\mathbb{R}^n$$
        - This means if you zoom in really close, a curved geometry begins to appear like $\mathbb{R}^n$. For instance, if you zoom into a donut, it looks like Euclidian space. This is important because much of mathematics is defined in $\mathbb{R}^n$.


## A Collection Of Data Is A Manifold
- What is the relationship between manifolds and datasets?
- The manifold assumption indicates that data points represent the state of an object and that these should distribute on a smooth low-dimensional manifold embedded in high-dimensional observation space. Consider the image of the duck shown below, the images of the rotating duck toy distribute on a one-dimensional manifold (a curve) embedded in high-dimensional pixel space. Each image depicts a particular state of the duck. Although the pixel values change dramatically from one image to the next, humans could easily identify that they are controlled by one key factor: the rotation of the duck.

![A Rotating Duck](https://static-01.hindawi.com/articles/mpe/volume-2021/6432929/figures/6432929.fig.001.svgz)


Other things to look into:
- Manifold Learning
- t-SNE
- Locally Linear Embeddings (LLE)


### Sources

* https://www.hindawi.com/journals/mpe/2021/6432929/
