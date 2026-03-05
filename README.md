# ERC20AZ Token

A custom ERC20 token implementation built with Solidity, demonstrating the fundamental standards for creating fungible tokens on the Ethereum blockchain.

## What is This?

This is a fully functional ERC20 token called **ERC20AZ (ERC)** with:

- Initial supply distribution
- Token minting capability
- Transfer and approval mechanisms
- SafeMath library integration for secure arithmetic operations

## Why is This an ERC20 Token?

This token complies with the **ERC20 standard** - a set of rules that all fungible tokens on Ethereum must follow. It implements:

**Required Functions (6):**

- `totalSupply()` - Returns total token supply
- `balanceOf()` - Returns token balance of an address
- `transfer()` - Transfers tokens to another address
- `approve()` - Approves someone to spend your tokens
- `allowance()` - Checks approved spending amount
- `transferFrom()` - Transfers tokens on behalf of someone

**Required Events (2):**

- `Transfer` - Emitted when tokens move between addresses
- `Approval` - Emitted when spending approval is granted

**Optional Metadata:**

- `name` = "ERC20AZ"
- `symbol` = "ERC"
- `decimals` = 18

By following this standard, the token is compatible with all ERC20-supporting wallets, exchanges, and dApps (Uniswap, MetaMask, etc.).

## Tech Stack

- Solidity ^0.8.0
- SafeMath Library (arithmetic overflow protection)
- ERC20 Interface Standard

## Features

### Basic ERC20 Operations

```solidity
// Check total supply
totalSupply()

// Check your balance
balanceOf(address)

// Send tokens
transfer(recipient, amount)

// Approve someone to spend your tokens
approve(spender, amount)

// Transfer on behalf of someone (requires approval)
transferFrom(owner, recipient, amount)
```

### Additional Features

```solidity
// Mint new tokens (increase supply)
increaseTotalSupply(newTokensAmount)
```

## Token Details

| Property       | Value             |
| -------------- | ----------------- |
| Name           | ERC20AZ           |
| Symbol         | ERC               |
| Decimals       | 18                |
| Initial Supply | Set at deployment |
| Mintable       | Yes               |

## Security

- Uses SafeMath library to prevent integer overflow/underflow
- Proper balance and allowance checks before transfers
- Event emissions for transparency

## Deployment

```solidity
// Deploy with initial supply (e.g., 1,000,000 tokens)
constructor(1000000 * 10**18)
```

The deployer receives all initial tokens and can mint more using `increaseTotalSupply()`.

## Educational Note

This project demonstrates:

- How ERC20 standards enable interoperability
- Implementation of token transfer mechanisms
- Approval pattern for delegated transfers
- Safe arithmetic operations in Solidity

Just like ERC20 is the standard for fungible tokens, **ERC721** is the standard for NFTs (non-fungible tokens), each requiring compliance with their respective set of functions and events.
