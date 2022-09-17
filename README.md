# Physics Informed Neural Networks (PINNs)

---

## What are PINNs?

A physics informed neural network refer to a supervised learning algorithm that makes use of data and knowledge from governing equations in order to approximate solutions to ODEs (Ordinary Differential Equations) and PDEs (Partial Differential Equations). (Raissi et al., 2019)

PINNs work by exploiting 2 fundamental properties of neural networks:

- The universal approximation theorem
- Automatic differentiation

which allows us to embed properties of differential equations in to the PINN, such that training the neural network will result in an approximation of the underlying differential equation. (Dagrada, 2022)

## Overview of this repository

This repository contains implementations of physics informed neural networks, to solve various relatively simple differential equations, currently this implementation only supports ODEs and **Not** PDEs

- The 'Results' directory contains output of solutions produced by the PINN and comparisons to either an analytic solution or solutions using an ODE solver
- 'Saved_Models' directory contains pretrained models from the implementation (In Pytorch saved model format) refer to source code in the respective jupyter notebook for the model architecture and training code

## Requirements

- Pytorch
- Numpy
- Scipy (ODE solver)
- Matplotlib

### Future plans and experiments

- Approximate PDEs using PINNs (Probably something simple like Heat equation)
- Investigate impact of noisy measurements (Overhead of adding a denoise model) [DONE]
- Try to approximate Systems of ODEs (Using jacobian for derivatives) [Tests were unsucessful]
- Test existing implementations and build an API to interact with the neural network [TODO]

_These plans are not in any particular order._

## References

- Ben Moseley. 2021. So, what is a physics-informed neural network? - Ben Moseley. So, what is a physics-informed neural network? https://benmoseley.blog/my-research/so-what-is-a-physics-informed-neural-network/ Date of access: 29 Jul. 2022.

- Dagrada, M. 2022. Introduction to Physics-informed Neural Networks. Medium. https://towardsdatascience.com/solving-differential-equations-with-neural-networks-afdcf7b8bcc4 Date of access: 29 Jul. 2022.

- Raissi, M., Perdikaris, P. & Karniadakis, G.E. 2019. Physics-informed neural networks: A deep learning framework for solving forward and inverse problems involving nonlinear partial differential equations. Journal of Computational Physics. 378:686–707.
