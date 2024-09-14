title: TP1 * PokeScript

# TP1 - PokeScript

## Temas a evaluar

- Manejo de terminal
- Bash scripting
- Piping
- Git

## Glosario

- **Pokemon**: monstruo ficticio de la serie animada japonesa Pokemon. Son comunmente utilizados para enfrentarse en batallas entre si. Actualmente hay mas de mil Pokemones. Un clásico ejemplo es Pikachu. Considerar que no existe un unico Pikachu en el mundo, pueden haber infinitos.
- **Tipo**: uno de los atributos que puede tener un Pokemon. Hay un total de 18 tipos diferentes en Pokemon. Los Pokemones pueden tener hasta un máximo de 2 tipos. Definen la efectividad y resistencia de los ataques que afecten al Pokemon.
- **Estadística**: al igual que el tipo, las estadísticas son los atributos que tiene un Pokemon. Existen las estadísticas de Ataque (ATK), Defensa (DEF), HitPoints (HP), Ataque Especial (SPATK), Defensa Especial (SDEF) y Velocidad (SPEED). Todos los Pokemones tienen distintas estadisticas base, pero por ejemplo todos los Pikachu tienen las mismas estadisticas base.
- **Habilidad**: efecto, usualmente beneficioso, que afecta a un Pokemon. Cada Pokemon tiene un pool de habilidades con las que puede existir, sin embargo, un Pokemon siempre tiene exactamente una Habilidad.

## Consigna

Se tiene un set de archivos `csv` con informacion variada de todos los Pokemones existentes.

Se precisan implementar dos scripts de bash que:

- El primero, debe obtener en un archivo todos los Pokemon que cumplan ciertos filtros ingresados por parámetro.
- El segundo, dado un Pokemon ingresado por stdin, muestre información del mismo por stdout.

A su vez, se requiere la creación de un repositorio en GitHub donde se desarrollaran dichos scripts y el trabajo correspondiente.

El trabajo esta dividido en 4 partes.

### Parte 0 - Creacion del repositorio de GitHub

Antes de iniciar con los scripts se necesita generar el repositorio de trabajo y mantener un control de versiones adecuado y ordenado.

El nombre del repositorio debe tener un nombre de formato `2024c2_<padron>`, por ejemplo `2024c2_123456`. Este repositorio debe ser **privado** y su rama principal debe estar vacia.

Cada script debe ser desarrollado en una rama independiente llamadas `parte_1` y `parte_2`. Al finalizar el desarrollo de cada una se debe crear un **Pull Request** a la rama principal dentro de su repositorio.

Es importante ser ordenados a la hora de trabajar y organizar el repositorio, revisen los PR antes de realizar la entrega y verifiquen no tener cosas de la `parte_1` en la `parte_2` y viceversa.

Luego de tener ambos scripts desarrollados, realizar la `parte_3`, creando el tercer y ultimo PR.

Una vez creado el repositorio, finalizados los scripts pedidos y teniendo los PRs listos, agregar a su ayudante al repositorio como colaborador con el rol de **Triage** para que pueda luego realizar las correcciones necesarias. Al agregar a su colaborador recomendamos también escribirle por Discord para notificarle de la entrega.

### Parte 1 - Filtrado de Pokemones

Para el primer script entregable `parte_1.sh` se precisa filtrar y obtener los nombres de los Pokemones que cumplan ciertas condiciones.

El script debe recibir por parámetro un padrón y un nombre de directorio donde se guardará un archivo llamado `resultado.txt`. En caso de no existir dicho directorio, el script debe crearlo y luego guardar el `resultado.txt` correspondiente. En caso de ya existir el archivo, sobreescribirlo.

El script debe, en base al padrón ingresado:

- Calcular el modulo (`%`) **18** y sumarle **1**. Este valor representara el **tipo** de los Pokemones a obtener.
- Calcular el modulo (`%`) **100** y sumarle **350**. Este valor representara el mínimo de **estadística total** de los Pokemones a obtener.

