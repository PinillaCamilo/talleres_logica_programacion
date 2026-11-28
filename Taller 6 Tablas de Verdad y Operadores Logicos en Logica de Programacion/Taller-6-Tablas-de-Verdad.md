# Taller: Tablas de Verdad y Operadores Lógicos en Lógica de Programación

**Asignatura:** Lógica de Programación

**Tema:** Operadores Booleanos y Tablas de Verdad

**Basado en:** Lógica de programación, Omar Iván Trejos Buriticá (Capítulo 4.4.3)

**Estudiante:** Camilo Andres Pinilla Garcia

**Fecha de entrega:** 27-11-2026

## Parte 1: ¿Qué es una tabla de verdad?

Una tabla de verdad es una herramienta que sirve para mostrar de forma ordenada todos los resultados posibles que puede tener una expresión lógica, dependiendo de si sus condiciones iniciales son verdaderas (V) o falsas (F). Como explica Omar Iván Trejos Buriticá en su libro Lógica de programación (Capítulo 4.4.3), evaluar correctamente estas expresiones compuestas es clave dentro de la programación porque los algoritmos dependen de ellas para tomar decisiones (por ejemplo, en estructuras condicionales como Si-Entonces o ciclos Mientras). Construir una tabla de verdad antes de codificar nos permite comprobar la lógica de un programa y asegurarnos de que funcione bien en cualquier escenario.
Para armar y resolver estas expresiones se utilizan tres operadores lógicos básicos:
**Operador Y (Conjunción):** Une dos o más condiciones y exige que todas se cumplan al mismo tiempo. El resultado solo es verdadero cuando absolutamente todas las proposiciones son verdaderas; si al menos una falla, toda la expresión se vuelve falsa.
**Operador O (Disyunción):** Es mucho más flexible, ya que basta con que al menos una de las condiciones sea verdadera para que el resultado final sea verdadero. Solo arroja falso cuando todas las condiciones individuales son falsas.
**Operador NO (Negación):** A diferencia de los anteriores, actúa sobre una sola condición y simplemente invierte su valor lógico; es decir, convierte algo verdadero en falso y algo falso en verdadero.

## Parte 2: Ejercicios resueltos

*Para cada ejercicio: completa la tabla de verdad (V = Verdadero, F = Falso), escribe el pseudocódigo del algoritmo que evalúa la condición y redacta una breve conclusión indicando en qué casos la condición es Verdadera. Agrega o quita filas si lo necesitas.*

### Nivel Básico (operadores simples)

#### Ejercicio 1: Operador Y

**Condición:** `(edad >= 18) Y (tiene_licencia = Verdadero)`


| Caso | `edad >= 18` (P) | `tiene_licencia = Verdadero` (Q) | `P Y Q` (Resultado) | Pantalla |
| :--- | :---: | :---: | :---: | :--- |
| 1 | V | V | V | "Usted puede conducir" |
| 2 | V | F| f| "Usted no puede conducir" |
| 3 | F| V | f | "Usted no puede conducir" |
| 4 | F| F| f | "Usted no puede conducir" |

**Pseudocódigo**

```
Algoritmo puede_conducir
	Definir edad como entero
	Definir tiene_licencia Como Logico
	
	Escribir "Digite su edad"
	Leer edad
	Escribir "Tiene licencia (verdadero/falso)"
	Leer tiene_licencia
	
	si edad >= 18 Y tiene_licencia = Verdadero Entonces
		Escribir "Usted puede conducir"
	sino
		Escribir "Usted no puede conducir"
	FinSi
FinAlgoritmo

```

**Conclusión:** ¿En qué casos la condición es Verdadera?

La condición es Verdadera únicamente cuando se cumplen las dos condiciones a la vez.

#### Ejercicio 2: Operador O

**Condición:** `(dia = "sábado" (P) ) O (dia = "domingo" (Q) )`


**Tabla de verdad**

| dia = "sábado" `(P)` | dia = "domingo" `(Q)` | Resultado final `(PoQ)`|
| --- | --- | --- |
|v |v | v |
|v |f | v |
|f |v | v |
|f |f | f |

**Pseudocódigo**

```
Algoritmo fin_semana
	definir dia Como caracter
	
	Escribir "Que dia es hoy"
	Leer dia
	
	si (dia = "sabado") o (dia = "domingo") Entonces
		Escribir "Es fin de semana"
	SiNo
		Escribir "Es entre semana"
	FinSi
FinAlgoritmo
```

