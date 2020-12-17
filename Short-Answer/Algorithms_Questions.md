# Analysis of Algorithms

## Exercise I

Give an analysis of the running time of each snippet of
pseudocode with respect to the input size n of each of the following:

```python
a)  
  # constant 0(1)
  a = 0
  # 0(n^3)
    while (a < n * n * n):
      # n^2
      a = a + n * n
```
`O(n)`

```
# constant O(1)
sum = 0
    # linear O(n)
    for i in range(n):
      # constant O(1)
      j = 1
      # ogarithmic Log(n) because j doubles each iteration
      while j < n:
        # constant O(1)
        j *= 2
        # constant O(1)
        sum += 1
```
`O(n*log(n))`

```
c)  def bunnyEars(bunnies):
      # constant
      if bunnies == 0:
        return 0
      # O(n)
      return 2 + bunnyEars(bunnies-1)
```
`O(n)`

## Exercise II

Suppose that you have an n-story building and plenty of eggs. Suppose also that an egg gets broken if it is thrown off floor f or higher, and doesn't get broken if dropped off a floor less than floor f. Devise a strategy to determine the value of f such that the number of dropped + broken eggs is minimized.

Write out your proposed algorithm in plain English or pseudocode AND give the runtime complexity of your solution.

`Search sorted floors by repeatedly dividing the search interval in half. Begin with an interval covering the whole array. If the eggs are broken, narrow the interval to the lower half. Otherwise narrow it to the upper half. Repeatedly check until the floor is found.`

`O(Log N)`