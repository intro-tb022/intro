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
- EVs: Son especializaciones de estadisticas para un Pokemon. Todos los pokemones tienen un máximo de 510 EVs para mejorar sus estadisticas y pueden asignarsele un máximo de 255 por estadistica.
- Naturaleza: Todo Pokemon, además, tiene una Naturaleza que le aumenta una estadistica y le reduce otra.

## Organizacion

Este trabajo practico es extenso y **grupal**. Deberan revisar el trabajo de sus compañeros y aplicar buenas prácticas de equipo de desarrollo así como escribir pruebas y mantener el orden.

Los grupos de este trabajo práctico son de **al menos 4 integrantes** con la posibilidad de extenderlo hasta **5 integrantes**. En general, va a ser mas sencillo organizarse con menos personas.

Los equipos conformados por 5 integrantes tendran la obligacion de completar el punto opcional del enunciado.

## Consigna

Recibimos un proyecto el cual tenemos que desarrollar en aproximadamente un mes y medio. Consiste en implementar un sitio web para obtener información sobre Pokemones, sus movimientos y habilidades así como también la posibilidad de creación de equipos de combate (similar a https://pokemondb.net/). Adicionalmente es deseable poder crear tu propio Pokemon para customizar la pagina aun mas.

A continuacion presentamos las funcionalidades necesarias para la realizacion del proyecto.

### Pagina de informacion de un Pokemon

Se debe servir una pagina que muestre la siguiente informacion de un pokemon cualquiera en base a su nombre o ID:

- Imagen del pokemon
- Informacion de la Pokedex (National Dex ID, Type, Height, Weight, Abilities/Hidden Abilities)
- Grupo de huevo (Egg group)
- Estadisticas base (ATK, DEF, SPDEF, SPATK, HP, SPEED, TOTAL)
- Tabla de debilidades de tipos
- Visualizacion de sus evoluciones
- Movimientos aprendibles por el pokemon al subir de nivel
- Movimientos aprendibles por el pokemon segun su Grupo de Huevo
- Movimientos aprendibles por el pokemon al evolucionar
- Movimientos aprendibles por el pokemon usando TMs (time machines)

### Pagina de informacion de movimientos

Se debe servir una pagina que muestre la siguiente informacion de un movimiento cualquiera en base a su nombre o ID:

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

### Pagina de creacion de equipos

Se requiere ademas poder crear nuestro propio equipo de pokemones. Sin embargo la escena competitiva del juego limita contenido hasta ciertas generaciones, por lo tanto es importante unicamente crear equipos en base a la ultima generacion disponible que el creador del equipo permita (esto incluye pokemones, movimientos, habilidades, etc).

Para ello debemos servir una pagina que le permita a un usuario que indique la generacion limite y en base a eso pueda:

- Seleccionar pokemones para agregar a su equipo dentro de los limites pedidos.
- Seleccionar movimientos para enseñarle a un Pokemon.
- Filtrar pokemones y movimientos bajo ciertas caracteristicas como:
	- Tipo
	- Categoria
	- Estadistica minima o maxima
- Asignar las EVs a cualquier Pokemon del equipo
- Asignar la naturaleza a un Pokemon
- Obtener un equipo creado
- Editar un equipo en caso de ser necesario
- Crear o guardar un equipo para luego usarlo

Debe poder crearse un equipo pokemon indicando la generacion del equipo deseada y limitar a la creacion solamente movimientos o pokemones que existan en dicha generacion.


### OPCIONAL: Pagina de creacion de pokemones

El organizador del proyecto mostro su deseo de tambien crear sus propios pokemones, similar a lo que ofrece [esta pagina](https://pokemon.alexonsager.net/). Esto implicaria que, para crear un pokemon, necesitamos de otros 2 para usarlos como "padres".

El pokemon creado debe cumplir ciertas condiciones en base a sus padres:

- Debe compartir al menos un tipo con AMBOS padres.
- Debe tener una cantidad de estadistica total exactamente igual al promedio de sus padres
- Debe compartir al menos una habilidad con AMBOS padres
- Puede aprender cualquier movimiento que sus padres puedan
- No tiene evoluciones
- Comparte el resto de sus features con alguno de sus padres (altura, peso, etc)
- Tiene una imagen customizada que combine las caracteristicas de ambos pokemones, por ejemplo [este pokemon](https://pokemon.alexonsager.net/25/11) que es la combinacion de `Pikachu` y `Metapod`

Este requisito, de formar grupos de 5 personas, pasa a ser **obligatorio**.

## Parte 1

Dado que va a ser un trabajo extenso, se decidió dividir el desarrollo en 3 "etapas" o "sprints" de 2 semanas cada una. En esta parte se explica lo necesario para realizar la primera entrega, el `Backend` del sitio.

Se necesita, para soportar la funcionalidad pedida, implementar _al menos_ los siguientes **endpoints** descritos en el siguiente [Trello](https://trello.com/b/bPw9uhmG/test). Este trello no incluye la funcionalidad opcional, de tener un grupo de 5 integrantes, les daremos las tareas necesarias para completarlo.

En ese tablero se encuentran una descripción más detallada de lo que debe hacer cada uno de los endpoints. Deben crear una copia del mismo y utilizarlo para organizarse a la hora de desarrollar el trabajo.

Para la creación de dichos endpoints y la resolución de las tareas en cuestión, utilizar los archivos que se encuentran en la sección de Documentos disponibles.

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

## Exigencias de entrega

- El repositorio debe tener la siguiente estructura:
	- Una rama `main`/`master` protegida que requiera de aprobación para mergearse en ella.
	- Una rama `parte_1` donde se haran todos los PRs de los integrantes del equipo y se mergearan los cambios. Esta rama tendra un PR a main que sera la entrega de esta parte.
	- Un .gitignore que incluya los contenidos comunes de python y los archivos csv/imagenes.
- Cada integrante debe resolver al menos una de las tareas descriptas en el Trello y revisar/aprobar una de las tareas de sus compañeros.
- Se requiere que el código esté probado correctamente con un coverage de al menos **75%**.
- Cada integrante debe tener un ambiente virtual de desarrollo (venv) localmente instalado.
- El backend pedido debe ser implementado utilizando `FastAPI`.
- El código debe ser probado con pruebas unitarias utilizando `pytest`.
- No subir los archivos de **csv** o imagenes utilizados para el desarrollo del trabajo práctico.
- En caso de usar alguna librería no vista en clase consultar con su corrector antes de utilizarla.