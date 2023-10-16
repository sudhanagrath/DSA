# Time and Space Complexity for the Data Structure Problems
## Introduction
This document briefly describes the Time and Space Complexity of the problems worked in the project 2. 

## Problem 1
LRU Cache is implemented by using doubly linked list and dictionary as hash map.

### Time Complexity : 
LRU Cache items are stored in the order from most recently used to least recently used. The cost of get operation for any item  is O(1). The cost of set operation is also O(1). 

### Space Complexity
LRU Cache is built using linked list of n elements and hash map of n elements, the space efficiency is O(n) using two data structures.

## Problem 2
Function is defined to find files with the given suffix and the given path using recursion.

### Time Complexity
Function is called recursively for every directory in the given path. So the cost of recursive call is O(n) where n is the number of directories in the path.

### Space Complexity
In this function, for each recursive call, call stack is waiting to execute for every directory until all the directories have been called. So if there are n directories in the path, space efficiency becomes O(n).

## Problem 3
Huffman coding algorithm has three parts, building a tree based on the frequency of characters in the input data, encoding the tree, and decoding the tree.

### Time Complexity 
In this problem, the tree is built using priority queue in which nodes having lowest frequency are given the highest priority to add to the tree. Each of the two methods in the HuffmanCoding class, build\_char\_freq_map and sort\_by\_freq has the time complexity of O(n) where n is the number of characters in the input data. The build\_tree method has the time complexity of O(logn). Time complexity for building the tree comes out to be O(nlogn)

Once the Huffman tree has been generated, it is traversed to generate a dictionary to map the characters to binary code using 0 and 1. The final encoding of any symbol  is then read by concatenating the edges along the paths from root node to the symbol. Time complexity is not very important in encoding and decoding here as the n is the number of symbols in the alphabetic list which is very small as compared to the length of the message being encoded, whereas complexity analysis is concerned with behaviour where n becomes very large.

### Space Complexity
If there are n symbols in the input data, we need to store each of them in an array, so the space complexity is O(n).


## Problem 4
In this problem, the function uses class objects of users and groups to check if the given user is in specified group. Because the group contains other groups called subgroups, function makes recursive calls to check if a user is in the subgroups.

### Time Complexity
Becuase the function makes recursive calls for every sub-group in the given group, Time complexity is of the linear order. It increases with the number of nested sub-groups in the group, the function has to check.

### Space Complexity
Each recursive call to check the sub-groups  is placed in the stack to wait to execute until all the sub-groups in the group have been processed. It makes the Space complexity O(n) where n is the number of sub-groups in the group.

## Problem 5
This problem is about building a simplest blockchain. We are given a class Block that defines the unit of the blockchain, block. We are asked to add this block to the blockchain using class Blockchain. This class uses linked list to build the blockchain by adding block as node to the blockchain as linked list. The class method add_block has been defined to carry out this task.

### Time Complexity
The class method add_block builds the blockchain by linking each block using hash digest of previous block in the chain and also tracking the latest block by its hash digest. The latest block is added at the tail of the blockchain making the time complexity O(1) for one block. If there are n blocks in the blockchain, time complexity will be O(n)

### Space Complexity
Each block in the blockchain is like a node in the linked list, and the block containing all the data, the space efficiency is O(1) for one block. Blockchain having n blocks will have space cost as O(n).

## Problem 6
Union of two linked lists is found in two steps, first by removing duplicates in the first linked list, and then from the second linked list. Finally use the set structure holding the unique elements from the two lists to insert into an empty linked list.

Intersection of two linked lists is found in similar way, first by adding the unique elements of first linked list to set and then iterate over the second linked list for each element in the set to add to an empty linked list.

### Time Complexity
If l1 and l2 are the length of two linked lists, the time complexity of function finding their union is O(l1+l2), and time complexity of function finding their intersection is O(l1*l2)

### Space Complexity



 
