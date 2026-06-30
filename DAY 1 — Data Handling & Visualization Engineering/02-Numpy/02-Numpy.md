# Array Creation, Shape Engineering, Indexing, and Slicing

In the previous section, we learned that NumPy's power comes from its efficient memory layout and the `ndarray` data structure. Understanding how arrays are stored is important, but as an ML engineer, most of your daily work revolves around creating arrays, manipulating their shapes, selecting specific portions of data, and preparing them for downstream models.

A surprising number of machine learning bugs have nothing to do with algorithms. They happen because the data has the wrong shape, the wrong dimensions, or because an engineer accidentally selected the wrong subset of data.

Learning how to inspect and manipulate array structures is therefore one of the most practical NumPy skills you can develop.

---

## Creating Arrays

Most real-world datasets come from files, databases, APIs, or preprocessing pipelines. However, during experimentation and model development, engineers constantly create arrays manually.

The most fundamental constructor is `np.array()`.

```python
import numpy as np

arr = np.array([1, 2, 3, 4, 5])

print(arr)
```

Output:

```python
[1 2 3 4 5]
```

NumPy automatically converts the Python list into an ndarray.

You can also create multi-dimensional arrays.

```python
matrix = np.array([
    [1, 2, 3],
    [4, 5, 6]
])

print(matrix)
```

Output:

```python
[[1 2 3]
 [4 5 6]]
```

At this point, NumPy has already stored the data as a structured block of contiguous memory.

---

## Common Array Creation Functions

When working in machine learning, you'll rarely create large arrays manually. Instead, you'll use specialized functions that allocate memory efficiently.

### Creating Arrays Filled with Zeros

```python
zeros = np.zeros((3, 4))

print(zeros)
```

Output:

```python
[[0. 0. 0. 0.]
 [0. 0. 0. 0.]
 [0. 0. 0. 0.]]
```

This creates a matrix with:

* 3 rows
* 4 columns

Functions like this are frequently used when initializing neural network parameters.

---

### Creating Arrays Filled with Ones

```python
ones = np.ones((2, 3))

print(ones)
```

Output:

```python
[[1. 1. 1.]
 [1. 1. 1.]]
```

---

### Creating Sequences with arange()

`arange()` behaves similarly to Python's `range()`.

```python
arr = np.arange(10)

print(arr)
```

Output:

```python
[0 1 2 3 4 5 6 7 8 9]
```

With custom intervals:

```python
arr = np.arange(0, 20, 2)

print(arr)
```

Output:

```python
[ 0  2  4  6  8 10 12 14 16 18]
```

This function appears frequently when generating indices, timestamps, and numerical sequences.

---

### Creating Evenly Spaced Values with linspace()

Machine learning often requires evenly distributed values.

```python
values = np.linspace(0, 1, 5)

print(values)
```

Output:

```python
[0.   0.25 0.5  0.75 1.  ]
```

Unlike `arange()`, NumPy automatically calculates the spacing.

This is useful when generating coordinate systems, simulation ranges, and visualization grids.

---

### Creating Identity Matrices

Identity matrices are heavily used in linear algebra.

```python
identity = np.eye(4)

print(identity)
```

Output:

```python
[[1. 0. 0. 0.]
 [0. 1. 0. 0.]
 [0. 0. 1. 0.]
 [0. 0. 0. 1.]]
```

Identity matrices behave like the number 1 in matrix multiplication.

---

## Shape Engineering

One of the most important concepts in machine learning is shape.

Many beginners focus entirely on values:

```python
[1, 2, 3, 4]
```

Experienced ML engineers immediately ask:

> What is the shape?

Because shape determines how data flows through a model.

---

### Understanding Shape

Consider:

```python
x = np.array([1, 2, 3, 4])

print(x.shape)
```

Output:

```python
(4,)
```

This represents a one-dimensional vector.

Now compare:

```python
x = np.array([[1, 2, 3, 4]])

print(x.shape)
```

Output:

```python
(1, 4)
```

And:

```python
x = np.array([
    [1],
    [2],
    [3],
    [4]
])

print(x.shape)
```

Output:

```python
(4, 1)
```

Although the values are identical, the mathematical meaning is completely different.

```text
(4,)   → Vector

(1,4)  → Row Matrix

(4,1)  → Column Matrix
```

Many neural network bugs originate from mixing these structures incorrectly.

---

## Inspecting Shapes

Several attributes help us understand data structure.

```python
arr = np.array([
    [1, 2, 3],
    [4, 5, 6]
])
```

Shape:

```python
print(arr.shape)
```

Output:

```python
(2, 3)
```

Dimensions:

```python
print(arr.ndim)
```

Output:

```python
2
```

Total elements:

```python
print(arr.size)
```

Output:

```python
6
```

These properties are used constantly when debugging ML pipelines.

---

## Reshaping Arrays

Real-world data rarely arrives in the shape required by a model.

NumPy provides tools to reorganize data without changing the values.

---

### reshape()

```python
arr = np.arange(12)

print(arr)
```

Output:

```python
[0 1 2 3 4 5 6 7 8 9 10 11]
```

Convert into a matrix:

```python
matrix = arr.reshape(3, 4)

print(matrix)
```

Output:

