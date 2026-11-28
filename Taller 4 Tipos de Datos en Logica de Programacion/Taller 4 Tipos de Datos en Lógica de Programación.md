# Taller 4: Tipos de Datos en Lógica de Programación

**Asignatura:** Lógica de Programación

**Tema:** Variables y Tipos de Datos

**Basado en:** Lógica de programación, Omar Iván Trejos Buriticá (Capítulo 3)

**Estudiante:** Camilo Andres Pinilla Garcia

**Fecha de entrega:** 27/11/26

## Parte 1: Importancia de los tipos de datos

Según plantea Omar Iván Trejos Buriticá en el Capítulo 3 de su libro Lógica de programación, comprender y definir correctamente los tipos de datos es uno de los pilares esenciales al diseñar cualquier algoritmo. Un dato es la unidad mínima de información con la que trabaja un programa, y asignarle un tipo específico le indica al computador tanto la naturaleza del valor que se va a almacenar como el espacio de memoria que ocupará y las operaciones válidas que pueden realizarse con él. Elegir el tipo de dato adecuado desde el inicio evita errores lógicos, impide mezclar operaciones incompatibles (como intentar sumar un texto con un número) y garantiza que las soluciones sean ordenadas, eficientes y fáciles de entender.

A partir de lo expuesto por Trejos Buriticá y los fundamentos de la programación estructurada, los cinco tipos de datos principales se diferencian de la siguiente manera:

    **Entero:** Representa valores numéricos exactos sin parte decimal, ya sean positivos, negativos o cero (por ejemplo, -8, 0, 25). Se utiliza principalmente para conteos, edades, posiciones en arreglos o cantidades indivisibles.

    **Real:** Representa valores numéricos que sí admiten parte decimal o fraccionaria (por ejemplo, 4.75, -0.5, 12.0). Es indispensable cuando se requiere precisión en cálculos matemáticos, promedios, medidas o porcentajes.

    **Carácter:** Corresponde a un único símbolo individual tomado del código ASCII, como una letra, un dígito tratado como símbolo o un signo de puntuación, encerrado generalmente entre comillas simples ('a', '9', '#').

    **Lógico:** También conocido como booleano, es el tipo de dato más simple en cuanto a valores posibles, pues únicamente admite dos estados: Verdadero o Falso. Resulta fundamental para evaluar condiciones y controlar la toma de decisiones dentro de un algoritmo.

    **Cadena:** Consiste en una secuencia o agrupación de varios caracteres organizados de forma continua (como nombres, palabras o frases completas entre comillas, por ejemplo, "Lógica de programación"), empleada para manejar textos y mensajes descriptivos.

## Parte 2: Ejercicios resueltos

*Para cada ejercicio: responde las preguntas, justifica el tipo de dato de cada variable, escribe el pseudocódigo completo (declaración de variables, Inicio y Fin) y, opcionalmente, una prueba de escritorio.*

### Ejercicio 1: Calcular el área de un triángulo

**Enunciado:** Leer la base y la altura de un triángulo y calcular su área (base × altura / 2).

**Respuestas a las preguntas**

1. ¿Qué tipo de dato usarías para la base y la altura? ¿Entero o Real? ¿Por qué?

  **Respuesta:** Use el dato como **real**, porque formula del area del triangulo es **area = (base * altura)/2**.

2. ¿Qué tipo de dato usarías para el área?

  **Respuesta:** Se usa el tipo de dato Real para el área porque la fórmula lleva una división entre 2, lo que puede generar números con decimales.

**Justificación de variables**

| Variable | Tipo de dato | Justificación |
| --- | --- | --- |        
| base      |real |         Permite ingresar medidas exactas con decimales (ej. 4.5).
| altura    |real |         Permite ingresar medidas exactas con decimales (ej. 3.2).
| area      |real |         Al dividir entre 2 en la fórmula, el resultado puede incluir decimales.       


**Pseudocódigo**

