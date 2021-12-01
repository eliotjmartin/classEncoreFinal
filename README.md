# classEncoreFinal

Prep Questions and Answers
1.	Describe at least one situation where a linked list is more efficient than an array and explain why it is more efficient. 
-	Insertion + deletion: insertion and deletion in an array requires shifting of existing elements; in a LL, one must simply update the pointers
-	No wastage of memory in LL: what if you declare an array of size 1000 but only use 3 elements worth of space? Wasteful! This can be avoided with LL as they are dynamic and do not require one to declare their size at the beginning. Also, what if we need more than 1000 elements to be stored? Array sizes are static.

2.	How is a queue different from a stack?

Queue -> FIFO
Stack -> LIFO

3.	How is the load factor of a hash table computed?

if there are m entries and n is the size of the array there would be m/n entries on each index. This value m/n is called the load factor that represents the load that is there on our map

4.	What is a “collision” in a hash table? Describe an effective way to handle collisions in a hash table.
-	a hash collision is a random match in hash values that occurs when a hashing algorithm produces the same hash value for two distinct pieces of data
-	use linked list to store map entries which ended in the same bucket due to a collision
5.	Compare and contrast mergesort and quicksort in terms of memory usage, complexity, and stability. If you needed a general-purpose sorting algorithm, which would you choose?
-	Mergesort: always O(nlogn), when sorting arrays, requires O(n) additional space, stable
-	Quicksort: O(nlogn) on average but worst case scenario O(n^2), space constant, not stable
6.	If in a quick sort algorithm, the first element is always chosen as a pivot, what qualities would the array that produces the worst case time complexity have?

the worst case time complexity The most naive pivot selection algorithm is to just choose the first element as your pivot. It's easy to see that this results in worst case behavior if your data is already sorted (the first element will always be the min)

7.	What does it mean for a sorting algorithm to be stable? 

If element1 precedes element2 in the unordered input array, and element1 and element2 have the same key, then element1 precedes element2 in the ordered output array
8.	Assume you are interested in the ith element of a linked list of length n. Why can you not access this element in O(1)?

Elements not adjacent in memory

9.	In a singly linked list, is it possible to insert at the tail in O(1) complexity? If so, how? If not, why?

Yes, just keep a tail pointer

10.	In a singly linked list, is removal from the tail in O(1) complexity possible? If so, how? If not, why?

Not possible. There is no way to update the previous element to be the new tail after the current tail is deleted without traversing the whole list to find the element that precedes the current tail. 

