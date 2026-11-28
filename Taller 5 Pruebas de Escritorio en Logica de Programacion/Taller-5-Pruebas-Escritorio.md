# Taller 5: Pruebas de Escritorio en Lógica de Programación

**Asignatura:** Lógica de Programación

**Tema:** Metodología de la Prueba de Escritorio

**Basado en:** Lógica de programación, Omar Iván Trejos Buriticá (Capítulos 2.3 y 6.1.3)

**Estudiante:** Camilo Andres Pinilla Garcia

**Fecha de entrega:** 27/11/2026

## Parte 1: ¿Qué es una prueba de escritorio?

*Resumen de media página sobre qué es una prueba de escritorio y por qué es importante (basado en el libro). Cita al autor y explica con tus palabras para qué sirve.*

Hacer una prueba de escritorio es básicamente ponerse en los zapatos del computador para probar el algoritmo antes de pasarlo a código real. La idea es ir leyendo línea por línea, en estricto orden y sin adivinar qué va a pasar, mientras vas apuntando en una tabla cómo cambian los datos guardados y qué va saliendo en pantalla. Como dice Omar Iván Trejos Buriticá, este ejercicio es la forma más segura de comprobar si la solución que armaste realmente resuelve el problema o no.

Este paso vale oro porque te deja cazar fallos de lógica a tiempo, cuando arreglarlos solo cuesta borrar y volver a escribir en una hoja, en vez de perder horas peleando con código ya programado. Además, esa misma tabla te queda como registro de cómo se comporta el programa paso a paso y te señala justo dónde se daña si algo sale mal. Por eso el autor recalca que saltarse esta revisión convierte cualquier algoritmo en una lista de instrucciones a ciegas que ni siquiera sabes si tiene sentido.

Para llevarla a cabo solo te hace falta tener el pseudocódigo listo, una cuadrícula para ir anotando el valor de cada variable, un espacio aparte para simular lo que ve el usuario y algunos datos de prueba para meterle. La clave está en seguir las reglas al pie de la letra: nada de sacar conclusiones por cuenta propia, solo ejecutar lo que dice cada línea tal cual está escrita. Al terminar, si el resultado final no es el que esperabas, ya sabes que toca revisar y ajustar la lógica.

## Parte 2: Ejercicios resueltos

*Para cada ejercicio: elige los valores de entrada, completa la tabla de memoria y pantalla paso a paso, responde la pregunta y escribe tu conclusión (¿el algoritmo cumple el objetivo? ¿Sí o no? ¿Por qué?). Agrega o quita filas según los pasos que necesites.*

### Ejercicio 1: Área de un círculo

**Pseudocódigo**

```
Algoritmo Area_Circulo
Variables
    Real: radio, area
    Real: pi = 3.1416
Inicio
    Escriba "Digite el radio del círculo:"
    Lea radio
    area = pi * radio * radio
    Escriba "El área es: ", area
Fin
```

**Prueba de escritorio:** supongamos que el usuario ingresa radio = 5

| Paso | pi | radio | area | Pantalla |
| :--- | :--- | :--- | :--- | :--- |
| 1 | 3.1416 | - | - | - |
| 2 | 3.1416 | 5 | - | "Digite el radio del círculo:" |
| 3 | 3.1416 | 5 | 78.54 | - |
| 4 | 3.1416 | 5 | 78.54 | "El área es: 78.54" |



**Pregunta:** ¿El resultado coincide con el cálculo manual (π × r²)?

**respuesta:** si el resultado manual de (π × r²) = (3.1416 * 5²) = 78.54 y es el mismo que arroja el algoritmo


**Conclusión:** ¿El algoritmo cumple el objetivo? ¿Sí o no? ¿Por qué?

**respuesta:** Sí, el algoritmo cumple el objetivo. Pide el radio, aplica correctamente la fórmula del área del círculo (π × r²) y muestra el resultado.

### Ejercicio 2: Determinar el mayor de dos números

**Pseudocódigo**

```
Algoritmo Mayor_Dos_Numeros
Variables
    Entero: a, b
Inicio
    Escriba "Digite el primer número:"
    Lea a
    Escriba "Digite el segundo número:"
    Lea b
    Si a > b Entonces
        Escriba "El mayor es: ", a
    Sino
        Escriba "El mayor es: ", b
    Fin_Si
Fin
```

**Prueba de escritorio:** Caso 1: a = 10, b = 7

| Paso | a | b | a > b | Pantalla |
| :--- | :--- | :--- | :--- | :--- |
| 1 | 10 | - | - | "Digite el primer número:" |
| 2 | 10 | 7 | - | "Digite el segundo número:" |
| 3 | 10 | 7 | Verdadero | - |
| 4 | 10 | 7 | Verdadero | "El mayor es: 10" |

