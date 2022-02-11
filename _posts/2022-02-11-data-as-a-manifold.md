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

- Understanding the \\ \epsilon-\delta \\ proof from Calculus requires Topology to define what we considered open (such as an interval of the form \\ (a,b) \\) or closed (such as an interval of the form \\ [a,b] \\).
    - What happens if you redefine derivatives in other systems other than $\mathbb{R}^n$?
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


## A collection of Data is a Manifold

Data can come from a variety of spaces. It can be the space of all images, or from a range of prices and numerical values. These high dimensional spaces have complex representations that cannot always be visualized. However, the data may come from a special subset that is represented by a manifold.
Thus, manifolds can act as a stepping stone from a complex space to a simpler, smoother subset.

Classification problems are prime examples for manifold learning — where we are specifically looking for manifolds that separate two types of data.

There are many approaches within manifold learning that perhaps have been seen before, such as t-SNE and Locally Linear Embeddings (LLE).
