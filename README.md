#include <iostream>
using namespace std;

// Function prototypes
void derivativePolynomial();
void derivativeSin();
void derivativeCos();
void derivativeTan();
void derivativeSec();
void derivativeCsc();
void derivativeCot();
void derivativePower();
void derivativeExp();
void derivativeLn();
void derivativeOneOverX();

int main() {
    int choice;

    for (int attempt = 1; attempt <= 12; attempt++) {
        cout << "\n========== DERIVATIVE CALCULATOR ==========\n";
        cout << "Attempt: " << attempt << " of 12\n";
        cout << "*****1. Polynomial (ax^2, bx, or c)*****\n";
        cout << "*****2. sin(x)*****\n";
        cout << "*****3. cos(x)*****\n";
        cout << "*****4. tan(x)*****\n";
        cout << "*****5. sec(x)*****\n";
        cout << "*****6. csc(x)*****\n";
        cout << "*****7. cot(x)*****\n";
        cout << "*****8. x^n (Power Rule)*****\n";
        cout << "*****9. e^x*****\n";
        cout << "*****10. ln(x)*****\n";
        cout << "*****11. 1/x*****\n";
        cout << "????12. Exit????\n";
        cout << "===>Enter choice:<=== ";
        cin >> choice;

        switch (choice) {
            case 1: derivativePolynomial();
 break;
            case 2: derivativeSin(); 
break;
            case 3: derivativeCos(); 
break;
            case 4: derivativeTan();
 break;
            case 5: derivativeSec();
 break;
            case 6: derivativeCsc();
 break;
            case 7: derivativeCot(); 
break;
            case 8: derivativePower();
 break;
            case 9: derivativeExp(); 
break;
            case 10: derivativeLn();
 break;
            case 11: derivativeOneOverX();
 break;
            case 12:
                cout << "?????\nExiting program…?????\n";
                return 0;
            default:
                cout << "\n===>Invalid choice! Try again.\n";
        }

        cout << "\n*****************************\n";
    }

    cout << "\n *****Thank you for using Derivative Calculator! ******\n";
    return 0;
}

// ===== Function Definitions =====

// Polynomial derivative based on type
void derivativePolynomial() {
    int type;
    double coeff;

    cout << "\n====>Select term type<===:\n";
    cout << "===>1. ax^2\n2. bx\n3. constant<===\nEnter type: ";
    cin >> type;

    if (type >= 1 && type <= 3) {
        cout << "***Enter coefficient:*** ";
        cin >> coeff;

        cout << "***\nDerivative:*** ";
        if (type == 1) cout << 2 * coeff << "x";
        else if (type == 2) cout << coeff;
        else if (type == 3) cout << "0";
        cout << endl;
    } else {
        cout << "===>Invalid type!<===\n";
    }
}

// Trigonometric derivatives
void derivativeSin() { cout << "\n===>Derivative: cos(x)<===\n"; }
void derivativeCos() { cout << "\n===>Derivative: -sin(x)<===\n"; }
void derivativeTan() { cout << "\n===>Derivative: sec^2(x)<===\n"; }
void derivativeSec() { cout << "\n===>Derivative: sec(x)*tan(x)<===\n"; }
void derivativeCsc() { cout << "\n===>Derivative: -csc(x)*cot(x)<===\n"; }
void derivativeCot() { cout << "\n===>Derivative: -csc^2(x)<===\n"; }

// Power rule x^n => n*x^(n-1)
void derivativePower() {
    float n;
    cout << "\n ==>Enter power n (for x^n)<==: ";
    cin >> n;
    cout << "\n===>Derivative: " << n << "x^" << (n - 1) << endl;
}

// Exponential
void derivativeExp() { cout << "\n==>Derivative: e^x\n"; }

// Natural logarithm
void derivativeLn() { cout << "\n==>Derivative: 1/x\n"; }

// 1/x
void derivativeOneOverX() { cout << "\n==>Derivative: -1/x^2\n";
 }# c-derivative-calculator-project
