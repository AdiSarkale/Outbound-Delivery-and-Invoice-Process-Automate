# Outbound Delivery & Invoice Process Automation

> **Copyright © 2026 Aditya Sarkale — All Rights Reserved to the extent of rights owned by the author.**
>
> No license is granted to copy, modify, redistribute, publish, sublicense, sell, or otherwise use substantial portions of this source code without prior written permission from the applicable rights holder.
>
> Company-owned, client-owned, SAP-proprietary, third-party, or confidential material remains subject to its applicable rights and agreements.

## Overview

This repository contains automation components for outbound delivery, invoice and related SAP document-processing workflows, together with a React/Vite web interface.

## Repository Structure

```
backend/     Python automation and backend services
website/     React/Vite web interface
```

The backend contains SAP connection handling, transaction-specific automation modules and input processing. The website provides the browser interface used to trigger and display workflow results.

## Technology

- Python
- Flask/backend services
- pywin32 / SAP GUI Scripting
- React
- Vite
- JavaScript
- CSV/Excel processing

## Prerequisites

- Windows
- SAP GUI for Windows
- SAP GUI Scripting enabled
- Python 3.x
- Node.js/npm
- Appropriate SAP authorization

## Backend Setup

Use the dependency and entry-point files present in the current `backend/` directory.

```powershell
cd backend
python -m venv venv
venv\Scripts\activate
pip install -r requirements.txt
```

If no `requirements.txt` exists in the current backend version, use the project's maintained dependency documentation/source imports rather than installing an assumed dependency set.

## Website Setup

```powershell
cd website
npm install
npm run dev
```

The `package.json` in `website/` is the source of truth for available scripts.

## Typical Workflow

1. Log in to SAP GUI.
2. Start the backend.
3. Start the website.
4. Provide the required input.
5. Trigger the automation.
6. Python connects to the active SAP GUI scripting session.
7. The required SAP workflow is executed.
8. Status/results are returned to the website.
9. Validate the resulting SAP documents.

## Troubleshooting

### "SAP not logged in or User cancelled the transaction"

If SAP is visibly logged in:

1. Confirm the correct SAP GUI session is active.
2. Open **RZ11**.
3. Check the required dynamic SAP GUI scripting parameter.
4. Confirm the parameter is **TRUE**.
5. Check whether the transaction was manually cancelled.
6. Escalate server-side configuration changes to the authorized SAP Basis team.

### Website inaccessible

Use the organization's approved internal server startup/restart procedure. Internal server names, credentials and confidential infrastructure details are intentionally not published here.

## Security

Never commit:

- SAP passwords
- API keys/tokens
- Cookies/session data
- Confidential company files
- Production exports
- Internal infrastructure credentials

## Author

**Aditya Sarkale**  
GitHub: https://github.com/AdiSarkale
