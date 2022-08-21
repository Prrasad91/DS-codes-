# DS codes 
 
This Repository  provides an implementation of the algorithm



*************
Heap_k.py
*************
Heaps are binary trees for which every parent node has a value less than or equal to any of its children. This implementation uses arrays for which heap[k] <= heap[2*k+1] and heap[k] <= heap[2*k+2] for all k, counting elements from zero. For the sake of comparison, non-existing elements are considered to be infinite. The interesting property of a heap is that its smallest element is always the root, heap[0].



************
TOPK Heap.py
************
Saw how min-heaps can efficiently allow us to query the least element in a heap (array). We would like to modify minheaps in this exercise to design a data structure to maintain the least k elements for a given  𝑘≥1
k≥1 with 𝑘=1
 
being the minheap data-structure.
Our design is to hold two arrays:
(a) a sorted array A of  𝑘  elements that forms our least k elements; and
(b) a minheap H with the remaining  𝑛−𝑘  elements.
Our data structure will itself be a pair of arrays (A,H) with the following property:
H must be a minheap
A must be sorted of size  𝑘
Every element of A must be smaller than every element of H.
The key operations to implement in this assignment include:
insert a new element into the data-structure
delete an existing element from the data-structure.
We will first ask you to design the data structure and them implement it.

case 1:
 insert element j is less than element in array ...

j < A[k-1] element in array A 
 j' = a[k-1]
replace a[k-1] by j
perform sort to move j to correct place ... now Array a is good .
Insert j' to heap

insert element is greater than element in array A:
j>=A[k-1]
insert in Heap using heap insert


************
Heap data structure to mantain/extract median (instead of minimum/maximum key)
*********


We have seen how min-heaps can efficiently extract the smallest element efficiently and maintain the least element as we insert/delete elements. Similarly, max-heaps can maintain the largest element. In this exercise, we combine both to maintain the "median" element.

    The median is the middle element of a list of numbers. 
- If the list has size $n$ where $n$ is odd, the median is the $(n-1)/2^{th}$ element where $0^{th}$ is least and $(n-1)^{th}$ is the maximum. 
- If $n$ is even, then we designate the median the average of the $(n/2-1)^{th}$ and $(n/2)^{th}$ elements.


#### Example 

- List is $[-1, 5, 4, 2, 3]$ has size $5$, the median is the $2^{nd}$ element (remember again least element is designated as $0^{th}$) which is $3$.
- List is $[-1, 3, 2, 1 ]$ has size $4$. The median element is the average of  $1^{st}$ element (1) and $2^{nd}$ element (2) which is  $1.5$.

 Design algorithm for insertion.

Suppose, we have the current data split between $H_{max}$ and $H_{min}$ and we wish to insert an element $e$ into the data structure, describe the algorithm you will use to insert. Your algorithm must decide which of the two heaps will $e$ be inserted into and how to maintain the size balance condition