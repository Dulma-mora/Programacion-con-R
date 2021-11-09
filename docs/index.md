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

| Paciente | Enfermo |
| ---      | ---     |
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


## Markdown

Markdown is a lightweight and easy-to-use syntax for styling your writing. It includes conventions for

```markdown
Syntax highlighted code block

# Header 1
## Header 2
### Header 3

- Bulleted
- List

1. Numbered
2. List

**Bold** and _Italic_ and `Code` text

[Link](url) and ![Image](src)
```



