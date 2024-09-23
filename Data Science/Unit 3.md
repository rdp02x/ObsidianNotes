### 3.1 Introduction to NumPy

- **NumPy (Numerical Python)** is an open source Python library widely used in science and engineering.
- It offers a multidimensional array object with outstanding capabilities and speed for interacting with these arrays.

**Why Use NumPy?**
1. **Faster Execution:** NumPy arrays are optimized for complex mathematical and statistical operations. Operations on NumPy arrays are up to 50x faster than iterating over native Python lists using loops.
2. **Compatibility with Various Libraries:** NumPy works with libraries like Pandas, SciPy, scikit-learn, etc.

**Installing and Importing NumPy in Python:**
- **Installing NumPy:**
  - Install NumPy using `conda install numpy` or `pip install numpy` if you already have Python.
  - Use Anaconda for a simpler start if Python is not installed.
  - Run `pip install numpy` in the command prompt or terminal to download and install the latest version of NumPy from PyPI.

- **Importing NumPy:**
  - Import NumPy in Python as `np`.
  - It’s a common convention to improve readability: `import numpy as np`.

**NumPy Array Operations and Methods:**
1. **Creating One-Dimensional Arrays:**
   ```python
   import numpy as np
   array = np.arange(20)

   - Output: `array([0, 1, 2, ..., 19])`
   - Check dimensions with `array.shape`.

2. **Creating Two-Dimensional Arrays:**
   ```python
   array = np.arange(20).reshape(4, 5)
   ```
   - Output: `array([[0, 1, 2, 3, 4], [5, 6, 7, 8, 9], [10, 11, 12, 13, 14], [15, 16, 17, 18, 19]])`

3. **Other NumPy Functions:**
   - `np.empty((2,3))`
   - `np.full((2,2), 3)`
     - Output: `array([[3, 3], [3, 3]])`
   - `np.eye(3,3)`
     - Output: `array([[1., 0., 0.], [0., 1., 0.], [0., 0., 1.]])`
   - `np.linspace(0, 10, num=4)`
     - Output: `array([0., 3.33333333, 6.66666667, 10.])`

**Questions:**
1. Explain the following NumPy array functions with examples:
   - `empty_like()`
   - `ones_like()`
   - `zeros_like()`
   - `full_like()`
   - `asarray()`
   - `geomspace()`
   - `copy()`
   - `diag()`
   - `frombuffer()`
   - `fromfile()`
   - `bmat()`
   - `mat()`
   - `vander()`
   - `triu()`
   - `tril()`
   - `tri()`
   - `diagflat()`
   - `fromfunction()`
   - `logspace()`
   - `meshgrid()`

### 3.2 Activity - Sequence it Right

**Sequence in Python using NumPy:**
- The `sort()` method sorts an array in ascending order.
- Syntax: `numpy.sort(arr, axis=-1, kind=None, order=None)`

**Parameters:**
1. **arr:** Input array to sort.
2. **axis:** Axis along which sorting is performed. Default is `-1` (last axis).
3. **order:** Specifies fields to compare first if array is structured.
4. **kind:** Sorting algorithm. Default is 'quicksort'. Other options: 'mergesort', 'heapsort'.

**How to Get a Sorted NumPy Array (Ascending Order):**
```python
arr[::-1].sort()
```
- This sorts the array in ascending order and then reverses it to descending.

**Class Assessment:**
1. How do I sort a 2D NumPy array along a specific axis?
2. Can a NumPy array be sorted in descending order?
3. How to sort a 2D NumPy array along a specific axis?
4. Can we sort a NumPy array of strings?
5. Does `numpy.sort()` modify the original array?

**Program to Get a Sorted NumPy Array (Ascending Order):**
```python
import numpy as np
arr = np.array([3, 1, 2])
sorted_arr = np.sort(arr)
print(sorted_arr)
```

### 3.3 Demo 01 - Creating and Printing an Array

```python
import numpy as np

# Creating a 1D array
arr_1d = np.array([1, 2, 3, 4, 5])

# Creating an array with a range of values
range_array = np.arange(0, 10, 2)

# Creating a 2D array
arr_2d = np.array([[1, 2, 3], [4, 5, 6]])

