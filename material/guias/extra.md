# Ejercicios extra

Estos ejercicios utilizan otros comandos no vistos en clase o cosas muy particulares de ellos. Van a necesitar investigar por su cuenta para poder resolverlos.

1. Escribir un script que dado un archivo devuelva la palabra con más apariciones y el número de apariciones (ignorar todos los caracteres que no sean texto, `"casa."` y `"Casa"` son la misma palabra)

1. Escribir un script que dado un archivo devuelva la línea más larga del mismo

1. Escribir un script que cada 60 segundos muestre cual es el proceso que está consumiendo más memoria

1. Escribir un script que funcione como un servicio \[[linux services](https://www.linuxtotal.com.mx/index.php?cont=info_admon_003) / [macOS services](https://mi-do.medium.com/homebrew-services-how-to-use-how-it-works-and-alternatives-8414bc0ad78c)] que cada vez que se inicie el sistema operativo genere un nuevo archivo en el directorio `~/dias_de_arranque` con la fecha y hora del día (formato `YYYY-MM-DD HH:MM:SS`).

1. Escribir un script de bash que usando los archivos generador por el servicio anterior muestr por stdout los días de la semana en los cuales el sistema operativo se inició sin repetir (si múltiples fechas son un día martes, mostrar martes una sola vez).