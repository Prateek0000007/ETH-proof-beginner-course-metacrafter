MyToken Contract:
This Solidity program is a simple smart contract for creating and managing a custom token on the Ethereum blockchain. The purpose of this program is to demonstrate the basic functionalities of minting and burning tokens, as well as managing token balances for different addresses.

Description:
This program is a smart contract written in Solidity, designed to create and manage a custom token named "Prateek" with the abbreviation "PS". It includes functionalities for minting new tokens, burning existing tokens, and maintaining the total supply and balances of tokens for different addresses. This contract serves as an introductory example for those new to Solidity and blockchain development.

Getting Started:
Executing Program:
To run this program, you can use Remix, an online Solidity IDE. To get started, go to the Remix website at https://remix.ethereum.org/.

Once you are on the Remix website, create a new file by clicking on the "+" icon in the left-hand sidebar. Save the file with a .sol extension (e.g., MyToken.sol). Copy and paste the following code into the file:

solidity
Copy code
// SPDX-License-Identifier: MIT
pragma solidity ^0.8.18;

contract MyToken {

    // public variables here
    string public tokenName = "Prateek";
    string public tokenAbbrv = "PS";
    uint public totalSupply = 0;

    // mapping variable here
    mapping(address => uint) public balances;

    // mint function
    function mint(address sender, uint value) public {
        totalSupply += value;
        balances[sender] += value;
    }

    // burn function
    function burn(address sender, uint value) public {
        if(balances[sender] >= value) {
            totalSupply -= value;
            balances[sender] -= value;
        }
    }
}
To compile the code, click on the "Solidity Compiler" tab in the left-hand sidebar. Make sure the "Compiler" option is set to "0.8.18" (or another compatible version), and then click on the "Compile MyToken.sol" button.

Once the code is compiled, you can deploy the contract by clicking on the "Deploy & Run Transactions" tab in the left-hand sidebar. Select the "MyToken" contract from the dropdown menu, and then click on the "Deploy" button.

Interacting with the Contract
Once the contract is deployed, you can interact with it by calling its functions. Here's how to use the mint and burn functions:

Mint Tokens:

Click on the "MyToken" contract in the left-hand sidebar.
Click on the "mint" function.
Enter the address to which you want to mint tokens and the number of tokens to mint.
Click on the "transact" button to execute the function and mint the tokens.

Burn Tokens:

Click on the "MyToken" contract in the left-hand sidebar.
Click on the "burn" function.
Enter the address from which you want to burn tokens and the number of tokens to burn.
Click on the "transact" button to execute the function and burn the tokens.

Authors:
Prateek saini
[prateek6398@gmail.com]
[22bcs12410@cuchd.in]

License:
This project is licensed under the MIT License - see the LICENSE.md file for details.






