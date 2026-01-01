# **Device Schemas — Narrow Identity Layer Zero**

This directory contains the **Device Identity Schemas** used within Narrow Identity Layer Zero.  
These schemas define how physical devices, virtual instances, and secure hardware modules are represented in a deterministic, portable, and privacy‑preserving way.

Device identity in Narrow is:

- **root‑based**  
- **schema‑driven**  
- **minimal and non‑correlatable**  
- **chain‑agnostic**  
- **compatible with physical and virtual hardware**  

These schemas form the foundation for device authentication, trust evaluation, and cross‑system interoperability.

---

## **Included Schemas**

### **1. device-fingerprint.schema.json**  
Base fingerprint schema for device type, fingerprint hash, environment metadata, and capabilities.

### **2. device.secure-enclave.schema.json**  
Represents hardware‑backed security modules such as TPM, TEE, Secure Enclave, SGX, or HSM.

### **3. device.virtual-instance.schema.json**  
Identity schema for cloud or virtualized instances (AWS, Azure, GCP, containers, VMs).

### **4. device.network-identity.schema.json**  
Network‑level identity signals such as hashed MAC, hashed IP, and network capabilities.

---

## **Purpose**

These schemas enable:

- device authentication  
- secure enclave verification  
- cloud instance identity  
- network identity modeling  
- cross‑system device trust  
- agent‑device interoperability  

All without exposing sensitive hardware identifiers.

---

## **Status**

This folder contains the **v1** versions of the Device Schemas.  
More advanced schemas (hardware attestation chains, multi‑interface identity, device lifecycle) will be added in future releases.

---
