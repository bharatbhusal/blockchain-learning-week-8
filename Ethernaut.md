# Game 0:
Its not actually the game. It gave me a guide for further actaul games. It was a introductory round. 


# Game 1(Fallback):
In my approach to interacting with the `Fallback` smart contract, I first executed the `contribute` function by using `await contract.contribute({ value: 1 });`. This action involved contributing 1 wei to the contract, incrementing my contribution balance, and potentially updating the owner if my contribution surpassed the current owner's.

Next, I attempted to use the `sendTransaction` function with `await sendTransaction({ to: "game address", value: 1, from: "my address" });`. This made me the new owner of the contract because I have more contribution than previous owner. 

Finally, I executed the `withdraw` function through `await contract.withdraw();`, which successfully transferred the entire contract balance to me as the owner. The `onlyOwner` modifier ensured that only I, as the owner, could trigger this function, preventing unauthorized withdrawals.


# Game 2:
In my interaction with the Fallout smart contract, I initiated by executing the Fal1out function: `await contract.Fal1out({value: 1});`. Despite the unconventional naming for the constructor, it seems to be an initialization function, setting the contract owner to the sender (msg.sender), which, in this case, is me. This action also allocated an initial value to the owner's address.