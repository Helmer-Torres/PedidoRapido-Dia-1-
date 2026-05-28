# Sistema de Gestión de Pedidos

> Proyecto desarrollado bajo metodología Scrum · Sprint 1 en curso

---

## Equipo

| Nombre | Rol | Correo |
|--------|-----|--------|
| Helmer José Torres Correa | Product Owner / Scrum Master / Developer | helmer.torres@unisimon.edu.co |

---

## Backlog del Producto

| ID | Tipo | Historia de Usuario | Sprint | Puntos | Prioridad |
|----|------|---------------------|--------|--------|-----------|
| US-01 | Registro de pedido | Como encargado, quiero registrar un pedido con nombre del cliente, productos, cantidades y total. | Sprint 1 | 5 | Alta |
| US-02 | Lista de pedidos activos | Como encargado, quiero ver todos los pedidos del día en una lista con su estado. | Sprint 1 | 3 | Alta |
| US-03 | Cambio de estado | Como encargado, quiero cambiar el estado de un pedido entre Pendiente, En proceso y Entregado. | Sprint 1 | 3 | Alta |
| US-04 | Historial de cliente | Como encargado, quiero buscar un cliente y ver sus pedidos anteriores. | Sprint 2 | 5 | Media |
| US-05 | Resumen del día | Como encargado, quiero ver un resumen diario con pedidos atendidos y total cobrado. | Sprint 2 | 3 | Media |
| US-06 | Eliminar pedido | Como encargado, quiero eliminar un pedido registrado por error. | Sprint 2 | 2 | Baja |
| US-07 | Exportar pedidos | Como encargado, quiero exportar los pedidos del día como archivo CSV. | Sprint 2 | 3 | Baja |

Los criterios de aceptación fueron sugeridos con ayuda de **ChatGPT**. El resumen del sprint fue generado con **Claude**.

---

## Estructura del Proyecto

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

Estructura propuesta inicialmente por **V0**, luego refinada para mayor claridad y organización.

---

## Diseño de UI (Wireframe)

El wireframe fue creado con **Google Stitch**. Incluye las siguientes secciones principales:

- **Pedidos:** lista de pedidos del día, entregas realizadas y estados.
- **Clientes:** información relevante para identificar a cada cliente.

> Se identificaron inconsistencias visuales generadas por la IA (ej. botones con estilos distintos entre pantallas). Estos se corregirán en iteraciones futuras.

---

## Desarrollo Sprint 1

El código del Sprint 1 fue desarrollado con apoyo de **V0** y **OpenCode**, obteniendo versiones similares con pequeñas diferencias.

### Funcionalidades implementadas

**Nuevo pedido**
- Selección de cliente registrado en el sistema.
- Campo de notas del pedido.
- Selección de productos disponibles con precio unitario.
- IVA fijo del 16%.
- Soporte para múltiples productos con control de cantidad.
- Cálculo automático de subtotal e IVA.
- Botones para guardar o cancelar.

**Lista de pedidos**
- Visualización de pedidos con los 3 estados: Pendiente, En proceso, Entregado.
- Historial de cambios por pedido.
- Filtros por estado.
- Barra de búsqueda para localizar pedidos rápidamente.

---

## Herramientas y tecnologías utilizadas

| Herramienta | Uso |
|-------------|-----|
| V0 | Generación de estructura de carpetas y código inicial |
| OpenCode | Apoyo en desarrollo del Sprint 1 |
| Google Stitch | Diseño del wireframe |
| ChatGPT | Criterios de aceptación del backlog |
| Claude | Resumen del sprint |
| TypeScript | Tipado del proyecto |

---

## Estado del proyecto

- [x] Kickoff y Sprint Planning 1
- [x] Conformación del equipo y asignación de roles
- [x] Revisión y definición del backlog
- [x] Diseño de wireframe (UI)
- [x] Definición de estructura de carpetas
- [x] Desarrollo Sprint 1 (US-01, US-02, US-03)
- [ ] Sprint 2 (US-04 a US-07)
