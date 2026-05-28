Payroll App – User Guide
====================================
Version: 2.0.0

Welcome to the Automating Innovating AI Payroll App — a secure, flexible, and fully automated payroll engine designed to run standalone or integrate seamlessly with all AIAI CRM Apps.

This application calculates payroll using custom overtime rules, piece‑rate logic, job‑pay, and hourly wages, all driven by a guided question system.

Core Architecture
-----------------
• Global Admin + Local Admin RBAC  
• company_id data isolation  
• Shared core tables (Companies, Divisions, Regions, Users, Roles, Permissions)  
• Centralized RBAC enforcement  
• Modular feature access per app  
• Inventory App + Payroll App integration  
• Offline‑first operation with secure local SQL storage  

============================================================
ADMIN ROLES
============================================================

GLOBAL ADMIN (Corporate Level)
• Creates companies, divisions, and regions  
• Manages subscription plans and license upgrades  
• Manages all admins (global + local)  
• Controls payroll schedules and exports  
• Oversees inventory, suppliers, and purchase orders  
• Integrates Payroll App and Inventory App with CRM modules  
• Full access to all reports and data  

LOCAL ADMIN (Division/Region Level)
• Enters employee job tickets and production data  
• Reviews work tickets before payroll is processed  
• Manages inventory and POs if permissions allow  
• Cannot modify subscription plans or corporate settings  
• Access limited by assigned role + permissions  

============================================================
OPERATING MODES
============================================================

Standalone Mode
---------------
Use the Payroll App independently with its own internal payroll database.

Integrated Mode
---------------
Connect to any AIAI CRM App database, including:
• Gutter App  
• Plumbing App  
• Roofing App  
• Handyman App  
• Electrician App  
• Production Manager App  

Switch between CRM databases at any time using the built‑in CRM Database Switcher.

============================================================
KEY FEATURES
============================================================

Secure Login
------------
• Encrypted admin authentication  
• Session verification for protected modules  

Custom Overtime Rule Engine
---------------------------
Define your company’s overtime rules using a guided question system:
• Daily overtime  
• Daily double‑time  
• Weekly overtime  
• Weekend overtime  
• Holiday overtime  
• 7th consecutive day overtime  
• Piece‑rate overtime  
• Blended‑rate calculations  
• Job‑pay overtime premiums  

Employee Management
-------------------
• Add, edit, and manage employees  
• Supports hourly, piece‑rate, and job‑pay types  
• Assign overtime rule profiles per employee  
• Set base hourly rates  

Time Entry Management
---------------------
• Log daily hours worked  
• Assign optional Job IDs  
• Import or manually enter time entries  
• Supports CRM‑linked or standalone workflows  

Job Pay Management
------------------
• Add job‑based pay entries  
• Supports multi‑employee job pay  
• Automatically included in payroll calculations  

Payroll Periods
---------------
• Create payroll periods with start and end dates  
• Close periods to lock data  
• Prevents accidental edits after payroll is finalized  

Payroll Calculation
-------------------
Automatically calculates:
• Regular hours  
• Overtime hours  
• Double‑time hours  
• Piece‑rate earnings  
• Blended‑rate overtime premiums  
• Job‑pay earnings  
• Total pay per employee  

CRM Database Switching
----------------------
• Select any CRM App database  
• Switch between CRM systems at any time  
• Keeps all CRM data isolated  
• Payroll App internal tables remain untouched  

Data Protection
---------------
• Prevents duplicate entries  
• Validates all inputs  
• Ensures safe and consistent payroll data  

Friendly Interface
------------------
• Clean, simple navigation  
• No technical knowledge required  

============================================================
SYSTEM REQUIREMENTS
============================================================
• Windows 10 or later  
• SQL Server Express or full SQL Server  
• ODBC Driver 18 for SQL Server  
• Internet connection required for initial license activation  
• ~50 MB disk space for internal payroll database  

============================================================
LICENSE ACTIVATION
============================================================
A valid Stripe subscription is required to use this application.

• On first launch, the app checks your subscription status securely through Stripe.
• If your subscription is active, the app unlocks full access.
• If your subscription is canceled, expired, or unpaid, access is restricted.
• Internet is required only during subscription verification and plan changes.
• All billing and upgrades are handled through Stripe’s secure checkout.

============================================================
GETTING STARTED
============================================================
1. Launch PayrollApp.exe  
2. Complete Stripe activation process
3. Connect to SQL Server  
4. Choose Standalone Mode or select a CRM Database  
5. Navigate to the Admin Interface  
6. Configure your Overtime Rules  
7. Add Employees  
8. Enter Time Entries and Job Pay  
9. Create a Payroll Period  
10. Run Payroll  

============================================================
NAVIGATION & EXITING
============================================================
• Use the dashboard to access all modules  
• Click Exit on any screen to close the app  
• Use Switch CRM Database to change CRM systems at any time  

============================================================
TIPS
============================================================
• Configure overtime rules before running payroll  
• Keep CRM databases clearly named  
• Export payroll results regularly for backup  
• Use strong admin credentials  
• Keep SQL Server updated  

============================================================
TROUBLESHOOTING
============================================================

Cannot connect to SQL Server:
• Verify server name, credentials, and network access  

CRM database not appearing:
• Ensure the CRM App is installed and its database exists  

Payroll calculation errors:
• Confirm overtime rules and employee types are set correctly  

============================================================
SUPPORT
============================================================
Questions or feedback?  
automatinginnovatingai@outlook.com  

Thank you for using the Payroll App!
