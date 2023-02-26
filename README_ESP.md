# Cálculo matricial de estructuras

Este repositorio contiene una función en Python que permite hacer el cálculo matricial de estructuras para estructuras en dos dimensiones a través de una hoja de cálculo de Excel para introducir las propiedades de los elementos, los valores de las fuerzas y los desplazamientos. La función es capaz de ensamblar la matriz de rigidez global a partir de los datos ingresados en la hoja de cálculo, leer las fuerzas de empotramiento perfecto, las condiciones de desplazamiento de los nodos y las reacciones desconocidas, y finalmente, resolver el sistema de ecuaciones.

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
- las unidades en el excel deben ser concordantes entre si
- no se puede tener celdas vacias, por lo menos se deben llenar con un cero.
