Add your answers to the Algorithms exercises here.

```
a)  a = 0
    while (a < n * n * n):
      a = a + n * n
```

answer:
first line is O(1)
second line is O(n)
third line is O(1)
==> big O does not care about constants so it will be O(n)

b) sum = 0
for i in range(n):
i += 1
for j in range(i + 1, n):
j += 1
for k in range(j + 1, n):
k += 1
for l in range(k + 1, 10 + k):
l += 1
sum += 1

```

answer:
first line is O(1)
second line is O(n)
third line is O(1)
fourth line is O(n)
fifth line is O(1)
sixth line is O(n)
seventh line is O(1)
eighth line is O(1)
ninth line is O(1)
tenth line is O(1)
==> i guess it will be O(n*3)


```

c) def bunnyEars(bunnies):
if bunnies == 0:
return 0

      return 2 + bunnyEars(bunnies-1)

```

answer:
first line is O(1)
second line is O(1)
third line is O(n)
==> so i guess it will be O(n)


```

Suppose that you have an _n_-story building and plenty of eggs. Suppose also that an egg gets broken if it is thrown off floor _f_ or higher, and doesn't get broken if dropped off a floor less than floor _f_. Devise a strategy to determine the value of _f_ such that the number of dropped eggs is minimized.

Write out your proposed algorithm in plain English or pseudocode and give the runtime complexity of your solution.

```

answer:

height of building = n
number of eggs = n
height of floor from where if thrown egg is broken = floor > f
height of floor from where if thrown egg is not broken = floor < f

1- do a binary search since the building is kind of sorted with same floor at each level
2- so i would divide n(height of building) by 2 to find the middle floor.
3- throw an egg, if broken, i would leave the floors above and repeat the second step from ground to middle floor -1
4- if not broken, i would skip the floors upto middle and repeat the second step from middle floor + 1 to n
```
