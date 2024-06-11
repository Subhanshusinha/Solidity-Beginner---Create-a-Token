# Project - Custom Token 

Custom Token is a simple Solidity smart contract for creating custom tokens on the Ethereum blockchain.

## Description

The Custom Token Project is a Solidity smart contract that allows you to create and manage your own custom ERC-20 token. This contract provides functionality for minting new tokens, burning existing tokens, and tracking the total supply and individual balances of token holders.

## Getting Started

### Installing

1. Make sure you have a compatible Solidity compiler installed (version 0.8.18 or higher).
2. Copy the provided Solidity code into a new file (e.g., `CustomToken.sol`).

### Executing program

To deploy and interact with the Custom Token contract, you will need to use a compatible Ethereum client or development environment, such as Remix IDE

1. Compile the `CustomToken.sol` file.
2. Deploy the contract, providing the required parameters:
  - `name`: The name of your custom token (e.g., "Karan").
  - `abbreviation`: The abbreviation or symbol for your token (e.g., "MIT").
  - `initialSupply`: The initial total supply of tokens to be minted.

```solidity```
//Example deployment
CustomToken myToken = new CustomToken("Karan", "MIT", 1000000);

### Once deployed, you can interact with the contract using its public functions:

1. `mint(address, uint)`: Mint new tokens and assign them to a specific address.
2. `burn(address, uint)`: Burn or destroy tokens from a specific address.
3. `balances(address)`: View the token balance of a specific address.
4. `totalSupply()`: View the total supply of tokens.

## Help

If you encounter any issues or have questions, feel free to reach out to the contributors.

## Authors

Contributors names and Email info

Subhanshu sinha and ( subhanshu.sinha667@gmail.com )

## License

This project is licensed under the MIT License - see the LICENSE file for details.

