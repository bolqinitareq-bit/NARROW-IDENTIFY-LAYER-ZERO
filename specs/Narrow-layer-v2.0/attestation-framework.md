# **Attestation Framework — Narrow Identity Layer Zero**

## **Overview**
The Narrow Attestation Framework defines how identities, devices, and agents issue, verify, and consume attestations across decentralized and traditional systems.  
It provides a unified, chain‑agnostic model for expressing trust, reputation, and verifiable claims without relying on tokens, fees, or platform‑specific logic.

Attestations in Narrow are portable, composable, and cryptographically verifiable.  
They form the trust fabric that applications and protocols can build on.

---

## **Design Principles**
- **Identity‑rooted**  
  Every attestation is anchored to a deterministic identity root.

- **Schema‑driven**  
  Attestations follow structured, versioned schemas defined in the Schema Registry.

- **Chain‑agnostic**  
  Attestations can be issued and verified on any chain or off‑chain environment.

- **Token‑less**  
  No token is required to issue, verify, or consume attestations.

- **Minimal and composable**  
  Attestations are small, portable objects that can be combined to form higher‑level trust models.

- **Verifiable anywhere**  
  Verification does not depend on a specific blockchain or execution environment.

---

## **Attestation Structure**
Every attestation follows a standardized structure:

```
{
  "attestation_id": "<deterministic-id>",
  "issuer_root": "<identity-root>",
  "subject_root": "<identity-root>",
  "schema_id": "<schema-reference>",
  "payload": { ... },
  "timestamp": "<unix-time>",
  "signature": "<issuer-signature>"
}
```

### **Key Fields**
- **attestation_id**  
  Deterministic identifier derived from issuer, subject, schema, and payload.

- **issuer_root**  
  Identity root of the entity issuing the attestation.

- **subject_root**  
  Identity root of the entity receiving the attestation.

- **schema_id**  
  Reference to the schema that defines the structure of the payload.

- **payload**  
  The actual claim or data being attested.

- **signature**  
  Cryptographic signature proving the issuer’s authority.

---

## **Attestation Types**
Narrow supports multiple attestation categories:

### **1. Identity Attestations**
Claims about the subject’s identity attributes.  
Examples: human verification, device fingerprint, agent classification.

### **2. Reputation Attestations**
Claims derived from behavior, performance, or trust signals.  
Examples: reliability score, compliance rating, contribution history.

### **3. Access Attestations**
Claims that grant or restrict access to systems or resources.  
Examples: role membership, permission flags, capability tokens.

### **4. Custom Attestations**
Application‑specific claims defined through custom schemas.

---

## **Issuance Model**
Attestations can be issued by:

- Humans  
- Devices  
- Autonomous agents  
- Applications  
- Protocols  
- Organizations  

Issuance requires:

1. A valid identity root  
2. A schema reference  
3. A signed payload  

No blockchain transaction is required unless the application chooses to anchor or publish the attestation on‑chain.

---

## **Verification Model**
Verification is deterministic and environment‑agnostic:

1. Resolve issuer and subject identity roots  
2. Fetch the schema definition  
3. Validate payload structure  
4. Verify signature  
5. Optionally check revocation or expiration rules  

Verification can happen:

- On‑chain  
- Off‑chain  
- In AI agents  
- In backend systems  
- In client applications  

---

## **Revocation & Expiration**
Attestations may include:

- **Expiration timestamps**  
- **Revocation references**  
- **Issuer‑controlled revocation lists**  
- **Schema‑defined validity rules**

Revocation is optional and depends on the use case.

---

## **Storage & Portability**
Attestations are portable objects that can be stored:

- Locally  
- In decentralized storage  
- In application databases  
- On‑chain (optional)  
- Inside agent memory systems  

Narrow does not enforce a storage layer — it defines the format and verification logic.

---

## **Use Cases**
- Human identity verification  
- Device authentication  
- Agent classification  
- Reputation systems  
- Access control  
- Compliance and audit trails  
- Cross‑chain identity mapping  
- AI trust signals  

---

## **Status**
The Attestation Framework is part of Narrow Identity Layer Zero v0.2 and is under active development.  
Additional schema definitions and integration guidelines will be published progressively.

