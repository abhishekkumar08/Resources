# C++ OOPs Concepts

The major purpose of C++ programming is to introduce the concept of object orientation to the C programming language.

Object Oriented Programming is a paradigm that provides many concepts such as inheritance, data binding, polymorphism etc.

The programming paradigm where everything is represented as an object is known as truly object-oriented programming language. Smalltalk is considered as the first truly object-oriented programming language.

# OOPs (Object Oriented Programming System)

Object means a real word entity such as pen, chair, table etc. Object-Oriented Programming is a methodology or paradigm to design a program using classes and objects. It simplifies the software development and maintenance by providing some concepts:

- Object
- Class
- Inheritance
- Polymorphism
- Abstraction
- Encapsulation

## Object

Any entity that has state and behavior is known as an object. For example: chair, pen, table, keyboard, bike etc. It can be physical and logical.

## Class

Collection of objects is called class. It is a logical entity.

## Inheritance

When one object acquires all the properties and behaviours of parent object i.e. known as inheritance. It provides code reusability. It is used to achieve runtime polymorphism.

## Polymorphism

When one task is performed by different ways i.e. known as polymorphism. For example: to convince the customer differently, to draw something e.g. shape or rectangle etc.

In C++, we use Function overloading and Function overriding to achieve polymorphism.

## Abstraction

Hiding internal details and showing functionality is known as abstraction. For example: phone call, we don't know the internal processing.

In C++, we use abstract class and interface to achieve abstraction.

## Encapsulation

Binding (or wrapping) code and data together into a single unit is known as encapsulation. For example: capsule, it is wrapped with different medicines.

# Advantage of OOPs over Procedure-oriented programming language

- OOPs makes development and maintenance easier where as in Procedure-oriented programming language it is not easy to manage if code grows as project size grows.
- OOPs provide data hiding whereas in Procedure-oriented programming language a global data can be accessed from anywhere.
- OOPs provide ability to simulate real-world event much more effectively. We can provide the solution of real word problem if we are using the Object-Oriented Programming language.

<hr>

# C++ Object and Class

Since C++ is an object-oriented language, program is designed using objects and classes in C++.

# C++ Object

In C++, Object is a real world entity, for example, chair, car, pen, mobile, laptop etc.

In other words, object is an entity that has state and behavior. Here, state means data and behavior means functionality.

Object is a runtime entity, it is created at runtime.

Object is an instance of a class. All the members of the class can be accessed through object.

Let's see an example to create object of student class using s1 as the reference variable.

```cpp
Student s1; //creating an object of Student
```

In this example, Student is the type and s1 is the reference variable that refers to the instance of Student class.

# C++ Class

In C++, class is a group of similar objects. It is a template from which objects are created. It can have fields, methods, constructors etc.

Let's see an example of C++ class that has three fields only.

```cpp
class Student
 {
 public:
 int id; //field or data member
 float salary; //field or data member
 String name;//field or data member
 }
```

# C++ Object and Class Example

Let's see an example of class that has two fields: id and name. It creates instance of the class, initializes the object and prints the object value.

```cpp
#include <iostream>
using namespace std;
class Student {
public:
int id;//data member (also instance variable)
string name;//data member(also instance variable)
};
int main() {
Student s1; //creating an object of Student
s1.id = 201;
s1.name = "Sonoo Jaiswal";
cout<<s1.id<<endl;
cout<<s1.name<<endl;
return 0;
}
```

```
Output:

201
Sonoo Jaiswal
```

# C++ Class Example: Initialize and Display data through method

Let's see another example of C++ class where we are initializing and displaying object through method.

```cpp
#include <iostream>
using namespace std;
class Student {
 public:
 int id;//data member (also instance variable)
 string name;//data member(also instance variable)
 void insert(int i, string n)
 {
 id = i;
 name = n;
 }
 void display()
 {
 cout<<id<<" "<<name<<endl;
 }
};
int main(void) {
 Student s1; //creating an object of Student
 Student s2; //creating an object of Student
 s1.insert(201, "Sonoo");
 s2.insert(202, "Nakul");
 s1.display();
 s2.display();
 return 0;
}
```

```
Output:

201 Sonoo
202 Nakul
```

# C++ Class Example: Store and Display Employee Information

Let's see another example of C++ class where we are storing and displaying employee information using method.

```cpp
#include <iostream>
using namespace std;
class Employee {
 public:
 int id;//data member (also instance variable)
 string name;//data member(also instance variable)
 float salary;
 void insert(int i, string n, float s)
 {
 id = i;
 name = n;
 salary = s;
 }
 void display()
 {
 cout<<id<<" "<<name<<" "<<salary<<endl;
 }
};
int main(void) {
 Employee e1; //creating an object of Employee
 Employee e2; //creating an object of Employee
 e1.insert(201, "Sonoo",990000);
 e2.insert(202, "Nakul", 29000);
 e1.display();
 e2.display();
 return 0;
}
```

```
Output:

201 Sonoo 990000
202 Nakul 29000
```

<hr>

# C++ Constructor

In C++, constructor is a special method which is invoked automatically at the time of object creation. It is used to initialize the data members of new object generally. The constructor in C++ has the same name as class or structure.

There can be two types of constructors in C++.

- Default constructor
- Parameterized constructor

# C++ Default Constructor

A constructor which has no argument is known as default constructor. It is invoked at the time of creating object.

Let's see the simple example of C++ default Constructor.

```cpp
#include <iostream>
using namespace std;
class Employee
 {
 public:
 Employee()
 {
 cout<<"Default Constructor Invoked"<<endl;
 }
};
int main(void)
{
 Employee e1; //creating an object of Employee
 Employee e2;
 return 0;
}
```

```
Output:

Default Constructor Invoked
Default Constructor Invoked
```

# C++ Parameterized Constructor

A constructor which has parameters is called parameterized constructor. It is used to provide different values to distinct objects.

Let's see the simple example of C++ Parameterized Constructor.

