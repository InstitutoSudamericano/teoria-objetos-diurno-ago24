## Configuración de la Aplicación NestJS

### main.ts

1. Modificar la línea del archivo `main.ts` por lo siguiente:

```typescript
await app.listen(process.env.PORT || 3000);
```

### Package.json

1. Añadir dentro del archivo `package.json`, en el apartado de scripts, la siguiente línea: `"postinstall": "npx prisma generate && npm run build"`

```json
"scripts": {
    "postinstall": "npx prisma generate && npm run build"
  },
```

2. Y modificar la línea de `start:prod` con lo siguiente:

```json
"start:prod": "node dist/src/main",
```

Luego de realizar los cambios, subir el proyecto a su repositorio en GitHub.

## Creación de Instancia en Railway

### Si tienes Base de Datos

Es recomendable crear el proyecto de NestJS en el mismo lugar donde se encuentra la base de datos para que las variables de la base de datos se llenen automáticamente. Se da un clic en donde está el botón "+New".

Permitir la instalación de Railway si es que lo solicita. Seleccionar nuestro proyecto de NestJS de la lista de repositorios de nuestro GitHub.

### Si no tienes Base de Datos

Crear una cuenta en Railway con la cuenta de GitHub donde yace el proyecto de NestJS y luego seleccionar "Deploy from Github repo".

Luego, permitir instalar Railway en su repositorio. Seleccionar el repositorio donde está nuestro proyecto de NestJS.

## Configuración de Railway

### Variables

En la pestaña "Variables", agregar la configuración del archivo `.env` de su proyecto. En el caso de que se encuentre en el mismo lugar que su base de datos, esto llenará automáticamente la configuración.

### Settings

En la pestaña "Settings", realizar los siguientes cambios:

#### Build Command
```
npm run postinstall
```

#### Watch Paths
```
/src/**/*.ts
```

#### Start Command
```
npm run start:prod
```

### Crear un dominio

Dar clic en "Generate Domain".

## Paso Final

1. Dar clic en el link del dominio generado y esperar que se hagan los cambios correspondientes.

2. Si no se inicia automáticamente, proceder a realizar un "Deployment" manualmente.

3. Verificar que el proyecto esté sin errores por medio de los logs.

4. Probar con Postman (Todo el CRUD correspondiente).

¡Listo! Has completado el deployment de tu aplicación NestJS en Railway.