//# calculator-
//Basic calculator in c programming

#include <iostream>
#include <string>
using namespace std;

int main() {
    double a, b, result;
    std::string operation;

    std::cout << "Available operations: add, subs, mult, div, exit\n";

    while (true) {
        cout << "\nChoose an operation: ";
        cin >> operation;

        if (operation == "exit") {
            cout << "Goodbye" << endl;
            break;
        }

        cout << "Enter first number (a): ";
        cin >> a;
        cout << "Enter second number (b): ";
        cin >> b;

        if (operation == "add") {
            result = a + b;
            cout << "Result: " << result << endl;
        }
        else if (operation == "subs") {
            result = a - b;
            cout << "Result: " << result << endl;
        }
        else if (operation == "mult") {
            result = a * b;
            cout << "Result: " << result << endl;
        }
        else if (operation == "div") {
            if (b != 0) {
                result = a / b;
                cout << "Result: " << result << endl;
            }
            else {
                cout << "Error: Division by zero is not possible." << endl;
            }
        }
        else {
            cout << "Operation Error. Please choose one of these options add, subs, mult, div, or exit." << endl;
        }
    }

    return 0;
}
