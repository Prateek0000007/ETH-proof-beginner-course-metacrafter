# ETH-proof-beginner-course-metacrafter
Public Variables: The contract stores details about the token such as the token name, abbreviation, and total supply.
Mapping of Balances: The contract maintains a mapping of addresses to balances.
Mint Function: This function increases the total supply and the balance of a specified address.
Burn Function: This function decreases the total supply and the balance of a specified address, ensuring that the balance is sufficient to burn the specified amount.

Public Variables
tokenName: The name of the token.
tokenAbbrv: The abbreviation of the token.
totalSupply: The total supply of the token.

Mapping
balances: A mapping of addresses to their respective token balances.

Functions
mint
This function allows the creation of new tokens.
Parameters:
sender: The address to which the tokens will be minted.
value: The number of tokens to mint.
Behavior:
Increases the total supply by value.
Increases the balance of sender by value.

burn
This function allows the destruction of tokens.
Parameters:
sender: The address from which the tokens will be burned.
value: The number of tokens to burn.
Behavior:
Decreases the total supply by value.
Decreases the balance of sender by value, provided that sender has a balance greater than or equal to value


Deploy the Contract: Deploy the contract on a compatible Ethereum network.
Mint Tokens: Call the mint function with the address to receive tokens and the amount to mint.
Burn Tokens: Call the burn function with the address from which to burn tokens and the amount to burn. Ensure the address has sufficient balance.
