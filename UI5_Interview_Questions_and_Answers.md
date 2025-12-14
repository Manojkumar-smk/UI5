# SAP UI5 Interview Questions and Answers

This document contains commonly asked SAP UI5 interview questions with clear and concise answers.
It covers fundamentals, core concepts, and advanced topics.

---

## 1. SAP UI5 Basics

### Q1. What is SAP UI5?
SAP UI5 is a JavaScript-based UI framework from SAP used to build responsive, enterprise-grade web applications based on Fiori design principles.

---

### Q2. What is the difference between SAP UI5 and OpenUI5?
- SAP UI5 is SAP-supported and includes additional enterprise controls.
- OpenUI5 is open-source and contains core UI5 functionality.

---

### Q3. Which architecture does SAP UI5 follow?
SAP UI5 follows the MVC (Model–View–Controller) architecture.

---

## 2. Views and Controllers

### Q4. What are the types of views in SAP UI5?
- XML View
- JavaScript View
- JSON View
- HTML View (deprecated)

---

### Q5. Why are XML views preferred?
XML views are declarative, easy to read, maintainable, and provide better performance.

---

### Q6. What are the controller lifecycle methods?
- onInit
- onBeforeRendering
- onAfterRendering
- onExit

---

## 3. Models

### Q7. What are the different models in SAP UI5?
- JSONModel
- ODataModel (V2 / V4)
- ResourceModel
- XMLModel

---

### Q8. What is JSONModel used for?
JSONModel is client-side and used for UI state, mock data, and temporary data.

---

### Q9. What is the default binding mode of JSONModel?
TwoWay binding.

---

### Q10. Where should models be initialized?
Models should be initialized in Component.js.

---

## 4. Data Binding

### Q11. What are the types of data binding?
- Property Binding
- Aggregation Binding
- Element Binding

---

### Q12. What is aggregation binding?
Aggregation binding binds a collection of data to controls like List or Table using a template.

---

### Q13. Difference between absolute and relative binding?
- Absolute binding starts with `/` and refers to the model root.
- Relative binding depends on the current binding context.

---

### Q14. What is element binding?
Element binding binds a control to a specific object, reducing path repetition.

---

## 5. Formatting and Validation

### Q15. What are data types in SAP UI5?
Data types handle formatting, parsing, and validation between model data and UI controls.

---

### Q16. Difference between formatter and data type?
- Data type handles parsing and formatting and is locale-aware.
- Formatter handles custom display logic only.

---

### Q17. When should formatters be used?
Formatters should be used only when standard UI5 data types are insufficient.

---

## 6. Expression Binding

### Q18. What is expression binding?
Expression binding allows simple conditional logic directly in XML views.

Example:
```xml
visible="{= ${/amount} > 100 }"
```

---

## 7. Internationalization (i18n)

### Q19. What is i18n?
i18n is used to support multiple languages by externalizing texts.

---

### Q20. Which model is used for i18n?
ResourceModel.

---

## 8. Fragments and Dialogs

### Q21. What is a fragment?
A fragment is a reusable UI part without its own controller.

---

### Q22. Why are fragments used for dialogs?
Fragments are lightweight, reusable, and share the parent controller.

---

### Q23. Why is addDependent() important?
It ensures proper lifecycle handling and model inheritance.

---

## 9. Routing and Navigation

### Q24. What is routing in SAP UI5?
Routing maps URL hashes to views and enables single-page application navigation.

---

### Q25. Where is routing configured?
Routing is configured in manifest.json.

---

### Q26. Difference between route and target?
- Route defines the URL pattern.
- Target defines the view to be displayed.

---

### Q27. What is deep linking?
Deep linking allows direct access to a specific app state via URL.

---

## 10. Back Navigation and History

### Q28. How is back navigation handled?
Using sap.ui.core.routing.History and browser history.

---

### Q29. Why should navTo() not always be used for back navigation?
It creates duplicate history entries and breaks browser back behavior.

---

## 11. Filtering and Sorting

### Q30. Which class is used for filtering?
sap.ui.model.Filter.

---

### Q31. Which class is used for sorting?
sap.ui.model.Sorter.

---

### Q32. What is grouping?
Grouping is a special case of sorting that creates group headers.

---

## 12. Icons and UI Controls

### Q33. How are icons used in SAP UI5?
Using SAP icon font with sap-icon://icon-name.

---

### Q34. Why use icon fonts instead of images?
They are scalable, theme-aware, and performant.

---

## 13. Custom Controls

### Q35. What is a custom control?
A custom control is created by extending sap.ui.core.Control.

---

### Q36. When should custom controls be created?
Only when standard UI5 controls cannot meet a reusable or complex requirement.

---

## 14. Responsiveness

### Q37. Which UI5 library is fully responsive?
sap.m.

---

### Q38. Which table is recommended for responsive applications?
sap.m.Table.

---

### Q39. Why should fixed widths be avoided?
They break responsiveness across devices.

---

## 15. CSS and Theming

### Q40. How should custom CSS be added?
Custom CSS should be added via manifest.json.

---

### Q41. Why use theme parameters?
To ensure compatibility across light, dark, and high-contrast themes.

---

## Final Notes
- Follow MVC strictly
- Prefer data binding over manual updates
- Use configuration over code
- Follow SAP Fiori design guidelines

---
