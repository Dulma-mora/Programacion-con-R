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

En R, las estructuras de datos pueden ser organizadas respecto a su dimensión y su contenido. Por dimensión entendemos que es una estructura plana de una dimensión, de dos dimensiones o de n dimensiones. Por su contenido nos referimos a si es homogeneo (datos del mismo tipo) o heterogeneo (datos de distintos tipos). Así, tenemos la siguiente clasificación para referirse a los cinco tipos de datos en R:

| Dimensiones |Homogéneo | Heterogéneo |
|---        | ---         | ---|
| 1d | Vectores atómicos | List |
| 2d | Matrices | Data Frames |
| 3d | Arrays | 

## Vectores

Los vectores son la unidad de estructura básica en R y cualquier lenguaje de programación. Los vectores pueden ser de dos tipos: **atómicos o listas**. Todos los vectores tienen tres características en común:
1. Pertenecen a una clasificación.
2. Tienen una longitud.
3. Tienen atributos.

De manera general, los datos que conforman a los vectores atómicos son del mismo tipo, mientras que los elementos que conforman a las listas pueden ser de diferentes tipos.

### Vectores atómicos

Existen cuatro tipos de vectores atómicos. Y además de lo anteriormente mencionado, es útil mencionar que los puedes reconocer porque suelen ser formados con la función 'c()' (combinar o concatenar). Estos cuatro vectores atómicos son:

- Double (también llamado numeric).
- Integers.
- Logical.
- Character.

**Los vectores atómicos son siempre planos, es decir, de una dimensión**

#### Double values

Los valores del tipo double corresponden a datos del tipo numérico que pueden ser o bien, números enteros y no enteros.

```markdown
1.2 # es double
-6.78 # es double
10 # es un valor numérico entero (double aún)
145/87 #el resultado de muchas operaciones con números decimales es double
```


#### Integer values

Los valores integer cumplen la característica de que son valores numéricos *enteros*. Por ejemplo:

```markdown
1 # es un valor numérico
-800 # también lo es
546 - 125 # el resultado de cualquier operación que dé como resultado cualquier entero también lo es
```

De esta manera podemos concluir que todos los valores enteros son numéricos, pero no todos los valores numéricos son enteros.

#### Logical values

Los vectores atómicos lógicos, o también conocidos como 'valores booleanos', son valores binarios del tipo 0 - 1 representados con:

```markdown
`TRUE` 
`FALSE`

# Ambos son valores categóricos _mutualmente excluyentes_. Estos valores se suelen utilizar para mostrar condiciones: sí / no, obtenido / no obtenido, enfermo / no enfermo. Es muy común ver estas variables en tablas y data frames. También se pueden representar solo con sus iniciales mayúsculas:

`T`
`F`

```

#### Ejemplo de uso de valores lógicos

| Paciente | Enfermo   |
| ---      | ---       |
| Emiliano | `TRUE`    |
| Marlene  | `TRUE`    |
| Dulma    | `FALSE`   |

Si quisiésemos saber cuántas personas enfermas hay en la tabla, nuestra búsqueda se resume a calcular el número de TRUE en la columna de enfermos. Y lo mismo para encontrar a las personas sanas.



#### Character values

Los valores de caractér son todas las secuencias de palabras o dígitos. Usualmente se usan para procesar cadenas de texto (palabras) y pueden mezclarse con números también. Sin embargo, los números que sean guardados como caracteres dejarán de poder usarse para hacer operaciones, ya que no se detectan como valores numéricos, sino como cadenas de texto.

```markdown
# los valores de caracter se escriben con comillas **siempre**:

"hola" # hola es un character value ahora
"Tengo 5 gatos" # también las frases aunque incluyan números son procesadas como cadenas de texto
"234322" # incluso los valores numéricos pueden guardarse así
"2" + "2" # SIN EMBARGO, no podemos hacer ningún tipo de operación con caracteres. Si intentamos correr esto nos saldrá ERROR.
```

Por ejemplo, con caracteres podemos guardar los nombres de pacientes de una tabla:

| Paciente   | Enfermo |
| ---        | ---     |
| "Emiliano" | 'TRUE'    |
| "Marlene"  | 'TRUE'    |
| "Dulma"    | 'FALSE'   |

Ahora R sí va a detectar los nombres.



Además, podemos pensar en los vectores atómicos simplemente como un conjunto de elementos ordenados en fila, es decir que es de una sola dimensión. 

