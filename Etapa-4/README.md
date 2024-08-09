# Etapa 4 - API con controllers y EF Core
En esta etapa vamos a crear una API con ASP.NET Core 6. Utilizaremos el ORM Entity Framework Core para generar un modelo de datos en nuestro código, a partir de una base de datos existente. Despúes vamos a crear una API con controllers, para procesar diversas solicitudes del cliente hacia la BD.

## Contenido
Revisa y realiza lo indicado en los videos tutoriales de la siguiente lista de reproducción en YouTube (hasta el video 13): [Controllers API con ASP.NET Core 6](https://tinyurl.com/2pn6tdwt).

También puedes apoyarte en el archivo PDF adjunto a esta etapa.

## Actividad - Crear controller para Account 
A continuación se describe la actividad que deberás realizar.

### Objetivo
Deberás construir un controller para el modelo Account.

### Instrucciones
- Crea un controller para el modelo **Account** (llamado **AccountController**):
  - Crea los métodos para procesar las solicitudes **GET** (**GetAll** y **GetByID**).  
  - Crea el método para procesar la solicitud **POST**:
    - Recuerda que tanto **Id** como **RegDate** se asignan automáticamente después del INSERT (no debes proporcionar esos campos en el objeto de la solicitud).
    - Si el valor del campo **ClientId** no existe en la BD, deberás generar un **Bad Request (400 status)**.
  - Crea el método para procesar la solicitud **PUT**:
    - Si el valor del campo **ClientId** no existe en la BD (si se quiere asignar la cuenta a otro cliente), deberás generar un **Bad Request (400 status)**.
  - Crea el método para procesar la solicitud **DELETE**.
- Deberás generar también la clase **AccountService**, en la carpeta **Service**. Ahí realizarás las operaciones adecuadas en el **contexto**; el controller va a consumir este servicio.

### Forma de entrega
- Crea un video corto probando el nuevo controller en Postman, súbelo a YouTube y comparte el enlace en la vía indicada.
- Sube el código de tu proyecto a un repositorio público en tu cuenta de GitHub y comparte el enlace en la vía indicada.
