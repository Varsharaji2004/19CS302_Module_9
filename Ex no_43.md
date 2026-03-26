# EX 43 C program to Write a function to display queue elements using array.
## DATE:
## AIM:
To Write a function to display queue elements using array.

## Algorithm
1.Start the program and declare a stack array and a variable top initialized to -1.

2.Define push() to insert an element into the stack if it is not full.

3.Define pop() to remove the top element from the stack if it is not empty.

4.Define peek() to return the topmost element without removing it.

5.Define display() to print all stack elements from top to bottom.

## Program:
```
/*

*/
#include <stdio.h>
#define MAX 100

int queue[MAX];
int front = -1, rear = -1;

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
    front = 0;
    rear = 3;
    queue[0] = 10;
    queue[1] = 20;
    queue[2] = 30;
    queue[3] = 40;

    display();

    return 0;
}


```


## Output:
<img width="424" height="228" alt="image" src="https://github.com/user-attachments/assets/ec9bb867-a9ec-4e4d-81ea-0f5cb1897072" />

## Result:
Thus the program was executed and the output was verified successfully.
