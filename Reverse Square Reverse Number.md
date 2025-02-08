#include <stdio.h>
int reverseNumber(int num);
int isRSRN(int num);

int main() {
    int num;
    printf("Enter a number between 1 and 100: ");
    scanf("%d", &num);

    if (num < 1 && num > 100) {
        printf("Please enter a number within the range of 1 to 100.\n");
    } else if (isRSRN(num)) {
        printf("%d is a Reverse Square Reverse Number.\n", num);
    } else {
        printf("%d is not a Reverse Square Reverse Number.\n", num);
    }

    return 0;
}


// Function to reverse a number
int reverseNumber(int num) {
    int reversed = 0;
    while (num > 0) {
        reversed = reversed * 10 + (num % 10);
        num /= 10;
    }
    return reversed;
}

// Function to check if a number is a Reverse Square Reverse Number
int isRSRN(int num) {
    int square = num * num;             // Calculate the square of the number
    int reversedSquare = reverseNumber(square); // Reverse the square
    int reversedNum = reverseNumber(num);       // Reverse the original number
    int reversedSquareOfReversedNum = reversedNum * reversedNum; // Square of the reversed number

    return reversedSquare == reversedSquareOfReversedNum; // Check equality
}


