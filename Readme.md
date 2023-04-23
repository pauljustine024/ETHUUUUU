# Hello World

This "Hello World"-style Solidity application shows the fundamental syntax and features of the Solidity programming language. This program's goal is to provide as a jumping-off point for individuals who are unfamiliar with Solidity and wish to acquire a sense of how it operates.

## Description

This program is a simple contract written in Solidity, a programming language used for developing smart contracts on the Ethereum blockchain. The contract has a single function that returns the string "Hello World!". This program serves as a simple and straightforward introduction to Solidity programming, and can be used as a stepping stone for more complex projects in the future.

## Getting Started

### Executing program

To run this program, you can use Remix, an online Solidity IDE. To get started, go to the Remix website at https://remix.ethereum.org/.

Once you are on the Remix website, create a new file by clicking on the "+" icon in the left-hand sidebar. Save the file with a .sol extension (e.g., HelloWorld.sol). Copy and paste the following code into the file:

```solidity
// SPDX-License-Identifier: MIT
pragma solidity 0.8.18;

contract NTC {
    
    string public tokenName = "NTC Token";
    string public tokenSymbol = "NTC";
    uint public totalSupply = 0;
    
    mapping(address => uint) public balances;

    function mint(address _address, uint _value) public {
        totalSupply += _value;
        balances[_address] += _value;
    }

    function burn(address _address, uint _value) public {
        if (balances[_address] >= _value){
        }
        totalSupply -= _value;
        balances[_address] -= _value;
    }
}
```

To compile the code, click on the "Solidity Compiler" tab in the left-hand sidebar. Make sure the "Compiler" option is set to "0.8.4" (or another compatible version), and then click on the "Compile HelloWorld.sol" button.

Once the code is compiled, you can deploy the contract by clicking on the "Deploy & Run Transactions" tab in the left-hand sidebar. Select the "HelloWorld" contract from the dropdown menu, and then click on the "Deploy" button.

Once the contract is deployed, you can interact with it by calling the sayHello function. Click on the "HelloWorld" contract in the left-hand sidebar, and then click on the "sayHello" function. Finally, click on the "transact" button to execute the function and retrieve the "Hello World!" message.
Third is I created a mint function that take two parameters, the address which I
declared as address add, and the value that I declared as uint val. This function
will increase our total supply by that number and increases the balance of the
sender address by that amount.

Lastly, I added a burn function in which it works the opposite way of the mint.
Beacause instead of increasing, it will destroy tokens. I did this by using 
conditional statements to ensure that the balance of the sender is greater or 
equal to the amount that is supposed to be burned.

It will take an address and value just like the mint functions. 

It will then deduct the value from the total supply and from the balance of 
the “sender”.

So let`s try running the code.

first let's try minting. 

Alright our minting works as you can see in our supply our sender now has 
2000 tokens.

now for the burn function. So I'll be dedacting 1000 tokens. Alright I guess our 
burn function work, 1000 tokens has been deducted.

So yeah, I guess that's all for this video. Thank you for watching and I hope you
enjoyed this video.
## Authors

Metacrafter Chris  
[@metacraftersio](https://www.facebook.com/pauljustine.laycano.75)


## License

This project is licensed under the MIT License - see the LICENSE.md file for details