# Creating an array with evenly spaced values
linspace_array = np.linspace(0, 1, 5)

# Creating an array of zeros
zeros = np.zeros((3, 3))

# Creating an array of ones
ones = np.ones((2, 4))

print(arr_1d)
print(arr_2d)
print(zeros)
print(ones)
print(range_array)
print(linspace_array)
```

### 3.4 Class and Attributes of an Array

**Class of Array:**
- NumPy's array class is `ndarray`.
- `ndarray` - N-dimensional array.
- Also known by the alias `array`.
- A fixed-sized array in memory with data of the same type (e.g., integers or floating-point values).

**Attributes of Array:**
- **ndim:** Number of dimensions.
- **size:** Number of elements.
- **dtype:** Data type of elements.
- **shape:** Size of the array in each dimension.
- **itemsize:** Size (in bytes) of each element.
- **data:** Buffer containing actual elements.

**Example:**
```python
import numpy as np
array1 = np.array([[1, 2, 3], [6, 7, 8]])

print("Array is of type:", type(array1))
print("Shape of array:", array1.shape)
print("No. of dimensions:", array1.ndim)
print("Size of array:", array1.size)
print("Array stores elements of type:", array1.dtype)
print("Data of array1 is:", array1.data)
```

### 3.5 Basic Operations

**1. Element-wise Operations:**
- NumPy arrays allow element-wise operations, which perform operations like addition, subtraction, etc., on each element.

**2. Mathematical Functions:**
- **Trigonometric Functions:**
  - `np.sin(data)`
  - `np.cos(data)`
  - `np.tan(data)`
  - `np.arcsin(data)`
  - `np.arccos(data)`
  - `np.arctan(data)`
  - `np.degrees(data)`
  - `np.radians(data)`

- **Arithmetic Operations:**
  - Addition: `np.add(d1, d2)`
  - Subtraction: `np.subtract(d1, d2)`
  - Multiplication: `np.multiply(d1, d2)`
  - Division: `np.divide(d1, d2)`
  - Exponentiation: `np.power(d1, d2)`
  - Modulus: `np.mod(d1, d2)`

- **Rounding Functions:**
  - `np.round(d1, 2)`
  - `np.floor(d1)`
  - `np.ceil(d1)`

**3. Array Manipulations:**
- **Creating Arrays:** Covered earlier.
- **Reshaping Arrays:** Covered earlier.
- **Concatenating Arrays:**
  ```python
  arr1 = np.array([1, 2, 3])
  arr2 = np.array([4, 5, 6])
  concatenated_arr = np.concatenate((arr1, arr2))
  ```

- **Adding/Removing Elements:**
  - Adding: `np.append(arr, [4, 5])`
  - Removing: `np.delete(arr, [0, 2])`

### 3.6 Activity - Slicing it

**Numpy Array Slicing:**
- Slicing extracts a range of elements from an array.
- Slicing is performed similarly to Python lists.

**Types of Indexing:**
1. **Field Access:** Direct access using index.
2. **Basic Slicing:** `array[start:end:step]`
3. **Advanced Indexing:** Uses arrays of indices or boolean arrays.

**Basic Slicing Example:**
```python
import numpy as np
a

 = np.arange(10)
s = slice(2, 7, 2)
print(a[s])  # Output: [2 4 6]
```

**Single Item Slicing Example:**
```python
import numpy as np
a = np.arange(15)
b = a[7]
print(b)  # Output: 7
```

### 3.7 Mathematical Functions of NumPy

- NumPy supports various mathematical operations and functions for data analysis and scientific computations.
- Includes functions for algebraic, statistical, and trigonometric computations.

**Common Functions:**
- **Algebraic Operations:**
  - `np.add()`, `np.subtract()`, `np.multiply()`, `np.divide()`
- **Statistical Operations:**
  - `np.mean()`, `np.median()`, `np.std()`, `np.var()`
- **Trigonometric Functions:**
  - `np.sin()`, `np.cos()`, `np.tan()`

**Example of Using Mathematical Functions:**
```python
import numpy as np
data = np.array([0, 1, 2])
Sine_data = np.sin(data)
```
