# EX 5C Kadane's Algorithm
## DATE:
## AIM:
To write a python program to find the maximum contiguous subarray.

## Algorithm:
```
1. Initialize `max_till_now` to the first element and `max_ending` to 0.
2. Iterate through each element, adding it to `max_ending`.
3. If `max_ending` becomes negative, reset it to 0.
4. Update `max_till_now` if `max_ending` is greater.
5. Return `max_till_now` as the maximum contiguous subarray sum.

```

## Program:
```
Developed by: Vignesh M
Register Number: 212223240176
def maxSubArraySum(a,size):
    #####################  Add your Code here #############
    max_till_now = a[0]
    max_ending = 0
    
    for i in range(0, size):
        max_ending = max_ending + a[i]
        if max_ending < 0:
            max_ending = 0
        
        
        elif (max_till_now < max_ending):
            max_till_now = max_ending
            
    return max_till_now
    
    
n=int(input())  
a =[] #[-2, -3, 4, -1, -2, 1, 5, -3]
for i in range(n):
    a.append(int(input()))
  
print("Maximum contiguous sum is", maxSubArraySum(a,n))
```

## Output:
![Screenshot 2025-04-30 212139](https://github.com/user-attachments/assets/45cf11fa-e479-4fa1-8408-1ddc358a0e62)

## Result:
Thus the program was executed successfully for finding the maximum contiguous sum of subarray..