```cpp
#include <iostream>
using namespace std;
class Employee {
public:
int id;//data member (also instance variable)
 string name;//data member(also instance variable)
float salary;
Employee(int i, string n, float s)
 {
 id = i;
 name = n;
 salary = s;
}
 void display()
 {
 cout<<id<<" "<<name<<" "<<salary<<endl;
 }
};
int main(void) {
Employee e1 =Employee(101, "Sonoo", 890000); //creating an object of Employee
Employee e2=Employee(102, "Nakul", 59000);
e1.display();
 e2.display();
 return 0;
}
```

```
Output:

101 Sonoo 890000
102 Nakul 59000
```

<hr>

# C++ Destructor

A destructor works opposite to constructor; it destructs the objects of classes. It can be defined only once in a class. Like constructors, it is invoked automatically.

A destructor is defined like constructor. It must have same name as class. But it is prefixed with a tilde sign (~).

### <b>Note: C++ destructor cannot have parameters. Moreover, modifiers can't be applied on destructors.</b>

# C++ Constructor and Destructor Example

Let's see an example of constructor and destructor in C++ which is called automatically.

```cpp
#include <iostream>
using namespace std;
class Employee
 {
 public:
 Employee()
 {
 cout<<"Constructor Invoked"<<endl;
 }
 ~Employee()
 {
 cout<<"Destructor Invoked"<<endl;
 }
};
int main(void)
{
 Employee e1; //creating an object of Employee
 Employee e2; //creating an object of Employee
 return 0;
}
```

```
Output:

Constructor Invoked
Constructor Invoked
Destructor Invoked
Destructor Invoked
```

<hr>

# C++ this Pointer

In C++ programming, this is a keyword that refers to the current instance of the class. There can be 3 main usage of this keyword in C++.

- It can be used to pass current object as a parameter to another method.
- It can be used to refer current class instance variable.
- It can be used to declare indexers.

# C++ this Pointer Example

Let's see the example of this keyword in C++ that refers to the fields of current class.

```cpp
#include <iostream>
using namespace std;
class Employee {
 public:
 int id; //data member (also instance variable)
 string name; //data member(also instance variable)
 float salary;
 Employee(int id, string name, float salary)
 {
 this->id = id;
 this->name = name;
 this->salary = salary;
 }
 void display()
 {
 cout<<id<<" "<<name<<" "<<salary<<endl;
 }
};
int main(void) {
 Employee e1 =Employee(101, "Sonoo", 890000); //creating an object of Employee
 Employee e2=Employee(102, "Nakul", 59000); //creating an object of Employee
 e1.display();
 e2.display();
 return 0;
}
```

```
Output:

101 Sonoo 890000
102 Nakul 59000
```

<hr>

# C++ static

In C++, static is a keyword or modifier that belongs to the type not instance. So instance is not required to access the static members. In C++, static can be field, method, constructor, class, properties, operator and event.

# Advantage of C++ static keyword

Memory efficient: Now we don't need to create instance for accessing the static members, so it saves memory. Moreover, it belongs to the type, so it will not get memory each time when instance is created.

# C++ Static Field

A field which is declared as static is called static field. Unlike instance field which gets memory each time whenever you create object, there is only one copy of static field created in the memory. It is shared to all the objects.

It is used to refer the common property of all objects such as rateOfInterest in case of Account, companyName in case of Employee etc.

# C++ static field example

Let's see the simple example of static field in C++.

```cpp
#include <iostream>
using namespace std;
class Account {
 public:
 int accno; //data member (also instance variable)
 string name; //data member(also instance variable)
 static float rateOfInterest;
 Account(int accno, string name)
 {
 this->accno = accno;
 this->name = name;
 }
 void display()
 {
 cout<<accno<< "<<name<< " "<<rateOfInterest<<endl;
 }
};
float Account::rateOfInterest=6.5;
int main(void) {
 Account a1 =Account(201, "Sanjay"); //creating an object of Employee
 Account a2=Account(202, "Nakul"); //creating an object of Employee
 a1.display();
 a2.display();
 return 0;
}
```

```
Output:

201 Sanjay 6.5
202 Nakul 6.5
```

# C++ static field example: Counting Objects

Let's see another example of static keyword in C++ which counts the objects.

```cpp
#include <iostream>
using namespace std;
class Account {
 public:
 int accno; //data member (also instance variable)
 string name;
 static int count;
 Account(int accno, string name)
 {
 this->accno = accno;
 this->name = name;
 count++;
 }
 void display()
 {
 cout<<accno<<" "<<name<<endl;
 }
};
int Account::count=0;
int main(void) {
 Account a1 =Account(201, "Sanjay"); //creating an object of Account
 Account a2=Account(202, "Nakul");
 Account a3=Account(203, "Ranjana");
 a1.display();
 a2.display();
 a3.display();
 cout<<"Total Objects are: "<<Account::count;
 return 0;
}
```

```
Output:

201 Sanjay
202 Nakul
203 Ranjana
Total Objects are: 3
```

<hr>

# C++ Structs

In C++, classes and structs are blueprints that are used to create the instance of a class. Structs are used for lightweight objects such as Rectangle, color, Point, etc.
Unlike class, structs in C++ are value type than reference type. It is useful if you have data that is not intended to be modified after creation of struct.
C++ Structure is a collection of different data types. It is similar to the class that holds different types of data.

## The Syntax Of Structure

```cpp
struct structure_name
{
 // member declarations.
}
```

In the above declaration, a structure is declared by preceding the struct keyword followed by the identifier(structure name). Inside the curly braces, we can declare the member variables of different types. Consider the following situation:

```cpp
struct Student
{
 char name[20];
 int id;
 int age;
}
```

In the above case, Student is a structure contains three variables name, id, and age. When the structure is declared, no memory is allocated. When the variable of a structure is created, then the memory is allocated. Let's understand this scenario.

## How to create the instance of Structure?

Structure variable can be defined as:

**Student s;**

Here, s is a structure variable of type Student. When the structure variable is created, the memory will be allocated. Student structure contains one char variable and two integer variable. Therefore, the memory for one char variable is 1 byte and two ints will be 2\*4 = 8. The total memory occupied by the s variable is 9 byte.

