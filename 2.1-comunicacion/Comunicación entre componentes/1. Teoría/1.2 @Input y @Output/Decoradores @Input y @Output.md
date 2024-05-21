## @Input() y @Output()

En Angular, `@Input()` y `@Output()` son decoradores utilizados para facilitar la comunicación entre componentes padres e hijos.

### @Input()

El decorador `@Input()` se utiliza para pasar datos del componente padre al componente hijo. El componente hijo declara una propiedad decorada con `@Input()`, y el componente padre vincula un valor a esa propiedad.

Ejemplo:

```typescript
// component-hijo.component.ts
import { Component, Input } from '@angular/core';

@Component({
  // ...
})
export class ComponenteHijoComponent {
  @Input() datos: string;
}
```

```html
<!-- component-padre.component.html -->
<app-component-hijo [datos]="mensaje"></app-component-hijo>
```

### @Output()

El decorador `@Output()` se utiliza para enviar datos del componente hijo al componente padre. El componente hijo emite un evento con los datos deseados, y el componente padre se suscribe a ese evento.

Ejemplo:

```typescript
// component-hijo.component.ts
import { Component, Output, EventEmitter } from '@angular/core';

@Component({
  // ...
})
export class ComponenteHijoComponent {
  @Output() datosEnviados = new EventEmitter<string>();

  enviarDatos() {
    this.datosEnviados.emit('Datos desde el componente hijo');
  }
}
```

```html
<!-- component-padre.component.html -->
<app-component-hijo (datosEnviados)="recibirDatos($event)"></app-component-hijo>
```
