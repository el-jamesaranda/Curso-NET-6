# Etapa 3 - SQL con SQL Server
En esta etapa veremos los fundamentos del lenguaje SQL, utilizando el motor de bases de datos MS SQL Server 2019. Veremos desde los comandos DDL y DML básicos, hasta el uso de triggers y transacciones en la BD.

## Contenido
Revisa y realiza lo indicado en los videos tutoriales de la siguiente lista de reproducción en YouTube: [SQL con SQL Server](https://www.youtube.com/playlist?list=PL0-hIHBwsOM6Bsv8ZNK4YnD3T-GtK40Jl).

También puedes apoyarte en el archivo PDF adjunto a esta etapa.

## Actividad - Modificar base de datos "Bank" y generar backup
A continuación se describe la actividad que deberás realizar.

### Objetivo
Deberás realizar las siguientes modificaciones a la base de datos 'Bank' y, posteriormente, deberás generar un backup de la BD.

### Instrucciones
- Crea un nuevo procedimiento almacenado, llamado **SelectClient**:
  - El procedimiento recibirá un sólo parámetro, llamado **@ClientID**, que puede ser **nulo**.  
    - Si el parámetro es nulo, ejecuta un **SELECT** para traer toda la información de todos los registros de **Client**.
    - Si el parámetro no es nulo, ejecuta un **SELECT** para traer toda la información del registro de **Client** con ese valor en su **ID**.
- Modifica el procedimiento almacenado **InsertClient** de la siguiente manera:
  - Agrega una validación para que el valor de la columna **Email** de la tabla **Client** no se repita. Si se introduce un valor que ya existe, el procedimiento no ejecutará el **INSERT** y deberá **devolver un mensaje** al usuario.
  - Puedes investigar el uso de la palabra clave **RETURN** de **T-SQL**.
- Modifica el procedimiento almacenado **InsertBankTransaction** de la siguiente manera:
  - Agrega una validación para el escenario en el que la variable **@NewBalance** sea menor que 0. Si la variable es menor que 0, el procedimiento deberá **devolver un mensaje** al usuario.
  - Puedes investigar el uso de la palabra clave **RETURN** de **T-SQL**.
- Genera un full backup de la base de datos **Bank**:
  - Investiga el uso del comando **BACKUP DATABASE**. 

### Forma de entrega
- Crea un video corto la ejecución de los tres procedimientos almacenados especificados en las **Instrucciones**, súbelo a YouTube y comparte el enlace en la vía indicada.
- Sube tu archivo **.bak** a un repositorio público en tu cuenta de GitHub y comparte el enlace en la vía indicada.
