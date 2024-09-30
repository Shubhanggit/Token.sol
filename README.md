

# MyToken Solidity Smart Contract

This Solidity program is a simple token contract that demonstrates basic token functionality such as minting and burning tokens. The purpose of this program is to serve as a foundational example for those who are learning how to create custom tokens on the Ethereum blockchain.

## Description

This program defines a smart contract written in Solidity, a programming language used to develop smart contracts on the Ethereum blockchain. The contract provides functionality to mint new tokens, burn existing tokens, and track token balances. The `mint` function allows the creation of new tokens for a specific address, while the `burn` function destroys tokens from a specified address. The contract also keeps track of the total supply of tokens and provides a public mapping to check the balances of different addresses.

This program serves as a straightforward introduction to token development and can be used as a base for more advanced token contracts in the future.

## Getting Started

### Executing Program

To run this program, you can use Remix, an online Solidity IDE. To get started, go to the Remix website at [Remix](https://remix.ethereum.org/).

1. Once you are on the Remix website, create a new file by clicking on the "+" icon in the left-hand sidebar. Save the file with a `.sol` extension (e.g., `MyToken.sol`). Copy and paste the following code into the file:

   ```solidity
   // SPDX-License-Identifier: MIT
   pragma solidity 0.8.18;

   contract MyToken {
       string public tokenName = "HELLO";
       string public tokenAbbrv = "HE";
       uint256 public totalSupply;

       mapping(address => uint256) public balances;

       function mint(address _to, uint256 _value) public {
           require(_to != address(0), "Cannot mint to the zero address");
           totalSupply += _value;
           balances[_to] += _value;
       }

       function burn(address _from, uint256 _value) public {
           require(_from != address(0), "Cannot burn from the zero address");
           require(balances[_from] >= _value, "Insufficient balance to burn");
           totalSupply -= _value;
           balances[_from] -= _value;
       }
   }
   ```

2. To compile the code, click on the "Solidity Compiler" tab in the left-hand sidebar. Ensure the "Compiler" option is set to "0.8.18" (or another compatible version), and then click on the "Compile MyToken.sol" button.

3. Once the code is compiled, you can deploy the contract by clicking on the "Deploy & Run Transactions" tab in the left-hand sidebar. Select the `MyToken` contract from the dropdown menu, and then click on the "Deploy" button.

4. After the contract is deployed, you can interact with it by calling the `mint` and `burn` functions. Use the input fields to specify the address and token amount, and then click "transact" to mint or burn tokens. You can also check balances by calling the `balances` function with an address.

## Authors

Metacrafter Chris  
[@metacraftersio](https://github.com/metacraftersio)

## License

This project is licensed under the MIT License - see the LICENSE.md file for details.

