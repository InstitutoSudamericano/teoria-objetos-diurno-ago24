# Nathaly Caballero

---
**Pregunta 1:** ¿Cuál es el paso inicial para configurar Railway con tu repositorio de NestJS?

- [ ] Conectar tu repositorio de NestJS con LinkedIn
- [ ] Tener tu repositorio listo y conectarlo con Railway
- [ ] Instalar una extensión en tu navegador

**Respuesta correcta:** - [ ] b) Porque una vez que el repositorio está conectado, podremos realizar otras configuraciones, como establecer variables de entorno, configurar despliegues automáticos, etc. Pero el paso crucial y inicial es tener el repositorio preparado y conectado correctamente con Railway.

**Pregunta 2:** ¿Dónde debes dirigirte en Railway para agregar las variables de entorno?

- [ ] Pestaña "Configuración"
- [ ] Pestaña "Variables"
- [ ] Pestaña "Documentos"

**Respuesta correcta:** - [ ] b) Porque es el lugar adecuado en Railway para agregar y administrar las variables de entorno de tu proyecto de NestJS, proporcionando un acceso directo y simplificado a estas configuraciones críticas.

**Pregunta 3:** ¿Cómo puede Railway detectar automáticamente la configuración del archivo .env?

- [ ] A través de la lectura de comentarios en el código
- [ ] Si el archivo .env está en la raíz del proyecto
- [ ] Si el archivo .env está en la misma ubicación que la base de datos

**Respuesta correcta:** - [ ] b) Porque puede detectar automáticamente la configuración del archivo .env si está ubicado en la raíz del proyecto porque esta es una ubicación estándar y conveniente para almacenar variables de entorno en aplicaciones Node.js, lo que facilita la carga y utilización de estas configuraciones por parte de Railway durante el despliegue y la ejecución de la aplicación.

# David Correa

---
**Pregunta 4:** Después de modificar el archivo main.ts para usar await app.listen(process.env.PORT || 3000);, ¿qué efecto tiene esta línea de código?

- [ ] Establece el puerto de escucha en 3000 si la variable de entorno PORT no está definida.
- [ ] Establece el puerto de escucha en 3000 independientemente del valor de la variable de entorno PORT.
- [ ] Ignora la configuración del puerto y siempre utiliza el valor 3000.

**Respuesta correcta:** - [ ] a) Porque garantiza que la aplicación NestJS escuche en el puerto definido por la variable de entorno PORT si está disponible, de lo contrario, utilizará el puerto 3000 como valor predeterminado si la variable de entorno PORT no está definida o tiene un valor no válido. Esto proporciona flexibilidad en la configuración del puerto de escucha de la aplicación dependiendo del entorno de ejecución.

**Pregunta 5:** ¿Qué hace el script "postinstall": "npx prisma generate && yarn build" en el archivo package.json durante el despliegue?

- [ ] Genera los archivos necesarios utilizando Prisma y luego compila el proyecto NestJS.
- [ ] Instala las dependencias del proyecto y luego ejecuta el comando de compilación.
- [ ] Ejecuta Prisma, genera el código y posteriormente genera la compilación del proyecto.

**Respuesta correcta:** - [ ] a) Porque en el archivo package.json realiza las tareas necesarias de generación de archivos utilizando Prisma y compilación del proyecto NestJS como parte del proceso de despliegue, asegurando que la aplicación esté lista para ser ejecutada en el entorno de producción.

**Pregunta 6:** Después de modificar "start:prod": "node dist/src/main" en el archivo package.json, ¿qué comando se ejecutará al iniciar la aplicación en producción?

- [ ] node dist/src/main
- [ ] npm run start
- [ ] yarn start:prod

**Respuesta correcta:** - [ ] a) Porque al modificar "start:prod": "node dist/src/main" en el archivo package.json, el comando que se ejecutará al iniciar la aplicación en producción será node dist/src/main, lo que asegura que la aplicación NestJS compilada se inicie correctamente utilizando Node.js en un entorno de producción.