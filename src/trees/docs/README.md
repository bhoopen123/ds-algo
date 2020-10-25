# Trees

## Introduction
Before we jump into trees, let us first see what all types of Linear data structure are present.

 1 - Array

 2 - Linked List

 3 - Stack 

 4 - Queues

All of these data structures are basically collection of different kinds in which data is arranged in a sequential manner.

### Choice of data structure
Following are few parameters, 

- What needs to be stored?
- Cost of operations
  - minimize the cost of most frequently performed operations.
- Memory usage
- Ease of implementation
  - although this is the least considered item.

### Introduction to trees
Trees data structures are quite often used to represent hierarchical data.
                     
                     John 
                     (CEO)
                   /      \
                 /          \
               /              \
            Steve              Rama
            (CTO)              (President)
          /   |   \           /      \
        Lee  Bob  Ella       Tom     Raj
            /   \           /
          Sal   Emma       Bill

So, a tree data structures are non-linear data structures and provides efficient way of storing and organizing data which is naturally hierarchical. Of course there are other application as well where tree are implemented.

### Some terminologies used in trees data structure

                     1    -----------> root
                 /      \  ----------> links/edges
                2        3  ------------> node
              / | \     /  \
             4  5  6   7    8 ----------->leaf
               / \    /
              9  10  11

              figure-1 

 * Nodes 2, 3 are **children** of node 1.
 * Node 1 is the **parent** of nodes 2, 3.
 * Children of same parent are called **siblings**, nodes 4, 5, 6 are siblings.
 * Root is the only node without parent.
 * Any node in the tree that doesn't has a child are called **leaf** node, node 9, 10, 11 are leaf nodes.
 * Node 1 is **ancestor** of 2, 4, etc.
 * Nodes 2, 4, 6, etc. are **descendent** of node 1.
 * Common ancestor of 4 and 9 are 2 and 1.

### Properties of tree

 * Trees are recursive data structure, 

                  ( )
                /  |  \
              /    |    \
            /     / \    /\
          / \    /   \  /  \
         /T1 \  / T2  \/ T3 \
  
  where T1, T2, T3 are subtrees .

* Trees with `n` nodes will have `n-1` edges/links.

### Depth of a node `x`
Depth of `x` = length of path from root to `x`  OR number of edges in the path from root to `x`. For example, in `figure-1`,
* Depth of node 2, 3 is 1
* Depth of node 4, 5, 6, 7, 8, is 2
* Depth of 9, 10, 11 is 3

### Height of a node `x`
Height of `x` = number of edges in longest path from `x` to a leaf. For example, in `figure-1`,
* Height of node 3 is 2
* Height of leaf nodes will be 0
* Height of the root node is 3

### Binary Tree
A tree in which each node can have at most 2 children.

![Binary Tree](/src/trees/images/binary-tree.png)

### Applications of trees data structure
1. Storing natually hierarchical data , e.g.   `file system`.
2. Organize data for quick search, insertion and deletion, e.g. Binary Search Trees.
3. Trie - which is a dictionary used for dynamic spell checking.
4. Network Routing Algorithm

