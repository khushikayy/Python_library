# 🔢 NumPy Library Guide

![Python](https://img.shields.io/badge/Python-3.9%2B-blue)
![NumPy](https://img.shields.io/badge/NumPy-Latest-brightgreen)
![License](https://img.shields.io/badge/License-MIT-yellow)

## 📖 Overview

**NumPy (Numerical Python)** is the fundamental library for numerical computing in Python. It provides powerful support for multi-dimensional arrays, matrices, and a large collection of mathematical functions that enable efficient scientific computing.

NumPy is the foundation of many popular Python libraries such as **Pandas**, **SciPy**, **Scikit-learn**, **TensorFlow**, **PyTorch**, and **Matplotlib**.

It is widely used in:

- Scientific Computing
- Data Science
- Machine Learning
- Artificial Intelligence
- Image Processing
- Signal Processing
- Financial Analysis
- Engineering Simulations
- Research and Development

---

# ✨ Features

- Fast multi-dimensional arrays (`ndarray`)
- Vectorized operations
- Broadcasting
- Advanced indexing and slicing
- Mathematical and statistical functions
- Linear algebra operations
- Random number generation
- Fourier transforms
- Array reshaping and manipulation
- File input and output
- Integration with C/C++ and Fortran

---

# 📦 Installation

## Install using pip

```bash
pip install numpy
```

## Install using conda

```bash
conda install numpy
```

## Verify Installation

```python
import numpy as np

print(np.__version__)
```

---

# 📚 Requirements

- Python 3.9 or higher
- pip or conda package manager

Recommended Libraries

```
matplotlib
pandas
scipy
scikit-learn
jupyter
```

Install recommended packages

```bash
pip install matplotlib pandas scipy scikit-learn jupyter
```

---

# 🚀 Quick Start

Import NumPy

```python
import numpy as np
```

Create an Array

```python
arr = np.array([1,2,3,4,5])

print(arr)
```

Display Shape

```python
print(arr.shape)
```

Display Data Type

```python
print(arr.dtype)
```

---

# 📌 Creating Arrays

1D Array

```python
arr = np.array([1,2,3])
```

2D Array

```python
arr = np.array([
    [1,2,3],
    [4,5,6]
])
```

Zeros

```python
np.zeros((3,3))
```

Ones

```python
np.ones((2,4))
```

Identity Matrix

```python
np.eye(4)
```

Random Values

```python
np.random.rand(3,3)
```

Random Integers

```python
np.random.randint(
    1,
    100,
    size=(5,5)
)
```

Evenly Spaced Values

```python
np.arange(0,20,2)
```

Linear Space

```python
np.linspace(0,10,5)
```

---

# 🔍 Array Attributes

```python
arr.shape  
arr.ndim  
arr.size  
arr.dtype  
arr.itemsize  
```

---

# 🎯 Indexing and Slicing

Access Elements

```python
arr[0]
```

2D Arrays

```python
matrix[1][2]
```

or

```python
matrix[1,2]
```

Slice Arrays

```python
arr[2:8]
```

2D Slice

```python
matrix[0:2,1:3]
```

Negative Indexing

```python
arr[-1]
```

---

# ➕ Array Operations

Addition

```python
a + b
```

Subtraction

```python
a - b
```

Multiplication

```python
a * b
```

Division

```python
a / b
```

Power

```python
a ** 2
```

Square Root

```python
np.sqrt(a)
```

Exponential

```python
np.exp(a)
```

Logarithm

```python
np.log(a)
```

---

# 📐 Reshaping Arrays

```python
arr.reshape(2,3)
```

Flatten

```python
arr.flatten()
```

Ravel

```python
arr.ravel()
```

Transpose

```python
arr.T
```

---

# 🔄 Combining Arrays

Vertical Stack

```python
np.vstack((a,b))
```

Horizontal Stack

```python
np.hstack((a,b))
```

Concatenate

```python
np.concatenate((a,b))
```

Split Arrays

```python
np.split(arr,3)
```

---

# 📊 Mathematical Functions

```python
np.sum(arr)  
np.mean(arr)  
np.median(arr)  
np.std(arr)  
np.var(arr)  
np.min(arr)  
np.max(arr)  
np.argmin(arr)  
np.argmax(arr)  
```

---

# 📈 Statistical Operations

```python
np.percentile(arr,50)  
np.quantile(arr,0.75)  
np.cumsum(arr)  
np.cumprod(arr)  
```

---

# 📚 Linear Algebra

Matrix Multiplication

```python
A @ B
```

or

```python
np.dot(A,B)
```

Inverse

```python
np.linalg.inv(A)
```

Determinant

```python
np.linalg.det(A)
```

Eigenvalues

```python
np.linalg.eig(A)
```

Solve Linear Equations

```python
np.linalg.solve(A,B)
```

---

# 🎲 Random Module

Random Number

```python
np.random.rand()
```

Random Integers

```python
np.random.randint(1,10,5)
```

Normal Distribution

```python
np.random.normal(0, 1, 1000)
```

Shuffle

```python
np.random.shuffle(arr)
```

Random Choice

```python
np.random.choice(arr)
```

Set Seed

```python
np.random.seed(42)
```

---

# 📂 File Operations

Save Array

```python
np.save("array.npy",arr)
```

Load Array

```python
np.load("array.npy")
```

Save Text

```python
np.savetxt("array.txt", arr)
```

Load Text

```python
np.loadtxt("array.txt")
```

---

# 📊 Broadcasting

```python
arr = np.array([1,2,3])

arr + 5
```

Output

```
[6 7 8]
```

Example

```python
matrix = np.array([
    [1,2,3],
    [4,5,6]
])

matrix + np.array([1,2,3])
```

---

# 🔁 Boolean Indexing

```python
arr[arr > 10]
```

Multiple Conditions

```python
arr[(arr > 10) & (arr < 50)]
```

---

# 📈 Performance Example

Without NumPy

```python
result = []

for i in range(1000000):
    result.append(i * 2)
```

With NumPy

```python
arr = np.arange(1000000)

result = arr * 2
```

NumPy performs operations much faster because it uses optimized C implementations and vectorized computations.

---

# 📚 Common NumPy Functions

| Function | Description |
|----------|-------------|
| array() | Create array |
| zeros() | Array of zeros |
| ones() | Array of ones |
| eye() | Identity matrix |
| arange() | Evenly spaced values |
| linspace() | Linear spacing |
| reshape() | Change shape |
| flatten() | Convert to 1D |
| concatenate() | Combine arrays |
| sum() | Sum of elements |
| mean() | Average |
| std() | Standard deviation |
| var() | Variance |
| dot() | Dot product |
| transpose() | Matrix transpose |
| random.rand() | Random floats |
| random.randint() | Random integers |
| save() | Save array |
| load() | Load array |

---

# ⚡ Best Practices

- Use vectorized operations instead of loops.
- Prefer broadcasting over manual iteration.
- Avoid unnecessary copies of arrays.
- Use appropriate data types to reduce memory usage.
- Utilize NumPy's built-in mathematical functions.
- Set random seeds for reproducible results.
- Use `np.where()` for efficient conditional operations.

---

# 🧪 Example Project

```python
import numpy as np

scores = np.array([ 78, 85, 90, 66, 95, 88, 74 ])

print("Scores:")
print(scores)

print("Average:", np.mean(scores))
print("Highest:", np.max(scores))
print("Lowest:", np.min(scores))

above_average = scores[
    scores > np.mean(scores)
]

print("Above Average:")
print(above_average)

normalized = (
    scores - np.mean(scores)
) / np.std(scores)

print("Normalized Scores:")
print(normalized)
```

---

# 🔥 Real-World Applications

- Numerical simulations
- Scientific computing
- Deep Learning
- Machine Learning
- Financial modeling
- Weather forecasting
- Image processing
- Robotics
- Medical imaging
- Computer vision
- Signal processing
- Data preprocessing

---

# 📖 Official Documentation

- https://numpy.org/
- https://numpy.org/doc/

---

# 👨‍💻 Acknowledgements

- NumPy Developers
- Python Software Foundation
- Scientific Python Community

---

## ⭐ Support

If you found this project helpful:

- ⭐ Star the repository
- 🍴 Fork the repository
- 🐞 Report bugs
- 💡 Suggest new features
- 📢 Share it with others

Happy Coding! 🚀