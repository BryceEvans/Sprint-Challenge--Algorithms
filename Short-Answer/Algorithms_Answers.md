Add your answers to the Algorithms exercises here.

Exercise 1:

a) 
```
a = 0 #  O(1)
while (a < n * n * n): #  O(n^3)
      a = a + n * n  # a + O(n^2)
      # O(n^3) / O(n^2) --> O(n)
```
 O(n)


b)
```
sum = 0  #O(1)
for i in range(n):  #O(n)
    i += 1
    for j in range(i + 1, n):  # O(n) --> here OR below
    j += 1
    for k in range(j + 1, n):  # O(n) --> here OR above (not actually a nested loop)
        k += 1
        for l in range(k + 1, 10 + k):  # O(n)
        l += 1
        sum += 1
            # O(n) * O(n) * O(n) --> O(n^3)
```
O(n^3)

c)
```
def bunnyEars(bunnies):
    if bunnies == 0:  #O(1)
    return 0

    return 2 + bunnyEars(bunnies-1)  # O(n) (although shouldn't this be 2 * and NOT 2 + ???)
```
O(n)

Exercise 2:

This process could be best be solved by using a recursive binary search. 

You could take the number of stories _n_ and find the midpoint. Drop an egg form there. If it breaks, move down, if it does not, move up. Repeat that process until you find the floor _f_ where the egg stops breaking (or starts breaking). 

I think the runtime complexity of a recursive binary search would be O(n).

