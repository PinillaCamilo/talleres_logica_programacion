# Taller 3: Manejo de Arrays en Lógica de Programación

**Estudiante:** Camilo Andres Pinilla Garcia
**Asignatura:** Lógica de Programación
**Tema:** Arreglos (vectores y matrices)
**Fecha:** 20-11-2026

---

## Parte 1: Resumen sobre arreglos

Un arreglo es una estructura que permite guardar varios datos del mismo tipo bajo un solo nombre, identificando cada elemento según la posición o índice que ocupa. Como explica Omar Iván Trejos Buriticá, funciona como un grupo de variables ubicadas según su orden respecto al primer dato, de forma similar a una fila en un banco, donde "la quinta persona" corresponde al lugar número cinco.

Cada arreglo reúne cinco elementos principales: un mismo tipo de dato para todo su contenido (como números enteros, reales o caracteres), un nombre que lo identifica, una dimensión definida al crearlo que indica cuántos datos puede guardar, un índice entero que señala la posición (que suele iniciar en 1 en pseudocódigo y en 0 en varios lenguajes de programación) y un tamaño total. Por esta organización, un ciclo Para permite recorrerlo con facilidad y aplicar una misma acción a todos los valores sin necesidad de crear una variable independiente para cada uno.

---

## Parte 2: Ejercicios resueltos

### Nivel básico (vectores)

#### Ejercicio 1: Llenar y mostrar un vector

*Enunciado: Leer 8 números enteros en un vector y mostrarlos en pantalla en el mismo orden en que fueron ingresados.*

**Pseudocódigo:**

```text
Algoritmo LlenarMostrarVector
	Definir i, x, vector Como Entero
	dimension vector[8]
	
	Para i = 1 Hasta 8 Con Paso 1 Hacer
		Escribir "ingrese el numero"
		Leer vector[i]
	FinPara
	x = 8
	Para i = 1 Hasta 8 Con Paso 1 Hacer
		Escribir vector[i]
		x = x -1
	FinPara
FinAlgoritmo
```

**Prueba de escritorio**
supongamos que el usuario ingresa 10, 20, 30, 40, 50, 60, 70, 80:

| i | x | vector[i] | Pantalla |
| :--- | :--- | :--- | :--- |
| 1 | - | 10 | "ingrese el numero" |
| 2 | - | 20 | "ingrese el numero" |
| 3 | - | 30 | "ingrese el numero" |
| 4 | - | 40 | "ingrese el numero" |
| 5 | - | 50 | "ingrese el numero" |
| 6 | - | 60 | "ingrese el numero" |
| 7 | - | 70 | "ingrese el numero" |
| 8 | - | 80 | "ingrese el numero" |
| - | 8 | - | - |
| 1 | 7 | 10 | "10" |
| 2 | 6 | 20 | "20" |
| 3 | 5 | 30 | "30" |
| 4 | 4 | 40 | "40" |
| 5 | 3 | 50 | "50" |
| 6 | 2 | 60 | "60" |
| 7 | 1 | 70 | "70" |
| 8 | 0 | 80 | "80" |


#### Ejercicio 2: Suma de un vector

*Enunciado: Leer 6 números reales en un vector y calcular la suma de todos sus elementos. Mostrar el resultado.*

**Pseudocódigo:**

```text
Algoritmo sumaVector
	Definir  numeros, suma, i Como Entero
	dimension numeros(6)
	
	suma<-0
	Para i <- 1 hasta 6 Con Paso 1 Hacer
		Escribir "Digite el numero ",i,":";
		leer numeros(i)
		suma <- suma + numeros(i)
	FinPara
	Escribir "la suma de los numeros ingresados es: "
	Escribir suma
FinAlgoritmo
```

**Prueba de escritorio**
 supongamos que el usuario ingresa 10, 20, 30, 40, 50, 60:**

| i | numeros(i) | suma | Pantalla |
| :--- | :--- | :--- | :--- |
| - | - | 0 | - |
| 1 | 10 | 10 | "Digite el numero 1:" |
| 2 | 20 | 30 | "Digite el numero 2:" |
| 3 | 30 | 60 | "Digite el numero 3:" |
| 4 | 40 | 100 | "Digite el numero 4:" |
| 5 | 50 | 150 | "Digite el numero 5:" |
| 6 | 60 | 210 | "Digite el numero 6:" |
| - | - | 210 | "la suma de los numeros ingresados es: " |
| - | - | 210 | "210" |


