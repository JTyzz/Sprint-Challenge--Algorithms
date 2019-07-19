a)  a = 0					O(1)
    while (a < n * n * n):	O(n^3)
      a = a + n * n			O(n^2)         

Answer is O(n^3)

b)  sum = 0										O(1)
    for i in range(n):							O(n)
      i += 1									O(1)
      for j in range(i + 1, n):					O(n) [nested, O(n^2)]
        j += 1									O(1)
        for k in range(j + 1, n):				O(n) [nested, O(n^3)]
          k += 1								O(1)
          for l in range(k + 1, 10 + k):		O(n) [nested, O(n^4 + 10)]
            l += 1
            sum += 1

Answer is O(n^4)

c)  def bunnyEars(bunnies):
      if bunnies == 0:
        return 0

      return 2 + bunnyEars(bunnies-1)	Linear recursion, O(n)

Answer is O(n)



Divide the floors into two and drop from the middle. 
If the egg doesn't break:
	Divide top half into two and drop egg from middle
If egg does break:
	Divide bottom half in two and drop egg from middle
Loop until you have found the lowest floor the egg breaks on then -1

The runtime is O(logn) because it's a binary search