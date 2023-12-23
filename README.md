## BLUEPRINT FOR THE STABLE COIN
1. Relative stability: pegged/anchored -> $1
    1. chainlink price feed
    2. set a function to exchage ETH and BTC -> $$$
2. Stability Mechanism (Minting): Algorithmic (Decentralised)
    1. People can only mint stable coin using enough collateral (coded)
3. Collateral: Exogenous (Crypto) 
    1. wETH
    2. wBTC
4. Unit and Fuzz tests. 

Certainly! Here's a concise README for the provided Solidity smart contract:

---

# Decentralized Stablecoin Engine (DSCEngine)

### Overview
The DSCEngine is the core contract within the Decentralized Stablecoin (DSC) system. It manages logic for minting and redeeming DSC tokens, handling collateral deposits and withdrawals, ensuring over-collateralization, and maintaining a stable 1 token = $1 peg.

### Key Features
- **Stability**: Maintains a 1 token = $1 peg at all times.
- **Over-collateralization**: Requires users to deposit more than the equivalent value of DSC they wish to mint.
- **Collateral Management**: Allows users to deposit, redeem, and manage collateral against their minted DSC tokens.
- **Liquidation Mechanism**: Enables users to liquidate insolvent accounts with a 10% bonus for assuming their debts.

### Components
- **Token Collateralization**: Tracks collateral deposits per user and facilitates minting/redeeming of DSC.
- **Health Factor Calculation**: Determines user solvency based on collateral value against minted DSC.
- **Liquidation Functionality**: Allows for partial user liquidation, ensuring system solvency.

### Usage
- **Collateral Deposit & DSC Minting**: Users can deposit collateral and mint DSC in a single transaction.
- **Collateral Redemption & DSC Burning**: Users can redeem collateral and burn DSC in a single transaction.
- **Liquidation**: Enables users to liquidate insolvent accounts, gaining a 10% bonus from the collateral.

### Customization
- **Supported Tokens**: Configurable list of supported ERC20 tokens for collateralization.
- **Adjustable Parameters**: Thresholds for liquidation, bonus percentages, and minimum health factors are customizable.

### Deployment
Deploy the contract with specified ERC20 tokens and price feed addresses, along with the associated Decentralized Stablecoin contract.

### Disclaimer
This contract is inspired by MakerDAO's DSS system, providing stability and collateral-backed minting of DSC tokens. Review and deploy with caution. Adjust parameters to suit specific use cases.

---
