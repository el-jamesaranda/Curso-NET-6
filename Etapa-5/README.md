# Etapa 5 - Seguridad en APIs
En esta etapa vamos a restringir el acceso a los controllers que hemos definido en la API, de manera que solamente usuarios registrados en la base de datos puedan acceder a ellos. Para esto, utilizaremos JSON Web Tokens (JWT) que formarán parte de las solicitudes hacia la API.

## Contenido
Revisa y realiza lo indicado en los videos tutoriales de la siguiente lista de reproducción en YouTube (a partir del video 15): [Controllers API con ASP.NET Core 6](https://tinyurl.com/2pn6tdwt).

También puedes apoyarte en el archivo PDF adjunto a esta etapa.

## Actividad - Crear controller para BankTransaction 
A continuación se describe la actividad que deberás realizar.

### Objetivo
Deberás construir un controller para el modelo **BankTransaction**; que deberá estar restringido por JWT. Los registros de **Client** podrán interactuar con el controller para 1) Consultar todas sus cuentas. 2) Realizar retiros de sus cuentas. 3) Realizar depósitos a sus cuentas. 4) Eliminar sus cuentas.

### Instrucciones
- Modifica la tabla **Client**: agrega una nueva columna llamada **Pwd** para almacenar la contraseña del cliente. Notas:
  - La columna **Pwd** puede ser simplemente un **varchar**, aunque puedes encriptar el valor si así lo deseas.
  - Este cambio va a requerir que **actualizes tu modelo** en el código.
- Genera un proceso para autenticar a los registros de **Client**:
  - Puedes trabajar con el **LoginController** que ya definimos (pero enfocado al modelo **Client**) o puedes crear otro controller.
- Genera un JWT con los **claims** del registro de **Client**. Así como en el tutorial, puedes incluir solamente las propiedades **Name** e **Email**.
- Crea un controller para el modelo **BankTransaction**. En este controller, los clientes podrán:
  1. **Consultar todas sus cuentas**. Ojo, un cliente sólamente debe poder ver sus cuentas, no las de otros clientes.  
  2. **Realizar retiros de sus cuentas**. Los retiros podrán ser vía transferencia (asociados a cuentas externas o propias) o en efectivo (sin cuentas externas asociadas).
  3. **Realizar depósitos a sus cuentas**. Los depósitos sólo podrán ser en efectivo (sin cuentas asociadas).
  4. **Eliminar sus cuentas**. Una cuenta sólo podrá ser eliminada si ya no dispone de dinero.
- El controller deberá estar **restringido al token** que acabas de crear.
- Deberás conservar el token para la autenticación de los registros de **Administrator**. Por lo que tu API trabajará con **dos tokens**:
  - Investiga el tema de **Policies** para la autorización en ASP.NET Core.
  - Puedes consultar la respuesta aceptada de [esta pregunta de GitHub](https://stackoverflow.com/questions/49694383/use-multiple-jwt-bearer-authentication).

### Forma de entrega
- Crea un video corto probando los nuevos requerimientos en Postman, súbelo a YouTube y comparte el enlace en la vía indicada.
- Sube el código de tu proyecto a un repositorio público en tu cuenta de GitHub y comparte el enlace en la vía indicada.
