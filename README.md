# Decentralized Onchain Pension Fund Administrator

[![Hackathon Badge](https://img.shields.io/badge/Octant%20DeFi%20Hackathon-2025-blueviolet)](https://octant.devfolio.co/) [![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](https://opensource.org/licenses/MIT) [![Solidity](https://img.shields.io/badge/Solidity-^0.8.20-green)](https://soliditylang.org/)

## Project Overview

This project introduces a decentralized, onchain pension fund administrator built on Octant v2's Yield Donating Vaults. It aims to disrupt and replace traditional pension institutions by providing a trustless, global alternative for retirement savings. Traditional pensions suffer from high fees (1-2%), opacity, centralized control, and limited accessibility—often requiring employers or specific geographies. Our solution leverages DeFi to enable:

- **Permissionless Participation**: Anyone can deposit USDC (simulating employee/employer contributions) without KYC or intermediaries.
- **Transparent Yield Generation**: Funds are diversified across high-yield protocols (Aave v3 Vaults, Spark, Yearn v3), generating sustainable returns.
- **Vesting and Security**: Time-locked withdrawals (minimum 30 days) to mimic pension vesting, preventing impulsive spending.
- **Inheritance Mechanisms**: Beneficiaries can claim funds after an inactivity period (365 days), simulating payouts for death or disability.
- **Social Impact via Public Goods**: Excess yield is automatically donated to a configurable "Pension DAO" multisig, funding web3 contributor "retirements" (e.g., OSS developers via Gitcoin), creating a self-sustaining ecosystem.
- **Cost Efficiency**: DeFi fees (~0.5%) vs. traditional 1-2%; fully auditable onchain.
- **Programmability**: Future extensions for recurring deposits (e.g., via Gelato), tax reporting, or multi-asset support.


## Features
- **Diversified Investment Strategy**: Allocates deposits equally (~33%) to Aave v3 Vault, Spark Lending, and Yearn v3 Vault (deployed via Kalani) for risk-managed yield.
- **Pension-Like Mechanics**:
  - Time-locked withdrawals to enforce long-term saving.
  - Beneficiary designation and claim function for secure inheritance.
- **Automated Donations**: Yield beyond base is donated to public goods, configurable via constructor (e.g., Gitcoin or custom DAO).
- **User-Friendly dApp**: Simple frontend for deposits, withdrawals, beneficiary settings, and claims.
- **Security**: Inherits Octant's BaseHealthCheck; adds ReentrancyGuard and nonReentrant modifiers.

## Tech Stack
- **Smart Contracts**: Solidity ^0.8.20, Foundry for testing/deployment.
- **Base Framework**: Octant v2 (YieldDonatingTokenizedStrategy, BaseHealthCheck).
- **Integrations**:
  - Aave v3 ERC-4626 Vault (for bounty-specific use).
  - Spark Lending Pool.
  - Yearn v3 Vault (deployed with Kalani).
- **Frontend**: Scaffold-ETH 2 (React, ethers.js) for wallet interactions.
- **Chain**: Ethereum Sepolia testnet (mainnet compatible).
- **Dependencies**: OpenZeppelin, Spark, Yearn, Aave libraries.

Built by UhOh.eth for Octant DeFi Hackathon 2025. Let's decentralize pensions! 🚀
