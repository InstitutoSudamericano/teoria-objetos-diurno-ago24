# Nathaly Caballero

---
**Pregunta 1:** ¿En qué URL quedarán documentados todos los endpoints de la aplicación NestJS utilizando Swagger?
- [ ] [http://localhost:3000/docs](http://localhost:3000/docs)
- [ ] [http://localhost:3000/api-docs](http://localhost:3000/api-docs)
- [ ] [http://localhost:3000/api](http://localhost:3000/api)

**Respuesta correcta:** C, Porque en el código de configuración de Swagger para la aplicación NestJS, se ha especificado el prefijo 'api' como el lugar donde se alojará la documentación.

**Pregunta 2:** ¿Dónde se define la configuración de conexión a la base de datos PostgreSQL en el módulo principal de la aplicación NestJS?
- [ ] En el fichero app.module.ts
- [ ] En el fichero creatures.module.ts
- [ ] En el fichero creatures.repository.ts

**Respuesta correcta:**  A, Porque en NestJS, el archivo app.module.ts es el módulo principal de la aplicación donde se centralizan las configuraciones globales, importaciones de módulos y configuraciones de proveedores para toda la aplicación.

**Pregunta 3:** ¿Cuál es el propósito del decorador @ApiProperty() en la clase CreateCreatureDto?
- [ ] Define propiedades privadas
- [ ] Documenta propiedades para generar la documentación de la API
- [ ] Controla el flujo de la aplicación

**Respuesta correcta:** B, Porque el propósito principal del decorador @ApiProperty() en NestJS es facilitar la generación automática de documentación de la API, permitiendo a los desarrolladores especificar cómo deben describirse y documentarse las propiedades de una clase en la especificación OpenAPI.

# David Correa

---
**Pregunta 4:** ¿Cuál es el propósito principal de un DTO en una aplicación NestJS?
- [ ] Representar los controladores de la aplicación
- [ ] Transferir datos entre diferentes capas de la aplicación
- [ ] Definir la estructura de las bases de datos

**Respuesta correcta:** B, Porque los DTOs suelen utilizarse para definir la estructura de los datos que se intercambian entre los controladores y los servicios de la aplicación. Esto promueve una separación clara de las responsabilidades y ayuda a mantener un acoplamiento bajo entre las diferentes partes del sistema.

**Pregunta 5:** ¿Qué indica el modificador required: false en un decorador @ApiProperty() de un DTO?
- [ ] Indica que la propiedad es obligatoria y no puede ser omitida
- [ ] Indica que la propiedad es opcional y puede ser omitida
- [ ] Indica que la propiedad tiene un valor por defecto

**Respuesta correcta:** B, Porque esto proporciona flexibilidad en el intercambio de datos sin comprometer la integridad de la estructura del objeto.

**Pregunta 6:** ¿Qué indica el modificador required: false en un decorador @ApiProperty() de un DTO?
- [ ] Indica que la propiedad es obligatoria y no puede ser omitida
- [ ] Indica que la propiedad es opcional y puede ser omitida
- [ ] Indica que la propiedad tiene un valor por defecto

**Respuesta correcta:** B, Porque esto proporciona flexibilidad en el intercambio de datos sin comprometer la integridad de la estructura del objeto.
