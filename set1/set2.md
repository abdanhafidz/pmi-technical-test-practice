# 2D Array Operations — Technical Test Practice

These problems cover four fundamental topics: **array rotation, translation, reflection, and matrix multiplication**. They are designed for technical interview and coding assessment practice, with difficulty increasing progressively.

## General Instructions

- Implement your solution using Python, C++, Java, or another programming language.
- Do not use specialized libraries for matrix transformations or matrix multiplication.
- Follow the specified input and output formats.
- For translation, elements moved outside the matrix boundaries are discarded, and empty cells are filled with `0`.

---

## Part A — Array Rotation

### 1. Rotate Matrix 90° Clockwise

**Difficulty:** Easy

Given an `N × N` matrix, rotate it 90 degrees clockwise.

**Input**
```text
3
1 2 3
4 5 6
7 8 9
```

**Output**
```text
7 4 1
8 5 2
9 6 3
```

**Constraints:** `1 ≤ N ≤ 100`

### 2. Rotate Matrix by K Degrees

**Difficulty:** Medium

Given an `N × N` matrix and an integer `K`, rotate the matrix clockwise by `K` degrees. The value of `K` is guaranteed to be a multiple of 90.

**Input**
```text
2 270
1 2
3 4
```

**Output**
```text
2 4
1 3
```

**Constraints:** `1 ≤ N ≤ 100`, `0 ≤ K ≤ 10⁹`, and `K mod 90 = 0`.

**Challenge:** Optimize the solution by reducing the rotation angle before performing the transformation.

### 3. Rotate a Rectangular Matrix

**Difficulty:** Medium

Given an `N × M` matrix, rotate it 90 degrees counterclockwise. The resulting matrix will have dimensions `M × N`.

**Input**
```text
2 3
1 2 3
4 5 6
```

**Output**
```text
3 6
2 5
1 4
```

**Constraints:** `1 ≤ N, M ≤ 100`

---

## Part B — Array Translation

For the following problems, elements that move outside the matrix boundaries are discarded. Empty cells are filled with zeros unless otherwise specified.

### 4. Shift Matrix to the Right

**Difficulty:** Easy

Given an `N × M` matrix, shift every element one position to the right. Elements that move outside the matrix are discarded, and the leftmost column is filled with zeros.

**Input**
```text
3 3
1 2 3
4 5 6
7 8 9
```

**Output**
```text
0 1 2
0 4 5
0 7 8
```

**Constraints:** `1 ≤ N, M ≤ 100`

### 5. Translate Matrix by (dx, dy)

**Difficulty:** Medium

Given an `N × M` matrix and two integers, `dx` and `dy`, translate each element horizontally by `dx` positions and vertically by `dy` positions.

- Positive `dx` moves elements right, while negative `dx` moves them left.
- Positive `dy` moves elements down, while negative `dy` moves them up.
- Elements outside the matrix are discarded, and empty cells are filled with zeros.

**Input**
```text
3 3
1 2 3
4 5 6
7 8 9
1 -1
```

**Output**
```text
4 5 6
7 8 9
0 0 0
```

**Constraints:** `1 ≤ N, M ≤ 100`, `-100 ≤ dx, dy ≤ 100`.

### 6. Circular Matrix Shift

**Difficulty:** Medium

Given an `N × M` matrix, perform a circular shift of all elements by `K` positions to the right. Treat the matrix as a single row-major sequence: the last element of each row is followed by the first element of the next row.

**Input**
```text
2 3 2
1 2 3
4 5 6
```

**Output**
```text
5 6 1
2 3 4
```

**Constraints:** `1 ≤ N, M ≤ 100`, `0 ≤ K ≤ 10⁹`.

**Challenge:** Handle shifts larger than the total number of elements efficiently.

---

## Part C — Array Reflection

### 7. Horizontal and Vertical Reflection

**Difficulty:** Easy

Given an `N × M` matrix, reflect it across a horizontal axis or a vertical axis, according to the given operation.

- `H`: Reverse the order of rows.
- `V`: Reverse the order of columns.

**Input**
```text
3 3 H
1 2 3
4 5 6
7 8 9
```

**Output**
```text
7 8 9
4 5 6
1 2 3
```

**Constraints:** `1 ≤ N, M ≤ 100`

### 8. Reflection Across the Main Diagonal

**Difficulty:** Medium

Given an `N × N` matrix, reflect the matrix across its main diagonal, swapping each element at position `(i, j)` with the element at `(j, i)`.

**Input**
```text
3
1 2 3
4 5 6
7 8 9
```

**Output**
```text
1 4 7
2 5 8
3 6 9
```

**Constraints:** `1 ≤ N ≤ 100`

**Challenge:** Try implementing the transformation in place, without creating another matrix.

### 9. Reflection Across the Anti-Diagonal

**Difficulty:** Hard

Given an `N × N` matrix, reflect it across the anti-diagonal, which runs from the top-right corner to the bottom-left corner.

**Input**
```text
3
1 2 3
4 5 6
7 8 9
```

**Output**
```text
9 6 3
8 5 2
7 4 1
```

**Constraints:** `1 ≤ N ≤ 100`

**Challenge:** Derive a direct mapping from each original coordinate `(i, j)` to its reflected coordinate.

---

## Part D — Matrix Multiplication

### 10. Standard Matrix Multiplication

**Difficulty:** Easy

Given two matrices `A` and `B`, compute their product:

`C = A × B`

Matrix `A` has dimensions `N × M`, and matrix `B` has dimensions `M × P`. The resulting matrix `C` must have dimensions `N × P`.

Each element is computed using the dot product of a row from `A` and a column from `B`.

**Input**
```text
2 3 2
1 2 3
4 5 6
7 8
9 10
11 12
```

**Output**
```text
58 64
139 154
```

**Constraints:** `1 ≤ N, M, P ≤ 100`, `-100 ≤ A[i][j], B[i][j] ≤ 100`.

**Challenge:** Implement matrix multiplication using three nested loops and analyze its time complexity.

### 11. Matrix Multiplication with Transposition

**Difficulty:** Hard

Given two matrices `A` and `B`, compute:

`C = A × Bᵀ`

Here, `Bᵀ` is the transpose of matrix `B`. You must compute the result **without explicitly constructing the transposed matrix**.

The first line contains `N`, `M`, and `P`. Matrix `A` has dimensions `N × M`, and matrix `B` has dimensions `P × M`.

**Input**
```text
2 3 2
1 2 3
4 5 6
7 8 9
10 11 12
```

**Output**
```text
50 68
122 167
```

**Constraints:** `1 ≤ N, M, P ≤ 100`, `-100 ≤ A[i][j], B[i][j] ≤ 100`.

**Challenge:** Adapt the indexing of the multiplication algorithm so that each row of `A` is multiplied by each row of `B`.

---

## Recommended Practice Order

| Level | Problems | Main Concept |
|---|---|---|
| Beginner | 1, 4, 7, 10 | Basic index manipulation |
| Intermediate | 2, 3, 5, 6, 8 | Coordinate mapping |
| Advanced | 9, 11 | Diagonal transformations and optimized indexing |

## Final Challenge

For each problem:

1. Implement a straightforward solution.
2. Analyze its time and space complexity.
3. Test edge cases, including minimum dimensions, negative translations, and rotations greater than 360 degrees.
4. Where possible, optimize the solution to work in place without allocating another matrix.
