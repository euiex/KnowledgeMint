# KnowledgeMint MVP Blockchain Specification

## 🎯 Goal

Develop a minimal Substrate-based blockchain that lays the foundation for the KnowledgeMint protocol, focusing on:

- Token issuance (KMNT)
- Knowledge registration as NFTs
- Basic DAO governance
- Placeholder for AI-based evaluation

## 📦 Core Components

### 1. KMNT Token Pallet
- Fungible token (KMNT), compatible with PSP22/ERC20 standards
- Functions: minting, burning, transfers

### 2. Knowledge NFT Pallet
- Each NFT represents a knowledge asset
- Properties: owner, IPFS hash, evaluation score (AI stub), timestamp
- Optional: Compatibility with RMRK/UNIQUE standards

### 3. AI Verifier Placeholder
- Simple field for “AI Evaluation” stored in the NFT metadata
- External interface to be developed later

### 4. DAO Governance Pallet
- Simple on-chain voting: proposals, quorum, majority rule
- Token-weighted voting using KMNT
- Optional: basic treasury module

## 🌐 Infrastructure

- Built with: Substrate Node Template
- Network: testnet (local & public)
- Off-chain knowledge storage: IPFS links
- Interfaces: CLI + basic REST API for external apps

## 🗓 Roadmap

| Phase | Timeline     | Deliverables                                  |
|-------|--------------|-----------------------------------------------|
| 1     | Week         | Substrate setup, test network, GitHub CI      |
| 2     | Week         | KMNT token + NFT pallets                      |
| 3     | Week         | Governance pallet (basic on-chain voting)     |
| 4     | Week         | IPFS integration + testing                    |
| 5     | Week         | Full MVP on testnet + basic documentation     |

## 🔮 Future Extensions

- Full integration with AI Verifier system
- Smart contracts (Ink! or EVM-based via Moonbeam)
- DAO treasury logic and funding mechanisms
- Migration to parachain or Moonbeam collator

---

