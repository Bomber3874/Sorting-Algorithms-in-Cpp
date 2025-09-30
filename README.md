# Sorting-Algorithms-in-Cpp

# Aim

To study and implement various sorting algorithms in C++, including Bubble Sort, Selection Sort, and Quick Sort, demonstrating their working principles, time complexities, and practical applications in organizing data efficiently.

# Software Used

Compiler: GNU GCC (g++)

IDE: Visual Studio Code

Operating System: Windows/Linux

# Theory

Sorting algorithms are fundamental computer science procedures that arrange elements of a list in a specific order (ascending or descending). Different sorting algorithms offer varying trade-offs between time complexity, space complexity, stability, and implementation complexity.

Key Sorting Algorithms:

Bubble Sort:

    Repeatedly steps through the list, compares adjacent elements and swaps them if they are in wrong order
    
    Time Complexity: O(n²) worst and average case, O(n) best case
    
    Space Complexity: O(1)
    
    Stable: Yes

Selection Sort:

    Divides the input list into two parts: sorted and unsorted
    
    Repeatedly finds the minimum element from unsorted part and puts it at the beginning
    
    Time Complexity: O(n²) in all cases
    
    Space Complexity: O(1)
    
    Stable: No

Quick Sort:

    Divide and conquer algorithm that picks an element as pivot and partitions the array around the pivot
    
    Recursively sorts the sub-arrays
    
    Time Complexity: O(n log n) average case, O(n²) worst case
    
    Space Complexity: O(log n)
    
    Stable: No

Importance of Sorting:

    Fundamental operation in computer science
    
    Essential for efficient searching (like binary search)
    
    Required for data analysis and visualization
    
    Critical in database operations
    
    Forms basis for many other algorithms

# Algorithms

# 1. Bubble Sort with Binary Search

Algorithm:

    Start the program
    
    Include necessary headers: <iostream> and <vector>
    
    Define bubbleSort class with public method:
    
      sort(std::vector<int>& arr) that takes vector reference
      
      Get array size n = arr.size()
    
      Implement nested loops:
    
        Outer loop i from 0 to n-2
        
        Inner loop j from 0 to n-i-2
        
        Compare arr[j] and arr[j+1]
        
        If arr[j] > arr[j+1], swap elements using std::swap()
    
    Define SearchArr class with public method:
    
      binarysearch(const std::vector<int>& arr, int target)
      
      Initialize low = 0 and high = arr.size()-1
      
      While low <= high:
    
        Calculate mid = low + (high - low)/2
        
        If arr[mid] == target, return mid index
        
        Else if arr[mid] < target, set low = mid + 1
        
        Else set high = mid - 1
    
      Return -1 if target not found
    
    In main() function:
    
      Create objects of bubbleSort and SearchArr classes
      
      Initialize vector arr = {-1, 0, 3, 5, 9, 12}
      
      Call sorter.sort(arr) to sort the array
      
      Display sorted array using for loop
      
      Set target = 9 and call binarysearch(arr, target)
      
      Check result and display appropriate message
    
    End the program

Key Characteristics:

Demonstrates importance of sorting for efficient searching

Shows class-based implementation of algorithms

Highlights the O(n²) time complexity of Bubble Sort

Illustrates O(log n) efficiency of Binary Search on sorted data

# 2. Quick Sort

Algorithm:

    Start the program
    
    Include necessary headers and using namespace std
    
    Define partition() function:
    
      Takes vector reference, low and high indices
      
      Select pivot = arr[high] (last element)
      
      Initialize i = low - 1 (index of smaller element)
      
      Loop j from low to high-1:
    
        If arr[j] < pivot:
    
          Increment i
          
          Swap arr[i] and arr[j]
          
        Swap arr[i+1] and arr[high]
    
    Return i + 1 (pivot position)
    
    Define quickSort() function:
    
      Takes vector reference, low and high indices
      
      If low < high:
    
        Get pivot index pi = partition(arr, low, high)
        
        Recursively call quickSort(arr, low, pi-1)
        
        Recursively call quickSort(arr, pi+1, high)
    
    In main() function:
    
      Initialize vector arr = {10, 7, 8, 9, 1, 5}
      
      Get size n = arr.size()
      
      Call quickSort(arr, 0, n-1)
      
      Display sorted array using for loop
    
    End the program

Key Characteristics:

Demonstrates divide and conquer strategy

Shows recursive implementation

Highlights average case O(n log n) efficiency

Illustrates in-place sorting with O(log n) space complexity

# 3. Selection Sort

Algorithm:

    Start the program
    
    Include necessary headers and using namespace std
    
    Define selectionSort() function:
    
      Takes vector reference
      
      Get size n = arr.size()
      
      Outer loop i from 0 to n-2:
    
        Set min_idx = i
        
        Inner loop j from i+1 to n-1:
    
          If arr[j] < arr[min_idx], set min_idx = j
    
        Swap arr[i] and arr[min_idx]
    
    In main() function:
    
      Initialize vector arr = {10, 7, 8, 9, 1, 5}
      
      Get size n = arr.size()
      
      Call selectionSort(arr)
      
      Display sorted array using for loop
    
    End the program

Key Characteristics:

Demonstrates selection-based sorting approach

Shows O(n²) time complexity in all cases

Illustrates minimal swapping (only n-1 swaps)

Highlights unstable nature of the algorithm

# Conclusion

This experiment successfully demonstrated the implementation and working of three fundamental sorting algorithms:

    Bubble Sort: Simple but inefficient algorithm suitable for small datasets or educational purposes. Its integration with binary search showed how sorting enables efficient searching operations.
    
    Selection Sort: Consistently O(n²) algorithm that performs minimal swaps, making it useful when write operations are costly.
    
    Quick Sort: Efficient divide-and-conquer algorithm with O(n log n) average case performance, making it suitable for large datasets despite its O(n²) worst-case scenario.

Through these implementations, we observed the trade-offs between algorithm simplicity, time complexity, and practical efficiency. The experiment highlighted that:

    Different sorting algorithms serve different use cases
    
    Time and space complexity considerations are crucial in algorithm selection
    
    Sorted data enables efficient operations like binary search
    
    Understanding underlying principles helps in choosing the right algorithm for specific applications

