# System-to-find-factorial-of-a-number-using-recursion-and-pointers
Design a C program to find factorial of a number   using recursion and pointers
#include <stdio.h>

int factorial(int *n) {
    if (*n == 0 || *n == 1) {
        return 1;   
    }

    int temp= *n-1;        
    return (*n) * factorial(&temp); 
}

int main() {
    int num = 5;
    int result = factorial(&num);

    printf("Factorial of %d is %d", num, result);

    return 0;
}

