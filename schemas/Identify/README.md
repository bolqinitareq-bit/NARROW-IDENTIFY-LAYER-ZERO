# **Identity Schemas — Narrow Identity Layer Zero**

This directory contains the **Identity Schemas** used within Narrow Identity Layer Zero.  
These schemas define how humans, devices, and agents are represented at the identity level, using deterministic, portable, and chain‑agnostic structures.

Identity in Narrow is:

- **root‑based** (anchored to a deterministic identity root)  
- **schema‑driven**  
- **minimal and privacy‑preserving**  
- **token‑less and chain‑agnostic**  
- **consistent across humans, devices, agents, and applications**

These schemas form the foundation for all attestations, reputation models, and access‑control structures built on top of Narrow.

---

## **Included Schemas**

### **1. human-verification.schema.json**  
Defines the verification level of a human identity (basic, strong, biometric, government‑verified) with optional evidence references.

### **2. device-fingerprint.schema.json**  
Represents a deterministic device fingerprint, including device type, fingerprint hash, environment metadata, and optional capabilities.

### **3. agent-profile.schema.json**  
Describes an autonomous agent’s classification, capabilities, model reference, and trust signals.

---

## **Purpose**

These schemas enable:

- human identity verification  
- device authentication  
- agent classification  
- cross‑system identity mapping  
- trust and reputation foundations  
- deterministic identity resolution  

They ensure that every entity in Narrow — human, device, agent, or application — has a **structured, verifiable identity model**.

---

## **Design Principles**

- **Deterministic**  
  Same inputs always produce the same identity representation.

- **Non‑correlatable**  
  No personal or sensitive data is exposed.

- **Composable**  
  Identity schemas can be extended or referenced by other schemas.

- **Portable**  
  Works across chains, agents, devices, and backend systems.

- **Minimal**  
  Only essential fields are included to keep attestations lightweight.
---

## **Status**

This folder contains the **v1** versions of the Identity Schemas.  
Additional schemas (secure enclave identity, virtual instance identity, agent safety profile) will be added in future releases.

---