## How to access the variable of Structure:

The variable of the structure can be accessed by simply using the instance of the structure followed by the dot (.) operator and then the field of the structure.

For example:

**s.id = 4;**

In the above statement, we are accessing the id field of the structure Student by using the dot(.) operator and assigns the value 4 to the id field.

# C++ Struct Example

Let's see a simple example of struct Rectangle which has two data members width and height.

```cpp
#include <iostream>
using namespace std;
struct Rectangle
{
int width, height;

};
int main(void) {
struct Rectangle rec;
rec.width=8;
rec.height=5;
cout<<"Area of Rectangle is: "<<(rec.width \* rec.height)<<endl;
return 0;
}
```

```
Output:

Area of Rectangle is: 40
```

# C++ Struct Example: Using Constructor and Method

Let's see another example of struct where we are using the constructor to initialize data and method to calculate the area of rectangle.

```cpp
#include <iostream>
using namespace std;
struct Rectangle {
int width, height;
Rectangle(int w, int h)
{
width = w;
height = h;
}
void areaOfRectangle() {
cout<<"Area of Rectangle is: "<<(width\*height); }
};
int main(void) {
struct Rectangle rec=Rectangle(4,6);
rec.areaOfRectangle();
return 0;
}
```

```
Output:

Area of Rectangle is: 24
```

# Structure v/s Class

## Structure

- If access specifier is not declared explicitly, then by default access specifier will be public.
- Syntax of Structure:

```
struct structure_name
{
// body of the structure.
}
```

- The instance of the structure is known as "Structure variable".

## Class

- If access specifier is not declared explicitly, then by default access specifier will be private.
- Syntax of Class:

```
class class_name
{
// body of the class.
}
```

- The instance of the class is known as "Object of the class".

<hr>

# C++ Copy Constructor

A Copy constructor is an overloaded constructor used to declare and initialize an object from another object.

## Copy Constructor is of two types:

- Default Copy constructor: The compiler defines the default copy constructor. If the user defines no copy constructor, compiler supplies its constructor.
- User Defined constructor: The programmer defines the user-defined constructor.

## Syntax Of User-defined Copy Constructor:

Class_name(const class_name &old_object);  
Consider the following situation:

```cpp
class A
{
 A(A &x) // copy constructor.
 {
 // copyconstructor.
 }
}
```

In the above case, copy constructor can be called in the following ways:

- A a2(a1);
- A a2=a1;

Let's see a simple example of the copy constructor.

```cpp
// program of the copy constructor.

#include <iostream>
using namespace std;
class A
{
 public:
 int x;
 A(int a) // parameterized constructor.
 {
 x=a;
 }
 A(A &i) // copy constructor
 {
 x = i.x;
 }
};
int main()
{
 A a1(20); // Calling the parameterized constructor.
 A a2(a1); // Calling the copy constructor.
 cout<<a2.x;
 return 0;
}
```

```
Output:

20
```

# When Copy Constructor is called

Copy Constructor is called in the following scenarios:

- When we initialize the object with another existing object of the same class type. For example, Student s1 = s2, where Student is the class.
- When the object of the same class type is passed by value as an argument.
- When the function returns the object of the same class type by value.

# Two types of copies are produced by the constructor:

- Shallow copy
- Deep copy

## Shallow Copy

- The default copy constructor can only produce the shallow copy.
- A Shallow copy is defined as the process of creating the copy of an object by copying data of all the member variables as it is.

Let's understand this through a simple example:

```cpp
#include <iostream>

using namespace std;

class Demo
{
 int a;
 int b;
 int *p;
 public:
 Demo()
 {
 p=new int;
 }
 void setdata(int x,int y,int z)
 {
 a=x;
 b=y;
 *p=z;
 }
 void showdata()
 {
 std::cout << "value of a is : " <<a<< std::endl;
 std::cout << "value of b is : " <<b<< std::endl;
 std::cout << "value of *p is : " <<*p<< std::endl;
 }
};
int main()
{
 Demo d1;
 d1.setdata(4,5,7);
 Demo d2 = d1;
 d2.showdata();
 return 0;
}
```

```
Output:

value of a is : 4
value of b is : 5
value of \*p is : 7
```

In the above case, a programmer has not defined any constructor, therefore, the statement Demo d2 = d1; calls the default constructor defined by the compiler. The default constructor creates the exact copy or shallow copy of the existing object. Thus, the pointer p of both the objects point to the same memory location. Therefore, when the memory of a field is freed, the memory of another field is also automatically freed as both the fields point to the same memory location. This problem is solved by the user-defined constructor that creates the Deep copy.

## Deep copy

Deep copy dynamically allocates the memory for the copy and then copies the actual value, both the source and copy have distinct memory locations. In this way, both the source and copy are distinct and will not share the same memory location. Deep copy requires us to write the user-defined constructor.

Let's understand this through a simple example.

```cpp
#include <iostream>
using namespace std;
class Demo
{
 public:
 int a;
 int b;
 int \*p;

    Demo()
    {
        p=new int;
    }
    Demo(Demo &d)
    {
        a = d.a;
        b = d.b;
        p = new int;
        *p = *(d.p);
    }
    void setdata(int x,int y,int z)
    {
        a=x;
        b=y;
        *p=z;
    }
    void showdata()
    {
        std::cout << "value of a is : " <<a<< std::endl;
        std::cout << "value of b is : " <<b<< std::endl;
        std::cout << "value of *p is : " <<*p<< std::endl;
    }

};
int main()
{
 Demo d1;
 d1.setdata(4,5,7);
 Demo d2 = d1;
 d2.showdata();
 return 0;
}
```

```
Output:

value of a is : 4
value of b is : 5
value of \*p is : 7
```

In the above case, a programmer has defined its own constructor, therefore the statement Demo d2 = d1; calls the copy constructor defined by the user. It creates the exact copy of the value types data and the object pointed by the pointer p. Deep copy does not create the copy of a reference type variable.

# Differences b/w Copy constructor and Assignment operator(=)

## Copy Constructor

