# WeaponToken 

## Overview

WeaponToken is a decentralized ERC-20 token on the Ethereum blockchain that represents in-game weapons. This smart contract allows users to mint, burn, transfer tokens, and redeem weapons based on their token balance. Each weapon has an associated cost in tokens, and users can exchange their tokens for specific weapons.

## Features

### ERC-20 Standard

WeaponToken is an ERC-20 compliant token, inheriting from the OpenZeppelin ERC-20 implementation. This ensures compatibility with various decentralized applications (DApps), wallets, and exchanges.

### Ownership

The contract includes the Ownable.sol library, allowing the owner to perform administrative tasks such as minting new tokens, adding new weapons, and modifying weapon costs.

### Minting and Burning

The owner can mint new WeaponToken tokens and users can burn their tokens if they choose to do so. This functionality is implemented to manage the token supply and provide flexibility for users.

### Weapon Redemption

Users can redeem in-game weapons by burning a specified amount of WeaponToken tokens. The cost of each weapon is predefined by the contract owner. Upon successful redemption, the user's selected weapon is recorded, and an event is emitted.

### Custom Weapons

The contract allows the owner to add custom weapons (beyond the initial four) with associated costs. Users can then redeem these custom weapons by burning the required tokens.

## Deployment

The contract is deployed on the Ethereum blockchain and is identified by the name "WeaponToken" and the symbol "WTK." The contract owner initially sets up the costs of four default weapons: "Wooden Sword," "Iron Dagger," "Bronze Axe," and "Steel Bow."

## Functions

1. **Minting:**
   - Function: `mint(address to, uint256 count)`
   - Access: Owner only
   - Description: Mint a specified number of tokens and assign them to the given address.

2. **Burning:**
   - Function: `burn(uint256 count)`
   - Access: Any user
   - Description: Burn a specified number of tokens from the caller's balance.

3. **Weapon Redemption:**
   - Function: `redeemWeapon(uint8 weaponNumber)`
   - Access: Any user
   - Description: Redeem a weapon by burning the required tokens. The chosen weapon is recorded.

4. **Token Transfer:**
   - Function: `transfer_Func(address recipient, uint256 count)`
   - Access: Any user
   - Description: Transfer tokens from the caller's balance to the specified recipient.

5. **Add Weapon:**
   - Function: `addWeapon(uint8 weaponNumber, uint256 weaponCost)`
   - Access: Owner only
   - Description: Add a new weapon with a specified number and associated cost.

6. **Claim Custom Weapon:**
   - Function: `claimCustomWeapon(uint8 weaponNumber)`
   - Access: Any user
   - Description: Redeem a custom weapon (beyond the initial four) by burning the required tokens.

## Events

1. `WeaponRedeemed(address indexed account, uint8 weapon, uint256 weaponCost)`
   - Triggered when a user successfully redeems a weapon.

2. `WeaponAdded(uint8 weaponNumber, uint256 weaponCost)`
   - Triggered when the owner adds a new weapon.


## Author
mohammed faiz

mohammedfaiz866@gmail.com

