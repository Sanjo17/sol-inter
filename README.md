# WAAW Token Contract

This Solidity contract defines a basic ERC20-like token named WAAW. It allows minting and burning tokens while maintaining balances and the total token supply.

## Contract Overview

### Contract Variables

- **`name`**: Represents the name of the token.
- **`abbrv`**: Represents the abbreviation of the token.
- **`supply`**: Tracks the total token supply.

### Functions

- **`mint(address _address, uint _value)`**: Mint new tokens and assign them to the specified address.
- **`burn(address _address, uint _value)`**: Burn tokens from the specified address.

### Usage

#### Mint Function

To create new tokens and assign them to an address, call the `mint` function with the target address and the value to mint.

```solidity
function mint(address _address, uint _value) public {
    // Example usage:
    // mint(address_to_receive_tokens, amount_to_mint);
    // mint(0xAddress, 100);
}
```

#### Burn Function

To burn tokens from a specific address, call the `burn` function with the target address and the amount to burn.

```solidity
function burn(address _address, uint _value) public {
    // Example usage:
    // burn(address_with_tokens, amount_to_burn);
    // burn(0xAddress, 50);
}
```

### Error Handling

- The `burn` function reverts with the message "Insufficient balance to burn" if the balance of the specified address is insufficient to perform the burn.

### Important Notes
- `assert` statements are used to ensure integrity but might cause immediate transaction revert if they fail.



---

