## Creación de @Input y @Output (Ejercicio de la compañía Apple)

Dentro de la compañia Apple existen dos actores, el Jefe y el Empleado. En esta aplicación, tenemos dos componentes principales: `FatherComponent`(Jefe) y `ChildComponent`(Empleado).

### @Input()

El `FatherComponent` representa al jefe de Apple, y necesita comunicar instrucciones a sus empleados (representados por el `ChildComponent`). Para ello, utilizamos el decorador `@Input()`.

```typescript
// father.component.ts
@Component({
  // ...
})
export class FatherComponent {
  parentMessageInput = 'Quiero que estén listos los iphone 13 para el lanzamiento de la nueva versión de la app de mensajería instantánea';
}
```

```html
<!-- father.component.html -->
<app-child [parentMessageInput]="parentMessageInput">
  <!-- Contenido proyectado -->
</app-child>
```

En este ejemplo, el `FatherComponent` tiene una variable `parentMessageInput` que contiene las instrucciones para el empleado. Utilizando el decorador `@Input()` en el `ChildComponent`, podemos pasar esta variable como una propiedad de entrada.

### @Output()

Por otro lado, el `ChildComponent` (el empleado) necesita informar al `FatherComponent` (el jefe) cuando haya completado una tarea. Para ello, utilizamos el decorador `@Output()`.

```typescript
// child.component.ts
@Component({
  // ...
})
export class ChildComponent {
  @Output() childMessageEventOutput = new EventEmitter<string>();

  sendMessage() {
    this.childMessageEventOutput.emit('Jefe, los iphone 13 están listos');
  }
}
```

```html
<!-- father.component.html -->
<app-child (childMessageEventOutput)="receiveMessage($event)">
  <!-- Contenido proyectado -->
</app-child>
```

En este ejemplo, el `ChildComponent` tiene un evento `childMessageEventOutput` que se emite cuando el empleado hace clic en un botón. En el `FatherComponent`, nos suscribimos a este evento utilizando el decorador `@Output()`, y podemos recibir el mensaje enviado por el empleado.

De esta manera, podemos simular la comunicación entre el jefe y los empleados de Apple utilizando los decoradores `@Input()` y `@Output()` en Angular.