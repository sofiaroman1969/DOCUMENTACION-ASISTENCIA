# Tecnológico de Software
## Materia: Fundamentos de álgebra
## Alumno: Sofia Roman
## Actividad #16.  Matrices documentación

---
# Objetivo

Familiarizarse con la clasificación y operaciones básicas de matrices, incluyendo suma, resta, multiplicación y transposición.

---

## Índice
- [Ejercicio 1: Clasificación de matrices](#ejercicio-1-clasificación-de-matrices)
- [Ejercicio 2: Operaciones con matrices](#ejercicio-2-operaciones-con-matrices)
- [Ejercicio 3: Multiplicación cadena](#ejercicio-3-multiplicación-cadena)

---

# Ejercicio 1: Clasificación de matrices

## Objetivo del ejercicio: 

Identificar y clasificar diferentes tipos de matrices según sus propiedades.


### a) 

$$A = \begin{bmatrix}
1 & 0 \\
0 & 1 
\end{bmatrix}$$

Es una matriz *identidad*, ya que su diagonal principal está compuesta por **unos** y los demás elementos son ceros. 

### b) 

$$ B = \begin{bmatrix}
3 & 0 & 0 \\
0 & -2 & 0 \\
0 & 0 & 5 
\end{bmatrix}  $$

Es una matriz *diagonal*, ya que todos los elementos están compuestos por ceros **exceptuando** su diagonal principal.

### c)

$$C = \begin{bmatrix}
2 & 1 & 4 \\
1 & 3 & 5 \\
4 & 5 & 6 
\end{bmatrix}  $$

Es una matriz *simétrica*, ya que $a_ij = a_ji$ es simétrica respecto a su diagonal principal.

### d)

$$ D = \begin{bmatrix}
1 & 2 & 3 \\
0 & 4 & 5 \\
0 & 0 & 6 
\end{bmatrix}  $$

Es una matriz *triangular superior*, ya que todos los elementos debajo de la diagonal principal son ceros.

---

# Ejercicio 2: Operaciones con matrices

## Objetivo del ejercicio:

Realizar operaciones básicas con matrices, incluyendo suma, resta, multiplicación y transposición.

Dadas las matrices:

$$ A = \begin{bmatrix}
2 & -1 \\
3 & 4 
\end{bmatrix}, \quad B = \begin{bmatrix}
5 & 2 \\
-1 & 3 
\end{bmatrix} $$

Calcula: 

### a) Suma de matrices: \( A + B \)
$$ A + B = \begin{bmatrix}
2 + 5 & -1 + 2 \\
3 + (-1) & 4 + 3
\end{bmatrix} = \begin{bmatrix}
7 & 1 \\
2 & 7
\end{bmatrix} $$

### b) Resta  y  multiplicación de matrices: \(2A - B \)

$$ 2A - B = 2 \begin{bmatrix}
2 & -1 \\
3 & 4
\end{bmatrix} - \begin{bmatrix}
5 & 2 \\    
-1 & 3
\end{bmatrix} = \begin{bmatrix}
4 & -2 \\
6 & 8
\end{bmatrix} - \begin{bmatrix}
5 & 2 \\
-1 & 3
\end{bmatrix} = \begin{bmatrix}
-1 & -4 \\
7 & 5
\end{bmatrix} $$

### c) Multiplicación de matrices: \( AB \)
$$ AB = \begin{bmatrix}
2 & -1 \\
3 & 4
\end{bmatrix} \begin{bmatrix}
5 & 2 \\
-1 & 3
\end{bmatrix} = \begin{bmatrix}
2\cdot5+(-1)\cdot(-1) & 2\cdot2+(-1)\cdot3\\
3\cdot5+4\cdot(-1)    & 3\cdot2+4\cdot3
\end{bmatrix} = \begin{bmatrix}
11 & 1 \\
11 & 18
\end{bmatrix} $$

### d) Multiplicación de matrices: \( BA \)
$$ BA = \begin{bmatrix}
5 & 2 \\
-1 & 3
\end{bmatrix} \begin{bmatrix}
2 & -1 \\
3 & 4
\end{bmatrix} = \begin{bmatrix}
(5\cdot2) + (2\cdot3) & (5\cdot-1) + (2\cdot4) \\
(-1\cdot2) + (3\cdot3) & (-1\cdot-1) + (3\cdot4)
\end{bmatrix} = \begin{bmatrix}
16 & 3 \\
7 & 13
\end{bmatrix} $$

### e) Transpuesta de la matriz A: \( A^T \)
$$ A^T = \begin{bmatrix}
2 & 3 \\
-1 & 4
\end{bmatrix} $$

---

# Ejercicio 3: Multiplicación cadena

## Objetivo del ejercicio:
Comprobar la propiedad asociativa de la multiplicación de matrices mediante el cálculo de productos en cadena.

---

*Verificar que* $(AB)C = A(BC)$ 

Dadas las matrices:

$$ A = \begin{bmatrix}
1 & 2 \\
3 & 4 
\end{bmatrix}, \quad B = \begin{bmatrix}
2 & 0 \\
1 & 3 
\end{bmatrix}, \quad C = \begin{bmatrix}
1 & 1 \\
0 & 2
\end{bmatrix} $$

### a) Calcular \( (AB)C \)
$$ AB = \begin{bmatrix}
1 & 2 \\
3 & 4
\end{bmatrix} \begin{bmatrix}
2 & 0 \\
1 & 3
\end{bmatrix} = \begin{bmatrix}
(1\cdot2) + (2\cdot1) & (1\cdot0) + (2\cdot3) \\
(3\cdot2) + (4\cdot1) & (3\cdot0) + (4\cdot3)
\end{bmatrix} = \begin{bmatrix}
4 & 6 \\
10 & 12
\end{bmatrix} $$
$$ (AB)C = \begin{bmatrix}
4 & 6 \\
10 & 12
\end{bmatrix} \begin{bmatrix}
1 & 1 \\
0 & 2
\end{bmatrix} = \begin{bmatrix}
(4\cdot1) + (6\cdot0) & (4\cdot1) + (6\cdot2) \\
(10\cdot1) + (12\cdot0) & (10\cdot1) + (12\cdot2)
\end{bmatrix} = \begin{bmatrix}
4 & 16 \\
10 & 34
\end{bmatrix} $$

### b) Calcular \( A(BC) \)
$$ BC = \begin{bmatrix}
2 & 0 \\
1 & 3
\end{bmatrix} \begin{bmatrix}
1 & 1 \\
0 & 2
\end{bmatrix} = \begin{bmatrix}
(2\cdot1) + (0\cdot0) & (2\cdot1) + (0\cdot2) \\
(1\cdot1) + (3\cdot0) & (1\cdot1) + (3\cdot2)
\end{bmatrix} = \begin{bmatrix}
2 & 2 \\
1 & 7
\end{bmatrix} $$
$$ A(BC) = \begin{bmatrix}
1 & 2 \\
3 & 4
\end{bmatrix} \begin{bmatrix}
2 & 2 \\
1 & 7
\end{bmatrix} = \begin{bmatrix}
(1\cdot2) + (2\cdot1) & (1\cdot2) + (2\cdot7) \\
(3\cdot2) + (4\cdot1) & (3\cdot2) + (4\cdot7)
\end{bmatrix} = \begin{bmatrix}
4 & 16 \\
10 & 34
\end{bmatrix} $$

*Conclusión*: Por lo tanto, se verifica que $(AB)C = A(BC)$.

