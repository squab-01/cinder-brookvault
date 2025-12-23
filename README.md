# Cinder Brookvault (Built for Base)

Cinder Brookvault is a lightweight, browser-based utility for the Base ecosystem. It is designed to validate Base network connectivity and inspect public onchain data using strictly read-only interactions.

---

## Repository layout

- app.cinder-brookvault.ts  
  Browser entry point responsible for wallet connection, network validation, and RPC-based reads.

- config/networks.json  
  Static configuration defining Base networks, including chain IDs, RPC endpoints, and explorer URLs.

- docs/design.md  
  Architectural notes describing Base alignment and enforced read-only constraints.

- docs/testnet-checks.md  
  Validation notes collected during testing on Base Sepolia.

- scripts/sample-inputs.json  
  Example addresses used for repeatable inspection and testing flows.

- contracts/  
  Solidity contracts deployed on Base Sepolia for testnet validation:
  - your_contract.sol — minimal contract for deployment verification  
  - your_contract.sol — simple stateful contract for interaction checks  
  - your_contract.sol — lightweight contract optimized for read-only queries  

- package.json  
  Dependency manifest referencing Coinbase SDKs and multiple Base and Coinbase repositories.

- README.md  
  Project documentation and deployment references.

---

## Capabilities overview

- Coinbase Wallet connection via EIP-1193  
- Validation of Base-compatible chain IDs (8453 / 84532)  
- ETH balance and nonce inspection  
- Latest block metadata retrieval  
- Direct Basescan links for quick verification  

No transactions are signed or broadcast.

---

## Base network context

Base Mainnet  
chainId (decimal): 8453  
Explorer: https://basescan.org  

Base Sepolia  
chainId (decimal): 84532  
Explorer: https://sepolia.basescan.org  

---

## Tooling and dependencies

This repository integrates tools from the Base and Coinbase open-source ecosystems:

- Coinbase Wallet SDK for wallet connectivity  
- OnchainKit references for Base-aligned primitives  
- viem for typed, efficient, read-only RPC access  
- Multiple Base and Coinbase GitHub repositories included as dependencies  

---

## License

MIT License  
Copyright (c) 2025 YOUR_NAME

---

## Author

GitHub: https://github.com/
Email: you@example.com  
Public contact: https://x.com/your-handle  

---

## Testnet Deployment (Base Sepolia)

For pre-production validation, one or more contracts may be deployed to the Base Sepolia test network to confirm tooling compatibility and expected behavior.

Network: Base Sepolia  
chainId (decimal): 84532  
Explorer: https://sepolia.basescan.org  

Contract #1 address:  
your_address  
- https://sepolia.basescan.org/address/your_address  
- https://sepolia.basescan.org/address/your_address#code  

Contract #2 address:  
your_address  
- https://sepolia.basescan.org/address/your_address  
- https://sepolia.basescan.org/address/your_address#code  

Contract #3 address:  
your_address  
- https://sepolia.basescan.org/address/your_address  
- https://sepolia.basescan.org/address/your_address#code  

These testnet deployments provide a controlled environment for validating Base tooling, account abstraction flows, and read-only onchain access before Base Mainnet usage.
