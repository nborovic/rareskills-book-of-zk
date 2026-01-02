# Signal v is power of two

## Problem

Create an arithmetic circuit to determine if a signal v is a power of two (1, 2, 4, 8, etc). Hint: create an arithmetic circuit that constrains another set of signals to encode the binary representation of v, then place additional restrictions on those signals.

## Solution

$x_0^2 \equiv x_0$

$x_1^2 \equiv x_1$

$...$

$x_{n - 1}^2 \equiv x_{n - 1}$

$v \equiv 2^{n - 1}x_{n - 1} + 2^{n - 2}x_{n - 2} + ... + 2^0x_0$

$1 \equiv x_{n - 1} + x_{n - 2} + x_{n - 3} + ... + x_0$