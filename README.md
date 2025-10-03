# Experiment-21

##  AIM
The aim of this project is to implement and understand different **sorting algorithms** in C++ using arrays. Sorting is a fundamental operation in computer science and data processing, used to arrange data in a specific order (usually ascending or descending).  

This project demonstrates:  
1. **Selection Sort** – Repeatedly finding the minimum element and placing it at the correct position.  
2. **Bubble Sort** – Repeatedly swapping adjacent elements if they are in the wrong order.  
3. **Quick Sort** – A divide-and-conquer approach for efficiently sorting large datasets.  



##  THEORY

### 1. Introduction to Sorting
**Sorting** is the process of arranging data in a particular sequence, typically **ascending or descending order**. Sorted data improves the efficiency of searching, merging, and analysis operations.  

Sorting algorithms are classified broadly as:  
- **Simple or Elementary Sorts**: Bubble Sort, Selection Sort, Insertion Sort.  
- **Efficient/Advanced Sorts**: Quick Sort, Merge Sort, Heap Sort.  
- **Specialized Sorts**: Counting Sort, Radix Sort, Bucket Sort.  

Sorting is critical in database management, report generation, computer graphics, and scientific computing.



### 2. Selection Sort
- **Principle**: Repeatedly find the minimum element from the unsorted portion and move it to the beginning.  
- **Steps**: Scan the array, locate the smallest element, swap it with the first unsorted element, repeat for remaining elements.  
- **Characteristics**:  
  - Simple and easy to implement.  
  - Does **n-1** passes for an array of size n.  
- **Time Complexity**: O(n²) in all cases.  
- **Space Complexity**: O(1) (in-place sort).  
- **Best Use**: Small datasets where simplicity is preferred over efficiency.  



### 3. Bubble Sort
- **Principle**: Repeatedly compare adjacent elements and swap if they are in the wrong order, “bubbling” larger elements to the end.  
- **Steps**: For each pass, compare `arr[j]` and `arr[j+1]`, swap if needed. Repeat until the array is sorted.  
- **Characteristics**:  
  - Very simple algorithm.  
  - Each pass guarantees the largest element is placed correctly.  
- **Time Complexity**:  
  - Best Case (already sorted): O(n) with optimized version.  
  - Average/Worst Case: O(n²).  
- **Space Complexity**: O(1) (in-place).  
- **Best Use**: Small arrays; educational purposes for algorithm learning.  



### 4. Quick Sort
- **Principle**: Divide-and-conquer. Pick a **pivot element**, partition the array into elements less than pivot and greater than pivot, then recursively sort subarrays.  
- **Steps**:  
  1. Select a pivot (commonly last element).  
  2. Rearrange elements: smaller left, larger right.  
  3. Recursively sort left and right partitions.  
- **Characteristics**:  
  - Highly efficient for large datasets.  
  - Average Time Complexity: O(n log n).  
  - Worst Case: O(n²) (when array is already sorted or pivot poorly chosen).  
  - Space Complexity: O(log n) (due to recursion stack).  
- **Best Use**: Large datasets where efficiency is required.  



### 5. Comparison of Algorithms

| Feature             | Selection Sort  | Bubble Sort      | Quick Sort         |
|---------------------|----------------|----------------|------------------|
| Time Complexity     | O(n²)          | O(n²)           | O(n log n) average|
| Space Complexity    | O(1)           | O(1)            | O(log n)          |
| Stability           | No             | Yes             | No                |
| In-place            | Yes            | Yes             | Yes               |
| Efficiency          | Low            | Low             | High              |
| Best Case           | O(n²)          | O(n) (optimized)| O(n log n)        |
| Worst Case          | O(n²)          | O(n²)           | O(n²)             |
| Use Case            | Small arrays   | Small/educational| Large arrays      |



### 6. Real-Life Applications
1. Sorting student grades, product prices, or scores.  
2. Organizing inventory in ascending order of IDs or quantities.  
3. Quick Sort is widely used in **standard library functions** like `std::sort()` in C++.  
4. Sorting is fundamental for search algorithms, database indexing, and scheduling tasks.  



##  ALGORITHM

### 1. Selection Sort
**Steps**:  
1. Start from the first element (i = 0).  
2. Find the minimum element in the unsorted portion.  
3. Swap the minimum element with `arr[i]`.  
4. Increment i and repeat until the array is sorted.  




### 2. Bubble Sort
**Steps**:  
1. Repeat n-1 passes.  
2. For each pass, compare adjacent elements `arr[j]` and `arr[j+1]`.  
3. Swap if `arr[j] > arr[j+1]`.  
4. After each pass, largest unsorted element is moved to the correct position.  




### 3. Quick Sort
**Steps**:  
1. Select a pivot element.  
2. Partition array into two parts: elements smaller than pivot and elements greater than pivot.  
3. Recursively apply Quick Sort to left and right subarrays.  





##  CONCLUSION

This project successfully demonstrates **three fundamental sorting algorithms**—Selection Sort, Bubble Sort, and Quick Sort—and highlights their working mechanisms, efficiency, and real-world relevance. Through these implementations, several key insights were gained.

### 1. Understanding Sorting Mechanics
- **Selection Sort**: Emphasizes scanning and selecting the minimum element repeatedly. Its simplicity makes it a good starting point for beginners.  
- **Bubble Sort**: Demonstrates iterative comparison and adjacent swapping. It also helps understand the concept of stable sorting.  
- **Quick Sort**: Introduces the divide-and-conquer paradigm and recursion, showing how large datasets can be efficiently organized.  

### 2. Efficiency Considerations
- Both Selection and Bubble Sort have **O(n²)** time complexity, which becomes impractical for large datasets.  
- Quick Sort, with average **O(n log n)** time complexity, efficiently handles large data and is widely used in industry.  
- Recursive algorithms like Quick Sort require additional stack memory, highlighting a trade-off between **speed** and **space**.

### 3. Stability and In-Place Sorting
- Bubble Sort is stable (preserves relative order), which is important when sorting complex data structures.  
- Quick Sort is not stable, but it is highly efficient.  
- All three algorithms are **in-place**, meaning they do not require additional memory for arrays, which is a significant advantage in memory-limited environments.

### 4. Real-Life Relevance
Sorting is not just an academic exercise—it is applied in:  
- Organizing files and records.  
- Search optimization (sorted data enables binary search).  
- Database indexing and retrieval.  
- Scheduling and priority-based systems.  

### 5. Conceptual Learning
By implementing these algorithms, the following were reinforced:  
- Algorithmic thinking: Breaking problems into stepwise logical procedures.  
- Time and space analysis: Evaluating which algorithm suits which scenario.  
- Recursion: Understanding divide-and-conquer logic in Quick Sort.  
- Trade-offs: Learning the balance between simplicity and efficiency.  
