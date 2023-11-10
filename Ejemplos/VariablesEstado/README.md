# Sistemas de Segundo Orden
## Definición
La función de transferencia de un sistema de primer orden se puede expresar como:

\[
\begin{align*}
\dot{x}_1 &= x_2 \\
\dot{x}_2 &= x_3 \\
\dot{x}_3 &= -a_3 x_3 - a_2 x_2 - a_1 x_1 + b_1 u
\end{align*}
\]

Donde:
- \(x_1\), \(x_2\), \(x_3\) son las variables de estado.
- \(u\) es la entrada del sistema.
- \(a_1\), \(a_2\), \(a_3\) y \(b_1\) son los coeficientes del sistema.

|                         | Python (control)                         | MATLAB                              |
|-------------------------|------------------------------------------|-------------------------------------|