**Conclusión:** ¿En qué casos la condición es Verdadera?

La condición es Verdadera cuando al menos una de las dos comparaciones se cumple: si el día es sábado, si es domingo, Solo es Falsa cuando el día no es ni sábado ni domingo, es decir, de lunes a viernes.

#### Ejercicio 3: Operador NO

**Condición:** `NO (esta_lloviendo)`

**Tabla de verdad**

| esta_lloviendo | Resultado final  |
| --- | --- |
| F | V |
| V | F |

**Pseudocódigo**

```
Algoritmo esta_lloviendo
	Definir estaLloviendo Como Logico
	
	Escribir "¿Esta lloviendo? (verdaero/falso)"
	leer estaLloviendo
	si no (estaLloviendo) Entonces
		Escribir "Puede salir, no esta lloviendo"
	SiNo
		Escribir "Puede salir pero lleve sombrilla"
	FinSi
FinAlgoritmo
```

**Conclusión:** ¿En qué casos la condición es Verdadera?

La condición es Verdadera únicamente cuando estaLloviendo es Falso y es falsa cuando se dice que NO estaLloviendo.

#### Ejercicio 4: Combinación de Y con NO

**Condición:** `(tengo_dinero) Y NO (esta_cerrado)`

**Tabla de verdad**

| tengo_dinero | esta_cerrado | NO (esta_cerrado) | Resultado final |
| --- | --- | --- | --- |
| v | v | f | f |
| v | f | v | v |
| f | v | f | f |
| f | f | v | f |

**Pseudocódigo**

```
Algoritmo comprar_algo
	definir tengoDinero, estaCerrado Como Logico
	
	Escribir "¿Tiene dinero?(verdadero/falso)"
	Leer tengoDinero
	
	Escribir "¿La tienda esta cerrada? (verdero/falso)"
	Leer estaCerrado
	
	si (tengoDinero) y NO (estaCerrado) Entonces
		Escribir "Puede ir a comprar"
	SiNo
		Escribir "No vaya, esta cerrado"
	FinSi
FinAlgoritmo
```

**Conclusión:** ¿En qué casos la condición es Verdadera?

La condición es Verdadera únicamente cuando la persona tiene dinero y la tienda no está cerrada, es decir, cuando tengoDinero = Verdadero y estaCerrado = Falso (tercera fila de la tabla). En los otros casos el resultado es Falso

#### Ejercicio 5: Combinación de O con NO

**Condición:** `NO (tengo_tarea) O (es_fin_de_semana)`

**Tabla de verdad**

| tengo_tarea | es_fin_de_semana | NO (tengo_tarea) | Resultado final |
| --- | --- | --- | --- |
| v | v | f | v |
| v | f | f | f |
| f | v | v | v |
| f | f | v | v |

**Pseudocódigo**

```
Algoritmo jugar
	Definir tengoTarea, esFinSemana como logico
	
	Escribir "¿Tiene tarea?(verdadero/falso)"
	Leer tengoTarea
	Escribir "¿Es fin de semana?(verdadero/falso)?"
	Leer esFinSemana
	
	si NO (tengoTarea) o (esFinSemana) Entonces
		Escribir "Puede salir a jugar"
	SiNo
		Escribir "No puede salir a jugar"
	FinSi
FinAlgoritmo
```

**Conclusión:** ¿En qué casos la condición es Verdadera?

La condición es Verdadera cuando no hay tarea (tengo_tarea = Falso), cuando es fin de semana, o cuando se dan ambas cosas.

### Nivel Intermedio (condiciones compuestas)

#### Ejercicio 6: Acceso a un sistema

**Condición:** `password_correcta Y NO (cuenta_bloqueada)`

**Tabla de verdad**

| password_correcta | cuenta_bloqueada | NO (cuenta_bloqueada) | Resultado final |
| --- | --- | --- | --- |
| v | v | f | f |
| v | f | v | v |
| f | v | f | f |
| f | f | v | f |

**Pseudocódigo**

```
Algoritmo pasword
	Definir password_correcta, cuenta_bloqueada Como Logico
	
	Escribir "La contraseña es correcta?(verdadero/falso)"
	Leer password_correcta
	Escribir "Tiene la cuenta bloqueada?(verdadero/falso)"
	Leer cuenta_bloqueada
	
	si password_correcta y No (cuenta_bloqueada) Entonces
		Escribir "acceso permitido"
	SiNo
		Escribir "acceso denegado"
	FinSi
FinAlgoritmo

```
**Conclusión:** ¿En qué casos la condición es Verdadera?

