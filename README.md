# VeriSync- No more "Trust me Bro"

VeriSync is a **decentralized application (dApp)** that enables **universities, certification bodies, students, and employers** to issue, own, and verify **tamper-proof credentials** on the blockchain.
Every degree or certification becomes a **unique, non-transferable NFT (Soulbound Token)** owned by the individual, stored immutably using **Stellar Soroban smart contracts** and **IPFS**.

---

## 🚀 Overview

VeriSync builds a transparent, fraud-proof ecosystem for credential management where:

* **Issuers** publish verified credentials on the blockchain.
* **Students** own their credentials as NFTs linked to decentralized identity (DID).
* **Employers** verify authenticity instantly without intermediaries.

Powered by **Rust**, **Soroban (Stellar Smart Contracts)**, and **IPFS**, VeriSync ensures **data integrity**, **ownership**, and **instant verification** across organizations and borders.

---

## 🌟 Problem Statement

Traditional credential verification faces multiple issues:

* ❌ **Forgery & Misrepresentation:** Paper or PDF-based credentials can be faked.
* 🕒 **Slow Verification:** Manual background checks take days or weeks.
* 🤩 **Data Silos:** Universities, job portals, and verifiers maintain isolated systems.
* 🔒 **Lack of Ownership:** Students have little control over how their credentials are shared.
* 🌍 **Global Verification Complexity:** Cross-border verification is inefficient and non-standardized.

---

## 💡 Solution

VeriSync addresses these problems through a **blockchain-based credential registry** that:

* Mints each verified degree/certificate as a **Soulbound NFT** (non-transferable).
* Stores proof and metadata on **IPFS**, ensuring decentralization and authenticity.
* Allows **issuers** to register and issue credentials securely via **Soroban smart contracts**.
* Enables **employers** to instantly verify authenticity on-chain by credential ID or wallet address.
* Grants **students full control** and privacy over their verified digital identities.

---

## 🧠 Key Features

| Feature                                      | Description                                                                      |
| -------------------------------------------- | -------------------------------------------------------------------------------- |
| 🧾 **Decentralized Credential Issuance**     | Universities and institutions issue blockchain-verified credentials.             |
| 🦪 **NFT-based Identity (Soulbound Tokens)** | Credentials are unique and non-transferable, tied to the student’s wallet.       |
| 🌐 **Instant Employer Verification**         | Employers verify credentials directly via blockchain data or credential ID.      |
| 🔗 **IPFS Integration**                      | Metadata and certificate files are stored securely on a decentralized network.   |
| 🏛️ **Multi-Issuer Support**                 | Multiple universities, academies, and online institutions can join the platform. |
| ⚠️ **Revocation & Expiry Controls**          | Issuers can revoke or expire credentials when necessary.                         |
| 🕵️ **Decentralized Identity (DID)**         | Wallets are mapped to verified DIDs, linking real-world entities.                |
| 💼 **Transparent Resume Building**           | Candidates can share blockchain-verified resumes and histories.                  |

---

## 👥 Target Users

* **🎓 Students & Professionals:** Own and share verified credentials securely.
* **🏛️ Universities / Institutions:** Issue and manage verifiable digital credentials.
* **💼 Employers / Recruiters:** Instantly verify authenticity of resumes.
* **💜 Certification Bodies:** Publish validated skill and training certifications.
* **🏢 Regulators / Authorities:** Audit and monitor credential authenticity at scale.

---

## 🧩 Tech Stack

| Layer                   | Technology                               |
| ----------------------- | ---------------------------------------- |
| **Smart Contracts**     | Rust + Soroban (Stellar Smart Contracts) |
| **Blockchain Network**  | Stellar Testnet                          |
| **Storage**             | IPFS (InterPlanetary File System)        |
| **Backend API**         | Rust (Axum) or Node.js (Express)         |
| **Frontend**            | React + TypeScript                       |
| **Identity Management** | Decentralized Identifiers (DID)          |
| **Version Control**     | Git + GitHub                             |

---

## 🗓️ Development Roadmap (25 Days)

### **Phase 1 — Foundations (Days 1–4)**

* Learn Stellar, Soroban, and blockchain fundamentals.
* Set up Rust, Soroban CLI, Stellar CLI, and IPFS.
* Design data models and architecture diagrams.
* Define credential lifecycle and DID system.

### **Phase 2 — Smart Contract Development (Days 5–11)**

* Create credential minting, verification, and revocation logic.
* Implement issuer registration and access control.
* Add event logging for transparency.
* Deploy smart contracts to the Stellar testnet.

### **Phase 3 — Backend + IPFS (Days 12–17)**

* Connect blockchain with REST APIs.
* Integrate IPFS for decentralized file storage.
* Implement employer verification endpoint.
* Test full credential issuance and verification pipeline.

