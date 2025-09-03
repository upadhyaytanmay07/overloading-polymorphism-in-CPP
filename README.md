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

# 2. Constructor Overloading
✅ Definition

Constructor overloading allows a class to have multiple constructors with different parameter lists to initialize objects in different ways.

📌 Rules

Constructors must differ in number or type of parameters.

Helps in creating objects with varying initial states.

🧪 Example

    cpp
    class Box {
    private:
        double length, width, height;
    
    public:
        // Constructor for cube
        Box(double side) {
            length = width = height = side;
        }
    
        // Constructor for cuboid
        Box(double l, double w, double h) {
            length = l;
            width = w;
            height = h;
        }
    
        double volume() {
            return length * width * height;
        }
    };

🎯 Use Cases

Flexibility in object creation

Default, parameterized, and copy constructors

# 3. Operator Overloading

✅ Definition

Operator overloading allows you to redefine the behavior of C++ operators for user-defined types (classes).

📌 Rules

Only existing operators can be overloaded.

Cannot change precedence or arity of operators.

Some operators like ::, ., .*, sizeof cannot be overloaded.

🧪 Example: Overloading + for a Point class

    cpp
    class Point {
    public:
        int x, y;
    
        Point(int a, int b) : x(a), y(b) {}
    
        Point operator+(const Point& p) {
            return Point(x + p.x, y + p.y);
        }
    
        void display() {
            cout << "(" << x << ", " << y << ")" << endl;
        }
    };
    
    int main() {
        Point p1(2, 3), p2(4, 5);
        Point p3 = p1 + p2;
        p3.display();  // Output: (6, 8)
    }

🎯 Use Cases

Intuitive syntax for complex types

Custom behavior for arithmetic, comparison, assignment

# Algorithms
# Program 1
Objective : 