#### Ejercicio 3: Contar números pares

*Enunciado: Leer 10 números enteros en un vector y contar cuántos son pares y cuántos son impares. Mostrar ambos resultados.*

**Pseudocódigo:**

```text
Algoritmo contarnumerosPares
	definir nume, i Como Entero
	Definir numpar Como entero
	definir numimpar Como Entero
	
	dimension numeros(10)
	
	Para i <- 1 hasta 10 Con Paso 1 Hacer
		Escribir "Digite el numero ",i,":";
		leer nume
		si nume % 2 = 0 Entonces
			numpar <- numpar + 1
		SiNo
			numimpar <- numimpar + 1
		FinSi
	FinPara
	Escribir "Cantidad de pares: ", numpar
	Escribir "Cantidad de impares: ", numimpar
	
FinAlgoritmo
```

**Prueba de escritorio**
 supongamos que el usuario ingresa 1, 2, 3, 4, 5, 6, 7, 8, 9, 10:**

| i | nume | numpar | numimpar | Pantalla |
| :--- | :--- | :--- | :--- | :--- |
| 1 | 1 | 0 | 1 | "Digite el numero 1:" |
| 2 | 2 | 1 | 1 | "Digite el numero 2:" |
| 3 | 3 | 1 | 2 | "Digite el numero 3:" |
| 4 | 4 | 2 | 2 | "Digite el numero 4:" |
| 5 | 5 | 2 | 3 | "Digite el numero 5:" |
| 6 | 6 | 3 | 3 | "Digite el numero 6:" |
| 7 | 7 | 3 | 4 | "Digite el numero 7:" |
| 8 | 8 | 4 | 4 | "Digite el numero 8:" |
| 9 | 9 | 4 | 5 | "Digite el numero 9:" |
| 10 | 10 | 5 | 5 | "Digite el numero 10:" |
| - | - | 5 | 5 | "Cantidad de pares: 5" |
| - | - | 5 | 5 | "Cantidad de impares: 5" |


#### Ejercicio 4: Promedio de un vector

*Enunciado: Leer 5 notas (reales) en un vector y calcular su promedio. Mostrar el promedio.*

**Pseudocódigo:**

```text
Algoritmo Promedio_de_un_Vector
	Definir notas Como Real
	dimension notas[5]
	suma <- 0
	Para i <- 1 Hasta 5 Con Paso 1 Hacer
		Escribir "Ingrese la nota", i, ": "
		Leer notas[i]
		suma <- suma + notas[i]
	FinPara
	
	promedio <- suma / 5
	Escribir "El promedio es: ", promedio
FinAlgoritmo
```

**Prueba de escritorio**
 supongamos que el usuario ingresa 4.0, 3.5, 5.0, 4.5, 3.0:

| i | notas[i] | suma | promedio | Pantalla |
| :--- | :--- | :--- | :--- | :--- |
| - | - | 0 | - | - |
| 1 | 4.0 | 4.0 | - | "Ingrese la nota 1: " |
| 2 | 3.5 | 7.5 | - | "Ingrese la nota 2: " |
| 3 | 5.0 | 12.5 | - | "Ingrese la nota 3: " |
| 4 | 4.5 | 17.0 | - | "Ingrese la nota 4: " |
| 5 | 3.0 | 20.0 | - | "Ingrese la nota 5: " |
| - | - | 20.0 | 4.0 | "El promedio es: 4.0" |


#### Ejercicio 5: Mostrar en orden inverso

*Enunciado: Leer 7 números enteros en un vector y mostrarlos en pantalla en orden inverso (del último al primero).*

**Pseudocódigo:**

```text
Algoritmo OrdenInverso
	Definir numeros Como Entero
	Definir i Como Entero
	
	dimension numeros[7]
	
	para i <- 1 Hasta 7 Con Paso 1 Hacer
		Escribir "Ingrese el numero ", i, ": "
		Leer numeros[i]
	FinPara
	
	Escribir "Los numeros en orden inverso son: "
	Para i <- 7 hasta 1 Con Paso -1 Hacer
		Escribir  numeros[i]
	FinPara
FinAlgoritmo
```

**Prueba de escritorio**
supongamos que el usuario ingresa 10, 20, 30, 40, 50, 60, 70:

