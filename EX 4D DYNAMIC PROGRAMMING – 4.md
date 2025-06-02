# EX 4D DYNAMIC PROGRAMMING – 4
## DATE:
## AIM:
To find the minimum number of operations to convert str1 to str2 using Naive recursive method.





## Algorithm
1. If either string is empty, return the length of the other string.
2. If the last characters of both strings match, set cost = 0; else set cost = 1.
3. Recursively calculate:
   - insert (s, t[:-1]) + 1
   - delete (s[:-1], t) + 1
   - replace (s[:-1], t[:-1]) + cost
4. Take the minimum of the three operations.
5. Return the minimum cost as the edit distance.

## Program:
```
/*
Program to implement to find the minimum number of operations to convert str1 to str2 using Naive recursive method

.
Developed by: D Vergin Jenifer
Register Number: 21223240174
def LD(s, t):
    if s=="":
        return len(t)
    if t=="":
        return len(s)
    if s[-1]==t[-1]:
        cost=0
    else:
        cost=1
    res=min([LD(s[:-1],t)+1,LD(s,t[:-1])+1,LD(s[:-1],t[:-1])+cost])
    return res
    
str1=input()
str2=input()
print('Edit Distance',LD(str1,str2))


*/
```

## Output:


![image](https://github.com/user-attachments/assets/3b390954-929b-439f-ac27-f5d87edb63ce)


## Result:
Thus the program was executed successfully for finding edit distance between two strings.
