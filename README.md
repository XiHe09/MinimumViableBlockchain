# MinimumViableBlockchain
To run the program, do:
python3 driver.py

Each node has a 3 in 10 chance of generating and broadcasting an invalid block.
Invalid reasons for blocks include bad pow, bad nonce, and missing field.

There are 5 set invalid transactions in the generate_transaction function that
generates 5 invalid transaction for various reasons.
Invalid reasons for transactions include missing field, double spending, 
duplicate transactions, overspending (value mismatch), and bad number.
Valid transactions are generated with random valid values between randomly selected
coin "users".

Each node keeps track of all known equal size longest blockchains, and discard them
if a longer blockchain is formed or received.
Each time a node generates a block, it will broadcast it to all nodes including
itself.
Then, the node will append it to his own chain and broadcast the updated chain 
to every nodes too.

See code and comments for more detail.
