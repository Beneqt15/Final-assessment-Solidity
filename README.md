# MyToken - Final-assessment-Solidity

This Solidity program is a  program that demonstrates the basic syntax and functionality of the Solidity programming language. The purpose of this program is to serve as a starting point for those who are new to Solidity and want to get a feel for how it works.

## Description

The Solidity program contract "MyToken" is a simple smart contract for creating a cryptocurrency token on the Ethereum blockchain. It has two public string variables for the token name and abbreviation, and a public uint variable to track the total supply of tokens. The contract uses a mapping to store the balance of tokens for each address that holds them. The contract also includes two functions: "mint" for creating new tokens and assigning them to an address, and "burn" for removing tokens from an address. This contract provides a basic framework for managing a token on the Ethereum blockchain.

## Getting Started

### Executing program

To run this program, you can use Remix, an online Solidity IDE. To get started, go to the Remix website at https://remix.ethereum.org/.

Once you are on the Remix website, create a new file by clicking on the "+" icon in the left-hand sidebar. Save the file with a .sol extension (e.g., HelloWorld.sol). Copy and paste the following code into the file:
contract MyToken {

    // public variables here
    string public tokenName = "Benedict Miguel";
    string public tokenAbbrv = "BM";
    uint public totalSupply = 0;

    // mapping variable here
    mapping(address => uint) public balances;

    // mint function
    function mint (address _address, uint _value) public{
        totalSupply += _value;
        balances [_address] += _value;
    }

    // burn function
    function burn (address _address, uint _value) public{
        if (balances[_address] >=_value) {

        totalSupply -= _value;
        balances [_address] -= _value;
    }

}
}


To compile the code, click on the "Solidity Compiler" tab in the left-hand sidebar. Make sure the "Compiler" option is set to "0.8.4" (or another compatible version), and then click on the "Compile token-maglente.sol" button.

Once the code is compiled, you can deploy the contract by clicking on the "Deploy & Run Transactions" tab in the left-hand sidebar. After that you can now see the Token Name, Token Abbrv., Total Supply) and you can now mint and burn the tokens

## Authors

Benedict Miguel Maglente


## License

This project is licensed under the MIT License - see the LICENSE.md file for details.