- It is an overloaded constructor.
- It initializes the new object with the existing object.
- Syntax of copy constructor:

```
Class_name(const class_name &object_name)
{
// body of the constructor.
}
```

- The copy constructor is invoked when the new object is initialized with the existing object.
- The object is passed as an argument to the function.
- It returns the object.
- Both the existing object and new object shares the different memory locations.
- If a programmer does not define the copy constructor, the compiler will automatically generate the implicit default copy constructor.

## Assignment Operator

- It is a bitwise operator.
- It assigns the value of one object to another object.
- Syntax of Assignment operator:

```
  Class_name a,b;
  b = a;
```

- The assignment operator is invoked when we assign the existing object to a new object.
- Both the existing object and new object shares the same memory location.
- If we do not overload the "=" operator, the bitwise copy will occur.

<hr>

# C++ Friend function

If a function is defined as a friend function in C++, then the protected and private data of a class can be accessed using the function.

By using the keyword friend compiler knows the given function is a friend function.

For accessing the data, the declaration of a friend function should be done inside the body of a class starting with the keyword friend.

# Declaration of friend function in C++

```cpp
class class_name
{
 friend data_type function_name(argument/s); // syntax of friend function.
};
```

In the above declaration, the friend function is preceded by the keyword friend. The function can be defined anywhere in the program like a normal C++ function. The function definition does not use either the keyword friend or scope resolution operator.

### Characteristics of a Friend function:

- The function is not in the scope of the class to which it has been declared as a friend.
- It cannot be called using the object as it is not in the scope of that class.
- It can be invoked like a normal function without using the object.
- It cannot access the member names directly and has to use an object name and dot membership operator with the member name.
- It can be declared either in the private or the public part.

# C++ friend function Example

Let's see the simple example of C++ friend function used to print the length of a box.

```cpp
#include <iostream>
using namespace std;
class Box
{
 private:
 int length;
 public:
 Box(): length(0) { }
 friend int printLength(Box); //friend function
};
int printLength(Box b)
{
 b.length += 10;
 return b.length;
}
int main()
{
 Box b;
 cout<<"Length of box: "<< printLength(b)<<endl;
 return 0;
}
```

```
Output:

Length of box: 10
```

Let's see a simple example when the function is friendly to two classes.

```cpp
#include <iostream>
using namespace std;
class B; // forward declarartion.
class A
{
 int x;
 public:
 void setdata(int i)
 {
 x=i;
 }
 friend void min(A,B); // friend function.
};
class B
{
 int y;
 public:
 void setdata(int i)
 {
 y=i;
 }
 friend void min(A,B); // friend function
};
void min(A a,B b)
{
 if(a.x<=b.y)
 std::cout << a.x << std::endl;
 else
 std::cout << b.y << std::endl;
}
 int main()
{
 A a;
 B b;
 a.setdata(10);
 b.setdata(20);
 min(a,b);
 return 0;
 }
```

```
Output:

10
```

In the above example, min() function is friendly to two classes, i.e., the min() function can access the private members of both the classes A and B.

# C++ Friend class

A friend class can access both private and protected members of the class in which it has been declared as friend.

Let's see a simple example of a friend class.

```cpp
#include <iostream>

using namespace std;

class A
{
 int x =5;
 friend class B; // friend class.
};
class B
{
 public:
 void display(A &a)
 {
 cout<<"value of x is : "<<a.x;
 }
};
int main()
{
 A a;
 B b;
 b.display(a);
 return 0;
}
```

```
Output:

value of x is : 5
```

In the above example, class B is declared as a friend inside the class A. Therefore, B is a friend of class A. Class B can access the private members of class A.

<hr>

# C++ Inheritance

In C++, inheritance is a process in which one object acquires all the properties and behaviors of its parent object automatically. In such way, you can reuse, extend or modify the attributes and behaviors which are defined in other class.

In C++, the class which inherits the members of another class is called derived class and the class whose members are inherited is called base class. The derived class is the specialized class for the base class.

# Advantage of C++ Inheritance

Code reusability: Now you can reuse the members of your parent class. So, there is no need to define the member again. So less code is required in the class.

## Types Of Inheritance

**C++ supports five types of inheritance:**

- Single inheritance
- Multiple inheritance
- Hierarchical inheritance
- Multilevel inheritance
- Hybrid inheritance

## Derived Classes

A Derived class is defined as the class derived from the base class.

The Syntax of Derived class:

```cpp
class derived_class_name :: visibility-mode base_class_name
{
 // body of the derived class.
}
```

Where,

**derived_class_name:** It is the name of the derived class.

**visibility mode:** The visibility mode specifies whether the features of the base class are publicly inherited or privately inherited. It can be public or private.

**base_class_name:** It is the name of the base class.

- When the base class is privately inherited by the derived class, public members of the base class becomes the private members of the derived class. Therefore, the public members of the base class are not accessible by the objects of the derived class only by the member functions of the derived class.
- When the base class is publicly inherited by the derived class, public members of the base class also become the public members of the derived class. Therefore, the public members of the base class are accessible by the objects of the derived class as well as by the member functions of the base class.
  **Note:**
- In C++, the default mode of visibility is private.
- The private members of the base class are never inherited.

# C++ Single Inheritance

Single inheritance is defined as the inheritance in which a derived class is inherited from the only one base class.
A->B
Where 'A' is the base class, and 'B' is the derived class.

# C++ Single Level Inheritance Example: Inheriting Fields

When one class inherits another class, it is known as single level inheritance. Let's see the example of single level inheritance which inherits the fields only.

```cpp
#include <iostream>
using namespace std;
 class Account {
 public:
 float salary = 60000;
 };
 class Programmer: public Account {
 public:
 float bonus = 5000;
 };
int main(void) {
 Programmer p1;
 cout<<"Salary: "<<p1.salary<<endl;
 cout<<"Bonus: "<<p1.bonus<<endl;
 return 0;
}
```

```
Output:

Salary: 60000
Bonus: 5000
```

In the above example, Employee is the base class and Programmer is the derived class.

# C++ Single Level Inheritance Example: Inheriting Methods

