# Binary Tree
Each node can have at most 2 children.

                           ()  ------------------> root
                         /    \ 
                       /        \
    left child <---- ()          ()   -----------> right child
                   /   \       /   \
                 ()     ()   ()     ()
                   \   /  \        /
                   () ()  ()      ()


 * A tree with just one node is also a binary tree

                    ()
                  /    \
                null   null

 * other examples of binary trees

                        ()                          ()
                       /                           /  \
                      ()                          ()   ()
                     /                           /       \
                    ()                          ()        ()
                                               /            \
                                              ()             () 

## Strict / proper / full binary tree
Each node can have either 2 or 0 children.

                                    ()      -----------> L1
                                  /    \
                                ()      ()  -----------> L2
                               /  \    /  \
                              ()   () ()   ()  --------> L3
                                  /  \
                                 ()  ()         -------> L4

## Complete binary tree
All levels except possibly the last level are completely filled and all nodes are as left as possible.

                                    ()          ----------> L1          
                                  /    \
                                /        \
                              ()          ()    ---------> L2
                             /  \        /  \
                           ()    ()     ()   ()  --------> L3
                          /  \  /  \
                         ()  ()()  ()             -------> L4
    
    
    
                                    ()          ----------> L1
                                  /    \
                                /        \
                              ()          ()    ---------> L2
                             /  \        /  \
                           ()    ()     ()   ()  --------> L3
                          /  \  /  
                         ()  ()()                 -------> L4
    
    
    max number of nodes at level i = 2 ^ i

## Perfect binary tree
All levels are completely filled except leaf and all leaves are at same level.

                                    ()          ----------> L1          
                                  /    \
                                /        \
                              ()          ()    ---------> L2
                             /  \        /   \
                           ()    ()     ()    ()  --------> L3
                          /  \  /  \   /  \  /  \
                         ()  ()()  () ()  ()()  () -------> L4


### maximum number of nodes in a tree with height `h`
    => 2^0 + 2^1 + 2^2 ........ + 2^h
    => 2^(h+1) - 1
    => 2^(number of levels) - 1

### max height of a perfect binary tree with total `n` nodes
    =>  n = 2^(h+1) -1
    =>  2^(h+1) = n + 1
    =>  h = log2(n+1) - 1

    for example, if `n` = 15
                    h = log2(15 + 1) - 1
                      = log2(16) - 1 
                      = 4 - 1 = 3
                    h = 3  

### another way of calculating height of perfect binary tree
    
    => h = |_log2(n)_|

Cost of lot of operation on tree in terms of time depends upon the height of the tree.

## Balanced binary tree
Difference between height of left and right subtree for every node is not more than `k` (mostly 1).

    Height of an empty tree  = -1
    Height of a tree with one node = 0

    H(diff) = | H(left) - H(right) |

![Balanced binary tree with height at each node](/src/trees/images/balanced-binary-tree.jpeg)


![Non Balanced binary tree with height at each node](/src/trees/images/non-balanced-binary-tree.jpeg)

### Height and Depth in a Binary Tree
 * The depth of a node is the number of edges from the root to the node.
 * The height of a node is the number of edges from the node to the deepest leaf.
 * The height of a tree is a height of the root.
 * The height of a tree is the maximum depth of any node in the tree (aka `max depth`).

![Height and Depth in a Binary Tree](/src/trees/images/height-and-depth-in-a-binary-tree.jpeg)

## Implementation of binary tree
### 1. using Doubly linked list
Dynamically created nodes linked to each other using pointers or references.

![Binary tree implementation with linked list](/src/trees/images/binary-tree-implementation-with-linked-list.jpeg)

### 2. using Arrays
This in only in some special cases, for example, `complete binary tree` or `perfect binary tree`.

![Binary tree implementation with array](/src/trees/images/binary-tree-implementation-with-array.jpeg)

for node at index `i`,

    left child index  = 2*i + 1
    right child index = 2*i + 2

Arrays are used to implement `Heaps`.