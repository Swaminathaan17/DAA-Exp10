## Objective

The objective of this program is to compare the performance of **Deterministic Quick Sort (DQS)** and **Randomized Quick Sort (RQS)** on different types of input data. The comparison is based on:

* Number of element comparisons performed
* Execution time (in milliseconds)

The experiment demonstrates how randomizing the pivot selection can significantly reduce the chances of encountering Quick Sort's worst-case behavior.

---

## Theory

### Deterministic Quick Sort

In Deterministic Quick Sort, the pivot is selected using a fixed strategy. In this implementation, the **last element** of the array is always chosen as the pivot.

* Average Time Complexity: **O(n log n)**
* Worst-Case Time Complexity: **O(n²)**
* Worst case occurs when the input is already sorted or reverse sorted.

### Randomized Quick Sort

Randomized Quick Sort selects the pivot randomly before partitioning.

* Expected Time Complexity: **O(n log n)**
* Worst-Case Time Complexity: **O(n²)** (rare)
* Randomization reduces the probability of consistently poor pivot choices.

---

## Features

* Implements Deterministic Quick Sort.
* Implements Randomized Quick Sort.
* Tests the algorithms on:

  * Random data
  * Sorted data
  * Reverse sorted data
  * Nearly sorted data
* Displays results in a formatted comparison table.

---

## Requirements

* Python 3.x

### Modules Used

```python
random
time
sys
```

All required modules are part of Python's standard library.

---

## Input Description

The program automatically generates test arrays of size **5000**.

### Test Cases

1. **Random**

   * Random integers between 1 and 100000.

2. **Sorted**

   * Elements arranged in ascending order.

3. **Reverse**

   * Elements arranged in descending order.

4. **Nearly Sorted**

   * Mostly sorted array with a small number of random swaps.

---

## Output

The program displays a table containing:

* Input Type
* Deterministic Quick Sort Comparisons
* Deterministic Quick Sort Execution Time
* Randomized Quick Sort Comparisons
* Randomized Quick Sort Execution Time

Example:

```text
Input Type          DQS Comps   DQS Time(ms)    RQS Comps   RQS Time(ms)
------------------------------------------------------------------------
Random                 70000          8.21        69000          7.95
Sorted             12497500        450.67        72000          8.34
Reverse            12497500        430.52        71000          8.01
Nearly Sorted        950000         35.44        70000          8.12
```

*Note: Actual values may vary because Randomized Quick Sort uses random pivot selection.*

---

## Algorithm

### Deterministic Quick Sort

1. Choose the last element as the pivot.
2. Partition the array around the pivot.
3. Recursively sort the left partition.
4. Recursively sort the right partition.

### Randomized Quick Sort

1. Select a random element as pivot.
2. Swap it with the last element.
3. Perform partitioning.
4. Recursively sort left and right partitions.

---

## Complexity Analysis

| Algorithm                | Best Case  | Average Case | Worst Case |
| ------------------------ | ---------- | ------------ | ---------- |
| Deterministic Quick Sort | O(n log n) | O(n log n)   | O(n²)      |
| Randomized Quick Sort    | O(n log n) | O(n log n)   | O(n²)      |

### Space Complexity

Both algorithms require:

```text
O(log n)
```

for recursion stack space on average.

---
in practical applications where input characteristics are unknown.
