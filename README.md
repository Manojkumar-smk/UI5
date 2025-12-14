# SAP UI5 Walkthrough

This repository contains the result of the [SAP UI5 Walkthrough Tutorial](https://sapui5.hana.ondemand.com/#/topic/3da5f4be63264db99f2e5b04c5e853db). It demonstrates the core concepts of SAPUI5 development, including MVC, Models, Routing, OData, and Mock Servers.

## 🚀 Getting Started

### Prerequisites
- [Node.js](https://nodejs.org/) (installed)

### Installation
1.  Clone the repository:
    ```bash
    git clone https://github.com/Manojkumar-smk/UI5.git
    cd UI5
    ```
2.  Install dependencies:
    ```bash
    npm install
    ```

## 🏃‍♂️ Running the Application

You can run the application in two modes:

### 1. Mock Data (Development Mode)
Uses a local Mock Server to simulate the Northwind OData service. Useful for offline development and testing.

- **Command**:
  ```bash
  npm start
  ```
- **URL**: [http://localhost:8080/test/mockServer.html](http://localhost:8080/test/mockServer.html)
- **Data**: You will see mocked data (e.g., "Pineapple", "Milk").

### 2. Real OData (Production Mode)
Connects to the public Northwind OData V2 service via a local proxy.

- **Command**:
  ```bash
  ui5 serve -o index.html
  ```
- **URL**: [http://localhost:8080/index.html](http://localhost:8080/index.html)
- **Data**: You will see real data (e.g., "Raclette Courdavault").

---

## 📚 Walkthrough Steps Implemented

This project follows the official tutorial steps:

### Phase 1: Setup & Basics
- **Hello World**: Bootstrapping SAPUI5 from CDN.
- **MVC Architecture**: Creating Views (XML) and Controllers (JS).
- **Modules**: Using `sap.ui.define` and `sap.ui.require` for dependency management.

### Phase 2: Data Binding & Models
- **JSON Model**: Binding local data (e.g., recipient name).
- **i18n**: implementing localization with resource bundles (`i18n.properties`).
- **Formatting**: Using custom formatter functions for status text.

### Phase 3: UI Controls & Dialogs
- **Fragments**: Reusing UI parts like the "Hello" Dialog.
- **Panels & Shell**: distinct layout structure.
- **Custom CSS**: Adding custom styles for specific controls.

### Phase 4: OData & Remote Data
- **Manifest**: Configuring `sap.app` and `dataSources`.
- **OData V2 Model**: connecting to the Northwind service.
- **Mock Server**: intercepting requests to simulation backend logic.

### Phase 5: Routing & Navigation
- **Routing Config**: Defining routes in `manifest.json`.
- **Navigation**: Passing parameters (e.g., Invoice Path) between views.
- **History**: Implementing "Back" navigation logic.

### Phase 6: Extension & Device Adaptation
- **Content Density**: Switching between Compact (Desktop) and Cozy (Touch) modes.
- **Custom Controls**: Implementing the `ProductRating` control with interactive stars.
