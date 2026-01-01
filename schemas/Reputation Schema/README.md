
## **README — Access Control Schemas (English)**

This directory contains the **Access Control Schemas** for Narrow Identity Layer Zero.  
These schemas define how roles, permissions, capabilities, and access groups are structured, issued, and verified across decentralized and traditional systems.

Access control in Narrow is:

- **Identity‑rooted**  
- **Schema‑driven**  
- **Token‑less**  
- **Chain‑agnostic**  
- **Composable and minimal**

These schemas form the foundation for any permission or authorization model built on top of Narrow.

---

### **Included Schemas**

#### **1. role-membership.schema.json**  
Defines the role assigned to an entity within a specific domain or subsystem (e.g., admin, member, viewer).

#### **2. capability-token.schema.json**  
Represents a single capability granted to an entity, optionally with constraints or contextual rules.

#### **3. permission-flags.schema.json**  
A flexible boolean permission map suitable for systems with many granular permissions.

#### **4. access-group.schema.json**  
Defines access groups containing members, roles, and optional metadata.

---

### **Purpose**
These schemas enable:

- Role‑based access control (RBAC)  
- Capability‑based access models  
- Permission flag systems  
- Access groups and membership structures  
- Trust‑based authorization  
- Agent capability frameworks  

All without relying on tokens, chain IDs, or platform‑specific logic.

---

### **Status**
This folder contains the **v1** versions of the Access Control Schemas.  
Additional schemas and advanced models will be added in future releases.
