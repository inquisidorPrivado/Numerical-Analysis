# Pequeña introducción a Python

## Variable

Las variables en Python son como etiquetas (permiten hacer referencia a los datos) y no como cajas.

Vamos a usar la nomenclatura snake_case.

Ejemplo:

```python
# Para el código se usa acento grave (`)
# alt+96 `

#<nombre de la variable> = <valor>

nombre_usuario = 'El Ranchero'
print(nombre_Usuario)


```

## Constante 

Variable que no puede cambiar su valor en tiempo de ejecución. En python no existe esto, pero usamos esta convención creada por la comunidad:

```python
TITULO_CURSO = 'Curso profesional de python'
```

## Palabras reservadas 

Aquí una página que enlista las [palabras reservadas](https://www.programiz.com/python-programming/keyword-list).

## Comentarios

```python
# Para
"""
comentario con saltos
de línea
"""
```

## Tipos de datos

La propiedad de un valor para poder determinar qué valores puede tomar.
Los cuatro tipos de datos más usados:

```python
# String
titulo_curso = "Curso python"
mensaje = "'Comillas simples'"
mensaje = '"Comillas dobles"'
mensaje_largo = ''' Te encuentras
en otro lado del multiuniverso
jajajaja lol equisdé
A la víbora víbora de la mar de la mar
'''

# Int
numero_uno = 10
division_entera = 10 // 3
division_con_decimal = 10 / 3
print(numero_uno)

# Float
numero_dos = 3.1416

# Bool - solo almacena dos valores
valor = True
valor = False
```

## Tipado dínamico 

La posibilidad que tienen las variables de poder almacenar diferentes tipos de datos en diferentes momentos.

```python
valor = "El pepe"
valor = 2
valor = True
```

Lo más recomendable es no almacenar diferentes tipos de datos en las variables

## Operadores relacionales

Nos permiten obtener un valor booleano para condicionar nuestro código.

Son 6 operadores relacionales:

* \>
* <
* \>=
* <=
* ==
* !=

## Operadores lógicos

Obtenemos un valor booleano

```python
# and, or y not

# and
# Todas las comparaciones deben de ser verdaderas
resultado_final = True and ( False or 50 > 10) 

# or
# Al menos uno debe de ser True
resultado_final = True or False or 10 < 20


# not
# Negar un valor Booleano (obtenemos el valor contrario)
resultado_final = not True  # False

```

## Conocer de tipos de datos

¿Qué tipo de dato almacena cierta variable?
Con la función type

```python
valor = 'Ranchero'
print(type(valor))  # Nos ahorramos una variable

valor = 3.1416
tipo_de_dato = type(valor)


print(tipo_de_dato)

```

## Leer valores por teclado 

```python

nombre_completo = input('Ingrese su nombre completo: ')

print(nombre_completo)

```

## Convertir tipos de datos 

```python

edad = input('Ingrese su edad: ')
# Función int: pasamos un string a un entero
edad = int(edad)
print(type(edad))

altura = input('Ingrese su altura')
# Función float: Pasamos un string a float
altura = float(altura)
print(type(altura))

autorizacion = input('¿Autorizas al programa? si/no')
autorizacion = autorizacion == 'si'
print(autorizacion)
```

Podemos refactorizar el código:

```python

edad = int(input('Ingrese su edad: '))
print(type(edad))

altura = float(input('Ingrese su altura'))
print(type(altura))

autorizacion = input('¿Autorizas al programa? si/no') == 'si'
print(autorizacion)
```

## Crear variables 

```python

#Normalmente no se crean más de tres variables en una línea
# Cuatro a lo máximio y tratamos de crear una relación entre sí
nombre, apellido, titulo = 'Leonor', 'HsLt', 'Dr.'

print(nombre)
print(apellido)
print(titulo)
```

# Ciclos y condiciones

# Tipo None

Para poder declarar variables vacias o nulas podemos hacer uso del tipo None. Ya sea porque aun no queramos poner algo dentro de ellas
```python
color_1 = "azul"
color_2 = "verde"
color_3 = None
print(color_1)
print(color_2)
print(color_3)
def cambiar_colores():
    color_3 = input("pon un nombre al color numero 3: ")
    # Ahora cuando ya queramos poner un valor a nuestro color_3 podremos hacerlo tranquilamente
    print("El color 3 ahora es: " + color_3) 
     
