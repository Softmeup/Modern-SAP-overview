# Modern SAP Development Overview: CAP & Fiori Elements

## Essential Resources

* **[CAP Java Backend](https://cap.cloud.sap/docs/java/getting-started)**: Documentation for developing service providers using Java
* **[CAP CDS Definitions](https://cap.cloud.sap/docs/cds/cdl)**: Language used to define data models, services, and annotations in CAP.
* **[CAP Fiori Elements Integration](https://cap.cloud.sap/docs/advanced/fiori#adding-fiori-apps)**: How to use CDS annotations to generate SAP Fiori Elements user interfaces.
* **[CAP Project Initialization](https://cap.cloud.sap/docs/get-started/in-a-nutshell)**: Steps to bootstrap and create a new CAP-based application.
* **[SAP CAP Java Samples](https://github.com/SAP-samples/cloud-cap-samples-java)**: A sample repository demonstrating a complete application using CAP Java for the backend and Fiori Elements for the frontend.
* **[SAP Fiori Tools (VS Code)](https://marketplace.visualstudio.com/items?itemName=SAPSE.sap-ux-fiori-tools-extension-pack)**: Visual Studio Code extension pack for Fiori Elements UI development (e.g., annotation editing, page generation).

## Sample Application Task: Transportation Management

Define a data model and corresponding UI based on the following requirements:

**Data Model:**

* Two primary entities: `TransportationOrder` and `TransportationOrderItem`.
* Relationship: A `TransportationOrder` can have multiple `TransportationOrderItem` records ($1..N$ relationship).
* **`TransportationOrder` Fields:**
    * `displayId`: Human-readable identifier.
    * `description`: Localized text field.
    * `totalWeight`: Calculated field, representing the sum of `weight` from all associated `TransportationOrderItem` records.
* **`TransportationOrderItem` Fields:**
    * `displayId`: Human-readable identifier.
    * `quantity`: Numerical quantity.
    * `weight`: Numerical weight for the item.

**User Interface:**

* **List Report Page:**
    * Displays a list of `TransportationOrder` entities.
    * Provides 'Create' and 'Delete' actions.
    * Allows navigation to the Object Page upon selecting an entry.
* **Object Page:**
    * Displays 'General Information' for a selected `TransportationOrder`.
    * Includes a section (e.g., a table) listing associated `TransportationOrderItem` records.
    * Supports standard 'Edit' functionality, including draft handling.

## Underlying Framework

* **[SAPUI5](https://sapui5.hana.ondemand.com/)**: The core JavaScript UI library that provides the foundation and controls for SAP Fiori Elements applications.
