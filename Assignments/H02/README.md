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
    Quadractic probing will instead choose the address/index index+n<sup>2<\sup> | n = # of tries
