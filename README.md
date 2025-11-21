# Tecnológico de Software
## Materia: Fundamentos de álgebra
## Alumno: Michelle Cámara González
## Actividad #19.  Matrices excel documentación

---
# Objetivo
Documentar el uso de matriz en Google Sheets, en donde se cree una imagen con dimensión 30x30 utilizando las herramientas de formato condicional y las funciones de Google Sheets.

---

# Desarrollo 

Para crear una imagen utilizando matrices en Google Sheets, se pueden seguir los siguientes pasos:

1. **Crear una nueva hoja de cálculo**: Abre Google Sheets y crea una nueva hoja de cálculo.

2. **Definir el tamaño de la matriz**: Decide el tamaño de la matriz que deseas crear. En este caso, se utilizará una matriz de 30x30.

3. **Llenar la matriz con datos**: Llena las celdas de la matriz con valores que representen los colores que deseas utilizar en la imagen. Por ejemplo, puedes usar números del 0 al 1 para representar diferentes tonos de gris. 

```
0 --> tonos blancos.
1 --> tonos negros.
```
4. **Crear matriz de la imagen**: Para crear la matriz en escala de grises se utiliza el código preliminar en Python. El cual se va editar la variable ```ruta``` con el path de la imagen. 

```Python
import cv2
import numpy as np
import matplotlib.pyplot as plt

def imagen_a_grises_30x30(ruta_imagen: str) -> np.ndarray:
    """
    Lee una imagen, la convierte a escala de grises, la redimensiona a 30x30  y la normaliza a valores entre 0 y 1.
    """

    #Cargar imagen en escala de grises
    img = cv2.imread(ruta_imagen, cv2.IMREAD_GRAYSCALE)

    if img is None:
        raise FileNotFoundError(f"No se pudo abrir la imagen: {ruta_imagen}")

    print("Tamaño original:", img.shape)

    # Redimensionar imagen
    img_30 = cv2.resize(img, (30, 30), interpolation=cv2.INTER_AREA)
    print("Tamaño redimensionado:", img_30.shape)


    # Convertir a float y normalizar imagen
    img_norm = 1- img_30.astype(np.float32) / 255.0

    return img_norm


def matriz_a_texto_comas(matriz: np.ndarray, decimales: int = 2) -> str:
    filas_str = []
    for fila in matriz:
        valores = [f"{v:.{decimales}f}" for v in fila]
        filas_str.append(",".join(valores))
    return "\n".join(filas_str)


if __name__ == "__main__":
    # Ruta de la imagen
    ruta = "/content/images.jpg"

    # Obtener matriz 30x30 en escala de grises [0,1]
    mat = imagen_a_grises_30x30(ruta)

    print("Shape de la matriz:", mat.shape)

    #Matriz por comas
    texto_comas = matriz_a_texto_comas(mat, decimales=2)
    print("\nMatriz formateada con comas:")
    print(texto_comas)

    with open("matriz_30x30.txt", "w", encoding="utf-8") as f:
        f.write(texto_comas)
    print("\nSe guardó la matriz en matriz_30x30.txt")

    
#Muestra cómo se ve la imagen
plt.imshow(mat, cmap='gray', vmin=0, vmax=1)
plt.title("Imagen 30x30 en escala de grises (normalizada)")
plt.show()

```

5. **Cambiar el formato de las celdas**: 
```
Seleccionar columna A hasta la columna AD (30 columnas). --> Cambiar tamaño el tamaño de las columnas a 20. --> Seleccionar fila 1 hasta la fila 30 (30 filas). --> Cambiar el tamaño de las filas a 20.
```

6. **Aplicar formato condicional**: 
```
Seleccionar el rango de A1:AD30 --> Formato --> Formato condicional --> Punto mínimo: 0 --> Color blanco. --> Punto máximo: 1 --> Color de tu elección. --> Listo.
```

7. **Ingresar los datos en la matriz**: Copia y pega los datos generados por el código Python en el rango A1:AD30 de tu hoja de cálculo de Google Sheets.


