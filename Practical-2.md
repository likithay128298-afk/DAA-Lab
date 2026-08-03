1. Linear Search Method
Introduction
Linear Search is the simplest searching algorithm. It searches for a target element by checking each element in the list sequentially from the beginning until the element is found or the end of the list is reached. It can be used on both sorted and unsorted arrays.

Aim
To search for a given element in a list using the Linear Search algorithm.

Objective
To understand the concept of sequential searching,
To locate the position of a specified element in a list,
To learn the implementation of Linear Search in Python,

Algorithm

Read the number of elements,
Store the elements in an array,
Read the element to be searched,
Compare the search element with each element of the array one by one,
If a match is found, display its position,
If the end of the array is reached without finding the element, display "Element not found.",

Pseudocode

START
Read n
Read array A
Read key

FOR i = 0 to n-1
    IF A[i] == key
        Print "Element found at position", i+1
        STOP
    ENDIF
ENDFOR
Print "Element not found"
STOP

Advantages

Very simple and easy to implement,
Works with both sorted and unsorted arrays,
No preprocessing or sorting is required,
Suitable for small datasets,

Disadvantages

Inefficient for large datasets,
Searches each element one by one,
Time complexity increases as the size of the data increases,

Conclusion
Linear Search is a basic searching technique that checks each element sequentially until the required element is found. It is easy to understand and implement, making it suitable for small datasets and unsorted lists. However, for large datasets, more efficient algorithms such as Binary Search are preferred.


2. Binary Search
Introduction
Binary Search is an efficient searching algorithm used to find an element in a sorted array. It works by repeatedly dividing the search interval into two halves until the required element is found or the search interval becomes empty.

Aim
To search for a given element in a sorted list using the Binary Search algorithm.

Objective
To understand the working of Binary Search,
To efficiently locate an element in a sorted array,
To reduce the number of comparisons during searching,

Algorithm

Read the number of elements,
Enter the elements in sorted order,
Read the search element,
Set low = 0 and high = n-1,
Find the middle element using mid = (low + high) // 2,
If the middle element equals the search element, display its position,
If the search element is greater, search the right half,
Otherwise, search the left half,
Repeat until the element is found or low > high,
If not found, display "Element not found.",

Pseudocode

START
Read n
Read sorted array A
Read key

low = 0
high = n - 1

WHILE low <= high
    mid = (low + high) // 2

    IF A[mid] == key
        Print "Element found at position", mid + 1
        STOP
    ELSE IF A[mid] < key
        low = mid + 1
    ELSE
        high = mid - 1
    ENDIF
ENDWHILE
Print "Element not found"
STOP

Advantages

Faster than Linear Search,
Time complexity is O(log n),
Efficient for large datasets,
Reduces the number of comparisons,

Disadvantages

Works only on sorted arrays,
Sorting the data beforehand may require additional time,
Not suitable for frequently changing datasets,

Conclusion
Binary Search is one of the most efficient searching algorithms for sorted datasets. By repeatedly dividing the search space into halves, it significantly reduces the number of comparisons, making it much faster than Linear Search for large collections of data.

| Algorithm                     | Best Case | Average Case | Worst Case   | Space Complexity |
| ----------------------------- | --------- | ------------ | ------------ | ---------------- |
| **Linear Search**             | **O(1)**  | **O(n)**     | **O(n)**     | **O(1)**         |
| **Binary Search (Iterative)** | **O(1)**  | **O(log n)** | **O(log n)** | **O(1)**         |
| **Binary Search (Recursive)** | **O(1)**  | **O(log n)** | **O(log n)** | **O(log n)**     |
