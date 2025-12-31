# **Identity Root — Narrow Identity Layer Zero**

## **Overview**
The Identity Root is the foundational primitive of Narrow Identity Layer Zero.  
It provides a deterministic, portable, and chain‑agnostic representation of any entity — human, device, agent, or application.

An Identity Root is not an account, not a wallet, and not a keypair.  
It is a **stable identity anchor** that all schemas, attestations, and trust relationships derive from.

---

## **Design Principles**
- **Deterministic**  
  The same inputs always produce the same identity root.

- **Portable**  
  Works across chains, systems, and environments without modification.

- **Key‑agnostic**  
  Not tied to a specific cryptographic key or wallet.

- **Minimal**  
  A small, fixed‑length representation that can be embedded anywhere.

- **Composable**  
  Can be used as the base for schemas, attestations, and resolution mappings.

- **Neutral**  
  No tokens, no fees, no platform dependencies.

---

## **Identity Root Structure**
An Identity Root is derived from a structured set of inputs:

```
identity_root = HASH(
    entity_type,
    entropy_source,
    optional_metadata
)
```

### **Components**
- **entity_type**  
  Defines whether the root belongs to a human, device, agent, or application.

- **entropy_source**  
  A deterministic seed used to derive the root.  
  This can be:
  - a device fingerprint  
  - a human verification seed  
  - an agent initialization seed  
  - an application‑defined seed  

- **optional_metadata**  
  Non‑sensitive metadata that helps classify or resolve the identity.

---

## **Properties**
### **1. Deterministic**
Given the same seed and entity type, the identity root will always be identical.

### **2. Non‑correlatable**
Identity roots do not expose personal data, device identifiers, or cryptographic keys.

### **3. Non‑revocable**
Identity roots are permanent anchors.  
Attestations and schemas can be revoked — the root itself cannot.

### **4. Non‑transferable**
Identity roots cannot be sold, transferred, or reassigned.

### **5. Chain‑agnostic**
Identity roots do not depend on:
- blockchain accounts  
- chain IDs  
- smart contracts  
- execution environments  

They are universal.

---

## **Identity Root Format**
The final representation is a compact, encoded string:

```
<version>:<entity-type>:<hash>
```

Example:

```
v1:agent:0x8f3a…c91e
```

---

## **Root Categories**
Narrow defines four primary identity categories:

### **1. Human Root**
Represents a verified human identity.  
Used for reputation, compliance, and trust signals.

### **2. Device Root**
Represents a physical or virtual device.  
Used for authentication, access control, and telemetry trust.

### **3. Agent Root**
Represents an autonomous agent (AI or software).  
Used for agent classification, capability attestations, and behavior tracking.

### **4. Application Root**
Represents an application or service.  
Used for issuing attestations, managing schemas, and interacting with other systems.

---

## **Root Lifecycle**
Identity roots follow a simple lifecycle:

1. **Initialization**  
   Entity generates or receives a deterministic seed.

2. **Derivation**  
   Identity root is computed using the Narrow hashing model.

3. **Binding**  
   Schemas and attestations are linked to the root.

4. **Resolution**  
   Applications resolve the root to its associated data.

Identity roots do not expire and cannot be reassigned.

---

## **Security Model**
- Identity roots contain no private keys.  
- Compromise of a device or agent does not compromise the root.  
- Attestations and schemas can be revoked independently.  
- Verification is purely cryptographic and environment‑agnostic.

---

## **Use Cases**
- Human identity verification  
- Device authentication  
- Agent classification  
- Cross‑chain identity mapping  
- Reputation systems  
- Access control  
- Compliance frameworks  
- AI trust layers  

---

## **Status**
The Identity Root specification is part of Narrow Identity Layer Zero v0.2 and is under active development.  
Additional derivation methods and resolution mechanisms will be published in future versions.

---
