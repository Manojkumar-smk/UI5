# SAPUI5 Walkthrough Tutorial – Important Points to Remember (Step by Step)

Official Tutorial Reference:  
https://sapui5.hana.ondemand.com/#/topic/3da5f4be63264db99f2e5b04c5e853db

---

## Step 1: Hello World
- SAPUI5 application starts with a simple control
- `sap.m.Text` is used for displaying text
- UI5 controls are rendered inside a view

---

## Step 2: Bootstrapping SAPUI5
- SAPUI5 is loaded via `index.html`
- UI5 bootstrap defines theme, libraries, and resource root
- Application entry starts after bootstrap completes

---

## Step 3: MVC Concept
- SAPUI5 follows MVC architecture
- View handles UI
- Controller handles logic
- Model handles data

---

## Step 4: XML Views
- XML views are declarative
- Easier to read and maintain
- Preferred over JavaScript views

---

## Step 5: Controllers
- Each view can have a controller
- Controller handles events and logic
- Controller lifecycle starts with `onInit`

---

## Step 6: Models
- Models store application data
- UI5 supports multiple model types
- Data binding connects model and view

---

## Step 7: JSON Model
- JSONModel is client-side
- Default binding mode is TwoWay
- Used mainly for UI state and mock data

---

## Step 8: Resource Model (i18n)
- Texts are externalized into properties files
- Supports multiple languages
- Text binding uses `{i18n>key}`

---

## Step 9: Component Configuration
- `Component.js` is the application entry point
- Models should be initialized in Component
- Component loads `manifest.json`

---

## Step 10: Descriptor for Applications
- Application configuration is in `manifest.json`
- Defines models, rootView, dependencies
- Replaces hardcoded configuration in JS

---

## Step 11: Pages and Panels
- `sap.m.Page` represents a screen
- `sap.m.Panel` groups related content
- Only root view should contain a Page

---

## Step 12: Buttons and Events
- Events are bound declaratively in XML
- Event handler logic is in controller
- Common events: `press`, `change`

---

## Step 13: Margins and Paddings
- Use SAP-provided utility CSS classes
- Avoid custom CSS for spacing
- Margin and padding are handled via classes

---

## Step 14: Custom CSS and Themes
- Custom CSS should be minimal
- CSS is loaded via `manifest.json`
- Theme parameters must be used instead of hardcoded colors

---

## Step 15: Nested Views
- Views can be embedded inside other views
- Used for UI reuse and modular design
- Nested views should not contain Pages

---

## Step 16: Dialogs and Fragments
- Fragments are reusable UI parts
- Fragments do not have controllers
- Dialogs are commonly implemented using fragments

---

## Step 17: Fragment Callbacks
- Fragment events are handled in parent controller
- Event handlers use `.` prefix
- Fragment logic must stay in controller

---

## Step 18: Icons
- UI5 uses icon fonts, not images
- Icons are referenced using `sap-icon://`
- Icons are theme-aware and scalable

---

## Step 19: Aggregation Binding
- Used for lists and tables
- Requires a collection and a template
- UI5 handles iteration automatically

---

## Step 20: Data Types
- Data types handle formatting and parsing
- Locale-aware by default
- Preferred over custom formatters

---

## Step 21: Expression Binding
- Allows simple logic in XML
- Used for conditional UI behavior
- Should remain simple and readable

---

## Step 22: Custom Formatters
- Used for custom display logic
- Formatter functions are reusable
- Formatter logic should be lightweight

---

## Step 23: Filtering
- Filtering is applied on bindings
- Uses `sap.ui.model.Filter`
- Same API works for JSON and OData models

---

## Step 24: Sorting and Grouping
- Sorting uses `sap.ui.model.Sorter`
- Grouping is a special case of sorting
- Group headers are created via grouping function

---

## Step 25: Search
- Search is implemented using filters
- Often combined with liveChange events
- Search updates list automatically

---

## Step 26: OData Model
- ODataModel connects UI5 to backend services
- Supports CRUD operations
- Uses metadata from service

---

## Step 27: Mock Server
- MockServer simulates backend services
- Used for local development
- Avoids dependency on real backend

---

## Step 28: Busy Indicator
- Used to indicate loading state
- Prevents user interaction during processing
- Improves user experience

---

## Step 29: Error Handling
- Errors should be handled centrally
- MessageBox and MessageToast are commonly used
- Avoid silent failures

---

## Step 30: Routing and Navigation
- Routing maps URL to views
- Defined in `manifest.json`
- Enables single-page application behavior

---

## Step 31: Routes with Parameters
- Route parameters are dynamic URL parts
- Used to pass context between views
- Enables deep linking

---

## Step 32: Routing Back and History
- Browser history must be handled carefully
- Back navigation should work for deep links
- History fallback is required

---

## Step 33: Custom Controls
- Custom controls extend `sap.ui.core.Control`
- Used for reusable and complex UI
- Include metadata and renderer

---

## Step 34: Responsiveness
- SAPUI5 is mobile-first
- `sap.m` library is fully responsive
- Fixed layouts should be avoided

---

## End of Walkthrough Notes
- Follow MVC strictly
- Prefer configuration over code
- Keep UI responsive and reusable
- Use standard UI5 patterns consistently

---
