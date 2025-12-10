# AI-opener

A small collection of Python examples demonstrating common patterns:
- Fibonacci series
- List comprehensions and enumerate
- Basic arithmetic and division types
- Simple loop-based product
- Input and formatted printing
- Geometric sequence generator
- Small NumPy / scikit-learn examples (reshaping, cosine similarity)

## Requirements

- Python 3.8+
- numpy
- scikit-learn

Install dependencies:
```bash
pip install numpy scikit-learn
```

## Examples

### Fibonacci series up to n
```python
def fib(n):
    a, b = 0, 1
    while a < n:
        print(a, end=' ')
        a, b = b, a + b
    print()

fib(1000)
```

### List comprehensions and enumerate
```python
fruits = ['Banana', 'Apple', 'Lime']
loud_fruits = [fruit.upper() for fruit in fruits]
print(loud_fruits)           # ['BANANA', 'APPLE', 'LIME']
print(list(enumerate(fruits)))  # [(0, 'Banana'), (1, 'Apple'), (2, 'Lime')]
```

### Simple arithmetic
```python
print(1 / 2)   # 0.5
print(2 ** 3)  # 8

# Classic (true) division
print(17 / 3)  # 5.666...

# Floor (integer) division
print(17 // 3)  # 5
```

### Product of a list
```python
numbers = [2, 4, 6, 8]
product = 1
for number in numbers:
    product = product * number

print('The product is:', product)  # The product is: 384
```

### Input and formatted printing
```python
name = input('What is your name?\n')
print(f'Hi, {name}.')
```

### Geometric sequence generator
```python
def geometric_sequence(a1, r, n):
    """
    Generates a list representing a geometric sequence.

    Args:
      a1: The first term of the sequence.
      r: The common ratio.
      n: The number of terms to generate.

    Returns:
      A list of the first n terms of the geometric sequence.
    """
    return [a1 * (r ** i) for i in range(n)]

# Example usage
sequence = geometric_sequence(2, 3, 5)
print("Geometric Sequence:", sequence)  # [2, 6, 18, 54, 162]
```

### NumPy reshape and scikit-learn cosine similarity
```python
import numpy as np
from sklearn.metrics.pairwise import cosine_similarity

# Input data (X) must be a 2D array: [[x1], [x2], ...]
X = np.array([5, 15, 25, 35, 45, 55]).reshape((-1, 1))
y = np.array([5, 20, 14, 32, 22, 38])

# Example: cosine similarity between two vectors
vec_a = np.array([[1, 0, 1]])
vec_b = np.array([[0, 1, 1]])
similarity = cosine_similarity(vec_a, vec_b)[0][0]  # ~0.707
print("Cosine similarity:", similarity)
```
