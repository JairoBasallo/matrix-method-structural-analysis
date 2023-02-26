## Cálculo matricial de estructuras

Este es un programa en Python que permite calcular la solución matricial para estructuras en dos dimensiones. El programa utiliza una hoja de cálculo de Excel para introducir las propiedades de los elementos, los valores de las fuerzas y los desplazamientos. Los resultados se imprimen en la consola y también se guardan en una hoja de Excel.

### Dependencias
El programa utiliza las siguientes bibliotecas de Python:

- openpyxl para leer la hoja de Excel que contiene los datos
- xlsxwriter para guardar la matriz de rigidez global ensamblada en una hoja de Excel
- sympy para la manipulación simbólica de las ecuaciones.
### Uso
Para utilizar el programa, se debe llamar a la función matricial(). Esta función tiene los siguientes parámetros:

- number_of_elements: número de elementos del sistema
- filename: nombre del archivo de Excel con los datos
- number_of_nodes: número de nodos del sistema
- sheet_name: nombre de la hoja de Excel con los datos
- cant_springs: cantidad de resortes del sistema
### Funcionamiento
El programa funciona de la siguiente manera:

1. Lee los datos de la hoja de Excel y ensambla la matriz de rigidez global.
2. Lee los valores de las fuerzas de empotramiento y los desplazamientos de la hoja de Excel.
3. Aplica la rotación a las fuerzas de empotramiento y la matriz global ensamblada dependiendo del ángulo de rotación de cada apoyo.
4. Resuelve el sistema de ecuaciones.
5. Imprime la solución del sistema de ecuaciones en la consola.
6. Guarda la matriz de rigidez global ensamblada en una hoja de Excel.
### Limitaciones
El programa tiene las siguientes limitaciones:

- Solo funciona para estructuras en dos dimensiones.
- La hoja de Excel debe tener un formato específico para que el programa pueda leer los datos correctamente.
- El programa no verifica si la matriz de rigidez global es simétrica y definida positiva.

### Licencia
Este programa se distribuye bajo la licencia MIT.
