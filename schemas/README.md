# **Narrow Identity Layer Zero — Schema Library**

This directory contains the complete **Schema Library** for Narrow Identity Layer Zero.  
Schemas define how identity, devices, agents, reputation, and access‑control data are structured, validated, and interpreted across all systems that integrate with Narrow.

Narrow uses a **schema‑driven architecture** to ensure:

- deterministic validation  
- cross‑system interoperability  
- chain‑agnostic identity modeling  
- minimal, portable attestations  
- composable trust structures  

Every attestation, identity object, or trust signal in Narrow references one of these schemas.

---

## **Schema Families**

### **1. Identity Schemas**  
Located in: `/schemas/identity/`  
Define how humans, devices, and agents are represented at the identity level.

Includes:
- human verification  
- device fingerprinting  
- agent profiles  
- advanced device and agent identity models  

---

### **2. Device Schemas**  
Located in: `/schemas/device/`  
Define physical and virtual device identity, secure enclaves, and network‑level identity.

Includes:
- base device fingerprint  
- secure enclave identity  
- virtual instance identity  
- network identity  

---

### **3. Agent Schemas**  
Located in: `/schemas/agent/`  
Define how autonomous agents are modeled, including capabilities, safety, and behavior.

Includes:
- agent profile  
- capability graph  
- safety profile  
- behavior model  

---

### **4. Reputation Schemas**  
Located in: `/schemas/reputation/`  
Define trust, behavior, compliance, and contribution scoring.

Includes:
- normalized reputation score  
- behavior reputation  
- compliance reputation  
- contribution reputation  

---

### **5. Access Control Schemas**  
Located in: `/schemas/access-control/`  
Define roles, permissions, capabilities, and access groups.

Includes:
- role membership  
- capability tokens  
- permission flags  
- access groups  

---

## **Design Principles**

- **Minimal**  
  Only essential fields are included to keep attestations lightweight.

- **Deterministic**  
  Same inputs always produce the same validation result.

- **Composable**  
  Schemas can reference or extend each other.

- **Chain‑agnostic**  
  Works across any blockchain or off‑chain environment.

- **Evidence‑driven**  
  Many schemas support references to attestations for trust and verification.

- **Versioned**  
  Schemas are immutable once published; updates create new versions.

---

## **Purpose**

The schema library enables:

- unified identity modeling  
- cross‑chain and cross‑system interoperability  
- portable trust and reputation signals  
- agent and device authentication  
- access‑control frameworks  
- deterministic attestation validation  

Schemas are the foundation of Narrow’s **Layer Zero identity substrate**.

---

## **Status**

This directory contains the **v1** schema families for Narrow Identity Layer Zero.  
Additional schemas, advanced models, and reference implementations will be added in future versions.

---
