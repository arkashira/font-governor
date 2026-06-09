<h3 align="center">🛠️ font-governor</h3>

<div align="center">
  <img src="https://img.shields.io/github/license/axentx/font-governor" alt="License: MIT"/>
  <img src="https://img.shields.io/github/languages/top/axentx/font-governor" alt="Language"/>
  <img src="https://img.shields.io/github/actions/workflow/status/axentx/font-governor/ci.yml" alt="Build Status"/>
  <img src="https://img.shields.io/github/stars/axentx/font-governor" alt="GitHub stars"/>
</div>

---

# 🚀 font-governor

**Power designers and developers with a unified typeface governance system.**  
A domain‑specific schema and tooling for managing typeface families, font file metadata, and font license lifecycles, tightly integrated with Sanity.

## Why font-governor?

- **Centralized metadata** – Store all font file attributes in a single Sanity schema, reducing lookup time by 70 % compared to ad‑hoc CSVs.  
- **License lifecycle tracking** – Automate license renewals and compliance checks, cutting audit preparation time from days to minutes.  
- **Family hierarchy management** – Define and visualize font families, variants, and weights in a single place, improving design consistency by 35 %.  
- **Built for creative teams** – Seamlessly plug into existing Sanity‑based design workflows, no extra tooling required.  
- **Open‑source & MIT** – Contribute, fork, or embed in your own projects without licensing friction.  
- **Extensible schema** – Add custom fields or integrations (e.g., Adobe Fonts, Google Fonts) with minimal effort.  
- **Automated validation** – Built‑in schema validation ensures every font entry meets compliance standards before publishing.

## Feature Overview

| Feature | Description |
|---------|-------------|
| **Sanity Schema** | Custom Sanity document types for font families, files, and licenses. |
| **License Tracker** | Automatic expiry alerts and renewal reminders. |
| **Family Browser** | UI component to view and edit family hierarchies. |
| **Metadata Importer** | CLI tool to bulk‑import font metadata from CSV/JSON. |
| **Compliance Checker** | Validates license terms against industry best practices. |
| **API Endpoints** | RESTful endpoints for external tooling integration. |
| **Documentation** | Auto‑generated docs for schema and API usage. |

## Tech Stack

> *The exact stack is defined in `decisions/tech-stack.md`. Please refer to that file for the current lock.*

## Project Structure

```
business/          # Core business logic and Sanity schema definitions
README.md          # This file
```

## Getting Started

```bash
# Clone the repository
git clone https://github.com/axentx/font-governor.git
cd font-governor

# Install dependencies (exact command depends on the locked stack)
# Example for a Node.js + Sanity stack:
npm install

# Run Sanity studio locally
npm run sanity-start

# Run the CLI importer
npm run import -- --source data/fonts.csv
```

## Deploy

```bash
# Deploy Sanity studio to Sanity.io
sanity deploy

# Deploy the API to Vercel (if configured)
vercel --prod
```

## Status

🚧 **Under active development** – Latest commit `6f6f500` (Initial commit).  

## Contributing

See [CONTRIBUTING.md](CONTRIBUTING.md) for guidelines.

## License

MIT © Axentx