**Caso 2: a = 3, b = 12

| Paso | a | b | a > b | Pantalla |
| :--- | :--- | :--- | :--- | :--- |
| 1 | 3 | - | - | "Digite el primer número:" |
| 2 | 3 | 12 | - | "Digite el segundo número:" |
| 3 | 3 | 12 | Falso | - |
| 4 | 3 | 12 | Falso | "El mayor es: 12" |


**Preguntas**

**¿En ambos casos el algoritmo muestra el número correcto?**

**respuesta:**  Sí, en ambos casos muestra el resultado esperado **10 en el Caso 1** y **12 en el Caso 2**.
 
**¿Qué pasa si a = b?**

**respuesta:**  Como la condición a > b resulta **Falsa** cuando ambos números son iguales, el algoritmo ejecuta el bloque Sino y muestra el mensaje "El mayor es: " seguido del valor de b, a pesar de que ninguno es mayor que el otro.


**Conclusión:** ¿El algoritmo cumple el objetivo? ¿Sí o no? ¿Por qué?

**respuesta:** í, el algoritmo cumple el objetivo. Compara los dos números con la condición a > b y muestra el mayor en los dos casos probados.

### Ejercicio 3: Suma de los primeros N números

**Pseudocódigo**

```
Algoritmo Suma_N_Numeros
Variables
    Entero: n, i, suma
Inicio
    Escriba "Digite un número entero positivo:"
    Lea n
    suma = 0
    Para i = 1 Hasta n Hacer
        suma = suma + i
    Fin_Para
    Escriba "La suma de 1 a ", n, " es: ", suma
Fin
```

**Valores de entrada:** n = 5

**Prueba de escritorio:** Supongamos que n = 5

| Paso | n | i | suma | Pantalla |
| :--- | :--- | :--- | :--- | :--- |
| 1 | 5 | - | - | "Digite un número entero positivo:" |
| 2 | 5 | - | 0 | - |
| 3 | 5 | 1 | 1 | - |
| 4 | 5 | 2 | 3 | - |
| 5 | 5 | 3 | 6 | - |
| 6 | 5 | 4 | 10 | - |
| 7 | 5 | 5 | 15 | - |
| 8 | 5 | 5 | 15 | "La suma de 1 a 5 es: 15" |

**Preguntas**

 **¿El resultado es 15?**
  
  **respuesta:** Sí, al completar las 5 vueltas del ciclo Para, la variable suma acumula 1 + 2 + 3 + 4 + 5 = 15 y muestra "La suma de 1 a 5 es: 15".

 **¿Qué pasa si n = 1?**
  
  **respuesta:** El ciclo Para i = 1 Hasta 1 se ejecuta **una sola vez** con i = 1, calcula suma = 0 + 1 y muestra en pantalla "La suma de 1 a 1 es: 1".



**Conclusión:** ¿El algoritmo cumple el objetivo? ¿Sí o no? ¿Por qué?

**respuesta:** Sí, el algoritmo cumple el objetivo. Inicia el acumulador en 0, suma cada valor de i desde 1 hasta n y muestra el total. 


### Ejercicio 4: Contar números pares e impares en un vector

**Pseudocódigo**

```
Algoritmo Contar_Pares_Impares
Variables
    Entero: v[5], i, pares, impares
Inicio
    Para i = 1 Hasta 5 Hacer
        Escriba "Digite el número ", i, ":"
        Lea v[i]
    Fin_Para
    pares = 0
    impares = 0
    Para i = 1 Hasta 5 Hacer
        Si v[i] mod 2 = 0 Entonces
            pares = pares + 1
        Sino
            impares = impares + 1
        Fin_Si
    Fin_Para
    Escriba "Cantidad de pares: ", pares
    Escriba "Cantidad de impares: ", impares
Fin
```

### Prueba de escritorio
**Prueba de escritorio** Supongamos que el usuario ingresa v = [8, 3, 10, 7, 2]

**Valores de entrada:** v = [4, 7, 10, 3, 8]

