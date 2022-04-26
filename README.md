# CSE1007-JAVA Digital Assignment
## Ujjwal Agarwal 20BCI0102

### Merkle/Hash Tree
Used for Data Verification and Synchronisation, in this every NON-leaf node is a hash of it's child nodes.
While all the leaf nodes are at the same depth and are as far left as possible.
It is usually implemented as Binary Tree but can have more children is needed.

The hashing is for maintaning data integrity.

## Architecture
In a Merkle Tree, the top node/hash is a hash of the entire tree. Similarly, all parent nodes are hashes of nodes below them.

This kind of a structure helps in efficient mapping of large data and is also great to validate integrity.
To check for integrity, we just have to check if root hash is consistent to find if the data of the entire tree is consistent. Hence is saves computation time by a lot.

A node for a merkle tree is basically the same as a normal binary tree.
We have a left pointer and a right pointer and we also use a key and the value field.

## Algorithm

### Addition
S1: We will take key and value as parameters.

S2: Take the hash(key) and store it in a variable called index.

S3: store arr[index].head in a pointer called tree of datatype node.

S4: create a new node with its key as key and value as value and both links as null.

S5: If the tree is null then assign the new node to the head and increment the size by 1.

S6: If the tree is not null then we will check if the key is already present in the tree using the find function.

S7: If the key is already present in the tree then we will update the value.

S8: If it is not present in the tree then we will use the insert function to insert the element.

### Insertion
S1: It will take tree and item pointers of node data type as parameters.

S2: If item->key is smaller than tree->key and tree->left is null then assign the item to tree->left.

S3: If item->key is smaller than tree->key and tree->left is not null then call insert function with tree->left and item as parameters.

S4: If item->key is greater than tree->key and tree->right is null then assign the item to tree->right.

S5: If item->key is greater than tree->key and tree->right is not null then call insert function with tree->right and item as parameters.


### Deletion
S1: We will take a key as a parameter.

S2: Take the hash(key) and store it in a variable called index.

S3: arr[index].head in a pointer called tree of datatype node.

S4: If the tree is null then the key is not present.

S5: If the tree is not null then we will check if the key is already present in the tree using the find function.

S6: If the find function returns null then the key is not present in the tree.

S7: If it is not null then we will use the remove function to delete the element.










