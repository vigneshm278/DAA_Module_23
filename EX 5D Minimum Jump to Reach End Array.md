# EX 5D Minimum Jump to Reach End Array
## DATE:
## AIM:
To write a python program for finding the minimum number of jumps needed to reach end of the array using Dynamic Programming.

## Algorithm:
```
1. If start index `l` equals end index `h`, return 0.
2. If `arr[l]` is 0, return infinity (no further moves possible).
3. Initialize `min` to infinity.
4. For each reachable index `i` from `l + 1` to `l + arr[l]`, recursively find minimum jumps from `i` to `h`.
5. Update `min` if a smaller jump count is found.
6. Return the minimum jumps required from `l` to `h`.
```

## Program:
```
Developed by: Vignesh M
Register Number: 212223240176

def minJumps(arr, l, h):
    ###########   Add your code here ###########
    if (h == l):
        return 0
    if (arr[l] == 0):
        return float('inf')
    min = float('inf')
    for i in range(l + 1, h + 1):
        if (i < l + arr[l] + 1):
            jumps = minJumps(arr, i, h)
            if (jumps != float('inf') and
                       jumps + 1 < min):
                min = jumps + 1
 
    return min
    
arr = []
n = int(input()) 
for i in range(n):
    arr.append(int(input()))
print('Minimum number of jumps to reach','end is', minJumps(arr, 0, n-1))
 
```

## Output:
![Screenshot 2025-04-30 212445](https://github.com/user-attachments/assets/527390d5-a6d2-41cb-9974-901577a40c1c)

## Result:
Thus the program was executed successfully for finding the minimum number of jumps to reach end.
