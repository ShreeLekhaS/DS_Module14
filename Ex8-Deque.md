# Ex 2(C) Deque
## DATE: 11.03.2025
## AIM:
To write a C function to count the number of elements present in the deque.

## Algorithm

1.Start the function count.

2.Initialize a counter variable c to 0.

3.Loop through the array from index 0 to MAX - 1.

4.For each element, check if it is not equal to 0.

5.If true, increment the counter c.

6.After the loop ends, return the value of c (the count of non-zero elements).  

## Program:
```
/*
Program to count the number of elements present in the deque
Developed by: Shree Lekha.S
RegisterNumber: 212223110052 

#include<stdio.h>
int count(int *arr) {
  int c = 0, i;
  for(i=0;i<MAX;i++)
  {
      if(arr[i]!=0)
      c++;
  }
  return c;
}
```

## Output:

![image](https://github.com/user-attachments/assets/483ebfec-ec48-4475-adad-037d587fff24)


## Result:
Thus, the C code to count the number of elements present in the deque is implemented successfully.