Let's see another example of inheritance in C++ which inherits methods only.

```cpp
#include <iostream>
using namespace std;
 class Animal {
 public:
 void eat() {
 cout<<"Eating..."<<endl;
 }
 };
 class Dog: public Animal
 {
 public:
 void bark(){
 cout<<"Barking...";
 }
 };
int main(void) {
 Dog d1;
 d1.eat();
 d1.bark();
 return 0;
}
```

```
Output:

Eating...
Barking...
```

Let's see a simple example.

```cpp
#include <iostream>
using namespace std;
class A
{
 int a = 4;
 int b = 5;
 public:
 int mul()
 {
 int c = a\*b;
 return c;
 }
};

class B : private A
{
 public:
 void display()
 {
 int result = mul();
 std::cout <<"Multiplication of a and b is : "<<result<< std::endl;
 }
};
int main()
{
 B b;
 b.display();

    return 0;

}
```

```
Output:

Multiplication of a and b is : 20
```

In the above example, class A is privately inherited. Therefore, the mul() function of class 'A' cannot be accessed by the object of class B. It can only be accessed by the member function of class B.

## How to make a Private Member Inheritable

The private member is not inheritable. If we modify the visibility mode by making it public, but this takes away the advantage of data hiding.

C++ introduces a third visibility modifier, i.e., protected. The member which is declared as protected will be accessible to all the member functions within the class as well as the class immediately derived from it.

## Visibility modes can be classified into three categories:

- Public: When the member is declared as public, it is accessible to all the functions of the program.
- Private: When the member is declared as private, it is accessible within the class only.
- Protected: When the member is declared as protected, it is accessible within its own class as well as the class immediately derived from it.

## Visibility of Inherited Members

