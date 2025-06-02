# EX 4A DYNAMIC PROGRAMMING - 1
## DATE:
## AIM:
To find longest common subsequence using Dynamic Programming.



## Algorithm
1. Initialize a 2D array dp[m+1][n+1] with zeros to store lengths of LCS for all subproblems.
2. For each character pair (u[i-1], v[j-1]), fill dp[i][j] = dp[i-1][j-1]+1 if they match, else max(dp[i-1][j], dp[i][j-1]).
3. Start from the bottom-right of the dp table to reconstruct the LCS string.
4. If characters match, add to result and move diagonally; else move to the cell with a larger value.
5. Return the constructed LCS string. 

## Program:
```
/*
Program to implement the longest common subsequence using Dynamic Programming

.
Developed by: D Vergin Jenifer
Register Number: 212223240174
def lcs(u,v):
    m=len(u)
    n=len(v)
    dp=[[0 for _ in range (n+1)]for _ in range (m+1)]
    for i in range(1,m+1):
        for j in range(1,n+1):
            if u[i-1]==v[j-1]:
                dp[i][j]=dp[i-1][j-1]+1
            else:
                dp[i][j]=max(dp[i-1][j],dp[i][j-1])
    i,j=m,n
    lcs_str=""
    while i>0 and j>0:
        if u[i-1]==v[j-1]:
            lcs_str=u[i-1]+lcs_str
            i-=1
            j-=1
        elif dp[i-1][j]>dp[i][j-1]:
            i-=1
        else:
            j-=1
    return lcs_str
u=input()
v=input()
print(lcs(u,v))

*/
```

## Output:


![image](https://github.com/user-attachments/assets/58f4ebca-58bb-4f77-b048-ea878b017795)


## Result:
Thus the program was executed successfully for computing the length of longest common subsequence.
