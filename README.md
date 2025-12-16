# StellarGauge

Built for Base

StellarGauge is a concise Base-native repository intended to validate connectivity, RPC access, and wallet onboarding flows on Base networks using official Coinbase tooling.

The project emphasizes infrastructure verification rather than application logic, making it suitable for quick Base environment checks and repeatable testing.

---

## Target Networks

Base Mainnet  
- chainId (decimal): 8453  
- Explorer: https://basescan.org  
- RPC endpoint: https://mainnet.base.org  

Base Sepolia  
- chainId (decimal): 84532  
- Explorer: https://sepolia.basescan.org  
- RPC endpoint: https://sepolia.base.org  

---

## Runtime Overview

Main file: `app/stellarGauge.ts`

At runtime, the application:
- Initializes an OnchainKit provider bound to the selected Base network
- Presents wallet connection UI via OnchainKit Wallet
- Uses a Viem public client for Base JSON-RPC reads
- Queries:
  - RPC-reported chainId
  - latest block number
  - native ETH balance for a provided address
- Displays Basescan explorers for transparent inspection

---

## Repository Structure

- app/
  - stellarGauge.ts  
    React-based entry file combining wallet UX with Base RPC reads.

Common auxiliary files expected in the repository:
- package.json
- tsconfig.json
- index.html / main.tsx
- .env (optional)

---

## Tooling

- OnchainKit  
  Wallet components and Base-oriented primitives  
  https://github.com/coinbase/onchainkit  

- Viem  
  EVM client used for Base chain queries  

---

## Installation Notes

Requirements:
- Node.js 18+
- Browser environment with wallet support

Install dependencies via your preferred package manager and run using a standard React/Vite or Next.js dev setup.

Optional configuration:
- VITE_BASE_RPC_URL
- VITE_BASE_SEPOLIA_RPC_URL

---

## Usage Flow

1. Launch the app in a browser
2. Select Base Sepolia for testing or Base Mainnet for production reads
3. Connect a wallet through the OnchainKit interface
4. Provide an address to query balance data
5. Execute the probe and review results
6. Follow Basescan links for further inspection

---

## Base Mainnet Deployment

Deployed on Base Mainnet

Network: Base Mainnet  
chainId (decimal): 8453  
Explorer: https://basescan.org  

Deployed contract address:  
your_adress  

Basescan deployment and verification links:
- Contract address:  
  https://basescan.org/address/your_adress  
- Contract verification (source code):  
  https://basescan.org/address/your_adress#code  

---

## License

MIT License

---

## Author

GitHub: https://github.com/your-handle  
Public contact (email): your-name@proton.me  
Public contact (X): https://x.com/your-handle  

---

## Testnet Deployment (Base Sepolia)

For pre-mainnet validation, up to several contracts can be deployed on Base Sepolia to ensure compatibility with Base tooling and explorers.

Network: Base Sepolia  
chainId (decimal): 84532  
Explorer: https://sepolia.basescan.org  

Contract #1 address:  
your_adress  

Deployment and verification:
- https://sepolia.basescan.org/address/your_adress  
- https://sepolia.basescan.org/your_adress/0#code  

Contract #2 address (optional):  
your_adress  

Deployment and verification:
- https://sepolia.basescan.org/address/your_adress  
- https://sepolia.basescan.org/your_adress/0#code  

Contract #3 address (optional):  
your_adress  

Deployment and verification:
- https://sepolia.basescan.org/address/your_adress  
- https://sepolia.basescan.org/your_adress/0#code  

These testnet deployments serve as a controlled environment for validating Base account abstraction flows, RPC reliability, and read-only onchain operations before mainnet usage.
