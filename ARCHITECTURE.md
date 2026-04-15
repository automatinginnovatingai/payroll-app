# Payroll App – Architecture Overview

## Overview
The Payroll App is a closed‑source Windows `.exe` application built for offline operation, secure license enforcement, and automated payroll calculation. It provides a fast, local payroll engine capable of running standalone or integrating with any AIAI CRM App. Unlike cloud‑based payroll systems, the Payroll App runs entirely on the user’s machine or internal network, ensuring reliability, data ownership, and zero external dependencies.

The application supports both SQL Server Express and Full SQL Server, selected during installation.

---

# Architecture

## Database Selection (Installer‑Driven)
During installation, the user selects one of two supported database modes:

### 1. SQL Server Express (Local Database – Recommended for 1–5 Users)
- Installer automatically installs and configures SQL Server Express
- Ideal for single‑machine setups or small office networks
- No licensing cost

### 2. Full SQL Server (Standard/Enterprise)
- User connects to an existing SQL Server instance
- Supports multi‑user environments and IT‑managed deployments
- Designed for medium to large companies

The installer writes a registry flag (`UseSQLExpress`) that determines which connection setup page the application loads on first launch.

---

## License Enforcement Flow
User Launch → License Prompt → Gumroad API Validation → Local Unlock

- User enters their Gumroad license key on first launch  
- Key is validated through Gumroad’s `/v2/licenses/verify` endpoint  
- Valid keys unlock the application and store the license state locally  
- Periodic revalidation may occur (e.g., every 7 days)  
- License tier determines access to Basic, Pro, or Enterprise features  

---

## Local Session Context
- All data is stored in SQL Server Express or Full SQL Server  
- No cloud sync, Redis, or external session store  
- Secure login using salted + hashed admin credentials  
- Fully offline operation after initial license activation  

---

## Standalone vs Integrated Modes

### Standalone Mode
The Payroll App operates using its own internal database (`Payroll_App_DB`) containing:
- PayrollEmployees  
- PayrollTimeEntries  
- PayrollJobPay  
- PayrollPeriods  
- PayrollOvertimeRules  

This mode requires no CRM apps installed.

### Integrated Mode (Multi‑CRM Support)
The Payroll App can connect to any AIAI CRM App database, including:

• Gutter App  
• Plumbing App  
• Roofing App  
• Handyman App  
• Electrician App  
• Insulation App  
• Landscaping App  
• Production Manager App  

Users may switch CRM databases at any time using the built‑in CRM Database Switcher.

The Payroll App automatically:
- Uses Payroll_App_DB for its internal tables  
- Uses the selected CRM DB for employees, job pay, and time‑entry data  

No data is ever mixed between CRM systems.

---

## Data Transfer Between Computers
The app includes a built‑in SQL migration tool for moving data to a new machine:

- Creates a `.bak` backup file from the old computer  
- Restores the `.bak` file on the new computer  
- Works for both SQL Express and Full SQL Server  
- Ideal for machine upgrades or office migrations  

---

## SQL Connection Pages
The application routes users to the correct connection setup page based on installer selection:

- `sql_connection_page.py` – SQL Express  
- `sql_server_connection_page.py` – Full SQL Server  

Both pages support:
- Connection testing  
- Credential validation  
- Database creation (if needed)  
- Secure admin login setup  

---

## Payroll Workflow
Admin Login → Select CRM DB (optional) → Enter Data → Run Payroll → Export

The Payroll App supports multiple pay calculation methods:
- Hourly wage  
- Piece‑rate  
- Job‑pay  
- Blended‑rate overtime  
- Daily overtime  
- Weekly overtime  
- Double‑time  
- Weekend and holiday overtime  
- 7th consecutive day overtime  

All rules are defined using a guided question system and stored in the Payroll App database.

---

## File Storage & Export
All payroll exports are stored locally under:

Documents/AIAI_Payroll_App/Payroll_Exports/YYYY-MM/

Exports include:
- Employee payroll summaries  
- Detailed breakdowns of regular, overtime, and double‑time hours  
- Piece‑rate and job‑pay earnings  
- Period‑based reports  

Excel must be installed to open exported files.
