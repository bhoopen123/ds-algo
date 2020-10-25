# Binary Search Tree

### What data structure will you use to store a modifiable collection in which Search, Insert, and Remove/Delete all are efficient?

| | Array (unsorted) | Linked List | Array (sorted) | Binary Search Tree
----------|------------------|-------------|----------------|-------------------
Search(x) |   O(n) | O(n) | O(log(n)) | O(log(n))
Insert(x) |   O(1) | O(1) | O(n) | O(log(n))
Delete(x) |   O(n) | O(n) | On) | O(log(n))

    Assume, the cost of 1 comparision = 10^(-6) sec (1 micro second)
    100 millions comparisions => 10^8 => 100 Seconds

    Which is quite slow if searching is a frequently performed operations.

## Binary Search Tree
A binary search tree is which, for each node value of all the nodes in the left subtree is lesser or equal and the value of all the nodes in the right subtree is greater.

                  ( )   ----------> root
                /    \
              /        \
            /\          /\
           /T1\        /T2\
          /____\      /____\
         
         left          right
         subtree       subtree
    (lesser or equal)  (greater)


### Examples
Below are the examples of Balanced Binary Search Tree

                    (15)
                   /    \
                 /        \
               (10)      (20)
              /   \      /   \
            (8)  (12)  (17) (25)


                    (12)1
                   /    \
                 /        \
                (8)1      (15)1
                  \       /   \
                  (10)0 (17)0 (20)1
                                \
                                (20)0

    The number after the node value denotes the height difference at that node.

Below are the examples of Un-balanced Binary Search Tree

                        (25)  -----> root
                        /
                     (20)
                     /
                  (17)
                  /
                (15)
                /
              (12)
              /
            (10)
            /
          (8)


            (15)  -----------------> root
               \
               (16)
                 \
                 (19)
                   \
                   (20)
                     \
                     (21)
                       \
                       (22)
                         \
                         (25)

