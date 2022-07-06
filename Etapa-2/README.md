# Etapa 2 - Programación Orientada a Objetos (y Git/GitHub)
En esta etapa veremos algunos de los conceptos más importantes en la POO, además, veremos algunos de los comandos más importantes de git y el flujo de trabajo en GitHub.

## Contenido
Revisa y realiza lo indicado en los videos tutoriales de las siguientes listas en YouTube: [POO en C#](https://www.youtube.com/playlist?list=PL0-hIHBwsOM4Ajlgt1Qis08nI9Hqakw7K) y [Git y Github](https://www.youtube.com/playlist?list=PL0-hIHBwsOM6uP8_ITUhDSt18uOq3MM_O).

También puedes apoyarte en los archivos PDF adjuntos a esta etapa.

## Actividad - Completar proyecto "BankConsole"
A continuación se describe la actividad que deberás realizar.

### Objetivo
Deberás completar el proyecto "BankConsole" que se mostró en los videos tutoriales, para agregar las validaciones necesarias a los procesos de agregar y eliminar usuarios a través de la terminal.

### Instrucciones
- Vas a trabajar en el menú que muestra la aplicación (cuando se ejecuta con argumentos), para mejorar los procesos de agregar y eliminar usuarios:

![BankConsoleMenu](https://user-images.githubusercontent.com/45106990/177648772-147d330f-a2c2-43a2-8465-5e7e98750206.png)

- Al **agregar usuarios**, deberás validar lo siguiente:
  - El **ID** debe ser un **entero positivo**; si no se ingresa un valor correcto, la aplicación mostrará un mensaje y permitirá volver a ingresarlo.
    - El **ID** ingresado **no se puede repetir**. Si ya hay un usuario con ese ID en el archivo JSON, la aplicación mostrará un mensaje y permitirá volver a ingresarlo. 
  - El **Email** debe ser un formato correcto de correo electrónico; investiga el uso de **expresiones regulares** para esta validación.
  - El **Saldo (Balance)** debe ser un **decimal positivo**; si no se ingresa un valor correcto, la aplicación mostrará un mensaje y permitirá volver a ingresarlo.
  - Al preguntar si el usuario es **Cliente** o **Empleado**, sólo se deberán permitir los caracteres **'c'** y **'e'**; si se ingresa algún otro valor, la aplicación mostrará un mensaje y volverá a pedir el valor.
- Al **eliminar usuarios**, deberás validar lo siguiente:
  - El **ID** debe ser un **entero positivo**; si no se ingresa un valor correcto, la aplicación mostrará un mensaje y permitirá volver a ingresarlo.
    - El **ID** ingresado **debe existir** en el archivo JSON. Si el ID no existe, la aplicación mostrará un mensaje y permitirá volver a ingresarlo. 

### Forma de entrega
- Crea un video corto de tu programa en ejecución, súbelo a YouTube y comparte el enlace en la vía indicada.
- Sube tu código a un repositorio público en tu cuenta de GitHub y comparte el enlace en la vía indicada.
