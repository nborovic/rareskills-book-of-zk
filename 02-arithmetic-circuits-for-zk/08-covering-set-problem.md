# Covering set problem

## Problem

The covering set problem starts with a set $S = \{1,2,...,10\}$ and several well-defined subsets of $S$, for example: $\{1,2,3\},\{3,5,7,9\},\{8,10\},\{5,6,7,8\},\{2,4,6,8\}$, and asks if we can take at most  subsets of  such that their union is $S$. In the example problem above, the answer for $k = 4$ is true because we can use $\{1,2,3\},\{3,5,7,9\},\{8,10\},\{2,4,6,8\}$. Note that for each problems, the subsets we can work with are determined at the beginning. We cannot construct the subsets ourselves. If we had been given the subsets $\{1,2,3\},\{4,5\},\{7,8,9,10\}$ then there would be no solution because the number $6$ is not in the subsets.

On the other hand, if we had been given $S = \{1,2,3,4,5\}$ and the subsets $\{1\},\{1,2\},\{3,4\},\{1,4,5\}$ and asked can it be covered with $k = 2$ subsets, then there would be no solution. However, if $k = 3$ then a valid solution would be $\{1,2\},\{3,4\},\{1,4,5\}$.

Our goal is to prove for a given set $S$ and a defined list of subsets of $S$, if we can pick a set of subsets such that their union is $S$. Specifically, the question is if we can do it with $k$ or fewer subsets. We wish to prove we know which $k$ (or fewer) subsets to use by encoding the problem as an arithmetic circuit.

## Example

$S = \{1,2,...,10\}$

$Subsets:$
$\{1,2,3\},\{3,5,7,9\},\{8,10\},\{5,6,7,8\},\{2,4,6,8\}$

$k = 4$

## Solution

$s_1^2 \equiv s_1$

$s_2^2 \equiv s_2$

$...$

$s_5^2 \equiv s_5$

----

$0 \equiv (1 - s_1)$

$0 \equiv (1 - s_1) \cdot (1 - s_5)$

$0 \equiv (1 - s_1) \cdot (1 - s_2)$

$0 \equiv (1 - s_5)$

$0 \equiv (1 - s_2) \cdot (1 - s_4)$

$0 \equiv (1 - s_4) \cdot (1 - s_5)$

$0 \equiv (1 - s_2) \cdot (1 - s_4)$

$0 \equiv (1 - s_3) \cdot (1 - s_4) \cdot (1 - s_5)$

$0 \equiv (1 - s_2)$

$0 \equiv (1 - s_3)$

----

$2^{n-1} + (k - (s_1 + s_2 + s_3 + s_4 + s_5)) \equiv 2^{n-1}c_{n-1} + 2^{n-2}c_{n-2} + ... 2^0c_0$

$c_0^2 \equiv c_0$

$c_1^2 \equiv c_1$

$...$

$c_{n-1} \equiv 1$