==========
Merge Sort
==========

Merge Sort is a divide-and-conquer algorithm that divides the input list into smaller sublists, sorts them, and then merges the sorted sublists to obtain the final sorted list.

Time Complexity:
- Best Case: O(n log n) - when the input list is randomly ordered.
- Average Case: O(n log n) - when the input list is randomly ordered.
- Worst Case: O(n log n) - when the input list is randomly ordered.

Space Complexity: O(n) - Merge Sort requires additional space to store the temporary sublists.

Python implementation:

.. code-block:: python

   def merge_sort(arr):
       if len(arr) <= 1:
           return arr

       mid = len(arr) // 2
       left_half = arr[:mid]
       right_half = arr[mid:]

       left_half = merge_sort(left_half)
       right_half = merge_sort(right_half)

       return merge(left_half, right_half)

   def merge(left, right):
       merged = []
       i = j = 0

       while i < len(left) and j < len(right):
           if left[i] <= right[j]:
               merged.append(left[i])
               i += 1
           else:
               merged.append(right[j])
               j += 1

       merged.extend(left[i:])
       merged.extend(right[j:])
       return merged