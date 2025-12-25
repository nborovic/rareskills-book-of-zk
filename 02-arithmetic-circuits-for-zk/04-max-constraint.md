# Max constraint

## Problem

Create an arithmetic circuit that constrains k to be the maximum of x, y, or z. That is, k should be equal to x if x is the maximum value, and same for y and z.

## Solution

$2^{n-2}x_{n-2} + 2^{n-3}x_{n-3} + ... + x_0 \equiv x$

$2^{n-2}y_{n-2} + 2^{n-3}y_{n-3} + ... + y_0 \equiv y$

$2^{n-2}z_{n-2} + 2^{n-3}z_{n-3} + ... + z_0 \equiv z$



$x_{n-2}^2 \equiv x_{n-2}$

$...$

$x_0^2 \equiv x_0$



$y_{n-2}^2 \equiv y_{n-2}$

$...$

$y_0^2 \equiv y_0$



$z_{n-2}^2 \equiv z_{n-2}$

$...$

$z_0^2 \equiv z_0$



$m_x^2 \equiv m_x$

$m_y^2 \equiv m_y$

$m_z^2 \equiv m_z$

$1 \equiv m_x + m_y + m_z$

$2^{n-1}+(x - y) \equiv 2^{n-1}c_{xy_{n-1}} + 2^{n-2}c_{xy_{n-2}} + ... + c_{xy_0}$

$2^{n-1}+(x - z) \equiv 2^{n-1}c_{xz_{n-1}} + 2^{n-2}c_{xz_{n-2}} + ... + c_{xz_0}$

$2^{n-1}+(y - z) \equiv 2^{n-1}c_{yz_{n-1}} + 2^{n-2}c_{yz_{n-2}} + ... + c_{yz_0}$



$c_{xy_{n-1}}^2 \equiv c_{xy_{n-1}}$

$...$

$c_{xy_0}^2 \equiv c_{xy_0}$



$c_{xz_{n-1}}^2 \equiv c_{xz_{n-1}}$

$...$

$c_{xz_0}^2 \equiv c_{xz_0}$



$c_{yz_{n-1}}^2 \equiv c_{yz_{n-1}}$

$...$

$c_{yz_0}^2 \equiv c_{yz_0}$



$0 \equiv m_x \cdot (c_{xy_{n-1}}c_{xz_{n-1}} - 1)$

$0 \equiv m_y \cdot ((1 - c_{xy_{n-1}})c_{yz_{n-1}} - 1)$

$0 \equiv m_z \cdot ((1 - c_{xz_{n-1}})(1 - c_{yz_{n-1}}) - 1)$

$k = m_x x + m_y y + m_z z$