Con esos dos valores y usando los archivos `csv` dispuestos en la consigna se debe escribir en `<directorio>/resultado.txt` todos los nombres de los Pokemones que cumplan ambos criterios en simultáneo.

Por ejemplo, si mi padrón es 99779:
```console
$ expr 99779 % 18
5
$ expr 99779 % 100
79
```

Debo obtener todos los Pokemones de tipo `5 + 1 => 6` (es decir, tipo Roca) que tengan una estadística total de al menos `79 + 350 => 429` y escribir el resultado en el directorio ingresado por parámetro.

Nota: Para calcular la **estadística total** de un Pokemon se deben sumar todas las estadísticas del mismo y ese sería su valor total. Por ejemplo el Pokemon `Pikachu` tiene 320 de estadística total ya que la suma de sus estadísticas (HP: 35, ATK: 55, DEF: 40, SPATK: 50, SPDEF: 50, SPEED: 90) da ese número.

Ejemplo de ejecución:

```console
$ ls directorio_resultados/
ls: cannot access 'directorio_resultados/': No such file or directory
$ ./parte_1.sh 99779 directorio_resultados
$ ls directorio_resultados/
resultado.txt
$ head -n 5 directorio_resultados/resultado.txt
golem
rhydon
omastar
kabutops
aerodactyl
```

El script **debe funcionar sin importar donde se encuentren los archivos de csv** (siempre y cuando estos archivos csv estén en un subdirectorio del directorio donde esté el script). Es decir, el script debe poder encontrar los archivos csv en cualquiera de estos casos:
```
/tp1
    parte_1.sh
    archivos.csv
```
o 
```
/tp1
    parte_1.sh
    /sub1
        /sub2
        /sub3
            archivos.csv
```
o cualquier otra combinación de subdirectorios.

### Parte 2 - Mostrar Pokemones

Para el segundo script entregable `parte_2.sh` se leerá de stdin nombres de Pokemones y se mostrará por stdout cierta información de los mismos.

La información a mostrar es:

- Peso
- Altura
- Habilidades

Ejemplo de ejecución:

```console
$ ./parte_2.sh
metagross
---------------------
Pokemon: metagross
Altura: 160 centimetros
Peso: 550 kilos

Habilidades:
 * Cuerpo Puro
 * Metal Liviano
---------------------
```

### Parte 3 - Combinacion de scripts

Una vez desarrollados ambos scripts y tener los dos PRs listos:

- Crear una nueva rama `parte_3` e integrar los cambios de `parte_1` y `parte_2` en ella.
- Ejecutar el script `parte_1.sh`: `./parte_1.sh <PADRON> resultado` (donde `PADRON` es su padrón propio, no el de alguien más).
- Ejecutar el script `parte_2.sh` usando el archivo generado por la parte 1 como entrada y redireccionar la salida a un archivo `output.txt`.
- Crear un PR contra la rama principal con **únicamente** el archivo resultado del segundo script (`output.txt`).

Nota: Revisar que el `output.txt` tenga la información esperada antes de entregarlo.

## Documentos disponibles

Se dispone de varios archivos de tipo csv adjuntos en un [archivos.zip](archivos.zip) para la ejecución del trabajo practico

Tener en cuenta que no todos los archivos son necesarios para la resolución del TP. Sin embargo, es importante leerlos para entender qué significa cada uno.


## Restricciones y condiciones de entrega

- La ejecución de los script no debe presentar errores.
- El trabajo debe ser entregado en tiempo y forma, de lo contrario se pierde la primera entrega.
- El entregable del trabajo practico es el repositorio de GitHub que ustedes creen. En el momento que agregan a su ayudante como Triage del mismo se considera que han realizado la entrega.
- **No** subir los archivos de `csv` al repositorio. Únicamente los resultados de la ejecución de los scripts cuando la consigna indique.
