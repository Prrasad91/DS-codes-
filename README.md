# DS codes 
 
We saw how min-heaps can efficiently allow us to query the least element in a heap (array). We would like to modify minheaps in this exercise to design a data structure to maintain the least k elements for a given  𝑘≥1
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

