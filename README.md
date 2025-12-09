# AI-opener

# Fibonacci series up to n
>>> def fib(n):
>>>     a, b = 0, 1
>>>     while a < n:
>>>         print(a, end=' ')
>>>         a, b = b, a+b
>>>     print()
>>> fib(1000)

# List comprehensions
>>> fruits = ['Banana', 'Apple', 'Lime']
>>> loud_fruits = [fruit.upper() for fruit in fruits]
>>> print(loud_fruits)
['BANANA', 'APPLE', 'LIME']

# List and the enumerate function
>>> list(enumerate(fruits))
[(0, 'Banana'), (1, 'Apple'), (2, 'Lime')]
#Simple arithmetic
>>> 1 / 2
0.5
>>> 2 ** 3
8
# classic division returns a 
>>> 17 / 3
5.666666666666667

# floor division
>>> 17 // 3
5
>>> numbers = [2, 4, 6, 8]
>>> product = 1
>>> for number in numbers:
...    product = product * number
... 
>>> print('The product is:', product)
The product is: 384
>>> print("Hello My Name Is AI-opener!")
Hello, I'm AI-opener!
>>> name = input('What is your name?\n')
What is your name?
AI-opener
>>> print(f'Hi, {}.')
Hi, AI-opener.name

# Input data (X) must be a 2D array: [[x1], [x2], ...]
X = np.array([5, 15, 25, 35, 45, 55]).reshape((-1, 1)) 

# Output data (y)
y = np.array([5, 20, 14, 32, 22, 38])
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

# Example usage: start=2, ratio=3, length=5
first_term = 2
common_ratio = 3
num_terms = 5
sequence = geometric_sequence(first_term, common_ratio, num_terms)
print("Geometric Sequence:", sequence)

# Output: Geometric Sequence: [2, 6, 18, 54, 162]
from sklearn.metrics.pairwise import cosine_similarity
vec_a = np.array([[1, 0, 1]])
vec_b = np.array([[0, 1, 1]])
similarity = cosine_similarity(vec_a, vec_b)[0][0] # ~0.707
