# System Architecture

This document provides an overview of the architecture of the KnowledgeMint system. It describes the components, their interactions, and the flow of data within the system.

## Architecture Overview

The KnowledgeMint system consists of three main layers:

1. **User Interface** — This is the entry point where users submit knowledge artifacts (data, problems, etc.) through a web-based platform or command-line interface.
2. **AI Assessment Engine** — The AI evaluates the submitted knowledge based on novelty, usefulness, and justification. It also actively generates new knowledge based on existing data.
3. **Blockchain Layer** — This layer ensures decentralization and transparency, storing user balances, minting history, and facilitating exchanges of tokens.


The following diagram illustrates the architecture of KnowledgeMint:

+-------------------------+
|    User Interface       |
|-------------------------|
|  Web Interface          |
|  Command-Line Interface |
|  Wallet Integration     |
+-----------+-------------+
            |
            | Submit Knowledge
            v
+-----------+-------------+
| AI Assessment Engine    |
|-------------------------|
|  Content Analysis       |
|  Knowledge Validation   |
|  Problem Parsing        |
+-----------+-------------+
            |
            | Evaluate Knowledge
            v
+-----------+-------------+
|     AI Database         |
|-------------------------|
|  Store Results          |
+-----------+-------------+
            |
            | Store Results
            v
+-----------+-------------+
|  Blockchain Layer       |
|-------------------------|
|  Mint Tokens            |
|  Store Minting History  |
|  Smart Contracts        |
+-----------+-------------+
            |
            | Mint Tokens
            v
+-----------+-------------+
|      User Wallet        |
+-------------------------+


## 3. Layer Details

### 3.1 User Layer

- **Web App**: Browser-based submission tool for uploading artifacts and problems.
- **CLI/API**: For developers, data scientists, and researchers.
- **Wallet Integration**: KMNT token management via Ethereum-compatible wallets.

### 3.2 AI Evaluation Layer

- **Content Analysis**: Uses LLMs, graph-based scoring, and embedding comparisons.
- **Knowledge Validation**:
  - Novelty (semantic uniqueness)
  - Usefulness (domain relevance)
  - Justification (source & evidence)
- **Problem Parsing**:
  - Clarity
  - Impact
  - Urgency

Evaluation is transparent and auditable.

### 3.3 Minting Orchestrator

- Acts as the bridge between the AI engine and blockchain.
- Generates a minting transaction if criteria are met.
- Logs metadata for reproducibility and governance.

### 3.4 Blockchain Layer

- **Ledger**: Stores token balances, minting records.
- **Smart Contracts**:
  - Token minting contract
  - Submission registry
  - DAO governance (future)
- **Supported Chains**: Initially compatible with Ethereum L2 (Polygon, Arbitrum), potentially evolving into a custom chain.

---

## 4. Modularity & Extensibility

- **Plugin Interfaces**: Future support for domain-specific scoring plugins.
- **External APIs**: Integration with scientific databases and publishing platforms.
- **Audit Layer**: Public logs of minting decisions and evaluation traces.

---

## 5. Security Considerations

- **Anti-Spam Filters**: AI + heuristic rules for submission throttling.
- **Forgery Detection**: Source traceability and citation cross-checking.
- **Human-in-the-Loop**: Optional expert validation for high-stake entries.

---

## 6. Governance

- The architecture is designed to evolve under DAO control.
- Evaluation logic is versioned and open to proposals and votes.

---

_This file is part of the open-source KnowledgeMint protocol. See also:_  
[`TECHNICAL_OVERVIEW.md`](./TECHNICAL_OVERVIEW.md)  
[`KNOWLEDGE_EVALUATION.md`](./KNOWLEDGE_EVALUATION.md)