```
Algoritmo area_triangulo
	Definir base, altura, area Como Real
	
	Escribir "Ingrese la base del triangulo:"
	Leer base
	
	Escribir "Ingrese la altura del triangulo:"
	Leer altura
	
	area <- (base * altura) / 2
	Escribir "El area del triangulo es: ", area
	
FinAlgoritmo

```

**Prueba de escritorio:** supongamos que el usuario ingresa base = 10 y altura = 5

| base | altura | area | Pantalla |
| :--- | :--- | :--- | :--- |
| 10 | - | - | "Ingrese la base del triangulo:" |
| 10 | 5 | - | "Ingrese la altura del triangulo:" |
| 10 | 5 | 25 | "El area del triangulo es: 25" |


### Ejercicio 2: Determinar si un número es positivo

**Enunciado:** Leer un número y determinar si es positivo. Mostrar un mensaje.

**Respuestas a las preguntas**

1. ¿Qué tipo de dato usarías para el número? ¿Entero o Real? ¿Por qué?

   **respuesta:** Se usa **Real** porque permite ingresar tanto números decimales como enteros sin perder parte decimal ni generar error con respecto a la condicion "num > 0".

2. ¿Necesitas una variable lógica? ¿Para qué?

   **respuesta:** No es necesaria; la condición **num > 0** ya se evalúa directamente en el **Si**.

**Justificación de variables**

| Variable | Tipo de dato | Justificación |
| --- | --- | --- |
| num| real| Real porque permite ingresar tanto números decimales como enteros|

**Pseudocódigo**

```
Algoritmo num_Positivo
	Definir num Como real
	
	Escribir 'Ingrese el numero:'
	Leer num
	Si (num>0) Entonces
		Escribir 'El numero ', num, ' es positivo'
	SiNo
		Escribir "El numero no es positivo"
	FinSi
FinAlgoritmo
```

**Prueba de escritorio:** Caso 1 supongamos que el usuario ingresa 8

| num | num > 0 | Pantalla |
| :--- | :--- | :--- |
| 8 | Verdadero | "Ingrese el numero:" |
| 8 | Verdadero | "El numero 8 es positivo" |

**Prueba de escritorio:** Caso 2 supongamos que el usuario ingresa -3

| num | num > 0 | Pantalla |
| :--- | :--- | :--- |
| -3 | Falso | "Ingrese el numero:" |
| -3 | Falso | "El numero no es positivo" |

### Ejercicio 3: Convertir una letra a mayúscula

**Enunciado:** Leer una letra minúscula y convertirla a mayúscula usando el código ASCII (restar 32).

**Respuestas a las preguntas**

1. ¿Qué tipo de dato usarías para la letra?

   **respuesta:** **caracter** tanto para la variable (letra) como para los elementos de los arreglos (letrasMin) y (letrasMayus), ya que almacenan un solo símbolo/letra (como 'a' o 'A') y permiten compararlos directamente en letrasMin[i] = letra.

2. ¿Qué pasa si el usuario ingresa un número en lugar de una letra?

  **Respuesta:** No coincide con ningún elemento de letrasMin[1..26]

**Justificación de variables**

| Variable | Tipo de dato | Justificación |
| --- | --- | --- |
| letra | caracter | porque guarda un solo símbolo y permite compararlo directamente con las letras del vector.|
| i | entero | Contador entero para recorrer las 26 posiciones del arreglo (1 a 26). |
| pos | entero | Almacena el índice entero (0 o 1..26) donde se ubica la letra encontrada. |
| codMinus | entero | Guarda el valor numérico ASCII (96 + pos) de la letra minúscula. |
| codMayus | entero | Guarda el valor numérico ASCII resultante (codMinus - 32) de la mayúscula. |
| encontrada | logico | Indica mediante Verdadero o Falso si la letra existía en el vector. |

**Pseudocódigo**

