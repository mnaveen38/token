# Token 

## Overview

This repository contains a Solidity smart contract for a basic ERC-20 token. The ERC-20 standard is a widely used standard for fungible tokens on the Ethereum blockchain. This token contract extends functionality from OpenZeppelin's ERC20, ERC20Burnable, and Ownable contracts, providing features such as burning tokens, minting tokens, and ownership management.

## Smart Contract Features

### ERC-20 Standard

The `Token` contract complies with the ERC-20 standard, providing the following basic functionalities:

- **Transfer**: Users can transfer tokens to other addresses.
- **Approval**: Users can approve other addresses to spend tokens on their behalf.
- **TransferFrom**: Addresses with approval can transfer tokens on behalf of the token owner.

### Minting

The contract allows the owner to mint additional tokens. The `mintTokens` function is restricted to the contract owner, enabling the creation of new tokens and distribution to specified addresses.

### Burning

Token holders can burn their own tokens using the `burnTokens` function. This feature is useful for reducing the total supply of tokens.

### Transfers and Ownership

The contract includes custom transfer functions, enabling the owner to transfer tokens to other addresses and increase/decrease token allowances for approved addresses. Ownership of the contract is managed through OpenZeppelin's Ownable contract, ensuring that only the owner can perform certain critical functions.

## Getting Started

To deploy and interact with this token contract, follow these steps:

1. Deploy the contract to an Ethereum-compatible blockchain using tools like Remix, Truffle, or Hardhat.
2. During deployment, provide the initial token name, symbol, and supply.
3. The contract owner can mint additional tokens using the `mintTokens` function.
4. Token holders can burn their own tokens using the `burnTokens` function.
5. The contract owner can transfer tokens to other addresses using the `transferFromOwner` function.
6. Adjust token allowances using the `increaseAllowance` and `decreaseAllowance` functions.

## Development Environment

Make sure you have the necessary tools installed for Solidity development:

- Solidity Compiler
- Ethereum Development Environment (Remix, Truffle, or Hardhat)
- Wallet for deploying and interacting with the contract (MetaMask, etc.)

## Testing

Test the contract thoroughly before deployment to ensure its functionality and security. Use automated testing tools and frameworks like Truffle or Hardhat, and consider writing unit tests for critical functions.

## License

This code is licensed under the MIT License. See the `LICENSE` file for details.
