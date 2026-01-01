# **Agent Schemas — Narrow Identity Layer Zero**

This directory contains the **Agent Identity Schemas** used within Narrow Identity Layer Zero.  
These schemas define how autonomous agents are represented, evaluated, and trusted across decentralized and traditional systems.

Agents in Narrow can be:

- AI agents  
- automation agents  
- service agents  
- bots  
- hybrid systems  

The goal is to provide a **portable, verifiable identity and capability model** for any type of agent.

---

## **Included Schemas**

### **1. agent-profile.schema.json**  
Base schema describing agent type, capabilities, model reference, and trust signals.

### **2. agent.capability-graph.schema.json**  
Defines the agent’s capabilities, dependencies, and operational constraints.

### **3. agent.safety-profile.schema.json**  
Represents the agent’s risk level, safety measures, and restricted actions.

### **4. agent.behavior-model.schema.json**  
Describes the agent’s behavior model, adaptivity, and behavior evaluation signals.

---

## **Purpose**

These schemas enable:

- agent capability modeling  
- safety classification  
- behavior evaluation  
- trust scoring  
- cross‑system interoperability  
- agent governance and access control  

All without exposing sensitive model internals or requiring chain‑specific logic.

---

## **Status**

This folder contains the **v1** versions of the Agent Schemas.  
More advanced schemas (agent lifecycle, delegation models, multi‑agent coordination) will be added in future releases.

---