```
Algoritmo ConvertirMayuscula
	Definir letra Como Caracter
	Definir i, pos, codMinus, codMayus Como Entero
	Definir encontrada Como Logico
	Dimension letrasMin[26], letrasMayus[26]
	
	letrasMin[1] <- 'a';  letrasMayus[1] <- 'A'
	letrasMin[2] <- 'b';  letrasMayus[2] <- 'B'
	letrasMin[3] <- 'c';  letrasMayus[3] <- 'C'
	letrasMin[4] <- 'd';  letrasMayus[4] <- 'D'
	letrasMin[5] <- 'e';  letrasMayus[5] <- 'E'
	letrasMin[6] <- 'f';  letrasMayus[6] <- 'F'
	letrasMin[7] <- 'g';  letrasMayus[7] <- 'G'
	letrasMin[8] <- 'h';  letrasMayus[8] <- 'H'
	letrasMin[9] <- 'i';  letrasMayus[9] <- 'I'
	letrasMin[10] <- 'j'; letrasMayus[10] <- 'J'
	letrasMin[11] <- 'k'; letrasMayus[11] <- 'K'
	letrasMin[12] <- 'l'; letrasMayus[12] <- 'L'
	letrasMin[13] <- 'm'; letrasMayus[13] <- 'M'
	letrasMin[14] <- 'n'; letrasMayus[14] <- 'N'
	letrasMin[15] <- 'o'; letrasMayus[15] <- 'O'
	letrasMin[16] <- 'p'; letrasMayus[16] <- 'P'
	letrasMin[17] <- 'q'; letrasMayus[17] <- 'Q'
	letrasMin[18] <- 'r'; letrasMayus[18] <- 'R'
	letrasMin[19] <- 's'; letrasMayus[19] <- 'S'
	letrasMin[20] <- 't'; letrasMayus[20] <- 'T'
	letrasMin[21] <- 'u'; letrasMayus[21] <- 'U'
	letrasMin[22] <- 'v'; letrasMayus[22] <- 'V'
	letrasMin[23] <- 'w'; letrasMayus[23] <- 'W'
	letrasMin[24] <- 'x'; letrasMayus[24] <- 'X'
	letrasMin[25] <- 'y'; letrasMayus[25] <- 'Y'
	letrasMin[26] <- 'z'; letrasMayus[26] <- 'Z'
	
	Escribir 'Ingrese una letra minuscula:'
	Leer letra
	
	encontrada <- Falso
	pos <- 0
	
	Para i <- 1 Hasta 26 Hacer
		Si letrasMin[i] = letra Entonces
			encontrada <- Verdadero
			pos <- i
		FinSi
	FinPara
	
	Si encontrada Entonces
		codMinus <- 96 + pos
		codMayus <- codMinus - 32
		Escribir 'Letra: ', letrasMin[pos], ' (ASCII ', codMinus, ') -> Mayuscula: ', letrasMayus[pos], ' (ASCII ', codMayus, ')'
	SiNo
		Escribir 'No se encontro una letra minuscula valida.'
	FinSi
FinAlgoritmo
```


### Ejercicio 4: Calcular el promedio de tres notas

**Enunciado:** Leer tres notas (pueden tener decimales) y calcular su promedio.

**Respuestas a las preguntas**

1. ¿Qué tipo de dato usarías para las notas? ¿Entero o Real? ¿Por qué?

  **respuesta:** usaria el tipo de dato como **real** porque las notas usan decimales.

2. ¿Qué tipo de dato usarías para el promedio?

   **respuesta:** el dato que se usaria para el promedio seria **real**, porque al realizar la operacion *(promedio = nota1 + nota2 + nota3)/3*; puede dar un numero **real**.

**Justificación de variables**

| Variable | Tipo de dato | Justificación |
| --- | --- | --- |
| nota1 | real | porque las notas normalmente suan numeros reales lo que impica que se pueden usar decimales. |
| nota2 | real | porque las notas normalmente suan numeros reales lo que impica que se pueden usar decimales. |
| nota3 | real | porque las notas normalmente suan numeros reales lo que impica que se pueden usar decimales. |

