# Bash

1. Contar la cantidad de palabras de un archivo. Si no existe, devolver 0.

1. Dadas las notas de del tp1 y tp2 en dos variables, quiero saber si aprobé o no (aprobar implica que el promedio de las notas sea mayor o igual a `7`).

1. Dada una cantidad indeterminada de notas, valores que mi script recibe por parámetro, deseo saber si aprobé o no (aprobar implica que el promedio de las notas sea mayor o igual a `7`).

1. En un directorio puntual, cuyos subdirectorios representan materias, y en cada una un archivo por cada ejercicio resuelto de la misma, quiero saber para qué materia practiqué más. Los ejercicios empiezan llamándose "ej" (los de programación son `.py` pero los de análisis `.doc`). Ignorar cualquier otro tipo de archivo. 

1. Dado un directorio el cual posee solamente archivos (no tiene subdirectorios) queremos saber el nombre del archivo que se encuentra en la mitad considerando que están ordenados por orden alfabético.

1. En un directorio `entregas/` se encuentran todas las entregas que todos los alumnos de la materia TB00 hicieron durante el cuatrimestre. Cada tipo de entrega tiene su propio directorio (ej: `tp1/`, `tp2/`) y en cada una, cada alumnos tiene su propio directorio con su padron de manera que el directorio tendría esta forma

    ```
    entregas/
        tp1/
            91234/
            101010/
        tp2/
            ...
        ...
    ```

    Queremos saber:

    {:.lower_alpha}
    1. Si un alumno puntual (dado su padrón) hizo todas las entregas

    2. Cuáles alumnos (por su padrón) hicieron todas las entregas

1. Supongamos ahora que el directorio `entregas/` esta dividido por cuatrimestre

    ```
    entregas/
        2024c2/
        2024c1/
        2023c2/
        ...
    ```

    Queremos saber qué alumnos recursaron la materia (es decir, que tuvieron entregas en más de un cuatrimestre).