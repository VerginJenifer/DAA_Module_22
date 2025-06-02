# EX 4B DYNAMIC PROGRAMMING – 2
## DATE:
## AIM:
To find the longest string (or strings) that is a substring (or are substrings) of two strings..



## Algorithm
1. Initialize a 2D array dp[m+1][n+1] with zeros and variables to track max length and ending index.
2. For each character pair (x[i-1], y[j-1]), if they match, set dp[i][j] = dp[i-1][j-1] + 1.
3. Update max_len and end_index if a longer common substring is found.
4. If characters don't match, set dp[i][j] = 0 (breaks the substring).
5. Return the substring from (end_index - max_len) to end_index in x.  

## Program:
```
/*
Program to implement the longest common substring problem

.
Developed by: D Vergin Jenfier
Register Number: 212223240174
def lcs(x,y):
    m=len(x)
    n=len(y)
    dp=[[0 for _ in range(n+1)]for _ in range(m+1)]
    max_len=0
    end_index=0
    for i in range(1,m+1):
        for j in range(1,n+1):
            if u[i-1]==v[j-1]:
                dp[i][j]=1+dp[i-1][j-1]
                if dp[i][j]>max_len:
                    max_len=dp[i][j]
                    end_index=i
            else:
                dp[i][j]=0
    return x[end_index-max_len:end_index]
u=input()
v=input()
print("The longest common substring is",lcs(u,v))
*/
```

## Output:


![image](https://github.com/user-attachments/assets/1e35f1d9-747a-449e-be76-5dac1c11ca4d)


## Result:
Thus the program was executed successfully for finding the longest common substring .
