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
**Associative containers** implement sorted data structures that can be quickly searched (O(log n) complexity).  
**Unordered associative** containers implement unsorted (hashed) data structures that can be quickly searched (O(1) amortized, O(n) worst-case complexity).  
**Container adaptors** provide a different interface for sequential containers.  
[Source][source-cont-structures]{:target="_blank_"}


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

[source-cont-structures]:   https://www.geeksforgeeks.org/containers-cpp-stl/
[stl-summary]:              https://users.cs.northwestern.edu/~riesbeck/programming/c++/stl-summary.html
[big-o-1]:                  https://www.bigocheatsheet.com/
[big-o-2]:                  https://cooervo.github.io/Algorithms-DataStructures-BigONotation/index.html