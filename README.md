# Recursive-function
#include <iostream>
using namespace std;

// Recursive function to calculate the nth Fibonacci number
int fibonacci(int n) {
    if (n <= 0) return 0;
    if (n == 1) return 0;  // Base case: The first Fibonacci number is 0
    if (n == 2) return 1;  // Base case: The second Fibonacci number is 1
    return fibonacci(n - 1) + fibonacci(n - 2);  // Recursive case
}

// Function to print the Fibonacci sequence up to n terms using recursion
void printFibonacciRecursive(int n) {
    for (int i = 1; i <= n; ++i) {
        cout << fibonacci(i) << " ";
    }
    cout << endl;
}

int main() {
    int n;
    cout << "Enter the number of terms of Fibonacci sequence to display: ";
    cin >> n;
    printFibonacciRecursive(n);
    return 0;
}
