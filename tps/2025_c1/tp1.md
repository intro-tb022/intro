---
math: true
---

{% assign tp = site.data.trabajos.TP1 %}
{% capture fecha %}{{tp.entrega | date: "%e/%m"}}{% endcapture %}

# TP1 - PokeScript

## Temas a evaluar

- Manejo de terminal
- Bash scripting
- Piping
- Git

## Glosario

- **Pokemon**: monstruo ficticio de la serie animada japonesa Pokemon. Son comunmente utilizados para enfrentarse en batallas entre si. Actualmente hay mas de mil Pokemones. Un clásico ejemplo es Pikachu. Considerar que no existe un unico Pikachu en el mundo, pueden haber infinitos.
- **Tipo**: uno de los atributos que puede tener un Pokemon. Hay un total de 18 tipos diferentes en Pokemon. Los Pokemones pueden tener hasta un máximo de 2 tipos. Definen la efectividad y resistencia de los ataques que afecten al Pokemon.
- **Estadística**: al igual que el tipo, las estadísticas son los atributos que tiene un Pokemon. Existen las estadísticas de Ataque (ATK), Defensa (DEF), HitPoints (HP), Ataque Especial (SPATK), Defensa Especial (SPDEF) y Velocidad (SPEED). Todos los Pokemones tienen distintas estadisticas base, pero por ejemplo todos los Pikachu tienen las mismas estadisticas base.
- **Habilidad**: efecto, usualmente beneficioso, que afecta a un Pokemon. Cada Pokemon tiene un pool de habilidades con las que puede existir, sin embargo, un Pokemon siempre tiene exactamente una Habilidad.

## Consigna

Se puede encontrar la consigna en [este link](https://classroom.github.com/a/mDEWbb-b) del Github Classroom de este cuatrimestre. Deben tener una cuenta de Github creada y con ella podrán identificarse con su padrón y acceder.