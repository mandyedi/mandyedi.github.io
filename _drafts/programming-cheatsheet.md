# Table of contents
1. [C++ Container Comparison](#cpp-container-time)
2. [C++ Containers](#cpp-containers)
3. [C++ Pointers](#cpp-pointers)
4. [Sorting Algorithms](#sorting)

## C++ Container Time Complexities <a name="cpp-container-time"></a>
| Containers          | Structure          | Sorted | Insertion | Access   | Erase    | Search  |
| ------------------- |:------------------:|:------:|:---------:|:--------:|:--------:|:-------:|
| vector              | sequence container | no     | O(n)      | O(1)     | O(n)     | O(n)     |
| array               | sequence c.        | no     | -         | O(1)     | -        | O(n)     |
| stack               | sequence c.        | no     | O(1)      | O(1)     | O(1)     | -        |
| queue               | container adaptors | no     | O(1)      | O(1)     | O(1)     | -        |
| deque               | sequence c.        | no     | O(1)      | O(1)     | O(1)     | -        |
| priority_queue      | container adaptors | yes    | O(log n)  | O(1)     | O(log n) | -        |
| list                | sequence c.        | no     | O(1)      | O(1)     | O(1)     | O(n)     |
| forward_list        | sequence c.        | no     | O(1)      | O(1)     | O(1)     | O(n)     |
| set                 | associative c.     | yes    | O(log n)  | O(log n) | O(log n) | O(log n) |
| map                 | associative c.     | yes    | O(log n)  | O(log n) | O(log n) | O(log n) |
| multiset            | associative c.     | yes    | O(log n)  | O(log n) | O(log n) | O(log n) |
| multimap            | associative c.     | yes    | O(log n)  | O(log n) | O(log n) | O(log n) |
| unordered_set       | unordered a. c.    | no     | O(1)      | O(1)     | O(1)     | O(1)     |
| unordered_map       | unordered a. c.    | no     | O(1)      | O(1)     | O(1)     | O(1)     |
| unordered_mulitset  | unordered a. c.    | no     | O(1)      | O(1)     | O(1)     | O(1)     |
| unordered_multimap  | unordered a. c.    | no     | O(1)      | O(1)     | O(1)     | O(1)     |

Useful links:  
[STL summary][stl-summary]{:target="_blank_"}  
[Big O cheat sheet 1][big-o-1]{:target="_blank_"}  
[Big O cheat sheet 2][big-o-2]{:target="_blank_"}

**Sequence containers** implement data structures which can be accessed sequentially.  
- **array** provides a static contiguous array
- **vector** provides a dynamic contiguous array
- **forward_list** provides a singly-linked list
- **list** provides a doubly-linked list
- **deque** provides a double-ended queue, where elements can be added to the front or back of the queue.

**Sequence container adapters** provide a different interface for sequential containers.  
hese container adapters encapsulate the underlying container type and limit the user interfaces accordingly.  

- **stack** provides an LIFO data structure, stack can be implemented on top of vector
- **deque** or list
- **queue** provides a FIFO data structure, queue can be implemented on top of deque or list
- **priority_queue** provides a priority queue, which allows for constant-time lookup of the largest element (by default), priority_queue can be implemented on top of deque or vector

**Associative containers** implement sorted data structures that can be quickly searched (O(log n) complexity). The STL AssociativeContainer types are can be divided in two ways: containers which require unique keys, and those which allow multiple entries using the same key.

Keys are unique:
- **set** is a collection of unique keys, sorted by keys
- **map** is a collection of key-value pairs, sorted by keys  

Multiple entries for the same key are permitted:
- **multiset** is a collection of keys, sorted by keys
- **multimap** is a collection of key-value pairs, sorted by keys
- Note that set and map are typically implemented using red-black trees.

**Unordered associative containers** implement unsorted (hashed) data structures that can be quickly searched (O(1) amortized, O(n) worst-case complexity). or all STL UnorderedAssociativeContainer types, a hashed key is used to access the data.

Keys are unique:
- **unordered set** is a collection of keys, hashed by keys
- **unordered_map** is a collection of key-value pairs, hashed by keys

Multiple entries for the same key are permitted:
- **unordered_multiset** is a collection of keys, hashed by keys
- **unordered_multimap** is a collection of key-value pairs, hashed by keys

[Source][c++-containers]{:target="_blank_"}  
[Source2][c++-containers-2]{:target="_blank_"}


## C++ Containers <a name="cpp-containers"></a>

### Vector

### List

### Queue

### Deque

### Stack

### Map

### Unordered Map

## C++ Pointers <a name="cpp-pointers"></a>
Pointers...

## Sorting Algorithms <a name="sorting"></a>
Sorting...

## Tree Traversal
Tree traversal...
https://www.hackerrank.com/challenges/30-binary-trees/problem

[c++-containers]:           https://www.geeksforgeeks.org/containers-cpp-stl/
[c++-containers-2]:         https://github.com/NelsonBilber/cpp-overview/blob/master/docs/containers.and.iterators.org
[stl-summary]:              https://users.cs.northwestern.edu/~riesbeck/programming/c++/stl-summary.html
[big-o-1]:                  https://www.bigocheatsheet.com/
[big-o-2]:                  https://cooervo.github.io/Algorithms-DataStructures-BigONotation/index.html