**Pseudocódigo**

```
Algoritmo promedioNotas
	Definir nota1, nota2, nota3 Como Real
	
	Escribir 'inicio'
	
	Escribir 'ingrese la primera nota:'
	
	Leer nota1
	Escribir 'ingrese la segunda nota:'
	Leer nota2
	
	Escribir 'ingrese la tercera nota:'
	Leer nota3
	
	promedio <- (nota1 + nota2 + nota3) / 3
	Escribir 'el promedio es:', promedio
FinAlgoritmo
```

**Prueba de escritorio:** supongamos que el usuario ingresa 4.0, 3.0, 5.0

| nota1 | nota2 | nota3 | promedio | Pantalla |
| :--- | :--- | :--- | :--- | :--- |
| - | - | - | - | "inicio" |
| 4.0 | - | - | - | "ingrese la primera nota:" |
| 4.0 | 3.0 | - | - | "ingrese la segunda nota:" |
| 4.0 | 3.0 | 5.0 | - | "ingrese la tercera nota:" |
| 4.0 | 3.0 | 5.0 | 4.0 | "el promedio es: 4.0" |

### Ejercicio 5: Validar si un usuario puede votar

**Enunciado:** Leer la edad de una persona y determinar si puede votar (mayor o igual a 18 años). Mostrar un mensaje.

**Respuestas a las preguntas**

1. ¿Qué tipo de dato usarías para la edad? ¿Entero o Real? ¿Por qué?

  **respuesta:** el tipo de dato que usare para la edad es *entero* porque una persona no puede tener **17.5** años.

2. ¿Necesitas una variable lógica? ¿Para qué?

   **respuesta:** como tal no use ninguna variable logica pero si use una expresion logica la cual seria la **(si la edad >= 18)** puede votar, porque si es menor a esa edad no podria participar de la votacion.

**Justificación de variables**

| Variable | Tipo de dato | Justificación |
| --- | --- | --- |
| edad | entero | todas las edades son con numeros enteros. |

**Pseudocódigo**

```
Algoritmo validar_votacion
	Definir edad Como Entero
	
	Escribir "Ingrese su edad"
	Leer edad
	
	si edad >= 18 Entonces
		Escribir "Puede votar"
	SiNo
		Escribir "Usted no puede votar"
	FinSi
	
FinAlgoritmo
```

**Prueba de escritorio** — Caso 1: supongamos que el usuario ingresa 20

| edad | edad >= 18 | Pantalla |
| :--- | :--- | :--- |
| 20 | Verdadero | "Ingrese su edad" |
| 20 | Verdadero | "Puede votar" |

**Prueba de escritorio** — Caso 2: supongamos que el usuario ingresa 15

| edad | edad >= 18 | Pantalla |
| :--- | :--- | :--- |
| 15 | Falso | "Ingrese su edad" |
| 15 | Falso | "Usted no puede votar" |


### Ejercicio 6: Concatenar nombre y apellido

**Enunciado:** Leer el nombre y el apellido de una persona y mostrar el nombre completo.

**Respuestas a las preguntas**

1. ¿Qué tipo de dato usarías para el nombre y el apellido? ¿Carácter o Cadena? ¿Por qué?

   **respuesta:** usare el tipo de dato como **caracter** porque al serel nombre y el apellido llevan varias letras seguidas, aunque usando el tipo de dato en cadena haria la misma funcion.

2. ¿Cómo se concatenan las cadenas en pseudocódigo?

 **respuesta:** con la funcion **concatenar** se pueden unir dos textos en una sola frase, en este caso se une el nombre con el apellido y se puede representar usando la siguiente "formula": -**completo = concatenar(nombre, " ")** -**completo = concatenar(completo, apellido)**

**Justificación de variables**

