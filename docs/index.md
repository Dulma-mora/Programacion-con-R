## Bases de programación con R

### Objetivo

El objetivo de este repositorio es brindar una guía accesible, fácil y útil para comenzar a familiarizarse con las bases de programación con R, sus paqueterías y sus maravillosos usos dentro del mundo godín.

_Por favor tenga paciencia para aprender._

### Índice

Por qué aprender a usar R.

Familiarizándose con el entorno de RStudio.

Tipos de datos.

Objetos.

Estructuras de datos.

...


# ¿Por qué aprender a usar R?

Si bien aprender a programar es una inversión a mediano plazo, las ventajas de ser godín programador son muy numerosas, ya que nos permite hacer las cosas de manera automatizada, compartida, eficiente y con más opciones de personalización.

Algunas de las actividades que podrán ser capaces de hacer si le tienen paciencia a aprender este bonito lenguaje son:
- Cargar datos de una hoja de excel en R (uso de las paqueterías readxl y xlsx).
- Filtrar datos de acuerdo a parámetros establecidos (uso de la paquetería dplyr).
- Hacer gráficos sencillos pero atractivos de visualización de datos (uso de la paquetería ggplot2).
- Crear repositorios compartidos donde puedan guardar y consultar su información (GitHub).


# Familiarizándose con el entorno de RStudio

Una vez que Emiliano les muestre cómo descargar R y RStudio en sus computadoras (aclaración, R es el lenguaje y RStudio el ambiente de desarrollo donde trabajaremos) encontrarán que al abrir este último, la pantalla de inicio se verá algo parecido a esto:

