# scientific-calculator-for-using-c-
we use this calculator for purpose of any solution
#include <iostream>
#scientific calculator for using c++ by Hammad , KKKUK Student
#include <cmath>  // For mathematical functions like sqrt, sin, cos, etc.
using namespace std;

void showMenu() {
    cout << "Select an operation:\n";
    cout << "1. Addition\n";
    cout << "2. Subtraction\n";
    cout << "3. Multiplication\n";
    cout << "4. Division\n";
    cout << "5. Square Root\n";
    cout << "6. Power\n";
    cout << "7. Sine\n";
    cout << "8. Cosine\n";
    cout << "9. Tangent\n";
    cout << "0. Exit\n";
}

int main() {
    int choice;
    double num1, num2, result;

    while (true) {
        showMenu();
        cout << "Enter your choice: ";
        cin >> choice;

        if (choice == 0) {
            break; // Exit the loop and terminate the program
        }

        switch (choice) {
            case 1:  // Addition
                cout << "Enter two numbers: ";
                cin >> num1 >> num2;
                result = num1 + num2;
                cout << "Result: " << result << endl;
                break;

            case 2:  // Subtraction
                cout << "Enter two numbers: ";
                cin >> num1 >> num2;
                result = num1 - num2;
                cout << "Result: " << result << endl;
                break;

            case 3:  // Multiplication
                cout << "Enter two numbers: ";
                cin >> num1 >> num2;
                result = num1 * num2;
                cout << "Result: " << result << endl;
                break;

            case 4:  // Division
                cout << "Enter two numbers: ";
                cin >> num1 >> num2;
                if (num2 != 0) {
                    result = num1 / num2;
                    cout << "Result: " << result << endl;
                } else {
                    cout << "Error: Division by zero!" << endl;
                }
                break;

            case 5:  // Square Root
                cout << "Enter a number: ";
                cin >> num1;
                if (num1 >= 0) {
                    result = sqrt(num1);
                    cout << "Square root: " << result << endl;
                } else {
                    cout << "Error: Negative number for square root!" << endl;
                }
                break;

            case 6:  // Power
                cout << "Enter base and exponent: ";
                cin >> num1 >> num2;
                result = pow(num1, num2);
                cout << "Result: " << result << endl;
                break;

            case 7:  // Sine
                cout << "Enter angle in radians: ";
                cin >> num1;
                result = sin(num1);
                cout << "Sine: " << result << endl;
                break;

            case 8:  // Cosine
                cout << "Enter angle in radians: ";
                cin >> num1;
                result = cos(num1);
                cout << "Cosine: " << result << endl;
                break;

            case 9:  // Tangent
                cout << "Enter angle in radians: ";
                cin >> num1;
                result = tan(num1);
                cout << "Tangent: " << result << endl;
                break;

            default:
                cout << "Invalid choice! Please try again.\n";
                break;
        }
    }

    cout << "Exiting the program...\n";
    return 0;
}
