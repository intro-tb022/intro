# TP2 Parte 1- IntroDex

## Temas a evaluar

- Git
- Trabajo en equipo
- Testing
- Web
- Desarrollo BackEnd (Framework: FastAPI)

## Glosario

- Equipo Pokemon: Un equipo Pokemon es un grupo de pokemones de entre 1 y 6 integrantes. Puede tener al mismo pokemon repetido muchas veces.
- Generacion: Los juegos de Pokemon llevan mucho tiempo lanzandose y cada nuevo grupo de Pokemones sale en nuevos juegos que conforman una Generacion. Es decir, las entregas de ciertos juegos forman parte de cierta generacion del 1 al 9. Por ejemplo, la Generacion 3 introdujo, entre otros, a los juegos de Pokemon Ruby, Zafiro y Esmeralda, asi como pokemones como Metagross.
- Movimiento: Es la ejecucion de una accion en combate de un Pokemon. Cada Pokemon sabe entre 1 y 4 movimientos, pudiendo olvidar uno para reemplazarlo por otr.
- Grupo de Huevo: Los pokemones para reproducirse ponen huevos. Un grupo de huevos son aquellos pokemones que son "compatibles entre si" para reproducirse.
- EVs: Son especializaciones de estadísticas para un Pokemon. Todos los pokemones tienen un máximo de 510 EVs para mejorar sus estadísticas y pueden asignarsele un máximo de 255 por estadística.
- Naturaleza: Todo Pokemon, además, tiene una Naturaleza que le aumenta una estadística y le reduce otra.

## Organizacion

Este trabajo practico es extenso y **grupal**. Deberan revisar el trabajo de sus compañeros y aplicar buenas prácticas de equipo de desarrollo así como escribir pruebas y mantener el orden.

Los grupos de este trabajo práctico son de **al menos 4 integrantes** con la posibilidad de extenderlo hasta **5 integrantes**. En general, va a ser mas sencillo organizarse con menos personas.

Los equipos conformados por 5 integrantes tendrán la obligacion de completar el punto opcional del enunciado.

## Consigna

