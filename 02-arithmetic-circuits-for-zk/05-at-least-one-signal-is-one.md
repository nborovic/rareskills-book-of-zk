# At least one signal is one

## Problem

Create an arithmetic circuit that takes signals x₁, x₂, …, xₙ, constrains them to be binary, and outputs 1 if at least one of the signals is 1. Hint: this is tricker than it looks. Consider combining what you learned in the first two problems and using the NOT gate.

## Solution

$x_1^2 \equiv x_1$

$x_2^2 \equiv x_2$

$...$

$x_n^2 \equiv x_n$

$y = 1 - (1 - x_1) \cdot (1 - x_2) \cdot ... \cdot (1 - x_n)$