| i | numeros[i] | Pantalla |
| :--- | :--- | :--- |
| 1 | 10 | "Ingrese el numero 1: " |
| 2 | 20 | "Ingrese el numero 2: " |
| 3 | 30 | "Ingrese el numero 3: " |
| 4 | 40 | "Ingrese el numero 4: " |
| 5 | 50 | "Ingrese el numero 5: " |
| 6 | 60 | "Ingrese el numero 6: " |
| 7 | 70 | "Ingrese el numero 7: " |
| - | - | "Los numeros en orden inverso son: " |
| 7 | 70 | "70" |
| 6 | 60 | "60" |
| 5 | 50 | "50" |
| 4 | 40 | "40" |
| 3 | 30 | "30" |
| 2 | 20 | "20" |
| 1 | 10 | "10" |


---

### Nivel intermedio (vectores con lógica)

#### Ejercicio 6: Buscar el menor

*Enunciado: Leer 8 números enteros en un vector y determinar cuál es el menor y en qué posición se encuentra.*

**Pseudocódigo:**

```text
Algoritmo buscarMenor
	Definir numeros, i, menor, posicion Como Entero
	Dimension numeros[8]
	
	Para i <- 1 Hasta 8 Con Paso 1 Hacer
		Escribir "Ingrese el número ", i, ":"
		Leer numeros[i]
	FinPara
	
	menor <- numeros[1]
	posicion <- 1
	
	Para i <- 2 Hasta 8 Con Paso 1 Hacer
		Si numeros[i] < menor Entonces
			menor <- numeros[i]
			posicion <- i
		FinSi
	FinPara
	
	Escribir "El menor es: ", menor
	Escribir "Está en la posición: ", posicion
FinAlgoritmo
```

**Prueba de escritorio:** (escribe aquí tu prueba con valores concretos)

#### Ejercicio 7: Contar un valor específico

*Enunciado: Leer 10 números enteros en un vector, luego leer un número adicional y determinar cuántas veces aparece ese número en el vector.*

**Pseudocódigo:**

```text
Algoritmo ContarValorEspecifico
	Definir numeros, i, buscado, contador Como Entero
	Dimension numeros[10]
	
	Para i <- 1 Hasta 10 Con Paso 1 Hacer
		Escribir "Ingrese el número ", i, ":"
		Leer numeros[i]
	FinPara
	
	Escribir "Ingrese el número a buscar:"
	Leer buscado
	
	contador <- 0
	Para i <- 1 Hasta 10 Con Paso 1 Hacer
		Si numeros[i] = buscado Entonces
			contador <- contador + 1
		FinSi
	FinPara
	
	Escribir "El número ", buscado, " aparece ", contador, " veces"
FinAlgoritmo
```

**Prueba de escritorio:** (escribe aquí tu prueba con valores concretos)

#### Ejercicio 8: Vector de factoriales

*Enunciado: Leer 5 números enteros en un vector y calcular el factorial de cada uno, almacenándolos en otro vector. Mostrar ambos vectores.*

**Pseudocódigo:**

```text
Algoritmo vector_factoriales
	Definir numeros, factoriales, i, j, fact Como Entero
	Dimension numeros[5]
	Dimension factoriales[5]
	
	Para i <- 1 Hasta 5 Con Paso 1 Hacer
		Escribir "Ingresar el número ", i, ":"
		Leer numeros[i]
	FinPara
	
	Para i <- 1 Hasta 5 Con Paso 1 Hacer
		fact <- 1
		Para j <- 1 Hasta numeros[i] Con Paso 1 Hacer
			fact <- fact * j
		FinPara
		factoriales[i] <- fact
	FinPara
	
	Escribir "Vector original:"
	Para i <- 1 Hasta 5 Con Paso 1 Hacer
		Escribir numeros[i]
	FinPara
	
	Escribir "Vector de factoriales:"
	Para i <- 1 Hasta 5 Con Paso 1 Hacer
		Escribir factoriales[i]
	FinPara
FinAlgoritmo
```

**Prueba de escritorio:** (escribe aquí tu prueba con valores concretos)

#### Ejercicio 9: Invertir un vector

*Enunciado: Leer 6 números enteros en un vector y crear un nuevo vector con los elementos en orden inverso. Mostrar ambos vectores.*

**Pseudocódigo:**

