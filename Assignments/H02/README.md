Please view the following as code. I don't know how to format properly.
Part A
1)Define Hashing and Collision Resolution
  a)What is a hash table and why is collision resolution necessary?
    Hash tables generate indicies/addresses for values to allow for quick data access. Sometimes multiple values share the same index and so collisions needs 
    to be dealt with.
  b)Explain the key differences between open hashing (chaining) and closed hashing (open addressing).
    Open hashing places colliding values into a linked list. Closed hashing will find a different index/address for collisions.
2)Collision Resolution Techniques
  a)Briefly describe at least two methods for resolving collisions in open addressing (e.g., linear probing, quadratic probing, double hashing).
    Linear probing will choose the next available address/index in line for each collision.
    Quadractic probing will instead choose the address/index index+n^2 | n = # of tries
  b)Explain the pros and cons of each method.
    Linear probing is simple to implement, but leads to primary clustering.
    Quadractic probing reduces clustering, but may not find an empty slot.
  c)Which collision resolution technique can handle more values than table slots. Explain.
    Open hashing, because multiple values can be stored in a linked list at each slot.
  d)What is the worst performance (big oh) for each type of collision resolution technique?
    O(n) for both. Open hashing can result with all values in the same index. Closed hashing might require that you check every possible location in the table.
3)Impact of Hash Table Size
  The table's size will often determine where different keys wind up. A poorly choosen table size such as powers of 2, multiples of 10, or other common pattern,
  can result in culstering.

Part B
1)Open Hashing
  0)0
  1)101
  2)22
  3)
  4)
  5)5 --> 35
  6)16
  7)17
  8)18 --> 8
  9)z
  Buckets 5 and 8 both had collisions and contain 2 elements each.
2)Linear Probing
  0)0
  1)101
  2)22
  3)8
  4) 
  5)5
  6)35
  7)17
  8)18
  9)16
  The clustering was most apparent when 35 took the spot of 16 as well as trying to place 8.
3) Impact of Poor Table Sizes
  Size 10
  0)10 --> 20 --> 30 --> 40
  1)
  2) 
  3) 
  4) 
  5)5 --> 15 --> 25 --> 35
  6) 
  7) 
  8) 
  9) 
  A lot of clustering on 0 and 5, because the table size and the keys were both multiples of 5.

  Size 11(prime)
  0)
  1)
  2)35
  3)25
  4)15
  5) 
  6) 
  7)40
  8)30
  9)20
  10)10
  No clustering, because 11 is not a multiple of anything but 1 and itself.

Extra)Quadratic Probing
  0) 
  1)12
  2)23
  3) 
  4)67
  5)34
  6)56
  7) 
  8) 
  9)78
  10)45
  Unplaced: 89
  It may be the table size I choose but there was a lot of secondary clustering due to all the values modding to 1.

Part C
  1)Real-World Impact
    a)Explain how choosing a poor hash table size can lead to performance degradation in real-world applications.
      A poor hash table size can result in clustering which might eat up time.
    b)How do open and closed hashing strategies differ in their handling of collisions in high-load scenarios?
      Open hashing means that more keys can be stored than table size. Closed hashing is more memory efficient.
  2)Design Considerations
    It would depend on whether I am doing more reading or inserting and deleting. For reading I would use closed hashing.
    For insertions and deletions I would use open hashing
  3)Limit bucket size, and use closed hashing when a bucket is full.
