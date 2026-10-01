# Script-Controlled ACL – Restrict Record Access Based on Field Value

## 📌 Project Overview
This project focuses on implementing advanced security and access control mechanisms within **ServiceNow** using script-driven **Access Control Lists (ACLs)**. By moving beyond static role-based access, this implementation dynamically evaluates user permissions against record-level field values (e.g., using server-side JavaScript to check `current.<field_name>`) and specific organizational roles to control CRUD operations.

---

## 👥 Team Members
* **Gokula Krishnan K** – *Team Leader*
* **Gogul krishnan R** – *Team Member*
* **Dhanush K** – *Team Member*

---

## 🧩 Modules
1. **User & Role Administration Module:**
   * Setup of test users, group mappings, and custom role assignments required for security testing.
2. **Schema & Table Definition Module:**
   * Configuration of custom ServiceNow tables, choice fields, and status indicators evaluated by security rules.
3. **Scripted Security & ACL Engine:**
   * Dynamic script-driven ACL definitions governing system access across four core database operations: READ, CREATE, WRITE, and DELETE.

---

## ✨ Features Implemented
* **User & Role Provisioning:** Created specialized user accounts and custom security roles to simulate distinct operational access levels.
* **Custom Table & Schema Design:** Designed tables with specific field conditions (e.g., State, Category, Assignment Group) to serve as triggers for access checks.
* **Scripted READ ACL:** Evaluates read visibility dynamically based on user identity, role, and the state of field values on individual records.
* **Scripted CREATE ACL:** Enforces conditional record creation permissions dependent on active user roles and designated field selections.
* **Scripted WRITE ACL:** Restricts field-level and record-level edit capabilities based on specific field state changes and approval conditions.
* **Scripted DELETE ACL:** Enforces strict deletion protection, permitting record removal only under specific high-privilege conditions and status values.
* **Validation & End-to-End Testing:** Conducted impersonation-based functional testing across all roles to ensure expected policy execution without data exposure.

---

## 🚀 How to Import / Deploy
1. Navigate to **System Update Sets > Local Update Sets** in your ServiceNow instance.
2. Click **Import Update Set from XML** and select the XML update file located in this repository.
3. Preview and commit the Update Set to apply the custom tables, roles, users, and ACL configurations.
