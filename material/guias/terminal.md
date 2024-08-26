# Manejo de Terminal

A falta de aclaración, podemos suponer que la estructura de archivos que queremos manejar es:
```
Documentos/
    TB022/
    TP1/
    TB021/
    ... (otras materias)
```


1. Parado en el directorio TB022, quiero crear otra carpeta para mi otra materia TB021 al mismo nivel de ésta.

1. Parado en mis Documentos, se encuentra un archivo que acabo de descargar (TP1.py) que quiero renombrar a TP1_enunciado.py y moverlo a TB022/ sabiendo que es de esta materia.

1. Estoy en medio de la clase y quiero tomar notas en un archivo de texto aclarando que es la clase 2 que trata sobre la terminal. ¿Cómo lo creo?

1. Creé un archivo y resolví todo el TP. Se llamaba algo con “tp1”, pero me di cuenta que no tengo idea en qué directorio estaba parado. ¿Cómo sé dónde estoy? ¿Cómo encuentro mi TP?

1. Es el final del cuatri y ya aprobé todo !! Quiero borrar toda la data de todas las materias del primer cuatri.

1. Un amigo me pidió las notas de la materia. Se las quiero copiar al usb que está montado como “machetes”. Todos los discos externos se montan bajo la carpeta “mnt” en el root.

1. En el directorio donde estoy parado, hay una gran cantidad de subdirectorios. Tengo algunos de las materias que hice del plan viejo, otras del nuevo, y un monton más que no se qué son. Las carpetas de las materias empiezan con su código (las viejas son xx.xx, ej 75.40) y las nuevas son (TBxxx, TCxxx o TAxxx, ej TB021).

    {:.lower_alpha}
    1. Quiero ver todas las materias que hice del plan viejo.

    2. Y ahora las del nuevo.

1. Para cada clase tomé notas y las fui guardando en su propio archivo `claseN.txt`. Quiero crear un archivo unificado con todas las notas que tomé de cada una de las clases de Intro manteniendo el orden de las mismas (el contenido de la tercer clase debe ir después del contenido de la segunda, que debe ir después de la primera). 

1. Tengo un script RE IMPORTANTE que en teoría me resuelve todo el TP1. Pero lo corro y no muestra nada ni hace nada. ¿Qué puedo hacer para entender qué está pasando?

1. Tengo un script que me calcula el promedio de un archivo que tiene cada una de mis notas, una por línea. ¿Cómo imprimo por pantalla mi promedio?

1. Acabo de crear un archivo por consola que sé que lo llamé “tp1.py” pero sin querer cerré la terminal y lo perdí porque no sé dónde estaba. ¿Cómo lo encuentro?

1. En la carpeta de la materia tengo un archivo `.py` por cada ejercicio que hice. Quiero contar todos los ejercicios que hice.
	
1. ¿Cómo abro un archivo de texto con Visual Studio Code desde la consola?

1. El SIU anda muy mal así que tengo un amigo que armó un programa en Swift que me permite subir una nota de una materia y me lo guarda y después puedo consultar mi historial y promedio. Para esto tiene una interfaz como la siguiente:

    ```
    Qué desea hacer?
    1. Agregar nota
    2. Consultar historial y promedio
    Enter para salir.
    <Elijo 1>
    Ingrese el código de materia:
    Ingrese la nota final:
    ¡Guardado! ¿Quiere hacer otra cosa?
    <Muestra nuevamente el menú>
    ```

    Descargué todo mi historial de notas hasta ahora del SIU pero no lo quiero ingresar uno por uno a mano y no sé programar en Swift. Si el archivo del SIU tiene la forma:
    ```
    codigo,nota
    ```

    ¿Cómo puedo hacer?