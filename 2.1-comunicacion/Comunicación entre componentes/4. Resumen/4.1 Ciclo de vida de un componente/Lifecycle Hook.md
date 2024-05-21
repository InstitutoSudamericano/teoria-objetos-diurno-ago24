## Ciclo de vida de un componente

En Angular, los componentes pasan por diferentes etapas de su ciclo de vida, desde la creación hasta la destrucción. Cada etapa del ciclo de vida tiene un conjunto de hooks (ganchos) que se pueden utilizar para ejecutar lógica específica en ese momento.

## Etapas del ciclo de vida de un componente:

1. **ngOnChanges()**:
   - Definición: Se ejecuta cuando los datos enlazados por `@Input()` han sido inicializados o cuando se produce un cambio en los valores de las propiedades de entrada.
   - Analogía: Cuando Apple lanza un nuevo modelo de iPhone, los empleados de las tiendas deben actualizarse sobre las nuevas características y cambios en los productos.

2. **ngOnInit()**:
   - Definición: Se ejecuta una vez, después de que el componente se haya inicializado por completo.
   - Analogía: Cuando Apple abre una nueva tienda, se realizan tareas de configuración e inicialización antes de que la tienda esté lista para recibir clientes.

3. **ngDoCheck()**:
   - Definición: Se ejecuta durante cada ciclo de detección de cambios, permitiendo realizar acciones personalizadas después de que Angular haya realizado el proceso de detección de cambios.
   - Analogía: Los empleados de Apple realizan verificaciones periódicas para asegurarse de que los productos y servicios se están ofreciendo correctamente.

4. **ngAfterContentInit()**:
   - Definición: Se ejecuta después de que Angular haya proyectado contenido externo en el componente.
   - Analogía: Cuando Apple lanza un nuevo producto, se preparan los materiales de marketing y publicidad para su distribución.

5. **ngAfterContentChecked()**:
   - Definición: Se ejecuta después de que Angular haya comprobado el contenido proyectado y sus hijos.
   - Analogía: Los gerentes de Apple revisan y aprueban los materiales de marketing y publicidad antes de su lanzamiento.

6. **ngAfterViewInit()**:
   - Definición: Se ejecuta después de que Angular haya inicializado completamente los componentes y las vistas secundarias.
   - Analogía: Después de que una nueva tienda de Apple está completamente configurada, se realiza una inspección final antes de abrir al público.

7. **ngAfterViewChecked()**:
   - Definición: Se ejecuta después de que Angular haya comprobado los componentes y las vistas secundarias.
   - Analogía: Los empleados de Apple realizan una última revisión de las tiendas y los productos antes de iniciar las operaciones diarias.

8. **ngOnDestroy()**:
   - Definición: Se ejecuta justo antes de que Angular destruya el componente.
   - Analogía: Cuando Apple cierra una tienda o discontinúa un producto, se realizan tareas de limpieza y desmantelamiento antes de finalizar las operaciones.