Recibimos un proyecto el cual tenemos que desarrollar en aproximadamente un mes y medio. Consiste en implementar un sitio web para obtener información sobre Pokemones, sus movimientos y habilidades así como también la posibilidad de creación de equipos de combate (similar a https://pokemondb.net/). Adicionalmente es deseable poder crear tu propio Pokemon para customizar la página aun mas.

A continuacion presentamos las funcionalidades necesarias para la realizacion del proyecto completo.

### Página de información de un Pokemon

Se debe servir una página que muestre la siguiente informacion de un Pokemon cualquiera en base a su nombre o ID:

- Imagen del pokemon
- Informacion de la Pokedex (National Dex ID, Type, Height, Weight, Abilities/Hidden Abilities)
- Grupo de huevo (Egg group)
- Estadísticas base (ATK, DEF, SPDEF, SPATK, HP, SPEED, TOTAL)
- Tabla de debilidades de tipos
- Visualizacion de sus evoluciones
- Movimientos aprendibles por el pokemon al subir de nivel
- Movimientos aprendibles por el pokemon al evolucionar
- Movimientos aprendibles por el pokemon usando TMs (time machines)
- Movimientos aprendibles por el pokemon segun su Grupo de Huevo

### Página de información de movimientos

Se debe servir una página que muestre la siguiente informacion de un movimiento cualquiera en base a su nombre o ID:

- Tipo de movimiento (Roca, Planta, etc)
- Categoria (Fisico/Estado/Especial, etc)
- Potencia (Power)
- Precision (Accuracy)
- Usos (PP)
- Generacion en la que fue introducido el movimiento
- Effecto en texto
- Pokemones que lo aprenden al subir de nivel
- Pokemones que lo aprenden al evolucionar
- Pokemones que lo aprenden con TMs (time machines)
- Pokemones que lo aprenden segun su Grupo de Huevo

### Página de creacion de equipos

Se requiere ademas poder crear nuestro propio equipo de Pokemones. Sin embargo la escena competitiva del juego limita contenido hasta ciertas generaciones, por lo tanto es importante únicamente crear equipos en base a la última generacion disponible que el creador del equipo permita (esto incluye Pokemones, movimientos, habilidades, etc).

Para ello debemos servir una página que le permita a un usuario que indique la generacion límite y en base a eso pueda:

- Seleccionar pokemones para agregar a su equipo dentro de los límites pedidos.
- Seleccionar movimientos para enseñarle a un Pokemon.
- Filtrar Pokemones y movimientos bajo ciertas caracteristicas como:
	- Tipo
	- Categoria
	- Mínimo o máximo valor de estadística
- Asignar las EVs a cualquier Pokemon del equipo
- Asignar la naturaleza a un Pokemon
- Obtener un equipo creado
- Editar un equipo en caso de ser necesario
- Crear o guardar un equipo para luego usarlo

Debe poder crearse un equipo Pokemon indicando la generación del equipo deseada y limitar a la creación solamente movimientos o Pokemones que existan en dicha generacion (es decir, que hayan sido introducidos por esa generación o una anterior).


### OPCIONAL: Página de creación de Pokemones

El organizador del proyecto mostró su deseo de también crear sus propios Pokemones, similar a lo que ofrece [esta página](https://pokemon.alexonsager.net/). Ésto implicaría que, para crear un Pokemon, necesitamos de otros 2 para usarlos como "padres".

El Pokemon creado debe cumplir ciertas condiciones en base a sus padres:

- Debe compartir al menos un tipo con AMBOS padres.
- Debe tener una cantidad de estadística total exactamente igual al promedio de sus padres
- Debe compartir al menos una habilidad con AMBOS padres
- Puede aprender cualquier movimiento que sus padres puedan
- No tiene evoluciones
- Comparte el resto de sus features con alguno de sus padres (altura, peso, etc)
- Tiene una imagen customizada que combine las caracteristicas de ambos Pokemones, por ejemplo [este pokemon](https://pokemon.alexonsager.net/25/11) que es la combinacion de `Pikachu` y `Metapod`

Este requisito, de formar grupos de 5 personas, pasa a ser **obligatorio**.

## Parte 1

Dado que va a ser un trabajo extenso, se decidió dividir el desarrollo en 3 "etapas" o "sprints" de ~2 semanas cada una. En esta parte se explica lo necesario para realizar la primera entrega, el `Backend` del sitio.

Se necesita, para soportar la funcionalidad pedida, implementar una JSON API con _al menos_ los siguientes **endpoints** descritos en el siguiente [Trello](https://trello.com/b/bPw9uhmG/test). Este Trello no incluye la funcionalidad opcional, de tener un grupo de 5 integrantes, les daremos las tareas necesarias para completarlo.

En ese tablero se encuentran una descripción más detallada de lo que debe hacer cada uno de los endpoints. Deben **crear una copia del mismo** y utilizarla para organizarse a la hora de desarrollar el trabajo.

Para la creación de dichos endpoints y la resolución de las tareas en cuestión, utilizar los archivos que se encuentran en la sección de Archivos Disponibles.

## Archivos Disponibles

Se adjunta [aquí]() un zip con los archivos .csv con la información necesaria para suportar la funcionalidad del trabajo. Algunos archivos se repiten con el TP1 pero no todos.

**IMPORTANTE**: el archivo `pokemon.csv` contiene la información básica de todos los Pokemon, pero no su imagen. Para ello vamos a usar imágenes ya subidas a la Internet. De manera que el endpoint que muestra información de un Pokemon, en el campo de la imagen debe mostrar una URL con este formato

`https://raw.githubusercontent.com/PokeAPI/sprites/master/sprites/pokemon/<id>.png`

reemplazar `<id>` por el ID del pokemon que se quiere mostrar.


## Flujo de trabajo en equipo

El flujo de trabajo esperado es el siguiente:

- Alumno 1 decide resolver la tarjeta `Endpoint GET pokemons`
- Alumno 1 se agrega a la tarjeta y la mueve a la columna "In-progress"
- Alumno 1 crea su rama de trabajo y realiza su trabajo, una vez listo pushea y realiza un PR.
- Alumno 1 mueve la tarjeta a "In-review" y notifica a sus compañeros que terminó su tarea.
- Alumno X revisa el PR de su compañero, dejando comentarios de ser necesario. En caso de que no haya comentarios, aprobar el PR.
- Alumno 1 revisa los comentarios de haberlos, los resuelve y realiza el paso anterior nuevamente. En caso de que el PR esté aprobado, Alumno 1 lo mergea.
- Alumno 1 mueve la tarjeta a "Done"

En caso de necesitar agregar alguna tarea, sientanse libres de hacerlo.

Es requisito para la aprobación del trabajo práctico que cada integrante haya resuelto **al menos una de las tareas** y que haya revisado y aprobado **al menos un PR** de algun compañero. En caso de que un integrante no cumpla el requisito tendrá el trabajo desaprobado.

## Exigencias de entrega Parte 1

- El repositorio debe tener la siguiente estructura:
	- Debe estar creado bajo una organización cuyo nombre será el nombre elegido para el grupo. Incluir en la organización a todos los miembros del grupo y al corrector asignado.
	- Una rama `main`/`master` protegida que requiera de aprobación para mergearse en ella.
	- Una rama `parte_1` donde se harán todos los PRs de los integrantes del equipo y se mergearán los cambios. Esta rama tendrá un PR a `main`/`master` que será la entrega de esta parte.
	- Un .gitignore que incluya los contenidos comunes de Python y los archivos csv/imagenes si los hubiese.
- Cada integrante debe resolver al menos una de las tareas descriptas en el Trello y revisar/aprobar una de las tareas de sus compañeros.
- Se requiere que el código esté probado correctamente con un coverage de al menos **75%**.
- Cada integrante debe tener un ambiente virtual de desarrollo (venv) localmente instalado.
- El backend pedido debe ser implementado utilizando `FastAPI`. Si bien la estructura del código no va a ser analizada en profundidad, se recomienda seguir la estructura y lineamientos establecidos en clase.
- El código debe ser probado con pruebas unitarias utilizando `pytest`.
- No es necesario que la información se persista entre distintas ejecuciones. Pueden cargar la información base de los CSV y mantenerla en memoria durante la ejecución del servidor.
- No subir los archivos de **csv** o imágenes utilizados para el desarrollo del trabajo práctico (aprovechar el .gititnore)
- En caso de usar alguna librería que no sea de la libería standard de Python (es decir, si hay que usar `pip` o algún otro manejador de paquetes para usarla) no vista en clase consultar con su corrector antes de utilizarla.