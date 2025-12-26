# Angular — Routing moderno con componentes standalone

> Objetivo: tener rutas limpias y componentes standalone sin NgModules.

## Ideas clave

- `app.routes.ts` centraliza las rutas.
- `<router-outlet>` renderiza la vista activa.
- `RouterLink` y `RouterLinkActive` para navegación.

## Ejemplo mínimo

```ts
import { Routes } from '@angular/router';

export const routes: Routes = [
  { path: '', loadComponent: () => import('./pages/home/home.component').then(m => m.HomeComponent) },
  { path: 'tareas', loadComponent: () => import('./pages/tasks/tasks.component').then(m => m.TasksComponent) },
  { path: '**', redirectTo: '' },
];
```

> Puedes ampliar esto con guards, resolvers y lazy loading por secciones.
