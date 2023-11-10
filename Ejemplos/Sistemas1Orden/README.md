# Sistemas de Primer Orden
## Definición
La función de transferencia de un sistema de primer orden se puede expresar como:

\[ G(s) = \frac{K}{\tau s + 1} \]

Donde:
- \( K \) es la ganancia del sistema.
- \( \tau \) es la constante de tiempo.

- $\sqrt{3x-1}+(1+x)^2$

|                          | Python (control)                                    | MATLAB               |
|--------------------------|-----------------------------------------------------|----------------------|
| **Crear Sistema**        | `G = ctrl.TransferFunction([1], [tau, 1])`         | `G = tf(1, [tau, 1])`|
| **Mostrar Func. Transferencia** | `print(G)`                                      | `disp(G)`            |
| **Respuesta al Escalón** | `time, response = ctrl.step_response(G)`           | `step(G)`            |
| **Graficar Respuesta**   | `plt.plot(time, response)`                         | `title('Respuesta al Escalón en MATLAB')` |

Codigo en Python
```python
import numpy as np
import matplotlib.pyplot as plt
from scipy import signal

# Parámetros del sistema de primer orden
tau = 1.0  # Constante de tiempo
K = 2.0    # Ganancia

# Crear el sistema de primer orden en Python
sistema_primer_orden_python = signal.TransferFunction([K], [tau, 1])

# Mostrar la representación en espacio de estados
print("Representación en espacio de estados en Python:")
print(signal.tf2ss([K], [tau, 1]))

# Graficar la respuesta al escalón en Python
time, response = signal.step(sistema_primer_orden_python)
plt.plot(time, response)
plt.title('Respuesta al escalón en Python')
plt.xlabel('Tiempo')
plt.ylabel('Respuesta al escalón')
plt.grid(True)
plt.show()
```

Codigo en Matlab
```matlab
% Parámetros del sistema de primer orden
tau = 1.0;  % Constante de tiempo
K = 2.0;    % Ganancia

% Crear el sistema de primer orden en MATLAB
sistema_primer_orden_matlab = tf([K], [tau, 1]);

% Mostrar la representación en espacio de estados
disp('Representación en espacio de estados en MATLAB:')
disp(tf2ss(sistema_primer_orden_matlab))

% Graficar la respuesta al escalón en MATLAB
step(sistema_primer_orden_matlab)
title('Respuesta al escalón en MATLAB')
```

## Matriz
| Lenguaje  | Librería/Función | Código para Crear una Matriz    | Ejemplo de Vector |
|------------|-------------------|------------------------------|-------------------|
| Python     | NumPy             | matriz_python = np.array([[1, 2, 3], [4, 5, 6], [7, 8, 9]]) | [1, 2, 3; 4, 5, 6; 7, 8, 9]   |
| MATLAB     | -                 | matriz_matlab = [1, 2, 3; 4, 5, 6; 7, 8, 9]; | [1, 2, 3; 4, 5, 6; 7, 8, 9]  |

Codigo en Python
```python
import numpy as np

# Crear una matriz en Python usando NumPy
matriz_python = np.array([[1, 2, 3], [4, 5, 6], [7, 8, 9]])

# Mostrar la matriz
print("Matriz en Python:\n", matriz_python)
```

Codigo en Matlab
```matlab
% Crear una matriz en MATLAB
matriz_matlab = [1, 2, 3; 4, 5, 6; 7, 8, 9];

% Mostrar la matriz
disp('Matriz en MATLAB:')
disp(matriz_matlab)
```

[Preguntas a ChatGPT](ChatGPT.md)
