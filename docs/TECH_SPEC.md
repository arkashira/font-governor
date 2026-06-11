# TECH_SPEC.md
## Technical Specification
### Overview
The font-governor project aims to provide a unified typeface governance system for designers and developers. This technical specification outlines the architecture, components, data model, key APIs/interfaces, tech stack, dependencies, and deployment strategy for the project.

### Architecture Overview
The font-governor system consists of the following components:

* **Sanity Schema**: A custom Sanity document type for font families, files, and licenses.
* **License Tracker**: A service responsible for automatic expiry alerts and renewal reminders.
* **Family Browser**: A UI component for viewing and editing family hierarchies.
* **Metadata Importer**: A CLI tool for bulk-importing font metadata from CSV/JSON files.
* **Compliance Checker**: A service that validates license terms against industry best practices.
* **API Endpoints**: RESTful endpoints for external tooling integration.

### Components
#### Sanity Schema
The Sanity schema is defined in the `business` directory and consists of the following document types:

* **Font Family**: A document type representing a font family, with fields for family name, description, and variants.
* **Font File**: A document type representing a font file, with fields for file name, format, and license.
* **License**: A document type representing a license, with fields for license name, terms, and expiry date.

#### License Tracker
The License Tracker service is responsible for sending automatic expiry alerts and renewal reminders. It uses the Sanity schema to retrieve license information and sends notifications via email or other notification channels.

#### Family Browser
The Family Browser UI component allows users to view and edit family hierarchies. It uses the Sanity schema to retrieve font family information and displays it in a tree-like structure.

#### Metadata Importer
The Metadata Importer CLI tool allows users to bulk-import font metadata from CSV/JSON files. It uses the Sanity schema to validate and import the metadata.

#### Compliance Checker
The Compliance Checker service validates license terms against industry best practices. It uses the Sanity schema to retrieve license information and checks it against a set of predefined rules.

#### API Endpoints
The API Endpoints provide a RESTful interface for external tooling integration. They allow users to retrieve and update font family, file, and license information.

### Data Model
The data model for the font-governor system consists of the following entities:

* **Font Family**: A font family, with attributes for family name, description, and variants.
* **Font File**: A font file, with attributes for file name, format, and license.
* **License**: A license, with attributes for license name, terms, and expiry date.

### Key APIs/Interfaces
The font-governor system provides the following APIs/interfaces:

* **Sanity API**: A RESTful API for interacting with the Sanity schema.
* **License Tracker API**: A RESTful API for interacting with the License Tracker service.
* **Family Browser API**: A RESTful API for interacting with the Family Browser UI component.
* **Metadata Importer API**: A RESTful API for interacting with the Metadata Importer CLI tool.
* **Compliance Checker API**: A RESTful API for interacting with the Compliance Checker service.

### Tech Stack
The tech stack for the font-governor system is defined in the `decisions/tech-stack.md` file. The current lock includes:

* **Node.js**: A JavaScript runtime environment.
* **Sanity**: A headless CMS platform.
* **Vercel**: A platform for deploying and hosting web applications.

### Dependencies
The font-governor system depends on the following packages:

* **@sanity/client**: A JavaScript client for interacting with the Sanity API.
* **@sanity/types**: A set of TypeScript types for working with the Sanity API.
* **node-csv**: A package for working with CSV files in Node.js.
* **json-schema**: A package for working with JSON schemas in Node.js.

### Deployment
The font-governor system can be deployed using the following commands:

* **Sanity Studio**: `sanity deploy`
* **API**: `vercel deploy`

Note: The deployment process may vary depending on the specific tech stack and dependencies used.
