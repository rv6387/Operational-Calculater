// Operational-Calculater
// Develop a basic calculator that performs addition, subtraction, multiplication, and division.
#include <iostream>

using namespace std;

void add(double x, double y) {
    cout << x << " + " << y << " = " << (x + y) << endl;
}

void subtract(double x, double y) {
    cout << x << " - " << y << " = " << (x - y) << endl;
}

void multiply(double x, double y) {
    cout << x << " * " << y << " = " << (x * y) << endl;
}

void divide(double x, double y) {
    if (y != 0) {
        cout << x << " / " << y << " = " << (x / y) << endl;
    } else {
        cout << "Error! Division by zero." << endl;
    }
}

int main() {
    int choice;
    double num1, num2;

    do {
        cout << "Select operation:" << endl;
        cout << "1. Addition" << endl;
        cout << "2. Subtraction" << endl;
        cout << "3. Multiplication" << endl;
        cout << "4. Division" << endl;

        cout << "Enter choice (1/2/3/4): ";
        cin >> choice;

        if (choice >= 1 && choice <= 4) {
            cout << "Enter first number: ";
            cin >> num1;
            cout << "Enter second number: ";
            cin >> num2;

            switch (choice) {
                case 1:
                    add(num1, num2);
                    break;
                case 2:
                    subtract(num1, num2);
                    break;
                case 3:
                    multiply(num1, num2);
                    break;
                case 4:
                    divide(num1, num2);
                    break;
            }
        } else if (choice != 5) {
            cout << "Blank" << endl;
        }

    } while (choice != 5);

    cout << "Exiting the calculator. Goodbye!" << endl;

    return 0;
}