| Paso | i | v[i] | pares | impares | v[i] mod 2 = 0 | Pantalla |
| :--- | :--- | :--- | :--- | :--- | :--- | :--- |
| 1 | 1 | 8 | - | - | - | "Digite el número 1:" |
| 2 | 2 | 3 | - | - | - | "Digite el número 2:" |
| 3 | 3 | 10 | - | - | - | "Digite el número 3:" |
| 4 | 4 | 7 | - | - | - | "Digite el número 4:" |
| 5 | 5 | 2 | - | - | - | "Digite el número 5:" |
| 6 | - | - | 0 | 0 | - | - |
| 7 | 1 | 8 | 1 | 0 | Verdadero | - |
| 8 | 2 | 3 | 1 | 1 | Falso | - |
| 9 | 3 | 10 | 2 | 1 | Verdadero | - |
| 10 | 4 | 7 | 2 | 2 | Falso | - |
| 11 | 5 | 2 | 3 | 2 | Verdadero | - |
| 12 | 5 | 2 | 3 | 2 | - | "Cantidad de pares: 3" |
| 13 | 5 | 2 | 3 | 2 | - | "Cantidad de impares: 2" |

### Respuesta a la pregunta

 **¿Cuántos pares e impares hay?**

 **respuesta:** Hay **3 números pares** (8, 10 y 2) y **2 números impares** (3 y 7).
  

**Conclusión:** ¿El algoritmo cumple el objetivo? ¿Sí o no? ¿Por qué?

**respuesta:** Sí, el algoritmo cumple el objetivo. Recorre los 5 elementos del vector y usa MOD 2 para decidir si cada uno es par o impar.
 


### Ejercicio 5: Validar contraseña con 3 intentos


**Pseudocódigo**

```
Algoritmo Login
Variables
    Carácter: password[10]
    Entero: intentos
    Lógico: acceso
Inicio
    intentos = 0
    acceso = Falso
    Mientras intentos < 3 Y NO acceso Hacer
        Escriba "Digite la contraseña:"
        Lea password
        Si password = "12345" Entonces
            acceso = Verdadero
        Sino
            intentos = intentos + 1
            Escriba "Contraseña incorrecta. Intento ", intentos, " de 3"
        Fin_Si
    Fin_Mientras
    Si acceso Entonces
        Escriba "Bienvenido"
    Sino
        Escriba "Cuenta bloqueada"
    Fin_Si
Fin
```

**Prueba de escritorio:** Caso 1: El usuario ingresa "12345" en el primer intento

| Paso | intentos | acceso | password | password = "12345" | Pantalla |
| :--- | :--- | :--- | :--- | :--- | :--- |
| 1 | 0 | Falso | - | - | - |
| 2 | 0 | Falso | "12345" | - | "Digite la contraseña:" |
| 3 | 0 | Verdadero | "12345" | Verdadero | - |
| 4 | 0 | Verdadero | "12345" | - | "Bienvenido" |

**Caso 2:** El usuario ingresa "111", "222", "333" (falla 3 veces)

| Paso | intentos | acceso | password | password = "12345" | Pantalla |
| :--- | :--- | :--- | :--- | :--- | :--- |
| 1 | 0 | Falso | - | - | - |
| 2 | 0 | Falso | "111" | - | "Digite la contraseña:" |
| 3 | 1 | Falso | "111" | Falso | "Contraseña incorrecta. Intento 1 de 3" |
| 4 | 1 | Falso | "222" | - | "Digite la contraseña:" |
| 5 | 2 | Falso | "222" | Falso | "Contraseña incorrecta. Intento 2 de 3" |
| 6 | 2 | Falso | "333" | - | "Digite la contraseña:" |
| 7 | 3 | Falso | "333" | Falso | "Contraseña incorrecta. Intento 3 de 3" |
| 8 | 3 | Falso | "333" | - | "Cuenta bloqueada" |

### Respuesta a la pregunta

 **Pregunta:** ¿Qué mensaje aparece en cada caso?

**respuesta** **Caso 1:** Muestra "Bienvenido" porque acceso cambia a **Verdadero** en el primer intento, haciendo que el ciclo Mientras termine inmediatamente.

**respuesta** **Caso 2:** Después de mostrar tres veces **"Contraseña incorrecta. Intento X de 3"**, la variable intentos llega a 3 (rompiendo la condición **intentos < 3**), sale del ciclo con acceso = Falso y muestra **Cuenta bloqueada**.


**Conclusión:** ¿El algoritmo cumple el objetivo? ¿Sí o no? ¿Por qué?

**respuesta** Sí, el algoritmo cumple el objetivo. El ciclo se repite mientras queden intentos y no se haya acertado, termina apenas la contraseña es correcta y bloquea la cuenta al fallar 3 veces.


## Reflexión final

Este taller logro resolver dudas acerca de las pruebas de escritorio desmotrandome que algo esta bien hecho hasta que se logra comprobar, tambien logre desenvolverme con ejercicios distintos, haciendo las distintas pruebas y los respectivos arreglos que se ocupaban.