![lol](https://upload.wikimedia.org/wikipedia/commons/thumb/3/3f/Array1.svg/1920px-Array1.svg.png)

El ejemplo por excelencia de un vector atómico es una secuencia numérica, digamos, del 1 al 10 o del 1 al 100.

```markdown
# Para crear un vector SIEMPRE tenemos que decirle a R que queremos hacer una serie lineal,
# hacemos esto con la función c( ) 

a <- c(1,2,3,4,5,6,7,8,9,10)  # hemos creado un objeto llamado "a" donde guardamos un vector con los números del 1 al 10

# Sin embargo, no es muy cómodo ir escribiendo número por número los elementos de nuestro vector.
# ¿Qué pasaría si queremos hacer un vector de 1000 números?
# Esto se soluciona con " : ", que se puede leer como "de tal a tal número"

b <- c( 1:10 )  # esta instrucción se puede leer como "crea un objeto b donde guardes un vector del 1 al 10 (de tal a tal numero)

```
Ahora que sabemos qué es un vector atómico, es necesario aclarar que una característica muy importante de ellos es que cada elemento cuenta con una celda para él. Estas celdas individuales reciben el nombre de posición o subíndice. En el caso de nuestra secuencia 1:10, resulta fácil ubicar la posición de cada dígito, la posición 1 va con el primer valor (1), la segunda con el segundo valor (2), la tercera con el tercer valor (3)... etc. Pero casi nunca será ese nuestro caso. Ilustremos un ejemplo:

Queremos almacenar la edad de 6 personas, dado que solo queremos hacer una secuencia de estas edades, el producto resultante es un vector numérico.

```markdown
EDAD <- c(18, 22, 25, 23, 17, 19) # creamos un objeto/variable llamado 'EDAD' donde guardamos un vector de 5 elementos, cada elemento corresponde a una edad
print(EDAD)
```
En este sencillo ejemplo, podemos ver que el subíndice 1 tiene un valor de 18, el subíndice 2 tiene uno de 22... y así y así. Ahora que hemos explicado bien la idea, podemos pensar en nuestro vector (y en todos los vectores) de la siguiente manera:

![ejemplo](https://progracomputacional.files.wordpress.com/2015/08/vecuni.gif)

Fácil 😄

Ahora recordemos que en un vector atómico podemos guardar elementos del mismo tipo, por lo que no solo podemos guardar series numéricas sino también series de caracteres.

```markdown
# Creemos un vector de caracteres

v.character <- c("hola", "cómo", "estás", "?")
print(v.character) # tenemos una secuencia lineal de valores del tipo character 
```
Siguiendo la misma lógica de la ilustración pasada, cada subíndice ahora en lugar de guardar un valor numérico almacena un valor de caracter.

**Importante.** Toda esta explicación fue necesaria para llegar al punto central de los vectores: puedes acceder a los subíndices de manera sencilla usando corchetes " [] "

```markdown
# Creémos un vector numérico con los dígitos del 25 al 52
v.numerico <- c(25:52)

# PREGUNTA. Si estuvieras en excel o cualquier otro programa, ¿cómo accederías al valor 17 del vector?
# ¿Cómo lo harías en R? -> la respuesta es simplemente usando []
v.numerico[17] 

# así obtenemos el valor número 17 de nuestro vector, que corresponde al número 41
```

Otro ejemplo más con vectores de caracter:

```markdown
v.familia <- c("Emiliano", "Natalia", "Dulce", "Josue", "Martha") # creamos un vector llamado v.familia donde están los nombres de los integrantes de mi familia lol

# queremos obtener el nombre que ocupa la posición 3, la lógica es la misma:
v.familia[3] 

# Dulce es el nombre que ocupa la tercera posición
```

Ejercicios

*1*
```markdown
# Crea un vector con el nombre que quieras donde guardes una secuencia del 34 al 128
# Después accede al número en la posición 37
```
*2*
```markdown
# Crea un vector donde guardes los nombres de: el amor de tu vida, la persona que más te caiga gorda del trabajo,
# el niño que te pegaba en la primaria, tu mejor amigo, el famoso que más odies y tu película favorita
# Después accede al nombre de la posición 4
```


# Listas

Las listas son distintas de los vectores atómicos porque sus elementos pueden ser de cualquier tipo (heterogéneos), incluso puede haber listas dentro de una lista. Para construir una lista se utiliza la función list( ) en lugar de c( ).









# Variables

Ahora que vimos los principales tipos de datos, es importante que sepamos qué hacer con ellos. No podemos simplemente ir escribiendo todas nuestras operaciones en la consola como si fuera una calculadora, eso haría que perdieramos muchos datos en el proceso, resultados e información útil. Es así que veremos qué son las variables.

¿Qué es una variable? Cuando hablamos de programación casi todo es una variable.

_TIP:_ Es útil pensar en las variables como si fueran cajas donde guardamos cualquier cosa dentro de R. En una caja podemos guardar una palabra, un número, un resultado, un valor booleano, incluso tablas, listas, matrices, gráficos... lo que quieras. Y lo importante es que las "cajas" donde guardemos nuestra información, adquieren las características de nuestros valores guardados.

```markdown
# Para crear una caja / variable necesitamos darle un nombre y declararla con <-
# Ejemplo:

caja1 <- 10    # aquí hemos creado una variable o caja llamado "caja1" y dentro hemos guardado un valor numérico entero (10)

print(caja1)  # ¿qué crees que aparezca si imprimes el contenido de caja1? La función print() imprime el contenido de una variable
class(caja1)  # esta otra función nos permite ver la clase de un objeto. Si dentro de nuestra caja hay un 10, ¿qué clase de objeto es "caja1"?

caja2 <- 5    # hemos creado otro objeto distinto donde guardamos un 5

caja1 - caja2   #si hacemos una operación entre nuestros dos objetos, ¿nos dará un resultado? Spoiler: SI!


caja3 <- caja1 - caja2   # intentemos algo aún más loco, guardar el resultado de la operación dentro de otro objeto llamado "caja3"
print(caja3)             # pregunta: ¿si imprimimos el valor de caja3 qué nos va a salir? 

IMPORTANTE: Nota que lo que R guarda en los objetos son **RESULTADOS**, no procedimientos.
Si imprimimos caja3 el output NO será "caja1-caja2" sino el resultado de dicha operación solamente, es decir "5".
Prueba obteniendo la clase de caja3

print(caja3)

```

## Ejercicios


```markdown
# Crea un objeto llamado "a" y asígnale un valor numérico

```

```markdown
# Crea un objeto "b" y asigna una variable de caracter de cualquier longitud

```

```markdown
# Imprime el valor de ambos objetos

```








