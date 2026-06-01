# Sistema de Gestión de Pedidos

Aplicación web para el control y seguimiento de pedidos de un negocio, desarrollada con metodología **Scrum** a lo largo de dos sprints.

---

## Equipo

| Nombre | Rol |
|---|---|
| Helmer Jose Torres Correa | Product Owner / Scrum Master / Development |

---

## Descripción

El sistema permite al encargado del negocio registrar pedidos, controlar su estado, consultar el historial de clientes y generar reportes diarios de ventas. La interfaz fue diseñada con wireframes en **Google Stitch** y el código desarrollado con apoyo de herramientas de IA como **V0**, **OpenCode** y **GitHub Copilot**.

---

## Funcionalidades

### Sprint 1
- **Registro de pedido** – Ingreso de cliente, productos, cantidades y total. El pedido se guarda con fecha y estado "Pendiente".
- **Lista de pedidos activos** – Visualización de pedidos del día con estado, ordenables por hora o estado.
- **Cambio de estado** – Flujo de estados: `Pendiente → En proceso → Entregado` (no reversible desde Entregado).

### Sprint 2
- **Historial de cliente** – Búsqueda por nombre con pedidos anteriores, fechas y montos.
- **Resumen del día** – Total de pedidos entregados y monto vendido, actualizado automáticamente.
- **Eliminar pedido** – Eliminación de pedidos pendientes con confirmación (no aplica a entregados).
- **Exportar pedidos** – Generación de archivo CSV con cliente, productos, total y estado del día seleccionado.
- **Perfil de cliente** – Tier/rango (Regular, VIP, Premium) y detalle de productos comprados con frecuencia.

---

## Estructura del proyecto

```
/lib
  ├── types.ts          → Tipos TypeScript (Order, Client, Product, etc.)
  ├── mock-data.ts      → Datos de ejemplo con clientes y pedidos
  └── export-csv.ts     → Utilidad de exportación CSV

/components
  ├── layout/           → app-sidebar, header, breadcrumbs
  ├── dashboard/        → stats-card, stats-grid
  ├── pedidos/          → orders-table, order-filters, order-status-badge
  └── shared/           → export-csv-button, search-input

/app/(dashboard)
  ├── layout.tsx        → Layout con sidebar compartido
  ├── page.tsx          → Dashboard principal
  ├── pedidos/          → Lista, nuevo y detalle de pedido
  ├── clientes/         → Lista y detalle de cliente
  ├── reportes/         → Placeholder de reportes
  └── ajustes/          → Configuración básica
```

---

## Tecnologías utilizadas

- **TypeScript** – Tipado estático del proyecto
- **Next.js** (App Router) – Framework principal
- **Tailwind CSS** – Estilos
- **V0 / OpenCode / GitHub Copilot** – Asistencia en generación de código
- **Google Stitch** – Diseño de wireframes

---

## Herramientas de IA utilizadas en el proceso

| Herramienta | Uso |
|---|---|
| ChatGPT | Criterios de aceptación de historias de usuario y refinación del backlog |
| Claude | Resumen del sprint y acta de reunión |
| V0 | Estructura de carpetas, UI de pedidos y cambio de estado |
| OpenCode | Código base del sprint 2 |
| GitHub Copilot | Mejora y refactorización del código en VS Code |
| Google Stitch | Wireframe de la interfaz |

---

## Backlog de historias de usuario

| ID | Historia | Sprint | Puntos | Prioridad |
|---|---|---|---|---|
| US-01 | Registro de pedido | Sprint 1 | 5 | Alta |
| US-02 | Lista de pedidos activos | Sprint 1 | 3 | Alta |
| US-03 | Cambio de estado | Sprint 1 | 3 | Alta |
| US-04 | Historial de cliente | Sprint 2 | 5 | Media |
| US-05 | Resumen del día | Sprint 2 | 3 | Media |
| US-06 | Eliminar pedido | Sprint 2 | 2 | Baja |
| US-07 | Exportar pedidos a CSV | Sprint 2 | 3 | Baja |

---

## Estado del proyecto

Sprint 1 completado exitosamente con las funcionalidades de registro, listado y cambio de estado de pedidos. Sprint 2 en curso con mejoras progresivas hasta alcanzar una versión completa.