| A | B | C | D | E | F | G | H | I | J | K | L | M | N | O | P | Q | R | S | T | U | V | W | X | Y | Z | AA | AB | AC | AD |
|---|---|---|---|---|---|---|---|---|---|---|---|---|---|---|---|---|---|---|---|---|---|---|---|---|---|---|---|---|---|
|0|0|0|0|0|0|0|0|0|0|0|0|0|0|0|0|0|0|0|0|0|0|0|0|0|0|0|0|0|0|
|0|0|0|0|0|0|0|0|0|0|0|0|0|0|0|0|0|0|0|0|0|0|0|0|0|0|0|0|0|0|
|0|0|0|0|0|0|0|0|0|0|0|0|0|0|0|0|0|0|0|0|0|0|0|0|0|0|0|0|0|0|
|0|0|0|0|0|0|0|0|0|0|0|0|0|0|0|0|0|0|0|0|0|0|0|0|0|0|0|0|0|0|
|0|0|0|0|0|0|0|0|0|0|0|0|0|0|0|0|0|0|0|0|0|0|0|0|0|0|0|0|0|0|
|0|0|0|0|0|0|0|0|0|0|0|0|0|0|0|0|0|0|0|0|0|0|0|0|0|0|0|0|0|0|
|0|0|0|0|0|0|0|0|0|0|0|0|0|0|0.2|0.2|0|0|0|0|0|0|0|0|0|0|0|0|0|0|
|0|0|0|0|0|0|0|0|0|0|0|0|0|0.2|0.3|0.2|0.2|0|0|0|0|0|0|0|0|0|0|0|0|0|
|0|0|0|0|0|0|0|0|0|0|0|0|0.2|0.3|0.4|0.3|0.2|0.2|0|0|0|0|0|0|0|0|0|0|0|0|
|0|0|0|0|0|0|0|0|0|0|0|0.2|0.3|0.4|0.5|0.4|0.3|0.2|0.2|0|0|0|0|0|0|0|0|0|0|0|
|0|0|0|0|0|0|0|0|0|0|0.2|0.3|0.4|0.5|0.6|0.5|0.4|0.3|0.2|0.2|0|0|0|0|0|0|0|0|0|0|
|0|0|0|0|0|0|0|0|0|0.2|0.3|0.4|0.5|0.6|0.7|0.6|0.5|0.4|0.3|0.2|0.2|0|0|0|0|0|0|0|0|0|
|0|0|0|0|0|0|0|0|0.2|0.3|0.4|0.5|0.6|0.7|0.8|0.7|0.6|0.5|0.4|0.3|0.2|0.2|0|0|0|0|0|0|0|0|
|0|0|0|0|0|0|0|0.2|0.3|0.4|0.5|0.6|0.7|0.8|0.9|0.8|0.7|0.6|0.5|0.4|0.3|0.2|0.2|0|0|0|0|0|0|0|
|0|0|0|0|0|0|0.2|0.3|0.4|0.5|0.6|0.7|0.8|0.9|1|0.9|0.8|0.7|0.6|0.5|0.4|0.3|0.2|0.2|0|0|0|0|0|0|
|0|0|0|0|0|0.2|0.3|0.4|0.5|0.6|0.7|0.8|0.9|1|1|1|0.9|0.8|0.7|0.6|0.5|0.4|0.3|0.2|0.2|0|0|0|0|0|
|0|0|0|0|0.2|0.3|0.4|0.5|0.6|0.7|0.8|0.9|1|1|1|1|1|0.9|0.8|0.7|0.6|0.5|0.4|0.3|0.2|0.2|0|0|0|0|
|0|0|0|0.2|0.3|0.4|0.5|0.6|0.7|0.8|0.9|1|1|1|1|1|1|1|0.9|0.8|0.7|0.6|0.5|0.4|0.3|0.2|0.2|0|0|0|
|0|0|0.2|0.3|0.4|0.5|0.6|0.7|0.8|0.9|1|1|1|1|1|1|1|1|1|0.9|0.8|0.7|0.6|0.5|0.4|0.3|0.2|0.2|0|0|
|0|0.2|0.3|0.4|0.5|0.6|0.7|0.8|0.9|1|1|1|1|1|1|1|1|1|1|1|0.9|0.8|0.7|0.6|0.5|0.4|0.3|0.2|0.2|0|
|0.2|0.3|0.4|0.5|0.6|0.7|0.8|0.9|1|1|1|1|1|1|1|1|1|1|1|1|1|0.9|0.8|0.7|0.6|0.5|0.4|0.3|0.2|0.2|
|0|0|0|0|0|0|0|0|0|0|0|0|0|0|0|0|0|0|0|0|0|0|0|0|0|0|0|0|0|0|
|0|0|0|0|0|0|0|0|0|0|0|0|0|0|0|0|0|0|0|0|0|0|0|0|0|0|0|0|0|0|
|0|0|0|0|0|0|0|0|0|0|0|0|0|0|0|0|0|0|0|0|0|0|0|0|0|0|0|0|0|0|
|0|0|0|0|0|0|0|0|0|0|0|0|0|0|0|0|0|0|0|0|0|0|0|0|0|0|0|0|0|0|
|0|0|0|0|0|0|0|0|0|0|0|0|0|0|0|0|0|0|0|0|0|0|0|0|0|0|0|0|0|0|
|0|0|0|0|0|0|0|0|0|0|0|0|0|0|0|0|0|0|0|0|0|0|0|0|0|0|0|0|0|0|
|0|0|0|0|0|0|0|0|0|0|0|0|0|0|0|0|0|0|0|0|0|0|0|0|0|0|0|0|0|0|
|0|0|0|0|0|0|0|0|0|0|0|0|0|0|0|0|0|0|0|0|0|0|0|0|0|0|0|0|0|0|
|0|0|0|0|0|0|0|0|0|0|0|0|0|0|0|0|0|0|0|0|0|0|0|0|0|0|0|0|0|0|