![Interfaz de Rstudio](https://swcarpentry.github.io/r-novice-gapminder-es/fig/01-rstudio.png)

Aunque al principio nada tenga sentido, con el tiempo es natural moverse por esta interfaz. De manera resumida, estas son las funcionalidades de cada una de las pantallas que se desglozan:

![funciones](https://i0.wp.com/gonzalezgouveia.com/wp-content/uploads/2019/04/imagen-2.png?resize=830%2C446&ssl=1)

### 1. Consola

La consola es el núcleo de R, es el espacio donde podremos ejecutar las órdenes que queramos darle a la computadora. En la consola se ejecutan todos nuestros cálculos, creación y modificación de variables.

### 2. Entorno 

En esta pequeña pestaña podemos ver el estado de todas las variables que vamos creando mientras programamos.

### 3. Editor

El editor de texto es un archivo con terminación .R donde guardamos todas las instrucciones que ejecutamos en la consola para poder replicarlo después con otros datos. Estos archivos tienen el nombre de 'scripts'.

### 4. Utilidades

Dentro de esta pestaña podemos encontrar cinco ventanas donde podemos observar los archivos y el directorio en el que estamos, los gráficos que vamos creando, las paqueterías, centro de ayuda y apoyo con funciones y paqueterías; y finalmente el viewer que nos ayuda a visualizar animaciones o gráficas interactivas.

### 5. Menú Superior

Es el espacio donde podremos controlar las configuraciones de nuestros archivos como 'Guardar', 'Abrir Archivo', 'Ajustes', etc.



# Tipos de datos

En todos los lenguajes de programación existen diferentes tipos de datos. En R, hay numerosos tipos de datos, pero los principales son cuatro:
- Numeric.
- Integers.
- Logical.
- Character.

### Numeric values

Los valores numéricos (numeric) corresponden a 

```markdown
1.2 # es un valor numérico
-6.78 # es un valor numérico
10 # es un valor numérico entero
145/0.5 #el resultado de muchas operaciones es numérico
```


### Integer values

Los valores integer cumplen la característica de que son valores numéricos *enteros*. Por ejemplo:

```markdown
1 # es un valor numérico
-800 # también lo es
546 - 125 # el resultado de cualquier operación que dé como resultado cualquier entero también lo es
```

De esta manera podemos concluir que todos los valores enteros son numéricos, pero no todos los valores numéricos son enteros.

### Logical values

Los valores lógicos, o también conocidos como 'valores booleanos', son solamente *dos* dígitos:

```markdown
`TRUE` 
`FALSE`

# Ambos son valores categóricos _mutualmente excluyentes_. Estos valores se suelen utilizar para mostrar condiciones: sí / no, obtenido / no obtenido, enfermo / no enfermo. Es muy común ver estas variables en tablas y data frames. También se pueden representar solo con sus iniciales mayúsculas:

`T`
`F`

```

```markdown
# Ejemplo de uso de valores lógicos

| Paciente | Enfermo   |
| ---      | ---       |
| Emiliano | `TRUE`    |
| Marlene  | `TRUE`    |
| Dulma    | `FALSE`   |

# Si quisiésemos saber cuántas personas enfermas hay en la tabla, nuestra búsqueda se resume a calcular el número de TRUE en la columna de enfermos. Y lo mismo para encontrar a las personas sanas.
```


### Character values

Los valores de caractér son todas las secuencias de palabras o dígitos. Usualmente se usan para procesar cadenas de texto (palabras) y pueden mezclarse con números también. Sin embargo, los números que sean guardados como caracteres dejarán de poder usarse para hacer operaciones, ya que no se detectan como valores numéricos, sino como cadenas de texto.

```markdown
# los valores de caracter se escriben con comillas **siempre**:

"hola" # hola es un character value ahora
"Tengo 5 gatos" # también las frases aunque incluyan números son procesadas como cadenas de texto
"234322" # incluso los valores numéricos pueden guardarse así
"2" + "2" # SIN EMBARGO, no podemos hacer ningún tipo de operación con caracteres. Si intentamos correr esto nos saldrá ERROR.
```

```markdown
# Por ejemplo, con caracteres podemos guardar los nombres de pacientes de una tabla:

| Paciente   | Enfermo |
| ---        | ---     |
| "Emiliano" | TRUE    |
| "Marlene"  | TRUE    |
| "Dulma"    | FALSE   |

# Ahora R sí va a detectar los nombres

```


# Objetos

Ahora que vimos los principales tipos de datos, es importante que sepamos qué hacer con ellos. No podemos simplemente ir escribiendo todas nuestras operaciones en la consola como si fuera una calculadora, eso haría que perdieramos muchos datos en el proceso, resultados e información útil. Es así que veremos qué son los objetos.

¿Qué es un objeto? Cuando hablamos de programación casi todo es un objeto.

_TIP:_ Es útil pensar en los objetos como si fueran cajas donde guardamos cualquier cosa dentro de R. En una caja podemos guardar una palabra, un número, un resultado, un valor booleano, incluso tablas, listas, matrices, gráficos... lo que quieras. Y lo importante es que las "cajas" donde guardemos nuestra información, adquieren las características de nuestros valores guardados.

```markdown
# Para crear un objeto / caja / variable necesitamos darle un nombre y declararla con <-
# Ejemplo:

caja1 <- 10    # aquí hemos creado un objeto o caja llamado "caja1" y dentro hemos guardado un valor numérico entero (10)

print(caja1)  # ¿qué crees que aparezca si imprimes el contenido de caja1?
class(caja1)  # esta función nos permite ver la clase de un objeto. Si dentro de nuestra caja hay un 10, ¿qué clase de objeto es "caja1"?

caja2 <- 5    # hemos creado otro objeto distinto donde guardamos un 5

caja1 - caja2   #si hacemos una operación entre nuestros dos objetos, ¿nos dará un resultado? Spoiler: SI!


caja3 <- caja1 - caja2   # intentemos algo aún más loco, guardar el resultado de la operación dentro de otro objeto llamado "caja3"
print(caja3)             # pregunta: ¿si imprimimos el valor de caja3 qué nos va a salir? 

IMPORTANTE: Nota que lo que R guarda en los objetos son **RESULTADOS**, no procedimientos.
Si imprimimos caja3 el output NO será "caja1-caja2" sino el resultado de dicha operación solamente, es decir "5".
Prueba obteniendo la clase de caja3

print(caja3)

```




```markdown


```








