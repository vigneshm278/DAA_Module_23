# EX 5B Coin Change Problem
## DATE:
## AIM:
To compute the fewest number of coins that we need to make up the amount given.

## Algorithm:
```
1. Create a DP array `dp[]` of size `amount + 1`, where `dp[i]` stores the minimum coins needed to make amount `i`.
2. Initialize `dp[0] = 0` and set all other entries to infinity.
3. For each coin, iterate through amounts from the coin value up to the target amount.
4. Update `dp[i]` as the minimum of its current value and `dp[i - coin] + 1`.
5. After filling the array, if `dp[amount]` is infinity, return -1.
6. Otherwise, return `dp[amount]` as the result.
```

## Program:
```
Developed by: Vignesh M
Register Number: 212223240176

class Solution(object):
   def coinChange(self, coins, amount):
       ####################      Add your Code Here ###########
        dp = [float('inf')] * (amount + 1)
        dp[0]=0
        for coin in coins:
            for i in range(coin, amount + 1):
                dp[i] = min(dp[i], dp[i - coin] + 1)
        return dp[amount] if dp[amount]!=float('inf') else -1
      
      
ob1 = Solution()
n=int(input())
s=[]
amt=int(input())
for i in range(n):
    s.append(int(input()))


print(ob1.coinChange(s,amt))
```

## Output:
![Screenshot 2025-04-30 211719](https://github.com/user-attachments/assets/4558eb9f-8e0b-4875-b47f-ba72f5579ce9)

## Result:
Thus the program was executed successfully for finding the minimum number of coins required to make amount.
