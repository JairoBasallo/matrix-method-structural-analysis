# matrix-method-structural-analysis

This repository contains a Python function that allows for matrix calculation of 2D structures using an Excel spreadsheet to input element properties, force values, and displacements. The function is capable of assembling the global stiffness matrix from the data entered in the spreadsheet, reading the perfectly fixed boundary forces, node displacement conditions, and unknown reactions, and finally, solving the system of equations.

### Dependencies
The program uses the following Python libraries:

- openpyxl to read the Excel spreadsheet containing the data
- xlsxwriter to save the assembled global stiffness matrix to an Excel spreadsheet
- sympy for symbolic manipulation of equations.
### Usage
To use the program, you should call the matricial() function. This function takes the following parameters:

- number_of_elements: number of elements in the system
- filename: name of the Excel file with the data
- number_of_nodes: number of nodes in the system
- sheet_name: name of the Excel sheet with the data
- cant_springs: number of springs in the system
### Functioning
The program works as follows:

1. Reads the data from the Excel sheet and assembles the global stiffness matrix.
2. Reads the fixed-end forces and displacements from the Excel sheet.
3. Applies rotation to the fixed-end forces and the assembled global matrix depending on the rotation angle of each support.
4. Solves the system of equations.
5. Prints the solution to the system of equations in the console.
6. Saves the assembled global stiffness matrix to an Excel sheet.
### Limitations
The program has the following limitations:

- It only works for two-dimensional structures.
- The Excel sheet must have a specific format for the program to read the data correctly.
- The program does not verify whether the global stiffness matrix is symmetric and positive definite.
