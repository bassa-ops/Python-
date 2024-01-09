1)# Python-
Python
Task
Given an integer, , perform the following conditional actions:

If  is odd, print Weird
If  is even and in the inclusive range of  to , print Not Weird
If  is even and in the inclusive range of  to , print Weird
If  is even and greater than , print Not Weird
Input Format

A single line containing a positive integer, .

**Solutions**
import math
import os
import random
import re
import sys

n=4
if n%2!=0:
    print("Weird")
elif n%2==0 and n>2 and n<=5:
    print("Not Weird")
elif n%2==0 and n>6 and n<=20:
    print("Weird")
else:
    print("Not Weird")



 2) Task
The provided code stub reads two integers from STDIN,  and . Add code to print three lines where:

The first line contains the sum of the two numbers.
The second line contains the difference of the two numbers (first - second).
The third line contains the product of the two numbers.

**Solution **
if __name__ == '__main__':
    a = int(input())
    b = int(input())
    
    print(a+b)
    print(a-b)
    print(a*b)

3)The provided code stub reads two integers,  and , from STDIN.
Add logic to print two lines. The first line should contain the result of integer division,  // . The second line should contain the result of float division,  / .
No rounding or formatting is necessary.

**Solution**
if __name__ == '__main__':
    a = int(input())
    b = int(input())
    print(a//b)
    print(a/b)

4)Task
The provided code stub reads and integer, i<n, from STDIN. For all non-negative integers i*i print.

**Solution**
if __name__ == '__main__':
    n = int(input())
    for i in range(n):
        print(i*i)

5)Question: Python List Comprehensions [Basic Data Types]
Let’s learn about list comprehension! You are given three integers x, y, and z representing the dimensions of a cuboid along with an integer n. Print a list of all possible coordinates given by (i, j, k) on a 3D grid where the sum of i + j + k is not equal to n. Here, 0 <= i <= x; 0 <= j <= y; 0 <= k <= z. Please use list comprehensions rather than multiple loops, as a learning exercise.

Example:
x = 1
y = 1
z = 2
n = 3

All permutations of [i, j, k] are:
if __name__ == '__main__':
    n = int(input())
    for i in range(1, n+1):
        print(i,end='')
[[0, 0, 0], [0, 0, 1], [0, 0, 2], [0, 1, 0], [0, 1, 1], [0, 1, 2], [1, 0, 0], [1, 0, 1], [1, 0, 2], [1, 1, 0], [1, 1, 1], [1, 1, 2]]
Print an array of the elements that do not sum to n = 3.
[[0, 0, 0], [0, 0, 1], [0, 0, 2], [0, 1, 0], [0, 1, 1], [1, 0, 0], [1, 0, 1],  [1, 1, 0],  [1, 1, 2]]

Input Format:
Four integers x, y, z and n, each on a separate line.
Constraints:
Print the list in lexicographic increasing order.

**Solution** 

**Solution-1: Using list comprehension**
if __name__ == '__main__':
    x = int(input())
    y = int(input())
    z = int(input())
    n = int(input())
   out= [[i,j,k]for i in range(x+1) for j in range(y+1) for k in range(z+1) if i+j+k != n]
   print(out)

**Solution-2: Using nested for loops**
if __name__ == '__main__':
    x = int(input())
    y = int(input())
    z = int(input())
    n = int(input())
    out_put = []
    for i in range(x+1):
        for j in range(y+1):
            for k in range(z+1):
                if i+j+k != n:
                 out_put.append([i, j, k])
    print(out_put)

6)Question: Find the Runner-up Score [Python Basic Data Types]

**Solution**
if __name__ == '__main__':
    n = int(input())
    arr = map(int, input().split())
    arr1=set(arr)
    arr2=sorted(arr1)
    print(arr2[-2])
