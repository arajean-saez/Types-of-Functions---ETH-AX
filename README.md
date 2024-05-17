# Types-of-Functions-ETH-AVAX

# Description 

AraToken is a Solidity smart contract that implements an ERC20 token. It extends the functionality of the ERC20 standard token by providing additional functions such as minting, burning, and transfer and transferFrom.

# Getting Started
To run this program, you can use Remix, an online Solidity IDE. To get started, go to the Remix website at https://remix.ethereum.org/.

Once you are on the Remix website, create a new file by clicking on the "+" icon in the left-hand sidebar. Save the file with a .sol extension (e.g., AraToken.sol). Copy and paste the following code into the file:

# Code Explaination 
mint(): This function is used to create new tokens and add them to a specified address. If the caller is the admin, the mint function from the ERC20 contract is called, which increases the total supply of tokens and adds the specified amount to the balance of the to address.

burn(): This function allows a user to destroy (burn) a specified amount of their own tokens. The burn function from the ERC20 contract is called, which reduces the total supply of tokens and subtracts the specified amount from the balance of msg.sender (the caller).

transfer(): This function enables a user to transfer a specified amount of tokens from their own address to another address. The transfer function from the ERC20 contract is overridden here, but it simply calls the parent ERC20 contract’s transfer function using super.transfer(to, amount). This ensures that the token transfer follows the standard ERC20 transfer mechanism, which includes checks like ensuring the sender has enough balance and updating the balances of both the sender and the recipient.

transferFrom(): This function allows a user to transfer tokens from another address to a specified address, given that they have been approved to do so. The transferFrom function from the ERC20 contract is overridden here, but it simply calls the parent ERC20 contract’s transferFrom function using super.transferFrom(from, to, amount). 
