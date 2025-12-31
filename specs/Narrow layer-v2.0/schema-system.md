# **Schema System — Narrow Identity Layer Zero**

## **Overview**
The Schema System defines how identity‑related data is structured, versioned, validated, and interpreted within Narrow Identity Layer Zero.  
Schemas act as the **blueprints** for identity attributes, device fingerprints, agent capabilities, reputation models, and access‑control rules.

Every attestation, resolution output, and identity‑linked object in Narrow is anchored to a schema.  
This ensures consistency, interoperability, and deterministic verification across all systems.

---

## **Design Principles**
- **Structured**  
  Every identity‑related object follows a defined schema.

- **Versioned**  
  Schemas are immutable once published; updates create new versions.

- **Composable**  
  Schemas can reference or extend other schemas.

- **Chain‑agnostic**  
  Schemas work across any blockchain or off‑chain environment.

- **Minimal**  
  Only essential fields are included; no unnecessary complexity.

- **Deterministic**  
  Validation rules produce consistent results across all implementations.

---

## **Schema Structure**
Each schema follows a standardized format:

```
{
  "schema_id": "<unique-id>",
  "version": "v1",
  "entity_type": "human | device | agent | application",
  "fields": {
      "<field-name>": {
          "type": "string | number | boolean | object | array",
          "required": true | false,
          "rules": { ... }
      }
  },
  "rules": {
      "validation": { ... },
      "constraints": { ... }
  }
}
```

### **Key Components**
- **schema_id**  
  Unique identifier for the schema.

- **version**  
  Immutable version tag (e.g., `v1`, `v2`).

- **entity_type**  
  Defines which identity category the schema applies to.

- **fields**  
  Structured definition of the data the schema expects.

- **rules**  
  Validation and constraint logic.

---

## **Schema Categories**
Narrow defines four primary schema families:

### **1. Identity Schemas**
Describe core identity attributes.  
Examples:
- human verification signals  
- device fingerprint structure  
- agent classification metadata  

### **2. Device Schemas**
Describe hardware or software device characteristics.  
Examples:
- device signature  
- environment metadata  
- capability flags  

### **3. Reputation Schemas**
Describe trust and behavior‑based attributes.  
Examples:
- reliability score  
- compliance rating  
- contribution metrics  

### **4. Access‑Control Schemas**
Describe permissions, roles, and capability models.  
Examples:
- role membership  
- access flags  
- capability tokens  

---

## **Schema Lifecycle**

### **1. Definition**
A schema is drafted and structured according to the Narrow format.

### **2. Publication**
Once published, a schema becomes immutable.

### **3. Versioning**
Updates create new versions:
```
v1 → v2 → v3
```
Older versions remain valid for backward compatibility.

### **4. Adoption**
Applications, agents, and protocols reference schemas when issuing or verifying attestations.

---

## **Schema Validation**
Validation ensures that any attestation or identity object conforms to its schema.

Validation steps:

1. Fetch schema definition  
2. Validate field types  
3. Check required fields  
4. Apply field‑level rules  
5. Apply schema‑level rules  
6. Return deterministic validation result  

Validation is environment‑agnostic and can run:

- on‑chain  
- off‑chain  
- in agents  
- in backend systems  

---

## **Schema Referencing**
Schemas can reference other schemas to enable composability.

Example:
```
"fields": {
  "device": {
      "type": "object",
      "schema_ref": "device.v1"
  }
}
```

This allows complex identity models to be built from smaller, reusable components.

---

## **Schema Registry**
The Schema Registry is the canonical index of all published schemas.

Registry responsibilities:

- Store schema definitions  
- Track versions  
- Provide lookup by schema_id  
- Ensure immutability  
- Enable cross‑system interoperability  

The registry can be implemented:

- off‑chain  
- on‑chain  
- hybrid  
- decentralized storage  

Narrow does not enforce a specific implementation.

---

## **Security Considerations**
- Schemas contain no sensitive data  
- Schemas are immutable once published  
- Validation is deterministic and cryptographically verifiable  
- Applications control which schemas they trust  
- Schema composition must avoid circular references  

---

## **Use Cases**
- Identity modeling  
- Device authentication  
- Agent capability definitions  
- Reputation systems  
- Access‑control frameworks  
- Compliance and audit structures  
- Cross‑chain identity mapping  
- AI trust signals  

---

## **Status**
The Schema System specification is part of Narrow Identity Layer Zero v0.2 and is under active development.  
Additional schema families and reference implementations will be published in future versions.