La condición es Verdadera únicamente cuando la contraseña es correcta y la cuenta no está bloqueada.

#### Ejercicio 7: Descuento en una tienda

**Condición:** `(compra_mayor_100 Y cliente_frecuente) O compra_mayor_200`

**Tabla de verdad**

| compra_mayor_100 | cliente_frecuente | compra_mayor_200 | compra_mayor_100 Y cliente_frecuente | Resultado final |
| --- | --- | --- | --- | --- |
| v | v | v | v | v |
| v | v | f | v | v |
| v | f | v | f | v |
| v | f | f | f | f |
| f | v | v | f | v |
| f | v | f | f | f |
| f | f | v | f | v |
| f | f | f | f | f |

**Pseudocódigo**

```
Algoritmo descuento
	Definir compra_mayor_100, cliente_frecuente, compra_mayor_200 Como Logico
	
	Escribir "la compra es mayor a 100? (verdadero/falso)"
	leer compra_mayor_100
	Escribir "usted es un cliente frecuente?(verdadero/falso)"
	Leer cliente_frecuente
	Escribir "la compra es mayor a 200?(verdadero/falso)"
	Leer compra_mayor_200
	
	si (compra_mayor_100 y cliente_frecuente) o compra_mayor_200 Entonces
		Escribir "se aplica descuento"
	SiNo
		Escribir "No se le aplica ningun descuento"
	FinSi
	
FinAlgoritmo
```

**Conclusión:** ¿En qué casos la condición es Verdadera?

La condición es Verdadera en dos situaciones: cuando la compra es mayor a $200, sin importar lo demás, o cuando la compra es mayor a $100 y además el cliente es frecuente . En los otros casos el resultado es Falso. 

#### Ejercicio 8: Aprobación de un crédito

**Condición:** `(ingresos_mayores_1000 Y sin_deudas) O tiene_fiador`

**Tabla de verdad**


| ingresos_mayores_1000 | sin_deudas | tiene_fiador | ingresos_mayores_1000 Y sin_deudas | Resultado final |
| --- | --- | --- | --- | --- |
| v | v | v | v | v |
| v | v | f | v | v |
| v | f | v | f | v |
| v | f | f | f | f |
| f | v | v | f | v |
| f | v | f | f | f |
| f | f | v | f | v |
| f | f | f | f | f |

**Pseudocódigo**

```
Algoritmo AprobarCredito
	Definir ingresos_mayores_1000, sin_deudas, tiene_fiador Como Logico
	
	Escribir "Tiene ingresos mayores a $1000? (Verdadero/Falso):"
	Leer ingresos_mayores_1000
	Escribir "Está libre de deudas? (Verdadero/Falso):"
	Leer sin_deudas
	Escribir "Tiene fiador? (Verdadero/Falso):"
	Leer tiene_fiador
	
	Si (ingresos_mayores_1000 Y sin_deudas) O tiene_fiador Entonces
		Escribir "su crédito fue aprobado."
	SiNo
		Escribir "su crédito fue rechazado."
	FinSi
FinAlgoritmo
```

**Conclusión:** ¿En qué casos la condición es Verdadera?

La condición es Verdadera en dos situaciones: cuando el solicitante tiene fiador, sin importar sus ingresos o deudas, o cuando tiene ingresos mayores a $1000 y además no tiene deudas. En los otros casos el resultado es Falso y el crédito se rechaza.


#### Ejercicio 9: Validación de un triángulo

**Condición:** `(a + b > c) Y (a + c > b) Y (b + c > a)`

**Tabla de verdad**

| a + b > c | a + c > b | b + c > a | Resultado final |
| --- | --- | --- | --- |
| v | v | v | v |
| v | v | f | f |
| v | f | v | f |
| v | f | f | f |
| f | v | v | f |
| f | v | f | f |
| f | f | v | f |
| f | f | f | f |


**Pseudocódigo**

```
Algoritmo ValidarTriangulo
	Definir a, b, c Como Real
	
	Escribir "Digite el lado a"
	Leer a
	Escribir "Digite el lado b"
	Leer b
	Escribir "Digite el lado c"
	Leer c
	
	Si (a + b > c) Y (a + c > b) Y (b + c > a) Entonces
		Escribir "Los lados forman un triángulo."
	SiNo
		Escribir "Los lados no forman un triángulo."
	FinSi
	
FinAlgoritmo
```

