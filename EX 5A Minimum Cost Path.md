Developed by: Vignesh M
Register Number: 212223240176# EX 5A Minimum Cost Path
## DATE:
## AIM:
To write a Python program using A Naive recursive implementation of Minimum Cost Path Problem.

## Algorithm:
```
1. If row `m` or column `n` is less than 0, return a large value to indicate an invalid path.
2. If `m == 0` and `n == 0`, return the cost of the starting cell.
3. Recursively compute the cost to reach cell `(m, n)` from the top-left diagonal, top, and left.
4. Add the current cell’s cost to the minimum of these three computed costs.
5. Return this minimum cost.
6. Call the recursive function starting from the bottom-right corner to get the final minimum cost.
```

## Program:
```
Developed by: Vignesh M
Register Number: 212223240176

R = int(input())
C = int(input())

import sys
def minCost(cost, m, n):
    ###########  Add your Code Here ##################
    if (n < 0 or m < 0):
        return sys.maxsize
    elif (m == 0 and n == 0):
        return cost[m][n]
    else:
        return cost[m][n] + min( minCost(cost, m-1, n-1),
                                minCost(cost, m-1, n),
                                minCost(cost, m, n-1) )
                                
def min(x, y, z):
    if (x < y):
        return x if (x < z) else z
    else:
        return y if (y < z) else z
cost= [ [1, 2, 3],
        [4, 8, 2],
        [1, 5, 3] ]
print(minCost(cost, R-1, C-1))
```

## Output:
![Screenshot 2025-04-30 211325](https://github.com/user-attachments/assets/0211da6d-ee34-4ecd-99a0-37f82c534dc5)

## Result:
Thus the above program was executed successfully for finding the minimum cost.
