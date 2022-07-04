# Etapa 1 - Introducción a C#
Esta etapa abarca algunos de los conceptos más importantes de programación, enfocados en el lenguaje C#.

## Contenido
Revisa y realiza lo indicado en los videos tutoriales de esta [Lista de Reproducción](https://www.youtube.com/playlist?list=PL0-hIHBwsOM525xhkhjAwcSZ4htMKdQIH) en YouTube.

También puedes apoyarte en el archivo PDF adjunto a esta etapa.

## Actividad - Cajas de banco
A continuación se describe la actividad que deberás realizar.

### Objetivo
Deberás implementar un programa que simule el comportamiento del servicio de cajas de un banco. A partir de un conjunto de cantidades de dinero que ingrese el usuario, el
programa imprimirá en consola la cantidad mínima de billetes y monedas que se deben entregar para esas cantidades.

## Instrucciones
- Deberás implementar un menú que permita al usuario escoger dos opciones, como en la siguiente imagen:
- Al seleccionar la primera opción, el programa preguntará al usuario la cantidad de retiros (sólo enteros positivos, con un valor máximo de 10) y posteriormente el usuario ingresará la cantidad de dinero (sólo enteros positivos, con un valor máximo
de 50,000) de cada retiro. Al terminar de ingresar las cantidades, el programa mostrará nuevamente el menú.
- Al seleccionar la segunda opción, el programa imprimirá en consola la cantidad mínima de billetes y monedas que se entregaron para cada cantidad. Se mostrará el
mensaje “Presiona ‘enter’ para continuar …” y cuando el usuario presione la tecla enter, el programa volverá al menú.
- La cantidad de dinero que se ingresará para cada retiro deberá ser un valor entero, mayor a 0 y menor o igual a 50,000.
- Los billetes que se considerarán en el programa serán de $500, $200, $100, $50 y $20 pesos.
- Las monedas que se considerarán en el programa serán de $10, $5 y $1 peso.
- Recuerda que se deberá imprimir la cantidad mínima de billetes y monedas para cada retiro. Por ejemplo, la cantidad de $2346 pesos necesita:
  - 4 billetes de $500 + 1 billete de $200 + 1 billete de $100 + 2 billetes de $20 = 8 billetes ($2340).
  - 1 moneda de $5 + 1 moneda de $1 = 2 monedas ($6).
- Deberás utilizar un arreglo que almacene los retiros del usuario.
- Considera bucles que aumenten contadores de billetes y monedas en cada iteración y que, además, también disminuyan la cantidad del retiro en cada iteración

### Forma de entrega
Deberás crear un repositorio público en tu cuenta de GitHub, y compartir el enlace del repositorio en la forma indicada.