**Conclusión:** ¿En qué casos la condición es Verdadera?

La condición es Verdadera únicamente cuando las tres desigualdades se cumplen a la vez, la suma de cada par de lados debe ser mayor que el lado restante. Si alguna de las tres falla, el resultado es Falso y los lados no forman un triángulo.


#### Ejercicio 10: Clasificación de un número

**Condición:** `(es_positivo Y es_par) O (es_negativo Y es_impar)`

**Tabla de verdad**

| es_positivo | es_par | es_negativo | es_impar | es_positivo Y es_par | es_negativo Y es_impar | Resultado final |
| --- | --- | --- | --- | --- | --- | --- |
| v | v | v | v | v | v | v |
| v | v | v | f | v | f | v |
| v | v | f | v | v | f | v |
| v | v | f | f | v | f | v |
| v | f | v | v | f | v | v |
| v | f | v | f | f | f | f |
| v | f | f | v | f | f | f |
| v | f | f | f | f | f | f |
| f | v | v | v | f | v | v |
| f | v | v | f | f | f | f |
| f | v | f | v | f | f | f |
| f | v | f | f | f | f | f |
| f | f | v | v | f | v | v |
| f | f | v | f | f | f | f |
| f | f | f | v | f | f | f |
| f | f | f | f | f | f | f |

**Pseudocódigo**

```
Algoritmo Numero_Especial
	Definir num Como Entero
	Definir es_positivo, es_par, es_negativo, es_impar Como Logico
	
	Escribir "Digite un número entero"
	Leer num
	
	es_par <- (num MOD 2 = 0)
	es_impar <- (num MOD 2 <> 0)
	es_positivo <- num > 0
	es_negativo <- num < 0
	
	
	Si (es_positivo Y es_par) O (es_negativo Y es_impar) Entonces
		Escribir "El número es especial"
	SiNo
		Escribir "El número no es especial"
	FinSi
FinAlgoritmo
```

**Conclusión:** ¿En qué casos la condición es Verdadera?

La condición es Verdadera cuando el número es positivo y par, o cuando es negativo e impar (filas 4, 8, 12, 13, 14, 15 y 16 de la tabla). En los demás casos es Falsa: por ejemplo, un positivo impar, un negativo par o el cero.


### Nivel Avanzado (aplicación en algoritmos)


#### Ejercicio 11: Sistema de inicio de sesión con múltiples condiciones

**Condición:** `usuario_correcto Y password_correcta Y NO (cuenta_bloqueada) Y (correo_verificado O telefono_verificado)`

**Tabla de verdad**


| usuario_correcto Y password_correcta | NO (cuenta_bloqueada) | correo_verificado O telefono_verificado | Resultado final |
| --- | --- | --- | --- |
| v | v | v | v |
| v | v | f | f |
| v | f | v | f |
| v | f | f | f |
| f | v | v | f |
| f | v | f | f |
| f | f | v | f |
| f | f | f | f |


**Pseudocódigo**

```
Algoritmo Inicio_Sesion
	Definir usuario_correcto, password_correcta, cuenta_bloqueada Como Logico
	Definir correo_verificado, telefono_verificado Como Logico
	
	Escribir "La cuenta está bloqueada? (Verdadero/Falso)"
	Leer cuenta_bloqueada
	
	Escribir "¿Verificó su correo? (Verdadero/Falso)"
	Leer correo_verificado
	
	Escribir "Verificó su teléfono? (Verdadero/Falso)"
	Leer telefono_verificado
	
	Escribir "El usuario es correcto? (Verdadero/Falso)"
	Leer usuario_correcto
	
	Escribir "La contraseña es correcta? (Verdadero/Falso)"
	Leer password_correcta
	
	Si usuario_correcto Y password_correcta Y NO (cuenta_bloqueada) Y (correo_verificado O telefono_verificado) Entonces
		Escribir "Inicio de sesión exitoso"
	SiNo
		Escribir "No puede iniciar sesión"
	FinSi
FinAlgoritmo
```

**Conclusión:** ¿En qué casos la condición es Verdadera?

La condición es Verdadera únicamente cuando se cumplen las tres partes a la vez, el usuario y la contraseña son correctos, la cuenta no está bloqueada y el usuario verificó al menos uno de los dos medios (correo o teléfono). Si falla cualquiera de las tres, el resultado es Falso.


