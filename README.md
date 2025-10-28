# 🪙 Simple Token DApp (Base Sepolia)

A minimal ERC-20 token deployed on **Base Sepolia** using Remix.  
This project was created to learn smart contract deployment and boost Base onchain score.

---

## ⚙️ Contract Overview
- **Name:** Simple Token  
- **Symbol:** SIM  
- **Total Supply:** 1000 SIM  
- **Network:** Base Sepolia (ChainID 84532)

---

## 🧠 Steps
1. Open [Remix IDE](https://remix.ethereum.org)
2. Create a new file `SimpleToken.sol`
3. Paste the contract below and compile with Solidity 0.8.20
4. Connect MetaMask → Select *Base Sepolia*
5. Deploy and copy the contract address

```solidity
// SPDX-License-Identifier: MIT
pragma solidity ^0.8.20;
import "@openzeppelin/contracts/token/ERC20/ERC20.sol";

contract SimpleToken is ERC20 {
    constructor() ERC20("Simple Token", "SIM") {
        _mint(msg.sender, 1000 * 10 ** decimals());
    }
}
