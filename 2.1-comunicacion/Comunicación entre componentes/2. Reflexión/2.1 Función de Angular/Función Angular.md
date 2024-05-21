## Función de Angular

Angular facilita la creación de aplicaciones web escalables, de alto rendimiento y fáciles de mantener. Su principal función es proporcionar una estructura y un conjunto de herramientas para el desarrollo de aplicaciones de una sola página (SPA) y aplicaciones web modernas.

Claro, aquí tienes la información sobre los comandos para crear una aplicación en Angular y cómo levantarla, agregada al archivo Reflexión.md:

### Crear una nueva aplicación Angular

Para crear una nueva aplicación Angular, puedes utilizar la interfaz de línea de comandos (CLI) de Angular. Primero, asegúrate de tener instalado Node.js y npm (el administrador de paquetes de Node.js). Luego, ejecuta el siguiente comando para instalar la CLI de Angular de manera global:

```
npm install -g @angular/cli
```

Una vez instalada la CLI de Angular, puedes crear una nueva aplicación con el siguiente comando:

```
ng new nombre-de-tu-aplicacion
```

Este comando creará una nueva carpeta con la estructura de archivos y dependencias necesarias para tu aplicación Angular.

### Levantar la aplicación Angular

Para levantar la aplicación Angular y verla en tu navegador, primero debes navegar a la carpeta de tu aplicación:

```
cd nombre-de-tu-aplicacion
```

Luego, puedes ejecutar el siguiente comando para iniciar el servidor de desarrollo de Angular:

``` bash
ng serve
```

o
```bash
ng serve -o
```

Estos comandos compilarán tu aplicación y la servirá en `http://localhost:4200`. Abre esta URL en tu navegador para ver tu aplicación Angular en ejecución.

**-o:** Sirve para abrir tu aplicación de forma automática.

Angular CLI también proporciona otros comandos útiles, como `ng build` para compilar tu aplicación para producción, `ng test` para ejecutar pruebas unitarias y `ng generate` para generar componentes, servicios y otros artefactos de Angular.
