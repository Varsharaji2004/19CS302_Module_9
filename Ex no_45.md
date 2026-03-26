# EX 45 C program that implements a queue using an array, and performs insertion (enqueue) and display operations.
## DATE:
## AIM:
To write a C program that implements a queue using an array, and performs insertion (enqueue) and display operations. 

## Algorithm
1.Start the program and declare an array to implement the queue with front and rear.

2.Define the enqueue() function to insert elements if the queue is not full.

3.Define the display() function to print all elements from front to rear.

4.In main(), call enqueue() multiple times and then call display() to show queue content.

5.End the program.

## Program:
```
/*
C program that implements a queue using an array, and performs insertion (enqueue) and display operations.

*/
#include <stdio.h>
#define MAX 100

int queue[MAX];
int front = -1, rear = -1;

void enqueue(int value)
{
    if(rear == MAX - 1)
    {
        printf("Queue overflow\n");
        return;
    }
    if(front == -1)
        front = 0;
    queue[++rear] = value;
    printf("%d enqueued to queue\n", value);
}

void display()
{
    if(front == -1 || front > rear)
    {
        printf("Queue is empty\n");
        return;
    }
    printf("Queue elements: ");
    for(int i = front; i <= rear; i++)
    {
        printf("%d ", queue[i]);
    }
    printf("\n");
}

int main()
{
    enqueue(5);
    enqueue(15);
    enqueue(25);

    display();

    return 0;
}


```


## Output:

<img width="392" height="292" alt="image" src="https://github.com/user-attachments/assets/58b04561-fc32-4fed-b034-95293b3d73fc" />

## Result:
Thus the program was executed and the output was verified successfully.
