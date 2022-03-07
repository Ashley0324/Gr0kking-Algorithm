# 算法图解
## 1 Introduction 
### 1-1 introduction 
#### An algorithm is a set of instructions for accomplishing a task
### 1-2 Binary Search 
#### Guess a number in fewest tries, eliminate half the numbers every time 
##### Log2 n times
### 1-3 Big O notation 
#### How fast an algorithm is
##### Simple Search
###### O(n)
* Linear time
##### Binary Search
###### O(log n)
* Log time
##### Quick sort
###### O(n log n)
* Fast sorting algorithm 
##### Selection sort
###### O(n2)
* Low sorting algorithms 
##### Traverling salesperson 
###### O(n!)
* Really low
### Recap
#### Binary search is a lot faster than simple search
#### Algorithm speed isn’t measured in seconds
#### Algorithm times are measured in terms of growth of an algorithm 
#### Algorithm times are written in big O notation 
## 2 Selection Sort
### 2-1 Memory works principal 
#### Store items in drawers 
### 2-2 Arrays and linked lists
#### Arrays
##### Tasks are stored contiguous 
##### Know the address for every item
##### Allow random access and sequential access
##### Are faster at read because they provide random access
##### Are used a lot
#### Linked lists
##### Solve the problem of adding items
##### Items can be anywhere in memory
##### Random memory address are linked together (like treasure hunt)
##### Are better to delete or add an element
##### Only allow sequential access 
#### Terminology
##### Elements in arrays are numbered from0
##### Position of an element is called it’s index 
### 2-3 Selection sort
#### It’s neat but not very fast, Quicksort is faster
#### Sort an array from smallest to largest
### Recap
#### Computer memory is like a giant set of drawers
#### Use an array or a list to store multiple elements 
#### Elements are stored right next to each other in arrays
#### Elements are strewn all over in a list
#### Arrays allow fast reads
#### Linked lists allow fast inserts and deletes 
#### All elements in the arrays should be the same
## 3 Recursion 
### 3-1 Recursion 
#### Matryoshka doll
#### There’s no performance benefit for programs , but achieve a performance gain for programmer
### 3-2 Component
#### Recursive case
##### The function calls itself 
#### Base case
##### The function doesn’t call itself again
### 3-3 Stack
#### Stack is a simple data structure
#### Has only two actions: push and pop
### 3-4 The call stack
#### Your computer uses a stack internally called the call stack
#### Used to save the variables for multiple functions
### 3-5 The call stack with recursion
#### Recursive functions use the call stack
##### Factorial function
#### Using a stack is convenient, but there’s a cost of memory to save info 
##### To solve it, you can rewrite your code to use a loop instead
##### Use tail recursion 
### 3-6 Recap
#### Recursion is when a function calls itself
#### Every recursive function has two cases: base cases and the recursive case
#### A stack has two operations: push and pop
#### All function calls go onto the call stack
#### The call stack can get very large, which takes up a lot of memory
## 4 Quicksort
### 4-1 Decide & conquer 
#### A recursive technique for solving problems
#### Examples
##### Divide farm evenly into square plots
##### Add up the numbers and return the total
#### Work principle
##### Figure out a simple case as the base case
##### Figure out how to reduce your problem and get to the base case
### 4-2 Quicksort
#### Quicksort is a sorting algorithm and it’s faster than selection sort
##### Eg: qsort in C standard library 
#### Pick an element called pivot
##### Sub-array less, pivot, sub-array more
##### Call Quicksort recursively on the two sub-arrays
### 4-3 Big O notion revisited
#### Merge sort
##### O(n log n)
#### Quick sort
##### Takes O(n log n)in the average case
##### Takes O(n2) in the worst case
### 4-4 Recap
#### Divide and conquer works by breaking a problem down into smaller and smaller pieces.
#### If you are implementing Quicksort, choose a random element as the pivot. The average runtime of Quicksort is O(n log n )
#### The constant in big O notation can matter sometimes.
#### The constant almost never matters for simple search versus binary search, because O(log n)is so much faster than O(n) when your list gets big
## 5. Hash tables
### 5-1 Find an item in O(1)
### 5-2 Hash functions
#### Is a function where you put in a string and you get back a number
#### Requirements 
##### It need to be consistent 
##### It should map different words to different numbers
##### Python has hash tables, called dictionaries 
#### Components 
##### Keys
###### The name of produce in the book hash
##### Values 
###### Their prices 
### 5-3 Use cases
#### Lookups 
##### Need to create a mapping from one thing to another thing
##### Need to look something up 
#### Preventing duplicate
##### Make sure everyone vote just once in a voting booth
#### Caching 
##### Make a request to server
##### The server thinks for a second and comes up with the web pages to you
##### You get a web page
##### The server has to serve millions of people, couple of seconds adds up for them
##### Work principle 
###### Remember the data instead of recalculating it
##### Advantages
###### You get the home page a lot faster
###### Company has to do less work
#### Recap(Advantages)
##### Modelling relationships from one thing to anything thing
##### Filtering out the duplicates
##### Caching or memorising data instead of making your server do work
### 5-4 Collisions
#### Two keys have been assigned the same slot
#### To solve it, start a linked list at the slot if multiple keys map to the same slot
#### A good hash function has less collisions
### 5-5 Performance 
#### O(1) constant time 
##### It means the time taken will stay the same, regardless of how big the hash table is.
#### O(n) linear time
##### In the worst case, a hash table takes linear time.
#### To perform better, you need to avoid collisions by
##### A low load factor
##### A good hash function
#### Load factor
##### Usage rate
#### A good hash function
##### Distributes values in the array evenly
##### With less collisions 
### 5-6 recap
#### You can make a hash table by combining a hash. function with an array
#### Collisions are bad. You need a hash function that minimises collisions
#### Hash tables are good for modelling relationships from one items to another items
#### Your load factor should less than0.7
#### Hash tables are used for caching data
#### Hash tables are great for catching duplicates
## 6. Breadth-first search
### It’s a graph algorithm 
#### Allows you find the shortest distance between two things 
### 6-1 Introduction to graphs
#### Shortest path problem 
##### First step model the problem as a graph
##### Solve the problem using breadth first search
### 6-2 what’s a graph 
#### Each graph is made up of nodes and edges
#### Connected nodes are called neighbours 
### 6-3 breadth first search
#### Solve two types problem 
##### Find a path from node A to node B
##### What is the shortest path from node A to node B
#### Finding the shortest path
##### Prefer the former connection 
##### Use data structure called queues 
#### Queues
##### Like stack,only has two operations:
###### Enqueue
###### Dequeue
##### The queue is called a FIFO data structure: first in, first out
##### The stack is a LIFO data structure: Last in, last out
### 6-4 implanting the graph
#### It doesn’t matter what order you add the key pairs in
### 6-5 Implementing the algorithm 
#### Coding example 
#### Running time
##### O(number of vertices +number of edges)
### 6-6 Recup
#### Breadth-first search tells you if there’s a path from A to B
#### If there’s a path, breadth first search will find the shortest path
#### A directed graph has arrows, and the relationship follows the direction of the arrow
#### Undirected graphs don’t have arrows, and the relationship goes both ways
#### Queues are FIFO, stacks are LIFO
#### You need to check people in the order they were added to the search list, so the search list needs to be queue.
#### Once you check someone, make sure you don’t check them again
## 7. Dijkstra’s algorithm 
### 7-0 introduction 
#### Answer what’s the shortest path to X, for weighted graph
#### Breadth first search will find you the path with the fewest segments
#### Dijkstra algorithm will find you the fastest path
### 7-1 Working with dijkstra algorithm 
#### Find the cheapest node
#### Update the costs of neighbours of this node 
#### Repeat until you’ve done this for every node in the path
#### Calculate the final path.
### 7-2 Terminology 
#### Weights
##### A graph with weight is called weighted graph
##### A graph without weight is called unweighted graph
#### Shortest path
##### Unweighted graph
###### Breadth first search 
##### Weighted graph 
###### Dijkstra algorithm 
#### Cycle
##### You can start at a node, travel around and end up at the same node.
##### An undirected graph means that both nodes point to each other. That’s a cycle
##### Dijkstra only works with undirected a cyclic graph,called DAGs
### 7-3 Trading for a piano
#### Negative weight edges
### 7-4 Implementation 
#### Coding example
#### Run time
## 8. Greedy Algorithm 
### 8-0 Introduction 
#### Tackle the NP-complete problems 
#### Identify such problems
#### Approximation algorithm 
#### Greedy algorithm 
### 8-1 classroom scheduling problem 
#### At each step, pick the locally optimal solution
### 8-2 The knapsack problem
#### The greedy strategy doesn’t give you the optimal solution, but it gets you pretty close.
### 8-3  The set-covering problem
#### Radio show problem
#### Approximation algorithms are judged by
##### How fast they are
##### How close to the optimal choice 
#### Code for setup
##### Subset
#### Calculating the answer
##### Set union 
##### Set intersection 
### 8-4 NP complete problem
#### To solve these problems, you have to calculate every possible set
#### How to tell if a problem is NP complete 
##### Run quickly with less items
##### All combinations of X
##### Have to calculate every possible version
##### Have a sequence 
### 8-5 Recup
#### Greedy algorithm optimize locally, hoping to end up with a global optimum
#### NP complete problems have no known fast solution 
#### If you have an NP complete problem,your best bet is to use an approximation algorithm 
#### Greedy algorithm are easy to write and fast to run,so they make good approximation algorithm 
## 9 Dynamic programming 
### 9-1 Revisit the knapsack problem 
#### The simple solution
##### Try every possible set of goods and find the set that gives you the most value
#### Dynamic programming 
##### Solve sub problems and big problem
##### Every dynamic programming algorithm starts with a grid.
### 9-2 Recup
#### Dynamic programming is useful when you are trying to optimize something given a constraint 
#### You can use dynamic programming when problems can be broken into discrete sub problems 
#### Every dynamic programming solution involves a grid
#### The values in the cells are usually what you’re trying to optimize 
#### Each cell is a sub problem 
#### There’s no single formula for a dynamic programming solution 
## 10. K-nearest neighbors 
### Classifying orange and grapefruit 
#### K-nearest neighbors
### Build a recommendation system 
#### Plot every user on a graph by similarity
#### Feature extraction 
##### Find the distance between two points
#### Regression
##### Predicting a response
#### Cosine similarity 
##### Look it up if you use KNN
##### Does not measure the distance between two points
##### It compare the angle of two vectors 
#### Picking good features 
### Introduction to machine learning
#### OCR optical character recognition 
##### Read the text of a page photo
##### Google use it to digitize books
#### Spam filter
##### Naive bayes classifier
### Recup
#### Classification 
##### Categorization into a group
##### Regression
###### Predicting a response
#### Feature extraction means converting an item into a list of numbers that can be compared 
#### Picking good features is an important part of a successful KNN algorithm 