#### Ejercicio 12: Elegibilidad para una beca

**Condición:** `(promedio_ge_8_5 Y sin_reprobadas) O (promedio_ge_9_0 Y tiene_publicaciones)`

**Tabla de verdad**

| promedio_ge_8_5 | sin_reprobadas | promedio_ge_9_0 | tiene_publicaciones | Resultado final |
| --- | --- | --- | --- | --- |
| v | v | v | v | v |
| v | v | v | f | v |
| v | v | f | v | v |
| v | v | f | f | v |
| v | f | v | v | v |
| v | f | v | f | f |
| v | f | f | v | f |
| v | f | f | f | f |
| f | v | v | v | v |
| f | v | v | f | f |
| f | v | f | v | f |
| f | v | f | f | f |
| f | f | v | v | v |
| f | f | v | f | f |
| f | f | f | v | f |
| f | f | f | f | f |

**Pseudocódigo**

```
Algoritmo Beca_Estudiante
	Definir promedio Como Real
	Definir reprobadas, publicaciones Como Entero
	Definir promedio_ge_8_5, sin_reprobadas, promedio_ge_9_0, tiene_publicaciones Como Logico
	
	promedio_ge_8_5 <- promedio >= 8.5
	sin_reprobadas <- reprobadas = 0
	promedio_ge_9_0 <- promedio >= 9.0
	tiene_publicaciones <- publicaciones >= 2
	
	Escribir "Digite el promedio del estudiante"
	Leer promedio
	
	Escribir "Digite la cantidad de materias reprobadas"
	Leer reprobadas
	
	Escribir "Digite la cantidad de publicaciones"
	Leer publicaciones
	
	Si (promedio_ge_8_5 Y sin_reprobadas) O (promedio_ge_9_0 Y tiene_publicaciones) Entonces
		Escribir "El estudiante es elegible para la beca"
	SiNo
		Escribir "El estudiante no es elegible para la beca"
	FinSi
FinAlgoritmo
```

**Conclusión:** ¿En qué casos la condición es Verdadera?

La condición es Verdadera en dos situaciones: cuando el promedio es mayor o igual a 8.5 y no hay materias reprobadas, o cuando el promedio es mayor o igual a 9.0 y hay al menos 2 publicaciones. En las demás filas el resultado es Falso.


#### Ejercicio 13: Control de acceso a una sala VIP

**Condición:** `(tiene_invitacion Y es_mayor) O (es_socio Y NO (acompanado_menores))`

**Tabla de verdad**

| tiene_invitacion | es_mayor | es_socio | acompanado_menores | Resultado final |
| --- | --- | --- | --- | --- |
| v | v | v | v | v |
| v | v | v | f | v |
| v | v | f | v | v |
| v | v | f | f | v |
| v | f | v | v | f |
| v | f | v | f | v |
| v | f | f | v | f |
| v | f | f | f | f |
| f | v | v | v | f |
| f | v | v | f | v |
| f | v | f | v | f |
| f | v | f | f | f |
| f | f | v | v | f |
| f | f | v | f | v |
| f | f | f | v | f |
| f | f | f | f | f |

**Pseudocódigo**

```
Algoritmo VerificarAcceso
    Definir tiene_invitacion, es_mayor, es_socio, acompanado_menores Como Logico
	
    Escribir "Tiene invitación? (Verdadero/Falso)"
    Leer tiene_invitacion
    Escribir "Es mayor de edad? (Verdadero/Falso)"
    Leer es_mayor
    Escribir "Es socio? (Verdadero/Falso)"
    Leer es_socio
    Escribir "Viene acompañado de menores? (Verdadero/Falso)"
    Leer acompanado_menores
	
    Si (tiene_invitacion Y es_mayor) O (es_socio Y NO (acompanado_menores)) Entonces
        Escribir "Acceso permitido"
    SiNo
        Escribir "Acceso denegado"
    FinSi
FinAlgoritmo
```

**Conclusión:** ¿En qué casos la condición es Verdadera?

La condición es Verdadera en dos situaciones: cuando la persona tiene invitación y es mayor de edad, o cuando es socio y no viene acompañado de menores. En las demás filas el resultado es Falso.


#### Ejercicio 14: Validación de una contraseña segura

**Condición:** `longitud_ok Y tiene_mayuscula Y tiene_numero Y tiene_especial`

