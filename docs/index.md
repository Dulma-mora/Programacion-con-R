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
```


### Integer values

Los valores integer cumplen la característica de que son valores numéricos *enteros*. Por ejemplo:

```markdown
1 # es un valor numérico
-800 # también lo es

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



