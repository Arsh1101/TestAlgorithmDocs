===========
Bubble Sort
===========

Bubble Sort is a simple comparison-based sorting algorithm. It repeatedly compares adjacent elements and swaps them if they are in the wrong order until the entire list is sorted.

Time Complexity:
- Best Case: O(n) - when the input list is already sorted.
- Average Case: O(n^2) - when the input list is randomly ordered.
- Worst Case: O(n^2) - when the input list is sorted in reverse order.

Space Complexity: O(1) - Bubble Sort requires a constant amount of additional space.

Python implementation:

.. code-block:: python

   def bubble_sort(arr):
       n = len(arr)
       for i in range(n):
           for j in range(0, n - i - 1):
               if arr[j] > arr[j + 1]:
                   arr[j], arr[j + 1] = arr[j + 1], arr[j]
