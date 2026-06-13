# The Deep Learning Archive
[Read in English](README.md) | [Leer en Español](es/README.md)

> Rigorous theoretical explorations into the core of Deep Learning architectures, broken down step by step.

---

## Introduction

Have you ever wondered why, when building a neural network, we can't simply initialize all weights to 1, or 0, or even giant random values as a starting point? After all, they’ll eventually tune themselves through training, right?

If you've spent any time with Deep Learning, you’ve likely heard about the "Vanishing Gradient" or "Exploding Gradient" problems. These phenomena cause your network to "die" prematurely: gradients vanish or neurons saturate, leaving the model unable to learn even the simplest patterns.

This space is more than just a collection of theoretical summaries; it is an archive of derivations from scratch. My goal is to walk you through deep logical, mathematical, and statistical reasoning behind the breakthroughs of Deep Learning. We will not accept any formula as "given by divine intervention", we will build every single one of them using the fundamental tools of mathematics.

---

## Published Articles

### Deep Learning Foundations
1.  **Why Neural Networks Die: The Math Behind the Vanishing Gradient Problem:**
  An in-depth analysis of data flow through a Multi-Layer Perceptron (MLP). This article opens the black box of multivariable calculus and the total chain rule during the backward pass to demonstrate mathematically the exact origin where gradients collapse.
  * [Read Article (EN)](https://bastianru.github.io/deep-learning-archive/en/why-nn-die/P1)
  * [Leer Artículo (ES)](https://bastianru.github.io/deep-learning-archive/es/why-nn-die/P1)

2.  **The Math Behind Xavier Initialization (Coming Soon):** A continuation directly from the first text,
  building upon the gradient degradation problem, we will mathematically derive the exact variance scaling factors proposed by Xavier Glorot and Yoshua Bengio in 2010 to keep signals alive across deep architectures.

---


## Is this for you? (Prerequisites)

These articles are designed to be as accessible as possible. However, to follow the thread of the proofs without getting lost, you should have the following prior knowledge:

**For forward pass and statistical analysis:**
- **MLP Architecture:** Understanding neurons, layers, and their connections (the fundamental dot product $z = Wx + b$).
- **Descriptive Statistics:** Feeling comfortable with the concepts of Mean ($\mu$) and Variance ($\sigma^2$) / Standard Deviation.
- **Basic Algebra:** Solving equations, powers, and square roots.

**For backward pass and optimization analysis:**
- **Differential Calculus:** Understanding what a derivative represents.
- **Partial Derivatives:** Understanding how to derive with respect to one variable while keeping others constant.
- **Basic Backpropagation:** A conceptual notion of how error flows backward through a network.

If you meet these requirements, we will build the rest here. Every advanced statistical property or mathematical trick will be formally defined right before we need it for the next step of the proof.