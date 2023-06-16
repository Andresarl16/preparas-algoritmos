# Preparadurías Taller de Python

**Preparador:** Andrés Rojas

# Contenido

- [Preparaduría 1](#preparaduría-1)
  - [Indentacion](#indentacion)
  - [Escritura de Informacion](#escritura-de-informacion)
  - [Comentarios](#comentarios)
  - [Variables](#variables)
  - [Tipos de Datos](#tipos-de-datos)
  - [Operadores](#operadores)
    - [Operadores Aritmeticos](#operadores-aritmeticos)
    - [Operadores de Asignacion](#operadores-de-asignacion)
    - [Operadores de Comparacion](#operadores-de-comparacion)
    - [Operadores Logicos](#operadores-logicos)
    - [Operadores de Identidad](#operadores-de-identidad)
    - [Operadores de Membresia](#operadores-de-membresia)
  - [Lectura de Informacion](#lectura-de-informacion)
  - [Formato de Cadenas](#formato-de-cadenas)
  - [Ejercicios](#ejercicios)
    - [Ejercicio 1](#ejercicio-1)
    - [Ejercicio 2 (Tarea)](#ejercicio-2-tarea)
    - [Ejercicio 3 (Tarea)](#ejercicio-3-tarea)
    - [Ejercicio 4 (Tarea)](#ejercicio-4-tarea)
    - [Ejercicio 5 (Tarea)](#ejercicio-5-tarea)

# Preparaduría 1

## Mostrar Informacion

Podemos _imprimir_ en la consola con **print()** como se muestra en el siguiente ejemplo:

**Código**

```python
print("Hello world!")
```

**Output**

```shell
Hello world!
```

Además, al momento de imprimir información podemos concatenar cadenas con **+**

**Código**

```python
print("Hello" + " world" + "!")
```

**Output**

```shell
Hello world!
```

## Comentarios

Los comentarios nos ayudan a describir nuestro código y su funcionamiento, de esta forma nuestro codigo llega a ser mas _legible_. Por otro lado, tambien podemos utilizar los comentarios para evitar que python ejecute partes de nuestro código.

Existen dos tipos de comentarios:

- Los comentarios de una única línea que se simbolizan utilizando _#_
- Los comentarios multilínea que se inician y terminan utilizando _"""_

**Código**

```python
# Esto es un comentario de una linea
"""
Esto es
un comentario
multilinea
"""
print("Hello world!") # Se imprimira por consola
#print ("Algoritmos") # No se imprimira por consola
```

**Output**

```shell
Hello world
```

## Tipos de Datos

Las variables pueden almacenar diferentes tipos de datos, como por ejemplo:
| Tipo | Clase | Ejemplo |
| ----------- | ----------- | ------------------------------------------------- |
| str | Cadena | "Hello" o 'Hello' |
| int | Entero | 11 |
| long | Entero | 11 |
| float | Decimal | 11.5 |
| complex | Complejo | 1j |
| bool | Booleano | True, False |
| list | Secuencia | ["1", "2", "3"] |
| tuple | Secuencia | ("1", "2", "3") |
| dict | Diccionario | {"nombre" : "Andrés", "apellido" : "Rojas"} |
| set | Conjunto | {"1", "2", "3"} |

Si deseamos conocer el tipo de dato de alguna variable podemos usar **type()**

**Código**

```python
numero_2 = 50 #Tipo entero (int)
print(type(numero_2))

```

**Output**

```shell
<class 'int'>
```

Pueden leer un poco mas sobre los tipos de datos en python en este link: https://eiposgrados.com/blog-python/tipos-de-datos-de-python/

## Casting

El Cast o Casting es la acción de convertir un tipo de dato a otro, existen dos tipos de conversiones:

- Conversiones implícitas: Son realizadas automáticamente por python.

**Código**

```python
a = 1   # <class 'int'>
b = 2.3 # <class 'float'>

a = a + b
print(a)
print(type(a))

```

**Output**

```shell
3.3
<class 'float'>
```

- Conversiones explícitas: Son realizadas de forma manual por nosotros.

```python
a = 3.5
print(type(a))
a = str(a)
print(type(a))
```

**Output**

```shell
<class 'float'>
<class 'str'>
```

En la siguiente tabla se muestran algunos ejemplos de casteos

| Casteo  | Tipo de Dato Resultante |
| ------- | ----------------------- |
| int()   | int                     |
| float() | float                   |
| str()   | string                  |
| list()  | list                    |
| set()   | set                     |

## Variables

Las variables nos servirán para guardar información durante la ejecución del código. A diferencia de otros lenguajes, python no requiere indicar el tipo de dato que se guardará en una variable. Ademas, permite cambiar el tipo de dato de la variable en cualquier momento

```python
numero_1 = 10 #Tipo entero (int)
numero_1 = ' 10 ' #Tipo cadena (str)
numero_1 = " 10 " #Tipo cadena (str)
```

Además, podemos crear mas de una variable en una misma linea de codigo

**Código**

```python
x, y = 1, 2
print(x)
print(y)
```

**Output**

```shell
1
2
```

Igualmente, le podemos asignar el mismo valor a distintas variables

**Código**

```python
x = y = 1
print(x)
print(y)
```

**Output**

```shell
1
1
```

Los nombres de variables tienen las siguientes características:

- Son sensibles a mayusculas y minusculas. (VARIABLE ≠ variable)
- Su nombre debe comenzar con una letra o un \_
- Su nombre solo puede contener contener letras, numeros o \_

Además hay buenas prácticas que se deben seguir al momento de nombrar variables

- Los nombres de las variables deben ser descriptivos y significativos
- En _Python_, se acostumbra a nombrar las variables utilizando _snake case_, lo que significa que se deben utilizar únicamente letras minúsculas y separar las palabras con guiones (ejemplo_de_nombre)

## Operadores

Utilizaremos los operadores para realizar diferentes operaciones sobre la informacion

### Operadores Aritmeticos

| Operador | Operacion           | Ejemplo  |
| -------- | ------------------- | -------- |
| +        | Suma                | x + y    |
| -        | Resta               | x - y    |
| \*       | Multiplicacion      | x \* y   |
| /        | Division            | x / y    |
| %        | Resto               | x % y    |
| \*\*     | Exponenciación      | x \*\* y |
| //       | Division redondeada | x // y   |

### Operadores de Asignacion

| Operador | Ejemplo   | Lo mismo que... |
| -------- | --------- | --------------- |
| =        | x = 1     | x = 1           |
| +=       | x += 1    | x = x + 1       |
| -=       | x -= 1    | x = x - 1       |
| \*=      | x \*= 1   | x = x \* 1      |
| /=       | x /= 1    | x = x / 1       |
| %=       | x %= 1    | x = x % 1       |
| \*\*=    | x \*\*= 1 | x = x \*\* 1    |
| //=      | x //= 1   | x = x // 1      |

### Operadores de Comparacion

| Operador | Comparacion       | Ejemplo |
| -------- | ----------------- | ------- |
| ==       | Igual             | x == y  |
| !=       | No igual          | x != y  |
| >        | Mayor que         | x > y   |
| <        | Menor que         | x < y   |
| >=       | Mayor o igual que | x >= y  |
| <=       | Menor o igual que | x <= y  |

### Operadores Lógicos

| Operador | Explicacion                                         | Ejemplo           |
| -------- | --------------------------------------------------- | ----------------- |
| and      | Verdadero si ambas condiciones son verdaderas       | x == y and x == z |
| or       | Verdadero si una o ambas condiciones son verdaderas | x == y or x == z  |
| not      | Verdadero si la condicion es falsa                  | not(x == y)       |

### Operadores de Identidad

| Operador | Explicacion                                             | Ejemplo    |
| -------- | ------------------------------------------------------- | ---------- |
| is       | Verdadero si ambas variables son el mismo objeto        | x is y     |
| is not   | Verdadero si ambas variables **no** son el mismo objeto | x is not y |

### Operadores de Membresia

| Operador | Explicacion                                | Ejemplo    |
| -------- | ------------------------------------------ | ---------- |
| in       | Verdadero si esta presente en el objeto    | x in y     |
| not in   | Verdadero si no esta presente en el objeto | x not in y |

## Lectura de Informacion

Utilizaremos **input()** para solicitarle informacion al usuario

**Código**

```python
numero = input("Ingrese un numero por favor") #Imaginemos que el usuario ingresa 73
print(numero)

```

**Output**

```shell
73
```

## Formato de Cadenas

Podemos usar **format()** para _editar_ una cadena

**Código**

```python
nombre = "Andrés"
apellido = "Rojas"
cargo = "preparador"
nro_prepa = 1
saludo = "Hola soy su {}, mi nombre es {} {} y esta es nuestra prepa nro {:.2f}."
print(saludo.format(cargo, nombre, apellido, nro_prepa))

```

**Output**

```shell
Hola soy su preparadora, mi nombre es Andrés Rojas y esta es nuestra prepa nro 1.00.
```

Pueden leer más sobre el uso de **format()** en este link: https://www.w3schools.com/python/python_string_formatting.asp

## Ejercicios

### Ejercicio 1

Escribir un programa que le pida al usuario la siguiente informacion: _nombre_, _apellido_, _edad_ (cada dato debe estar en una variable distinta). Luego, muestre por pantalla:

**Output**

```shell
¡Hola soy (nombre) (apellido) y tengo (edad) años de edad.
```

Cada dato debe ser el que haya sido introducido por el usuario.

### Ejercicio 2

Escribir un programa que le pida al usuario el _precio de un artículo_ y la _cantidad de unidades_ compradas. Posteriormente, debe mostrar por pantalla el subtotal que debe pagar por los n artículos (monto sin iva), el iva (16%) y el total (monto con iva).

**Output**

```shell
Numero de articulos: (número de articulos)
Precio por unidad: (precio unitario)
El subtotal de la compra es de (subtotal), con un iva de (iva), lo que genera un monto total de (total).
```

### Ejercicio 3

Escribir un programa que pida al usuario su **peso** (en kg) y **estatura** (en metros), y que luego calcule el **índice de masa corporal** del usuario y que muestre por pantalla:

**Output**

```shell
Peso: (peso)kg
Estatura: (estatura)m
Tu índice de masa corporal es (índice de masa corporal).
```

La fórmula para calcular el índice de masa corporal es peso/(altura^2).

### Ejercicio 4

Escribir un programa que le pida al usuario _dos números_ y que imprima por pantalla:

**Output**

```shell
Numero 1: (numero 1)
Numero 2: (numero 2)
La suma de los dos números es: (suma).
La resta de los dos números es: (resta).
La multiplicación de los dos números es: (multiplicación).
La división de los dos números es: (división).
```

## If, elif y else

Las sentencias _If_ nos permiten ejecutar bloques de codigo de acuerdo a si una condicion es **verdadera**.

```python
numero = int(input("Ingrese un número"))
if (numero == 0):
  print("El número es 0")
```

Por otro lado, la sentencia _elif_ nos servirá para considerar múltiples casos al momento de realizar condiconales. Finalmente, si no se cumple **ningun caso**, entonces se ejecutara lo que este dentro de la sentencia _else_ (en caso de existir).

```python
numero = int(input("Ingrese un numero"))
if (numero == 0):
  print("El numero es cero")
elif (numero > 0):
    print("El numero es positivo")
else:
  print("El numero es negativo")
```

## Indentacion

Son los espacios al comienzo de cada línea de nuestro código, de esta manera python reconoce los bloques de codigo. Una forma sencilla de reconocer en que situaciones debemos indentar nuestro código, es identificar las líneas que terminan con _:_.

**Código**

```python
if True:
	print("Hello world")
```

**Output**

```shell
Hello world
```

En el codigo anterior python entiende que si se cumple la condicion del _if_, entonces debe ejecutar el bloque de codigo que esta **adentro** de este _if_. Se debe usar la misma cantidad de espacios en el mismo bloque de código, de lo contrario tu codigo puede fallar.

**Código**

```python
if True:
print("Hello world")
```

**Output**

```shell
File "main.py", line 2
    print("Hello world")
    ^
IndentationError: expected an indented block
```

**Código**

```python
if True:
    print("Hello")
        print("world")
```

**Output**

```shell
File "main.py", line 3
    print("world")
IndentationError: unexpected indent
```

En estos dos últimos bloques de código se generan errores por la falta de indentación como es en el primer caso, o por la inconsistencia de la misma como en el segundo.

### Ejercicio 5

Escribir un programa que le pida al usuario dos números y la operación que desea realizar, para esto se le debe mostrar un menú con los números equivalentes a cada una de las opciones.

**Output**

```shell
El primer número es: (numero 1)
El segundo número es: (numero 2)
Y el resultado de la (operación) es: (resultado)
```

## While

Con while podemos ejecutar el mismo bloque de codigo _una y otra vez_, siempre que una condición sea **verdadera**.

```python
print('Inicia el programa')
cadena = ''
while (cadena != '10'):
    cadena = input("Ingrese el numero 10: ")
print('Termina el programa')
```

Tenemos que tener cuidado al usar los while ya que podemos generar un **bucle infinito**. Si corren el siguiente codigo, veran que el programa nunca saldra del bucle.

```python
print('Inicia el programa')
num = 0
while (num >= 0):
    print(num)
    num += 1
print('Termina el programa')
```

Tambien tenemos otra forma de finalizar un while,podemos usar _break_ para esto:

```python
print('Inicia el programa')
num = 0
while (num >= 0):
    print(num)
    num += 1
    if (num == 10):
      break
print('Termina el programa')
```

Ademas, si queremos saltar una ejecucion del while podemos usar _continue_. Si corren el siguiente codigo podran ver que el numero 5 no se va a imprimir:

```python
print('Inicia el programa')
num = 0
while (num < 10):
    num += 1
    if(num == 5):
      continue
    print(num)
print('Termina el programa')
```

## Listas

Las listas nos permiten almacenar varios elementos en una misma variable y se crean usando **corchetes**.

**Código**

```python
listaDeNombres = ["Andres", "Laura", "Luis"]
print(listaDeNombres)
```

**Output**

```shell
['Andres', 'Laura', 'Luis']
```

Tambien podemos crear una lista usando **list()**:

```python
listaDeNombres = list(("Andres", "Laura", "Luis"))
print(listaDeNombres)
print(listaDeNombres[1]) #Laura
print(listaDeNombres[-1]) #Luis
```

Podemos generar otra lista con un **rango de indices** indicando dónde comenzar y dónde terminar. El valor devuelto será una _nueva lista_ con los elementos especificados.

**Código**

```python
listaDeNombres = ["Andres", "Laura", "Luis", "Rommel", "Andrea"] # Indices: 0 1 2 3 4
print(listaDeNombres[1:4]) # 1 2 3
print(listaDeNombres[:4]) # 0 1 2 3
```

**Output**

```shell
['Laura', 'Luis', 'Rommel']
['Andres','Laura', 'Luis', 'Rommel']
['Luis', 'Rommel']
```

Podemos usar **in** para saber si un elemento esta en la lista.

```python
listaDeNombres = ["Andres", "Laura", "Luis", "Rommel", "Andrea"] # Indices: 0 1 2 3 4
if "Luis" in listaDeNombres:
  print("Luis esta en la lista de nombres")
else:
  print("Luis no esta en la lista de nombres")
```

Si queremos cambiar un elemento de la lista podemos hacerlo mediante los indices:

**Código**

```python
listaDeNombres = ["Andres", "Laura", "Luis", "Rommel", "Andrea"] # Indices: 0 1 2 3 4
listaDeNombres[1] = "Sofia"
print(listaDeNombres)
```

**Output**

```shell
['Andres', 'Sofia', 'Luis', 'Rommel', 'Andrea']
```

### Caracteristicas de las listas

- Las listas permiten valores repetidos.
- Los elementos de la lista están ordenados (los elementos tienen un orden definido y ese orden "no" cambiará.).
- Los elementos de la lista pueden ser cambiados (podemos cambiar, agregar y eliminar elementos de la lista).
- Los elementos de la lista están indexados, esto quiere decir que el primer elemento tiene índice [0], el segundo elemento tiene índice [1]...
- Los elementos de la lista pueden ser de cualquier tipo de dato, aunque es preferible no mezclar distintos tipos de datos en una misma lista.

### Metodos de listas

| Metodo    | Explicacion                                                                         |
| --------- | ----------------------------------------------------------------------------------- |
| len()     | Indica el tamaño de la lista                                                        |
| append()  | Agrega un elemento al final de la lista                                             |
| clear()   | Vacia la lista (elimina todos los elementos)                                        |
| copy()    | Crea una copia de la lista                                                          |
| count()   | Indica el numero de elementos en la lista con el valor indicado                     |
| extend()  | Agrega los elementos de una lista(o cualquier iterable) al final de la lista actual |
| index()   | Devuelve el índice del primer elemento con el valor especificado                    |
| insert()  | Agrega un elemento a la lista en la posición indicada                               |
| pop()     | Elimina el elemento de la posición indicada (por defecto es el ultimo elemento)     |
| remove()  | Elimina el elemento con el valor indicado                                           |
| reverse() | Invierte el orden de la lista                                                       |
| sort()    | Ordena la lista                                                                     |

Si quieren investigar un poco mas sobre estos metodos:
['List Methods'](https://www.w3schools.com/python/python_lists_methods.asp)

### Matriz (Lista de listas)

Con las listas podemos crear matrices, que en verdad serian listas de listas.

**Código**

```python
matriz = [[1,2,3], [4,5,6], [7,8,9]]
print(matriz)
print(matriz[2][1])
```

**Output**

```shell
[[1, 2, 3], [4, 5, 6], [7, 8, 9]]
8
```

## For

Usamos **for** para iterar sobre una secuencia (lista, tupla, diccionario, conjunto o cadena). De esta forma podemos ejecutar un bloque de codigo una vez por cada elemento de la secuencia o de acuerdo a un rango.

**Código**

```python
listaDeNumeros = [1, 70, 3, 7, 6]
for numero in listaDeNumeros:
  print(numero)
```

**Output**

```shell
1
70
3
7
6
```

Podemos recorrer cadenas con **for**:

**Código**

```python
cadena = "Hello"
for letra in cadena:
  print(letra)
```

**Output**

```shell
H
e
l
l
o
```

Al igual que con while, podemos usar **break** para detener el bucle for, y podemos tambien usar **continue** como se indico con while.

**Código**

```python
cadena = "Hello"
for letra in cadena:
  if(letra == "l"):
    break
  else:
    print(letra)
```

**Output**

```shell
H
e
```

### Rango

Para ejecutar un bloque de codigo un número específico de veces, podemos usar **range()**. La función **range()** devuelve una secuencia de números, comenzando desde 0 (por defecto), se incrementa en 1 (por defecto) y termina en un número específico (requerido).

**Código**

```python
contador = 0
for x in range(10):
  contador += x
  print(x)
print('El resultado es: ', contador)
```

**Output**

```shell
0
1
2
3
4
5
6
7
8
9
El resultado es:  45
```

Podemos indicarle a **range()** el inicio del rango:

**Código**

```python
contador = 0
for x in range(5,10):
  contador += x
  print(x)
print('El resultado es: ', contador)
```

**Output**

```shell
5
6
7
8
9
El resultado es:  35
```

Ademas, tambien podemos indicarle a **range()** el incremento o decremento del valor inicio:

**Código**

```python
contador = 0
for x in range(5,10,2):
  contador += x
  print(x)
print('El resultado es: ', contador)
```

**Output**

```shell
5
7
9
El resultado es:  21
```

## Funciones

Una función es un bloque de código que solo se ejecuta cuando se le llama. Las funciones pueden recibir datos (_parametros_) y tambien pueden _retornar_ datos como resultado de su llamada. Para crear una funcion debemos usar **def**:

**Código**

```python
def imprimir(cadena):
  print(cadena)

imprimir("Holaa") #Llamada de la funcion enviandole un parametro string
```

**Output**

```shell
Holaa
```

## Metodos de cadenas

| Metodo         | Explicacion                                                                     |
| -------------- | ------------------------------------------------------------------------------- |
| capitalize()   | Convierte el primer caracter en mayúscula                                       |
| lower()        | Convierte toda la cadena en minusculas                                          |
| upper()        | Convierte toda la cadena en mayusculas                                          |
| center()       | Devuelve una cadena centrada (requiere indicar el numero de espacios)           |
| count()        | Devuelve la cantidad de veces que aparece en la cadena el valor indicado        |
| endswith()     | Devuelve verdadero si la cadena termina con el valor indicado                   |
| find()         | Busca en la cadena un valor específico y devuelve la posición donde se encontró |
| format()       | Nos permite agregar variables a una cadena                                      |
| index()        | Busca en la cadena un valor específico y devuelve la posición donde se encontró |
| isalnum()      | Devuelve verdadero si todos los caracteres de la cadena son alfanuméricos       |
| isalpha()      | Devuelve verdadero si todos los caracteres de la cadena están en el alfabeto    |
| isidentifier() | Devuelve verdadero si la cadena es un identificador valido                      |
| islower()      | Devuelve verdadero si todos los caracteres de la cadena están en minúscula      |
| isupper()      | Devuelve verdadero si todos los caracteres de la cadena están en mayusculas     |
| isspace()      | Devuelve verdadero si todos los caracteres de la cadena son espacios en blanco  |
| replace()      | Convierte un valor especificado en otro segun lo que se le indique              |
| split()        | Divide la cadena segun el separador indicado y devuelve una lista               |
| title()        | Convierte la primera letra de cada palabra en mayúscula                         |
| strip()        | Elimina los espacios en blanco al principio y al final de la cadena             |

Si quieren investigar un poco mas sobre estos metodos:
['String Methods'](https://www.w3schools.com/python/python_strings_methods.asp)

## Ejercicios

### Ejercicio 8

Realizar un programa donde se reciba un **número entero** por teclado e imprima un mensaje diciendo si el número es _par o impar_ y evaluar si es _positivo o negativo_.

**Output**

```shell
El número: X es par/impar y positivo/negativo
```

Donde **X** es el número ingresado por teclado.

### Ejercicio 9 (Tarea)

Una famosa cadena de cines en Venezuela te contrató para hacerles un programa de descuento basado en la _edad del cliente_, para ello tendrás que recibir por teclado la _edad_ y _nombre_ del cliente y verificar los siguientes casos:

    Si su edad es menor o igual a 4 años el precio de su entrada es gratis.
    Si su edad es menor o igual a 18 años el precio de su entrada es de $1.50.
    Si su edad es mayor o igual a los 60 años su entrada tendrá un valor de $1.00.
    La entrada para un adulto promedio es de $2.00.

Deberás imprimir un mensaje dependiendo de la edad del cliente para saber el precio de su entrada.

**Output**

```shell
El cliente: {nombre} tiene: {edad} años y su entrada de cine cuesta: ${precio_entrada}.
```

### Ejercicio 10

Te contrataron para realizar un programa que calcule el **premio** de un juego.

Los premios estan basados en puntos:

| Puntos  |    Premio     |
| :-----: | :-----------: |
|  1-50   | No hay premio |
| 51-150  |    Bronce     |
| 151-180 |     Plata     |
| 181-200 |      Oro      |

Todos los límites inferiores y superiores son _inclusivos_, y los puntos solo pueden tomar _valores enteros positivos hasta 200_.

En su declaración _if_, asigne la variable resultado a una cadena que contenga el mensaje _apropiado_ según el valor de los puntos.

Si ganaron un premio, el mensaje debería decir:

**Output**

```shell
 "¡Felicitaciones, ganaste la medalla de {nombre del premio} por haber tenido {puntos} pts!"
```

Si no hay premio, el mensaje debe decir:

**Output**

```
 "Ay, lo sentimos pero no hay premios para {puntos} pts."
```

### Ejercicio 14

Escribir un programa que pida al usuario un **número entero positivo** y muestre por pantalla _todos los números impares desde 1 hasta ese número separados por comas_.

### Ejercicio 15 (Tarea)

Escribir un programa que pida al usuario un número entero positivo y muestre por pantalla la cuenta atrás desde ese número hasta cero separados por comas.

**Nota**: La cuenta atras debe ser impresa en una sola linea.

### Ejercicio 16 (Tarea)

Escribir un programa que pida al usuario un **número entero positivo** y muestre por pantalla un triángulo rectángulo (como el que se indica a continuacion), que tenga de **altura** el número ingresado.

```shell
*
**
***
****
*****
```

### Ejercicio 17

Escribir un programa que pida al usuario un **número entero** y que muestre por pantalla si es un **número primo** o no.

**Nota:** Si el numero dado es negativo debe transformarlo en positivo.

### Ejercicio 18

Las palabras o números **palíndromos** son aquellas que _se leen igual de izquierda a derecha_. Por ejemplo: 101 es un número palíndromo, y 236 no lo es. Ana es una palabra palíndroma y pan no lo es.

Sabiendo esto, diseñe un programa que determine si un número o palabra ingresada por el usuario, es palíndroma o no.

### Ejercicio 19 (Tarea)

Escribir un programa que le pida al usuario una **frase** y una **letra**. Luego, muestre por pantalla el _número de veces que aparece la letra en la frase_.

### Ejercicio 21 (Tarea)

Realice un programa que dada una **lista** de nombres, pida al usuario introducir un **nombre** y _verificar si este está o no en la lista_.

### Ejercicio 23

Elabore un algoritmo que le pida al usuario un **número de partida** y un **número final**, para luego imprimir por pantalla los números de la **sucesión de Fibonacci** contenidos dentro de ese rango de números. Los numeros de la sucesion deben guardarse en una lista, y los numeros dentro del rango deben guardarse en otra lista. Luego, debe indicar por pantalla esta ultima lista de los numeros dentro del rango.

### Ejercicio 24 (Tarea)

Escribir un programa que almacene los vectores _(1,2,3)_ y _(-1,0,2)_ en dos listas y muestre por pantalla su **producto escalar**.

### Ejercicio 25 (Tarea)

Realizar un algoritmo que dado un número **N** cualquiera, busque todos los **numeros primos** menores a **N** y que los guarde en una **lista**. Luego, debe buscar en la lista _dos numeros primos cuya multiplicación de como resultado N_, en caso de no existir se le debe mostrar al usuario un mensaje de error.

### Ejercicio 26

Realice un algoritmo que realice las operaciones de **suma** y **resta** entre las siguientes **matrices**:

|     | Matriz | A   |
| --- | ------ | --- |
| 1   | 4      | 6   |
| 4   | 2      | 5   |
| 6   | 5      | 3   |

|     | Matriz | B   |
| --- | ------ | --- |
| 1.3 | 20     | 12  |
| 1.8 | 28     | 15  |
| 2.5 | 40     | 18  |

El programa debera imprimir _dos matrices resultantes_, una correspondiente a cada operación.

**Pista**: Una matriz puede ser modelada como una _lista de listas_.

### Ejercicio 27 (Tarea)

Realice un algoritmo que dado un **número** ingresado por el usuario realice la operación de _multiplicación por la matriz A_ del ejercicio anterior. El programa deberá
mostrar como respuesta la _matriz resultante_ de la misma.
