# HTTP STATUS CODES

> Información sobre los códigos de estado de respuesta HTTP

---

## Contenidos {docsify-ignore}
1. [Códigos de estado HTTP](#Códigos-de-estado-HTTP)
    - [Respuestas Informativas 1xx](#Respuestas-Informativas-1xx)
    - [Respuestas satisfactorias 2xx](#Respuestas-satisfactorias-2xx)
    - [Respuestas de redirección 3xx](#Respuestas-de-redirección-3xx)
    - [Errores del cliente 4xx](#Errores-del-cliente-4xx)
    - [Errores de servidor 5xx](#Errores-de-servidor-5xx)
2. [Códigos más usados en una API](#Códigos-más-usados-en-una-API)
    - [Ejemplos de errores en una API](#Ejemplos-de-errores-en-una-API)

---

## Códigos de estado HTTP

### Respuestas Informativas 1xx

- [100](https://developer.mozilla.org/es/docs/Web/HTTP/Status/100) - **Continue** - Indica que el cliente debe continuar con la solicitud o ignorarla si ya está terminada.
- [101](https://developer.mozilla.org/es/docs/Web/HTTP/Status/101) - **Switching Protocols** - El servidor acepta el cambio de protocolo propuesto por el User-Agent.
- [102](http://httpstatus.es/102) - **Processing** - El servidor ha recibido la solicitud y aún se encuentra procesándola.
- [103](https://developer.mozilla.org/en-US/docs/Web/HTTP/Status/103) - **Early Hints** - Diseñado para usarse con el encabezado _Link_ y permitir la precarga de recursos, mientras el servidor prepara una respuesta.

### Respuestas satisfactorias 2xx

- [200](https://developer.mozilla.org/es/docs/Web/HTTP/Status/200) - **Ok** - La solicitud ha tenido éxito.
- [201](https://developer.mozilla.org/es/docs/Web/HTTP/Status/201) - **Created** - La solicitud ha sido un éxito y se ha creado un nuevo recurso (PUT o POST).
- [202](https://developer.mozilla.org/es/docs/Web/HTTP/Status/202) - **Accepted** - Solicitud aceptada, pero aún no se ha procesado. Pensada para respuestas asíncronas.
- [203](https://developer.mozilla.org/es/docs/Web/HTTP/Status/203) - **Partial Information** - Solicitud completada con éxito, pero la información se ha obtenido de una copia o de un tercero.
- [204](https://developer.mozilla.org/es/docs/Web/HTTP/Status/204) - **No Response** - Solicitud ha sido un éxito, pero la respuesta no contiene contenido. Los encabezados pueden contener información nueva.
- [205](https://developer.mozilla.org/es/docs/Web/HTTP/Status/205) - **Reset Content** - Solicitud ha sido un éxito, la repuesta no tiene contenido, y el User-Agent debe inicilizar la página desde donde se realizó la petición. Ejemplo: Formularios cuyo contenido debe borrarse.
- [206](https://developer.mozilla.org/es/docs/Web/HTTP/Status/206) - **Partial Content** - La petición servirá parcialmente el contenido solicitado. Usada por herramientas de descarga para continuar la transferencia interrumpida.
- [207](https://httpstatuses.com/206) - **Multi-Status** - XML, puede contener multiples respuestas separadas.
- [208](https://httpstatuses.com/208) - **Already Reported** - La repuesta ya ha sido notificada previamente.
- [226](https://httpstatuses.com/226) - **Im Used** - Petición completada, la respuesta es el resultado de la manipulación de una o varias instancias.

### Respuestas de redirección 3xx

- [300](https://developer.mozilla.org/es/docs/Web/HTTP/Status/300) - **Multiple Choice** - Solicitud con más de una respuesta. El User-Agent o usuario debe seleccionar una de ellas.

- [301](https://developer.mozilla.org/es/docs/Web/HTTP/Status/301) - **Moved Permanently** - Significa que la URI del recurso solicitado ha sido cambiada, y automáticamente te dirige al nuevo destino.
- [302](https://developer.mozilla.org/es/docs/Web/HTTP/Status/302) - **Found** - El recurso de la URI solicitada ha sido cambiado temporalmente, y nuevos cambios serán agregados en el futuro, por lo que la  misma URI podrá ser usada en futuras solicitudes.
- [303](https://developer.mozilla.org/es/docs/Web/HTTP/Status/303) - **See Other** - El servidor envia esta respuesta para dirigir al cliente a un nuevo recurso solcitado a otra dirección usando una petición GET.
- [304](https://developer.mozilla.org/es/docs/Web/HTTP/Status/304) - **Not Modified** - Usada para propósitos de caché, le indica al cliente que la respuesta no ha sido modificada, por lo que el cliente puede seguir usando la respuesta que tiene almacenada en caché.
- [307](https://developer.mozilla.org/es/docs/Web/HTTP/Status/307) - **Temporary Redirect** - El servidor envía esta respuesta para dirigir al cliente a obtener el recurso solicitado a otra URI con el mismo metodo que se uso la petición anterior. Similar al código `302 Found`.
- [308](https://developer.mozilla.org/es/docs/Web/HTTP/Status/308) - **Permanent Redirect** - Significa que el recurso ahora se encuentra permanentemente en otra URI, especificada por la respuesta de encabezado `HTTP Location:`. Similar al código `301 Moved Permanently`.

### Errores del cliente 4xx

- [400](https://developer.mozilla.org/es/docs/Web/HTTP/Status/400) - **Bad Request** - El servidor no pudo interpretar la solicitud por una sintaxis inválida.
- [401](https://developer.mozilla.org/es/docs/Web/HTTP/Status/401) - **Unauthorized** - Es necesario autenticar para obtener la respuesta solicitada. Esta es similar a `403 Forbidden`, pero en este caso, autenticación es posible.
- [402](http://httpstatus.es/402) - **Payment Required** - Código fue creado para ser utilizado en sistemas digitales de pagos.
- [403](https://developer.mozilla.org/es/docs/Web/HTTP/Status/403) - **Forbidden** - El cliente no posee los permisos necesarios para cierto contenido, por lo que el servidor está rechazando dar una respuesta apropiada.
- [404](https://developer.mozilla.org/es/docs/Web/HTTP/Status/404) - **Not Found** - El servidor no pudo encontrar el contenido solicitado.
- [405](https://developer.mozilla.org/es/docs/Web/HTTP/Status/405) - **Method Not Allowed** - El método solicitado no es soportado por este recurso. Los dos métodos obligatorios, GET y HEAD, nunca deben ser deshabilitados y no deben retornar este código de error.
- [406](https://developer.mozilla.org/es/docs/Web/HTTP/Status/406) - **Not Acceptable** - Contenido no aceptado de acuerdo a los encabezados _Accept_.
- [407](https://developer.mozilla.org/es/docs/Web/HTTP/Status/407) - **Proxy Authentication Required** - Similar al código `401 Unauthorized`, pero la autenticación debe estar hecha a partir de un proxy.
- [408](https://developer.mozilla.org/es/docs/Web/HTTP/Status/408) - **Request Timeout** - El servidor agotó el tiempo de espera de la solicitud.
- [409](https://developer.mozilla.org/es/docs/Web/HTTP/Status/409) - **Conflict** - Esta respuesta puede ser enviada cuando una petición tiene conflicto con el estado actual del servidor.
- [410](https://developer.mozilla.org/es/docs/Web/HTTP/Status/410) - **Gone** - Esta respuesta se envía cuando el recurso solicitado ha sido borrado del servidor o va a estar disponible más.
- [411](https://developer.mozilla.org/es/docs/Web/HTTP/Status/411) - **Length Required** - Se rechaza la petición porque el campo de encabezado _Content-Length_ no esta definido y el servidor lo requiere.
- [412](https://developer.mozilla.org/es/docs/Web/HTTP/Status/412) - **Precondition Failed** - El cliente ha indicado pre-condiciones en sus encabezados la cual el servidor no cumple.
- [413](https://developer.mozilla.org/es/docs/Web/HTTP/Status/413) - **Request Entity Too Large** - La entidad de petición es más larga que los limites definidos por el servidor.
- [414](https://developer.mozilla.org/es/docs/Web/HTTP/Status/414) - **Request URI Too Large** - La URI solicitada por el cliente es más larga que la soportada por el servidor.
- [415](https://developer.mozilla.org/es/docs/Web/HTTP/Status/415) - **Unsupported Media Type** - Formato multimedia no soportado por el servidor.
- [416](https://developer.mozilla.org/es/docs/Web/HTTP/Status/416) - **Requested Rage Not Satisfiable** - El rango especificado por el campo de encabezado _Range_ en la solicitud no se cumple.
- [417](https://developer.mozilla.org/es/docs/Web/HTTP/Status/417) - **Expectation Failed** - Significa que la expectativa indicada por el campo de encabezado _Expect_ solicitada no puede ser cumplida por el servidor.
- [421](https://tools.ietf.org/html/rfc7540#page-66) - **Misdirected Request** - La petición fue dirigida a un servidor que no es capaz de producir una respuesta.
- [422](https://developer.mozilla.org/es/docs/Web/HTTP/Status/422) - **Unprocessable Entity** - La petición estaba bien formada pero no se pudo seguir debido a errores de semántica.
- [423](http://httpstatus.es/423) - **Locked** - El recurso que está siendo accedido está bloqueado.
- [424](http://httpstatus.es/424) - **Failed Dependency** - La petición falló debido a una falla de una petición previa.
- [426](https://developer.mozilla.org/es/docs/Web/HTTP/Status/426) - **Upgrade Required** - El cliente debe cambiar a un protocolo diferente.
- [428](https://developer.mozilla.org/es/docs/Web/HTTP/Status/428) - **Precondition Required** - El servidor de origen requiere que la solicitud sea condicional.
- [429](https://developer.mozilla.org/es/docs/Web/HTTP/Status/429) - **Too Many Requests** - El usuario ha enviado demasiadas solicitudes en un periodo de tiempo dado.
- [431](https://developer.mozilla.org/es/docs/Web/HTTP/Status/431) - **Request Header Fields Too Large** - El servidor no está dispuesto a procesar la solicitud porque los campos de encabezado son demasiado largos.
- [440](https://en.wikipedia.org/wiki/List_of_HTTP_status_codes#Internet%20Information%20Services) - **Login Timeout** - La sesión del cliente ha caducado y debe loguearse.
- [444](http://httpstatus.es/444) - **No Response** - El servidor no devuelve información al usuario y cierra la conexión. Se suele usar en contra de uno o varios software maliciosos.
- [449](http://httpstatus.es/449) - **Retry With** - Indica que la solicitud debe repetirse después de implementar la acción adecuada.
- [451](https://developer.mozilla.org/es/docs/Web/HTTP/Status/451) - **Wrong Exchange Server** - El usuario solicita un recurso ilegal, como alguna página web censurada por algún gobierno.
- [499](http://httpstatus.es/499) - **Client Closed Request** - La conexión ha sido cerrada por el cliente, mientras el servidor procesaba una petición.

### Errores de servidor 5xx

- [500](https://developer.mozilla.org/es/docs/Web/HTTP/Status/500) - **Internal Error** - El servidor ha encontrado una situación que no sabe como manejarla.
- [501](https://developer.mozilla.org/es/docs/Web/HTTP/Status/501) - **Not Implemented** - El método solicitado no esta soportado por el servidor y la solicitud no puede ser manejada.
- [502](https://developer.mozilla.org/es/docs/Web/HTTP/Status/502) - **Service temporarily overloaded** - Se muestra cuando el servidor, actuando como una puerta de enlace o proxy, recibe del servidor ascendente un mensaje de respuesta no válida.
- [503](https://developer.mozilla.org/es/docs/Web/HTTP/Status/503) - **Gateway timeout** - El servidor no esta listo para manejar la petición. Causas comunes puede ser que el servidor está caido por mantenimiento o está sobrecargado. Similiar al código `500 Internal Error`
- [504](https://developer.mozilla.org/es/docs/Web/HTTP/Status/504) - **Gateway Timeout** - Esta respuesta de error es dada cuando el servidor está actuando como una puerta de enlace y no puede obtener una respuesta a tiempo.
- [505](https://developer.mozilla.org/es/docs/Web/HTTP/Status/505) - **Http Version Not Supported** - Versión HTTP usada en la petición no está soportada por el servidor.
- [506](https://developer.mozilla.org/es/docs/Web/HTTP/Status/506) - **Variant Also Negotiates** - El servidor tiene un error de configuración interna: negociación de contenido para la petición resulta en una referencia circular.
- [507](https://developer.mozilla.org/es/docs/Web/HTTP/Status/507) - **Insufficient Storage** - Ocurre cuando el servidor no puede mandar los datos debido a que no hay suficiente espacio para la solicitud actual.
- [508](https://developer.mozilla.org/es/docs/Web/HTTP/Status/508) - **Loop Detected** - El servidor detectó un ciclo infinito mientras procesaba la solicitud.
- [509](https://sitechecker.pro/es/http-status-codes#509) - **Bandwidth Limit Exceeded** - Indica que el límite de ancho de banda ha sido excedido.
- [510](https://developer.mozilla.org/es/docs/Web/HTTP/Status/510) - **Not Extended** - Indica que no hay una extensión que el cliente quiere utilizar.
- [511](https://developer.mozilla.org/es/docs/Web/HTTP/Status/511) - **Network Authentication Required** - El cliente necesita estar autenticado para tener acceso a la red.

---

## Códigos más usados en una API

| Código | Descripción |
| ------ | ----------- |
| `200` | Ok |
| `201` | Created |
| `204` | No Content |
| `400` | Bad Request |
| `401` | Unauthorized |
| `403` | Forbidden |
| `404` | Not Found |
| `409` | Conflict |
| `422` | Unprocessable Entity |
| `500` | Internal Server Error |
| `503` | Service Unavailable |

### Ejemplos de errores en una API

| Ejemplo | Código |
| ------- | ------ |
| API project configuration not found | `404` |
| Bad request | `400` |
| Batch upload not allowed | `400` |
| Collection not found | `404` |
| Default project not configured properly | `503` |
| Duplicate item | `409` |
| Endpoint not found | `404` |
| Expired reset password token | `401` |
| Expired token | `401` |
| Failed generating SQL query | `500` |
| Failed to connect to the database | `500` |
| Field Invalid | `400` |
| Field not found | `404` |
| Forbidden | `403` |
| Inactive user | `401` |
| Installation invalid database information | `400` |
| Internal error | `500` |
| Invalid configuration path | `422` |
| Invalid credentials | `404` |
| Invalid Filesystem path | `500` |
| Invalid or empty payload | `400` |
| Invalid request, validación | `400` |
| Invalid reset password token | `401` |
| Invalid token | `401` |
| Item not found | `404` |
| Method not allowed | `405` |
| Missing storage configuration | `500` |
| Not allow direct access to system table | `401` |
| Not found | `404` |
| Project name already exists | `409` |
| Reading, creating, updating, deleting denied | `403` |
| Too many requests | `429` |
| Unauthorized | `401` |
| Unauthorized location access | `401` |
| Unknown data type | `400` |
| Unprocessable entity | `422` |
| User not authenticated | `401` |
| User not found | `404` |
| User with provided email not found | `404` |

---

## Referencias

- [Mozilla Developer](https://developer.mozilla.org/es/docs/Web/HTTP/Status)
- [HTTP Status Code](https://httpstatuses.com/)
- [Sitechecker](https://sitechecker.pro/es/http-status-codes/)
- [Wikipedia](https://en.wikipedia.org/wiki/List_of_HTTP_status_codes)