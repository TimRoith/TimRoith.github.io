---
permalink: /KCBO/
title: "Kernelized Consensus Based Optimization"
toc: false
layout: single
classes: wide
---


# Consensus Based Optimization

## Setting
We consider a function $V:\R^d\to\R^+_0$ for which we want to solve the global optimization problem

$$
\min_{x\in\R^d} V(x).
$$


* The function $V$ may be non-convex.
* We do not want to employ gradient-based methods.
* Instead: agent based/particle methods.

## Particle Swarm Optimization

We first consider Particle Swarm Optimization (PSO) proposed by Kennedy and Eberhart [(1995)](#1) which was motivated by bird-flocking simulations of Reynolds [(1987)](#2).

For particles $x_1,\ldots, x_N\in\R^d$ with velocities $v_i\in\R^d$ one considers the scheme

$$
\begin{align*}
x_i &\gets x_i + v_i,\\
v_i &\gets v_i + \xi_1\circ (p_i - x_i) + \xi_2 \circ (p_\text{g} - x_i).
\end{align*}
$$


Here,
* $\xi_1, \xi_2\in\R^d$ are chosen randomly,
* $p_i\in\R^d$ denotes the best position particle $i$ has seen,
* $p_\text{g}$ denotes the best the swarm has seen.

## Consensus

$$\newcommand{\mean}{\alpha}$$

The first step to derive standard CBO proposed by Pinnau [(2017)](#3) is to only consider a common point $\mean\in\Rd$.


Secondly, this point is chosen as the weighted average

$$
\mean[\rho^N] = \frac{\int y\ \exp(-\beta\ V(y)) d\rho^N(y)}{\int \exp(-\beta\ V(y)) d\rho^N(y)}
$$

where $\rho^N = \sum_{i=1}^N \delta_{x_i}$.

<img src="/assets/img/v_filed/v_field_CBO.pdf" width="500" class="align-right">

For $i=1,\ldots,N$ the dynamics then read

$$
\boxed{
\dot{x}_i = -(x_i - \mean[\rho^N]) + \sigma \abs{x_i - \mean[\rho^N]}\dot{W_i},
}
$$

where the parameter $\sigma \geq 0$ determines the influence of the noise term.

Considering the mean-field equation (formally) one obtains the dynamic

$$
\dot{x} = -(x - \mean[\rho]) + \sigma \abs{x - \mean[\rho]}\dot{W_i},\qquad \rho = \text{law}(x)
$$


\aycite{carillo_18}: the equation is well-posed.
\end{frame}

## Modifications and Details

* The parameter $\beta$ is typically updated during the iteration.
%
* Especially for higher-dimensional problems \aycite{carillo_18} proposed a noise term that is scaled component-wise.
%
* \aycite{carillo_18} also proposed a batching strategy over the particles.
%
* In some formulations the term $(x_i - \mean)$ is multiplied by a term that enforces an improvement in every step.


## References
<a id="1">[1]</a> 
Kennedy, J. and Eberhart, R. (1995). 
Particle swarm optimization
Proceedings of ICNN'95 - International Conference on Neural Networks