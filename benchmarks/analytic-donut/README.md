# Analytic-Donut Benchmark

## Overview
This benchmark consists of an analytically defined PDF $\pi : \mathbb{R}^2 \rightarrow \mathbb{R}$ resembling the shape of a donut.

## Purpose
Simple test case especially useful for sampling methods.

## Run
```
docker run -it -p 4243:4243 linusseelinger/benchmark-analytic-donut
```

## Properties
Value | Dimensions
---|---
inputSizes | [2]
outputSizes | [1]

Feature | Supported
---|---
Evaluate | True
Gradient | True
ApplyJacobian | True
ApplyHessian | False

### Configuration

None

### Description

- Input: 2D coordinates $x \in \mathbb{R}^2$
- Output: PDF $\pi$ evaluated at $x$

## Model

The PDF $\pi$ is defined as

$$ \pi(x) := - \frac{(\| x \| - r)^2}{\sigma^2}, $$

where $r = 2.6$ and $\sigma^2 = 0.033$.

The implementation then returns the log PDF $\log(\pi(x))$.