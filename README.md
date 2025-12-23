# Frost Anchorline (Built for Base)

Frost Anchorline is a compact, browser-first Base diagnostic utility designed for inspecting public onchain state without broadcasting transactions. It focuses on fast validation of Base connectivity and explorer-linked verification.

---

## Capabilities overview

The application provides a minimal read-only surface for Base networks:

- Coinbase Wallet connection using EIP-1193  
- Validation of Base-compatible chainIds (8453 / 84532)  
- ETH balance inspection for arbitrary addresses  
- Latest block metadata retrieval  
- Direct Basescan links for independent verification  

No transactions are signed or sent.

---

## Repository layout

- app/frost-anchorline.ts  
  Browser script handling wallet connection, chain validation, and RPC reads.

- contracts/  
  Solidity contracts deployed to Base Sepolia for testnet validation:
  - control.sol — minimal deployment verification contract  
  - storage.sol — simple stateful interaction contract  
  - structs.sol — lightweight contract for read-only queries
    
- docs/overview.md  
  Internal notes covering validation flow and dependency mapping.

- package.json  
  Dependency manifest referencing Coinbase SDKs and multiple Base repositories.

- README.md  
  Technical documentation and testnet deployment records.

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

This repository integrates tooling from the Base and Coinbase open-source ecosystems:

- Coinbase Wallet SDK for wallet access  
- OnchainKit references for Base-aligned primitives  
- viem for typed, efficient read-only RPC communication  
- Multiple Base and Coinbase GitHub repositories referenced directly  

---

## License

MIT License

Copyright (c) 2025 fauna-cyan0e

---

## Author

GitHub: https://github.com/fauna-cyan0e  
Email: fauna_cyan0e@icloud.com  
discord: modizan5876  

---

## Testnet Deployment (Base Sepolia)

As part of pre-production validation, one or more contracts may be deployed to the Base Sepolia test network to confirm correct behavior and tooling compatibility.

Network: Base Sepolia  
chainId (decimal): 84532  
Explorer: https://sepolia.basescan.org  

Contract #1 address:  
0x3ea48941cafd72ca1855073ba0cdea91454e1aa3

Deployment and verification:
- https://sepolia.basescan.org/address/0x3ea48941cafd72ca1855073ba0cdea91454e1aa3
- https://sepolia.basescan.org/0x3ea48941cafd72ca1855073ba0cdea91454e1aa3/0#code  

Contract #2 address:  
0x02d8e38745b589a7ebcbefb5c55bb4652cfd70a2 

Deployment and verification:
- https://sepolia.basescan.org/address/0x02d8e38745b589a7ebcbefb5c55bb4652cfd70a2
- https://sepolia.basescan.org/0x02d8e38745b589a7ebcbefb5c55bb4652cfd70a2/0#code  

Contract #3 address:  
0xd375773e18d8cca7a5c7ec1174f62dc4da9fa873 

Deployment and verification:
- https://sepolia.basescan.org/address/0xd375773e18d8cca7a5c7ec1174f62dc4da9fa873
- https://sepolia.basescan.org/0xd375773e18d8cca7a5c7ec1174f62dc4da9fa873/0#code  

These testnet deployments provide a controlled environment for validating Base tooling, account abstraction flows, and read-only onchain interactions prior to Base Mainnet usage.
