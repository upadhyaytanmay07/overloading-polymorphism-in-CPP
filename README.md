# Aim
To study overloading ( polymorphism ) in C++

# Software 
Visual studio code

Windows/Linux

# Theory
# Overloading in C++
Overloading in C++ allows multiple definitions for the same name (function or operator) with different parameters or behaviors. It enhances polymorphism, making code more intuitive and flexible.

# Types of Overloading
Function Overloading - Multiple functions with the same name but different parameter lists.

Constructor Overloading - Multiple constructors in a class with different parameter lists.

Operator Overloading - Redefining the behavior of operators for user-defined types (classes).

# 1. Function Overloading
✅ Definition
Function overloading allows you to define multiple functions with the same name but different number or types of parameters.

📌 Rules
Functions must differ in number or type of parameters.

Return type alone cannot distinguish overloaded functions.

🧪 Example
    cpp
    #include <iostream>
    using namespace std;
    
    class Print {
    public:
        void show(int i) {
            cout << "Integer: " << i << endl;
        }
    
        void show(double d) {
            cout << "Double: " << d << endl;
        }
    
        void show(string s) {
            cout << "String: " << s << endl;
        }
    };
    
    int main() {
        Print p;
        p.show(10);
        p.show(3.14);
        p.show("Hello");
        return 0;
    }
🎯 Use Cases
Simplifies naming: add(int, int) vs add(double, double)

Improves readability and maintainability
