# EX 41 C program to write a function to find the peek of stack using array.
## DATE:
## AIM:
To write a function to find the peek of stack using array.

## Algorithm
1.Start the program and declare an array to implement the stack.

2.Define a function peek to return the top element of the stack.

3.Check if the stack is empty before accessing the top element.

4.If the stack is empty, return a suitable message or value indicating an empty stack.

5.End the program.  

## Program:
```
/*
C program to write a function to find the peek of stack using array.

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
    }
    else
    {
        printf("Stack overflow\n");
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
        return -1;  // Returning -1 to indicate empty stack
    }
}

int main()
{
    push(10);
    push(20);
    push(30);

    printf("Top of the stack: %d\n", peek());

    return 0;
}


```

## Output:

<img width="606" height="239" alt="image" src="https://github.com/user-attachments/assets/a3a33ead-0e14-4119-be91-3841ada70938" />


## Result:
Thus the program was executed and the output was verified successfully.
