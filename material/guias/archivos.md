# Procesamiento de Archivos (grep, sed, cut)


Escribir un script que:

1. Reciba un archivo y una palabra y cuente la cantidad de líneas en las que aparece

1. Reciba un directorio y una palabra y cuente la cantidad de líneas en todos los archivos del mismo (y sus subdirectorios) en los que aparece

1. Reciba un directorio y una palabra y muestre el nombre de los archivos del mismo (y sus subdirectorios) en los que aparece

1. Reciba un archivo y una palabra y cuente la cantidad de **apariciones** de esa palabra

1. Reciba un archivo y una cantidad indefinida de palabras y cuente la cantidad de líneas en las que aparece **alguna** de ellas

1. Reciba un archivo y una cantidad indefinida de palabras y cuente la cantidad de líneas en las que aparecen **todas** ellas


## Dado el siguiente archivo padron.csv:

```
dni;nombre;apellido;edad;nacionalidad;localidad;codigo_postal
```

1. Mostrar todas las personas con apellido compuesto (ej: García Lopez)

1. Mostrar todas las personas cuya localidad contiene al menos dos números

1. Mostrar todas las personas que están mal cargadas y su nombre o apellido está solo en minúscula

1. Mostrar todas las personas cuyo DNI empieza con 40 millones, su apellido termina con 'ez' y su nacionalidad **no** es Argentina.

1. Mostrar únicamente el DNI de todas las personas

1. Mostrar únicamente el DNI de quienes viven en la localidad de 'Lomas de Zamora'

1. Mostrar únicamente las 3 primeras letras del nombre de las personas que se apellidan García

1. Generar un nuevo archivo tal que contenga únicamente a las personas cuya edad es exactamente 20 o 30 y que modifique el codigo postal guardado tal que sólo los números del código postal sean guardados (ejemplo de código postal: C1423ABC)