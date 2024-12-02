# MyToken

A simple Solidity smart contract demonstrating basic token functionality with minting and burning capabilities.

## Description

MyToken is an Ethereum blockchain smart contract that implements a basic token system. The contract allows for creating tokens, tracking total supply, and managing token balances across different addresses. Key features include:

- Public token metadata (name, abbreviation)
- Token supply tracking
- Mint function to create new tokens
- Burn function to destroy existing tokens
- Balance tracking per address

## Getting Started

### Prerequisites

- Solidity compiler (v0.8.26 or compatible)
- Ethereum development environment (Hardhat, Truffle, or Remix)

### Deploying the Contract

1. Compile the contract using a Solidity compiler
2. Deploy to an Ethereum network (mainnet, testnet, or local blockchain)

### Interacting with the Contract

```solidity
// Mint tokens (increases total supply)
function mint(address _to, uint _amount) public {
    totalSupply += _amount;
    balances[_to] += _amount;
}

// Burn tokens (decreases total supply)
function burn(address _from, uint _amount) public {
    require(balances[_from] >= _amount, "Insufficient balance");
    totalSupply -= _amount;
    balances[_from] -= _amount;
}
```

## Contract Details

- **Token Name**: Big K
- **Token Abbreviation**: BIK
- **Initial Total Supply**: 0

## Security Considerations

- Burn function includes balance validation
- Only addresses with sufficient balance can burn tokens

## Authors

- Anonymous Developer

## License

This project is licensed under the MIT License - see the LICENSE file for details.
