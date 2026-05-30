# 📦 Sistema de Gestión de Pedidos

Aplicación web para el control y seguimiento de pedidos de un negocio, desarrollada con metodología **Scrum** como parte de un proyecto académico en la Universidad Simón Bolívar.

---

## 👥 Equipo

| Nombre | Rol |
|---|---|
| Helmer Jose Torres Correa | Product Owner / Scrum Master / Development |

---

## 🚀 Funcionalidades

### Sprint 1 (Implementadas)

- **Registro de pedidos** — Ingreso de cliente, productos, cantidades y cálculo automático del total. El pedido se guarda con fecha y estado "Pendiente".
- **Lista de pedidos activos** — Vista de todos los pedidos del día con su estado, ordenables por hora o estado.
- **Cambio de estado** — Flujo de estados: `Pendiente → En proceso → Entregado`. No se puede revertir un pedido ya entregado.

### Sprint 2 (Planificadas)

- **Historial de cliente** — Búsqueda por nombre con historial de fechas y montos.
- **Resumen del día** — Dashboard con cantidad de pedidos entregados y total vendido.
- **Eliminar pedido** — Eliminación con confirmación; solo aplica a pedidos pendientes.
- **Exportar a CSV** — Descarga del listado del día con cliente, productos, total y estado.

---

## 🏗️ Estructura del Proyecto

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

## 📋 Product Backlog

| ID | Tipo | Historia de Usuario | Sprint | Puntos | Prioridad |
|---|---|---|---|---|---|
| US-01 | Registro de pedido | Como encargado, quiero registrar un pedido con cliente, productos, cantidades y total. | Sprint 1 | 5 | Alta |
| US-02 | Lista de pedidos activos | Como encargado, quiero visualizar todos los pedidos activos. | Sprint 1 | 3 | Alta |
| US-03 | Cambio de estado | Como encargado, quiero cambiar el estado de un pedido para controlar el flujo de atención. | Sprint 1 | 3 | Alta |
| US-04 | Historial de cliente | Como encargado, quiero consultar el historial de pedidos de un cliente. | Sprint 2 | 5 | Media |
| US-05 | Resumen del día | Como encargado, quiero ver un resumen diario de ventas. | Sprint 2 | 3 | Media |
| US-06 | Eliminar pedido | Como encargado, quiero eliminar pedidos registrados por error. | Sprint 2 | 2 | Baja |
| US-07 | Exportar pedidos | Como encargado, quiero exportar los pedidos del día a CSV. | Sprint 2 | 3 | Baja |

---

## 🛠️ Herramientas utilizadas

| Herramienta | Uso |
|---|---|
| **V0** | Generación de código y estructura de componentes |
| **OpenCode** | Desarrollo asistido de funcionalidades |
| **Google Stitch** | Diseño del wireframe de la UI |
| **ChatGPT** | Sugerencia de criterios de aceptación y refinamiento del backlog |
| **Claude** | Resumen de sprint y generación del acta de reunión |

---

## 📌 Estado del Proyecto

El **Sprint 1** fue completado exitosamente, cumpliendo con las tres historias de usuario planificadas:

- ✅ Registro de pedidos
- ✅ Lista de pedidos activos con filtros y búsqueda
- ✅ Cambio de estado de pedidos

El **Sprint 2** está en planificación, con el objetivo de añadir historial de clientes, reportes diarios, eliminación y exportación de pedidos, además de mejoras visuales e iteraciones sobre las funcionalidades del Sprint 1.
