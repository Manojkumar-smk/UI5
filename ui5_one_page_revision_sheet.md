# SAPUI5 One-Page Revision Sheet

Official SDK: https://sapui5.hana.ondemand.com

---

## 1. Architecture & Entry Points
- SAPUI5 follows **MVC**
- **index.html** → bootstraps UI5
- **Component.js** → application entry point
- **manifest.json** → central configuration (descriptor)

---

## 2. Views & Controllers
- Preferred view type: **XML View**
- Views are declarative, controllers contain logic
- Controller lifecycle (important):
  - `onInit`
  - `onBeforeRendering`
  - `onAfterRendering`
  - `onExit`

---

## 3. Models (Core Concept)
- **JSONModel** → client-side, UI state, TwoWay by default
- **ODataModel** → server-side, business data
- **ResourceModel** → i18n texts
- Models should be set in **Component.js**

---

## 4. Data Binding
### Binding Types
- Property binding → single value
- Aggregation binding → collections (lists/tables)
- Element binding → bind a control to an object

### Binding Paths
- Absolute → `{ /path }`
- Relative → `{ property }`

---

## 5. Aggregation Binding
- Used for `List`, `Table`, `Select`
- Requires:
  - Collection path
  - Template
- No loops in UI5 — framework handles iteration

---

## 6. Formatting & Validation
### Data Types (Preferred)
- `Date`, `DateTime`
- `Integer`, `Float`
- `Currency`, `Percent`
- Locale-aware
- Handle parsing + formatting

### Formatters
- Custom display logic only
- No parsing or validation
- Keep lightweight and synchronous

---

## 7. Expression Binding
- Inline logic in XML
- Syntax: `{= condition ? value1 : value2 }`
- Use only for simple conditions

---

## 8. i18n
- Texts stored in `.properties` files
- Binding syntax: `{i18n>key}`
- Defined in `manifest.json`
- No hardcoded texts

---

## 9. Fragments & Dialogs
- Fragments are UI-only (no controller)
- Share parent controller
- Always call `addDependent()`
- Use `.` prefix for event handlers

---

## 10. Routing & Navigation
- Routing defined in `manifest.json`
- Route → URL pattern
- Target → View
- `router.initialize()` is mandatory
- Navigation via `navTo()`

---

## 11. Routes with Parameters
- Defined using `{param}` in route pattern
- Passed via `navTo(route, params)`
- Read using `attachPatternMatched`
- Enables deep linking

---

## 12. Back Navigation & History
- Use `sap.ui.core.routing.History`
- If history exists → browser back
- Else → fallback route using `navTo(..., {}, true)`

---

## 13. Filtering & Sorting
### Filtering
- Uses `sap.ui.model.Filter`
- Applied on aggregation binding

### Sorting & Grouping
- Uses `sap.ui.model.Sorter`
- Grouping = sorting + group headers

---

## 14. Icons
- Use SAP icon pool
- Syntax: `sap-icon://icon-name`
- Icon fonts (not images)
- Always provide tooltip for icon-only buttons

---

## 15. Custom Controls
- Extend `sap.ui.core.Control`
- Use metadata (properties, events)
- Renderer generates HTML
- Use only when standard controls are insufficient

---

## 16. Responsiveness
- Mobile-first design
- Use **sap.m** library
- Responsive layouts:
  - `SimpleForm (ResponsiveGridLayout)`
  - `FlexBox`
- Avoid fixed widths

---

## 17. CSS & Theming
- Load CSS via `manifest.json`
- Use SAP utility classes for spacing
- Use theme parameters (no hardcoded colors)
- Avoid inline styles and media queries

---

## Key Rules to Remember
- Configuration > Code
- Data binding > Manual updates
- Data types > Formatters
- Fragments > Custom controls (when possible)
- `sap.m` > `sap.ui.table` for Fiori apps

---
