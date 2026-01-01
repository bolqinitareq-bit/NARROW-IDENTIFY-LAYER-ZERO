# **Narrow Identity Layer Zero — Specifications**

This directory contains the **core technical specifications** of Narrow Identity Layer Zero.  
These documents define the architecture, data models, validation rules, and interoperability standards that form the foundation of the Narrow protocol.

The specifications in this folder represent the **canonical source of truth** for how Narrow works across identity, attestations, schemas, resolution, and integration layers.

---

## **Purpose of the Specifications**

The specs in this directory serve as the authoritative reference for:

- developers integrating Narrow  
- protocol designers  
- AI agent frameworks  
- device identity systems  
- auditors and security reviewers  
- investors evaluating the architecture  
- contributors building on top of Narrow  

Each document defines a self‑contained part of the protocol, and together they form the complete Layer Zero identity substrate.

---

## **Included Specification Files**

### **1. identity-root.md**  
Defines the deterministic, chain‑agnostic identity root model for humans, devices, agents, and applications.

### **2. schema-system.md**  
Describes the schema architecture, versioning model, validation rules, and schema registry.

### **3. attestation-framework.md**  
Specifies how attestations are structured, issued, validated, and resolved across systems.

### **4. resolution-layer.md**  
Explains how identity roots are resolved into schemas, attestations, metadata, and external mappings.

### **5. integration-layer.md**  
Defines how external systems (chains, apps, agents, devices) integrate with Narrow using a unified interface.

---

## **Versioning**

This folder contains the **v0.2** specification set — the first unified version of Narrow as a full **Layer Zero identity protocol**.

Older versions are archived under:

```
/specs/archive/
```

Each version is immutable once finalized.

---

## **Design Principles**

- **Minimal** — only essential components, no unnecessary complexity  
- **Deterministic** — same inputs always produce the same outputs  
- **Composable** — components can be combined or extended  
- **Chain‑agnostic** — works across any blockchain or off‑chain system  
- **Portable** — identity and attestations move across ecosystems  
- **Evidence‑driven** — trust is based on verifiable attestations  
- **Transparent** — clear versioning and evolution history  

---

## **Status**

The v0.2 specification is under active development.  
Additional components, examples, and reference implementations will be added progressively as Narrow evolves.


