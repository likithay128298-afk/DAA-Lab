Max Heap Sort
Introduction

Heap Sort is a comparison-based sorting algorithm that uses a Binary Heap data structure. In Max Heap Sort, the largest element is placed at the root of the heap. The root is repeatedly swapped with the last element, and the heap is rebuilt until the array is sorted in ascending order.

Aim

To sort a list of elements in ascending order using the Max Heap Sort algorithm.

Objective
To understand the concept of a Max Heap,
To implement Heap Sort using a Binary Heap,
To efficiently sort data with O(n log n) time complexity.

Algorithm

Read the number of elements,
Store the elements in an array,
Build a Max Heap from the array,
Swap the root (maximum element) with the last element,
Reduce the heap size by one,
Heapify the root to restore the Max Heap,
Repeat Steps 4–6 until all elements are sorted,
Display the sorted array.

Pseudocode

START
Read n
Read array A

Build Max Heap

FOR i = n-1 DOWNTO 1
    Swap A[0] and A[i]
    Heapify(A, i, 0)
ENDFOR
Print A
STOP

Advantages

Efficient with O(n log n) time complexity,
Performs sorting in-place (no large extra memory required),
Suitable for large datasets,
Worst-case performance is guaranteed.

Disadvantages

Not a stable sorting algorithm,
Slightly more complex than Bubble, Selection, and Insertion Sort,
Can be slower than Quick Sort in practice due to cache performance.

Time Complexity
Best Case	O(n log n)
Average Case	O(n log n)
Worst Case	O(n log n)

Space Complexity
O(1) (In-place sorting)

Conclusion
Max Heap Sort is an efficient comparison-based sorting algorithm that uses a Max Heap to repeatedly place the largest element in its correct position. It guarantees O(n log n) time complexity in all cases and is well suited for sorting large datasets efficiently.
