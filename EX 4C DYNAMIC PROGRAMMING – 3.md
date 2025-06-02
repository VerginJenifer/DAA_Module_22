# EX 4C DYNAMIC PROGRAMMING – 3
## DATE:
## AIM:
Given a sequence, find the length of the longest palindromic subsequence in it.





## Algorithm
1. Reverse the original string to get a second string v.
2. Initialize a 2D dp table of size (m+1) x (n+1) with zeros.
3. For each character pair (u[i-1], v[j-1]), if they match, set dp[i][j] = dp[i-1][j-1] + 1.
4. If characters don't match, set dp[i][j] = max(dp[i-1][j], dp[i][j-1]).
5. Return dp[m][n], which contains the length of the longest palindromic subsequence.

## Program:
```
/*
Program to implement to find the length of the longest palindromic subsequence in it

.
Developed by: D Vergin Jenifer
Register Number: 212223240174

def lps(u,v,m,n,dp):
    if m==0 or n==0:
        return 0
    for i in range(1,m+1):
        for j in range(1,n+1):
            if u[i-1]==v[j-1]:
                dp[i][j]=1+dp[i-1][j-1]
            else:
                dp[i][j]=max(dp[i-1][j],dp[i][j-1])
    return dp[m][n]
u=input()
v=u[::-1]
dp=[[0 for _ in range(1001)]for _ in range(1001)]
print("The length of the LPS is",lps(u,v,len(u),len(v),dp))
*/
```

## Output:


![image](https://github.com/user-attachments/assets/a1656a0f-3279-4580-a600-66a83fd29140)


## Result:
Thus the program was executed successfully for finding the length of longest palindromic string.
