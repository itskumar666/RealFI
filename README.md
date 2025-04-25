
# 🏠 RealEstateFi

**Tokenized Real Estate + DeFi Lending Protocol**

RealEstateFi lets verified property owners tokenize their land and monetize it through yield generation and decentralized lending. It brings real-world assets (RWAs) onto the blockchain and enables users to earn, borrow, and govern—trustlessly.

## ✨ Features

- **Property Verification** via ERC-721 NFTs tied to off-chain legal proof  
- **Fractional Ownership** with ERC-20 tokens per property  
- **Yield Rewards** based on property value growth (via oracles)  
- **Lending Protocol** where users borrow stablecoins using property tokens  
- **Governance** powered by the reward token (`YIELD`)

## 🛠 Tech Stack

- **Solidity + Foundry** for smart contracts  
- **ERC-721 / ERC-20** token standards  
- **Chainlink (mock)** oracles for property prices  
- **Optional:** React + Wagmi + IPFS for frontend & storage

## 🧱 Architecture

```
contracts/
│
├── PropertyNFT.sol             → ERC721 token for verified property
├── PropertyRegistry.sol        → Registry + verification tracking
├── FractionalTokenFactory.sol  → ERC20 token deployment per property
├── YieldToken.sol              → Daily minted reward token
├── LendingPool.sol             → Lending logic (collateral + liquidation)
└── OracleMock.sol              → Simulated property price oracle

scripts/
└── deploy.s.sol                → Foundry deploy script

test/
└── *.t.sol                     → Unit tests
```

## 📅 Roadmap

### Phase 1 – Property Setup  
- Property NFT contract  
- Registry with verification hash  
- Manual property approval (off-chain doc simulation)

### Phase 2 – Tokenization + Rewards  
- Fractional token factory per verified property  
- Reward token (`YIELD`)  
- Oracle-mocked dynamic emission per property

### Phase 3 – Lending System  
- Accept fractional tokens as collateral  
- Borrow stablecoins (USDC)  
- Liquidation system

### Phase 4 – Governance & Testnet  
- Governance via `YIELD`  
- Simple CLI / dApp UI  
- Deploy to Sepolia or zkSync testnet

## 📦 Quick Start

```bash
git clone https://github.com/your-username/realestatefi
cd realestatefi
forge install
forge build
forge test
```

## 🙌 Contributing

- Prioritize modular, gas-efficient, and secure code  
- Suggest improvements to verification, emissions, or lending logic

## ⚠️ Disclaimer

For demo and educational purposes only. Not financial advice.
