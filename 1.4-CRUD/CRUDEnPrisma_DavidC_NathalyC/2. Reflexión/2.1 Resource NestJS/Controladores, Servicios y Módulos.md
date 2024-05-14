## Resource de Nestjs

Los desarroladores y programadores necesitan de controladores, servicios, módulos, dto y entities para realizar diferentes tipos de recursos. En este caso una API REST.
Pero crear los módulos, servicios y los demás recursos uno por uno es muy agobiante. Por lo que NestJS cuenta con un comando que realiza todo eso por nosotros los programadores. El comando es:

```bash
npx nest generate resource
```

Este comando generará automáticamente todos los recursos que necesitamos para una API REST, los cuales son:

1. **Controladores:**
   Los controladores son funciones o clases que manejan las solicitudes HTTP entrantes en una aplicación web. En una aplicación construida con Prisma, los controladores podrían utilizar el cliente Prisma para interactuar con la base de datos y realizar operaciones CRUD en los modelos de datos.

2. **Servicios:**
   Los servicios son capas intermedias entre los controladores y la capa de acceso a datos. Contienen la lógica empresarial de la aplicación y son responsables de coordinar las operaciones relacionadas con los datos. En una aplicación con Prisma, los servicios podrían contener funciones que encapsulan la lógica para realizar operaciones CRUD en los modelos de datos utilizando el cliente Prisma.

3. **Módulos:**
   Los módulos son componentes de código independientes que encapsulan funcionalidades relacionadas en una unidad coherente. En TypeScript, los módulos pueden ser archivos separados que exportan funciones, clases u otros elementos que pueden ser importados y utilizados en otros lugares de la aplicación.
   
4. **DTO (Data Transfer Objects):** Los DTOs son objetos utilizados para transferir datos entre diferentes capas de la aplicación, como entre los controladores y los servicios. Proporcionan una forma de estructurar y validar los datos que se reciben y envían a través de la API.

5. **Entities (Entidades):**
   Las entidades en Prisma representan los modelos de datos en tu base de datos. Por ejemplo, puedes tener una entidad llamada `User` que representa a los usuarios en tu aplicación. Esta entidad define la estructura y las relaciones de los datos.

#### También lo puedes hacer uno por uno, de la siguiente manera:

1. Para generar un módulo:

   ```bash
   npx nest generate module module-name
   ```

2. Para generar un controlador:

   ```bash
   npx nest generate controller controller-name
   ```

3. Para generar un servicio:

   ```bash
   npx nest generate service service-name
   ```

4. Para generar un DTO:

   ```bash
   npx nest generate dto dto-name
   ```