
# **Resolution Layer — Narrow Identity Layer Zero**

## **Overview**
The Resolution Layer is the mechanism that connects identity roots to their associated schemas, attestations, metadata, and external mappings.  
It acts as the lookup and interpretation layer of Narrow Identity Layer Zero, enabling applications, agents, and protocols to understand **what an identity represents** and **how it should be used**.

Resolution is deterministic, chain‑agnostic, and does not depend on any specific storage or blockchain environment.

---

## **Design Principles**
- **Universal**  
  Works across Web2, Web3, AI agents, and device ecosystems.

- **Deterministic**  
  The same identity root always resolves to the same structured output.

- **Modular**  
  Applications can resolve only what they need (schemas, attestations, metadata, mappings).

- **Token‑less**  
  No fees or tokens are required for resolution.

- **Flexible Storage**  
  Resolution can be implemented locally, off‑chain, on‑chain, or through hybrid models.

- **Privacy‑preserving**  
  Identity roots contain no personal or sensitive data.

---

## **Resolution Model**
The Resolution Layer defines a standard interface for retrieving identity‑linked data.

### **Resolution Request**
```
resolve(identity_root)
```

### **Resolution Output**
```
{
  "identity_root": "...",
  "schemas": [...],
  "attestations": [...],
  "metadata": {...},
  "mappings": {...}
}
```

Each field is optional depending on the implementation and the application’s needs.

---

## **Resolution Components**

### **1. Schema Resolution**
Retrieves all schema definitions associated with an identity.

```
resolve_schemas(identity_root)
```

Output:
```
[
  {
    "schema_id": "...",
    "version": "v1",
    "fields": {...}
  }
]
```

Schemas define the structure of identity‑related data.

---

### **2. Attestation Resolution**
Retrieves all attestations issued **to** or **by** the identity.

```
resolve_attestations(identity_root)
```

Output:
```
[
  {
    "attestation_id": "...",
    "issuer_root": "...",
    "subject_root": "...",
    "schema_id": "...",
    "payload": {...},
    "timestamp": "...",
    "signature": "..."
  }
]
```

Attestations form the trust and reputation layer.

---

### **3. Metadata Resolution**
Retrieves optional metadata associated with the identity root.

```
resolve_metadata(identity_root)
```

Metadata may include:
- classification (human, device, agent, application)  
- creation timestamp  
- optional descriptive tags  

Metadata is always non‑sensitive.

---

### **4. Mapping Resolution**
Retrieves external identifiers linked to the identity root.

```
resolve_mappings(identity_root)
```

Mappings may include:
- blockchain addresses  
- device IDs  
- agent IDs  
- application accounts  
- off‑chain identifiers  

Mappings are application‑defined and optional.

---

## **Resolution Flow**
A typical resolution flow:

1. **Input**: identity_root  
2. **Fetch**: schemas, attestations, metadata, mappings  
3. **Validate**: structure and signatures  
4. **Assemble**: unified resolution object  
5. **Return**: deterministic output to the caller

Resolution can be partial or full depending on the request.

---

## **Storage Flexibility**
The Resolution Layer does not enforce a storage model.  
Implementations may use:

- Local storage  
- Decentralized storage (IPFS, Arweave, etc.)  
- Application databases  
- Smart contracts  
- Hybrid models  

This flexibility allows Narrow to integrate with any ecosystem.

---

## **Security Considerations**
- Identity roots contain no private keys  
- Resolution does not expose sensitive data  
- Attestations are cryptographically verifiable  
- Applications control their own mapping logic  
- Storage layers can be permissioned or public  

---

## **Use Cases**
- Identity lookup  
- Agent trust evaluation  
- Device authentication  
- Reputation systems  
- Access control  
- Compliance and audit  
- Cross‑chain identity mapping  
- AI agent verification  

---

## **Status**
The Resolution Layer specification is part of Narrow Identity Layer Zero v0.2 and is under active development.  
Additional resolution strategies and reference implementations will be published in future versions.

---
