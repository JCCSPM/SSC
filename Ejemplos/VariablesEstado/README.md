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
| **Crear Sistema de Espacio de Estados** | `ctrl.StateSpace(A, B, C, D)` | `ss(A, B, C, D)` |
| **Mostrar Representación en Variables de Estado** | `print(sistema_python)`               | `disp(sistema_matlab)`               |

Codigo en Python
```python
import control as ctrl

# Parámetros del sistema de tercer orden
A = [[-1, 0, 0], [0, -2, 0], [0, 0, -3]]
B = [[1], [2], [3]]
C = [[1, 0, 0]]
D = [[0]]

# Crear el sistema de espacio de estados en Python usando control
sistema_python = ctrl.StateSpace(A, B, C, D)

# Mostrar la representación en variables de estado
print("Representación en variables de estado en Python:")
print(sistema_python)
```

Codigo en Matlab
```matlab
% Parámetros del sistema de tercer orden
A = [-1, 0, 0; 0, -2, 0; 0, 0, -3];
B = [1; 2; 3];
C = [1, 0, 0];
D = 0;

% Crear el sistema de espacio de estados en MATLAB
sistema_matlab = ss(A, B, C, D);

% Mostrar la representación en variables de estado en MATLAB
disp('Representación en variables de estado en MATLAB:')
disp(sistema_matlab)
```

[Preguntas a ChatGPT](ChatGPT.md)
