

# MyToken Smart Contract

A simple token contract that demonstrates how to mint and burn tokens on the Ethereum blockchain. It allows you to create tokens, destroy them, and track balances.

## Description

This project is a basic token contract written in Solidity for managing token supply through minting and burning operations. It features the ability to create new tokens (`mint` function) for a specific address, burn existing tokens (`burn` function) from a specific address, and maintain the total supply. This contract can serve as the foundation for more complex token-related applications on the Ethereum network, including fungible token development.

## Getting Started

### Installing

To interact with the smart contract, you'll need to use an Ethereum development environment like Remix. Follow the steps below:

1. Go to the [Remix IDE](https://remix.ethereum.org/).
2. Create a new file and save it as `MyToken.sol`.
3. Copy and paste the contract code into the file.

### Executing Program

Once the contract is created and set up, follow these steps to run and deploy it:

1. **Compile the contract**:
   - In Remix, go to the "Solidity Compiler" tab.
   - Set the compiler version to `0.8.18` (or another compatible version).
   - Click the "Compile MyToken.sol" button.

2. **Deploy the contract**:
   - Go to the "Deploy & Run Transactions" tab.
   - Select the `MyToken` contract from the dropdown menu.
   - Click the "Deploy" button to deploy the contract to a local blockchain (using Remix VM or connected wallet like MetaMask).

3. **Interact with the contract**:
   - Use the `mint` function to create new tokens by specifying the address and token amount.
   - Use the `burn` function to destroy tokens from a specific address.
   - Use the `balances` mapping to check the balance of any address.
  
Example commands in Remix interface:

```solidity
mint("0xYourAddress", 100)
burn("0xYourAddress", 50)
```

### Help

If you encounter issues with deployment or interaction:

- Ensure the Ethereum wallet or VM you're using is properly configured.
- Double-check the addresses used for minting and burning to avoid zero address errors.
- Make sure the balance being burned is sufficient to avoid insufficient balance errors.

For debugging help, try the following command in Remix's console for more detailed output:

```solidity
debug
```


## License

This project is licensed under the MIT License - see the LICENSE file for details.
