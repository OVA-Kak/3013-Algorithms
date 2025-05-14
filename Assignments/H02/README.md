Part A
1)Define Hashing and Collision Resolution
  a)What is a hash table and why is collision resolution necessary?
    Hash tables generate indicies/addresses for values to allow for quick data access. Sometimes multiple values share the same index and so collisions needs to
    be dealt with.
  b)Explain the key differences between open hashing (chaining) and closed hashing (open addressing).
    Open hashing places colliding values into a linked list. Closed hashing will find a different index/address for collisions.
2)Collision Resolution Techniques
  a)Briefly describe at least two methods for resolving collisions in open addressing (e.g., linear probing, quadratic probing, double hashing).
    Linear probing will choose the next available address/index in line for each collision.
    Quadractic probing will instead choose the address/index index+n<sup>2</sup> | n = # of tries
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
