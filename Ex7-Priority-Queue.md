# Ex 2(B) Priority Queue
## DATE: 08.03.2025
## AIM:
To formulate the C code to display the elements of the priority queue after insertion and deletion operation.

## Algorithm

1.Start the program and declare an integer array and size variable.

2.Read the number of elements to insert (m) and loop to insert each element into the heap.

3.Read the number of elements to delete (r) and loop to delete each specified element from the heap.

4.Use insert function to add elements maintaining heap property.

5.Use deleteRoot function to remove elements and restore heap order.

6.Print the resulting max-heap array after all insertions and deletions, then end the program.

  

## Program:
```
/*
Program to o display the elements of the priority queue after insertion and deletion operation
Developed by: Shree Lekha.S
RegisterNumber: 212223110052
*/

#include <stdio.h>
int size = 0;
int main() {
    int m,k,e,r,e1;
  int array[10];
  scanf("%d",&m);
  for(k=0;k<m;k++)
  {
      scanf("%d",&e);
      insert(array,e);
  }
  scanf("%d",&r);
  for(k=0;k<r;k++)
  {
      scanf("%d",&e1);
      deleteRoot(array,e1);
  }
  printf("Max-Heap array after insertion and deletion: ");
  printArray(array,size);
}
```

## Output:

![image](https://github.com/user-attachments/assets/e8142f44-e466-4f77-a893-2f1d3211aaaa)


## Result:
Thus, the C program to display the elements of the priority queue after insertion and deletion operation is implemented successfully