| Variable | Tipo de dato | Justificación |
| --- | --- | --- |
| nombre | caracter| porque son palabras con una serie de letras  |
| apellido | caracter | porque son palabras con una serie de letras |
| completo | caracter | porque son palabras con una serie de letras |

**Pseudocódigo**

```
Algoritmo NombreCompleto
    Definir nombre, apellido, completo Como Caracter
	
    Escribir "Ingrese su nombre:"
    Leer nombre
	
    Escribir "Ingrese su apellido:"
    Leer apellido
	
    completo <- Concatenar(nombre, " ")
    completo <- Concatenar(completo, apellido)
	
    Escribir "El nombre completo es: ", completo
FinAlgoritmo
```

**Prueba de escritorio:** supongamos que el usuario ingresa (nombre = "Ana" y apellido = "Gómez")

| nombre | apellido | completo | Pantalla |
| :--- | :--- | :--- | :--- |
| "Ana" | - | - | "Ingrese su nombre:" |
| "Ana" | "Gómez" | - | "Ingrese su apellido:" |
| "Ana" | "Gómez" | "Ana " | - |
| "Ana" | "Gómez" | "Ana Gómez" | "El nombre completo es: Ana Gómez" |


### Ejercicio 7: Diferencia entre aritmética entera y real

**Enunciado:** Realizar las siguientes operaciones y mostrar los resultados: a = 10 / 3 (con variables enteras) y b = 10.0 / 3.0 (con variables reales).

**Respuestas a las preguntas**

1. ¿Qué diferencia hay entre los resultados?

**respuesta:** que con las variablen **enteras** va a generar un error ya que al ser dividio en 3 va a dar un numero decimar el cual 3.3333; a diferencia de las variables **reales** que dan su resultado correcto sin generar error el cual es 3.3333.

2. ¿Por qué ocurre esta diferencia?

**respuesta:** porque los numeros enteros no pueden ser decimales y al dividir en 3 da un numero decimal


**Justificación de variables**

| Variable | Tipo de dato | Justificación |
| --- | --- | --- |
| a | entero | especificacion de ejercicio |
| x | entero | especificacion de ejercicio|
| j | entero |especificacion de ejercicio |
| b |real| especificacion de ejercicio |
| m | real|especificacion de ejercicio |
| n | real | especificacion de ejercicio |
**Pseudocódigo**

```
Algoritmo DivisionEnterosYReales
    Definir a, x, j Como entero
    Definir b, m, n Como Real
	
    x <- 10
    j <- 3
    a <- x / j
    Escribir "a = 10 / 3 (enteros) = ", a
	
    m <- 10.0
    n <- 3.0
    b <- m / n
    Escribir "b = 10.0 / 3.0 (reales) = ", b
FinAlgoritmo
```

**Prueba de escritorio**

| x | j | a | m | n | b | Pantalla |
| :--- | :--- | :--- | :--- | :--- | :--- | :--- |
| 10 | - | - | - | - | - | - |
| 10 | 3 | - | - | - | - | - |
| 10 | 3 | 3 | - | - | - | "a = 10 / 3 (enteros) = 3" |
| 10 | 3 | 3 | 10.0 | - | - | - |
| 10 | 3 | 3 | 10.0 | 3.0 | - | - |
| 10 | 3 | 3 | 10.0 | 3.0 | 3.33 | "b = 10.0 / 3.0 (reales) = 3.33" |


### Ejercicio 8: Calcular el salario neto

**Enunciado:** Leer el salario bruto de un empleado y el porcentaje de descuento (ej: 0,10 para 10%). Calcular y mostrar el salario neto.

**Respuestas a las preguntas**

1. ¿Qué tipo de dato usarías para el salario y el descuento? ¿Entero o Real? ¿Por qué?

   **respuesta:** usaria el tipo real, porque puede ser un valor decimal.

2. ¿Qué pasa si el descuento se ingresa como entero (ej: 10 en lugar de 0.10)? ¿Cómo lo corregirías?