**Tabla de verdad**


| longitud_ok | tiene_mayuscula | tiene_numero | tiene_especial | Resultado final |
| --- | --- | --- | --- | --- |
| v | v | v | v | v |
| v | v | v | f | f |
| v | v | f | v | f |
| v | v | f | f | f |
| v | f | v | v | f |
| v | f | v | f | f |
| v | f | f | v | f |
| v | f | f | f | f |
| f | v | v | v | f |
| f | v | v | f | f |
| f | v | f | v | f |
| f | v | f | f | f |
| f | f | v | v | f |
| f | f | v | f | f |
| f | f | f | v | f |
| f | f | f | f | f |

**Pseudocódigo**

```
Algoritmo ValidarContrasena
    Definir longitud_ok, tiene_mayuscula, tiene_numero, tiene_especial Como Logico
	
    Escribir "Tiene longitud adecuada? (Verdadero/Falso)"
    Leer longitud_ok
    Escribir "Tiene al menos una mayúscula? (Verdadero/Falso)"
    Leer tiene_mayuscula
    Escribir "Tiene al menos un número? (Verdadero/Falso)"
    Leer tiene_numero
    Escribir "Tiene al menos un carácter especial? (Verdadero/Falso)"
    Leer tiene_especial
	
    Si longitud_ok Y tiene_mayuscula Y tiene_numero Y tiene_especial Entonces
        Escribir "Contraseña segura"
    SiNo
        Escribir "Contraseña insegura"
    FinSi
FinAlgoritmo
```

**Conclusión:** ¿En qué casos la condición es Verdadera?

La condición es Verdadera en una única situación: cuando la contraseña cumple con la longitud adecuada, tiene al menos una letra mayúscula, tiene al menos un número y tiene al menos un carácter especial al mismo tiempo. En las demás filas el resultado es Falso.

#### Ejercicio 15: Sistema de alerta de temperatura

**Condición:** `(temp_mayor_40 Y humedad_mayor_80) O (temp_menor_0 Y viento_fuerte)`

**Tabla de verdad**


| temp_mayor_40 | humedad_mayor_80 | temp_menor_0 | viento_fuerte | Resultado final |
| --- | --- | --- | --- | --- |
| v | v | v | v | v |
| v | v | v | f | v |
| v | v | f | v | v |
| v | v | f | f | v |
| v | f | v | v | v |
| v | f | v | f | f |
| v | f | f | v | f |
| v | f | f | f | f |
| f | v | v | v | v |
| f | v | v | f | f |
| f | v | f | v | f |
| f | v | f | f | f |
| f | f | v | v | v |
| f | f | v | f | f |
| f | f | f | v | f |
| f | f | f | f | f |

**Pseudocódigo**

```
Algoritmo Alerta_Temperatura
	Definir temperatura, humedad Como Real
	Definir viento_fuerte Como Logico
	Definir temp_mayor_40, humedad_mayor_80, temp_menor_0 Como Logico
	
	temp_mayor_40 <- temperatura > 40
	humedad_mayor_80 <- humedad > 80
	temp_menor_0 <- temperatura < 0
	
	Escribir "Digite la temperatura en °C"
	Leer temperatura
	Escribir "Digite la humedad en %"
	Leer humedad
	Escribir "¿Hay viento fuerte?(Verdadero/Falso)"
	Leer viento_fuerte
	
	Si (temp_mayor_40 Y humedad_mayor_80) O (temp_menor_0 Y viento_fuerte) Entonces
		Escribir "Alarma activada"
	SiNo
		Escribir "Alarma desactivada"
	FinSi
FinAlgoritmo
```

**Conclusión:** ¿En qué casos la condición es Verdadera?

La condición es Verdadera en dos situaciones: cuando la temperatura es mayor a 40 °C y la humedad mayor al 80%, o cuando la temperatura es menor a 0 °C y hay viento fuerte. En las demás filas el resultado es Falso y la alarma no se activa.

## Reflexión final

Al hacer estas tablas de verdad aprendí a entender mucho mejor cómo se combinan los operadores lógicos (Y, O y NO) y cómo un simple paréntesis puede cambiar todo el resultado. Creo que son súper importantes a la hora de escribir condiciones en los algoritmos porque te permiten ver todos los casos posibles antes de ponerte a programar, evitando errores de lógica o que el programa tome decisiones raras según lo que ingrese el usuario.

