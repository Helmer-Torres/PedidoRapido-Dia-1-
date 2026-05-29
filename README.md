# Sistema de Gestión de Pedidos

Proyecto desarrollado bajo metodología **Scrum**, con planificación de sprints, diseño de UI y estructura de código orientada a la gestión de pedidos de un negocio.

---

## Equipo

| Nombre | Rol | Correo |
|--------|-----|--------|
| Helmer José Torres Correa | Product Owner / Scrum Master / Development | helmer.torres@unisimon.edu.co |

---

## Descripción

Aplicación web para que el encargado de un negocio pueda registrar, consultar y gestionar pedidos de clientes. Incluye control de estados, historial de clientes, resumen diario y exportación de datos.

---

## Historias de Usuario

### Sprint 1

| ID | Tipo | Historia | Puntos | Prioridad |
|----|------|----------|--------|-----------|
| US-01 | Registro de pedido | Como encargado, quiero registrar un pedido con nombre del cliente, productos, cantidades y total. | 5 | Alta |
| US-02 | Lista de pedidos activos | Como encargado, quiero ver todos los pedidos del día en una lista con sus estados. | 3 | Alta |
| US-03 | Cambio de estado | Como encargado, quiero cambiar el estado de un pedido entre Pendiente, En proceso y Entregado. | 3 | Alta |

### Sprint 2

| ID | Tipo | Historia | Puntos | Prioridad |
|----|------|----------|--------|-----------|
| US-04 | Historial de cliente | Como encargado, quiero buscar un cliente y ver sus pedidos anteriores. | 5 | Media |
| US-05 | Resumen del día | Como encargado, quiero ver un resumen con el número de pedidos atendidos y el total cobrado. | 3 | Media |
| US-06 | Eliminar pedido | Como encargado, quiero eliminar un pedido registrado por error. | 2 | Baja |
| US-07 | Exportar pedidos | Como encargado, quiero exportar los pedidos del día como archivo CSV. | 3 | Baja |

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

---

## Funcionalidades Implementadas (Sprint 1)

- **Nuevo pedido:** selección de cliente, nota, productos disponibles con precio e IVA (16%), cálculo automático de subtotal y total, opción de guardar o cancelar.
- **Lista de pedidos:** visualización con los 3 estados (Pendiente, En proceso, Entregado), filtros y barra de búsqueda.
- **Cambio de estado:** el encargado puede actualizar el estado directamente desde la lista con un clic.

---

## Herramientas Utilizadas

| Herramienta | Uso |
|-------------|-----|
| **V0** | Generación de estructura de código y componentes de UI |
| **OpenCode** | Apoyo en el desarrollo del Sprint 1 |
| **Google Stitch** | Creación del wireframe de la UI |
| **ChatGPT** | Sugerencia de criterios de aceptación |
| **Claude** | Generación del resumen del sprint |

---

## Notas

- Los criterios de aceptación fueron sugeridos por ChatGPT como punto de partida para cada historia de usuario.
- El resumen del sprint fue generado por Claude en base al backlog definido.
- El wireframe presenta algunas inconsistencias visuales (estilos de botones) comunes al usar IA generativa; se prevén mejoras en iteraciones futuras.
- La estructura de carpetas y los lenguajes definitivos se ajustarán conforme avance la implementación.
