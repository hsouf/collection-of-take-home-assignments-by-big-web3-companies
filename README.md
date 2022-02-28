# A Collection of take home assignments by big web3 companies (Solved)

In this repo I'll be sharing with you the most relevant challenges proposed as take home assignments for senior solidity/web3 engineers  by  big blockchain companies (Consensys included).


### 1_challenge: 

Write a simple CLI script, that when given a 64-byte string, it finds a suitable 4-byte prefix so that, a
SHA256 hash of the prefix combined with the original string of bytes, has two last bytes as 0xca, 0xfe.
Script should expect the original string to be passed in hexadecimal format and should return two lines,
first being the SHA256 string found and second 4-byte prefix used (in hexadecimal format).

For example:
````
./simple-pow
129df964b701d0b8e72fe7224cc71643cf8e000d122e72f742747708f5e3bb6294c619604e52dcd8f54
46da7e9ff7459d1d3cefbcc231dd4c02730a22af9880c
````
Should return
````
6681edd1d36af256c615bf6dcfcda03c282c3e0871bd75564458d77c529dcafe
00003997
````

### 2_challenge: (by Fluencytech.com)

Imagine you are a developer working on adding staking functionality to some ERC20 token. Some of
the work has already been done, but few methods are still missing and assigned to you to implement.
Please use repository https://github.com/wealthpal-ltd/dlt-recruitment/tree/master/tests/simple-pos
to download the smart contract from and fill in the missing code, to enable staking for that custom
ERC20 implementation.
Note #1: staking should allow any token holder to temporarily lock-in their funds in the contract by
calling method “stake”. To withdraw staked tokens, their owner should be able to use “unstake” method
to do so. To receive reward for staking, the method “reward” should be used. Annual interest rate is
hardcoded and set to 10%.
Note #2: fix all the bugs found as well.
Note #3: all interfaces used in the contract are the default ones taken from open source library
OpenZeppelin https://github.com/OpenZeppelin/openzeppelin-contracts-ethereum-package

### 3_challenge: Firewall Factory

Write a simple factory contract with built-in Firewall mechanism.
The factory should be ownable and provide a public function to deploy any custom contract when
provided with its bytecode.
On success - the custom contract should be deployed and its address returned.
On failure - an event indicating the problem should be thrown and NO contract should be created.
Additionally, the factory should have a built-in firewall that decides whether a contract is allowed to be
deployed or not. Firewall should work in a way that it is possible to whitelist contract deployment using
its bytecode. Factories should be able to deploy only whitelisted contracts, all other ones should be
rejected automatically as not allowed. Only a contract owner should be able to add to or remove from
whitelist, while everyone should be able to use factory for creation of whitelisted contracts.
### 4_challenge:Full Stack Web Challenge

Write a React web application using any of the well-known frameworks (Gatsby, Material UI,
etc.) that connects to either Energi or Ethereum blockchains using Web3 library, and displays
the latest:
- Block number
- Number of transactions
- Miner (address that mined the block)
- Total difficulty
- Add a button to pause or resume requests.

```
Extra: If you want to impress, add a table populated with all transactions sorted by amount in the
descending order.
``` 
