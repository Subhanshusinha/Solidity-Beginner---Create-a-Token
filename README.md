# Project - Custom Token 

Custom Token is a simple Solidity smart contract for creating custom tokens on the Ethereum blockchain.

## Description

The Custom Token Project is a Solidity smart contract that allows you to create and manage your own custom ERC-20 token. This contract provides functionality for minting new tokens, burning existing tokens, and tracking the total supply and individual balances of token holders.

## Getting Started

### Installing

1. Solidity compiler version 0.8.18 or higher
2. Copy the provided Solidity code into a new file named `CustomToken.sol`.

### Executing program

To deploy and interact with the Custom Token contract:

1. Compile the `CustomToken.sol` file:

   Use Remix IDE or another development environment to compile the Solidity file.

2. Deploy the contract:
   
   Provide the required parameters during deployment:
  - `name`: The name of your custom token (e.g., "Karan").
  - `abbreviation`: The abbreviation or symbol for your token (e.g., "MIT").
  - `initialSupply`: The initial total supply of tokens to be minted.

Example deployment in Solidity:
    CustomToken myToken = new CustomToken("Karan", "MIT", 1000);

3. Once deployed, Interact with the contract using its public functions:

  - `mint(address _address, uint _amount)`: Mint new tokens and assign them to a specific address.
` - `burn(address _from, uint _amount)`: Burn or destroy tokens from a specific address.
  ` `balances(address _address)`: View the token balance of a specific address.
  - `totalSupply()`: View the total supply of tokens.
## Help

If you encounter any issues or have questions, feel free to reach out to the contributors.

## Authors

  - Subhanshu sinha and - subhanshu.sinha667@gmail.com 

## License

This project is licensed under the MIT License - see the LICENSE file for details.

