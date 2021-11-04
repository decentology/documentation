---
description: Create your own cryptocurrency tokens and track or trade digital assets.
---

# 🔎 Asset and Value Tracking

## Custom Tokens

**Tokens are divisible and one unit is not uniquely different from another unit of the same token (like currency).**

| Type | **Function**       | **What it does**                                                                                         |
| ---- | ------------------ | -------------------------------------------------------------------------------------------------------- |
| GET  | **totalSupply()**  | Returns the total supply of tokens                                                                       |
| GET  | **balance()**      | Gets the balance of the calling address (current account)                                                |
| GET  | **balanceOf()**    | Gets the balance of a specific address                                                                   |
| GET  | **allowance()**    | Checks the amount of tokens that an owner allowed to a spender                                           |
| POST | **transfer()**     | Transfers token for a specified address                                                                  |
| POST | **transferFrom()** | Transfers tokens from one address to another                                                             |
| POST | **approve()**      | <p>Approves the passed address to spend the specified amount of tokens</p><p>on behalf of msg.sender</p> |

### totalSupply()

| `totalSupply()` returns the total supply of tokens |
| -------------------------------------------------- |
| **Syntax**                                         |
| `totalSupply()`                                    |
| **Parameters**                                     |
| None                                               |
| **Return value**                                   |
| `uint256` representing the total amount of tokens  |

### balance()

**Gets the balance of the calling address (current account)**

### balanceOf()

**Gets the balance of a specific address**

### transfer()

**Transfers tokens to a specified address (current account)**

### transferFrom()

**Transfers token from one address to another**

## **Collectibles**

{% hint style="info" %}
**Collectibles are uniquely different‒ each unit of a collectible is different from any other (like trading cards). This feature block is coming soon!**
{% endhint %}
