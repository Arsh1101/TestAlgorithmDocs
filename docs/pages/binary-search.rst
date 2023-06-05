=============
Binary Search
=============

Binary Search is an efficient algorithm for finding an element's position in a sorted list. It repeatedly divides the search space in half by comparing the target element with the middle element of the sorted list.

Time Complexity: O(log n) - Binary Search halves the search space in each iteration, resulting in a logarithmic time complexity.

Space Complexity: O(1) - Binary Search does not require any additional space.

Code implementation:

.. code-block:: python
  :linenos:

   def binary_search(arr, target):
       low = 0
       high = len(arr) - 1

       while low <= high:
           mid = (low + high) // 2
           if arr[mid] == target:
               return mid
           elif arr[mid] < target:
               low = mid + 1
           else:
               high = mid - 1

       return -1

.. code-block:: javascript
  :linenos:

   function binarySearch(arr, el, compare_fn) {
       let m = 0;
       let n = arr.length - 1;
       while (m <= n) {
           let k = (n + m) >> 1;
           let cmp = compare_fn(el, arr[k]);
           if (cmp > 0) {
               m = k + 1;
           } else if(cmp < 0) {
               n = k - 1;
           } else {
               return k;
           }
       }
       return ~m;
   }