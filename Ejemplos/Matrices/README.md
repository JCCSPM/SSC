# Matrices y Vectores en Python y Matlab
## Vector
| Lenguaje  | Librería/Función | Código para Crear un Vector    | Ejemplo de Vector |
|------------|-------------------|------------------------------|-------------------|
| Python     | NumPy             | `vector_python = [1, 2, 3, 4, 5]` | [1, 2, 3, 4, 5]   |
| MATLAB     | -                 | `vector_matlab = [1, 2, 3, 4, 5];` | [1, 2, 3, 4, 5]   |

Codigo en Python
```python
import numpy as np

# Crear un vector en Python usando NumPy
vector_python = np.array([1, 2, 3, 4, 5])

# Mostrar el vector en Python
print("Vector en Python:", vector_python)
```

Codigo en Matlab
```matlab
% Crear un vector en MATLAB
vector_matlab = [1, 2, 3, 4, 5];

% Mostrar el vector en MATLAB
disp('Vector en MATLAB:')
disp(vector_matlab)
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
