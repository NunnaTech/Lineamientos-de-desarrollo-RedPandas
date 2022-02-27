# 10. Desarrollo y consumo de APIs

Las aplicaciones que se desarrollan y se guían por reglas para poder obtener un producto de calidad, deben de tener independencia de la plataforma, esto quiere decir, que los programas escritos en cierto lenguaje pueden ejecutarse en cualquier tipo de hardware. Todo esto se logra utilizando arquitectura REST, esta característica debe ser implementada para el consumo interno de la aplicación, así también para hacer operaciones con otras aplicaciones.

Las operaciones que se realizan en la aplicación deben tener el protocolo HTTP, este es el mediador entre las peticiones del cliente y las respuestas del servidor para hacer una comunicación fluida, se tienen algunos métodos de petición para poder indicar la acción que se desea realizar para un recurso determinado estos son: 

- **GET**: Permite realizar es solicitar un recurso.
- **POST**: Permite crear un nuevo recurso.
- **DELETE**: Elimina un recurso.
- **PUT**: Modificación de un recurso existente.

Existen más métodos que se pueden solicitar, pero estos 4 son los métodos más utilizados principalmente para realizar operaciones CRUD (create, read, update y delete).

## 10.1 Interacción con servicios legados

Cuando se tiene un sistema nuevo y este quiere interactuar con sistemas antiguos se debe hacer mediante una integración, la arquitectura REST es la que va a ayudar en que se puede intercambiar información por parte de las nuevas aplicaciones.

## 10.2 Exposición y autentificación de servicios

Al usar los servicios REST se deben utilizar mecanismos donde puedan autenticarse para tener así un consumo privado, de igual manera se debe de mantener el token que se compartirá con las demás aplicaciones realizando así el intercambio de información entre las aplicaciones de una manera eficiente.

Al diseñar la aplicación se debe considerar que consumirá y proveerá recursos por medio de la arquitectura REST, por lo que es necesario el uso de funciones y/o frameworks que permitan lograr desarrollar un buen servicio.

## 10.3 Desarrollo orientado a interoperabilidad

La definición de URI de recursos debe de seguir las prácticas con ejemplos, como:

- Usar sustantivos para describir los recursos:
» GET /usuarios/ lista todos los usuarios
» GET /usuarios/12 muestra detalle del usuario con ID 12
    
    » POST /usuarios crear usuario
    » PUT /usuarios/12 actualiza usuario con ID 12
    » DELETE /usuarios/12 borra al usuario con ID 12.
    
- Usar “/” para indicar la relación de jerarquía:
» GET /usuarios/12/mensajes muestra mensajes del usuario con ID 12
» GET /usuarios/12/mensajes/93 obtiene mensaje con ID 93 del usuario con ID 12
- Usar parámetros de consulta (query strings) para realizar operaciones de filtro, ordenamiento, paginación y/o búsqueda:
    
    » GET /instituciones/2/usuarios?estado=inactivo lista todos los usuarios de la institución 2 con estado inactivo.
    
- Formato de las URIs:
    
    » No usar “/” al final de la URI.
    » No usar mayúsculas.
    /instituciones/2/usuarios ✔
    /Instituciones/2/Usuarios/ ❌
    
- Usar guion “-” (y no guion bajo “_”) para facilitar la comprensión de la URI:
/oficinas/134/como-llegar ✔
/oficinas/134/como_llegar ❌
- No usar extensiones de archivos:
    
    /instituciones/2/descripcion ✔
    /instituciones/2/descripcion.txt ❌
    /instituciones/2/descripcion.json ❌