**respuesta:** daria error y si el valor ingresado es mayor que 1, se asume que el usuario escribió un porcentaje entero y se divide entre 100.

**Justificación de variables**

| Variable | Tipo de dato | Justificación |
| --- | --- | --- |
|bruto|real| el salario bruto como Real, porque pueden tener decimales.|
|porcentaje|real  | el porcentaje como Real, porque pueden tener decimales.|
|neto|real  |porque es el resultado de la multiplicacion de del bruto y el porcentaje.|

**Pseudocódigo**

```
Algoritmo salario_neto
    Definir bruto, porcentaje, neto Como Real
	
    Escribir "Ingrese el salario bruto:"
    Leer bruto
    Escribir "Ingrese el porcentaje de descuento:"
    Leer porcentaje
	
    neto <- bruto - (bruto * porcentaje)
	
    Escribir "Salario neto: ", neto
FinAlgoritmo
```

### Ejercicio 9: Determinar si un carácter es una vocal

**Enunciado:** Leer un carácter y determinar si es una vocal (a, e, i, o, u). Mostrar un mensaje.

**Respuestas a las preguntas**

1. ¿Qué tipo de dato usarías para el carácter?

  **respuesta:** Tipo Caracter, porque se lee una sola letra.

2. ¿Cómo compararías el carácter con las vocales?

  **respuesta:** Con el operador de igualdad **=** combinado con **O**.

**Justificación de variables**

| Variable | Tipo de dato | Justificación |
| --- | --- | --- |
| letra | caracter |lee una letra.  |

**Pseudocódigo**

```
Algoritmo Vocal
    Definir letra Como Caracter
	
    Escribir "Ingrese una letra:"
    Leer letra
	
    Segun letra Hacer
        "a", "e", "i", "o", "u":
            Escribir "La letra es una vocal."
        De Otro Modo:
            Escribir "La letra no es una vocal."
    FinSegun
FinAlgoritmo
```

**Prueba de escritorio:** — Caso 1 supongamos que el usuario ingresa "e"

| letra | Pantalla |
| :--- | :--- |
| "e" | "Ingrese una letra:" |
| "e" | "La letra es una vocal." |

**Prueba de escritorio:** — Caso 2 supongamos que el usuario ingresa "b"

| letra | Pantalla |
| :--- | :--- |
| "b" | "Ingrese una letra:" |
| "b" | "La letra no es una vocal." |


### Ejercicio 10: Calcular el factorial de un número

**Enunciado:** Leer un número entero positivo y calcular su factorial (ej: 5! = 120). Mostrar el resultado.

**Respuestas a las preguntas**

1. ¿Qué tipo de dato usarías para el número y el factorial? ¿Entero o Real? ¿Por qué?

   **respuesta:** usaria el **real** porque puede ingresar un decimal y le va a dar un resultado entero. 

2. ¿Qué pasa si el número es muy grande? ¿Qué tipo de dato usarías para evitar el desbordamiento?

   **respuesta:** un vector como entero que permita solo realizar el factorial hasta un valor dado 

**Justificación de variables**

| Variable | Tipo de dato | Justificación |
| --- | --- | --- |
| n   |real |  el numero ingresado puede ser un decimal.|
| f   |real | el factorial puede salir de un decimal.|
**Pseudocódigo**

```
Algoritmo Factorial_de_un_Numero
	Definir n, f Como Real
	f<-1
	
	Escribir "ingrese un numero"
	Leer n
	
	Para i<-1 Hasta n Con Paso 1 Hacer
		f<-f*i
	FinPara
	Escribir "El factorial de ",n, " es: ", f 
FinAlgoritmo
```

## Reflexión final

La eleccion de datos no solo me enseño que se puede hacer un proceso mucho mas corto sino que tambien se puede lograr un proceso mucho mas eficaz y capaz de realizar lo que se esta buscando, me ha servido de ayuda para la conpresion de datos y lo distintos tipos que hay de estos dentro de la logica de programacion.