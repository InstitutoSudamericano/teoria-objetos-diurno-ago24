## ¿Qué es una API?

Una **API** (Application Programming Interface) es un conjunto de reglas y definiciones que permiten que diferentes software o sistemas se comuniquen entre sí. Esencialmente, proporciona una forma estructurada y documentada para que los programas interactúen y compartan datos entre sí.

Las API pueden tomar muchas formas, pero en esencia, actúan como intermediarios que permiten que una aplicación acceda a los recursos o funcionalidades de otra aplicación o servicio de una manera controlada y segura. Esto puede incluir la obtención o envío de datos, la ejecución de operaciones específicas o la integración de servicios externos en una aplicación.

## ¿Qué es una API REST?

Una **API REST** (Transferencia de Estado Representacional, por sus siglas en inglés) es un tipo específico de API que sigue un conjunto de principios y convenciones diseñados para crear servicios web escalables, eficientes y fáciles de usar. Estos principios están basados en la arquitectura de la web y se derivan del protocolo HTTP.

Algunas características principales de una API REST incluyen:

- **Protocolo HTTP:** Utiliza los métodos estándar HTTP (GET, POST, PUT, DELETE) para realizar operaciones en los recursos.
  
- **Sin estado (Stateless):** Cada solicitud HTTP contiene toda la información necesaria para ser entendida por el servidor, lo que significa que no mantiene ningún estado de sesión entre solicitudes.

- **Recursos y URIs:** Los datos y funcionalidades se modelan como recursos accesibles a través de URIs (Uniform Resource Identifiers) específicas.

- **Operaciones CRUD:** Las operaciones CRUD (Crear, Leer, Actualizar, Eliminar) se mapean a los métodos HTTP GET, POST, PUT y DELETE respectivamente.

- **Formatos de Datos:** Los datos se transfieren típicamente en formatos estándar como JSON o XML.

## Diferencias entre una API y una API REST

- **Definición y Estándares:** Una API es un término general que abarca cualquier interfaz de programación entre sistemas. Por otro lado, una API REST es un tipo específico de API que sigue principios y convenciones particulares, basadas en la arquitectura web y el protocolo HTTP.

- **Protocolo y Estilo de Arquitectura:** Una API puede utilizar varios protocolos y estilos de arquitectura, como SOAP, RPC, GraphQL, entre otros. En contraste, una API REST sigue el protocolo HTTP y está basada en la arquitectura REST.

- **Operaciones y Recursos:** Las API pueden proporcionar diferentes tipos de operaciones y acceder a una variedad de recursos, mientras que una API REST sigue un conjunto específico de operaciones CRUD y modela los datos como recursos accesibles a través de URIs.

- **Estado:** Las API pueden ser stateful o stateless, mientras que las API REST son stateless, lo que significa que cada solicitud contiene toda la información necesaria para ser procesada por el servidor sin necesidad de mantener un estado de sesión.

- **Formato de Datos:** Las API pueden transferir datos en varios formatos, mientras que las API REST típicamente transfieren datos en formatos estándar como JSON o XML.