```

## Valores falsos

```python
# True (1) / False (0) 
```

Cualquier valor que no se encuentre en la lista, es verdadero:

* False
* None
* 0
* 0.0
* ''
* ""
* []
* ()
* {}

## Condiciones

Son las estructuras que permiten la toma de decisiones en el código, siempre y cuando se cumpla una condición. Con los operadores matemáticos, lógicos y relacionales podemos decidir que hacer y de acuerdo al resultado se ejecutará un código u otro.

```python
resultado = 10

if resultado==10:
    print('La variable cumple con la condición')
else:
    print('La condición no se cumple :( ')  
```

***Identación***: Python utiliza la indentación para delimitar la estructura permitiendo establecer bloques de código. No existen comandos para finalizar las líneas ni llaves con las que delimitar el código. Los únicos delimitadores existentes son los dos puntos ( : ) y la indentación del código.

<br>

## *elif*

Se pueden verificar varias condiciones al incluir una o más verificaciones elif después de su declaración if inicial. (Solo se ejecutará una condición):

```python
calificacion = 8

if calificacion == 10:
    print("Felicidades, aprobaste con calificación perfecta")
elif calificacion < 10 or calificacion > 7:
     print("Felicidades, aprobaste")
elif calificacion < 8 or calificacion > 5.99:
     print("Aprobaste")
else:
    print("Shiale, reprobaste, mijo")

```

## Ternario

Como el operador ternario evalúa primero la condición, permite el cortocircuito y solo se evaluará una de las dos expresiones. Si la condición es verdadera, la primera expresión se evalúa; de lo contrario, se evalúa la segunda expresión:

```python
calificacion = 10

#Versión común
color = None
if calificacion >= 7:
    color = 'verde'
else:
    color = 'rojo'

print(calificacion, color)


#Versión ternaria
calificacion = 6
#El else es obligatorio para el if ternario
color = 'Verde' if calificacion >= 7 else 'Rojo'
print(calificacion, color)


```

## Asignar valores mediante operadores lógicos

```python
# La lectura es de izquierda a derecha
variable = 'Cody' or 'CodigoFacilito'
print(variable) #Cody

variable = '' or 'CodigoFacilito'
print(variable) #CodigoFacilito


#Ejemplo 2
listado = []
nombre = 'Cody'

if listado:
    variable = listado
else:
    variable = nombre
print(variable)

```

## Ciclo While

```python
#Ejemplo 1
contador = 1
#Lo usamos cuando no sepamos la cantidad 
# de iteraciones que vayamos a usar
while contador <= 10:
    print(contador)

    contador = contador + 1


#Ejemplo 2

numero = 1234567
contador_digitos = 0

while numero >= 1:
    contador_digitos += 1

    numero = numero / 10
else:
    print(contador_digitos)
#print(contador_digitos)

```

## Foreach

Sirve para iterar sobre tipos de datos de secuencia.

```python
usuarios = ['usuario1', 'usuario2', 'usuario3', 'usuario4']

for usuario in usuarios:
    print(usuario)

# Ponemos en plural la colección, y en singular 
# la variable local

```

## Función enumerate

```python 
#Comienza por default en 0
rango = range(11)   # 0 - 10


#Podemos modificar el rango 
# start, end, skips
# Inicio, final-1, saltos
for valor in range(5, 21, 2):
    print(valor)



#Función enumerate
# Va a retornar una tupla con valores
numeros = [10, 20, 30, 40, 50]
#Estas tuplas van a almacenar dos valores 
# índice y número
for indice, numero in enumerate(numeros):
    print(indice, numero)
#El segundo argumento es para modificar el indice
```

## Break and continue

```python
#Para separar los caracteres de un String
titulo_curso = 'Curso profesional de Python'


#Break rompe el ciclo
for caracter in titulo_curso:

    if caracter == 'P':
        break
    print(caracter)

#Continue omite ciertos elementos (el código que sigue)
for caracter in titulo_curso:

    if caracter == 'P':
        continue
    print(caracter)
```
