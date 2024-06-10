# Solidity-Beginner---Create-a-Token

#Code Explanation

Features:

      a. Token Details: Public variables for token name, abbreviation, and total supply.

      b. Minting: Functionality to mint new tokens and increase the total supply.

      c. Burning: Functionality to burn tokens and decrease the total supply.

      d. Balance Tracking: Mapping to keep track of balances for each address.

1. SPDX-License-Identifier:MIT :-This line specifies the license under which the contract is published. In this case, it’s the MIT license.

2. pragma solidity 0.8.18 :- This line indicates that the source code is written for Solidity version 0.8.18.
   
3. contract CustomToken {

      This line begins the definition of the CustomToken contract.

5. string public tokenName;

   string public tokenAbbreviation;

   uint public totalSupply;

         These lines declare three public state variables:

         a. tokenName: Stores the name of the token.

         b. tokenAbbreviation: Stores the abbreviation (symbol) of the token.

         c. totalSupply: Stores the total supply of the token.


5. mapping(address => uint) public balances :- This line declares a mapping called balances that links an address to the number of tokens held by that address.

6. constructor(string memory _name, string memory _Abbreviation, uint _initialSupply) {

        tokenName = _name;
   
        tokenAbbreviation = _Abbreviation;
   
        totalSupply = _initialSupply;
   
        balances[msg.sender] = _initialSupply;
   
    }

                  The constructor is a special function that runs once when the contract is deployed. It initializes the token's details:

                  a. tokenName: Sets the token's name to _name.

                  b. tokenAbbreviation: Sets the token's abbreviation to _Abbreviation: 

                  c. totalSupply: Sets the initial total supply to _initialSupply.

                  d. balances[msg.sender]: Assigns the entire initial supply to the address that deploys the contract (msg.sender).

7.  function mint(address _address, uint _value) public {         
        totalSupply += _value;
        balances[_address] += _value;
    }

 This function creates new tokens and assigns them to a specified address.
   Parameters:
    .  _address: The address to which new tokens will be assigned.
    .  _value: The number of tokens to mint.
   Functionality:
    a.  totalSupply += _value;: Increases the total supply by the specified amount.
    b.  balances[_address] += _value;: Increases the balance of the specified address by the same amount.

8. function burn(address _from, uint _value) public {                     
        require(balances[_from] >= _value, "Too little balance to burn");
        totalSupply -= _value;
        balances[_from] -= _value;
    }
 The burn function allows us to destroy tokens:
   Parameters:
     .  _from: The address from which tokens will be burned.
     .  _value: The number of tokens to burn.
   Functionality:
    a.   require(balances[_from] >= _value, "Too little balance to burn");: Ensures the address has enough tokens to burn. If not, it reverts the transaction with 
        an error message.
    b.   totalSupply -= _value;: Decreases the total supply by the specified amount.
    c.   balances[_from] -= _value;: Decreases the balance of the specified address by the same amount.
   
   