```text
Algoritmo invertir_vector
	Definir original, inverso, i Como Entero
	Dimension original[6]
	Dimension inverso[6]
	
	Para i <- 1 Hasta 6 Con Paso 1 Hacer
		Escribir "Ingrese el número ", i, ":"
		Leer original[i]
	FinPara
	
	Para i <- 1 Hasta 6 Con Paso 1 Hacer
		inverso[7 - i] <- original[i]
	FinPara
	
	Escribir "Vector original:"
	Para i <- 1 Hasta 6 Con Paso 1 Hacer
		Escribir original[i]
	FinPara
	
	Escribir "Vector invertido:"
	Para i <- 1 Hasta 6 Con Paso 1 Hacer
		Escribir inverso[i]
	FinPara
FinAlgoritmo
```

**Prueba de escritorio:** (escribe aquí tu prueba con valores concretos)

#### Ejercicio 10: Suma de vectores

*Enunciado: Leer dos vectores de 5 elementos cada uno y crear un tercer vector que contenga la suma de los elementos correspondientes. Mostrar el vector resultante.*

**Pseudocódigo:**

```text
Algoritmo suma_vectores
	Definir A, B, C, i Como Entero;
	Dimension A[5], B[5], C[5]
	Para i <- 1 Hasta 5 Con Paso 1 Hacer
		Escribir "Digite A[", i, "]:"
		Leer A[i]
	FinPara
	Para i <- 1 Hasta 5 Con Paso 1 Hacer
		Escribir "Digite B[", i, "]:"
		Leer B[i]
	FinPara
	Para i <- 1 Hasta 5 Con Paso 1 Hacer
		C[i] <- A[i] + B[i]
	FinPara
	Escribir "Vector resultante:"
	Para i <- 1 Hasta 5 Con Paso 1 Hacer
		Escribir C[i]
	FinPara
FinAlgoritmo
```



### Nivel avanzado (matrices)

#### Ejercicio 11: Llenar y mostrar una matriz

*Enunciado: Leer una matriz de 3x3 (9 números enteros) y mostrarla en pantalla en forma de tabla.*

**Pseudocódigo:**

```text
Algoritmo llerar_mostrar_matriz
	Definir matriz, l, j Como Entero
	Dimension matriz[3,3]
	
	Para l <- 1 Hasta 3 Con Paso 1 Hacer
		Para j <- 1 Hasta 3 Con Paso 1 Hacer
			Escribir "Ingrese el elemento [", l, ",", j, "]:"
			Leer matriz[l,j]
		FinPara
	FinPara
	
	Escribir "La matriz es:"
	Para l <- 1 Hasta 3 Con Paso 1 Hacer
		Para j <- 1 Hasta 3 Con Paso 1 Hacer
			Escribir Sin Saltar matriz[l,j], "  "
		FinPara
		Escribir ""
	FinPara
FinAlgoritmo
```


#### Ejercicio 12: Suma de filas y columnas

*Enunciado: Leer una matriz de 4x4 y calcular la suma de cada fila y la suma de cada columna. Mostrar los resultados.*

**Pseudocódigo:**

```text
Algoritmo fila_suma
	Definir matriz, i, j, sumaFila, sumaColumna Como Entero
	Dimension matriz[4,4]
	
	Para i <- 1 Hasta 4 Con Paso 1 Hacer
		Para j <- 1 Hasta 4 Con Paso 1 Hacer
			Escribir "Ingrese el elemento [", i, ",", j, "]:"
			Leer matriz[i,j]
		FinPara
	FinPara
	
	Para i <- 1 Hasta 4 Con Paso 1 Hacer
		sumaFila <- 0
		Para j <- 1 Hasta 4 Con Paso 1 Hacer
			sumaFila <- sumaFila + matriz[i,j]
		FinPara
		Escribir "Suma de la fila ", i, ": ", sumaFila
	FinPara
	
	Para j <- 1 Hasta 4 Con Paso 1 Hacer
		sumaColumna <- 0
		Para i <- 1 Hasta 4 Con Paso 1 Hacer
			sumaColumna <- sumaColumna + matriz[i,j]
		FinPara
		Escribir "Suma de la columna ", j, ": ", sumaColumna
	FinPara
FinAlgoritmo
```


#### Ejercicio 13: Buscar un valor en una matriz

*Enunciado: Leer una matriz de 3x3, luego leer un número adicional y determinar si ese número se encuentra en la matriz y en qué posición (fila, columna).*

**Pseudocódigo:**

