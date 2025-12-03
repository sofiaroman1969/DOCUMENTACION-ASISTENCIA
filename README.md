# Tecnológico de Software
## Materia: Fundamentos de álgebra
## Alumno: Sofia Roman
## Actividad #18. Matrices: Determinantes y operaciones básicas

---

# Objetivo

Resolver ejercicios prácticos relacionados con el cálculo de determinantes de matrices de diferentes tamaños (2x2, 3x3, 4x4) utilizando diversos métodos, así como verificar propiedades y aplicaciones geométricas de los determinantes.

---

## Índice
- [Ejercicio 1: Determinantes 2x2](#ejercicio-1-determinantes-2x2)
- [Ejercicio 2: Regla de Sarrus](#ejercicio-2-regla-de-sarrus)
- [Ejercicio 3: Método de cofactores](#ejercicio-3-método-de-cofactores)
- [Ejercicio 4: Verificar propiedades](#ejercicio-4-verificar-propiedades)
- [Ejercicio 5: Aplicación geométrica](#ejercicio-5-aplicación-geométrica)

---

## Ejercicio 1: Determinantes 2x2

### Objetivo del ejercicio
Calcular el determinante de las matrices 2x2 utilizando la fórmula adecuada y aplicar este conocimiento en la resolución de problemas prácticos.

---

Calcula el determinante de las siguientes matrices 2x2:

$$A = \begin{pmatrix}
5 & 2 \\
3 & 1  
\end{pmatrix}, \quad 
B = \begin{pmatrix}
-1 & 4 \\
2 & -8
\end{pmatrix}$$

$$C = \begin{pmatrix}
6 & 9 \\
2 & 3
\end{pmatrix}, \quad 
D = \begin{pmatrix}
0 & 5 \\
-5 & 0
\end{pmatrix}$$

### Solución

**Paso 1:** El determinante de una matriz 2x2 se calcula con la fórmula:
$$\det(A) = ad - bc$$

**Paso 2:** Calculamos el determinante de cada matriz:

- **Para la matriz A:**
    $$\det(A) = (5)(1) - (2)(3) = 5 - 6 = -1$$

- **Para la matriz B:**
    $$\det(B) = (-1)(-8) - (4)(2) = 8 - 8 = 0$$

- **Para la matriz C:**
    $$\det(C) = (6)(3) - (9)(2) = 18 - 18 = 0$$

- **Para la matriz D:**
    $$\det(D) = (0)(0) - (5)(-5) = 0 + 25 = 25$$

---

## Ejercicio 2: Regla de Sarrus

### Objetivo del ejercicio
Calcular el determinante de matrices 3x3 utilizando la regla de Sarrus y aplicar este conocimiento en la resolución de problemas prácticos.

---

Usa la regla de Sarrus para calcular el determinante de:

$$E = \begin{pmatrix}
1 & 2 & 3 \\
0 & 1 & 4 \\
5 & 6 & 0
\end{pmatrix}, \quad 
F = \begin{pmatrix}
2 & -1 & 3 \\
1 & 4 & 0 \\
3 & 2 & -2
\end{pmatrix}$$

### Solución

**Paso 1:** Procedimiento de la regla de Sarrus:
1. Dibujar una línea debajo de la matriz
2. Copiar en orden las dos primeras filas de la matriz
3. El número de diagonales debe ser igual a 2 × n

#### Para la matriz E:

**Paso 2:** Extendemos la matriz E:

$$\det(E) = \begin{pmatrix}
1 & 2 & 3 \\
0 & 1 & 4 \\
5 & 6 & 0 \\
\hline
1 & 2 & 3 \\
0 & 1 & 4
\end{pmatrix}$$

**Paso 3:** Calculamos las diagonales de izquierda a derecha:
- $1 \times 1 \times 0 = 0$
- $2 \times 4 \times 5 = 40$
- $3 \times 0 \times 6 = 0$

**Paso 4:** Calculamos las diagonales de derecha a izquierda:
- $3 \times 1 \times 5 = 15$
- $2 \times 0 \times 1 = 0$
- $1 \times 4 \times 6 = 24$

**Paso 5:** Aplicamos la fórmula:
$$\det(E) = (0 + 40 + 0) - (15 + 0 + 24) = 40 - 39 = 1$$

#### Para la matriz F:

**Paso 1:** Extendemos la matriz F:

$$\det(F) = \begin{pmatrix}
2 & -1 & 3 \\
1 & 4 & 0 \\
3 & 2 & -2 \\
\hline
2 & -1 & 3 \\
1 & 4 & 0
\end{pmatrix}$$

**Paso 2:** Calculamos las diagonales de izquierda a derecha:
- $2 \times 4 \times (-2) = -16$
- $(-1) \times 0 \times 3 = 0$
- $3 \times 1 \times 2 = 6$

**Paso 3:** Calculamos las diagonales de derecha a izquierda:
- $3 \times 4 \times 3 = 36$
- $2 \times 0 \times 2 = 0$
- $(-2) \times 1 \times (-1) = 2$

**Paso 4:** Aplicamos la fórmula:
$$\det(F) = (-16 + 0 + 6) - (36 + 0 + 2) = -10 - 38 = -48$$

---

## Ejercicio 3: Método de cofactores

### Objetivo del ejercicio
Calcular el determinante de matrices 4x4 utilizando el método de cofactores y aplicar este conocimiento en la resolución de problemas prácticos.

---

Calcula usando cofactores (expandir por la fila o columna más conveniente):

$$G = \begin{pmatrix}
1 & 0 & 2 \\
-1 & 3 & 1 \\
2 & 0 & 1   
\end{pmatrix}$$

### Solución

**Paso 1:** Procedimiento del método de cofactores:
1. La primera columna se le agrega un signo positivo y negativo de forma alternada.
2. Se multiplica cada elemento de la fila o columna seleccionada por el determinante de la matriz que resulta al eliminar la fila y columna del elemento seleccionado.

**Paso 2:** Expandimos por la primera fila:

$$\det(G) = 1 \cdot \begin{vmatrix}
3 & 1 \\
0 & 1
\end{vmatrix} - 0 \cdot \begin{vmatrix}
-1 & 1 \\
2 & 1
\end{vmatrix} + 2 \cdot \begin{vmatrix}
-1 & 3 \\
2 & 0
\end{vmatrix}$$

**Paso 3:** Calculamos los determinantes de las matrices 2x2 restantes:

$$= 1 \cdot (3 \cdot 1 - 1 \cdot 0) + 2 \cdot (-1 \cdot 0 - 3 \cdot 2)$$
$$= 1 \cdot 3 + 2 \cdot (-6) = 3 - 12 = -9$$

---

## Ejercicio 4: Verificar propiedades

### Objetivo del ejercicio
Verificar las propiedades de los determinantes en matrices 2x2 y 3x3 mediante ejemplos prácticos.

---

Dadas A y B, verifica que:

- $\det(AB) = det(A) \cdot det(B)$

- $\det(A^T) = det(A)$

$$ A = \begin{pmatrix}
2 & 1 \\
1 & 3
\end{pmatrix}, \quad
B = \begin{pmatrix}
1 & 2 \\
3 & 1  
\end{pmatrix}$$

### Solución

**Paso 1:** Calculamos $\det(A)$ y $\det(B)$:
$$\det(A) = (2)(3) - (1)(1) = 6 - 1 = 5$$
$$\det(B) = (1)(1) - (2)(3) = 1 - 6 = -5$$

**Paso 2:** Calculamos $AB$:

$$AB = \begin{pmatrix}
2 & 1 \\
1 & 3
\end{pmatrix} \begin{pmatrix}
1 & 2 \\
3 & 1
\end{pmatrix} = \begin{pmatrix}
2(1) + 1(3) & 2(2) + 1(1) \\
1(1) + 3(3) & 1(2) + 3(1)
\end{pmatrix} = \begin{pmatrix}
5 & 5 \\
10 & 5
\end{pmatrix}$$

**Paso 3:** Calculamos $\det(AB)$:
$$\det(AB) = (5)(5) - (5)(10) = 25 - 50 = -25$$

**Paso 4:** Verificamos la propiedad:
$$\det(A) \cdot \det(B) = 5 \cdot (-5) = -25$$
Por lo tanto, $\det(AB) = \det(A) \cdot \det(B)$ se cumple.

**Paso 5:** Calculamos $A^T$:
$$A^T = \begin{pmatrix}
2 & 1 \\
1 & 3
\end{pmatrix}$$

**Paso 6:** Calculamos $\det(A^T)$:
$$\det(A^T) = (2)(3) - (1)(1) = 6 - 1 = 5$$

**Paso 7:** Verificamos la propiedad:
$\det(A^T) = \det(A)$ se cumple. 

---

## Ejercicio 5: Aplicación geométrica

### Objetivo del ejercicio

Comprender la interpretación geométrica del determinante en términos de áreas y volúmenes.

---

Dados los vectores $\vec{u} = (3, 2)$ y $\vec{v} = (1, 4)$. 

a) Cacula el área del paralelogramo que forman.

b) ¿Cambia el área si intercambian los vectores?

c) ¿Qué representa el signo del determinante?

### Solución

a) El área del paralelogramo formado por los vectores $\vec{u}$ y $\vec{v}$ se calcula usando el determinante de la matriz formada por estos vectores:

$$\text{Area} = \begin{pmatrix}
3 & 1 \\
2 & 4
\end{pmatrix}$$

**Paso 1:** Calculamos el determinante:
$$\det(Area) = (3)(4) - (1)(2) = 12 - 2 = 10$$

b) Si intercambiamos los vectores, la matriz se convierte en:

$$Area = \begin{pmatrix}
1 & 3 \\
4 & 2
\end{pmatrix}$$

**Paso 1:** Calculamos el determinante:
$$\det(Area) = (1)(2) - (3)(4) = 2 - 12 = -10$$

El área sigue siendo 10, pero el signo del determinante cambia.

c) El signo de la determinante representa la orientación de los vectores.

