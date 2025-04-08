#include <stdio.h>

int add(int a, int b) {
    return a + b;
}
int subtract(int a, int b) {
    return a - b;
}
int multiply(int a, int b) {
    return a * b;
}
float divide(int a, int b) {
    return (float)a / b;
}
int main() {
    int num1, num2;
    char sign;

    printf("Enter first number: ");
    scanf("%d", &num1);

    printf("Enter operator (+, -, *, /): ");
    scanf(" %c", &sign);

    printf("Enter second number: ");
    scanf("%d", &num2);

    if (sign == '+') {
        printf("Answer = %d\n", add(num1, num2));
    } else if (sign == '-') {
        printf("Answer = %d\n", subtract(num1, num2));
    } else if (sign == '*') {
        printf("Answer = %d\n", multiply(num1, num2));
    } else if (sign == '/') {
        if (num2 != 0) {
            printf("Answer = %.2f\n", divide(num1, num2));
        } else {
            printf("Cannot divide by zero.\n");
        }
    } else {
        printf("Invalid operator.\n");
    }
    return 0;
}