```text
Algoritmo buscar_valor_matriz
	Definir matriz, i, j, buscado, filaEnc, colEnc Como Entero
	Definir encontrado Como Logico
	Dimension matriz[3,3]
	
	Para i <- 1 Hasta 3 Con Paso 1 Hacer
		Para j <- 1 Hasta 3 Con Paso 1 Hacer
			Escribir "Ingrese el elemento [", i, ",", j, "]:"
			Leer matriz[i,j]
		FinPara
	FinPara
	Escribir "Ingrese el número a buscar:"
	Leer buscado
	encontrado <- Falso
	Para i <- 1 Hasta 3 Con Paso 1 Hacer
		Para j <- 1 Hasta 3 Con Paso 1 Hacer
			Si matriz[i,j] = buscado Y encontrado = Falso Entonces
				encontrado <- Verdadero
				filaEnc <- i
				colEnc <- j
			FinSi
		FinPara
	FinPara
	Si encontrado Entonces
		Escribir "El número está en la fila ", filaEnc, " y columna ", colEnc
	SiNo
		Escribir "El número no se encuentra en la matriz"
	FinSi
FinAlgoritmo
```


#### Ejercicio 14: Transponer una matriz

*Enunciado: Leer una matriz de 3x3 y crear su matriz transpuesta (intercambiar filas por columnas). Mostrar ambas matrices.*

**Pseudocódigo:**

```text
Algoritmo transponer_matriz
	Definir matriz, transpuesta, i, j Como Entero
	Dimension matriz[3,3]
	Dimension transpuesta[3,3]
	
	Para i <- 1 Hasta 3 Con Paso 1 Hacer
		Para j <- 1 Hasta 3 Con Paso 1 Hacer
			Escribir "Ingrese el elemento [", i, ",", j, "]:"
			Leer matriz[i,j]
		FinPara
	FinPara
	Para i <- 1 Hasta 3 Con Paso 1 Hacer
		Para j <- 1 Hasta 3 Con Paso 1 Hacer
			transpuesta[j,i] <- matriz[i,j]
		FinPara
	FinPara
	
	Escribir "Matriz original:"
	Para i <- 1 Hasta 3 Con Paso 1 Hacer
		Para j <- 1 Hasta 3 Con Paso 1 Hacer
			Escribir Sin Saltar matriz[i,j], "  "
		FinPara
		Escribir ""
	FinPara
	
	Escribir "Matriz transpuesta:"
	Para i <- 1 Hasta 3 Con Paso 1 Hacer
		Para j <- 1 Hasta 3 Con Paso 1 Hacer
			Escribir Sin Saltar transpuesta[i,j], "  "
		FinPara
		Escribir ""
	FinPara
FinAlgoritmo
```


#### Ejercicio 15: Contar números primos en una matriz

*Enunciado: Leer una matriz de 4x4 y contar cuántos de sus elementos son números primos. Mostrar el total.*

**Pseudocódigo:**

```text
Algoritmo primos_matriz
	Definir matriz, i, j, k, divisores, totalPrimos Como Entero
	Dimension matriz[4,4]
	
	Para i <- 1 Hasta 4 Con Paso 1 Hacer
		Para j <- 1 Hasta 4 Con Paso 1 Hacer
			Escribir "Ingrese el elemento [", i, ",", j, "]:"
			Leer matriz[i,j]
		FinPara
	FinPara
	
	totalPrimos <- 0
	Para i <- 1 Hasta 4 Con Paso 1 Hacer
		Para j <- 1 Hasta 4 Con Paso 1 Hacer
			divisores <- 0
			Para k <- 1 Hasta matriz[i,j] Con Paso 1 Hacer
				Si matriz[i,j] MOD k = 0 Entonces
					divisores <- divisores + 1
				FinSi
			FinPara
			Si divisores = 2 Entonces
				totalPrimos <- totalPrimos + 1
			FinSi
		FinPara
	FinPara
	
	Escribir "Cantidad de números primos: ", totalPrimos
FinAlgoritmo
```

---

## Reflexión final

Al trabajar con arreglos comprendí cómo agrupar varios datos relacionados bajo un mismo nombre, evitando llenar el programa de variables separadas y usando el orden de sus posiciones para recorrer toda la información de forma sencilla. Considero que son muy importantes en la programación porque facilitan el manejo de grandes cantidades de datos, hacen que las soluciones sean más ordenadas y permiten automatizar tareas repetitivas con mucho menos esfuerzo.