8. **Visualizar la imagen**: Una vez que hayas ingresado todos los datos, deberías ver una representación visual de la imagen en escala de grises en tu hoja de cálculo.

## Suma de matrices en Google Sheets 

Para sumar dos matrices en Google Sheets, se usa la función  `=ARRAYFORMULA()` junto con la operación de suma.

De acuerdo a cómo se llame tu hoja de cálculo en donde tienes tu primera matriz, por ejemplo: "Triangulo".
```
=ARRAYFORMULA(Triangulo!A1:AD30 + OtraHoja!A1:AD30)
```

Se obtendrá la suma de las matrices.

## Resta de matrices en Google Sheets

Para restar dos matrices en Google Sheets, se usa la función  `=ARRAYFORMULA()` junto con la operación de resta. 

De acuerdo a cómo se llame tu hoja de cálculo en donde tienes tu primera matriz, por ejemplo: "Triangulo".
```
=ARRAYFORMULA(Triangulo!A1:AD30 - OtraHoja!A1:AD30)
```

Se obtendrá la resta de las matrices.

## Multiplicación Escalar en Google Sheets

Para multiplicar una matriz por un escalar en Google Sheets, se usa la función  `=ARRAYFORMULA()` junto con la operación de multiplicación. 

**Nota**: Elige una celda en donde escribirás el escalar por el que se va a multiplicar. Ejemplo: F33.

```
=ARRAYFORMULA($F$33 * Triangulo!A1:AD30)
```

Y se obtendrá la mátriz multiplicada por un escalar. 

## Transponer una matriz en Google Sheets

Para transponer una matriz en Google Sheets, se usa la función `=TRANSPOSE()`. 

De acuerdo a como se llame tu hoja de cálculo en donde tienes tu primera matriz, por ejemplo: "Triangulo".

```
=TRANSPONSE(Triangulo!A1:AD30)
```

Y se obtendrá la matriz transpuesta.

## Invertir una matriz en Google Sheets

Para invertir una matriz en Google Sheets, se usa la función `=ARRAYFORMULA()`. Se va a restar a 1 la hoja de cálculo en donde se tiene la matriz, ejemplo: "Triangulo".

```
=ARRAYFORMULA(1-Triangulo!A1:AD30)
```

Y se obtendrá la imagen invertida.

---
