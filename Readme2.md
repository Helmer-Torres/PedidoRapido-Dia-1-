# Dia 2

Proyecto desarrollado bajo metodología **Scrum** para el control y seguimiento de pedidos de un negocio. Permite registrar, consultar, cambiar el estado y exportar pedidos del día, además de mantener un historial por cliente.

---

## 👤 Equipo

| Nombre | Rol | Correo |
|---|---|---|
| Helmer Jose Torres Correa | Product Owner / Scrum Master / Development | helmer.torres@unisimon.edu.co |

---

## 🗂️ Historias de Usuario

| ID | Tipo | Descripción | Sprint | Prioridad |
|---|---|---|---|---|
| US-01 | Registro de pedido | Registrar pedido con cliente, productos, cantidades y total | Sprint 1 | Alta |
| US-02 | Lista de pedidos activos | Ver todos los pedidos del día con su estado | Sprint 1 | Alta |
| US-03 | Cambio de estado | Cambiar estado entre Pendiente, En proceso y Entregado | Sprint 1 | Alta |
| US-04 | Historial de cliente | Buscar cliente y ver pedidos anteriores | Sprint 2 | Media |
| US-05 | Resumen del día | Ver total de pedidos atendidos y monto cobrado | Sprint 2 | Media |
| US-06 | Eliminar pedido | Eliminar pedidos registrados por error | Sprint 2 | Baja |
| US-07 | Exportar pedidos | Exportar pedidos del día como CSV | Sprint 2 | Baja |

---

## 🗃️ Estructura del Proyecto

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

## 🎨 Diseño de UI

El wireframe fue creado con **Google Stitch**. Incluye las secciones principales:

- **Pedidos:** lista de pedidos activos, estado y entregas realizadas.
- **Clientes:** información relevante para identificar y rastrear clientes frecuentes.

> Se identificaron inconsistencias visuales menores en algunos componentes (ej. el botón de búsqueda y el de exportar tienen estilos distintos), las cuales serán corregidas durante la implementación.

---

## 🤖 Herramientas de IA utilizadas

| Herramienta | Uso |
|---|---|
| **ChatGPT** | Sugerencia de criterios de aceptación para las historias de usuario |
| **Claude** | Generación del resumen del sprint a partir del backlog |
| **Google Stitch** | Creación del wireframe de la interfaz |
| **V0** | Propuesta inicial de la estructura de carpetas del proyecto |

---

## 🚀 Estado del Proyecto

- [x] Kickoff y Sprint Planning 1
- [x] Conformación del equipo y asignación de roles
- [x] Revisión del backlog
- [x] Diseño de wireframe (UI)
- [x] Propuesta de estructura de código
- [ ] Implementación Sprint 1
- [ ] Implementación Sprint 2
