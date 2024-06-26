# Steven

Hi, my name is Steven, studying and working in data. Looking forward to learning a lot from https://epf.wiki/#/ and meet new amazing people. 
X/tele/ig: @im24steven

## Notes

### 04/05

Referencing: https://epf.wiki/#/wiki/protocol/data-structures?id=data-structures-in-ethereum 

#### Data Structures in ETH

(Delving into the data structures of eth for a better understanding of building relational databases for eth transactions.)

1. Merkle Patricia Trie as the primary data structure for storing the execution layer state. PT: all data is stored in the leaf nodes. Space efficient.

	3 types of nodes in ETH MPT:
	
	- Branch Nodes: 1 node value + 16 branches = 17-element array. 
	- Extension Nodes: optimized, compressed, eliminating redundant branch nodes with single children.
	- Leaf Nodes: key-value pairs. Value = node content; Key = node hash.

![MPT](https://github.com/WildcatsC/eth-projects/blob/main/assets-pics/ETH-MPT.jpg)
(The root is also an extension node)

2. Within one ETH block, 4 different modified MPTs:

 	- Transaction Trie: Nonce, from, to, value, etc.
	- Receipt Trie : logs, status code, etc.
	- World State Trie: nonce, balance, storageRoot, etc.
	- Account State(Storage) Trie, storageRoot

([Visualization](https://epf.wiki/#/wiki/protocol/data-structures))

Insight: 1. Efficient data retrieval in MPT. 2. translating MPT into relational schemas, different parts of the Merkle tree can be stored in different tables. For building/saving historical data as relational databases using schemas with certain normalization levels, tables can be stored separately--nodes table, accounts state table, transactions table, etc. 

3. TODO: On Merkle Trees in ETH and ZKP: how ZKP project tables could be generated?

	



