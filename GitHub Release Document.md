# Payroll App — Unified SQL Express & SQL Server Edition
## Initial GitHub Release — Version 2.0.0

This release introduces the fully unified version of the Payroll App, redesigned for the new AIAI architecture. 
All features and license tiers (Basic, Pro, Enterprise) are now included in a single Windows `.exe` application. 
The app supports both SQL Server Express and Full SQL Server, selected during installation, eliminating the need 
for separate builds or database versions.

The Payroll App can operate in:
• Standalone Mode (using its own Payroll_App_DB)  
• Integrated Mode (connecting to any AIAI CRM App database)

Supported CRM Apps:
• Gutter App  
• Plumbing App  
• Roofing App  
• Handyman App  
• Electrician App  
• Production Manager App  

All CRM connections enforce strict `company_id` isolation.

---

## Included in This Release
- Basic Plan  
- Pro Plan  
- Enterprise Plan  
- Unified SQL Express + SQL Server architecture  
- One installer, one app, one onboarding flow  
- Standalone payroll engine  
- Multi‑CRM database integration  
- CRM Database Switcher UI  
- Centralized RBAC enforcement  
- Plan‑tier enforcement (Basic / Pro / Enterprise)  
- Custom overtime rule engine  
- Payroll periods + locking  
- Time entry manager + editor  
- Job pay manager + editor  
- Employee manager  
- Payroll export engine (Excel/PDF)  
- Audit logs (Enterprise)  
- Full offline operation after activation  

---

## Plan Descriptions

### Basic Plan
Provides essential payroll management features for individuals or small teams.  
Includes:
- Employee list  
- Time entry viewing  
- Job pay viewing  
- Basic payroll reporting  
- View‑only access to Pro/Enterprise screens  

Ideal for users who need a reliable, cost‑effective payroll foundation.

---

### Pro Plan
Expands on the Basic plan with full editing capabilities and advanced payroll tools.  
Designed for growing teams that manage multiple employees and need more flexibility.

Includes:
- Full time entry management  
- Full job pay management  
- Payroll period creation + closing  
- Advanced overtime rule configuration  
- Piece‑rate + blended‑rate support  
- Payroll exports (Excel/PDF)  

---

### Enterprise Plan
Unlocks the full capabilities of the system, including everything in Pro plus enterprise‑grade controls.

Enterprise includes:
- Priority support  
- Multi‑CRM database switching  
- Audit logs  
- Multi‑division/region filtering  
- Advanced reporting  
- Additional administrative controls  
- Global Admin tools  

---

## License Activation
A valid Gumroad license key is required to unlock full functionality.

- You will be prompted to enter your license key on first launch  
- The app verifies your key securely via Gumroad’s API  
- If the license is invalid or revoked, access is restricted  
- Internet access is required for initial validation  

After activation, the app operates fully offline.

---

## Database
The Payroll App supports two database modes, selected during installation:

### SQL Express (Local Database — Recommended for 1–5 users)
- Automatically installed and configured  
- Ideal for individuals, small teams, and single‑machine setups  
- Fully offline and self‑contained  

### SQL Server (Remote or On‑Prem Server)
- Connect to an existing SQL Server instance  
- Supports multi‑user environments and IT‑managed deployments  
- Ideal for medium‑to‑large teams or companies with dedicated servers  

Both modes use the same unified application and feature set.

---

## Standalone Mode
In standalone mode, the Payroll App uses its own internal database (`Payroll_App_DB`) to store:
- Employees  
- Time entries  
- Job pay  
- Payroll periods  
- Overtime rules  
- Audit logs (Enterprise)  

No CRM apps are required.

---

## Integrated Mode (Multi‑CRM Support)
The Payroll App can connect to any AIAI CRM App database, including:
- Gutter App  
- Plumbing App  
- Roofing App  
- Handyman App  
- Electrician App  
- Production Manager App  

Users may switch CRM databases at any time using the CRM Database Switcher.

The Payroll App automatically:
- Uses Payroll_App_DB for internal payroll tables  
- Uses the selected CRM DB for employee, job pay, and time‑entry data  
- Enforces strict `company_id` isolation  

No data is ever mixed between CRM systems.

---

## Stability
This version is the current stable build distributed through the updater and serves as the foundation for all future updates.  
It includes major architectural upgrades, improved RBAC, plan enforcement, SQL Server unification, and enhanced reliability.

