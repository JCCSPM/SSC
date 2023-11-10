# Sistemas de Segundo Orden
## Definición
La función de transferencia de un sistema de primer orden se puede expresar como:

$G(s) = \frac{w_n^2}{s^2+2\zeta w_n + w_n^2}$

Donde:
- $w_n^2$ Frecuencia Natural.
- $\zeta$ Coeficiente de amortiguamiento.

|                         | Python (control)                         | MATLAB                              |
|-------------------------|------------------------------------------|-------------------------------------|
| **Crear Función de Transferencia** | `ctrl.TransferFunction([omega_n**2], [1, 2*zeta*omega_n, omega_n**2])` | `tf([omega_n^2], [1, 2*zeta*omega_n, omega_n^2])` |
| **Mostrar Función de Transferencia** | `print(sistema_python)`               | `disp(sistema_matlab)`               |
| **Respuesta al Escalón** | `ctrl.step_response(sistema_python)`    | `step(sistema_matlab)`               |

Codigo en Python
```python
import control as ctrl
import matplotlib.pyplot as plt

# Parámetros del sistema de segundo orden
zeta = 0.7   # factor de amortiguamiento
omega_n = 2.0 # frecuencia natural

# Crear la función de transferencia en Python usando control
sistema_python = ctrl.TransferFunction([omega_n**2], [1, 2*zeta*omega_n, omega_n**2])

# Mostrar la función de transferencia
print("Función de transferencia en Python:")
print(sistema_python)

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
% Parámetros del sistema de segundo orden
zeta = 0.7;   % factor de amortiguamiento
omega_n = 2.0; % frecuencia natural

% Crear la función de transferencia en MATLAB
sistema_matlab = tf([omega_n^2], [1, 2*zeta*omega_n, omega_n^2]);

% Mostrar la función de transferencia en MATLAB
disp('Función de transferencia en MATLAB:')
disp(sistema_matlab)

% Graficar la respuesta al escalón en MATLAB
figure;
step(sistema_matlab);
title('Respuesta al escalón en MATLAB');
```
