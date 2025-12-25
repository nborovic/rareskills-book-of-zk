# Bipartite graph

## Problem

A bipartite graph is a graph that can be colored with two colors such that no two neighboring nodes share the same color. Devise an arithmetic circuit scheme to show you have a valid witness of a 2-coloring of a graph. Hint: the scheme in this tutorial needs to be adjusted before it will work with a 2-coloring.

## Example

$L = {v_1, v_3, v_5}$
$R = {v_2, v_4, v_6}$

$Edges:$
$(v_1, v_2), (v_1, v_4),$
$(v_3, v_2), (v_3, v_6),$
$(v_5, v_4), (v_5, v_6)$

## Solution

$0 \equiv (x_1 - 1) \cdot (x_1 - 2)$

$0 \equiv (x_2 - 1) \cdot (x_2 - 2)$

$0 \equiv (x_3 - 1) \cdot (x_3 - 2)$

$0 \equiv (x_4 - 1) \cdot (x_4 - 2)$

$0 \equiv (x_5 - 1) \cdot (x_5 - 2)$

$0 \equiv (x_6 - 1) \cdot (x_6 - 2)$

$0 \equiv (x_1x_2 - 2)$

$0 \equiv (x_1x_4 - 2)$

$0 \equiv (x_3x_2 - 2)$

$0 \equiv (x_3x_6 - 2)$

$0 \equiv (x_5x_4 - 2)$

$0 \equiv (x_5x_6 - 2)$

