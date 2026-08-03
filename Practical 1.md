1. Bubble Sort
Introduction
Bubble Sort is the simplest sorting algorithm. It repeatedly compares adjacent elements and swaps them if they are in the wrong order. After each pass, the largest element moves to its correct position at the end of the array.

Aim
To sort a list of elements in ascending order using the Bubble Sort algorithm.

Objective
*To understand the working of Bubble Sort.
*To arrange data in ascending order.
*To learn element comparison and swapping.

Algorithm
1.Read the number of elements.
2.Store the elements in an array.
3.Compare each pair of adjacent elements.
4.Swap them if they are in the wrong order.
5.Repeat until the array is sorted.
6.Display the sorted array.

Pseudocode
START
Read n
Read array A

FOR i = 0 to n-2
    FOR j = 0 to n-i-2
        IF A[j] > A[j+1]
            Swap A[j] and A[j+1]
        ENDIF
    ENDFOR
ENDFOR
Print A
STOP

Advantages

*Easy to understand and implement.
*Works well for small datasets.
*Requires no extra memory.

Disadvantages

*Slow for large datasets.
*Large number of comparisons and swaps.
*Not suitable for real-world applications.

Conclusion
Bubble Sort is a simple algorithm suitable for learning sorting concepts, but it is inefficient for large datasets.

2. Selection Sort
Introduction
Selection Sort repeatedly selects the smallest element from the unsorted portion of the array and places it at the correct position.

Aim
To sort elements using the Selection Sort algorithm.

Objective
*To learn minimum element selection.
*To understand in-place sorting.
*To arrange data efficiently for small datasets.

Algorithm
*Read the array.
*Find the smallest element.
*Swap it with the first unsorted element.
*Repeat until the array is sorted.
*Print the sorted array.

Pseudocode
START
Read n
Read array A

FOR i = 0 to n-1
    min = i

    FOR j = i+1 to n-1
        IF A[j] < A[min]
            min = j
        ENDIF
    ENDFOR

    Swap A[i] and A[min]
ENDFOR
Print A
STOP

Advantages

1,Easy to implement.
2.Requires less memory.
3.Performs fewer swaps than Bubble Sort.

Disadvantages

1.Time complexity is O(n²).
2.Inefficient for large datasets.
3.Does not preserve the order of equal elements.

Conclusion
Selection Sort is simple and performs fewer swaps, but its quadratic time complexity makes it unsuitable for large datasets.

3. Insertion Sort
Introduction
Insertion Sort builds the sorted array one element at a time by inserting each element into its proper position.

Aim
To sort elements using the Insertion Sort algorithm.

Objective
*To understand insertion-based sorting.
*To sort data efficiently for small datasets.
*To learn shifting of elements.

Algorithm

*Read the array.
*Assume the first element is sorted.
*Pick the next element.
*Insert it into the correct position.
*Repeat until all elements are sorted.
*Display the sorted array.

Pseudocode
START
Read n
Read array A

FOR i = 1 to n-1
    key = A[i]
    j = i-1

    WHILE j >= 0 AND A[j] > key
        A[j+1] = A[j]
        j = j-1
    ENDWHILE

    A[j+1] = key
ENDFOR
Print A
STOP

Advantages

*Efficient for small datasets.
*Stable sorting algorithm.
*Works well for nearly sorted data.

Disadvantages

*Slow for large datasets.
*Time complexity is O(n²) in average and worst cases.
Conclusion
Insertion Sort is efficient for small and nearly sorted datasets but becomes slow as the dataset size increases.

4. Merge Sort
Introduction
Merge Sort is a Divide and Conquer algorithm. It divides the array into smaller subarrays, sorts them recursively, and merges them into a sorted array.

Aim
To sort elements using the Merge Sort algorithm.

Objective
*To understand Divide and Conquer.
*To efficiently sort large datasets.
*To learn recursive sorting techniques.

Algorithm
*Divide the array into two halves.
*Recursively sort both halves.
*Merge the sorted halves.
*Repeat until the complete array is sorted.
*Display the sorted array.

Pseudocode
START

MergeSort(A)

IF length(A) > 1
    Divide A into Left and Right

    MergeSort(Left)
    MergeSort(Right)

    Merge Left and Right into A
ENDIF
Print A
STOP

Advantages

*Fast and efficient.
*Stable sorting algorithm.
*Guaranteed O(n log n) time complexity.

Disadvantages

*Requires extra memory.
*Recursive implementation is more complex.
Conclusion
Merge Sort is one of the most efficient sorting algorithms for large datasets and guarantees consistent performance.

5. Quick Sort
Introduction
Quick Sort is a Divide and Conquer algorithm that selects a pivot element and partitions the array into smaller and larger elements before recursively sorting them.

Aim
To sort elements using the Quick Sort algorithm.

Objective
*To understand partitioning.
*To efficiently sort large datasets.
*To implement recursive sorting.

Algorithm

*Choose a pivot element.
*Partition the array.
*Place the pivot in its correct position.
*Recursively sort left and right subarrays.
*Display the sorted array.

Pseudocode

START

QuickSort(A, low, high)

IF low < high
    pivot = Partition(A)

    QuickSort(A, low, pivot-1)
    QuickSort(A, pivot+1, high)
ENDIF
Print A
STOP

Advantages

*Very fast in practice.
*Average time complexity is O(n log n).
*Requires less memory than Merge Sort.

Disadvantages

*Worst-case time complexity is O(n²).
*Recursive implementation.
*Performance depends on pivot selection.

Conclusion
Quick Sort is one of the fastest sorting algorithms for practical applications. Although its worst-case complexity is O(n²), good pivot selection usually provides excellent average-case performance of O(n log n).
____________________________________________________________________
| Algorithm      | Best       | Average    | Worst      | Space    |
| -------------- | ---------- | ---------- | ---------- | -------- |
| Bubble Sort    | O(n)*      | O(n²)      | O(n²)      | O(1)     |
| Selection Sort | O(n²)      | O(n²)      | O(n²)      | O(1)     |
| Insertion Sort | O(n)       | O(n²)      | O(n²)      | O(1)     |
| Merge Sort     | O(n log n) | O(n log n) | O(n log n) | O(n)     |
| Quick Sort     | O(n log n) | O(n log n) | O(n²)      | O(log n) |
|__________________________________________________________________|
