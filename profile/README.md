# **Akyba Protocol**

### *(You can copy/paste this directly into your GitHub repo)*

````markdown
# Akyba Protocol  
### ROSCA v1.1.1 • ASCA v1.0.1 • CIP-68 Identity • Cardano eUTxO  
**Fund 15 — Cardano Use Cases: Prototype & Launch**

---

<img src="docs/diagrams/rosca.png" width="650"/>

---

## 1. Overview

Akyba Protocol is a **decentralized savings and micro-credit primitive** built on Cardano.  
It converts traditional community finance systems (ROSCA "tontines" and ASCA credit groups) into **transparent, permissionless, verifiable state machines** running fully on the eUTxO ledger.

This repository hosts the **Catalyst prototype implementation** for Fund 15, including:

- Plutus V2 smart contracts  
- CIP-68 membership identity system  
- State Thread Token (STT) mechanism  
- Off-chain backend services (TypeScript or Haskell)  
- Minimal web/mobile UI for testnet interactions  
- Documentation, diagrams, and formal whitepapers

Akyba aims to become the **first Cardano-native, high-volume, community-driven financial primitive** suitable for Africa, Asia, and global ROSCA/ASCA markets.

---

## 2. Problem

Community savings systems (ROSCA/ASCA) suffer from:

- lack of transparency  
- risk of fraud or mismanagement  
- no auditability  
- no automated enforcement of contributions  
- no collateral-based guarantees  
- no fair loan governance  
- no dispute resolution  
- no standardized digital identity  

Billions of dollars circulate yearly in informal tontines.  
No blockchain protocol currently provides a **verifiable, programmable, identity-bound implementation**.

---

## 3. Why Cardano?

Cardano’s eUTxO model, native tokens, and Plutus V2 validators uniquely enable:

- deterministic, immutable group rules  
- CIP-68 metadata for on-chain identity  
- token-bound membership  
- state machines without global mutable state  
- predictable, low-fee monthly cycles  
- programmable collateral logic  
- verifiable loan governance on-chain  

Akyba is designed **exclusively** for Cardano’s architecture.  
It is not a port from Ethereum.

---

## 4. Value Proposition and Ecosystem Gap

### 4.1 Ecosystem Research Summary  
(Full research included in `/docs/ecosystem-research.md`)

Findings:

- No Catalyst project or live Cardano dApp implements a full ROSCA or ASCA engine.
- No project provides on-chain CIP-68 membership + collateral slashing + contribution cycles.
- Micro-lending tools exist but lack governance, state guarantees, or identity binding.

### 4.2 Uniqueness  
Akyba introduces:

- **CIP-68 programmable identity tokens per member**
- **Collateral-backed savings cycles**
- **State Thread Token state machine**  
- **Loan application and voting flows**
- **Batch contribution & distribution transactions**
- **UTxO-based fairness guarantees**

Akyba is a **new financial primitive**, not a DeFi derivative.

---

## 5. Architecture

### 5.1 High-Level Components

- `plutus/` – Smart contracts (ROSCA, ASCA, CIP-68 minting, STT)  
- `offchain/` – Backend services (TypeScript or Haskell)  
- `frontend/` – Minimal UI for testnet prototype  
- `docs/` – Whitepapers, diagrams, specs

### 5.2 Core Tokens

- **STT** (State Thread Token): unique UTxO with group state  
- **CIP-68 Tokens**:  
  - UserToken  
  - RefToken  
  - LoanApp Token (ASCA)  

---

## 6. Protocol Flow

### 6.1 ROSCA (v1.1.1)

<img src="docs/diagrams/rosca.png" width="650"/>

Features:
- Init → Join → Start → Contribute → Distribute → Rejoin → End → Withdraw  
- Collateral slashing for late/missing contributions  
- Batch contribution logic  
- Winner nomination rules  

### 6.2 ASCA (v1.0.1)

<img src="docs/diagrams/asca.png" width="650"/>

Features:
- Loan application  
- Voting (Yes / No with voting power = contributions)  
- Borrow, Repay, Liquidate  
- Unlock period  
- Kick inactive members  
- End group & refunds  

### 6.3 eUTxO Architecture

<img src="docs/diagrams/utxo.png" width="650"/>

---

## 7. Whitepaper & Documentation

- **IEEE-style Whitepaper (PDF)**  
  `/docs/Akyba-IEEE-Whitepaper.pdf`  
- **ROSCA v1.1.1 Specification**  
  `/docs/spec-rosca.md`  
- **ASCA v1.0.1 Specification**  
  `/docs/spec-asca.md`  
- **Technical Diagrams**  
  `/docs/diagrams/*.png`  

---

## 8. Catalyst Prototype Goal (Fund 15)

Deliver a **working Akyba prototype** deployed to Cardano Preprod or Preview testnet, enabling:

- Create a ROSCA or ASCA group  
- Mint STT + CIP-68 tokens  
- Join group  
- Submit contributions  
- Execute distributions 
- Apply for loans (ASCA)  
- Vote on loans  
- Borrow & repay  
- End group & withdraw  

All via UI + backend + contracts.

This aligns perfectly with Catalyst “prototype & launch”.

---

## 9. Milestones (≤ 12 months)

| Month | Milestone | Deliverable |
|------|-----------|-------------|
| 1–2  | Contract scaffolding + STT/CIP-68 | Smart contract structure |
| 3–4  | Implement ROSCA contract | Init/Join/Start/Contribute/Distribute |
| 5–6  | Implement ASCA contract | Loan flows + Voting + Repay |
| 7–8  | Off-chain backend | APIs + integration |
| 9    | Prototype UI | Web/mobile demo |
| 10–11| Testnet deployment | Public access + documentation |
| 12   | Community testing | Feedback report |

---

## 10. Team

### Ange Thierry Yobo — Lead Architect  
- Fintech CTO, Cardano developer  
- Creator of Oxalio (tax infra) + AyaPay (mobile money)  
- Expertise: UTxO, Java/Spring, TypeScript, full-stack finance systems  
- GitHub: *link*  
- LinkedIn: *link*

### Co-Founders / Engineering  
(Names + links added later)

---

## 11. Running the Prototype (Placeholder)

This section will be updated as contracts are implemented.

```bash
# clone
git clone https://github.com/akylabs/akyba-protocol
cd akyba-protocol

# build plutus contracts
cabal build

# run backend server
cd offchain
npm install
npm run dev
````

---

## 12. License

Apache 2.0 (to be confirmed)

---

## 13. Contact

Email: [contact@akyba.io](mailto:contact@akyba.io)
Telegram: [https://t.me/akyba](https://t.me/akyba)
Twitter: [https://twitter.com/akyba](https://twitter.com/akyba)

---

### Akyba is designed to become the **first large-scale Cardano-native financial primitive powering millions of global ROSCA and ASCA users**.

```
