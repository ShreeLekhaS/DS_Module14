# Ex 2(A) Dequeue Elements from Circular Queue
## DATE: 06.03.2025
## AIM:
To write a C program to delete three elements from the filled circular queue.

## Algorithm

1.Start the function deQueue.

2.Check if the queue is empty using isEmpty(). If yes, print "Queue is empty" and return -1.

3.Otherwise, store the front element to return later.

4.If there is only one element (front == rear), reset both to -1 (empty queue).

5.Else, move the front pointer to the next position in a circular manner.

6.Return the stored element.   

## Program:
```
/*
Program to delete three elements from the filled circular queue
Developed by: Shree Lekha.S
RegisterNumber: 212223110052
*/

int deQueue() {
    int element;
    if(isEmpty())
    {
        printf("Queue is empty\n");
        return -1;
    }
    else
    {
        element = items[front];
        if(front==rear)
        {
            front=-1;
            rear=-1;
        }
        else
        {
            front=(front+1)%SIZE;
        }
        return element;
    }
}
```

## Output:
![image](https://github.com/user-attachments/assets/356a82ca-fd0f-4060-ac12-87adc29dd5b9)



## Result:
Thus, the C program to delete three elements from the filled circular queue is implemented successfully.
