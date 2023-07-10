# Contract Creation

This Solidity program describes the functionality of a contract. The purpose of this program is to demonstrate the working of public variables, mapping , conditionals and functions, also how to mint and burn tokens. 


## Description

The program represents a simple ERC-20 token contract called "MyToken." The contract allows for the creation, transfer, and destruction of tokens. The contract is defined using the contract keyword followed by the contract name (MyToken). The contract declares three public variables:
TokenName: A string representing the name of the token, set to "B Devi."
TokenAbbrv: A string representing the abbreviation or symbol of the token, set to "Devi."
totalSupply: An unsigned integer representing the total supply of tokens, initially set to 0.

The contract defines a mapping called balances that associates addresses with their respective token balances. The mapping is public, allowing external access to balance information.
The mint function is used to create new tokens and assign them to a specified address. It takes two parameters: _address (the address to mint tokens for) and _value (the number of tokens to create). The function increases the total supply by the given value and adds the minted tokens to the balance of the specified address.
The burn function is used to destroy tokens held by a specified address. It takes two parameters: _address (the address to burn tokens from) and _value (the number of tokens to burn). The function checks if the address has enough tokens to burn, and if so, it decreases the total supply and reduces the balance of the address accordingly.

Overall, this contract allows for the creation of tokens through the mint function and the destruction of tokens through the burn function. The token balances of addresses are stored in the balances mapping, and the total supply of tokens is tracked by the totalSupply variable.


## Getting Started

### Executing program

To run this program, you can use Remix, an online Solidity IDE. To get started, go to the Remix website at https://remix.ethereum.org/.

Once you are on the Remix website, create a new file by clicking on the "+" icon in the left-hand sidebar. Save the file with a .sol extension (e.g., HelloWorld.sol). Copy and paste the following code into the file:

```javascript

// SPDX-License-Identifier: MIT
pragma solidity 0.8.18;

contract MyToken {

    // public variables here
string public TokenName="B Devi";
string public TokenAbbrv="Devi";
uint public totalSupply=0;

    // mapping variable here
mapping(address => uint)public balances;
   
    // mint function
    function mint (address _address, uint _value) public{
        totalSupply+=_value;
        balances[_address]+=_value;
    }

    // burn function

    function burn (address _address, uint _value) public{
        if (balances[_address]>= _value){
        totalSupply -=_value;
        balances[_address] -=_value;
    }
    }}
```
To compile the code, click on the "Solidity Compiler" tab in the left-hand sidebar. Make sure the "Compiler" option is set to "0.8.4" (or another compatible version), and then click on the "Compile HelloWorld.sol" button.

Once the code is compiled, you can deploy the contract by clicking on the "Deploy & Run Transactions" tab in the left-hand sidebar. Select the "HelloWorld" contract from the dropdown menu, and then click on the "Deploy" button.

 After that click on deployed contracts , thereafter add the address as well as amount from the above inside mint contract button , check the balance and total supply. Then go to burn option ,add the same address and amount to be burnt and check the balance.At the end also check the condition by burning amount greater than the balance.
## Authors

Contributors names and contact info

 [B Devi](devibattini@gmail.com)



## License

This project is licensed under the MIT License License - see the LICENSE.md file for details