### **Phase 4 — Frontend Development (Days 18–22)**

* Design UI/UX for issuers, students, and employers.
* Integrate blockchain and backend APIs.
* Display credentials, metadata, and verification results.
* Polish visuals, navigation, and branding.

### **Phase 5 — Testing, Documentation & Demo (Days 23–25)**

* Perform integration and stress tests.
* Finalize documentation and diagrams.
* Create a live or recorded demo.
* Prepare a professional pitch deck for presentation.

---

## 🧱 System Architecture

```
+-------------------+          +----------------+           +-------------------+
| University /      |          | Soroban Smart  |           |       IPFS        |
| Certification Body|  ----->  | Contract Layer |  ----->   | (Metadata, Files) |
| (Issuer)          |          |  (Verification)|           |                   |
+-------------------+          +----------------+           +-------------------+
          ↓
      Student Wallet (NFT Ownership)
          ↓
    Employer Verification Portal
```

---

## 🔐 Credential Lifecycle

1. **Issuer Registration:**
   Authorized institutions register as credential issuers.

2. **Credential Issuance:**
   Issuer uploads credential data to IPFS, then mints a credential NFT on Stellar.

3. **Ownership Assignment:**
   Credential is linked permanently to the student’s wallet (non-transferable).

4. **Verification:**
   Employer searches credential ID or wallet → system fetches blockchain + IPFS data.

5. **Revocation (Optional):**
   Issuer can revoke a credential through a verified transaction.

---

## 🧮 Installation & Setup

> **Prerequisites:**
>
> * Rust & Cargo
> * Soroban CLI
> * Stellar CLI (Testnet account funded via Friendbot)
> * Node.js (v18+)
> * IPFS Daemon or Infura Account

### 1. Clone Repository

```bash
git clone https://github.com/yourusername/VeriSync.git
cd VeriSync
```

### 2. Setup Smart Contract

```bash
cd contracts
soroban build
soroban deploy --network testnet
```

### 3. Setup Backend

```bash
cd backend
npm install
npm start
```

### 4. Setup Frontend

```bash
cd frontend
npm install
npm run dev
```

---

## 🧩 Data Model Overview

| Entity              | Description                                                                            |
| ------------------- | -------------------------------------------------------------------------------------- |
| **Issuer**          | Registered institution or organization allowed to issue credentials.                   |
| **Credential**      | NFT-bound record linking owner, issuer, and IPFS data.                                 |
| **Student**         | Wallet address representing individual credential owner.                               |
| **Employer**        | Entity verifying credential authenticity.                                              |
| **Metadata (IPFS)** | JSON object containing credential name, date, issuer, hash, and certificate file link. |

---

## 🧪 Testing Scenarios

| Test                      | Expected Result               |
| ------------------------- | ----------------------------- |
| Register new issuer       | Issuer added to registry      |
| Mint credential           | NFT issued to student wallet  |
| Verify credential         | Returns “Valid” with metadata |
| Revoke credential         | Status changes to “Revoked”   |
| Unauthorized mint attempt | Transaction rejected          |

---

## 🛡️ Security Considerations

* Only verified issuers can mint or revoke credentials.
* All sensitive data (names, files) stored off-chain via IPFS.
* Credentials are **non-transferable** (Soulbound NFTs).
* On-chain verification prevents tampering or replay attacks.
* Input validations prevent malformed or malicious CIDs.

---

## 📚 Documentation

### 🧩 Smart Contract Docs

* **Functions:** Register Issuer, Mint Credential, Verify, Revoke.
* **Events:** CredentialIssued, CredentialRevoked.
* **Data Stored:** Credential mappings, issuer registry, status flags.

### 🔧 Backend Docs

* `/api/issue` — Issue new credential.
* `/api/verify/:id` — Verify credential authenticity.
* `/api/revoke/:id` — Revoke credential.

### 🌐 Frontend Docs

* `/issuer` — Dashboard for issuing credentials.
* `/student` — View all owned credentials.
* `/employer` — Search and verify credentials.

---

## 🧱 Architecture Deep Dive

### Components:

* **Smart Contract Layer (Soroban):**
  Handles issuance, verification, revocation, and ownership logic.

* **Backend API Layer:**
  Bridges smart contract and frontend, manages IPFS operations, and caches queries.

* **Storage Layer (IPFS):**
  Stores credential metadata and files, accessible via CIDs linked on-chain.

* **Frontend Layer (React):**
  Provides user interface for all stakeholders, wallet integration, and verification tools.

---

## 📈 Future Enhancements

* Support for **W3C Verifiable Credentials**.
* Integration with **government digital ID systems**.
* QR-based instant credential verification.
* On-chain reputation scoring for issuers.
* Mobile wallet integration for credentials.
* Zero-Knowledge Proofs (ZKPs) for privacy-preserving verification.

---

##