```python
[[ 0  1  2  3]
 [ 4  5  6  7]
 [ 8  9 10 11]]
```

The total number of elements must remain unchanged.

```text
12 Elements

3 × 4 = 12 ✓

2 × 6 = 12 ✓

5 × 5 = 25 ✗
```

---

### Automatic Dimension Inference

NumPy can calculate one dimension automatically.

```python
arr.reshape(3, -1)
```

Output:

```python
[[ 0  1  2  3]
 [ 4  5  6  7]
 [ 8  9 10 11]]
```

The `-1` tells NumPy:

> Figure out this dimension yourself.

This feature is extremely common in machine learning code.

---

### Flattening Arrays

Convert a matrix back into a vector.

```python
matrix = np.array([
    [1, 2],
    [3, 4]
])

flat = matrix.flatten()

print(flat)
```

Output:

```python
[1 2 3 4]
```

This is frequently required before feeding data into classical ML models.

---

## Indexing Arrays

Indexing allows access to individual elements.

### One-Dimensional Indexing

```python
arr = np.array([10, 20, 30, 40])

print(arr[0])
```

Output:

```python
10
```

Last element:

```python
print(arr[-1])
```

Output:

```python
40
```

Negative indexing works exactly like Python lists.

---

### Two-Dimensional Indexing

```python
matrix = np.array([
    [10, 20, 30],
    [40, 50, 60]
])
```

Access:

```python
print(matrix[0, 1])
```

Output:

```python
20
```

Interpretation:

```text
matrix[row, column]
```

This syntax is used heavily throughout ML and data science.

---

## Slicing Arrays

Slicing extracts portions of an array.

Consider:

```python
arr = np.array([10, 20, 30, 40, 50])
```

Extract middle elements:

```python
print(arr[1:4])
```

Output:

```python
[20 30 40]
```

The stopping index is excluded.

---

### Matrix Slicing

```python
matrix = np.array([
    [1, 2, 3],
    [4, 5, 6],
    [7, 8, 9]
])
```

First row:

```python
print(matrix[0])
```

Output:

```python
[1 2 3]
```

First column:

```python
print(matrix[:, 0])
```

Output:

```python
[1 4 7]
```

Submatrix:

```python
print(matrix[0:2, 1:3])
```

Output:

```python
[[2 3]
 [5 6]]
```

This style of slicing is one of the most frequently used NumPy operations.

---

## Fancy Indexing

NumPy allows selecting arbitrary elements.

```python
arr = np.array([10, 20, 30, 40, 50])
```

Choose specific positions:

```python
selected = arr[[0, 2, 4]]

print(selected)
```

Output:

```python
[10 30 50]
```

This is called fancy indexing.

It is commonly used when selecting batches of training samples.

---

## Why Shape Engineering Matters in ML

Consider a housing dataset.

```text
1000 Houses
10 Features Per House
```

The correct shape is:

```python
(1000, 10)
```

Meaning:

```text
1000 Samples

10 Features
```

A neural network expects data in a specific format.

If the shape becomes:

```python
(10, 1000)
```

the model interprets:

```text
10 Samples

1000 Features
```

The data now means something completely different.

Understanding shapes is therefore not optional—it is a fundamental machine learning skill.

---

## Industry Insight

Ask an experienced ML engineer what causes the most debugging headaches.

The answer is rarely "the algorithm."

The answer is usually:

* Wrong shapes
* Wrong dimensions
* Incorrect indexing
* Misaligned matrices

Learning to inspect shapes quickly will save countless hours when working with deep learning frameworks later.

---

## Common Misconception

**"If two arrays contain the same numbers, they represent the same thing."**

Not necessarily.

```python
(4,)
```

and

```python
(4,1)
```

contain the same values but represent entirely different mathematical objects.

Shape gives data meaning.

Ignoring shape is one of the fastest ways to create bugs in ML systems.

---

## Quick Revision Notes

* Use `np.array()` to create arrays.
* `zeros()`, `ones()`, `arange()`, and `linspace()` are common creation methods.
* Shape determines how data is interpreted.
* `shape`, `ndim`, and `size` are essential inspection tools.
* `reshape()` changes structure without changing values.
* `flatten()` converts matrices into vectors.
* Indexing accesses individual elements.
* Slicing extracts subsets efficiently.
* Fancy indexing selects arbitrary positions.
* Shape mismatches are one of the most common ML errors.

---

## Interview Questions

1. What is the difference between `(4,)` and `(4,1)`?
2. When would you use `linspace()` instead of `arange()`?
3. What does `reshape(-1, 1)` mean?
4. Why is shape important in machine learning?
5. How do you select the first column of a matrix?
6. What is fancy indexing?
7. What happens if reshape dimensions don't match the total number of elements?
8. What is the difference between indexing and slicing?
9. What does `arr.ndim` return?
10. Why are shape mismatches so common in neural networks?

---

### Section Summary

In this section, we moved from understanding how arrays are stored to learning how to create, inspect, reshape, and manipulate them. These operations form the foundation of nearly every machine learning workflow. Before building models, engineers must be comfortable navigating multidimensional data, understanding shapes, and extracting meaningful subsets efficiently. In the next part, we'll explore boolean masking, vectorization, and broadcasting—the techniques that make NumPy both expressive and incredibly fast.
