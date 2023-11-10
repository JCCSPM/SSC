# Sistemas de Primer Orden
## Definición
La función de transferencia de un sistema de primer orden se puede expresar como:

$G(s) = \frac{K}{\tau s + 1}$

Donde:
- $K$ es la ganancia del sistema.
- $\tau$ es la constante de tiempo.

|                          | Python (control)                                    | MATLAB               |
|--------------------------|-----------------------------------------------------|----------------------|
| **Crear Sistema**        | `G = ctrl.TransferFunction([1], [tau, 1])`         | `G = tf(1, [tau, 1])`|
| **Mostrar Func. Transferencia** | `print(G)`                                      | `disp(G)`            |

Codigo en Python
```python
import control as ctrl
import matplotlib.pyplot as plt

# Parámetros del sistema de primer orden
tau = 1.0  # constante de tiempo
K = 2.0    # ganancia

# Crear la función de transferencia en Python usando control
sistema_python = ctrl.TransferFunction([K], [tau, 1])

# Mostrar la función de transferencia
print("Función de transferencia en Python:")
print(sistema_python)
```

Codigo en Matlab
```matlab
% Parámetros del sistema de primer orden
tau = 1.0;  % constante de tiempo
K = 2.0;    % ganancia

% Crear la función de transferencia en MATLAB
sistema_matlab = tf([K], [tau, 1]);

% Mostrar la función de transferencia en MATLAB
disp('Función de transferencia en MATLAB:')
disp(sistema_matlab)
```

## Respuesta a Entrada Paso
|                          | Python (control)                                    | MATLAB               |
|--------------------------|-----------------------------------------------------|----------------------|
| **Respuesta al Escalón** | `time, response = ctrl.step_response(G)`           | `step(G)`            |
| **Graficar Respuesta**   | `plt.plot(time, response)`                         | - |

Codigo en Python
```python
# Graficar la respuesta al escalón en Python
time, response = ctrl.step_response(sistema_python)
plt.plot(time, response)
plt.title('Respuesta al escalón en Python')
plt.xlabel('Tiempo')
plt.ylabel('Respuesta al escalón')
plt.grid(True)
plt.show()
```

Codigo en Matlab
```matlab
% Graficar la respuesta al escalón en MATLAB
figure;
step(sistema_matlab);
title('Respuesta al escalón en MATLAB');
```

[Preguntas a ChatGPT](ChatGPT.md)
