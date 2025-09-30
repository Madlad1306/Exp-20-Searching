## Theory: Searching in C++

**Searching** is the process of finding the location of a specific element (key) within a dataset such as an array, linked list, or database. Searching is fundamental in programming and data management, as efficient searching improves program performance, especially for large datasets.

### 1. Types of Searching Algorithms

Searching algorithms are broadly classified into **linear (sequential) searches** and **optimized searches** for sorted data.

---

### 1️⃣ Linear Search (Sequential Search)

* Examines each element in the dataset one by one until the target element is found.
* Works on **unsorted arrays**.
* **Algorithm Steps:**

  1. Start from the first element.
  2. Compare each element with the key.
  3. If a match is found, return the index.
  4. If end of array is reached without a match, return -1.
* **Time Complexity:** O(n)
* **Space Complexity:** O(1)
* **Pros:** Simple, works on unsorted arrays.
* **Cons:** Inefficient for large datasets.

---

### 2️⃣ Binary Search

* Efficient searching technique for **sorted arrays**.
* Divides the array into halves repeatedly, reducing the search space exponentially.
* **Algorithm Steps:**

  1. Initialize `low = 0`, `high = size - 1`.
  2. Calculate middle index: `mid = (low + high) / 2`.
  3. If `arr[mid] == key`, return `mid`.
  4. If `arr[mid] < key`, search right half (`low = mid + 1`).
  5. If `arr[mid] > key`, search left half (`high = mid - 1`).
  6. Repeat until `low > high`. Return -1 if not found.
* **Time Complexity:** O(log n)
* **Space Complexity:** O(1) (iterative), O(log n) (recursive)
* **Pros:** Fast and efficient.
* **Cons:** Requires sorted data.

---

### 3️⃣ Interpolation Search

* Best suited for **uniformly distributed sorted arrays**.
* Estimates the probable position of the key using a linear formula instead of always dividing in half.
* **Time Complexity:** O(log log n) best case, O(n) worst case
* **Space Complexity:** O(1)
* **Pros:** Faster than binary search for large, uniform datasets.
* **Cons:** Less efficient for non-uniform distributions.

---

### 4️⃣ Exponential Search

* Designed for **unbounded or infinite lists**.
* Steps:

  1. Find a range where the element may exist by repeatedly doubling the index.
  2. Apply binary search within that range.
* **Time Complexity:** O(log n)
* **Space Complexity:** O(1)
* **Pros:** Handles unbounded lists.
* **Cons:** Requires sorted data.

---

### 5️⃣ Jump Search

* Divides the array into **blocks of fixed size**, then performs linear search within the block.
* Optimal step size = √n.
* **Time Complexity:** O(√n)
* **Space Complexity:** O(1)
* **Pros:** Reduces number of comparisons compared to linear search.
* **Cons:** Requires sorted array.

---

### 6️⃣ Comparison Table of Searching Algorithms

| Algorithm            | Best Case | Worst Case | Space Complexity | Data Requirement |
| -------------------- | --------- | ---------- | ---------------- | ---------------- |
| Linear Search        | O(1)      | O(n)       | O(1)             | Sorted/Unsorted  |
| Binary Search        | O(1)      | O(log n)   | O(1)             | Sorted           |
| Interpolation Search | O(1)      | O(n)       | O(1)             | Sorted, Uniform  |
| Jump Search          | O(√n)     | O(√n)      | O(1)             | Sorted           |
| Exponential Search   | O(log n)  | O(log n)   | O(1)             | Sorted           |

---

### 7️⃣ Summary

* **Linear and Sequential Search**: Simple, works on unsorted arrays, but slower for large datasets.
* **Binary Search**: Much faster, requires sorted arrays.
* **Interpolation and Jump Search**: Optimized for sorted arrays, reduce comparisons.
* **Exponential Search**: Efficient for unbounded lists.

Choosing the right searching algorithm depends on:

1. **Data size** (small vs large dataset).
2. **Data order** (sorted vs unsorted).
3. **Memory and time constraints**.

Do you want me to do that?
