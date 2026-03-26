# EX 42 C program to write a fuctions to perform push,pop,display,peek in stack using array.
## DATE:
## AIM:
To write a fuctions to perform push,pop,display,peek in stack using array.

## Algorithm
1.Start the program and declare a stack array and a variable top initialized to -1.

2.Define push() to insert an element into the stack if it is not full.

3.Define pop() to remove the top element from the stack if it is not empty.

4.Define peek() to return the topmost element without removing it.

5.Define display() to print all stack elements from top to bottom.

## Program:
```
/*
C program to write a fuctions to perform push,pop,display,peek in stack using array.

*/
#include <stdio.h>
#define MAX 100

int stack[MAX];
int top = -1;

void push(int value)
{
    if(top < MAX - 1)
    {
        stack[++top] = value;
        printf("%d pushed to stack\n", value);
    }
    else
    {
        printf("Stack overflow\n");
    }
}

void pop()
{
    if(top >= 0)
    {
        printf("%d popped from stack\n", stack[top--]);
    }
    else
    {
        printf("Stack underflow\n");
    }
}

int peek()
{
    if(top >= 0)
    {
        return stack[top];
    }
    else
    {
        printf("Stack is empty\n");
        return -1;
    }
}

void display()
{
    if(top >= 0)
    {
        printf("Stack elements: ");
        for(int i = top; i >= 0; i--)
        {
            printf("%d ", stack[i]);
        }
        printf("\n");
    }
    else
    {
        printf("Stack is empty\n");
    }
}

int main()
{
    push(10);
    push(20);
    push(30);

    display();

    printf("Top element: %d\n", peek());

    pop();
    display();

    return 0;
}


```

## Output:

<img width="416" height="392" alt="image" src="https://github.com/user-attachments/assets/cb80c0be-23b8-49ba-9e5e-996eb97d10a8" />


## Result:
Thus the program was executed and the output was verified successfully.
