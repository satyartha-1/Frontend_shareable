# Frontend_shareable

Instead of a traditional backend, our backend is a smart contract on the ethereum network. We can read from and write to the chain using smart contract methods (or functions) defined by us.

The activities we need to perform from the front-end are as follows:

1. Take input from user and pass it as argument into smart contract function. 
2. Call smart contract methods to retrieve data from chain 
3. Write to the chain

To connect our frontend to the chain, we need to do the following: 
1. Initialize Web3
2. Initialize our smart contract object (need ABI and contract address for that)
3. Load an instance of the smart contract object

Web3 is a js library to allow our frontend to talk to the smart contract using JS. Under the hood it converts our JS to JSON (which is used to interact with a contract on the node)
ABI is application binary interface. It is a JSON artifact generated during the compilation of our
contract. Think of it as the representation of a contract and its methods so that our JS can talk to it.

Now as the basics are out of the way, lets look at what we want.

Following are the methods we need to call:
1. CreateCert
2. GetHashByIndex

CreateCert takes the following inputs from user and passes them into the function to create a new certificate:
1. Name ( string, text)
2. GPA (string, text)
3. Passing year (uint 256, number)
4. Institute name (string, text)

In brackets, the data type in solidity and js is given respectively.
The js code i have written is getting some error while trying to pass values. The issue has something to do with the inability of js to deal with big numbers.
The error is included in the repository as error.txt
