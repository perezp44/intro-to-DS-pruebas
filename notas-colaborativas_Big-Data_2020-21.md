# Notas-colaborativas (Big Data 2020-21) :book:

Se trata de hacer unas notas/apuntes entre todos. A ver si salen ok.

-------------------------------------
# Índice

Hay que pensar en como se estructuran las notas. No lo tengo claro.

* Sección 1: Intro
* Sección 2: Rmarkdown
* Sección 3: Iniciación a R-base
* Sección 4: Las Funciones (y su ayuda)
* Sección 5: Estructuras de datos en R


-------------------------------------

# Sección 1: Intro

**R** es un **programa y un lenguaje de programación**. Y su interfaz o forma de darle los datos es a través de R-Studio (a quien se le dan las ordenes)
 -	El repositorio oficial de R: CRAN
 -	El repositorio no oficial es GitHub
 -	**Tidyverse**: es un conjunto de paquetes R diseñados para la ciencia de datos. Permite hacer las cosas en R de otra manera, más sencilla. 
 
 Para **dar órdenes a R** se puede hacer de varias maneras:
 -	En la consola, escribiendo la orden y pulsando **ENTER**.
 -	**Usando un script o fichero .R** (Siguiendo la siguiente ruta:  File - New file - R Script) 
 Una vez creado el fichero, se escribe la función y **Ctrl + ENTER**

 **Script** - Es un fichero de texto con extensión .R (Donde se escriben las instrucciones para que R las ejecute)
 En un script solo se pueden escribir dos cosas:
 -	Comentarios (Cuando la línea empieza con #) 
 -	Instrucciones R (R las ejecutará si siguen las reglas del lenguaje R, si están mal escritas dará un mensaje de error) 
 
Los **Rprojects** son carpetas donde guardar los ficheros necesarios para hacer análisis de datos. (Dentro de estas carpetas habrá unos ficheros (scripts o Rmd) que contendrán las instrucciones para ser ejecutadas

 Para crear un R Project hay que seguir los siguientes pasos:
- Abrir RStudio.
- Seguir la siguiente ruta: File - New Project - New Directory - New Project
 
**En Rproject el directorio de trabajo del proyecto es la propia carpeta del proyecto. Eso permite trabajar con rutas (paths) relativas.** 


# Sección 2: Rmarkdown

Estos documentos son ficheros con extensión .Rmd

Tienen: Encabezados, chunks y texto (con # se pueden escribir los títulos)

- El Rmd. es plenamente reproducible
- Estos documentos se procesan con un paquete de R llamado **knitr**. 
-  El encabezamiento empieza y acaba con **- - -**
 

Los trozos de código o chunks van dentro de estas marcas: (Se pueden poner con el siguiente atajo de teclado: CTRL + ALT + I)

```
```{r}
<Código R>
``
```

Si quieres que el código R no se muestre en el documento final has de poner la opción `echo = FALSE`: 


```
```{r, echo = FALSE}
<Código R>
``
```

# Sección 3: Iniciación a R base

Algunas ideas...

**ASIGNACIÓN** --> Los cálculos intermedios se pierden sino creamos un “objeto”, para ello se utiliza el símbolo: `<-`
(Ejemplo `aa < - 2+5`, al poner aa y ejecutar mostrará el valor 7)



### **R PUEDE MANEJAR DIFERENTES TIPOS DE DATOS:**

**Operadores con números** (de comparación) - Cabe destacar que:
-	El símbolo de diferente, se escribe como: **`!=`**
-	El símbolo igual se expresa con el doble igual, es decir **`==`**

Devuelven un “boolean”, ya que el resultado de la comparación solo puede ser TRUE o FALSE si la afirmación es cierta o no

**Operaciones con texto**
-	No se puede sumar 2 textos, pero si se puede pegar o concatenar.
**Función: paste()**

**Operadores lógicos:**
-	**&** es el operador lógico **AND**
-	**|** es el operador **OR** (Solo devuelve FALSE si no se cumple alguna de las condiciones)
-	**¡** es el operador **NOT**. Cambia el sentido de una afirmación lógica, es decir, niega. (Por ejemplo: ¡(4>3) es true, pero como está puesta la exclamación que niega, dará False)

