
# MyToken Smart Contract

This repository contains the source code for a custom ERC20 token smart contract called `MyToken`. The contract is implemented in Solidity and includes functionality for minting, burning, and transferring tokens.

## Overview

`MyToken` is an ERC20 token that inherits from OpenZeppelin's `ERC20` and `Ownable` contracts. It allows the contract owner to mint new tokens, burn existing tokens, and transfer tokens to other addresses.

**## Getting Started**

### Prerequisites

- Remix IDE (or any Solidity development environment)
- MetaMask (or any Ethereum wallet for deploying and interacting with the contract)

### Installation

1. CREATE the `MyToken.sol` file in Remix IDE.
2. Write the necessary code(https://github.com/mranand2004/module3/blob/main/mytoken.sol)
3. Compile and deploy the contract using Remix.

### Deployment

1. Deploy the `MyToken` contract in Remix IDE.

2. Use the `Remix VM(Cancun)` environment in Remix to interact with the deployed contract.

### Interacting with the Contract

Once deployed, you can interact with the `MyToken` contract using the following functions:

- **Mint Tokens**: Allows the owner to create and assign new tokens to a specified address.
  
  ```solidity
  function mint(address to, uint256 amount) public onlyOwner {
      _mint(to, amount);
  }
  ```

- **Burn Tokens**: Allows any token holder to burn (destroy) their own tokens.

  ```solidity
  function burn(uint256 amount) public {
      _burn(msg.sender, amount);
  }
  ```

- **Transfer Tokens**: Allows any token holder to transfer tokens to another address.

  ```solidity
  function transfer(address recipient, uint256 amount) public override returns (bool) {
      return super.transfer(recipient, amount);
  }
  ```

## License

This project is licensed under the MIT License. See the [LICENSE](./LICENSE) file for details.

---
