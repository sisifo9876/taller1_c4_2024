A.Conceptos Fundamentales
    I.¿Qué es un servicio REST?
        -Un servicio REST (Representational State Transfer) es un tipo de arquitectura 
        para diseñar servicios web que permite la comunicación entre sistemas
        a través del protocolo HTTP.
    II.¿Cuáles son los principios del diseño RESTful?
        -Arquitectura Cliente-Servidor: El cliente y el servidor son entidades separadas que se comunican a través de una red. 
        Esta separación permite que ambos se desarrollen de forma independiente.
        Sin Estado (Stateless): Cada solicitud del cliente al servidor debe contener toda la información necesaria para entender y procesar la solicitud.
        El servidor no almacena ninguna información sobre el estado del cliente entre las solicitudes.
        Cacheable: Las respuestas del servidor pueden ser almacenadas en caché por el cliente. Esto mejora el rendimiento al reducir la carga en el servidor y la red.
        Interfaz Uniforme: La API debe tener una estructura consistente y predecible. Esto facilita a los desarrolladores entender y usar la API.
        Incluye el uso de métodos HTTP estándar (GET, POST, PUT, DELETE) y URIs para identificar recursos.
        Sistema en Capas: La arquitectura puede estar compuesta por capas jerárquicas, donde cada capa tiene una funcionalidad específica.
        Esto ayuda a mejorar la escalabilidad y la seguridad.
        Código Bajo Demanda (opcional): Los servidores pueden proporcionar código ejecutable al cliente cuando sea necesario, lo que permite extender la funcionalidad
        del cliente.
    III.¿Qué es HTTP y cuáles son los métodos HTTP más comunes?
        -HTTP (Hypertext Transfer Protocol) es el protocolo utilizado para la transferencia de información en la web.
        Es la base de la comunicación de datos en la World Wide Web y define cómo se formatean y transmiten los mensajes, así como las acciones que los servidores web
        y los navegadores deben tomar en respuesta a varios comandos.
        -Métodos HTTP más comunes:
        GET: Solicita una representación de un recurso específico. Las peticiones que usan GET solo deben recuperar datos y no deben tener efectos secundarios.
        POST: Se utiliza para enviar datos a un servidor para crear o actualizar un recurso. Esto puede causar cambios en el estado del servidor o tener efectos secundarios.
        PUT: Reemplaza todas las representaciones actuales del recurso de destino con la carga útil de la petición.
        DELETE: Borra un recurso específico.
        HEAD: Pide una respuesta idéntica a la de una petición GET, pero sin el cuerpo de la respuesta. Es útil para obtener metadatos de un recurso sin descargar
        su contenido.
        OPTIONS: Describe las opciones de comunicación para el recurso de destino. Es útil para comprobar qué métodos HTTP son soportados por el servidor.
        PATCH: Se utiliza para aplicar modificaciones parciales a un recurso1.Estos métodos permiten a los desarrolladores interactuar con los recursos web 
        de manera eficiente y estructurada.
    IV.¿Qué es un recurso en el contexto de un servicio REST?
        -En el contexto de un servicio REST,un recurso es cualquier tipo de información que puede ser nombrada y manipulada a través de un URI (Uniform Resource Identifier).
        Los recursos son los elementos fundamentales con los que interactúan los clientes y servidores en una arquitectura RESTful.
    V.¿Qué es un endpoint?
        Un endpoint en el contexto de una API REST es una URL específica a la que se puede enviar una solicitud para interactuar con un recurso.
        Los endpoints son los puntos de acceso a los recursos y definen las rutas a través de las cuales los clientes pueden realizar operaciones como obtener,
        crear, actualizar o eliminar datos.
B.Estructura de un Servicio REST
    I.¿Qué es un URI y cómo se define?
        -Un URI (Uniform Resource Identifier) es una cadena de caracteres que identifica de manera única un recurso en Internet. Los URIs son fundamentales para la web, 
        ya que permiten localizar y acceder a recursos como páginas web, imágenes, videos, y más.
    II.¿Qué es una API RESTful?
        Una API RESTful es una interfaz de programación de aplicaciones (API) que sigue los principios de diseño de la arquitectura REST (Representational State Transfer).
        Estas APIs permiten la comunicación entre diferentes sistemas a través de HTTP, utilizando métodos estándar como GET, POST, PUT y DELETE.
    III.¿Qué son los códigos de estado HTTP y cómo se usan en REST?
        -Los códigos de estado HTTP son números de tres dígitos que el servidor devuelve en respuesta a una solicitud HTTP del cliente. Estos códigos indican 
        si la solicitud se ha completado con éxito y proporcionan información sobre el resultado de la operación. En el contexto de una API RESTful,
        los códigos de estado son esenciales para la comunicación entre el cliente y el servidor, ya que ayudan a entender el estado de la solicitud 
        y cualquier acción adicional que pueda ser necesaria.
        -En una API RESTful, los códigos de estado HTTP se utilizan para comunicar el resultado de las operaciones solicitadas por el cliente.
    IV.Agregar una tabla con los códigos HTTP de respuesta más comunes, y su significado.
        -100 Continue: El servidor ha recibido los encabezados de la solicitud y el cliente debe proceder a enviar el cuerpo de la solicitud.
         200 OK: La solicitud ha tenido éxito.
         201 Created: La solicitud ha tenido éxito y se ha creado un nuevo recurso.
         204 No Content: La solicitud ha tenido éxito, pero no hay contenido que devolver.
         301 Moved Permanently: El recurso solicitado ha sido movido permanentemente a una nueva URL.
         302 Found: El recurso solicitado se encuentra temporalmente en una URL diferente.
         400 Bad Request: La solicitud no pudo ser entendida o estaba malformada.
         401 Unauthorized: La solicitud requiere autenticación.
         403 Forbidden: El servidor entiende la solicitud, pero se niega a autorizarla.
         404 Not Found: El recurso solicitado no pudo ser encontrado.
         500 Internal Server Error: El servidor encontró una condición inesperada que le impidió cumplir con la solicitud.
         503 Service Unavailable: El servidor no está disponible temporalmente, generalmente debido a mantenimiento o sobrecarga.
    V.¿Qué es JSON y por qué se usa comúnmente en APIs REST?
        -JSON (JavaScript Object Notation) es un formato ligero y fácil de leer para el intercambio de datos.Se usa comúnmente en APIs REST por estas razones:
         Simplicidad: Fácil de entender y escribir.
         Compatibilidad: Funciona con cualquier lenguaje de programación.
         Eficiencia: Más ligero que otros formatos como XML.
         Facilidad de Uso: Muchas bibliotecas integradas para trabajar con JSON.
