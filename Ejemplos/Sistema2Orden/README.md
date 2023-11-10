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
```
|                          | Python (control)                                    | MATLAB               |
|--------------------------|-----------------------------------------------------|----------------------|
| **Respuesta al Escalón** | `time, response = ctrl.step_response(G)`           | `step(G)`            |
| **Graficar Respuesta**   | `plt.plot(time, response)`                         | - |
| **Calcular Respuesta en Frecuencia** | `frecuencia, magnitud, fase = ctrl.bode(sistema_python)` | `[magnitud, fase, frecuencia] = bode(sistema_matlab);` |
| **Graficar Diagrama de Bode** | ```plt.semilogx(frecuencia, magnitud)```<br>```plt.semilogx(frecuencia, fase)``` | ```semilogx(frecuencia, 20*log10(magnitud))```<br>```semilogx(frecuencia, fase)``` |
| **Obtener Polos/Ceros**| `polos, ceros = ctrl.pzmap(sistema, plot=False)`             | `polos = pole(sistema); ceros = zero(sistema);` |
| **Graficar Diagrama**  | ```python plt.scatter(np.real(polos), np.imag(polos), ...``` | ```matlab figure pzmap(sistema) title('Diagrama de Polos y Ceros - MATLAB')``` |

[Preguntas a ChatGPT](ChatGPT.md)
