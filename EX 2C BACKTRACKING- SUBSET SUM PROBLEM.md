![image](https://github.com/user-attachments/assets/8f9314c6-44fa-4129-99de-9e5fadf4b722)# EX 2C BACKTRACKING- SUBSET SUM PROBLEM
## DATE: 25.5.2025
## AIM:
To demonstrate that the sum of the subset of a given set is equal to the given sum.
## Algorithm
1.Start from the first element and explore all subsets by including or excluding current element.
2.Maintain a running sum while recursively traversing the array.
3.If end of array is reached, check if current sum equals the target.
4.If any recursive path leads to the target sum, return True.
5.If no subset adds up to the target, return False.  

## Program:
```
/*
Program to implement Subset sum problem.
Developed by: Samyuktha S
Register Number: 212222240089 
*/
```
```
def SubsetSum(a,i,sum,target,n):

    if(i==n):
        return sum==target
    if SubsetSum(a,i+1,sum+a[i],target,n):
        return True
    if SubsetSum(a,i+1,sum,target,n):
        return True
        
    return False

a=[]
size=int(input())
for i in range(size):
    x=int(input())
    a.append(x)

target=int(input())
n=len(a)
if(SubsetSum(a,0,0,target,n)==True):
    for i in range(size):
        print(a[i])
    print("True,subset found")
else:
    for i in range(size):
        print(a[i])
    print("False,subset not found")
```

## Output:
![image](https://github.com/user-attachments/assets/548a1aa9-4c79-4196-afa5-449e34f488f2)

## Result:
The Subset Sum program executed successfully, and the result was determined based on whether a subset matching the target sum was found or not.
