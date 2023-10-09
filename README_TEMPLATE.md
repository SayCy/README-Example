# Creating a Token

A token is established on a blockchain in order to represent, share, and manage various digital assets or rights in a distributed, secure, and open manner. This makes a variety of applications across sectors possible.

## Description

Making tokens on a blockchain means making a digital item with a name, a short name, and a total amount. To make and give out these items, you need a special function, and to get rid of them, you need another special function. It's crucial that the second function checks if there are enough items to get rid of so that we don't mess up the total number of items.

## Getting Started

### Executing program

To run this program, you can use Remix, an online Solidity IDE. To get started, go to the Remix website at https://remix.ethereum.org/.

After you've arrived at the Remix website, start by making a fresh file. You can do this by tapping on the "+" symbol found on the left side of the screen. Make sure to save this file with a .sol extension, like "HelloWorld.sol." Below, you'll find a sample of my token's code:


```
// SPDX-License-Identifier: MIT
pragma solidity 0.8.18;

contract MyToken {

    // public variables here
string public tokenName = "CYRILL";
string public tokenAbbrv = "CY";
uint public totalSupply = 0;

    // mapping variable here
mapping(address => uint) public balances;

    // mint function
function mint (address token_address, uint token_value) public{
    totalSupply += token_value;
    balances[token_address] += token_value;
}

    // burn function
function burn (address token_address, uint token_value) public{
    if (balances[token_address] >= token_value){
        totalSupply -= token_value;
        balances[token_address] -= token_value;
        }
    }
}
```

## Authors



Cyrill James G. Dela Cruz
202010525@fit.edu.ph


