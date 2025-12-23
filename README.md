# Cinder Brookvault (Built for Base)

Cinder Brookvault is a lightweight, browser-based utility for the Base ecosystem. It is designed to validate Base network connectivity and inspect public onchain data using strictly read-only interactions.

---

## Repository layout

- app/cinder-brookvault.ts  
  Browser entry point responsible for wallet connection, network validation, and RPC-based reads.

- config/networks.json  
  Static configuration defining Base networks, including chain IDs, RPC endpoints, and explorer URLs.

- contracts/  
  Solidity contracts deployed on Base Sepolia for testnet validation:
  - control.sol — minimal contract for deployment verification  
  - minimal.sol — simple stateful contract for interaction checks  
  - errors.sol — lightweight contract optimized for read-only queries  

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

## Contacts:

GitHub: https://github.com/squab-01

Email: squab-01.unwary@icloud.com 

Public contact: https://x.com/mimi04793 

---

## Testnet Deployment (Base Sepolia)

For pre-production validation, one or more contracts may be deployed to the Base Sepolia test network to confirm tooling compatibility and expected behavior.

Network: Base Sepolia  
chainId (decimal): 84532  
Explorer: https://sepolia.basescan.org  

Contract #1 address:  
0xdbC470C23c4A57b29d32275F1877FB6790D16441 
- https://sepolia.basescan.org/address/0xdbC470C23c4A57b29d32275F1877FB6790D16441 
- https://sepolia.basescan.org/address/0xdbC470C23c4A57b29d32275F1877FB6790D16441#code  

Contract #2 address:  
0xf573C33C0462F7A9Ad055E51Ea43DBe212c559Bb 
- https://sepolia.basescan.org/address/0xf573C33C0462F7A9Ad055E51Ea43DBe212c559Bb  
- https://sepolia.basescan.org/address/0xf573C33C0462F7A9Ad055E51Ea43DBe212c559Bb#code  

Contract #3 address:  
0xe5415729564B3910057adb23a1062630F6B9360f
- https://sepolia.basescan.org/address/0xe5415729564B3910057adb23a1062630F6B9360f 
- https://sepolia.basescan.org/address/0xe5415729564B3910057adb23a1062630F6B9360f#code  

These testnet deployments provide a controlled environment for validating Base tooling, account abstraction flows, and read-only onchain access before Base Mainnet usage.