![image](https://user-images.githubusercontent.com/59651136/141831795-a2961422-6c9a-4931-abf6-463af52ac10f.png)

## C++ Multilevel Inheritance

Multilevel inheritance is a process of deriving a class from another derived class.
A->B->C
Where 'A' is the base class, 'B' is the derived class and 'C' is the derived class of 'B'.

## C++ Multi Level Inheritance Example

When one class inherits another class which is further inherited by another class, it is known as multi level inheritance in C++. Inheritance is transitive so the last derived class acquires all the members of all its base classes.

Let's see the example of multi level inheritance in C++.

```cpp
#include <iostream>
using namespace std;
 class Animal {
 public:
 void eat() {
 cout<<"Eating..."<<endl;
 }
 };
 class Dog: public Animal
 {
 public:
 void bark(){
 cout<<"Barking..."<<endl;
 }
 };
 class BabyDog: public Dog
 {
 public:
 void weep() {
 cout<<"Weeping...";
 }
 };
int main(void) {
 BabyDog d1;
 d1.eat();
 d1.bark();
 d1.weep();
 return 0;
}
```

```
Output:

Eating...
Barking...
Weeping...
```

## C++ Multiple Inheritance

![image](https://user-images.githubusercontent.com/59651136/141832170-e1a47b5c-4796-4f2b-97d4-b1cd79eced44.png)

**Multiple inheritance** is the process of deriving a new class that inherits the attributes from two or more classes.

**Syntax of the Derived class:**

```cpp
class D : visibility B-1, visibility B-2, ?
{
 // Body of the class;
}
```

Let's see a simple example of multiple inheritance.

```cpp
#include <iostream>
using namespace std;
class A
{
 protected:
 int a;
 public:
 void get_a(int n)
 {
 a = n;
 }
};

class B
{
 protected:
 int b;
 public:
 void get_b(int n)
 {
 b = n;
 }
};
class C : public A,public B
{
 public:
 void display()
 {
 std::cout << "The value of a is : " <<a<< std::endl;
 std::cout << "The value of b is : " <<b<< std::endl;
 cout<<"Addition of a and b is : "<<a+b;
 }
};
int main()
{
 C c;
 c.get_a(10);
 c.get_b(20);
 c.display();

    return 0;

}
```

```
Output:

The value of a is : 10
The value of b is : 20
Addition of a and b is : 30
```

In the above example, class 'C' inherits two base classes 'A' and 'B' in a public mode.

# Ambiquity Resolution in Inheritance

Ambiguity can be occurred in using the multiple inheritance when a function with the same name occurs in more than one base class.

Let's understand this through an example:

```cpp
#include <iostream>
using namespace std;
class A
{
 public:
 void display()
 {
 std::cout << "Class A" << std::endl;
 }
};
class B
{
 public:
 void display()
 {
 std::cout << "Class B" << std::endl;
 }
};
class C : public A, public B
{
 void view()
 {
 display();
 }
};
int main()
{
 C c;
 c.display();
 return 0;
}
```

```
Output:

error: reference to 'display' is ambiguous
display();
```

The above issue can be resolved by using the class resolution operator with the function. In the above example, the derived class code can be rewritten as:

```cpp
class C : public A, public B
{
 void view()
 {
 A :: display(); // Calling the display() function of class A.
 B :: display(); // Calling the display() function of class B.

    }

};
```

An ambiguity can also occur in single inheritance.

Consider the following situation:

```cpp
class A
{
 public:
void display()
{
 cout<<?Class A?;
}
} ;
class B
{
 public:
 void display()
{
 cout<<?Class B?;
}
} ;
```

In the above case, the function of the derived class overrides the method of the base class. Therefore, call to the display() function will simply call the function defined in the derived class. If we want to invoke the base class function, we can use the class resolution operator.

```cpp
int main()
{
 B b;
 b.display(); // Calling the display() function of B class.
 b.B :: display(); // Calling the display() function defined in B class.
}
```

# C++ Hybrid Inheritance

Hybrid inheritance is a combination of more than one type of inheritance.
![image](https://user-images.githubusercontent.com/59651136/141908780-ad021bd8-b45f-46c6-b89c-d4ba250bcbe4.png)

Let's see a simple example:

```cpp
#include <iostream>
using namespace std;
class A
{
 protected:
 int a;
 public:
 void get_a()
 {
 std::cout << "Enter the value of 'a' : " << std::endl;
 cin>>a;
 }
};

class B : public A
{
 protected:
 int b;
 public:
 void get_b()
 {
 std::cout << "Enter the value of 'b' : " << std::endl;
 cin>>b;
 }
};
class C
{
 protected:
 int c;
 public:
 void get_c()
 {
 std::cout << "Enter the value of c is : " << std::endl;
 cin>>c;
 }
};

class D : public B, public C
{
 protected:
 int d;
 public:
 void mul()
 {
 get_a();
 get_b();
 get_c();
 std::cout << "Multiplication of a,b,c is : " <<a*b*c<< std::endl;
 }
};
int main()
{
 D d;
 d.mul();
 return 0;
}
```

```
Output:

Enter the value of 'a' :
10
Enter the value of 'b' :
20
Enter the value of c is :
30
Multiplication of a,b,c is : 6000
```

# C++ Hierarchical Inheritance

Hierarchical inheritance is defined as the process of deriving more than one class from a base class.
![image](https://user-images.githubusercontent.com/59651136/141909381-f6755ad2-19d5-4c74-986f-c86b9b81986f.png)
Syntax of Hierarchical inheritance:

```cpp
class A
{
 // body of the class A.
}
class B : public A
{
 // body of class B.
}
class C : public A
{
 // body of class C.
}
class D : public A
{
 // body of class D.
}
```

Let's see a simple example:

```cpp
#include <iostream>
using namespace std;
class Shape // Declaration of base class.
{
 public:
 int a;
 int b;
 void get_data(int n,int m)
 {
 a= n;
 b = m;
 }
};
class Rectangle : public Shape // inheriting Shape class
{
 public:
 int rect_area()
 {
 int result = a*b;
 return result;
 }
};
class Triangle : public Shape // inheriting Shape class
{
 public:
 int triangle_area()
 {
 float result = 0.5*a\*b;
 return result;
 }
};
int main()
{
 Rectangle r;
 Triangle t;
 int length,breadth,base,height;
 std::cout << "Enter the length and breadth of a rectangle: " << std::endl;
 cin>>length>>breadth;
 r.get_data(length,breadth);
 int m = r.rect_area();
 std::cout << "Area of the rectangle is : " <<m<< std::endl;
 std::cout << "Enter the base and height of the triangle: " << std::endl;
 cin>>base>>height;
 t.get_data(base,height);
 float n = t.triangle_area();
 std::cout <<"Area of the triangle is : " << n<<std::endl;
 return 0;
}
```

```
Output:

Enter the length and breadth of a rectangle:
23
20
Area of the rectangle is : 460
Enter the base and height of the triangle:
2
5
Area of the triangle is : 5
```

<hr>

# C++ Polymorphism

The term "Polymorphism" is the combination of "poly" + "morphs" which means many forms. It is a greek word. In object-oriented programming, we use 3 main concepts: inheritance, encapsulation, and polymorphism.

# Real Life Example Of Polymorphism

Let's consider a real-life example of polymorphism. A lady behaves like a teacher in a classroom, mother or daughter in a home and customer in a market. Here, a single person is behaving differently according to the situations.

There are two types of polymorphism in C++:
![image](https://user-images.githubusercontent.com/59651136/141919603-823869af-e2a3-4162-91ee-06b8105819da.png)

- Compile time polymorphism: The overloaded functions are invoked by matching the type and number of arguments. This information is available at the compile time and, therefore, compiler selects the appropriate function at the compile time. It is achieved by function overloading and operator overloading which is also known as static binding or early binding. Now, let's consider the case where function name and prototype is same.

```cpp
class A // base class declaration.
 {
 int a;
 public:
 void display()
 {
 cout<< "Class A ";
 }
 };
class B : public A // derived class declaration.
{
 int b;
 public:
 void display()
 {
 cout<<"Class B";
 }
};
```

In the above case, the prototype of display() function is the same in both the base and derived class. Therefore, the static binding cannot be applied. It would be great if the appropriate function is selected at the run time. This is known as run time polymorphism.

- Run time polymorphism: Run time polymorphism is achieved when the object's method is invoked at the run time instead of compile time. It is achieved by method overriding which is also known as dynamic binding or late binding.

# Differences b/w compile time and run time polymorphism.

### Compile time polymorphism

- The function to be invoked is known at the compile time.
- It is also known as overloading, early binding and static binding.
- Overloading is a compile time polymorphism where more than one method is having the same name but with the different number of parameters or the type of the parameters.
- It is achieved by function overloading and operator overloading.
- It provides fast execution as it is known at the compile time.
- It is less flexible as mainly all the things execute at the compile time.

### Run time polymorphism

- The function to be invoked is known at the run time.
- It is also known as overriding, Dynamic binding and late binding.
- Overriding is a run time polymorphism where more than one method is having the same name, number of parameters and the type of the parameters.
- It is achieved by virtual functions and pointers.
- It provides slow execution as it is known at the run time.
- It is more flexible as all the things execute at the run time.

# C++ Runtime Polymorphism Example

Let's see a simple example of run time polymorphism in C++.

```cpp
// an example without the virtual keyword.

#include <iostream>
using namespace std;
class Animal {
 public:
void eat(){
cout<<"Eating...";
 }
};
class Dog: public Animal
{
 public:
 void eat()
 { cout<<"Eating bread...";
 }
};
int main(void) {
 Dog d = Dog();
 d.eat();
 return 0;
}
```

```
Output:

Eating bread...
```

# C++ Run time Polymorphism Example: By using two derived class

Let's see another example of run time polymorphism in C++ where we are having two derived classes.

```cpp
// an example with virtual keyword.

#include <iostream>
using namespace std;
class Shape { // base class
 public:
virtual void draw(){ // virtual function
cout<<"drawing..."<<endl;
 }
};
class Rectangle: public Shape // inheriting Shape class.
{
 public:
 void draw()
 {
 cout<<"drawing rectangle..."<<endl;
 }
};
class Circle: public Shape // inheriting Shape class.

{
 public:
 void draw()
 {
 cout<<"drawing circle..."<<endl;
 }
};
int main(void) {
 Shape \*s; // base class pointer.
 Shape sh; // base class object.
 Rectangle rec;
 Circle cir;
 s=&sh;
 s->draw();
 s=&rec;
 s->draw();
 s=?
 s->draw();
}
```

```
Output:

drawing...
drawing rectangle...
drawing circle...
```

# Runtime Polymorphism with Data Members

Runtime Polymorphism can be achieved by data members in C++. Let's see an example where we are accessing the field by reference variable which refers to the instance of derived class.

```cpp
#include <iostream>
using namespace std;
class Animal { // base class declaration.
 public:
 string color = "Black";
};
class Dog: public Animal // inheriting Animal class.
{
 public:
 string color = "Grey";
};
int main(void) {
 Animal d= Dog();
 cout<<d.color;
}
```

```
Output:

Black
```

<hr>

# C++ Overloading (Function and Operator)

If we create two or more members having the same name but different in number or type of parameter, it is known as C++ overloading. In C++, we can overload:

- methods,
- constructors, and
- indexed properties
  It is because these members have parameters only.

## Types of overloading in C++ are:

- Function overloading
- Operator overloading

## C++ Function Overloading

Function Overloading is defined as the process of having two or more function with the same name, but different in parameters is known as function overloading in C++. In function overloading, the function is redefined by using either different types of arguments or a different number of arguments. It is only through these differences compiler can differentiate between the functions.

The advantage of Function overloading is that it increases the readability of the program because you don't need to use different names for the same action.

# C++ Function Overloading Example

Let's see the simple example of function overloading where we are changing number of arguments of add() method.

// program of function overloading when number of arguments vary.

```cpp
#include <iostream>
using namespace std;
class Cal {
 public:
static int add(int a,int b){
 return a + b;
 }
static int add(int a, int b, int c)
 {
 return a + b + c;
 }
};
int main(void) {
 Cal C; // class object declaration.
 cout<<C.add(10, 20)<<endl;
 cout<<C.add(12, 20, 23);
 return 0;
}
```

```
Output:

30
55
```

Let's see the simple example when the type of the arguments vary.

```cpp
// Program of function overloading with different types of arguments.

#include<iostream>
using namespace std;
int mul(int,int);
float mul(float,int);

int mul(int a,int b)
{
 return a*b;
}
float mul(double x, int y)
{
 return x*y;
}
int main()
{
 int r1 = mul(6,7);
 float r2 = mul(0.2,3);
 std::cout << "r1 is : " <<r1<< std::endl;
 std::cout <<"r2 is : " <<r2<< std::endl;
 return 0;
}
```

```
Output:

r1 is : 42
r2 is : 0.6
```

## Function Overloading and Ambiguity

When the compiler is unable to decide which function is to be invoked among the overloaded function, this situation is known as function overloading.

When the compiler shows the ambiguity error, the compiler does not run the program.

Causes of Function Overloading:

- Type Conversion.
- Function with default arguments.
- Function with pass by reference.
- Type Conversion:
  Let's see a simple example.

```cpp
#include<iostream>
using namespace std;
void fun(int);
void fun(float);
void fun(int i)
{
 std::cout << "Value of i is : " <<i<< std::endl;
}
void fun(float j)
{
 std::cout << "Value of j is : " <<j<< std::endl;
}
int main()
{
 fun(12);
 fun(1.2);
 return 0;
}
```

The above example shows an error "call of overloaded 'fun(double)' is ambiguous". The fun(10) will call the first function. The fun(1.2) calls the second function according to our prediction. But, this does not refer to any function as in C++, all the floating point constants are treated as double not as a float. If we replace float to double, the program works. Therefore, this is a type conversion from float to double.

- Function with Default Arguments

Let's see a simple example.

```cpp
#include<iostream>
using namespace std;
void fun(int);
void fun(int,int);
void fun(int i)
{
 std::cout << "Value of i is : " <<i<< std::endl;
}
void fun(int a,int b=9)
{
 std::cout << "Value of a is : " <<a<< std::endl;
 std::cout << "Value of b is : " <<b<< std::endl;
}
int main()
{
 fun(12);

    return 0;

}
```

The above example shows an error "call of overloaded 'fun(int)' is ambiguous". The fun(int a, int b=9) can be called in two ways: first is by calling the function with one argument, i.e., fun(12) and another way is calling the function with two arguments, i.e., fun(4,5). The fun(int i) function is invoked with one argument. Therefore, the compiler could not be able to select among fun(int i) and fun(int a,int b=9).

- Function with pass by reference

Let's see a simple example.

```cpp
#include <iostream>
using namespace std;
void fun(int);
void fun(int &);
int main()
{
int a=10;
fun(a); // error, which f()?
return 0;
}
void fun(int x)
{
std::cout << "Value of x is : " <<x<< std::endl;
}
void fun(int &b)
{
std::cout << "Value of b is : " <<b<< std::endl;
}
```

The above example shows an error "call of overloaded 'fun(int&)' is ambiguous". The first function takes one integer argument and the second function takes a reference parameter as an argument. In this case, the compiler does not know which function is needed by the user as there is no syntactical difference between the fun(int) and fun(int &).

## C++ Operators Overloading

Operator overloading is a compile-time polymorphism in which the operator is overloaded to provide the special meaning to the user-defined data type. Operator overloading is used to overload or redefines most of the operators available in C++. It is used to perform the operation on the user-defined data type. For example, C++ provides the ability to add the variables of the user-defined data type that is applied to the built-in data types.

The advantage of Operators overloading is to perform different operations on the same operand.

Operator that cannot be overloaded are as follows:

- Scope operator (::)
- Sizeof
- member selector(.)
- member pointer selector(\*)
- ternary operator(?:)

## Syntax of Operator Overloading

```cpp
return_type class_name : : operator op(argument_list)
{
 // body of the function.
}
```

Where the **return type** is the type of value returned by the function.

**class_name** is the name of the class.

**operator op** is an operator function where op is the operator being overloaded, and the operator is the keyword.

## Rules for Operator Overloading

- Existing operators can only be overloaded, but the new operators cannot be overloaded.
- The overloaded operator contains atleast one operand of the user-defined data type.
- We cannot use friend function to overload certain operators. However, the member function can be used to overload those operators.
- When unary operators are overloaded through a member function take no explicit arguments, but, if they are overloaded by a friend function, takes one argument.
- When binary operators are overloaded through a member function takes one explicit argument, and if they are overloaded through a friend function takes two explicit arguments.

# C++ Operators Overloading Example

Let's see the simple example of operator overloading in C++. In this example, void operator ++ () operator function is defined (inside Test class).

```cpp
// program to overload the unary operator ++.

#include <iostream>
using namespace std;
class Test
{
 private:
 int num;
 public:
 Test(): num(8){}
 void operator ++() {
 num = num+2;
 }
 void Print() {
 cout<<"The Count is: "<<num;
 }
};
int main()
{
 Test tt;
 ++tt; // calling of a function "void operator ++()"
 tt.Print();
 return 0;
}
```

```
Output:

The Count is: 10
```

Let's see a simple example of overloading the binary operators.

```cpp
// program to overload the binary operators.

#include <iostream>
using namespace std;
class A
{

    int x;
      public:
      A(){}
    A(int i)
    {
       x=i;
    }
    void operator+(A);
    void display();

};

void A :: operator+(A a)
{

    int m = x+a.x;
    cout<<"The result of the addition of two objects is : "<<m;

}
int main()
{
 A a1(5);
 A a2(4);
 a1+a2;
 return 0;
}
```

```
Output:

The result of the addition of two objects is : 9
```

<hr>

# C++ Function Overriding

If derived class defines same function as defined in its base class, it is known as function overriding in C++. It is used to achieve runtime polymorphism. It enables you to provide specific implementation of the function which is already provided by its base class.

# C++ Function Overriding Example

Let's see a simple example of Function overriding in C++. In this example, we are overriding the eat() function.

```cpp
#include <iostream>
using namespace std;
class Animal {
    public:
void eat(){
cout<<"Eating...";
    }
};
class Dog: public Animal
{
 public:
 void eat()
    {
       cout<<"Eating bread...";
    }
};
int main(void) {
   Dog d = Dog();
   d.eat();
   return 0;
}
```

```
Output:

Eating bread...
```

<hr>

# C++ virtual function

- A C++ virtual function is a member function in the base class that you redefine in a derived class. It is declared using the virtual keyword.
- It is used to tell the compiler to perform dynamic linkage or late binding on the function.
- There is a necessity to use the single pointer to refer to all the objects of the different classes. So, we create the pointer to the base class that refers to all the derived objects. But, when base class pointer contains the address of the derived class object, always executes the base class function. This issue can only be resolved by using the 'virtual' function.
- A 'virtual' is a keyword preceding the normal declaration of a function.
  -When the function is made virtual, C++ determines which function is to be invoked at the runtime based on the type of the object pointed by the base class pointer.

# Late binding or Dynamic linkage

In late binding function call is resolved during runtime. Therefore compiler determines the type of object at runtime, and then binds the function call.

### Rules of Virtual Function

- Virtual functions must be members of some class.
- Virtual functions cannot be static members.
- They are accessed through object pointers.
- They can be a friend of another class.
- A virtual function must be defined in the base class, even though it is not used.
- The prototypes of a virtual function of the base class and all the derived classes must be identical. If the two functions with the same name but different prototypes, C++ will consider them as the overloaded functions.
- We cannot have a virtual constructor, but we can have a virtual destructor
- Consider the situation when we don't use the virtual keyword.

```cpp
#include <iostream>
using namespace std;
class A
{
 int x=5;
 public:
 void display()
 {
 std::cout << "Value of x is : " << x<<std::endl;
 }
};
class B: public A
{
 int y = 10;
 public:
 void display()
 {
 std::cout << "Value of y is : " <<y<< std::endl;
 }
};
int main()
{
 A \*a;
 B b;
 a = &b;
 a->display();
 return 0;
}
```

```
Output:

Value of x is : 5
```

In the above example, \* a is the base class pointer. The pointer can only access the base class members but not the members of the derived class. Although C++ permits the base pointer to point to any object derived from the base class, it cannot directly access the members of the derived class. Therefore, there is a need for virtual function which allows the base pointer to access the members of the derived class.

## C++ virtual function Example

Let's see the simple example of C++ virtual function used to invoked the derived class in a program.

```cpp
#include <iostream>
{
 public:
 virtual void display()
 {
 cout << "Base class is invoked"<<endl;
 }
};
class B:public A
{
 public:
 void display()
 {
 cout << "Derived Class is invoked"<<endl;
 }
};
int main()
{
 A\* a; //pointer of base class
 B b; //object of derived class
 a = &b;
 a->display(); //Late Binding occurs
}
```

```
Output:

Derived Class is invoked
```

# Pure Virtual Function

- A virtual function is not used for performing any task. It only serves as a placeholder.
- When the function has no definition, such function is known as "do-nothing" function.
- The "do-nothing" function is known as a pure virtual function. A pure virtual function is a function declared in the base class that has no definition relative to the base class.
- A class containing the pure virtual function cannot be used to declare the objects of its own, such classes are known as abstract base classes.
- The main objective of the base class is to provide the traits to the derived classes and to create the base pointer used for achieving the runtime polymorphism.

**Pure virtual function can be defined as:**

```virtual void display() = 0; ````
Let's see a simple example:

```cpp
#include <iostream>
using namespace std;
class Base
{
 public:
 virtual void show() = 0;
};
class Derived : public Base
{
 public:
 void show()
 {
 std::cout << "Derived class is derived from the base class." << std::endl;
 }
};
int main()
{
 Base \*bptr;
 //Base b;
 Derived d;
 bptr = &d;
 bptr->show();
 return 0;
}
```

```
Output:

Derived class is derived from the base class.
```

In the above example, the base class contains the pure virtual function. Therefore, the base class is an abstract base class. We cannot create the object of the base class.
