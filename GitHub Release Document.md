# Payroll App — Unified SQL Express & SQL Server Edition
## Initial GitHub Release — Version 1.1.0

This release introduces the fully unified version of the Payroll App, combining all features and license tiers into a single Windows `.exe` application. The app supports both SQL Express and SQL Server, selected during installation, eliminating the need for separate builds or database versions.

All license tiers (Basic, Pro, Enterprise) are included in one unified application, with access determined by the user’s Gumroad license key.

The Payroll App can operate in:
• Standalone Mode (using its own Payroll_App_DB)  
• Integrated Mode (connecting to any AIAI CRM App database)

Supported CRM Apps:
• Gutter App  
• Plumbing App  
• Roofing App  
• Handyman App  
• Electrician App  
• Insulation App  
• Landscaping App  
• Production Manager App  

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
- Custom overtime rule engine  
- Payroll periods and locking  
- Time entry manager  
- Job pay manager  
- Employee manager  
- Full offline operation after activation  

---

## Plan Descriptions

### Basic Plan
Provides essential payroll management features for individuals or small teams.  
Includes core payroll tools, employee management, time entry, job pay, and standard reporting.  
Ideal for users who need a reliable, cost‑effective payroll foundation.

---

### Pro Plan
Expands on the Basic plan with enhanced productivity tools and deeper reporting.  
Designed for growing teams that manage multiple employees and need more flexibility.  
Includes advanced overtime rule configuration and expanded payroll period controls.

---

### Enterprise Plan
Unlocks the full capabilities of the system, including everything in Pro plus enterprise‑grade controls.  
Required for organizations with multiple administrators or complex operational needs.

Enterprise includes:
- Priority support  
- Advanced overtime rule profiles  
- Multi‑CRM switching  
- Database migration tools  
- Additional administrative controls  

---

## License Activation
This app requires a valid Gumroad license key to unlock full functionality.

- You will be prompted to enter your license key on first launch.  
- The app verifies your key securely via Gumroad’s API.  
- If the license is invalid or revoked, access will be restricted.  
- Internet access is required for initial license validation.

After activation, the app operates fully offline.

---

## Database
The Payroll App supports two database modes, selected during installation:

### SQL Express (Local Database — Recommended for 1–5 users)
- Automatically installed and configured by the installer  
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

No data is ever mixed between CRM systems.

---

## Stability
This version is the current stable build distributed through the updater and serves as the foundation for all future updates.
