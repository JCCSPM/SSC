# Sistemas de Segundo Orden
## Definición
La función de transferencia de un sistema de primer orden se puede expresar como:

$$
\begin{bmatrix}
\dot{x}_1 \\
\dot{x}_2 \\
\dot{x}_3
\end{bmatrix} =
\begin{bmatrix}
-1 & 0 & 0 \\
0 & -2 & 0 \\
0 & 0 & -3
\end{bmatrix}
\begin{bmatrix}
x_1 \\
x_2 \\
x_3
\end{bmatrix} +
\begin{bmatrix}
1 \\
2 \\
3
\end{bmatrix} u
$$

$$
y =
\begin{bmatrix}
1 & 0 & 0
\end{bmatrix}
\begin{bmatrix}
x_1 \\
x_2 \\
x_3
\end{bmatrix}
$$

|                         | Python (control)                         | MATLAB                              |
|-------------------------|------------------------------------------|-------------------------------------|
