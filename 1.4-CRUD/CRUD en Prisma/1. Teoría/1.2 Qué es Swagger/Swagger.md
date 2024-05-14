## Qué es Swagger?

Cuando hablamos de **Swagger** nos referimos a una serie de reglas, especificaciones y herramientas que nos ayudan a documentar nuestras APIs. De esta manera, podemos realizar documentación que sea realmente útil para las personas que la necesitan. Swagger nos ayuda a crear documentación que todo el mundo entienda.

## Instala Swagger

  
Para instalar Swagger UI Express, que es una herramienta para visualizar la documentación de Swagger en una aplicación Express, necesitarás instalar el paquete `swagger-ui-express`. Puedes hacerlo ejecutando el siguiente comando en tu terminal:

```bash
npm install swagger-ui-express
```

Si tienes un proyecto en Nestjs, entonces ingresa el siguiente comando:

```bash
npm install --save @nestjs/swagger swagger-ui-express
```

Para configurar Swagger, dentro de nuestro archivo `main.ts` debemos poner el siguiente código:

``` typescript
import { NestFactory } from '@nestjs/core';
import AppModule } from './app.module';
import { SwaggerModule, DocumentBuilder } from '@nestjs/swagger';

async function bootstrap() {
    const app = await NestFactory.create(AppModule);

    const config = new DocumentBuilder()
        .setTitle('Median')
        .setDescription ('The Median API description')
        .setVersion ('0.1')
        .build();

    const document = SwaggerModule.createDocument (app, config); SwaggerModule.setup('api', app, document);
    await app.listen(3000);
}
bootstrap();
```

Este código configurará Swagger dentro del proyecto de nestjs, donde los endpoints se quedarán documentados en `localhost:3000/api`